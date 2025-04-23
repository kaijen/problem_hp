Vielen Dank für die ausführliche Ausgabe. Die entscheidenden Hinweise sind am Ende:

```
[   10.084587] resource: resource sanity check: requesting [mem 0x00000000000c0000-0x00000000000dffff], which spans more than PCI Bus 0000:00 [mem 0x000c0000-0x000cbfff window]
[   10.084594] caller pci_map_rom+0x6c/0x1d0 mapping multiple BARs
[   10.084614] amdgpu 0000:04:00.0: Invalid PCI ROM header signature: expecting 0xaa55, got 0xffff
```

---

### Interpretation

1. **`pci_map_rom` schlägt fehl**, weil der Treiber einen **ROM-Bereich außerhalb des erlaubten Speicherbereichs anfordert**. Das ist ein **klassisches Ressourcen-/Mapping-Problem** auf BIOS/UEFI- oder Kernel-Ebene.
2. Die Speicherregion `[mem 0x000c0000-0x000dffff]` ist der klassische **Legacy-Option-ROM-Bereich** für PCI-Geräte – hier soll das VBIOS der GPU liegen.
3. Das BIOS oder der Kernel stellt diesen Bereich aber **nicht vollständig bereit** (nur bis `0x000cbfff`), daher schlägt das Mapping fehl, und der Treiber erhält nur `0xFFFF` statt einer gültigen Signatur.

---

### Ursachen

- Timing-/Initialisierungsproblem bei der Bereitstellung des ROM BAR
- BIOS reserviert nicht ausreichend Speicher
- Kernel stellt zu früh oder zu spät darauf zu
- Option-ROM der iGPU ist **nur manchmal** verfügbar (u. U. wegen Stromsparmechanismen oder fehlerhafter ACPI-Implementierung)

---

### Empfohlene Maßnahmen (nach Wichtigkeit sortiert)

#### ✅ 1. **Kernelparameter `pci=nocrs` setzen**

Dieser Parameter **ignoriert restriktive ACPI-Ressourcenzuweisungen** (CRS = Current Resource Settings) und erlaubt dem Kernel, mehr Speicherbereiche für PCIe-Geräte zu nutzen.

In `/etc/default/grub`:
```bash
GRUB_CMDLINE_LINUX_DEFAULT="quiet splash pci=nocrs"
```

Dann:
```bash
sudo update-grub
sudo reboot
```

#### ✅ 2. **Alternativen testen**

Falls `pci=nocrs` allein nicht hilft, zusätzlich probieren:

- `pci=nocrs pci=assign-busses`
- `pci=nocrs acpi=off` (nur testweise!)
- `pci=nocrs pci=realloc` (kann Ressourcen neu verteilen)

Immer nur **ein zusätzliches Argument gleichzeitig** testen.

---

### Debug-Tipp

Wenn Du den Erfolg systematisch beobachten willst, kann ein Mini-Skript beim Bootvorgang prüfen, ob `amdgpu` geladen wurde und ob der VBIOS-Zugriff erfolgreich war.

Beispiel:

```bash
#!/bin/bash
if dmesg | grep -q 'amdgpu.*ATOM BIOS'; then
    echo "✅ VBIOS geladen"
else
    echo "❌ VBIOS fehlt"
fi
```

---

### Fazit

Der Fehler entsteht eindeutig durch eine **fehlerhafte oder zu restriktive Speicherzuweisung** beim Initialisieren des PCI-ROMs.  
Der Parameter `pci=nocrs` ist der **empfohlene erste Schritt**, um dieses Problem zu umgehen.

Wenn Du möchtest, kann ich Dir auch ein Bash-Skript zum systematischen Durchprobieren und Testen der Parameterkombinationen generieren.
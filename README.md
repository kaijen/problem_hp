## Erfolgreicher Boot (sehr selten):

Ausgabe von `journalctl -b | grep amdgpu`:

```
Apr 23 15:01:55 manul kernel: [drm] amdgpu kernel modesetting enabled.
Apr 23 15:01:55 manul kernel: amdgpu: Virtual CRAT table created for CPU
Apr 23 15:01:55 manul kernel: amdgpu: Topology: Add CPU node
Apr 23 15:01:55 manul kernel: amdgpu 0000:04:00.0: amdgpu: Fetched VBIOS from ROM BAR
Apr 23 15:01:56 manul kernel: amdgpu: ATOM BIOS: SWBRT48929.001
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: vgaarb: deactivate vga console
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: Trusted Memory Zone (TMZ) feature enabled
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: VRAM: 2048M 0x000000F400000000 - 0x000000F47FFFFFFF (2048M used)
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: GART: 1024M 0x0000000000000000 - 0x000000003FFFFFFF
Apr 23 15:01:56 manul kernel: [drm] amdgpu: 2048M of VRAM memory ready
Apr 23 15:01:56 manul kernel: [drm] amdgpu: 2913M of GTT memory ready.
Apr 23 15:01:56 manul kernel: amdgpu: hwmgr_sw_init smu backed is smu10_smu
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: reserve 0x400000 from 0xf47fc00000 for PSP TMR
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: RAS: optional ras ta ucode is not available
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: RAP: optional rap ta ucode is not available
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: psp gfx command LOAD_TA(0x1) failed and response status is (0x7)
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: psp gfx command INVOKE_CMD(0x3) failed and response status is (0x4)
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: Secure display: Generic Failure.
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: SECUREDISPLAY: query securedisplay TA failed. ret 0x0
Apr 23 15:01:56 manul kernel: snd_hda_intel 0000:04:00.1: bound 0000:04:00.0 (ops amdgpu_dm_audio_component_bind_ops [amdgpu])
Apr 23 15:01:56 manul kernel: kfd kfd: amdgpu: Allocated 3969056 bytes on gart
Apr 23 15:01:56 manul kernel: kfd kfd: amdgpu: Total number of KFD nodes to be created: 1
Apr 23 15:01:56 manul kernel: amdgpu: Virtual CRAT table created for GPU
Apr 23 15:01:56 manul kernel: amdgpu: Topology: Add dGPU node [0x15d8:0x1002]
Apr 23 15:01:56 manul kernel: kfd kfd: amdgpu: added device 1002:15d8
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: SE 1, SH per SE 1, CU per SH 11, active_cu_number 6
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring gfx uses VM inv eng 0 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.0.0 uses VM inv eng 1 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.1.0 uses VM inv eng 4 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.2.0 uses VM inv eng 5 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.3.0 uses VM inv eng 6 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.0.1 uses VM inv eng 7 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.1.1 uses VM inv eng 8 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.2.1 uses VM inv eng 9 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring comp_1.3.1 uses VM inv eng 10 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring kiq_0.2.1.0 uses VM inv eng 11 on hub 0
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring sdma0 uses VM inv eng 0 on hub 8
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring vcn_dec uses VM inv eng 1 on hub 8
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring vcn_enc0 uses VM inv eng 4 on hub 8
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring vcn_enc1 uses VM inv eng 5 on hub 8
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: ring jpeg_dec uses VM inv eng 6 on hub 8
Apr 23 15:01:56 manul kernel: amdgpu: pp_dpm_get_sclk_od was not implemented.
Apr 23 15:01:56 manul kernel: amdgpu: pp_dpm_get_mclk_od was not implemented.
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: amdgpu: Runtime PM not available
Apr 23 15:01:56 manul kernel: [drm] Initialized amdgpu 3.59.0 for 0000:04:00.0 on minor 1
Apr 23 15:01:56 manul kernel: fbcon: amdgpudrmfb (fb0) is primary device
Apr 23 15:01:56 manul kernel: amdgpu 0000:04:00.0: [drm] fb0: amdgpudrmfb frame buffer device
Apr 23 15:01:56 manul systemd[1]: Starting systemd-backlight@backlight:amdgpu_bl1.service - Load/Save Screen Backlight Brightness of backlight:amdgpu_bl1...
Apr 23 15:01:56 manul systemd[1]: Finished systemd-backlight@backlight:amdgpu_bl1.service - Load/Save Screen Backlight Brightness of backlight:amdgpu_bl1.
```
Ausgabe von `xrandr --verbose`:

```
Screen 0: minimum 320 x 200, current 1920 x 1080, maximum 16384 x 16384
eDP connected primary 1920x1080+0+0 (0x57) normal (normal left inverted right x axis y axis) 309mm x 174mm
        Identifier: 0x52
        Timestamp:  12984
        Subpixel:   unknown
        Gamma:      1.0:1.4:1.9
        Brightness: 1.0
        Clones:    
        CRTC:       0
        CRTCs:      0 1 2 3
        Transform:  1.000000 0.000000 0.000000
                    0.000000 1.000000 0.000000
                    0.000000 0.000000 1.000000
                   filter: 
        _KDE_SCREEN_INDEX: 1 
        EDID: 
                00ffffffffffff0030e40f0600000000
                001c0104951f117803aa95955e598e27
                1b505400000001010101010101010101
                0101010101012e3680a070381f403020
                350035ae100000191b2480a070381f40
                3020350035ae10000019000000000000
                00000000000000000000000000000002
                000c3fff0a3c7d10101e7d0000000090
        GAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        DEGAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        GAMMA_LUT: 0 
                range: (0, 65535)
        CTM: 0 1 0 0 0 0 0 0 0 1 0 0 0 0 0 0 
                0 1 
        DEGAMMA_LUT: 0 
                range: (0, 65535)
        TearFree: auto 
                supported: off, on, auto
        HDCP Content Type: HDCP Type0 
                supported: HDCP Type0, HDCP Type1
        Content Protection: Undesired 
                supported: Undesired, Desired, Enabled
        vrr_capable: 0 
                range: (0, 1)
        Colorspace: Default 
                supported: Default, BT709_YCC, opRGB, BT2020_RGB, BT2020_YCC
        max bpc: 16 
                range: (8, 16)
        underscan vborder: 0 
                range: (0, 128)
        underscan hborder: 0 
                range: (0, 128)
        underscan: off 
                supported: off, on, auto
        scaling mode: None 
                supported: None, Full, Center, Full aspect
        link-status: Good 
                supported: Good, Bad
        CONNECTOR_ID: 87 
                supported: 87
        non-desktop: 0 
                range: (0, 1)
  1920x1080 (0x57) 138.700MHz -HSync -VSync *current +preferred
        h: width  1920 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height 1080 start 1083 end 1088 total 1111           clock  60.02Hz
  1920x1080 (0x58) 92.430MHz -HSync -VSync
        h: width  1920 start 1968 end 2000 total 2080 skew    0 clock  44.44KHz
        v: height 1080 start 1083 end 1088 total 1111           clock  40.00Hz
  1680x1050 (0x59) 138.700MHz -HSync -VSync
        h: width  1680 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height 1050 start 1083 end 1088 total 1111           clock  60.02Hz
  1280x1024 (0x5a) 138.700MHz -HSync -VSync
        h: width  1280 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height 1024 start 1083 end 1088 total 1111           clock  60.02Hz
  1440x900 (0x5b) 138.700MHz -HSync -VSync
        h: width  1440 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height  900 start 1083 end 1088 total 1111           clock  60.02Hz
  1280x800 (0x5c) 138.700MHz -HSync -VSync
        h: width  1280 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height  800 start 1083 end 1088 total 1111           clock  60.02Hz
  1280x720 (0x5d) 138.700MHz -HSync -VSync
        h: width  1280 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height  720 start 1083 end 1088 total 1111           clock  60.02Hz
  1024x768 (0x5e) 138.700MHz -HSync -VSync
        h: width  1024 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height  768 start 1083 end 1088 total 1111           clock  60.02Hz
  800x600 (0x5f) 138.700MHz -HSync -VSync
        h: width   800 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height  600 start 1083 end 1088 total 1111           clock  60.02Hz
  640x480 (0x60) 138.700MHz -HSync -VSync
        h: width   640 start 1968 end 2000 total 2080 skew    0 clock  66.68KHz
        v: height  480 start 1083 end 1088 total 1111           clock  60.02Hz
DisplayPort-0 disconnected (normal left inverted right x axis y axis)
        Identifier: 0x53
        Timestamp:  12984
        Subpixel:   unknown
        Clones:    
        CRTCs:      0 1 2 3
        Transform:  1.000000 0.000000 0.000000
                    0.000000 1.000000 0.000000
                    0.000000 0.000000 1.000000
                   filter: 
        GAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        DEGAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        GAMMA_LUT: 0 
                range: (0, 65535)
        CTM: 0 
        DEGAMMA_LUT: 0 
                range: (0, 65535)
        TearFree: auto 
                supported: off, on, auto
        subconnector: Unknown 
                supported: Unknown, VGA, DVI-D, HDMI, DP, Wireless, Native
        HDCP Content Type: HDCP Type0 
                supported: HDCP Type0, HDCP Type1
        Content Protection: Undesired 
                supported: Undesired, Desired, Enabled
        vrr_capable: 0 
                range: (0, 1)
        Colorspace: Default 
                supported: Default, BT709_YCC, opRGB, BT2020_RGB, BT2020_YCC
        max bpc: 16 
                range: (8, 16)
        underscan vborder: 0 
                range: (0, 128)
        underscan hborder: 0 
                range: (0, 128)
        underscan: off 
                supported: off, on, auto
        scaling mode: None 
                supported: None, Full, Center, Full aspect
        link-status: Good 
                supported: Good, Bad
        CONNECTOR_ID: 95 
                supported: 95
        non-desktop: 0 
                range: (0, 1)
DisplayPort-1 disconnected (normal left inverted right x axis y axis)
        Identifier: 0x54
        Timestamp:  12984
        Subpixel:   unknown
        Clones:    
        CRTCs:      0 1 2 3
        Transform:  1.000000 0.000000 0.000000
                    0.000000 1.000000 0.000000
                    0.000000 0.000000 1.000000
                   filter: 
        GAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        DEGAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        GAMMA_LUT: 0 
                range: (0, 65535)
        CTM: 0 
        DEGAMMA_LUT: 0 
                range: (0, 65535)
        TearFree: auto 
                supported: off, on, auto
        subconnector: Unknown 
                supported: Unknown, VGA, DVI-D, HDMI, DP, Wireless, Native
        HDCP Content Type: HDCP Type0 
                supported: HDCP Type0, HDCP Type1
        Content Protection: Undesired 
                supported: Undesired, Desired, Enabled
        vrr_capable: 0 
                range: (0, 1)
        Colorspace: Default 
                supported: Default, BT709_YCC, opRGB, BT2020_RGB, BT2020_YCC
        max bpc: 16 
                range: (8, 16)
        underscan vborder: 0 
                range: (0, 128)
        underscan hborder: 0 
                range: (0, 128)
        underscan: off 
                supported: off, on, auto
        scaling mode: None 
                supported: None, Full, Center, Full aspect
        link-status: Good 
                supported: Good, Bad
        CONNECTOR_ID: 101 
                supported: 101
        non-desktop: 0 
                range: (0, 1)
DisplayPort-2 disconnected (normal left inverted right x axis y axis)
        Identifier: 0x55
        Timestamp:  12984
        Subpixel:   unknown
        Clones:    
        CRTCs:      0 1 2 3
        Transform:  1.000000 0.000000 0.000000
                    0.000000 1.000000 0.000000
                    0.000000 0.000000 1.000000
                   filter: 
        GAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        DEGAMMA_LUT_SIZE: 4096 
                range: (0, -1)
        GAMMA_LUT: 0 
                range: (0, 65535)
        CTM: 0 
        DEGAMMA_LUT: 0 
                range: (0, 65535)
        TearFree: auto 
                supported: off, on, auto
        subconnector: Unknown 
                supported: Unknown, VGA, DVI-D, HDMI, DP, Wireless, Native
        HDCP Content Type: HDCP Type0 
                supported: HDCP Type0, HDCP Type1
        Content Protection: Undesired 
                supported: Undesired, Desired, Enabled
        vrr_capable: 0 
                range: (0, 1)
        Colorspace: Default 
                supported: Default, BT709_YCC, opRGB, BT2020_RGB, BT2020_YCC
        max bpc: 16 
                range: (8, 16)
        underscan vborder: 0 
                range: (0, 128)
        underscan hborder: 0 
                range: (0, 128)
        underscan: off 
                supported: off, on, auto
        scaling mode: None 
                supported: None, Full, Center, Full aspect
        link-status: Good 
                supported: Good, Bad
        CONNECTOR_ID: 106 
                supported: 106
        non-desktop: 0 
                range: (0, 1)
```

Ausgabe von `lspci -vv -s 04:00.0`:

```
04:00.0 VGA compatible controller: Advanced Micro Devices, Inc. [AMD/ATI] Picasso/Raven 2 [Radeon Vega Series / Radeon Vega Mobile Series] (rev d3) (prog-if 00 [VGA controller])
        DeviceName: Onboard IGD
        Subsystem: Hewlett-Packard Company Picasso/Raven 2 [Radeon Vega Series / Radeon Vega Mobile Series]
        Control: I/O+ Mem+ BusMaster+ SpecCycle- MemWINV- VGASnoop- ParErr- Stepping- SERR- FastB2B- DisINTx+
        Status: Cap+ 66MHz- UDF- FastB2B- ParErr- DEVSEL=fast >TAbort+ <TAbort- <MAbort- >SERR- <PERR- INTx-
        Latency: 0
        Interrupt: pin A routed to IRQ 44
        IOMMU group: 11
        Region 0: Memory at e0000000 (64-bit, prefetchable) [size=256M]
        Region 2: Memory at f0000000 (64-bit, prefetchable) [size=2M]
        Region 4: I/O ports at 2000 [size=256]
        Region 5: Memory at f0600000 (32-bit, non-prefetchable) [size=512K]
        Expansion ROM at 000c0000 [virtual] [disabled] [size=128K]
        Capabilities: [48] Vendor Specific Information: Len=08 <?>
        Capabilities: [50] Power Management version 3
                Flags: PMEClk- DSI- D1- D2- AuxCurrent=0mA PME(D0-,D1+,D2+,D3hot+,D3cold+)
                Status: D0 NoSoftRst- PME-Enable- DSel=0 DScale=0 PME-
        Capabilities: [64] Express (v2) Legacy Endpoint, MSI 00
                DevCap: MaxPayload 256 bytes, PhantFunc 0, Latency L0s <4us, L1 unlimited
                        ExtTag+ AttnBtn- AttnInd- PwrInd- RBE+ FLReset+
                DevCtl: CorrErr- NonFatalErr- FatalErr- UnsupReq-
                        RlxdOrd+ ExtTag+ PhantFunc- AuxPwr- NoSnoop+ FLReset-
                        MaxPayload 128 bytes, MaxReadReq 512 bytes
                DevSta: CorrErr- NonFatalErr- FatalErr- UnsupReq- AuxPwr- TransPend-
                LnkCap: Port #0, Speed 8GT/s, Width x16, ASPM L0s L1, Exit Latency L0s <64ns, L1 <1us
                        ClockPM- Surprise- LLActRep- BwNot- ASPMOptComp+
                LnkCtl: ASPM Disabled; RCB 64 bytes, Disabled- CommClk+
                        ExtSynch- ClockPM- AutWidDis- BWInt- AutBWInt-
                LnkSta: Speed 8GT/s, Width x16
                        TrErr- Train- SlotClk+ DLActive- BWMgmt- ABWMgmt-
                DevCap2: Completion Timeout: Not Supported, TimeoutDis- NROPrPrP- LTR+
                         10BitTagComp- 10BitTagReq- OBFF Not Supported, ExtFmt+ EETLPPrefix+, MaxEETLPPrefixes 1
                         EmergencyPowerReduction Not Supported, EmergencyPowerReductionInit-
                         FRS-
                         AtomicOpsCap: 32bit- 64bit- 128bitCAS-
                DevCtl2: Completion Timeout: 50us to 50ms, TimeoutDis- LTR- 10BitTagReq- OBFF Disabled,
                         AtomicOpsCtl: ReqEn-
                LnkCap2: Supported Link Speeds: 2.5-8GT/s, Crosslink- Retimer- 2Retimers- DRS-
                LnkCtl2: Target Link Speed: 8GT/s, EnterCompliance- SpeedDis-
                         Transmit Margin: Normal Operating Range,EnterModifiedCompliance- ComplianceSOS-
                         Compliance Preset/De-emphasis: -6dB de-emphasis, 0dB preshoot
                LnkSta2: Current De-emphasis Level: -3.5dB, EqualizationComplete+ EqualizationPhase1+
                         EqualizationPhase2+ EqualizationPhase3+ LinkEqualizationRequest-
                         Retimer- 2Retimers- CrosslinkRes: unsupported
        Capabilities: [a0] MSI: Enable- Count=1/4 Maskable- 64bit+
                Address: 0000000000000000  Data: 0000
        Capabilities: [c0] MSI-X: Enable+ Count=3 Masked-
                Vector table: BAR=5 offset=00042000
                PBA: BAR=5 offset=00043000
        Capabilities: [100 v1] Vendor Specific Information: ID=0001 Rev=1 Len=010 <?>
        Capabilities: [200 v1] Physical Resizable BAR
                BAR 0: current size: 256MB, supported: 256MB 512MB 1GB
                BAR 2: current size: 2MB, supported: 2MB 4MB 8MB 16MB 32MB 64MB 128MB 256MB
        Capabilities: [270 v1] Secondary PCI Express
                LnkCtl3: LnkEquIntrruptEn- PerformEqu-
                LaneErrStat: 0
        Capabilities: [2a0 v1] Access Control Services
                ACSCap: SrcValid- TransBlk- ReqRedir- CmpltRedir- UpstreamFwd- EgressCtrl- DirectTrans-
                ACSCtl: SrcValid- TransBlk- ReqRedir- CmpltRedir- UpstreamFwd- EgressCtrl- DirectTrans-
        Capabilities: [2b0 v1] Address Translation Service (ATS)
                ATSCap: Invalidate Queue Depth: 00
                ATSCtl: Enable+, Smallest Translation Unit: 00
        Capabilities: [2c0 v1] Page Request Interface (PRI)
                PRICtl: Enable+ Reset-
                PRISta: RF- UPRGI- Stopped+
                Page Request Capacity: 00000020, Page Request Allocation: 00000020
        Capabilities: [2d0 v1] Process Address Space ID (PASID)
                PASIDCap: Exec+ Priv+, Max PASID Width: 10
                PASIDCtl: Enable+ Exec- Priv-
        Capabilities: [320 v1] Latency Tolerance Reporting
                Max snoop latency: 0ns
                Max no snoop latency: 0ns
        Kernel driver in use: amdgpu
        Kernel modules: amdgpu
```


## Nicht erfolgreicher Boot (Standard)

Ausgabe von `journalctl -b | grep amdgpu`:

```
Apr 23 16:04:35 manul kernel: [drm] amdgpu kernel modesetting enabled.
Apr 23 16:04:35 manul kernel: amdgpu: Virtual CRAT table created for CPU
Apr 23 16:04:35 manul kernel: amdgpu: Topology: Add CPU node
Apr 23 16:04:35 manul kernel: amdgpu 0000:04:00.0: Invalid PCI ROM header signature: expecting 0xaa55, got 0xffff
Apr 23 16:04:35 manul kernel: amdgpu 0000:04:00.0: amdgpu: Unable to locate a BIOS ROM
Apr 23 16:04:35 manul kernel: amdgpu 0000:04:00.0: amdgpu: Fatal error during GPU init
Apr 23 16:04:35 manul kernel: amdgpu 0000:04:00.0: amdgpu: amdgpu: finishing device.
Apr 23 16:04:35 manul kernel: amdgpu 0000:04:00.0: probe with driver amdgpu failed with error -22
```

Ausgabe von `xrandr --verbose`:

```
None-1 connected primary 1920x1080+0+0 (0x41) normal (normal left inverted right x axis y axis) 0mm x 0mm
        Identifier: 0x3f
        Timestamp:  12024
        Subpixel:   unknown
        Gamma:      1.0:1.4:1.9
        Brightness: 1.0
        Clones:    
        CRTC:       0
        CRTCs:      0
        Transform:  1.000000 0.000000 0.000000
                    0.000000 1.000000 0.000000
                    0.000000 0.000000 1.000000
                   filter: 
        _KDE_SCREEN_INDEX: 1 
        link-status: Good 
                supported: Good, Bad
        CONNECTOR_ID: 36 
                supported: 36
        non-desktop: 0 
                range: (0, 1)
  1920x1080 (0x41) 124.416MHz *current +preferred
        h: width  1920 start 1920 end 1920 total 1920 skew    0 clock  64.80KHz
        v: height 1080 start 1080 end 1080 total 1080           clock  60.00Hz
```

## Status

- Aktuellstes BIOS: `R81 Ver.01.30.00 01/15/2025`
- Linux-Distribution:
- Kernel:

## Tipps

Ausgabe von `lspci -vv -s 04:00.0`:
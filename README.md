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
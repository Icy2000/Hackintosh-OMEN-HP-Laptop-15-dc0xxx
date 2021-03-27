**Hackintosh for OMEN-HP-Laptop-15-dc0xxx**

>HP OMEN Laptop 15-dc0xxx Hackintosh OpenCore EFI

- Original Author: MooreHarris
- Original Link: See on [PC Beta](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1832126)
- Repair Big Sur To Work by [Spoience](https://www.spoience.com)
- License: [MIT](https://github.com/Spoience/Hackintosh-OMEN-HP-Laptop-15-dc0xxx/blob/master/LICENSE)

**Configuration information**

- CPU: Intel(R) Core i5-8300H
- Integrated Graphics: Intel(R) UHD 630
- Discrete Graphics Card: Nvidia(R) Geforce GTX 1050 Ti
- Wireless Network & Bluetooth Card: Intel(R) Wireless-AC 9560AC 160 MHZ
- Sound Card: Realtek ALC 265
- Port: USB 3*Gen3, 1\*Type-C, 1\*Rj45,1*mini DP, 1*HDMI

**What Works**

- CPU: Work
- Integrated Graphics: Work
- Discrete Graphics Card: Shield
- Wireless Network & Bluetooth Card: Work (See On [OpenIntelWireless](https://openintelwireless.github.io/))
- Sound Card: Work
- USB Ports: Work
- Screen Brightness Adjustment: Work
- Wake Up From Sleep: Work
- CPU Frequency Conversion: Work
- Touchpad: Work (Most gestures are available, but due to the gap between the trackpad and Mackintosh, the experience may not be increased)
- Type-C to HDMI: Work

**Test Installation Environment**

- Test System Image: Original macOS Big Sur 11.2 20D64 Installer.dmg
- System Image Writing Tool：[balenaEtcher](https://www.balena.io/etcher/)
- OpenCore Version: v0.6.2


**File Directory Tree**

```TREE
EFI
    ├─BOOT
    │      BOOTX64.efi
    │      
    └─OC
        │  config.plist
        │  OpenCore.efi
        │  
        ├─ACPI
        │      DSDT-FN F4 键盘灯.aml
        │      DSDT.aml
        │      SSDT-DGPU.aml
        │      SSDT-EC.aml
        │      SSDT-PMC.aml
        │      SSDT-PNLFCFL.aml
        │      SSDT-SMBUS.aml
        │      SSDT-XCPM.aml
        │      SSDT-XOSI.aml
        │      
        ├─Bootstrap
        │      Bootstrap.efi
        │      
        ├─Drivers
        │      HfsPlus.efi
        │      OpenCanopy.efi
        │      OpenRuntime.efi
        │      
        ├─Kexts
        │  ├─ACPIBatteryManager.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              ACPIBatteryManager
        │  │              
        │  ├─AirportItlwm.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              AirportItlwm
        │  │              
        │  ├─AppleALC.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              AppleALC
        │  │              
        │  ├─ApplePS2SmartTouchPad.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      ├─MacOS
        │  │      │      ApplePS2SmartTouchPad
        │  │      │      
        │  │      ├─PlugIns
        │  │      │  ├─ApplePS2Controller.kext
        │  │      │  │  └─Contents
        │  │      │  │      │  Info.plist
        │  │      │  │      │  
        │  │      │  │      └─MacOS
        │  │      │  │              ApplePS2Controller
        │  │      │  │              
        │  │      │  └─ApplePS2Keyboard.kext
        │  │      │      └─Contents
        │  │      │          │  Info.plist
        │  │      │          │  
        │  │      │          └─MacOS
        │  │      │                  ApplePS2Keyboard
        │  │      │                  
        │  │      └─Resources
        │  │          ├─Features Documentation.rtfd
        │  │          │      11493706554_130fa58d5f_n.jpg
        │  │          │      8524384148_7da070dae6_c.jpg
        │  │          │      9718452526_b6414cd8e7_n.jpg
        │  │          │      TXT.rtf
        │  │          │      
        │  │          └─Synaptics documentation.rtfd
        │  │                  page30image13008.png
        │  │                  page30image13432.png
        │  │                  page30image13912.png
        │  │                  page30image14840.png
        │  │                  page30image15160.png
        │  │                  page30image16448.png
        │  │                  page30image16608.png
        │  │                  page30image18496.png
        │  │                  page30image18808.png
        │  │                  page30image20328.png
        │  │                  page30image21840.png
        │  │                  page30image22000.png
        │  │                  page30image24168.png
        │  │                  page30image24328.png
        │  │                  page30image25088.png
        │  │                  page30image25248.png
        │  │                  page30image26496.png
        │  │                  page30image26984.png
        │  │                  page30image28496.png
        │  │                  page30image29088.png
        │  │                  page30image31456.png
        │  │                  page30image31616.png
        │  │                  page30image31776.png
        │  │                  page30image31936.png
        │  │                  page30image32096.png
        │  │                  page30image32256.png
        │  │                  page30image32416.png
        │  │                  page30image33264.png
        │  │                  page30image33848.png
        │  │                  page30image34168.png
        │  │                  page30image34328.png
        │  │                  page30image34920.png
        │  │                  page30image35080.png
        │  │                  page30image35672.png
        │  │                  page30image35992.png
        │  │                  page30image36312.png
        │  │                  page30image36472.png
        │  │                  page30image36632.png
        │  │                  page30image36792.png
        │  │                  page30image36952.png
        │  │                  page30image37112.png
        │  │                  page30image37272.png
        │  │                  page30image38680.png
        │  │                  page30image39000.png
        │  │                  page30image40360.png
        │  │                  page30image41264.png
        │  │                  page30image42512.png
        │  │                  page30image42992.png
        │  │                  page30image44072.png
        │  │                  page30image44392.png
        │  │                  page30image45080.png
        │  │                  page30image45400.png
        │  │                  page30image45872.png
        │  │                  page30image47224.png
        │  │                  page30image47840.png
        │  │                  page30image48000.png
        │  │                  page30image49832.png
        │  │                  page30image49992.png
        │  │                  page30image50744.png
        │  │                  page30image51992.png
        │  │                  page30image52480.png
        │  │                  page30image53728.png
        │  │                  page30image54320.png
        │  │                  page30image54640.png
        │  │                  page30image56688.png
        │  │                  page30image56848.png
        │  │                  page30image57008.png
        │  │                  page30image57328.png
        │  │                  page30image57488.png
        │  │                  page30image57648.png
        │  │                  page30image58464.png
        │  │                  page30image59048.png
        │  │                  page30image59368.png
        │  │                  page30image59528.png
        │  │                  page30image60112.png
        │  │                  page30image60272.png
        │  │                  page30image60432.png
        │  │                  page30image61880.png
        │  │                  page30image62040.png
        │  │                  page30image62200.png
        │  │                  page30image63104.png
        │  │                  page30image63424.png
        │  │                  page30image63744.png
        │  │                  page30image64064.png
        │  │                  page30image64672.png
        │  │                  page30image64832.png
        │  │                  page30image65424.png
        │  │                  page30image65744.png
        │  │                  page30image65904.png
        │  │                  page30image66064.png
        │  │                  page30image66224.png
        │  │                  page30image67312.png
        │  │                  page30image67472.png
        │  │                  page30image67632.png
        │  │                  page30image68112.png
        │  │                  page30image68432.png
        │  │                  page30image68856.png
        │  │                  page30image69176.png
        │  │                  page42image103272.png
        │  │                  page42image105384.png
        │  │                  page42image105808.png
        │  │                  page42image75600.png
        │  │                  page42image75760.png
        │  │                  page42image76080.png
        │  │                  page42image76672.png
        │  │                  page42image76832.png
        │  │                  page42image77440.png
        │  │                  page42image77600.png
        │  │                  page42image77920.png
        │  │                  page42image78240.png
        │  │                  page42image78848.png
        │  │                  page42image79272.png
        │  │                  page42image81272.png
        │  │                  page42image82192.png
        │  │                  page42image83992.png
        │  │                  page42image84520.png
        │  │                  page42image85104.png
        │  │                  page42image85528.png
        │  │                  page42image86456.png
        │  │                  page42image86936.png
        │  │                  page42image87360.png
        │  │                  page42image88112.png
        │  │                  page42image88272.png
        │  │                  page42image88912.png
        │  │                  page42image93040.png
        │  │                  page42image95864.png
        │  │                  page42image96184.png
        │  │                  page42image97536.png
        │  │                  page42image99496.png
        │  │                  page43image24304.png
        │  │                  page43image24464.png
        │  │                  page43image24784.png
        │  │                  page43image25376.png
        │  │                  page43image25536.png
        │  │                  page43image26144.png
        │  │                  page43image26304.png
        │  │                  page43image26624.png
        │  │                  page43image26944.png
        │  │                  page43image27568.png
        │  │                  page43image28152.png
        │  │                  page43image29984.png
        │  │                  page43image30408.png
        │  │                  page43image30736.png
        │  │                  page43image31160.png
        │  │                  page43image32696.png
        │  │                  page43image33232.png
        │  │                  page43image33392.png
        │  │                  page43image33816.png
        │  │                  page43image34240.png
        │  │                  page43image35168.png
        │  │                  page43image35648.png
        │  │                  page43image35968.png
        │  │                  page43image36720.png
        │  │                  page43image36880.png
        │  │                  page43image37520.png
        │  │                  page43image46136.png
        │  │                  page43image48136.png
        │  │                  page43image48560.png
        │  │                  page43image49048.png
        │  │                  page43image50440.png
        │  │                  page43image51704.png
        │  │                  page43image52024.png
        │  │                  page43image53736.png
        │  │                  page43image54056.png
        │  │                  page43image54544.png
        │  │                  page43image55936.png
        │  │                  TXT.rtf
        │  │                  
        │  ├─CtlnaAHCIPort.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  version.plist
        │  │      │  
        │  │      ├─MacOS
        │  │      │      CtlnaAHCIPort
        │  │      │      
        │  │      └─_CodeSignature
        │  │              CodeResources
        │  │              
        │  ├─HibernationFixup.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              HibernationFixup
        │  │              
        │  ├─IntelBluetoothFirmware.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              IntelBluetoothFirmware
        │  │              
        │  ├─IntelBluetoothInjector.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              IntelBluetoothInjector
        │  │              
        │  ├─IOElectrify.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              IOElectrify
        │  │              
        │  ├─Lilu.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              Lilu
        │  │              
        │  ├─NVMeFix.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              NVMeFix
        │  │              
        │  ├─RealtekRTL8111.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      ├─MacOS
        │  │      │      RealtekRTL8111
        │  │      │      
        │  │      └─Resources
        │  │          └─en.lproj
        │  │                  InfoPlist.strings
        │  │                  
        │  ├─SMCBatteryManager.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      ├─MacOS
        │  │      │      SMCBatteryManager
        │  │      │      
        │  │      └─Resources
        │  │              SSDT-BATC.dsl
        │  │              
        │  ├─SMCDellSensors.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              SMCDellSensors
        │  │              
        │  ├─SMCLightSensor.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              SMCLightSensor
        │  │              
        │  ├─SMCProcessor.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              SMCProcessor
        │  │              
        │  ├─SMCSuperIO.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              SMCSuperIO
        │  │              
        │  ├─USBPorts.kext
        │  │  └─Contents
        │  │          Info.plist
        │  │          
        │  ├─VirtualSMC.kext
        │  │  └─Contents
        │  │      │  Info.plist
        │  │      │  
        │  │      └─MacOS
        │  │              VirtualSMC
        │  │              
        │  └─WhateverGreen.kext
        │      └─Contents
        │          │  Info.plist
        │          │  
        │          └─MacOS
        │                  WhateverGreen
        │                  
        ├─Resources
        │  ├─Font
        │  │      Font_1x.bin
        │  │      Font_1x.png
        │  │      Font_2x.bin
        │  │      Font_2x.png
        │  │      
        │  ├─Image
        │  │      AppleRecv.icns
        │  │      AppleTM.icns
        │  │      Cursor.icns
        │  │      ExtAppleRecv.icns
        │  │      ExtAppleTM.icns
        │  │      ExtHardDrive.icns
        │  │      HardDrive.icns
        │  │      OldAppleRecv.icns
        │  │      OldAppleTM.icns
        │  │      OldCursor.icns
        │  │      OldExtAppleRecv.icns
        │  │      OldExtAppleTM.icns
        │  │      OldExtHardDrive.icns
        │  │      OldHardDrive.icns
        │  │      OldSelected.icns
        │  │      OldSelector.icns
        │  │      OldShell.icns
        │  │      OldTool.icns
        │  │      OldWindows.icns
        │  │      Selected.icns
        │  │      Selector.icns
        │  │      Shell.icns
        │  │      Tool.icns
        │  │      Windows.icns
        │  │      
        │  └─Label
        │          Apple.l2x
        │          Apple.lbl
        │          AppleRecv.l2x
        │          AppleRecv.lbl
        │          AppleTM.l2x
        │          AppleTM.lbl
        │          EFIBoot.l2x
        │          EFIBoot.lbl
        │          Other.l2x
        │          Other.lbl
        │          ResetNVRAM.l2x
        │          ResetNVRAM.lbl
        │          Shell.l2x
        │          Shell.lbl
        │          Tool.l2x
        │          Tool.lbl
        │          Windows.l2x
        │          Windows.lbl
        │          
        └─Tools
                BootKicker.efi
                ChipTune.efi
                CleanNvram.efi
                GopStop.efi
                HdaCodecDump.efi
                KeyTester.efi
                MmapDump.efi
                OpenControl.efi
                OpenShell.efi
                ResetSystem.efi
                RtcRw.efi
                VerifyMsrE2.efi
                

```


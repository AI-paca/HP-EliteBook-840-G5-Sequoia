EliteBook 840 G5
- Intel UHD Graphics 620
- Core i7 - 8550U (Kaby Lake-R)
---
Interfaces:
- USB 3.1 - testing
- RJ45 (LAN) - testing
- 3.5 jack - testing
- Mic - testing
- Cam - testing
- HDMI - testing
- Thunderbolt 3 - testing
- Card Reader - testing
- LAN (RJ-45) - testing
- WiFi - testing
- Bluetooth - testing
---
EFI/OC/Drivers
- [HfsPlus.efi](https://github.com/acidanthera/OcBinaryData/blob/master/Drivers/HfsPlus.efi)
- OpenRuntime.efi
- the other drivers are up to your liking

EFI/OC/Kexts<br>
pre-compiled [kext](https://dortania.github.io/builds/)
- Lilu.kext
- VirtualSMC
  - SMCBatteryManager.kext
  - SMCLightSensor.kext
  - SMCProcessor.kext
  - SMCSuperIO.kext
  - VirtualSMC.kext
- WhateverGreen.kext
- AppleALC.kext
- IntelMausi.kext
- RealtekRTL8111.kext (it's my spare adapter, you don't need it.)
- USBInjectAll.kext (alternative USBToolBox.kext)
- USBPorts.kext (alternative UTBMap.kext, generated from the target device, using the [tool](https://github.com/USBToolBox/tool), if this does not work for you, generate the ports after the system boots - UTBDefault.kext)
- IntelBluetoothFirmware (all)
- BrcmPatchRAM
  - BlueToolFixup.kext
  - BrcmBluetoothInjector.kext
  - BrcmPatchRAM3.kext
- [AirportItlwm.kext](https://github.com/OpenIntelWireless/itlwm/releases)(possible error in [config](https://dortania.github.io/OpenCore-Install-Guide/ktext.html#wifi-and-bluetooth))
- CpuTscSync.kext
- VoodooPS2Controller.kext
- VoodooRMI.kext

I use a WD SSD, if you use a different SSD add this:
- NVMeFix.kext
- [SATA-unsupported.kext](https://github.com/khronokernel/Legacy-Kexts/blob/master/Injectors/Zip/SATA-unsupported.kext.zip)(probably don't need it)
- [EmeraldSDHC.kext](https://github.com/acidanthera/EmeraldSDHC/releases/tag/0.1.2)(probably don't need it)

EFI/OC/ACPI<br>
- generate ASPI on the target device via [SSDTTime](https://github.com/corpnewt/SSDTTime) (btw I got it from [here](https://github.com/kecinzer/hpelitebook850g5-opencore))
---
Errors:
<br>— ACPI Error: battery detection, this error is related to the updated version of BIOS (potential solution not [here](https://github.com/kecinzer/hpelitebook850g5-opencore/tree/master/EFI/OC/ACPI))
<br>— BIOS error 005 (loss of real time clock power, suspecting this is a consequence of the previous problem)

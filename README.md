# ASRock Z390M Pro4 Hackintosh on OpenCore

## macOS Versions
#### macOS Catalina 10.15.2

## SMBIOS
#### iMac19,1

### What works
- **dGPU** Hardware Accelaration (Final Cut Pro X, VideoProc, Compressor), DRM Content (Apple TV+/Safari Netflix/Amazon Prime)
- **iGPU** Hardware Accelaration (Final Cut Pro X), Apple Sidecar
- **WIFI,Bluetooth** BCM94360CD Required
- **AirDrop, Handoff** BCM94360CD Required
- **USB** All USB3.1 Gen1/USB2.0 Port (Type-C may not works)
- **Audio** Realtek ALC892, (layout id: 5)
- **NVRAM** 300 series motherboards now support native NVRAM

### Not works
- **iMessage,FaceTime,Location-based service** Specific cause cannot be identified

### Device Lists
| Device | Model |
|----|----|
| MotherBoard | ASRock Z390M Pro4 |
| CPU | Intel i5 9500 |
| RAM | Asgard LOKI 51℃ 2666 8GB * 4|
| Video Card | Sapphire RX 5500XT 8GB|
| Sound Card | Realtek ALC892 （MotherBoard）|
| Network Interface Card | PCI-E BCM94360CD (WI-FI + Bluetooth) |
| Hard Disk | Hikvision C2000Pro 1TB NVMe SSD |
| Case | JONSBO UMX3 |

### Software Version
#### Boot firmware
| Boot  | Versions |
|----|----|
| OpenCore | [Latest release(0.5.4)](https://github.com/acidanthera/OpenCorePkg) |

#### Kext
| Kext | Downloads |
|----|----|
| Lilu | [Latest release(1.4.1)](https://github.com/acidanthera/Lilu) |
| VirtualSMC,SMCProcessor,SMCSuperIO| [Latest release(1.1.0)](https://github.com/acidanthera/VirtualSMC) |
| WhateverGreen | [Latest release(1.3.6)](https://github.com/bugprogrammer/WhateverGreen) Revision |
| AppleALC | [Latest release(1.4.5)](https://github.com/acidanthera/AppleALC) |
| IntelMausi | [Latest release(1.0.2)](https://github.com/acidanthera/IntelMausi) |
| USBInjectAll | [Version: 2018-1108](https://bitbucket.org/RehabMan/os-x-usb-inject-all/downloads/?tab=downloads) |
| CPUFriend | [Latest release(1.2.0)](https://github.com/acidanthera/CPUFriend) |
| NoTouchID | [Latest release(1.0.3)](https://github.com/al3xtjames/NoTouchID) |

#### EFI
| EFI | Downloads |
|----|----|
| ApfsDriverLoader | [Latest release](https://github.com/acidanthera/AppleSupportPkg) |
| HfsPlus | Latest release |
| FwRuntimeServices | [Latest release](https://github.com/acidanthera/AppleSupportPkg) |
| MemoryAllocation | [Latest release](https://github.com/williambj1/OpenCore-Factory/releases/tag/OpenCore-UEFI-Drivers) |


### Where you need to modify

- **Use Tools:** Macserial

![Where you need to modify](https://github.com/SeonMe/ASRock-Hackintosh-OC/raw/master/Images/config_edit.png)

- **Use tools:** Hackintool > PCI

![DeviceProperties_Edit](https://github.com/SeonMe/ASRock-Hackintosh-OC/raw/master/Images/DeviceProperties_Edit.png)

### BIOS Settings
- **BIOS Version** 4.30

| Disabled | Enabled |
|----|----|
| Fast Boot | VT-x |
| CFG Lock (MSR 0xE2 write protection) | Above 4G |
| VT-d | Hyper Threading (If you use a CPU with K) |
| CSM | Execute Disable Bit |
| | EHCI/XHCI Hand-off |
| | OS type: other types |

### Changelog

### 20/1/2020
* Modify SSDT to support native NVRAM

### 15/1/2020
* UPDATE OpenCore 0.5.4(Latest release)
* UPDATE All Kext and EFI Latest release
* UPDATE config.plist
* Delete USBPort.kext USBPower.kext CPUFriendDataProvider.kext

#### 12/1/2020
* UPDATE OpenCore to 12/1/2020 Versions
* UPDATE All Kext and EFI latest Versions
* UPDATE config.plist

#### 7/1/2020
* UPDATE OpenCore to 7/1/2020 Versions
* UPDATE VirtualSmc to 7/1/2020 Versions
* Delete VirtualSMC.efi from OC>Drivers
* Delete VirtualSMC.efi from config.plist

#### 28/12 2019
* Rewrite README.md
* Update config.plist dGPU configuration

#### 1/12 2019
* Initial release

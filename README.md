# ASRock-Hackintosh-OC

## macOS Versions
#### macOS Catalina 10.15.2

## SMBIOS
#### iMac19,1

### What works
- **dGPU** Hardware Accelaration (Final Cut Pro X, VideoProc, Compressor), DRM Content (Apple TV+/Safari Netflix/Amazon Prime)
- **iGPU** Hardware Accelaration (Final Cut Pro X), Apple Sidecar
- **AirDrop, Handoff** BCM94360CD Required
- **USB** All USB3.1 Gen1/USB2.0 Port (Type-C may not works)
- **Audio** Realtek ALC892, (layout id: 5)

### Device Lists
| Device | Model |
|----|----|
| MotherBoard | ASRock Z390M Pro4 |
| CPU | Intel i5 9500 |
| RAM | Asgard LOKI 51℃ 2666 8GB |
| Video Card | Sapphire RX 5500XT 8GB * 4|
| Sound Card | Realtek ALC892 （MotherBoard）|
| Network Interface Card | PCI-E BCM94360CD (WI-FI + Bluetooth) |
| Hard Disk | WD Black SN750 NVMe SSD 250G |
| Case | JONSBO UMX3 |

### Software Version
#### Boot firmware
| Boot  | Versions |
|----|----|
| OpenCore | [0.5.4](https://github.com/acidanthera/OpenCorePkg/releases) |

#### Kext
| Kext | Downloads |
|----|----|
| Lilu | [1.4.1](https://github.com/acidanthera/Lilu/releases) |
| VirtualSMC | [1.0.9](https://github.com/acidanthera/VirtualSMC/releases) |
| WhateverGreen | [1.3.6](https://github.com/bugprogrammer/WhateverGreen/releases) Revision |
| AppleALC | [1.4.5](https://github.com/acidanthera/AppleALC/releases) |
| IntelMausi | [1.0.2](https://github.com/acidanthera/IntelMausi/releases) |
| USBPort | [About USB port customization](https://blog.daliansky.net/Intel-FB-Patcher-USB-Custom-Video.html) |
| USBPower | Customized |
| CPUFriend | [1.2.0](https://github.com/acidanthera/CPUFriend/releases) |
| CPUFriendDataProvider | [CPUFriendDataProvider](https://blog.xjn819.com/?p=543) |
| NoTouchID | [1.0.3](https://github.com/al3xtjames/NoTouchID/releases) |

#### EFI
| EFI | Downloads |
|----|----|
| ApfsDriverLoader | [ApfsDriverLoader](https://github.com/acidanthera/AppleSupportPkg/releases) |
| HfsPlus | HfsPlus |
|FwRuntimeServices | [FwRuntimeServices](https://github.com/acidanthera/AppleSupportPkg/releases) |
| VirtualSmc | [VirtualSmc](https://github.com/acidanthera/VirtualSMC/releases) |
| MemoryAllocation | [MemoryAllocation](https://github.com/williambj1/OpenCore-Factory/releases/tag/OpenCore-UEFI-Drivers) |
| UsbKbDxe | [UsbKbDxe](https://github.com/acidanthera/AppleSupportPkg/releases) |


### Where you need to modify
![Where you need to modify](https://github.com/SeonMe/ASRock-Hackintosh-OC/raw/master/Images/config_edit.png)

### BIOS Settings
- **BIOS Version** 4.20

| Disabled | Enabled |
|----|----|
| Fast Boot | VT-x |
| CFG Lock | Above 4G |
| VT-d | Hyper Threading (If you use a CPU with K) |
| CSM | XHCI Hand-off |

### Changelog

#### 28/12 2019
* Rewrite README.md
* Update config.plist dGPU configuration

#### 1/12 2019
* Initial release

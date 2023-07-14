# Dell-Vostro-3670-OpenCore
Hackintosh Dell Vostro 3670 with OpenCore - macOS Monterey

|   Thông số kỹ thuật   |        Chi Tiết        |
| --------------------- | ---------------------- |
| Computer Models       | DELL VOSTRO 3670       |
| Operating System      | macOS Monterey  (12.5) |
| Processor             | I5-8500 (I3-8100..)    |
| Memory                | 16G                    |
| Graphics              | Intel UHD 630 Graphics |
| Network adapter       | Realtek RTL8111H       |

### NOT WORKING
- Wifi
- Bluetooth
###  BIOS SETUP

#### [#](https://dortania.github.io/OpenCore-Install-Guide/config.plist/coffee-lake.html#disable)Disable

- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d (can be enabled if you set `DisableIoMapper` to YES)
- CSM
- Thunderbolt(For initial install, as Thunderbolt can cause issues if not setup correctly)
- Intel SGX
- Intel Platform Trust
- CFG Lock (MSR 0xE2 write protection)(**This must be off, if you can't find the option then enable both `AppleCpuPmCfgLock` and `AppleXcpmCfgLock` under Kernel -> Quirks. Your hack will not boot with CFG-Lock enabled**)

#### [#](https://dortania.github.io/OpenCore-Install-Guide/config.plist/coffee-lake.html#enable)Enable

- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated(iGPU Memory): 64MB
- SATA Mode: AHCI
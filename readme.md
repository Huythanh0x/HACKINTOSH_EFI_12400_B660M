# OPENCORE EFI B660M DS3H and Intel I5 12400 - Sonoma 14.7

| ![screenshot](screenshot.png) | 
|:--:| 
| More detailed at [Geekbench report](https://browser.geekbench.com/v6/cpu/7613482) |

### Specs:

- **CPU:** Intel Core i5 12400 (nonF)
- **Motherboard:** Gigabyte B660M DS3H DDR4
- **GPU:** MSI MECH RX 6600 8GB
- **RAM:** 4x Corsair Vengence LPX 8GB 3200Mhz
- **Audio:** Realtek ALC897 (default in mainboard)
- **LAN:** Realtek RTL8125 2.5GbE (default in mainboard)
- **Storage:**
    - WD NVME Black SN850 2TB (Mac)
    - WD NVME Blue SN570 500GB (Mac storage)
    - 2x WD Ultrastar HDD 16TB (Raid1)
- **Wireless:** Intel's AX210 Wi-Fi 6E
- **Monitor:**
    - LG 27QN600 27" IPS 2K
    - TomKo T2721Q 27" IPS 2K
- **Microphone:** MAONO AU-PM461TR
- **Headphone:** Blon BL-03

### Working:

- ✅ CPU Power Management
- ✅ Graphics Acceleration
- ✅ Sleep/Wake
- ✅ Ethernet
- ✅ Audio (alcid=11)
- ✅ USB
- ✅ Wifi and Bluetooth
- ✅ And almost everything else

### Not Working:
- ❌ Handoff and Airdrop (Intel wireless card not supported)

### BIOS Settings
> In most cases, just a bios difference could lead to boot loop. So read this carefully.

**Disable:**
- Fast Boot
- Secure Boot
- Serial/COM Port
- Parallel Port
- VT-d
- Compatibility Support Module (CSM).
- Intel SGX
- Intel Platform Trust

**Enable:**
- VT-x
- Above 4G decoding.
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- SATA Mode: AHCI

### Some notes
I didn't build this EFI on my own. I just chose and built my hardware specs based on [one Reddit post](https://www.reddit.com/r/hackintosh/comments/u78vbx/triple_boot_moneterywindowsubuntu_on_i512400f/). 

**Update 1**: And then I updated the opencore and all kext versions through GUI with [this tool - OCAuxiliaryTools](https://github.com/ic005k/OCAuxiliaryTools).

**Update 2**: I also pick some variables from [another EFI - Sonoma](https://github.com/psabadac/GIGABYTE-B660M-DS3H-DDR4-i7-13700F-Hackintosh-OpenCore) to update to Sonoma 14.4

**Update 3**: I added support for my wireless card Intel Ax210 following [this guide](https://github.com/perez987/Intel-AX210-wifi6-on-macOS-Sonoma).\
*`SecureBootModel` should stay `Disabled` or your PC would be **panic***. \
Creds: [luchina-gabriel](https://github.com/luchina-gabriel/BASE-EFI-INTEL-DESKTOP-12THGEN-ALDER-LAKE-PUBLIC?tab=readme-ov-file#macos-sonoma-144-or-above-versions-including-macos-sequoia-v15)\
If you don't have a wirelesscard. Download the file from [previous release](https://github.com/Huythanh0x/HACKINTOSH_EFI_12400_B660M/releases/tag/1.0) intead.

**Update 4**: Updated `PickerMode` and `ShowPicker` to let Macos Boot directly to login screen like a real Mac. If you got bootloop use the EFI from [previous release](https://github.com/Huythanh0x/HACKINTOSH_EFI_12400_B660M/releases/tag/1.0) intead.
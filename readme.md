EFI for GIGABYTE B660M DS3H and INTEL I5-12400

I din't build this EFI on my own. I just chose and built my hardware based on [one Reddit post](https://www.reddit.com/r/hackintosh/comments/u78vbx/triple_boot_moneterywindowsubuntu_on_i512400f/). 

**ps**: And then I updated the opencore and all kexts through GUI with [this tool](https://github.com/ic005k/OCAuxiliaryTools)

**ps**: I also pick some variables from [another EFI](https://github.com/psabadac/GIGABYTE-B660M-DS3H-DDR4-i7-13700F-Hackintosh-OpenCore)

### Specs:

- **CPU:** Intel Core i5-12400
- **Motherboard:** Gigabyte B660M DS3H DDR4
- **GPU:** MECH RX 6600 8GB
- **RAM:** 4 x Corsair Vengence LPX 8GB 3200Mhz
- **Audio:** Realtek ALC897 (default in mainboard)
- **LAN:** Realtek RTL8125 2.5GbE (default in mainboard)
- **Wireless:** Intel's AX210 Wi-Fi 6E
- **Storage:**
    - WD NVME SN570 500GB (Mac)
    - Kingspec NVME 256GB (Ubuntu)
    - Kingspec (China) 2.5 SSD (Windows)
    - Tosiba HDD 1TB for storage

### Working:

- CPU Power Management
- Graphics Acceleration
- Sleep/Wake
- Ethernet
- Audio (alcid=11)
- USB
- Wifi
- And almost everything else

### Not Working:

- Bluetooth (for now)
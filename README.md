## Disclaimer ❗
This repository contains an outdated and non-functional driver. More recent work is being done on a different repository: [https://github.com/DarkMatter-999/mt7902-dkms](https://github.com/DarkMatter-999/mt7902-dkms). We are attempting to adapt the mt7921 driver, while that has shown some promise, a complete driver design would not be possible without assistance from MediaTek or would necessitate significant time and resources for reverse engineering.

---

# MT7902 Driver for Linux
A newbie-friendly, temporary solution that encourages all contributions for long-term and stable use for MT7902 driver on Linux
This repository provides the necessary files and script to install the MT7902 Wi-Fi driver on a Linux system using NDISWrapper.

## Contents

- `install_wifi_driver.sh`: Shell script to automate the installation of the MT7902 driver on Linux.
- Driver files:
  - `mtkihvx.dll`
  - `mtkwl1.dat`
  - `mtkwl1_2.dat`
  - `mtkwl2.dat`
  - `mtkwl2_2.dat`
  - `mtkwl2_2s.dat`
  - `mtkwl2s.dat`
  - `mtkwl3.dat`
  - `mtkwl3_2.dat`
  - `mtkwl4.dat`
  - `mtkwl6ex.cat`
  - `mtkwl6ex.inf`
  - `mtkwl6ex.sys`
  - `WIFI_MT7902_patch_mcu_1_1_hdr.bin`
  - `WIFI_MT7922_patch_mcu_1_1_hdr.bin`
  - `WIFI_RAM_CODE_MT7902_1.bin`
  - `WIFI_RAM_CODE_MT7922_1.bin`

## Prerequisites

- A Linux system with sudo privileges.
- Internet connection to download necessary packages and driver files.

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/Nevergiveup11837/mt7902driverforlinux.git
   cd mt7902driverforlinux

NOTES: You should use chmod +x install_wifi_driver.sh and sudo ./install_wifi_driver.sh to run the sh file corectly.
After install you will need to reboot your system to apply changes.
Encourage contributions to create a driver that runs directly and stably on Linux.

Or you can update kernel
```sh
wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.15-rc6/amd64/linux-headers-5.15.0-051500rc6-generic_5.15.0-051500rc6.202110180730_amd64.deb
wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.15-rc6/amd64/linux-headers-5.15.0-051500rc6_5.15.0-051500rc6.202110180730_all.deb
wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.15-rc6/amd64/linux-image-unsigned-5.15.0-051500rc6-generic_5.15.0-051500rc6.202110180730_amd64.deb
wget https://kernel.ubuntu.com/~kernel-ppa/mainline/v5.15-rc6/amd64/linux-modules-5.15.0-051500rc6-generic_5.15.0-051500rc6.202110180730_amd64.deb
sudo dpkg -i *.deb
sudo reboot now

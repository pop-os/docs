# Create Pop!\_OS Installation Media

Pop!\_OS can be run from a USB drive in a live environment. You can use the live USB to install Pop!\_OS permanently on a system, demo Pop!\_OS without installing, or use the drive as a system recovery tool.

---
## Preparation

Creating a bootable Pop!\_OS USB drive requires three components:

- A USB flash drive. The flash drive must have at least 8 GB of free space. All data on the flash drive will be lost during the creation process.

- The Pop!\_OS.iso image: [Download Pop!\_OS at this link.](https://pop.system76.com/)

- A program to write the Pop!\_OS.iso image to the flash drive. Reference the table below for popular image flashing software.

| Program | OS Compatibility |
|-----------|-------------|
| [balenaEtcher](https://www.balena.io/etcher/) | Windows, macOS, Linux |
| [Popsicle](https://github.com/pop-os/popsicle)  |  Linux  |
| [Rufus](https://rufus.ie/en/)  |  Windows |

## Choose a Pop!\_OS Image

Pop!\_OS offers its ISO image in 3 varieties:

- **Intel/AMD** - An ISO that does not include propriety NVIDIA drivers.

>**Note**: If you accidentally install the non-NVIDIA version on a PC with a discrete NVIDIA GPU, run `sudo apt install system76-driver-nvidia` in a Terminal session to obtain the missing drivers.

- **NVIDIA** - An ISO containing proprietary NVIDIA drivers for systems with discrete NVIDIA GPUs.

- **RAS PI 4** - An ISO image compatible with the ARM64 processor in a Raspberry Pi 4.

## Create the Installation Media

This process will vary depending on the host operating system. Refer to the appropriate page for your current operating system. 

- [Create a Bootable Pop!\_OS USB in Linux](bootable-usb-using-linux.md)
- [Create a Bootable Pop!\_OS USB in Windows](bootable-usb-using-windows.md)
- [Create a Bootable Pop!\_OS USB in MacOS](bootable-usb-using-macos.md)

# Create a Bootable Pop!_OS USB in Linux

Use this guide to create Pop!_OS bootable USB media from Linux:

- Install ISO flashing software.
- Download the Pop!_OS.iso file.
- Verify the ISO.
- Flash the ISO to your USB storage device.

---
## I. Install Popsicle

![Popsicle Icon](/images/create-bootable-usb-linux/popsicle-icon.png)

Create a bootable USB drive for Pop!_OS using Popsicle. Popsicle is a Linux utility for flashing multiple USB devices in parallel, written in Rust.

>**Note**: Intermediate to advanced Linux users may prefer alternative imaging software programs. USB boot media creation for the Pop!_OS.iso requires no special considerations compared to other Linux distros. Skip this section if you are familiar with creating bootable USB media in Linux.

Popsicle's installation process may vary depending on your distribution. If you are already running Pop!_OS, skip to the USB creation steps.

### Ubuntu & Ubuntu-based Distributions

#### Apt

1. Add the System76 PPA. 

```[bash]
sudo add-apt-repository ppa:system76/pop
```

2. Install Popsicle with the below command.

```[bash]
sudo apt install popsicle popsicle-gtk
```

3. Remove the System76 PPA to prevent messages prompting to upgrade Pop!_OS.

```bash
sudo add-apt-repository -r ppa:system76/pop
```

#### Flatpak

Linux users with [Flatpak installed](https://flatpak.org/setup/) in their distribution can simply download and install the [Popsicle flatpak](https://flathub.org/apps/details/com.system76.Popsicle) from Flathub. 

### Other Linux Distributions

Refer to the README.md file in the official [Popsicle github repository.](https://github.com/pop-os/popsicle)

## II. Download the Pop!_OS.iso File

![Linux Download ISO](/images/create-bootable-usb-linux/using-linux-download-iso.png)

Download the appropriate Pop!_OS.iso file for your target system. See the [preparation guide](create-bootable-usb.md#standard-nvidia--ras-pi-4-isos) for information about each version.

## III. Verify the Pop!_OS.iso File

You should verify that your download matches the checksum before trying to install. This ensures that you've received the full, complete download and that it is not corrupted. Compare the hash values generated using the below commands to the values shown on the Pop!_OS download page. **Do not use the image below to verify hash values.**

>**Note**: Popsicle also provides a feature for easily checking the SHA256 checksum of an ISO file. Skip this section if you prefer a GUI method.

![Compare Hash Values](/docs/images/create-bootable-usb-linux/compare-hash-values.png)

When entering the appropriate checksum command below, ensure:

- The file name in your command matches the downloaded ISO in your local directory. 
- The examples below use the ~/Downloads folder. Make sure the appropriate explicit or relative path is used in your command.

### Verify the Intel/AMD ISO

```bash
sha256sum Downloads/pop-os_21.10_amd64_intel_7.iso
```

### Verify the NVIDIA ISO

```bash
sha256sum Downloads/pop-os_21.10_amd64_nvidia_7.iso
```

### Verify the RASP PI 4 ISO

```bash
sha256sum Downloads/pop-os_21.10_arm64_raspi_7.img.xz
```

## IV. Create the Bootable USB

Flash your USB media with the Pop!_OS.iso image. Note that this process will completely erase all previous data on the USB storage device.

1. Launch Popsicle. The app may display as USB Flasher in search results.

![Launch Popsicle](/images/create-bootable-usb-linux/launch-popsicle.png)

2. Click `Choose Image`.

![Choose Image](/images/create-bootable-usb-linux/choose-image.png)

3. Navigate to local directory with your Pop!_OS.iso file and select it.

>**Note**: You can optionally check the hash of the ISO file in this step before clicking `Next`.

![Find Image](/images/create-bootable-usb-linux/find-image.png)

4. Click `Next`. 

5. Select the USB installation media. Click `Next`.

![Select Media](/images/create-bootable-usb-linux/select-media.png)

6. Enter your system password if prompted; then wait for the installation to complete.

![Flashing Process](/images/create-bootable-usb-linux/flashing-process.png)

7. Click `Done` when the process completes. 

## V. Next Steps

Use your bootable Pop!_OS USB to demo, install, or recover a current Pop!_OS installation.

### Install Pop!_OS

Poweroff the target computer and insert the bootable USB. Power on the computer and enter the boot device menu selection for your BIOS or UEFI system. Follow the steps in the [Standard Installation](/Getting-Started/Installation/installation.md) section.

>**Note**: If your computer has Secure Boot Enabled; it must be disabled before installing Pop!_OS. See [Microsoft's official documentation](https://docs.microsoft.com/en-us/windows-hardware/manufacture/desktop/disabling-secure-boot?view=windows-10) for this procedure.

### Demo Pop!_OS

Use the bootable USB to demo Pop!_OS as a live system.
<!--This chapter will be linked when completed-->

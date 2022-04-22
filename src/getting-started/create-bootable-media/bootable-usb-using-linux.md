# Create a Bootable Pop!_OS USB in Linux

This section explains the process of creating a bootable Pop!\_OS USB in Linux using Popsicle.

- [Install ISO flashing software.](/getting-started/create-bootable-media/bootable-usb-using-linux.html#install-popsicle)
- [Download the Pop!_OS.iso file.](/getting-started/create-bootable-media/bootable-usb-using-linux.html#download-the-pop_osiso-file)
- [Flash the ISO to your USB storage device.](/getting-started/create-bootable-media/bootable-usb-using-linux.html#create-the-bootable-usb)

---

## Install Popsicle

Popsicle is a Linux utility for flashing multiple USB devices at once. You can install Popsicle as an AppImage or a Flatpak.

### AppImage

1. Download the Popsicle AppImage from this [Popsicle repository.](https://github.com/pop-os/popsicle/releases/latest)

2. Navigate to the downloaded AppImage. Right-click the AppImage and select `Properties`.

3. Select the `Permissions` tab and check the `Execute` box.

![AppImage Execute Permission](/images/create-bootable-usb-linux/appimage-execute.png)

4. Double click the Popsicle AppImage to launch it.

### Flatpak

1. Follow the instructions on [Flatpak.org](https://flatpak.org/setup/) if Flatpak is not installed in your Linux distribution.

2. Open a Terminal session and enter this command: 

```bash
flatpak install flathub com.system76.Popsicle
```

3. Enter this command to launch Popsicle: 

```bash 
flatpak run com.system76.Popsicle
```

## Download the Pop!_OS.iso File

![Linux Download ISO](/images/create-bootable-usb-linux/using-linux-download-iso.png)

Download the appropriate Pop!_OS.iso file for your target system. See the [preparation guide](/getting-started/create-bootable-media/create-bootable-usb.html#choose-a-pop_os-image) for information about each version. 

Take note of the hash value for your chosen ISO. Use this value to verify the integrity of the ISO file in step four of the installation process.

![Compare Hash Values](/images/create-bootable-usb-linux/compare-hash-values.png)

## Create the Bootable USB

Flash your USB media with the Pop!_OS.iso image. Note that this process will completely erase all previous data on the USB storage device.

1. Launch Popsicle. The app may display as USB Flasher in search results.

![Choose Image](/images/create-bootable-usb-linux/launch-popsicle-app.png)

2. Click `Choose Image`.

![Launch Popsicle](/images/create-bootable-usb-linux/choose-image.png)

3. Navigate to the local directory with your Pop!_OS.iso file and select it.

![Find Image](/images/create-bootable-usb-linux/find-image.png)

4. Click the drop down menu next to `Hash` and choose `SHA256`, then click `Check`. Compare the hash result to the value you saw when selecting your Pop!\_OS.iso file.

![Verify ISO](/images/create-bootable-usb-linux/verify-iso.png)

4. Click `Next`. 

5. Select the USB installation media. Click `Next`.

![Select Media](/images/create-bootable-usb-linux/select-media.png)

6. Enter your system password if prompted, then wait for the installation to complete.

![Flashing Process](/images/create-bootable-usb-linux/flashing-process.png)

7. Click `Done` when the process completes. 

## Next Steps

Use your bootable Pop!_OS USB to demo, install, or recover a current Pop!_OS installation.

### Install Pop!_OS

Power off the target computer and insert the bootable USB. Power on the computer and enter the boot device menu selection for your BIOS or UEFI system. Follow the steps in the [Standard Installation](/getting-started/installation/installation.md) section.

### Demo Pop!_OS

Use the bootable USB to demo Pop!_OS as a live system.
<!--This chapter will be linked when completed-->

# Create a Bootable Pop!\_OS USB in Windows 10

This section explains the process of creating a bootable Pop!\_OS USB in macOS using balenaEtcher.

- [Install ISO flashing software.](/getting-started/create-bootable-media/bootable-usb-using-windows.html#install-etcher)
- [Download the Pop!\_OS.iso file.](/getting-started/create-bootable-media/bootable-usb-using-windows.html#download-the-pop_osiso-file)
- [Verify the Pop!\_OS.iso hash value.](/getting-started/create-bootable-media/bootable-usb-using-windows.html#verify-the-hash-value)
- [Flash the ISO to your USB storage device.](/getting-started/create-bootable-media/bootable-usb-using-windows.html#create-the-bootable-usb)

---

## Install Etcher

1. Navigate to Etcher's [download page](https://www.balena.io/etcher/) and click `Download for Windows (x86|x64)`.

    ![Download Etcher](/src/images/create-bootable-usb-win10/download_etcher.png)

2. Navigate to the downloaded executable and run it.

    ![Run Etcher Executable](/src/images/create-bootable-usb-win10/run-etcher-exe.png)

3. Click `I Agree` and wait for the installation to complete.

    ![Install Etcher](/src/images/create-bootable-usb-win10/install-etcher.png)

4. Wait for the installation process to complete.

    ![Complete Installation](/src/images/create-bootable-usb-win10/complete-install.png)

## Download the Pop!\_OS.iso File

![Linux Download ISO](/src/images/create-bootable-usb-linux/using-linux-download-iso.png)

Download the appropriate Pop!\_OS.iso file for your target system. See the [preparation guide](/getting-started/create-bootable-media/create-bootable-usb.html#choose-a-pop_os-image) for information about each version.

Take note of the hash value for your chosen ISO. Use this value to verify the integrity of the ISO file.

![Compare Hash Values](/src/images/create-bootable-usb-linux/compare-hash-values.png)

## Verify the Hash Value

1. Launch the Windows Command Prompt.

    ![Launch CMD](/src/images/create-bootable-usb-win10/launch-cmd.png)

2. Navigate to the folder where the Pop!\_OS.iso file is located. The user's Downloads folder is used in the below example. Substitute your username for `USERNAME`.

    ```bash
    cd C:\Users\USERNAME\Downloads
    ```

3. Use the `CertUtil` program to verify your ISO file. Make sure the name of the ISO matches exactly what is in your folder. The filename varies depending on the ISO version you chose.

    ```bash
    CertUtil -hashfile pop-os_21.10_amd64_intel_8.iso sha256
    ```

4. This command will output a long string of characters. Compare the output to the appropriate hash value on the Pop!\_OS download site.

## Create the Bootable USB

Flash your USB media with the Pop!\_OS.iso image. Note that this process will completely erase all previous data on the USB storage device.

1. Launch Etcher if it is not already running.

2. Select `Flash from file`, then navigate to and select your Pop!\_OS.iso file.

    ![Flash From File](/src/images/create-bootable-usb-win10/flash-from-file.png)

3. Click `Select target` and select your USB drive.

    ![Select Target](/src/images/create-bootable-usb-win10/select-target.png)

4. Click `Flash!`.

    ![Click Flash](/src/images/create-bootable-usb-win10/click-flash.png)

5. Close Etcher once the installation completes.

    ![Click Finish](/src/images/create-bootable-usb-win10/click-finish.png)

## Next Steps

Use your bootable Pop!\_OS USB to demo, install, or recover a current Pop!\_OS installation.

### Install Pop!\_OS

Follow the steps in the [Standard Installation](/getting-started/installation/installation.md) section.

### Demo Pop!\_OS

Use the bootable USB to demo Pop!\_OS as a live system.
<!--This chapter will be linked when completed-->

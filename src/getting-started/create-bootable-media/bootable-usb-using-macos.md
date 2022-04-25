# Create a Bootable Pop!\_OS USB in macOS

This section explains the process of creating a bootable Pop!\_OS USB in macOS using balenaEtcher.

- [Install ISO flashing software.](/getting-started/create-bootable-media/bootable-usb-using-macos.html#install-etcher)
- [Download the Pop!\_OS.iso file.](/getting-started/create-bootable-media/bootable-usb-using-macos.html#download-the-pop_osiso-file)
- [Verify the Pop!\_OS.iso hash value.](/getting-started/create-bootable-media/bootable-usb-using-macos.html#verify-the-hash-value)
- [Flash the ISO to your USB storage device.](/getting-started/create-bootable-media/bootable-usb-using-macos.html#create-the-bootable-usb)

---

## Install Etcher

1. Navigate to Etcher's [download page](https://www.balena.io/etcher/) and click `Download for macOS`.

![Download Etcher](/images/create-bootable-usb-macos/download-etcher.png)

2. Click the Downloads folder from the Dock and select the Etcher .dmg file.

![Run Etcher dmg](/images/create-bootable-usb-macos/run-etcher-dmg.png)

3. Drag the Etcher logo into the applications folder.

![Install Etcher](/images/create-bootable-usb-macos/install-etcher.png)

## Download the Pop!\_OS.iso File

![Linux Download ISO](/images/create-bootable-usb-linux/using-linux-download-iso.png)

1. Download the appropriate Pop!\_OS.iso file for your target system. See the [preparation guide](/getting-started/create-bootable-media/create-bootable-usb.html#choose-a-pop_os-image) for information about each version.

2. Take note of the hash value for your chosen ISO. Use this value to verify the integrity of the ISO file.

![Compare Hash Values](/images/create-bootable-usb-linux/compare-hash-values.png)

3. If prompted, confirm you want to allow downloads from pop.system76.com.

## Verify the Hash Value

1. Click the Launchpad icon, then search for `terminal`. Click the `Terminal` icon to launch it.

![Launch Terminal](/images/create-bootable-usb-macos/launch-terminal.png)

2. Change directory to the folder containing your Pop!\_OS ISO file. In this example, the ISO is in the Downloads folder.

```bash
cd Downloads
```

3. Use the `shasum` command to verify your ISO file. Make sure the name of the ISO matches exactly what is in your folder. The filename varies depending on the ISO version you choose.

```bash
shasum -a 256 pop-os_21.10_amd64_intel_8.iso
```

4. This command will output a long string of characters. Compare the output to the appropriate hash value on the Pop!\_OS download site.

## Create the Bootable USB

1. After installation, click the Launchpad icon on the Dock. Select the `balenaEtcher` icon to launch the app. If prompted, confirm you want to open the app.

![Launch Etcher](/images/create-bootable-usb-macos/launch-etcher.png)

2. Select `Flash from file`, then navigate to and select your Pop!\_OS.iso file.

![Flash From File](/images/create-bootable-usb-macos/flash-from-file.png)

3. Click `Select target` and select your USB drive.

![Select Target](/images/create-bootable-usb-macos/select-target.png)

4. Click `Flash!`. Enter your password if prompted.

![Click Flash](/images/create-bootable-usb-macos/click-flash.png)

5. Close Etcher once the installation completes.

![Click Finish](/images/create-bootable-usb-macos/click-finish.png)

## Next Steps

Use your bootable Pop!\_OS USB to demo, install, or recover a current Pop!\_OS installation.

### Install Pop!\_OS

Follow the steps in the [Standard Installation](/getting-started/installation/installation.md) section.

### Demo Pop!\_OS

Use the bootable USB to demo Pop!\_OS as a live system.
<!--This chapter will be linked when completed-->
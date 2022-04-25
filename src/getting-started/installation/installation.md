# Installing Pop!\_OS

The Pop!\_OS installer guides the user through setup of basic system settings.

- Verify system and installation requirements.
- Choose a locale and keyboard language.
- Perform system hard drive selection and partitioning (advanced).
- Create a user account.
- Enable system disk encryption.

---

## Requirements

### System Specifications

| Component | Requirement | Recommended |
|-----------|-------------|-------------|
| CPU       | 64-bit x86 architecture |
| RAM       | 2 GB        | 4 GB        |
| Drive Storage | 20 GB   |             |

### Secure Boot

Systems with Secure Boot enabled must disable this feature before installing Pop!\_OS. Secure boot can be disabled in the BIOS of most computers; however, the process to disable secure boot will vary by laptop and motherboard model.

### Installation Media

The Pop!\_OS.iso can be easily flashed to a USB drive. See [Create a Bootable Pop!\_OS USB.](/getting-started/create-bootable-media/create-bootable-usb.md)

### Installation Media Selected as Boot Device

Power off the target computer and insert the bootable USB. Power on the computer and enter the boot device menu selection for your BIOS or UEFI system. The table below lists lists several common methods for System76 laptops and desktops. Consult your computer manufacturer's documentation to access this menu on third-party computers.

| Firmware               | BIOS key | Boot Menu key                    |
|:----------------------:|:--------:|:--------------------------------:|
| Laptop - Open Firmware | ESC      | ESC (select one time boot option) |
| Laptop - Proprietary   | F2       | F7                               |
| Older Laptops          | Depends on the system | F1                  |
| Thelio                 | Del      |  F8 or F12                       |
| Meerkat                | F2       | F10                              |

---

## Pop!\_OS Installation

1. Choose a language.

![Choose Language](/images/installation/choose-language.png)

2. Select a locale.

![Language Region](/images/installation/language-region.png)

3. Select a keyboard input language.

![Keyboard Language](/images/installation/keyboard-language.png)

4. Select a keyboard layout.

![Keyboard Layout](/images/installation/keyboard-language2.png)

5. Choose the `Clean Install` option for a standard installation. This is the best option for new Linux users, but be aware that this will erase all contents of the target drive.

>**Note**: The `Custom (Advanced)` option opens GParted. GParted allows users to choose partition tables and create custom partitions.  <!-- See Using [GParted Custom (Advanced)](advanced-installation.md) for more information. -->

![Clean Install](/images/installation/clean-install.png)

6. Choose the target drive for the OS installation. Click `Erase and Install`.

![Select Drive](/images/installation/select-system-drive.png)

7. Enter your first and last name (or a display name). A suggested username will populate in the User Name field.

>**Tip**: You don't need to type your username when logging into Pop!\_OS normally, but it can be handy to remember when logging into a terminal session, logging in remotely via SSH, or performing certain configurations.

![Enter Username](/images/installation/enter-username.png)

8. Enter the account password.

![Enter Password](/images/installation/enter-password.png)

9. Choose to encrypt the drive, and optionally create a separate encryption password.

>**Note**: Encrypting the system disk ensures user data is secure in the event that someone gains unauthorized physical access to the device. 

![Encrypt Drive](/images/installation/encrypt-drive.png)

10. Wait for the installation to complete. Click `Restart Device` when prompted.

![Restart System](/images/installation/restart-system.png)

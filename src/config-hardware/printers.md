# Setting up Printers

Most printers are plug-and-play in Pop!\_OS. Add a network or USB-connected printer in `Settings` ➞ `Printers`. Click `Add a Printer` to automatically search for any connected printers. Add a printer manually by clicking `Additional Printer Settings`.

![Printer Settings Screen](/images/printers/printer-settings.png)

Pop!\_OS uses the Common Unix Printing System (CUPS) print server to manage print jobs, manage print queues, and recognize connected printers. While CUPS recognizes a wide range of printer models, printer functionality may vary. Check if your printer is compatible using <a href="https://www.openprinting.org/printers" target="_blank">OpenPrinter.com</a>.

---

## Adding a Printer in the Settings Application

Most printers will be automatically added to the computer. If a printer is not automatically added, you can manually add printers in `Settings` ➞ `Printers`.

1. Press the `Super` key and type the word "Printers".

2. Choose the `Printers` result the search box.

3. In the `Printers` settings panel, click the `Add a Printer...` button to search for locally connected printers.

    ![Click Add a Printer](/images/printers/add-a-printer.png)

4. Wait a few seconds for printers to appear in the Device List.

5. Select your printer and click `Add`.

    ![Click Add](/images/printers/click-add.png)

## Checking Printer Status in CUPS

CUPS can be managed directly using a web browser by navigating to the following local URL:

<a href="http://localhost:631" target="_blank">localhost:631</a>

The status window will show current print jobs, detected printers, and other information about the printing system.

![CUPS Status Window](/images/printers/cups-settings.png)

### Adding Users to the lpadmin Group

CUPS allows you to manage printers using Terminal commands. Configuring printers requires that the user is a part of the `lpadmin` group. You can confirm you are a part of this group with the following command:

```bash
groups
```

You can add yourself to this group using the below command:

```bash
sudo usermod -aG lpadmin $USER
```

If you prefer to manage printers in Terminal, See the [CUPS documentation](https://www.cups.org/doc/admin.html) for full documentation.

### Sharing a Printer to the Local Network

Share a printer with the local network by clicking the `Administration` tab.

![CUPS Administration Tab](/images/printers/admin-tab.png)

Check the box for `Share printers connected to this system`.

Locally shared printers are visible in the `Printers` tab in the `Settings` application. Users with the appropriate group assignments can now select the printer and enter their username and password to gain access to the network printer. If a user is unable to see the printer, see the above section to confirm the user is in the `lpadmin` group, and to add the user to the group.

## HP Printers

HP printers are supported with the hplip package, which is installed by default in Pop!\_OS.

```bash
sudo apt install hplip
```

### HP Device Manager (GUI)

If you would like to use a guided GUI application from HP, you will need to install a python dependency:

```bash
sudo apt install python3-pyqt5
```

Then run `hp-setup` to start the HP Device Manager.

![HP Device Manager](/images/printers/hp-setup.png)

## Brother Printers

Brother provides a driver installation tool for Linux users. Install the appropriate driver for your Brother printer by downloading this tool and running the installer with your printer model appended to the command.

1. Click <a href="https://support.brother.com/g/b/productsearch.aspx?c=us&lang=en&content=dl" target="_blank">this link</a> to search for the appropriate printer.

2. Once you've located your printer, select `Linux (deb)` for your "OS Version", then click `OK`.

3. Select the `Linux (deb)` radio button.

    ![Select deb File](/images/printers/select-deb-file.png)

4. Click `Agree to the EULA and Download`.

5. Choose the `Save File` option if prompted.

6. Press `Super` + `T` to launch the Terminal application.

7. Change directory to where you downloaded the driver (usually the Downloads directory). Unzip the file using this command:

    ```bash
    cd Downloads
    gunzip linux-brprinter-installer-*.gz
    ```

8. Run the installer by typing the unzipped installer name into the terminal.

    > **Note**: Your installer version may differ from this guide. Type the first portion of the installer name as shown below, and then hit `TAB` to complete the installer name. Substitute PRINTERNAME with your exact printer model name.

   ```
   sudo bash linux-brprinter-installer PRINTERNAME
   ```
  
 9. If prompted for a `DeviceURI`, you can find that by navigating to `Settings` ➞ `Printers` ➞ `Additional Printer Settings`, then right-clicking your printer and selecting `Properties`.

    ![Printer Properties](/images/printers/printer-properties.png)

## Epson Printers

Epson printer drivers are in the `printer-driver-escpr` package, which is also installed by default. You may need to install the lsb package for some printer versions:

```bash
sudo apt install lsb printer-driver-escpr
```

## Useful Printer Commands

Reinstall CUPS:

```bash
sudo apt --reinstall cups cups-client
```

Reinstall the system control panel in case printer settings are not available.

```bash
sudo apt install --reinstall system-config-printer
```

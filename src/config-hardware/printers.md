# Setting up Printers

Most printers are plug-and-play in Pop!\_OS. Add a network or USB connected printers in `Settings` ➞ `Printers`. Clicking `Add a Printer` will automatically search for any connected printers. Printers can also be added manually by clicking `Additional Printer Settings`.

![Printer Settings Screen](/images/printers/printer-settings.png)

---

## CUPS and Printer Compatibility

Pop!\_OS uses the Common Unix Printing System (CUPS) print server to manage print jobs, print queues, and recognizes connected printers. While CUPS recognizes a wide range of printer models, printer functionality may vary. Check if your printer is compatible using [OpenPrinter.com](https://www.openprinting.org/printers).

## Checking Printer Status in CUPS

Open this web page to look at the CUPS (Common Unix Printing System) configuration and status window:

[localhost:631](http://localhost:631)

The status window will show current print jobs, detected printers, and other information about the printing system. If you would like to share this printer with others on your local network, click on the 'Admin' link, under Server, click on the "Share printers connected to this system" and save the changes. Other computers on your network should than see that printer. When there is a prompt for your username and password, use your user name, and password used to login.

![CUPS Status Window](/images/printers/cups-settings.png)

CUPS allows you to manage printers using Terminal commands. See the [CUPS documentation](https://www.cups.org/doc/admin.html) for more information.

## Adding a Printer

Most printers will be automatically added to the computer. If a printer is not automatically added, you can manually add printers in `Settings` ➞ `Printers`.

1. Press the `Super` key and type the word Printers.

2. Choose the `Printers` application in the search box.

3. In the `Printers Application`, click the `Add a Printer...` button and a box will pop up with different options.

    ![Click Add a Printer](/images/printers/add-a-printer.png)

4. Wait a few seconds for printers to appear in the Device List.

5. Select your printer and click `Add`.

    ![Click Add](/images/printers/click-add.png)

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

1. Click [this link](https://support.brother.com/g/b/productsearch.aspx?c=us&lang=en&content=dl) to download Brother's Driver Install Tool for Linux while searching for the appropriate printer.

2. Click the `Click here to download the tool` link on the Brother download page.

3. Select Linux (deb) for your "OS Version", then click `OK`.

4. Click `Agree to the EULA and Download`.

5. Choose the `Save File` option when prompted.

6. Press `Super` + `T` to launch the Terminal application.

7. Change directory to where you downloaded the driver (usually the Downloads directory). Unzip the file using this command:

    ```bash
    cd Downloads
    gunzip linux-brprinter-installer-*.gz
    ```

8. Run the installer by typing the unzipped installer name into the terminal.

    > **Note**: Your installer version may differ from this guide. Type the first portion of the installer name as shown below, and then hit <kbd>TAB</kbd> to complete the installer name. Place your exact printer model where we wrote PRINTERNAME below.

   ```
   sudo bash linux-brprinter-installer PRINTERNAME
   ```
  
    > **Note**: If prompted for a "DeviceURI", you can find that by opening up Settings > Printers > Additional Printer Settings, then right click your printer and click Properties. In the resulting window, you'll be able to find your Device URI, as shown in the screenshot below.

    ![Printer Properties](/images/printers/printer-properties.png)

## Epson Printers

Epson printer drivers are in the `printer-driver-escpr` package and is also installed by default. You may need to install the lsb package for some printer versions:

```bash
sudo apt install lsb printer-driver-escpr
```

Automatically installed printers will work fine, but if you need to make changes to the configuration of the printers, you will need to add your user to the `lpadmin` group. To do that run the following command:

```bash
sudo usermod -aG lpadmin $USER
```

## Useful Printer Commands

This command reinstalls CUPS:

```bash
sudo apt install --reinstall cups cups-client
```

This command reinstalls the system control panel if the settings are not available.

```bash
sudo apt install --reinstall system-config-printer
```

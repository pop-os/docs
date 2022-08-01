# Default Applications

Options to set the default web browser, email client, calendar application, music player, video player, and photo viewer are located in `Settings` ➞ `Default Applications`. This menu allows setting a single application as the default handler for a larger number of similar file types.

![Default Applications](/images/application-settings/default-applications.png)

Designate an application as the default by selecting it from the dropdown menu. If no appropriate application is installed to handle a media type, the dropdown selection will be grayed out. <!--link to installing applications section when complete-->

![Select Default](/images/application-settings/select-default.png)

## Set Default Applications Using the File Manager

Launch the file manager and navigate to the file you want to open. Right click the file and select `Properties`.

![File Properties](/images/application-settings/file-properties.png)

Click the `Open With` tab and choose the appropriate program from the list.

![Open With](/images/application-settings/open-with.png)

## Set Default Applications Using the Terminal

### Modify the MIME Apps List File

The `mimeapps.list` file contains entries associating applications with specific links and MIME file types. Application names listed in this file will be appended with `.desktop`.

1. Determine your application's .desktop name using this command to list all .desktop applications:

    ```bash
    ls /usr/share/applications
    ```

Take note of your desired default application's .desktop name, or leave this Terminal window open and start a new Terminal session to complete the next steps.

>**Note**: The `/usr/share/applications` directory will show most system-wide apps installed, but it won't show user-local apps; apps can be placed in any of the directories you see in the output of echo $XDG_DATA_DIRS. For example, Flatpak apps are installed to ~/.local/share/flatpak/exports/share/applications/ by default.

2. Open the `mimeapps.list` file using this command:

    ```bash
    nano ~/.config/mimeapps.list
    ```

4. Locate the file MIME type entry and edit it using the .desktop application name. For example, this entry specifies that all .webm files are opened with VLC media player by default:

    ```bash
    video/webm=vlc.desktop;
    ```

If a file's MIME type is not listed in `mimeapps.list`, you can determine a file's MIME type by navigating to the file's location and using the `mimetype` command:

```bash
mimetype my-image.png
my-image.png: image/png
```

Then create an entry in the `[Added Associations]` section of the `mimeapps.list` file:

```bash
image/png=deepin-image-viewer.desktop;
```

### Using the `mimeopen` Command

Launch a Terminal session, navigate to your file, and type this command:

```bash
mimeopen -d my-image.png
```

Enter a number to correspond with a listing in the output:

```
Please choose a default application for files of type image/png

	1) Deepin Image Viewer  (deepin-image-viewer)
	2) GNU Image Manipulation Program  (org.gimp.GIMP)
	3) Gwenview  (org.kde.gwenview)
	4) ksnip  (org.ksnip.ksnip)
	5) ImageMagick (color depth=q16)  (display-im6.q16)
	6) Firefox Web Browser  (firefox)
	7) Image Viewer  (org.gnome.eog)
	8) Other...
```

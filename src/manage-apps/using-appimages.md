# AppImages

The AppImage format packages an application in a single, self-contained file. This format allows for a simplified installation process. [Appimage.github.io](https://appimage.github.io/) provides links to download hundreds of applications as AppImages. Once downloaded, an AppImage must be given execute permissions in order to launch.

---

## Downloading an AppImage

1. Navigate to [appimage.github.io](https://appimage.github.io/) and click the `Download` button next to an application.

    ![Click Download](/images/using-appimages/click-download.png)

2. The link may take you to the application's GitHub repository. Download the latest stable version of the AppImage. Make sure you download the compatible version for your 32-bit (i386) or 64-bit (x86-64) CPU architecture. All modern personal computers will have a 64-bit CPU.

    ![Download AppImage](/images/using-appimages/download-appimage.png)

3. Navigate to the downloaded AppImage. Right-click the AppImage file and choose `Properties`.

    ![Choose Properties](/images/using-appimages/choose-properties.png)

4. Select the `Permissions` tab and check the box for `Execute`.

    ![Execute Permissions](/images/using-appimages/execute-permissions.png)

5. Close the `Properties` window and double-click the AppImage to launch it, or right click the AppImage and select `Run`.

    ![Launch AppImage](/images/using-appimages/launch-appimage.png)

## Updating an AppImage

AppImages are easily updated by downloading the latest version to replace the currently downloaded AppImage. Alternatively, the [AppImageUpdate](https://github.com/AppImage/AppImageUpdate) project provides a method for keeping AppImage applications up-to-date.

### Installing AppImageUpdate

Download the latest AppImageUpdate version from [its Github repository](https://github.com/AppImage/AppImageUpdate/releases/continuous). Again, make sure you download the compatible version for your CPU architecture.

![Download AppImageUpdate](/images/using-appimages/download-appimageupdate.png)

Navigate to the file and right-click it. Select `Properties` and click the `Permissions` tab. Check the box next to `Execute`.

![Execute Permissions-2](/images/using-appimages/execute-permissions2.png)

### Updating an AppImage with AppImageUpdate

Launch AppImageUpdate by double-clicking its .AppImage file, navigate to the location of the AppImage application that you wish to update, and then select it and click `Open`.

![Click Open](/images/using-appimages/click-open.png)

AppImageUpdate will fetch the latest version of the AppImage, and the selected AppImage will have .old appended to its name.

![New Version](/images/using-appimages/new-version.png)

## Deleting an AppImage

Simply select the AppImage file and press `Del` on your keyboard, right click and choose `Move to Trash`, or click and drag the AppImage to the trash.

![Move to Trash](/images/using-appimages/move-to-trash.png)

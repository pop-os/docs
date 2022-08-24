# The Pop!\_Shop

Pop!\_OS includes a GUI application called the Pop!\_Shop for easy installation and management of open-source and proprietary applications. Packages listed in the Pop!\_Shop reference several sources:

- **Debian (.deb) Packages** - Debian packages from default sources are referenced from System76's worldwide CDN. This CDN combines mirrored Ubuntu repositories with applications packaged specifically for Pop!\_OS. This dedicated CDN also provides Pop!\_OS users with improved bandwidth and resource up-time.
- **Flatpak Applications** - The Pop!\_Shop also references Flathub applications hosted on [FlatHub.org](https://flathub.org/home).
- **AppStream Data from Third-party Repositories** - Applications will appear in the Pop!\_Shop if the user configures third-party repositories in Repoman, and the application provides AppStream metadata to the Pop!\_Shop.

---

## Pop!\_Picks

Pop!\_Picks offers a curated list of applications that System76 recommends to developers and general users.

![Pop Picks](/images/using-pop-shop/pop-picks.png)

## Recently Updated

Find applications with recent developer support.

![Recently Updated](/images/using-pop-shop/recently-updated.png)

## Categories

Find the appropriate application by category.

![Application Categories](/images/using-pop-shop/application-categories.png)

## Installing Applications through the Pop!\_Shop

1. Open the Pop!\_Shop by clicking the rocket ship icon in the dock, or by pressing `SUPER` and typing “pop shop”.

    ![Launch Pop Shop](/images/using-pop-shop/launch-pop-shop.png)

2. Type the application's name in the search field.

    ![Search Apps](/images/using-pop-shop/search-apps.png)

3. Some applications will provide the option to install either a Flatpak or Deb version. See [AppImages, Flatpaks, & Deb Packages](managing-applications.md#appimages-flatpaks--deb-packages) for a comparison of these packages types.

    ![Select Package Type](/images/using-pop-shop/select-package-type.png)

4. Click `Install`.

## Updating Applications through the Pop!\_Shop

Click `Installed` in the top middle of the window.

![Click Installed](/images/using-pop-shop/click-installed.png)

Click `Update` next to an app to update an individual application. To apply all updates, select `Update All`.

![Select Update](/images/using-pop-shop/select-update.png)

>**Note**: If you experience errors updating packages using the Pop!\_Shop, it's possible these can be easily resolved by [running simple maintenance](fix-packages.md) commands that clean up `apt` and Flatpak packages.

## Removing Applications through the Pop!\_Shop

Select the application that you want to remove from the `Installed` list.

![Select App](/images/using-pop-shop/select-app.png)

Select `Uninstall`.

![Select Uninstall](/images/using-pop-shop/select-uninstall.png)

<!--## Sections 

**Pop!_Picks**

These tools are recommended by System76 to improve your user experience and workflow efficiency.

![]

**Recently Updated**

This list displays applications with recently applied updates. For more information about updating applications in the Pop!\_Shop, see [Updating Applications through the Pop!\_Shop](update-apps.md#updating-applications-through-the-pop_shop)

![]

**Categories**

In addition to search, you can find applications organized by categories. Categories include: 

- Accessories
- Audio
- Communication
- Development
- Education
- Finance
- Games
- Graphics
- Internet
- Math, Science, & Engineering
- Media Production
- Office
- Privacy & Security
- System
- Universal Access
- Video
- Writing & Language

-->
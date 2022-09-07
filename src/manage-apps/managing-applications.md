# Managing Applications

Users can install, update, and remove application packages using GUI and CLI options in Pop!\_OS.

- [Manage applications with Pop!_OS's built-in app store](using-pop-shop.md) - Find, install, update, and remove software packages using the Pop!\_Shop.
- [Download and install applications from a publisher's web site](using-eddy.md) - Download Debian packages from the internet and install them using a simple GUI utility called Eddy.
- [Download and immediately run your applications without installing](using-appimages.md) - Quickly add applications using self-contained AppImages.
- [Install, update, and remove applications using typed commands](using-terminal.md) - Use apt (Advanced Package Tool) or Flatpak to install applications using the Terminal.
- [Manage repositories](manage-repos.md) - Install packages even if they're not available in commonly-used repositories by adding new sources with Repoman or the Terminal.
- [Resolve package issues](fix-packages.md) - Use Terminal commands to securely remove packages and fix common package errors for `apt` and Flatpak packages.

---

## Installing Applications in Pop!\_OS

In Linux, applications can share libraries of code in order to streamline software development and deployment. These libraries are grouped into packages. Packages required by an application are called **dependencies**. When you install an application in Pop!\_OS, an application's dependencies are downloaded to your computer.

Pop!\_OS comes pre-packaged with several tools for installing software applications.

- [Using the Pop!\_Shop](using-pop-shop.md) - Manage applications using a GUI interface. Applications in the Pop!\_Shop are downloaded from System76's worldwide CDN, which mirror's Ubuntu's repositories for .deb packages. The Pop!\_Shop also displays Flatpak applications from [FlatHub.org](https://flathub.org/home), and any apps with AppStream data from third-party repositories that are configured in Repoman.
- [Using Eddy](using-eddy.md) - Install .deb packages downloaded from the web.
- [Using the Terminal](using-terminal.md) - Manage applications packaged as .deb files and Flatpaks using typed commands.

## AppImages, Flatpaks, & Deb Packages

Different formats use different strategies to ensure all dependencies are present. Some methods are more convenient and include all dependencies, while others provide efficiency by checking to see if any of the required dependencies are already on your computer.

- **Flatpaks** - Flatpaks install a “containerized” version of the software. This means the software runs in its own sandbox and the installation will include all dependencies (called [runtimes](https://docs.flatpak.org/en/latest/basic-concepts.html#runtimes)) and libraries required by the application. By default, Flatpaks pull all dependencies from [FlatHub.org](https://flathub.org/home). Additional Flatpak repositories can be configured using [Repoman](manage-repos-repoman.md#managing-flatpak-repositories-with-repoman).
- **Deb Packages** - Deb is the package format used by Debian-based distributions. This is the package type that `apt` will handle when installing applications via the Terminal. You can also download .deb packages online and install them with Eddy.
- **AppImage** - An AppImage is a completely self-contained single file that includes all required dependencies. Users only need to download the file to their local storage and provide it with execute privileges.

<!--define open source?-->
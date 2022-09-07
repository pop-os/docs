# Installing Applications with the Terminal

The Terminal provides more flexibility and efficiency when installing applications. Apt and Flatpak are powerful package management tools that allow users to install, update, and remove packages using simple and intuitive commands.

---

## Understanding Package Managers

A package manager is an application that keeps track of packages' files on your computer. A package manager can also verify and retrieve dependencies for any program the user wishes to install, and check for updates for currently installed programs.

### The Advanced Packaging Tool (apt)

Pop!\_OS comes preinstalled with the Advanced Packaging Tool (`apt`). `apt` is a package manager that lies on top of another package manager called `dpkg`. When a user wants to update their system or a single application, `apt` checks for its dependencies, downloads the the application and its dependencies, and installs them. `apt`  accomplishes this by referencing online package databases called repositories.

| Tool | Functionality | Use Cases |
|------|---------------|-----------|
| apt  | <ul><li>Handle dependency resolution and update checking.</li><li>Download packages from online repositories. | Install, update, or remove applications or the entire system. |
| dpkg | <ul><li>Install and remove files within a package.</li><li>Run application pre-install and post-install configuration scripts.</li><li>Keep track of packages' files on the system.</li><li>Install downloaded applications (without dependency resolution).</li></ul> | Advanced troubleshooting for package issues. |

`dpkg` can install applications downloaded in the .deb format. However, `dpkg` does not have `apt`'s functionality for downloading applications, or for automatically fetching and installing dependencies. `dpkg` commands remain a useful tool for troubleshooting package issues.

### Flatpak

**Flatpak** is a package format that installs a “containerized” version of the software. This means the software runs in its own sandbox, and the installation will include all dependencies and libraries required by the application. In Flatpak, dependencies are grouped into "runtimes" that are compatible with any Linux distribution. Flatpaks pull all runtimes and libraries from [Flathub.org](https://flathub.org/home) by default. Flatpaks also do not require installing using super user privileges (`sudo`).

## Launching the Terminal

**Apt** and **Flatpak** are command-line based applications that require users to enter typed commands into a Terminal.

You can launch the Terminal using one of these methods:

- Click the Terminal icon in the Dock.
- Press `SUPER` + `T`.
- Press `SUPER` to bring up the launcher, and then type "terminal" and hit `Enter`.

### Using Sudo

Commands beginning with `sudo` tell the Terminal that the command should be run with super user (root) privileges. These privileges are required when installing applications or making other modifications to the operating system. The first time you run `sudo` in a command prompt, you will need to provide your password.

## Managing Applications with apt

It is best practice to run `sudo apt update` before installing any packages with apt. This command fetches the most up-to-date index of all repositories that apt manages.

```bash
sudo apt update
```

### Installing with apt

To install an application, run the command below and substitute [packagename] with the desired application (do not include brackets in the command).

```bash
apt install [packagename]
```

### Updating Applications with apt

Update apt's index:

```bash
sudo apt update
```

Run this command to update a single application:

```bash
sudo apt --only-upgrade install [packagename]
```

Run this command to update the entire system, including all installed applications:

```bash
sudo apt full-upgrade
```

>**Note**: The `full-upgrade` option will downgrade or remove dependencies as necessary when upgrading packages. The `upgrade` option will not perform these tasks. Running the `full-upgrade` option will avoid many dependency and package-related issues that may occur when updating Pop!\_OS.

### Removing Applications with apt

Uninstall an application using the `remove` command.

```bash
sudo apt remove [packagename]
```

>**Note**: The `remove` command removes a single application. However, it may leave behind a small number of configuration files. The `purge` command will completely remove all trace of an application, including residual configuration files. To completely remove a package, [see instructions](fix-packages.md#purge) for using the `autoremove` command with the `--purge` option.

## Managing Applications with Flatpak

### Installing Applications with Flatpak

```bash
flatpak install [packagename]
```

### Updating Applications with Flatpak

Run this command to update a single application using Flatpak:

```bash
flatpak update [packagename]
```

Run this command to update all Flatpak applications on your computer:

```bash
flatpak update
```

### Removing Applications with Flatpak

Run this command to remove a single Flatpak application:

```bash
flatpak uninstall [packagename]
```

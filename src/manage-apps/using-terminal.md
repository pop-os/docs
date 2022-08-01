# Installing Applications with the Terminal

The Terminal provides more flexibility and efficiency when installing applications. Apt and Flatpak are powerful package management tools that allow users to install, update, and remove packages using simple and intuitive commands.

---

## Understanding Package Managers

### Apt

Pop!\_OS comes preinstalled with the **apt**. Apt is a package manager; an application that verifies and retrieves dependencies for any program the user wishes to install. Apt accomplishes this by referencing its own database of packages, called a repository.

### Flatpak

A **Flatpak** is a package format that installs a “containerized” version of the software. This means the software runs in its own sandbox, and the installation will include all dependencies and libraries required by the application. Flatpaks pull all dependencies from flathub.org. Flatpak's also do not require installing using super user privileges.

## Launching the Terminal

**Apt** and **Flatpak** are command-line based applications that require users to enter typed commands into a Terminal.

You can launch the Terminal using one of these methods:

- Click the Terminal icon in the Dock.
- Press `SUPER` + `T`.
- Press `SUPER` to bring up the launcher, and then type "terminal" and hit `Enter`.

**Using Sudo**

Commands beginning with `sudo` tell the Terminal that the command should be run with super user privileges. These privileges are required when installing applications or making other modifications to the operating system. The first time you run `sudo` in a command prompt, you will need to provide your password.

## Managing Applications with Apt

It is best practice to run `sudo apt update` before installing any packages with apt. This command fetches the most up-to-date index of all repositories that apt manages.

```bash
sudo apt update
```

### Installing with Apt

To install an application, run the command below and substitute [packagename] with the desired application (do not include brackets in the command).

```bash
apt install [packagename]
```

### Updating Applications with Apt

Update apt's index:

```bash
sudo apt update
```

Run this commend to update a single application:

```bash
sudo apt --only-upgrade install [packagename]
```

Run this command to update the entire system, including all installed applications:

```bash
sudo apt upgrade
```

### Removing Applications with Apt

Run this command to remove a single application:

```bash
sudo apt remove [packagename]
```

The `remove` command will remove the application, but may leave behind a small number of configuration files. The `purge` command will completely remove all trace of an application, including residual configuration files.

```bash
sudo apt purge [packagename]
```

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
Flatpak uninstall [packagename]
```

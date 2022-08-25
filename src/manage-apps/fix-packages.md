# Package Manager Maintenance

If your system complains about a failed upgrade, package manager conflicts, broken upgrades, or other package-related issues, there are several common fixes to these problems. Some package manager issues can be resolved with the graphical update program, but many require the command line.

___

## General Fixes for Apt Packages

These commands perform general cleanup that can resolve many of `apt`'s errors. These commands should be run one at a time.

```bash
sudo apt clean
sudo apt update -m
sudo dpkg --configure -a
sudo apt install -f
sudo apt full-upgrade
sudo apt autoremove --purge
```

- `apt clean` - The `clean` command clears out the local repository of retrieved package files.
- `apt update -m` - The `-m` option allows the `apt-update` process to continue fetching indexes, even if errors are detected.
- `dpkg --configure -a` - The `--configure -a` command configures any unpacked but not yet configured packages.
- `apt install -f` - The `-f` option attempts to correct broken dependencies
- `apt full-upgrade` - In addition to downloading and installing package updates, `full-upgrade` downgrades or removes dependencies as necessary when upgrading packages.
- `apt autoremove --purge [packagename]` - In addition to removing a package, `autoremove` will remove dependencies no longer required by any installed application. Combining with `purge` will remove any residual configuration files related to the package.
- `apt autoremove --purge` - Running this command with no specified package will remove any packages that were previously dependencies for other installed packages but are no longer required (either because the dependent package was removed, or because the package was updated to no longer depend on certain packages.)

## Fixing Individual Apt Packages

### The reinstall Option

You may see packages that are still broken and need to be installed manually or purged manually. This may indicate that the package has broken or cyclical dependencies.

This command reinstalls the package, which can be useful if the package has many reverse dependencies (the packages that depend on a given package):

```bash
sudo apt install --reinstall [packagename]
```

### The purge Option

>**Note**: Be careful when using `purge` and `autoremove`. Verify the terminal output to confirm the command will only affect the packages you are trying to fix. If unrecognized packages are removed causing unexpected changes, run `sudo apt install pop-desktop` and reboot to ensure those critical Pop!\_OS components are reinstalled.

This command will remove a package and its system-wide configuration files. Use it to remove a package that is causing issues:

```bash
sudo apt purge [packagename]
```

### Using autoremove with purge

Running the `autoremove` option will remove dependencies that are no longer required by any application after removing a package. Removing unneeded dependencies saves disk space, saves network bandwidth (from future updates to those dependencies), and is a good security practice to reduce the attack surface of the system. To remove both the package and all of its dependencies, run:

```bash
sudo apt autoremove --purge [packagename]
```

### Installing a Specific Version with the policy Option

The `policy` option shows the available versions of a package. This is useful if you want to tell apt to install a specific version using the `[packagename]=[version]`.

Use this command to list all available versions for an application:

```bash
apt policy [packagename]
```

Use this command to install a specific version:

```bash
sudo apt install [packagename]=[version]
```

## General Fixes for Flatpak Packages

If the Pop!_Shop is showing an update available, but there are no updates listed on the update page, there may be a Flatpak runtime (a backend program that another Flatpak depends on) with an update available. Run these commands to update all Flatpaks and remove any Flatpak runtimes that are no longer required by any installed programs:

```bash
flatpak update
flatpak uninstall --unused
flatpak repair --user
```

- `flatpak update` - Search for and apply updates updates for installed Flatpak applications.
- `flatpak uninstall --unused` - Remove unused [runtimes](https://docs.flatpak.org/en/latest/basic-concepts.html#runtimes).
- `flatpak repair --user` - Repair Flatpak packages for the current user's installation.

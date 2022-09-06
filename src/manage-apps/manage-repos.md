# Managing Repositories

Pop!\_OS repositories can be managed using Repoman (GUI) or the `apt-manage` command, which is unique to Pop!\_OS.

- [Manage Repositories with Repoman](manage-repos-repoman.md) - Access the Repoman tool through the Pop!\_Shop to add and remove repositories.
- [Manage Repositories with the Terminal](manage-repos-terminal.md) - Use the `apt-manage` or `flatpak` command line tools to add, modify, and remove repositories.  
- [Manually Add and Remove Repositories](manage-repos-manually.md) - Directly modify the `/etc/apt/sources.list.d/` and `~/.local/share/flatpak/repo/` text files that control package sources.

___________

## Understanding Repositories

A repository is developer-maintained online resource that hosts applications' packages. When you use apt or Flatpak, the tool handles requests to download necessary files from a repository for an application. Distributions will have default, or "official" repositories that they use to maintain the applications that a developer chooses to include in the distribution. A repository may also be referred to as a source, repo, or remote (for Flatpak).

Pop!\_OS includes these built-in repositories:

- **http://apt.pop-os.org/ubuntu/** - This is System76's Ubuntu mirror, which is available via a global CDN.
- **https://apt.pop-os.org/release** - This repository provides the released versions of Pop!_OS packages.
- **https://apt.pop-os.org/proprietary** - This repository contains a number of applications not packaged by Ubuntu, or that are out of date on Ubuntu.

If any of these repositories have been removed from a system, they can be added back using the information on [this page](https://apt-origin.pop-os.org/).

## Understanding the Use Case for Third-Party Repositories

Pop!\_OS's official sources listed in Repoman's `Settings` and `Extra Sources` tabs will provide all package resources required for Pop!\_OS's out-of-the-box functionality. This includes all applications included in the default installation and available in the Pop!\_Shop. A third-party repository is required if a desired application's files are not hosted in these official repositories.

### Third-Party Repositories and PPA's

A Personal Package Archive is a type of third-party apt repository that is hosted on Canonical's Launchpad platform. PPAs and third-party repositories allow an application to install and update from unofficial sources. Users should exercise caution when installing these, as their packages are often not examined by community developers. You should only install a PPA or third-party repository from sources you trust.

### Why Use Third-Party Hosting?

Developers may choose to host their application's files outside of a distribution's official repositories for a number of reasons:

- To provide easy and quick access for new and experimental versions of their software.
- To quickly apply bug fixes and updates.
- To provide convenient access to their application to users across Linux distributions.

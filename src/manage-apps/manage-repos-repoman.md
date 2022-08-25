# Managing Repositories with Repoman

Add, remove, and edit repositories using Repoman. Repoman allows users to add apt and Flatpak repositories. Users may want to add an apt repository or additional Flatpak repository if their software is not included in the Pop!\_Shop, or they may want to remove an unneeded repository after uninstalling the only application that required it.

Access Repoman by launching the Pop!\_Shop, clicking the three lines, and then clicking `System Software Sources...`.

![Access Repoman](/images/manage-repos/access-repoman.png)

>**Caution**: Adding 3rd-party apt or Flatpak repositories allows installation of software that has not been validated by System76 or other trusted Linux communities. Software available via 3rd-party apt and Flatpak repositories may not be vetted against packages that introduce security vulnerabilities. Users should take caution and only add external repositories that they trust.
---

## Official Sources

This section lists System76's official Pop!\_OS mirror. This mirror includes installation files and updates for all applications included in a default Pop!\_OS installation. This is also where installation files for many applications in the Pop!\_Shop reside. Changing this mirror is not necessary since Pop!\_OS will automatically download updates from the fastest source using System76's worldwide CDN.

The toggle switches enable or disable software components based on licensing and support:

- **Restricted** - Proprietary drivers and components that are not open source
- **Universe** - Free and open-source software that is community maintained
- **Multiverse** - Software restricted by copyright or legal reasons

![Official Sources Tab](/images/manage-repos/official-sources-tab.png)

## Managing apt Repositories with Repoman

Apt archives (including [PPAs](manage-repos.md#ppas)) are created by developers to distribute software not included in default Ubuntu or Pop!\_OS repositories.

### Viewing Extra Sources

Click on the `Extra Sources` tab to display repositories used by 3rd-party applications.

![Extra Sources](/images/manage-repos/extra-sources.png)

>**Note:** While this page is generally used to add sources for 3rd-party apt repositories, most sources with a URI containing `http://apt.pop-os.org` are critical to Pop!\_OS's desktop functionality and should not be removed. [See this page](https://apt-origin.pop-os.org/) for more information about Pop!\_OS's apt sources.

### Adding an apt Repository

Click the `+` button.

![Click Plus](/images/manage-repos/click-plus.png)

Enter the source details for the repository and click `Add`. Enter your user password when prompted.

![Add Repo](/images/manage-repos/add-repo.png)

The repository will appear in the `Extra Sources` list.

![View Repo](/images/manage-repos/view-repo.png)

### Removing an apt Repository

Select a repository from the list and then click on the trash can icon to delete the repository.

![Remove Repo](/images/manage-repos/remove-repo.png)

Click `Remove` to confirm removal of the PPA.

![PPA Click Remove](/images/manage-repos/ppa-click-remove.png)

## Managing Flatpak Repositories with Repoman

Flatpak uses [FlatHub.org](https://flathub.org/home) by default, but developers may choose to host their own Flatpak repository to offer the latest, potentially unstable, versions of their software.

### Viewing Flatpak Repositories

Access Repoman by launching the Pop!\_Shop, clicking the three lines, and then clicking `System Software Sources...`.

![Access Repoman](/images/manage-repos/access-repoman.png)

Click on the `Flatpak` tab. This tab displays repositories used by Flatpak applications.

![View Flatpak Repo](/images/manage-repos/view-flatpak-repo.png)

### Adding a Flatpak Repository

Click the `+` button.

![Click Flatpak Plus](/images/manage-repos/click-flatpak-plus.png)

Enter the source details for the repository and click `Add`.

![Add Flatpak Repo](/images/manage-repos/add-flatpak-repo.png)

### Removing a Flatpak Repository

Select a repository from the list and then click on the trash can icon to delete the repository.

![Remove Flatpak Repo](/images/manage-repos/remove-flatpak-repo.png)

Click `Remove` to confirm removal of the Flatpak repository.

![Flatpak Click Remove](/images/manage-repos/flatpak-click-remove.png)

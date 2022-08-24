# Directly Editing Repository Configuration Files

Add and remove repositories by directly editing text files located in `/etc/apt/sources.list.d/` (Debian repositories) or `~/.local/share/flatpak/repo/` (Flatpak repositories).

## Manually Adding Debian Debian Repositories

In order to manually create a text file for a repository, it's important to understand the deb822 format. This format organizes a repository's attributes into human-readable fields.

| Field | Function |
|-------|----------|
| X-Repolib-Name | Define the name of the source. This is used by Repoman in the `Source` column of the `Extra Sources` tab.|
| Enabled | Enable or disables the repository.|
| Types | Define the source file or code used to install packages.|
| URIs | Provide the repository's address.|
| Suites | Add the sources used to update packages. This field corresponds with the toggle switches in the `Updates` tab in Repoman.|
| Components | Specify if the source should include software that is open-source, closed-source, officially supported by canonical, or community-maintained. This option corresponds with the toggle switches in the `Settings` tab in Repoman.|

For example, here is the deb822-formatted file for Pop!\_OS's 22.04 proprietary application repository:

```bash
X-Repolib-Name: Pop_OS Apps
Enabled: yes
Types: deb
URIs: http://apt.pop-os.org/proprietary
Suites: jammy
Components: main
```

To manually create a Debian source, open the Terminal and navigate to `/etc/apt/sources.list.d/`:

```bash
cd /etc/apt/sources.list.d/
```

Create a new text file using `nano`, or a text editor of your choice:

```bash
sudo nano [my-new-source-name].sources
```

Define the fields for your source:

![Define Source Fields in Text Editor](/images/manage-repos/define-debian-source-fields.png)

Save your text file. Use the `apt-manage` tool with the `list` option to verify the Debian source has been added:

```bash
apt-manage list
```

![Verify Manually Added Source with Apt-Manage](/images/manage-repos/verify-manually-added-debian-source.png)

## Manually Removing Debian Repositories

Open the Terminal and navigate to `/etc/apt/sources.list.d/`.

```bash
cd /etc/apt/sources.list.d/
```

Use the `rm` command with the source's filename to remove a Debian source.

```bash
sudo rm [SourceFileName]
```

![Manually Remove Debian Source File](/images/manage-repos/manually-remove-debian-source.png)

Use the `ls` command to list the current sources and confirm the source has been removed.

```bash
ls
```

![List Debian Source File After Manual Removal](/images/manage-repos/verify-manually-removed-debian-source.png)

## Manually Adding Flatpak Repositories

All fields for a remote repository are described in the [Flatpak command reference](https://docs.flatpak.org/en/latest/flatpak-command-reference.html).

| Field | Function |
|-------|----------|
| [remote "repo-name"] | Define the name of the repository. |
| url | Specify the repository's location. |
| xa.title* | Define the title of the repository. |
| gpg-verify | Specify if GPG verification should be used for content in this repository. |
| gpg-verify-summary | Specify if GPG verification should be used for the summary. |
| xa.comment* | Add an optional comment. |
| xa.description* | Add an optional full-paragraph description. |
| xa.icon* | Add an optional URL that points to an icon. |

*These options are often used to represent the remote repository in a GUI program.

This example shows the config file entry for the Flatub beta repository:

```bash
[remote "flathub-beta"]
url=https://dl.flathub.org/beta-repo/
xa.title=Flathub beta
gpg-verify=true
gpg-verify-summary=true
xa.comment=Beta builds of Flatpak applications
xa.description=Beta builds of Flatpak applications
xa.icon=https://dl.flathub.org/repo/logo.svg
xa.homepage=https://flathub.org/
```

To manually add a Flatpak remote repository, open the Terminal and navigate to `~/.local/share/flatpak/repo`:

```bash
cd ~/.local/share/flatpak/repo
```

Open the `config` file using `nano`, or your preferred text editor:

```bash
nano config
```

At minimum, a Flatpak remote repository should contain these fields:

```bash
[remote "New Flatpak Repository"]
url=https://new.flatpak.repo.org/apps/
gpg-verify=value
gpg-verify-summary=value
```

![Define Fields for Flatpak Repo](/images/manage-repos/define-fields-for-flatpak-repo.png)

Save the `config` file and exit your text editor.

Use the `flatpak` command with the `remote-list` option to verify the new Flatpak repository has been added:

```bash
flatpak remote-list
```

![Verify Manually Added Flatpak Repo](/images/manage-repos/verify-manually-added-flatpak-repo.png)

## Manually Removing Flatpak Repositories

Open the Terminal and navigate to `~/.local/share/flatpak/repo/`.

```bash
cd ~/.local/share/flatpak/repo/
```

Open the `config` file using `nano`, or your preferred text editor:

```bash
nano config
```

Delete the lines that define the Flatpak repository you want to remove:

![Delete Flatpack Repo Lines](/images/manage-repos/delete-flatpak-repo-lines.png)

Save the file and exit your text editor.

Use the `flatpak` command with the `remote-list` option to verify the new Flatpak repository has been removed:

```bash
flatpak remote-list
```

![Verify Manually Deleted Flatpak Repository](/images/manage-repos/verify-manually-deleted-flatpak-repository.png)
# Managing Repositories with the Terminal

Use the `apt-manage` tool to add and remove Debian repositories in the `/etc/apt/sources.list.d/` directory. Use the `flatpak` tool to add and remove Flatpak repositories from the `~/.local/share/flatpak/repo/` directory. Both of these directories can also be manually edited using Terminal text editor like `nano`.

## Using the apt-manage Command

The `apt-manage` command is unique to Pop!\_OS and comes from `repolib` the same library that Repoman is built upon. All options for the `apt-manage` command can be viewed by opening a Terminal and entering:

```bash
apt-manage -h
```

### Add a Repository Using apt-manage

The `add` option will create an entry in the text file located in `/etc/apt/sources.list.d/` (Debian repositories). Enter this command and enter your password when prompted.

```bash
apt-manage add [RepositoryURI]
```

In this example the Debian repository for the ProtonVPN CLI tool is added:

![Add Repo with apt-manage](/images/manage-repos/apt-manage-add-repo.png)

Confirm the repository has been added using the `list` option:

```bash
apt-manage list
```

![apt-manage View Added Repo](/images/manage-repos/apt-manage-list-added-repo.png)

### Remove a Repository Using apt-manage

While sources can be added using the URI, they must be removed using the repository's source name.

Use the `list` option to obtain the source name of the repo you wish to remove:

```bash
apt-manage list
```

![Find Repo Source Name](/images/manage-repos/find-repo-source-name.png)

Use the `remove` option to remove the source:

```bash
apt-manage remove [SourceName]
```

Press `y` to confirm you want to remove the source and enter your password when prompted.

![apt-manage Confirm Removal](/images/manage-repos/apt-manage-confirm-removal.png)

Confirm the repository has been removed using the `list` option:

```bash
apt-manage list
```

![apt-manage List Repos](/images/manage-repos/apt-manage-confirm-removed.png)

## Using the Flatpak Tool

Flatpak repositories can be added and removed using options available with the Flatpak command line tool. Type `flatpak -h` to see all options available for the Flatpak tool.

### Adding a Repository with the Flatpak Tool

Use the `remote-add` option to add the name and URL of the remote Flatpak repository.

```bash
flatpak remote-add [repo-name] [repo-url]
```

![Add Repo with Flatpak Tool]()

Use the `remote-list` option to confirm the repository has been added:

```bash
flatpak remote-list
```

![View Added Flatpak Repo Command]()

### Removing a Repository with the Flatpak Tool

Use the `remote-delete` command to remove a repository. Specify the name of the repository in this command. Use the `remote-list` option to confirm the repository's name if you aren't sure.

```bash
flatpak remote-delete [repository name]
```

![Remove Repo with Flatpak Tool]()

## Directly Editing Configuration Files

You can directly edit or create text files located in `/etc/apt/sources.list.d/` (Debian repositories) or `~/.local/share/flatpak/repo/` (Flatpak repositories).

### Manually Adding Debian Debian Repositories

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

To manually create a Debian source:

Navigate to `/etc/apt/sources/list.d/`:

```bash
cd /etc/apt/sources/list.d/
```

Create a new text file using `nano`, or a text editor of your choice:

```bash
sudo nano [my-new-source-name].sources
```

Define the fields for your source:

![Define Source Fields in Text Editor]()

```bash
X-Repolib-Name: My New Source
Enabled: Yes
Types: deb
URIs: http://my.new.sources.org/files
Components: main
```

Save your text file.

### Manually Removing Debian Repositories

Open the Terminal and navigate to `/etc/apt/sources.list.d/`.

```bash
cd /etc/apt/sources.list.d/
```

Use the `rm` command with the source's filename to remove a Debian source.

```bash
sudo rm [SourceFileName]
```

![Manually Remove Debian Source File]()

Use the `ls` command to list the current sources and confirm the source has been removed.

```bash
ls
```

![List Debian Source File After Manual Removal]()

### Manually Adding Flatpak Repositories

### Manually Removing Flatpak Repositories

Open the Terminal and navigate to `~/.local/share/flatpak/repo/`.

```bash
cd ~/.local/share/flatpak/repo/
```

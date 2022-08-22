# Managing Repositories with the Terminal

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

## Directly Editing the Config Files

You can directly edit text files located in `/etc/apt/sources.list.d/` (Debian repositories) or `~/.local/share/flatpak/repo/` (Flatpak repositories)

### Adding and Removing Debian Repositories

Open the Terminal and navigate to `/etc/apt/sources.list.d/`.

```bash
cd /etc/apt/sources.list.d/
```

Use the `rm` command with the source's filename to remove a Debian source.

```bash
sudo rm [SourceFileName]
```

Use the `ls` command to list the current sources.

```bash
ls
```

### Adding and Removing Flatpak Repositories

Open the Terminal and navigate to `~/.local/share/flatpak/repo/`.

```bash
cd ~/.local/share/flatpak/repo/
```

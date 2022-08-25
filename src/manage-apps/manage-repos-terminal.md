# Managing Repositories with the Terminal

Use the `apt-manage` tool to add and remove apt repositories in the `/etc/apt/sources.list.d/` directory. Use the `flatpak` tool to add and remove Flatpak repositories from the `~/.local/share/flatpak/repo/` directory.

## Using the apt-manage Command

The `apt-manage` command is unique to Pop!\_OS and comes from `repolib`, the same library that Repoman is built upon. All options for the `apt-manage` command can be viewed by opening a Terminal and entering:

```bash
apt-manage -h
```

### Add a Repository Using apt-manage

The `add` option will create an entry in the text file located in `/etc/apt/sources.list.d/`. Enter this command and enter your password when prompted.

```bash
apt-manage add [RepositoryURI]
```

In this example, the apt repository for the ProtonVPN CLI tool is added:

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

## Using the flatpak Command

Flatpak repositories can be added and removed using options available with the `flatpak` command. See all available options for the `flatpak` command by opening the Terminal and entering:

```bash
flatpak -h
```

### Adding a Repository with the flatpak Command

Use the `remote-add` and `user` options to add a remote Flatpak repository for the current user.

```bash
flatpak remote-add --user [repo-name] [repo-url]
```

![Add Repo with Flatpak Tool](/images/manage-repos/flatpak-command-add-repo.png)

Use the `remote-list` option to confirm the repository has been added:

```bash
flatpak remote-list
```

![View Added Flatpak Repo Command](/images/manage-repos/flatpak-view-added-repo-command.png)

### Removing a Repository with the flatpak Command

Use the `remote-delete` command to remove a repository. Specify the name of the repository in this command. Use the `remote-list` option to confirm the repository's name if you aren't sure.

```bash
flatpak remote-delete [repository name]
```

![Remove Repo with Flatpak Tool](/images/manage-repos/flatpak-remote-delete-command.png)

Use the `remote-list` option to confirm the repository has been deleted:

```bash
flatpak remote-list
```

![View Deleted Flatpak Repo Command](/images/manage-repos/view-deleted-flatpak-repo-command.png)

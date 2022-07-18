# Managing User Themes

User themes include changes to window animations, desktop color schemes, window designs, icons, and workspaces. You can install custom GNOME Themes from [Gnome-look.org](https://www.gnome-look.org/browse/), or other similar web sites. The Pop!\_OS default themes can be re-applied using GNOME Tweaks or the by using Terminal commands.

>**Note**: Applying custom GNOME theming options may cause system instability or glitchy behavior. Additionally, custom themes are not subject to testing by Pop!\_OS or application developers.

## Enabling User Themes

1. Launch the [GNOME Extension Manager](gnome-extensions.md#installing-the-gnome-extensions--extension-manager-apps).

    ![Launch GNOME Extension Manager](/images/user-themes/launch-ext-manager.png)

2. Click `Browse` and search for `user-theme@gnome`, then click `Install`.

    ![Install User Themes](/images/user-themes/install-user-themes.png)

3. Click `Installed` and ensure the toggle switch for `User Themes` is enabled.

    ![Verify User Themes is Enabled](/images/user-themes/verify-enabled.png)

## Adding a Custom User Theme

> **Note**: Themes in Pop!\_OS 22.04 must support GTK 4. Additionally, it may be necessary to disable some [COSMIC components](gnome-extensions.md#built-in-extensions) from GNOME Extensions for certain themes to work properly.

### Downloading a Custom Theme

Custom GNOME user themes can be downloaded from [Gnome-look.org](https://www.gnome-look.org/browse/).

![GNOME Themes on Gnome-look.org](/images/user-themes/open-desktop-themes.png)

Download files for the theme are usually listed under the `Files` section on the theme's page.

### Installing a Custom Theme

Follow the instructions on the theme's page to add it to your system; these are typically listed in the `Product` section on the theme's page. If no instructions are listed, click the link provided next to `Source` and view the theme's README.

![Theme Installation Instructions](/images/user-themes/installation-instructions.png)

Installation methods will vary, but the process will usually involve extracting a tar.gz file to either */usr/share/themes* requiring `sudo`, or to *~/.themes*. In the example below, a theme called `example-theme.tar.xz` is extracted to *~/.themes*.

```bash
tar -xf example-theme.tar.xz -C ~/.themes
```

### Applying a Custom Theme

Launch GNOME Tweaks, then select the `Appearance` tab and choose a theme from the `Shell` dropdown menu.

![Select Theme from Appearance Tab](/images/user-themes/select-theme.png)

You may need to restart GNOME Tweaks if it was open when extracting the theme to your local directory. Additionally, you may also need to restart GNOME Shell by pressing `Alt` + `F2`, then typing `r` and hitting `Enter`.

## Resetting the User Theme to Default

You can reset user themes to the Pop!\_OS defaults using GNOME Tweaks and Extensions, or by entering Terminal commands.

### Using GNOME Tweaks and Extensions

Launch GNOME Tweaks, then select the `Appearance` tab and select Pop options for all available theme settings. You should also disable any additional extensions you have installed if you want to fully restore the default COSMIC experience.

>**Note**: Navigating to [Appearance settings](/customize-pop/appearance-settings.md) in the Settings application and selecting a Pop!\_OS theme will also reset the shell theme.

![Select Theme from Appearance Tab](/images/user-themes/reset-theme.png)

Launch GNOME Extensions and re-enable any built-in extensions you may have disabled when applying a custom theme.

![Re-enable Built-in Extensions](/images/user-themes/enable-built-in-ext.png)

### Using the Terminal

1. Reset the shell theme:

    ```bash
    dconf reset /org/gnome/shell/extensions/user-theme/name
    ```

2. Disable the user-themes extension:

    ```bash
    gnome-extensions disable user-theme@gnome-shell-extensions.gcampax.github.com
    ```

3. Reset the Legacy Applications theme (GTK Theme):

    ```bash
    gsettings reset org.gnome.desktop.interface gtk-theme
    ```

4. Re-enable built-in extensions by running these commands one at a time:

    ```bash
    gnome-extensions enable cosmic-workspaces@system76.com
    gnome-extensions enable cosmic-dock@system76.com
    gnome-extensions enable pop-cosmic@system76.com
    gnome-extensions enable pop-shell@system76.com
    ```

5. (Optional) Disable all user-installed extensions to restore the default COSMIC desktop experience: 

    ```bash
    gsettings set org.gnome.shell disable-user-extensions true
    ```

# Customizing the Desktop

Options to change the look and feel of Pop!\_OS are located in `Settings` ➞ `Desktop`.

- [`Desktop Options`](/customize-pop/customize-desktop.md#desktop-options): Modify the `SUPER` key's function, enable the Hot Corner, and add or position top bar elements.
- [`Background` settings](/customize-pop/customize-desktop.md#background): Set pre-installed wallpaper or user images as the background image.
- [`Appearance` settings](/customize-pop/customize-desktop.md#appearance) Choose a dark or light theme that applies across the entire desktop environment.
- [`Dock` settings](/customize-pop/customize-desktop.md#dock): Modify the Dock's visibility, placement, size, and displayed icons.
- [`Workspaces` settings](/customize-pop/customize-desktop.md#workspaces) includes options to configure workspace positioning and behavior.

---

## Desktop Options

Settings to customize desktop elements are available in the `Desktop Options` tab.

![General Settings](/images/customize-desktop/general-settings.png)

| Setting | Function |
|----------|----------|
| Super Key Action | Assign the `SUPER` key to start the Launcher, display workspace navigation, or view installed applications. |
| Hot Corner | Display workspace navigation when the user moves the mouse cursor to the upper left corner of the screen. |
| Top Bar | Display or hide items along the top bar. |
| Window Controls | Enable or disable the minimize and maximize buttons in windows. |

## Background

Settings to change the desktop background are located in the `Background` tab . Alternatively, this option is available by right-clicking anywhere on the desktop and selecting `Change Background...`.

>**Note**: Background adjustments such as centered, scaled, spanned, stretched, and zoom are set using the GNOME Tweaks application: [GNOME Tweaks Appearance Settings](gnome-tweaks-extensions.md#appearance)

![Background Tab](/images/customize-desktop/background-tab.png)

### Set Pre-installed Images as Wallpaper

Select an image from the list. There is no “apply” button; the desktop background will update automatically when an image is selected.

![Set Pre-installed Image](/images/customize-desktop/set-preinstalled-image.png)

### Set User Images as Wallpaper

1. Click `Add Picture…` and navigate to the location of your image.

    ![Click Add Picture](/images/customize-desktop/click-add-picture.png)

2. Click `Open`.

    ![Click Open](/images/customize-desktop/click-open.png)

3. Select the image added to the list of available wallpapers.

    ![Select Added Image](/images/customize-desktop/select-added-image.png)

Alternatively, right-click the image and choose `Set as Wallpaper` from within the file browser.

![Set as Wallpaper](/images/customize-desktop/set-as-wallpaper.png)

## Appearance

Pop!\_OS includes two default themes: Light and Dark. These themes apply to all system and application windows across the operating system. Selecting a theme also assigns a default desktop background. The Light and Dark theme options are located in the `Appearance` tab.

**Light Theme**

![Light Theme](/images/customize-desktop/light-theme.png)

**Dark Theme**

![Dark Theme](/images/customize-desktop/dark-theme.png)

>**Note**: Custom themes may cuase graphical glitches, but they can be applied using [GNOME Tweaks](gnome-tweaks-extensions.md).

![Change Theme](/images/customize-desktop/change-theme.png)

## Dock

Settings for modifying Dock visibility behavior and Dock icons are located in the `Dock` tab.

![Modify Dock](/images/customize-desktop/customize-dock.png)

| Setting | Function |
|----------|----------|
| Enable Dock | Disable or enable the Dock's visibility. |
| Dock Options | <ul><li>Extend dock to edges of the screen: Lengthen the Dock's edges so that it appears as a panel that extends to the screen edges.</li><li>Show Launcher Icon in Dock: Display an icon that starts the Launcher when clicked.</li><li>Show Workspaces Icon in Dock: Display an icon that activates the workspaces and windows view when clicked.</li><li>Show Applications Icon in Dock: Display an icon that launches the Application menu when clicked.</li><li>Show Mounted Drives: Display an icon for each mounted drive.</li><li>Icon Click Action: Specify behavior when an application icon is clicked. See examples of Icon Click Action behavior in [Navigate Between Running Applications](/navigate-pop/switching-apps.md#using-the-dock). <ul><li>Launch or Cycle Windows: A running application is focused when its icon is clicked. Additional clicks cycle through instances of that application.</li><li>Launch or Minimize Windows: A running application is focused or minimized when its icon is clicked.</li><li>Launch, Minimize, or Preview Windows: When clicked, if a running application has multiple windows open, a menu displays wih a preview of each window and focus applied to the selected window. Otherwise, a running application is focused or minimized. |
| Dock Visibility | **Visibility options**<ul><li>Always visible: The Dock remains static with no hiding behavior.</li><li>Always hide: The Dock always hides unless actively being revealed by the mouse.</li><li>Intelligently hide: The Dock hides when any window covers the dock area.</ul>**Additional settings**<ul><li>Show Dock on Display: Display the Dock on all displays or only the primary display.|
| Dock Size | The Dock size is set to Small (36px), Medium (48px), Large (60px), or specify a custom size.|
| Position on the Desktop | Display the Dock horizontally along the bottom of the screen, or vertically on the left or right sides of the screen. |

## Workspaces

Workspace placement and behavior is controlled in the `Workspaces` tab. Learn more about using Workspaces in the [Using Workspaces](/navigate-pop/using-workspaces.md) section.

![Workspace Settings](/images/customize-desktop/workspace-settings.png)

| Setting | Function |
|---------|----------|
| Dynamic Workspaces | Automatically remove empty Workspaces. |
| Fixed Number of Workspaces | Specify a static number of workspaces. |
| Multi-monitor Behavior | <ul><li>Worskpaces Span Displays: Include all connected displays in workspaces. </li><li>Workspaces on Primary Display Only: Only include windows from the primary display in workspaces. |
| Placement of the Workspace Picker | Specify whether the workspace picker appears along the left or right side. |

# Customizing the Desktop

Change the function of the `SUPER` key, desktop backgrounds, workspace features, and placement and visibility of desktop components in `Settings` ➞ `Desktop`.

- [`Desktop Options`](/customize-pop/customize-desktop.md#desktop-options) provides options to modify the `SUPER` key's function, enabling the Hot Corner, and adding or positioning top bar elements.
- [`Background` settings](/customize-pop/customize-desktop.md#background) allows users to set pre-installed wallpaper or user images as the background image.
- [`Appearance` settings](/customize-pop/customize-desktop.md#appearance) provides the option to choose a dark or light theme that applies across the entire desktop environment.
- [The `Dock`'s settings](/customize-pop/customize-desktop.md#dock) provides options to modify the Dock's visibility, placement, size, and displayed icons.
- [`Workspaces` settings](/customize-pop/customize-desktop.md#workspaces) includes options to configure workspace positioning and behavior.

---

## Desktop Options

Customize basic desktop elements in the `Desktop Options` tab.

![General Settings](/images/customize-desktop/general-settings.png)

| Setting | Function |
|----------|----------|
| Super Key Action | Assigns the `SUPER` key to start the Launcher, display Workspace navigation, or view installed applications. |
| Hot Corner | Displays Workspace navigation when the user moves the mouse cursor to the upper left corner of the screen. |
| Top Bar | Display or hide items along the top bar. |
| Window Controls | Enable or disable the minimize and maximize buttons in windows. |

## Background

Choose a pre-installed desktop background or assign a custom image in the `Background` tab. Alternatively, right-click anywhere on the desktop and select `Change Background...`.

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

Pop!\_OS includes two default themes: Light and Dark. These themes apply to all system and application windows across the operating system. Selecting a theme also assigns a default desktop background.

**Light Theme**

![Light Theme](/images/customize-desktop/light-theme.png)

**Dark Theme**

![Dark Theme](/images/customize-desktop/dark-theme.png)

Enable the Light or Dark theme in the `Appearance` tab.

>**Note**: Custom themes may case graphical glitches, but they can be applied using [GNOME Tweaks](gnome-tweaks-extensions.md).

![Change Theme](/images/customize-desktop/change-theme.png)

## Dock

The `Dock` tab contains settings for modifying Dock visibility behavior and the appearance of system and application icons.

![Modify Dock](/images/customize-desktop/customize-dock.png)

| Setting | Function |
|----------|----------|
| Enable Dock | Disabling this option causes the Dock to disappear entirely. |
| Dock Options | Display utility icons and mounted drives in the Dock, make the Dock appear as a panel that extends to the screen edges, and specify what happens when an application icon is clicked. See examples of Icon Click Action behavior in [Navigate Between Running Applications](/navigate-pop/switching-apps.md#using-the-dock). <ul><li>Launch or Cycle Windows: A running application is focused when its icon is clicked. Additional clicks cycle through instances of that application.</li><li>Launch or Minimize Windows: A running application is focused or minimized when its icon is clicked.</li><li>Launch, Minimize, or Preview Windows: When clicked, if a running application has multiple windows open, a menu displays wih a preview of each window and focus applied to the selected winodw. Otherwise, a running application is focused or minimized. |
| Dock Visibility | **Visibility options**<ul><li>Always visible: The Dock remains static with no hiding behavior.</li><li>Always hide: The Dock always hides unless actively being revealed by the mouse.</li><li>Intelligently hide: The Dock hides when any window covers the dock area.</ul> **Additional settings**<ul><li>Show Dock on Display: Choose to display the dock on all displays or only the primary display.|
| Dock Size | Choose between Small (36px), Medium (48px), Large (60px), or specify a custom size.|
| Position on the Desktop | Choose to display the Dock horizontally along the bottom of the screen, or vertically on the left or right sides of the screen. |

## Workspaces

The `Workspaces` tab provides settings to control Workspace placement and behavior. Learn more about Workspaces in the [Using Workspaces](/navigate-pop/using-workspaces.md) section.

![Workspace Settings](/images/customize-desktop/workspace-settings.png)

| Setting | Function |
|---------|----------|
| Dynamic Workspaces | Automatically remove empty workspaces. |
| Fixed Number of Workspaces | Specify a static number of workspaces. |
| Multi-monitor Behavior | <ul><li>Worskpaces Span Displays: Workspace areas inlude all connected displays. </li><li>Workspaces on Primary Display Only: Workspace areas apply only to the primary display. |
| Placement of the Workspace Picker | Specify whether the workspace picker appears along the left or right side. |

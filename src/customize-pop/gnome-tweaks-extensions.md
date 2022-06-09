# GNOME Tweaks & Extensions

GNOME Tweaks and GNOME Shell Extensions provide additional customization beyond the Settings menu.

---

## GNOME Tweaks

GNOME Tweaks is an optional software package allowing users to further customize the appearance and behavior of Pop!\_OS. GNOME Tweaks features include changing power settings, managing startup applications, enabling desktop icons, and changing fonts.

### Install GNOME Tweaks

Launch the Pop!\_Shop from the Dock and search “gnome tweaks”. Click `Install`.

![Install Tweaks](/images/gnome-tweaks-extensions/install-tweaks.png)

## GNOME Tweaks Settings

### General

![General Settings](/images/gnome-tweaks-extensions/general-settings.png)

| Option | Function |
|--------|----------|
| Suspend when laptop lid is closed | Place the system into a suspended state when the laptop lid is closed. |
| Over-Amplification | Allow the volume to be increased above 100%. |

### Appearance

`Appearance` settings modify the theme, background, and lock screen elements of the desktop environment.

![Appearance Tweaks](/images/gnome-tweaks-extensions/appearance-tweaks.png)

#### Theme Options

| Option | Function |
|--------|----------|
| Applications | Select the theme that will be applied to application windows. |
| Cursor | Select a cursor design. |
| Icons | Choose an icon set that displays custom icons for system tools and applications. |
| Shell | Select or upload a shell theme. Using this option requires enabling `User Themes` in GNOME Extensions. |
| Sound | Modify system feedback and notification sounds. |

#### Background Options

| Option | Function |
|--------|----------|
| Image | Select an image to set as the desktop background. |
| Adjustment | Manipulate the appearance of the desktop background. Options include: <ul><li>Zoom</li><li>Centered</li><li>Scaled</li><li>Spanned</li><li>Stretched</li><li>Wallpaper |

#### Lock Screen Options

| Option | Function |
|--------|----------|
| Image | Select an image that will display at the lock screen. |
| Adjustment | Manipulate the appearance of the lock screen background. Options include: <ul><li>Zoom</li><li>Centered</li><li>Scaled</li><li>Spanned</li><li>Stretched</li><li>Wallpaper |

### Fonts

`Fonts` settings allow you to specify the default fonts used throughout the operating system.

![Fonts Tweaks](/images/gnome-tweaks-extensions/fonts-tweaks.png)

| Option | Function |
|--------|----------|
| Interface Text | Choose the font used for displayed text inside of a running application. |
| Document Text | Choose the font used when creating a new text document. Applications like Libreoffice may override this selection. |
| Monospace Text | Choose the font used in a Terminal session. This may also include coding applications and basic text editors. |
| Legacy Window Titles | Choose the font used to display information in the top bar of running application windows. This is usually the name of the application. |
| Hinting | Enable text hinting, which improves text readability for low-resolution displays. |
| Antialiasing | Enable antialiasing, which improves text visibility when high-resolution text is displayed on a low-resolution screen. |
| Scaling Factor | Enable text scaling, which increases font size for HiDPI displays while retaining text sharpness. |

### Keyboard & Mouse

`Keyboard & Mouse` settings extend customization of keyboard and mouse input behavior.

![Keyboard Mouse Tweaks](/images/gnome-tweaks-extensions/keyboard-mouse-tweaks.png)

#### Keyboard

| Option | Function |
|--------|----------|
| Show Extended Input Sources | Display additional number of input sources found in the Settings application. |
| Emacs Input | Apply Emacs keybindings throughout the operating system. |
| Overview Shortcut | Choose whether left or right `SUPER` keys start the Launcher. |

#### Mouse

| Option | Function |
|--------|----------|
| Acceleration Profile | Choose how mouse movement speed adapts to user gestures. |
| Pointer Location | Pressing the `Ctrl` key creates a visual notification at the mouse pointer location. |
| Middle Click Paste | Clicking the middle mouse button pastes content from the clipboard. |
| (Touchpad) Disable While Typing | The touchpad is disabled when using the keyboard. |
| (Touchpad) Mouse Click Emulation | Select touchpad input that will be interpreted as input from a standard mouse: <ul><li>Fingers: Click with two fingers on the touch pad to input right-click, and three fingers input a middle-click.</li><li>Area: Click the bottom right of the touch pad to input right-click, and the bottom middle for a middle-click.</li><li>Disabled: The touch pad input will not be interpreted as right, middle, or left-click actions. |

### Startup Applications

Choose applications that will automatically start after you log in.

![Startup App Tweaks](/images/gnome-tweaks-extensions/startup-app-tweaks.png)

Add an application by clicking the `+`, selecting an application from the list, and then clicking `Add`.

![Select Startup App](/images/gnome-tweaks-extensions/select-startup-app.png)

### Top Bar

Configure the clock to display additional information.

![Top Bar Tweaks](/images/gnome-tweaks-extensions/top-bar-tweaks.png)

You can also choose to display week numbers in the system calendar application.

![Calendar Tweaks](/images/gnome-tweaks-extensions/calendar-tweaks.png)

### Window Titlebars

Configure settings that allow you to interact with windows using mouse clicks. You can also choose available titlebar buttons and their placement. Right, middle, and left-click buttons can each be configured to perform one of the following actions when clicking a window's titlebar:

![Titlebar Tweaks](/images/gnome-tweaks-extensions/titlebar-tweaks.png)

| Option | Function |
|--------|----------|
| Lower | A "send to back" action occurs. |
| Menu | A window manipulation menu is displayed. |
| Minimize | A window is minimized.|
| Toggle Maximize | A window is maximized, the window returns to its previous size on second click. |
| Toggle Maximize Horizontally* | A window is extended to the left and right sides of the screen without modifying vertical dimensions. |
| Toggle Maximize Vertically* | A window is expanded to the top and bottom of the screen without modifying horizontal dimensions. |
| Toggle Shade* | A window is collapsed into or expanded from its titlebar when the window's titlebar. |

\* This feature is not supported by all application windows.

### Windows

The `Windows` menu offers additional features for interacting with system and application windows.

![Windows Tweaks](/images/gnome-tweaks-extensions/windows-tweaks.png)

| Option | Function |
|--------|----------|
| Attach Modal Dialogs | Modal dialogs (such as windows that spawn when performing a "Save as...") stay in a fixed position within their parent window. |
| Center New Windows | New windows launch perfectly centered on the screen. |
| Resize with Secondary-Click | A window can be maximized or returned to previous size by double-clicking the primary mouse button. |
| Window Action Key | Windows can be dragged freely by holding this key, left-clicking anywhere in the window, and dragging with the mouse. Windows can be resized by holding this key, right-clicking anywhere in a window, and dragging the mouse. |
| Window Focus | Set the action that brings a window into focus: <ul><li>Click to Focus: Clicking a window brings it into focus.</li><li>Focus on Hover: Hovering the cursor over a window brings it into focus. Focus is maintained if the cursor is moved to the desktop.</li><li>Secondary-Click: Hovering the cursor over a window brings it into focus. Focus is not maintained if the cursor is moved to the desktop.</li><li>Raise Windows When Focused: The focused window is brought to the front. This option can be enabled when either `Focus on Hover` or `Secondary-Click` is chosen. |

## GNOME Shell Extensions

GNOME shell extensions are features written by third party developers that build upon the GNOME Shell. Extensions are similar to Chrome Extensions or Firefox Addons. GNOME Extensions is an application that provides settings to manage extensions. Extension Manager is a utility for browsing and installing extensions. Both applications provide menus for configuring, disabling, or removing installed extensions.

### Installing the GNOME Extensions & Extension Manager Apps

Launch the Pop!\_Shop and type `extensions` then click `Install` for each application.

![Install Extensions App](/images/gnome-tweaks-extensions/install-extensions-app.png)

### Built-In Extensions

Components packaged in Pop!\_OS are listed in the `Built-In` section. Toggle the switches to enable or disable an extension.

| Extension | Description |
|-----------|-------------|
| [Cosmic Dock](https://github.com/pop-os/cosmic-dock) | A modified version of Dash to Dock with different defaults. |
| [Cosmic Workspaces](https://github.com/pop-os/cosmic-workspaces) | Pop!\_OS's workspaces feature with vertical stacking. |
| [Pop COSMIC](https://github.com/pop-os/cosmic) | The collection of unique components that comprise the Pop!\_OS experience: Customized Dash-to-Dock, vertical workspaces, and additional configuration options in Settings. |
| [Pop Shell](https://github.com/pop-os/shell) | a keyboard-driven layer for GNOME Shell which allows for quick and sensible navigation and management of windows. |
| [System76 Power](https://github.com/pop-os/gnome-shell-extension-system76-power) | A GNOME Shell extension that adds graphical integration to the system76-power daemon. |

![Built-in Ext](/images/gnome-tweaks-extensions/built-in.png)

### Installing Additional Extensions

Launch the Extension Manager application. Select `Browse` at the top of the window. Use the search bar to find an extension. Click `Install` to install the extension.

![Select Browse](/images/gnome-tweaks-extensions/click-browse.png)

### Extension Settings

Extensions can be managed from the `User-Installed Extensions` list.

![User Installed](/images/gnome-tweaks-extensions/user-installed-extensions.png)

Toggle the switch next to the listed extension to enable or disable it. Click the gear icon to view specific settings for an extension.

![Gear Icon](/images/gnome-tweaks-extensions/gear-icon.png)

### Removing Extensions

Select the chevron to the right of the extension's listing. This will expand a menu. Click the `Remove` button to uninstall the extension.

![Remove Extension](/images/gnome-tweaks-extensions/remove-extension.png)

<!--Extensions are available from [extensions.gnome.org](https://extensions.gnome.org). A web browser plugin is needed to interact with the site.

![Extensions Plugin](/images/gnome-tweaks-extensions/extensions-plugin.png)

To add an extension from extensions.gnome.org, navigate to the extension's page and toggle the switch to `On`.

![Toggle Extension](/images/gnome-tweaks-extensions/toggle-extension.png)-->

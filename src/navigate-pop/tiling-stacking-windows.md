# Tiling & Stacking Windows

This sections describes the Auto Tiling and Stacking window management features in Pop!\_OS, and provides instructions to configure their behavior.

---

## Tiling Windows

Pop!\_OS optimizes workflows using a smart window management system called Auto Tiling.

![]

Enable Auto Tiling by clicking on the tile icon in the upper right corner and toggling the button. Tiling settings include options for window titles, active window hint, active window color, and gaps.

![]

| Option                 | Function |
|:----------------------:|:--------:|
| Tile Windows| Toggles the Window Tiling Feature On or Off  |
| Floating Window Exception  | Allows adding exceptions to the tiling feature allowing free positioning of specified windows |
| Toggle Tiling          | Enable/Disable Window Tiling with a keyboard shortcut |
| Show Active Hint       | Highlights the selected window with a border color |
| Gaps                | Sets gap spacing between tiled windows |

### Enable a Floating Window Exception

Enabling a Floating Window Exception will exclude individual windows from Auto Tiling. Pop!\_OS applies default exceptions to some applications based on user feedback.

1. Run the application that needs to be exempted from Auto Tiling. Click the tile menu, then click `Floating Window Exceptions`.

![]

2. Click `Select` to add an exception.

![]

3. Select the running application that should be exempted from Auto Tiling.

![]

4. Choose to create an exception for all windows belonging to an application, or only the currently selected window. In this example only the current Terminal window will be selected for exemption.

![]

5. Notice the shell can now be dragged around freely, and an exception has been added to the list. 

![]

## Stacking Windows

Stacking is an additional Auto Tiling feature enabling multiple windows to fit on a small screen.

1. Press SUPER + S to enable stacking on application windows while in Tiling mode.

![]

2. Press SUPER + Enter to highlight a window for stacking.

![]

3. Use the arrow keys to move the window into another application window for stacking.

![]


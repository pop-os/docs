# Tiling & Stacking Windows

This section describes the Auto Tiling and Stacking window management features in Pop!\_OS, and provides instructions to configure their behavior.

---

## Tiling Windows

Pop!\_OS optimizes workflows using a smart window management system called Auto Tiling.

![Auto Tiling](/images/tiling-stacking-windows/auto-tiling.png)

Enable Auto Tiling by clicking on the tile icon in the upper right corner and toggling the button. Tiling settings include options for window titles, active window hint, active window color, and gaps.

![Enable Autotiling](/images/tiling-stacking-windows/enable-autotiling.png)

| Option                 | Function |
|----------------------|--------|
| Tile Windows| Toggles the Window Tiling Feature On or Off  |
| Floating Window Exception  | Allows adding exceptions to the tiling feature allowing free positioning of specified windows |
| Toggle Tiling          | Enable/Disable Window Tiling with a keyboard shortcut |
| Show Active Hint       | Highlights the selected window with a border color |
| Gaps                | Sets gap spacing between tiled windows |

### Enable a Floating Window Exception

Enabling a Floating Window Exception will exclude individual windows from Auto Tiling. Pop!\_OS applies default exceptions to some applications based on user feedback.

1. Run the application that needs to be exempted from Auto Tiling. Click the tile menu, then click `Floating Window Exceptions`.

![Floating Window Exceptions](/images/tiling-stacking-windows/floating-window-exceptions.png)

2. Click `Select` to add an exception.

![Click Select](/images/tiling-stacking-windows/click-select.png)

3. Select the running application that should be exempted from Auto Tiling.

![Select Exempted App](/images/tiling-stacking-windows/select-exempted-app.png)

4. Choose to create an exception for all windows belonging to an application, or only the currently selected window. In this example only the current Terminal window will be selected for exemption.

![Current Window Only](/images/tiling-stacking-windows/current-window-only.png)

5. The shell window can now be dragged around freely.

![Drag Shell Freely](/images/tiling-stacking-windows/drag-shell-freely.png)

## Stacking Windows

Stacking is an additional Auto Tiling feature enabling multiple windows to fit on a small screen.

1. While in Tiling mode, select a window and press SUPER + S. Make additional windows stackable by selecting them and press SUPER + S. Stackable windows are designated with a yellow bar at the top.

![Enable Stacking](/images/tiling-stacking-windows/enable-stacking.png)

2. Press SUPER + Enter to highlight a window to merge into a stack. The window to be merged is designated by a yellow highlight across the entire window.

![Highlight for Stacking](/images/tiling-stacking-windows/highlight-for-stacking.png)

3. Use the arrow keys to move the window into another application window for stacking.

![Use Arrow Keys](/images/tiling-stacking-windows/use-arrow-keys.png)

4. Launching additional applications while a stack is selected will automatically add that application to the stack.

![Launch Additional App](/images/tiling-stacking-windows/launch-additional-app.png)

5. Use SUPER + left and right arrow keys to navigate between windows in the stack.

![Navigate Stacked Windows](/images/tiling-stacking-windows/navigate-stacked-windows.png)

6. To remove a window from a stack, press SUPER + Enter and use arrow keys to position the window outside of the stack.

![Remove from Stack](/images/tiling-stacking-windows/remove-from-stack.png)
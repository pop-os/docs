# Manipulating Windows with Tiling, Stacking & Resizing

This section describes the Auto Tiling, Stacking, and window adjustment features in Pop!\_OS.

---
## Window Adjustment Mode

Adjustment mode allows users to easily manipulate the placement of windows using keyboard shortcuts.

Place a window into adjustment mode by bringing the window into focus, and then pressing `SUPER` + `Enter`. The window will be highlighted in yellow. You can now manipulate the window with the `🠐` `🠑` `🠒` `🠓` keys in combination with other keys.

<video autoplay loop>
    <source src="/images/tiling-stacking-windows/adjustment-mode.webm" />
</video>

While in adjustment mode, press and hold `Shift` and use the `🠐` `🠑` `🠒` `🠓` keys to resize the window. Hit `Enter` to apply sizing.

<video autoplay loop>
    <source src="/images/tiling-stacking-windows/adjustment-mode-resize.webm" />
</video>

All keyboard shortcuts available in adjustment mode can be viewed and modified in Settings ➞ Keyboard ➞ View and Customize Shortcuts ➞ Move, resize, and swap windows. You can also view all tiling shortcuts by clicking the tiling button in the upper right corner of the screen, and then clicking `View All`.

![Drop Down Shortcuts](/images/tiling-stacking-windows/top-right-dropdown-shortcuts.png)

## Auto Tiling Windows

Pop!\_OS optimizes workflows using a smart window management system called Auto Tiling. Auto Tiling automatically positions and sizes windows to minimize wasted screen space.

![Auto Tiling](/images/tiling-stacking-windows/auto-tiling.png)

Enable Auto Tiling by clicking on the tile icon in the upper right corner and enabling the toggle, or by pressing `SUPER` + `Y`. Tiling settings include options for window titles, active window hint, active window color, and gaps.

![Enable Autotiling](/images/tiling-stacking-windows/enable-autotiling.png)

All keyboard shortcuts for Auto Tiling mode can be found in Settings ➞ Keyboard ➞ View and Customize Shortcuts ➞ Tiling.

| Option                 | Function |
|----------------------|--------|
| Tile Windows| Toggles the Auto Tiling feature on or off.  |
| Floating Window Exceptions  | Allows adding exceptions to the Auto Tiling feature allowing free positioning of specified windows.|
| Toggle Tiling          | Enables or disables the Auto Tiling feature with a keyboard shortcut. |
| Show Active Hint       | Highlights the selected window with a colored border. |
| Gaps                | Sets gap spacing between tiled windows. |

### Add a Floating Window Exception

Floating Window Exceptions exclude individual windows from Auto Tiling. Pop!\_OS applies default exceptions to some applications based on user feedback.

1. Run the application that needs to be exempted from Auto Tiling. Click the tile menu, then click `Floating Window Exceptions`.

    ![Floating Window Exceptions](/images/tiling-stacking-windows/floating-window-exceptions.png)

2. Click `Select` to add an exception.

    ![Click Select](/images/tiling-stacking-windows/click-select.png)

3. Select the running application that should be exempted from Auto Tiling.

    ![Select Exempted App](/images/tiling-stacking-windows/select-exempted-app.png)

4. Choose to create an exception for all windows belonging to an application, or only the currently selected window.

    - **Current Window Only**: This option uses the window's title to apply the exception in addition to its application, so any windows with the same title (now or in the future) will all have the exception applied.
    - **This App's Window**: This option will apply the exception to all windows launched by a specified application.

    In this example, only the current Terminal window will be selected for exemption.

    ![Current Window Only](/images/tiling-stacking-windows/current-window-only.png)

5. The Terminal window can now be dragged around freely.

    ![Drag Shell Freely](/images/tiling-stacking-windows/drag-shell-freely.png)

## Stacking Windows

Stacking is an additional Auto Tiling feature enabling multiple windows to occupy the same screen space.

1. While Auto Tiling is enabled, select a window and press `SUPER` + `S` to create a stack. Stacks have a yellow list of windows at the top.

    <video autoplay loop>
        <source src="/images/tiling-stacking-windows/enable-stacking.webm" />
    </video>

2. Select a separate window and press `SUPER` + `Enter` to enter adjustment mode. The window to be merged is designated by a yellow highlight across the entire window.

    <video autoplay loop>
        <source src="/images/tiling-stacking-windows/highlight-for-stacking.webm" />
    </video>

3. Use the `🠐` `🠑` `🠒` `🠓` keys to move the window into the stack.

    <video autoplay loop>
        <source src="/images/tiling-stacking-windows/move-into-stack.webm" />
    </video>

4. Launching additional applications while a window within a stack is selected will automatically add that application to the same stack.

    <video autoplay loop>
        <source src="/images/tiling-stacking-windows/launch-additional-app.webm" />
    </video>

5. Use `SUPER` + `🠐` `🠒` keys to navigate between windows in the stack.

    <video autoplay loop>
        <source src="/images/tiling-stacking-windows/navigate-stacked-windows.webm" />
    </video>

6. Remove a window from the stack by pressing `SUPER` + `Enter` to activate adjustment mode, and then use `🠐` `🠑` `🠒` `🠓` keys to move the window outside of the stack.

    <video autoplay loop>
        <source src="/images/tiling-stacking-windows/remove-from-stack.webm" />
    </video>

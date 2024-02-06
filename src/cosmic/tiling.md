# Window Management

Windows are managed by the [cosmic-comp](https://github.com/pop-os/cosmic-comp) Wayland compositor. In addition to classic drag-and-drop movement, COSMIC includes several advanced window management features:

- [Tiling](#tiling)
- [Workspaces](#workspaces)
- [Stacking](#stacking)

## Tiling

Window tiling automatically arranges windows so there's no wasted space between them. To enable or disable tiling on a workspace, press `Super` + `Y`.

To move a window in tiling mode, click and drag the window to the desired location, or hold down `Super` + `Shift` and press the arrow keys to move the window into the desired location.

To change the orientation of a window (from portrait to landscape, or vice-versa), press `Super` + `O`.

To maximize a window (covering up all other windows on the workspace), or to unmaximize a window, press `Super` + `M`.

## Workspaces

Workspaces provide virtual screens, allowing windows to be separated into groups. Workspaces are automatically created and removed as needed-- a workspace is created when you move a window onto it, and it's removed when it has no more windows. To see an overview of your workspaces, press `Super` + `D`.

To switch workspaces, hold down `Super` and use the arrow keys. (The desktop will switch to the next workspace if you arrow past the last window.)

To move an open window to another workspace, hold down `Super` + `Shifft` and press the arrow keys to move the window past the edge of the screen.

## Stacking

Stacking allows multiple windows to be grouped into one window "stack" with tabs.

![Stacked windows]()

To create a stack, focus a window in the desired position and press `Super` + `S`, then move other windows into the stack using the normal methods (`Super` + direction keys, or the mouse).
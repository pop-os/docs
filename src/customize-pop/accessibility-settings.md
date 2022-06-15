# Accessibility Settings

Options to configure accessibility settings are located in `Settings` ➞ `Accessibility`. Accessibility features provide visual and audio enhancements to highlight system actions for greater usability. This section briefly describes each setting, but more information can be found on [GNOME's help page](https://help.gnome.org/users/gnome-help/stable/a11y.html).

![Accessibility Settings](/images/accessibility-settings/accessibility-settings.png)

## Always Show Accessibility Menu

When the `Always Show Accessibility Menu` is enabled, accessibility options can be toggled using an icon in the upper right corner.

![Menu in Tray](/images/accessibility-settings/menu-in-tray.png)

**Click image to enlarge**

<a href="/images/accessibility-settings/always-show-menu.png" target="blank">
    <img src="/images/accessibility-settings/always-show-menu.png" width="758px" height="428px">
</a>

## Seeing

`Seeing` settings provide visual enhancements to help visually impaired users navigate the operating system's user interface.

### High Contrast

Enabling `High Contrast` to applies a high contrast theme to windows and icons.

#### High Contrast Mode Off

**Click image to enlarge**

<a href="/images/accessibility-settings/contrast-mode-off.png" target="blank">
    <img src="/images/accessibility-settings/contrast-mode-off.png" width="733px" height="456px">
</a>

#### High Contrast Mode On

**Click image to enlarge**

<a href="/images/accessibility-settings/contrast-mode-on.png" target="blank">
    <img src="/images/accessibility-settings/contrast-mode-on.png" width="733px" height="456px">
</a>

### Large Text

Enabling `Large Text` increases the size of text across system windows and supported applications.

#### Large Text Disabled

**Click image to enlarge**

<a href="/images/accessibility-settings/before-lt.png" target="blank">
    <img src="/images/accessibility-settings/before-lt.png" width="733px" height="456px">
</a>

#### Large Text Enabled

**Click image to enlarge**

<a href="/images/accessibility-settings/after-lt.png" target="blank">
    <img src="/images/accessibility-settings/after-lt.png" width="733px" height="456px">
</a>

### Enable or Disable Animations

Animations appear when minimizing and maximizing windows. Disabling animations may improve performance on systems with low video resources.

#### Animations Enabled

<video autoplay loop>
    <source src="/images/accessibility-settings/animations-enabled.webm" />
</video>

#### Animations Disabled

<video autoplay loop>
    <source src="/images/accessibility-settings/animations-disabled.webm" />
</video>

### Cursor Size

`Cursor Size` allows users to choose between five cursor sizes.

![Cursor Size](/images/accessibility-settings/cursor-size.png)

### Zoom

The `Zoom` setting designates all or a part of the screen to display magnified content. This feature can be further customized to render the zoomed area specific portions of the screen, increase or decrease the zoom magnification, add a crosshair, and add color effects to the zoomed area.

**Click image to enlarge**

<a href="/images/accessibility-settings/zoom-options.png" target="blank">
    <img src="/images/accessibility-settings/zoom-options.png" width="733px" height="456px">
</a>

#### Magnification

This option determines the magnification of the zoom effect. Values range from 1-20 and correspond to percentages; a value of 4.0 applies a magnification of 400%.

![Magnification](/images/accessibility-settings/magnification.png)

#### Follow Mouse Cursor & Screen Part

If `Full Screen` is selected under `Screen part` and the `Follow mouse cursor` radio button is selected, the magnification affect is rendered to the entire display area.

<video autoplay loop>
    <source src="/images/accessibility-settings/full-zoom.webm" />
</video>

#### Follow Mouse Cursor & Half Screen Zoom

Select a portion of the screen to display the rendered zoom effect. If `Follow mouse cursor` remains selected, the `Top Half` and `Bottom Half` options will render the zoom effect to an unfixed narrow band of the screen. The `Left Half` and `Right Half` options will render the zoom effect to an unfixed rectangular portion of the screen.

<video autoplay loop>
    <source src="/images/accessibility-settings/half-zoom.webm" />
</video>

#### Magnify a Fixed Portion of the Screen

Select the radio button next to `Screen part` to focus zoom rendering to the section of the screen selected in the dropdown.

![Screen Part](/images/accessibility-settings/screen-part.png)

The zoomed area of the screen renders to a static portion that corresponds with the selected drop-down option.

<video autoplay loop>
    <source src="/images/accessibility-settings/screen-part.webm" />
</video>

**Magnifier Extends Outside of the Screen**

When `Magnifier extends outside of the screen` is enabled, magnified content continues to scroll when the cursor moves toward the edges of the screen.

**Disabled**

![Screen Part](/images/accessibility-settings/extend-disabled.png)

**Enabled**

![Screen Part](/images/accessibility-settings/extend-enabled.png)

**Keep Magnifier Cursor Centered**

When `Keep magnifier cursor centered` is enabled, the cursor stays in a fixed position in the center unless moving along the screen's edges. Magnified content always scrolls beneath the cursor.

<video autoplay loop>
    <source src="/images/accessibility-settings/cursor-centered.webm" />
</video>

**Magnifier Cursor Pushes Contents Around**

When `Magnifier cursor pushes contents around` is enabled, magnified contents do not move until the cursor pushes against the edges of the magnified area.

<video autoplay loop>
    <source src="/images/accessibility-settings/pushes-content.webm" />
</video>

**Magnifier Cursor Moves with Contents**

Magnified content moves with the mouse, but the mouse does not remain in a fixed position on the screen. This provides indication of the general area of the mouse's position on the un-magnified screen.

<video autoplay loop>
    <source src="/images/accessibility-settings/moves-with-content.webm" />
</video>

#### Crosshairs

Crosshairs help useres locate their mouse while navigating zoomed content.

<video autoplay loop>
    <source src="/images/accessibility-settings/crosshairs.webm" />
</video>

| Option | Function |
|---------|----------|
| Overlaps mouse cursor | Check this setting to layer the crosshairs over the cursor. Uncheck this setting end the crosshair lines before they reach the cursor. |
| Thickness | Adjust the thickness of the crosshair's lines between 1 and 100 pixels. |
| Length | Set the length of the visible crosshair. |
| Color | Launch a color picker to customize the crosshair's color and transparency. |

#### Color Effects

Color effects modify the color of zoomed content. These settings assist users with photophobia or when using the computer under poor lighting conditions.

<video autoplay loop>
    <source src="/images/accessibility-settings/color.webm" />
</video>

| Option | Function |
|--------|----------|
| White on black | Toggle on to invert white and black colors: White becomes black, black becomes white, dark grays become lighter, lighter colors and grays become darker. Color hues do not change. |
| Brightness | Adjust the overall brightness of the zoomed content. `Low` and `High` are reversed when `White on black` is toggled to the on position. |
| Contrast | Adjust the contrast of the zoomed content. `Low` decreases contrast, while `High` increases contrast. |
| Color | Adjust the color saturation of zoomed content. Setting this to `None` will convert zoomed content to grayscale. |

### Screen Reader

The Screen Reader option enables a feature that converts the displayed text of a focused window to audible speech.

![Screen Reader](/images/accessibility-settings/screen-reader.png)

### Sound Keys

When `Sound Keys` is enabled, users will hear a beep whenever `Num Lock` or `Caps Lock` are turned on or off.

![Sound Keys](/images/accessibility-settings/sound-keys.png)

## Hearing

When the `Visual Alerts` setting is enabled, alert sounds will be accompanied by a visual flickering of the entire screen or window.

### Flash the Entire Window

<video autoplay loop>
    <source src="/images/accessibility-settings/flash-window.webm" />
</video>

### Flash the Entire Screen

<video autoplay loop>
    <source src="/images/accessibility-settings/flash-screen.webm" />
</video>

## Typing

Typing accessibility features enhance keyboard input behavior.

### Screen Keyboard

Enabling `Screen Keyboard` will display an interactive keyboard wherever text entry is possible.

<video autoplay loop>
    <source src="/images/accessibility-settings/screen-keyboard.webm" />
</video>

### Repeat Keys

Enabling `Repeat Keys` causes key inputs to repeat when a key is held down. Users can configure the delay before this actions occurs, and the repeat speed once the action occurs. Disabling `Repeat Keys` causes every key press to render as a single input.

<video autoplay loop>
    <source src="/images/accessibility-settings/repeat-keys.webm" />
</video>

### Cursor Blinking

When `Cursor Blinking` is enabled, the cursor will blink when a text field is selected. Users can also adjust the blink speed.

<video autoplay loop>
    <source src="/images/accessibility-settings/cursor-blinking.webm" />
</video>

### Typing Assist

`Typing Assist` settings modify the way a keyboard accepts input from the user.

![Typing Assist](/images/accessibility-settings/typing-assist.png)

| Option | Function |
|--------|--------|
| Sticky Keys | Perform multi-key shortcuts by pressing keys individually instead of holding down multiple keys simultaneously. |
| Slow Keys | Increase the delay between the time a key is pressed and when it appears on the screen. |
| Bounce Keys | Ignore subsequent key presses if they occur too quickly on the same key. |

## Pointing & Clicking

`Pointing & Clicking` settings extends input options for controlling the mouse.

![Pointing & Clicking](/images/accessibility-settings/pointing-clicking.png)

| Option | Function |
|--------|----------|
| Mouse Keys | Control the mouse cursor using the num keypad. `Num Lock` must be off. |
| Locate Pointer | The cursor performs an animation whenever the left `Ctrl` key is pressed. |
| Click Assist | Trigger a simulated double-click when holding down the primary mouse button. A click can also be triggered simply by hovering the mouse over an item on the screen. |
| Double Click Delay | Set the amount of time required to register a double click. |

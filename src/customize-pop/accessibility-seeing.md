# Seeing

`Seeing` settings provide visual enhancements to help visually impaired users navigate the operating system's user interface.

---

## High Contrast

Enabling `High Contrast` applies a high contrast theme to windows and icons.

### High Contrast Mode Off

<img src="/images/accessibility-settings/contrast-mode-off.png" alt="High contrast mode off" class="thumbnail" />

### High Contrast Mode On

<img src="/images/accessibility-settings/contrast-mode-on.png" alt="High contrast mode on" class="thumbnail" />

## Large Text

Enabling `Large Text` increases the size of text across system windows and supported applications.

### Large Text Disabled

<img src="/images/accessibility-settings/before-lt.png" alt="Large text disabled" class="thumbnail" />

### Large Text Enabled

<img src="/images/accessibility-settings/after-lt.png" alt="Large text enabled" class="thumbnail" />

## Enable or Disable Animations

Animations appear when minimizing and maximizing windows. Disabling animations may improve performance on systems with low video resources.

### Animations Enabled

<video autoplay loop>
    <source src="/images/accessibility-settings/animations-enabled.webm" />
</video>

### Animations Disabled

<video autoplay loop>
    <source src="/images/accessibility-settings/animations-disabled.webm" />
</video>

## Cursor Size

`Cursor Size` allows users to choose between five cursor sizes.

![Cursor Size](/images/accessibility-settings/cursor-size.png)

## Zoom

The `Zoom` setting designates all or a part of the screen to display magnified content. This feature can be further customized to render the zoomed area to specific portions of the screen, increase or decrease the zoom magnification, add a crosshair, and add color effects to the zoomed area.

<img src="/images/accessibility-settings/zoom-options.png" alt="zoom options" class="thumbnail" >

### Magnification

This option determines the magnification of the zoom effect. Values range from 1-20 and correspond to percentages; a value of 4.0 applies a magnification of 400%.

![Magnification](/images/accessibility-settings/magnification.png)

### Follow Mouse Cursor & Screen Part

If `Full Screen` is selected under `Screen part` and the `Follow mouse cursor` radio button is selected, the magnification effect is rendered to the entire display area.

<video autoplay loop>
    <source src="/images/accessibility-settings/full-zoom.webm" />
</video>

### Follow Mouse Cursor & Half Screen Zoom

Select a portion of the screen to display the rendered zoom effect. If `Follow mouse cursor` remains selected, the `Top Half` and `Bottom Half` options will render the zoom effect to an unfixed horizontal band of the screen. The `Left Half` and `Right Half` options will render the zoom effect to an unfixed vertical band of the screen.

<video autoplay loop>
    <source src="/images/accessibility-settings/half-zoom.webm" />
</video>

### Magnify a Fixed Portion of the Screen

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

Crosshairs help users locate their mouse while navigating zoomed content.

<video autoplay loop>
    <source src="/images/accessibility-settings/crosshairs.webm" />
</video>

| Option | Function |
|---------|----------|
| Overlaps mouse cursor | Check this setting to layer the crosshairs over the cursor. Uncheck this setting to end the crosshair lines before they reach the cursor. |
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
| Brightness | Adjust the overall brightness of the zoomed content. `Low` and `High` are reversed when `White on black` is enabled. |
| Contrast | Adjust the contrast of the zoomed content. `Low` decreases contrast, while `High` increases contrast. |
| Color | Adjust the color saturation of zoomed content. Setting this to `None` will convert zoomed content to grayscale. |

## Screen Reader

The Screen Reader option enables a feature that converts the displayed text of a focused window to audible speech.

![Screen Reader](/images/accessibility-settings/screen-reader.png)

## Sound Keys

When `Sound Keys` is enabled, users will hear a beep whenever `Num Lock` or `Caps Lock` are turned on or off.

![Sound Keys](/images/accessibility-settings/sound-keys.png)
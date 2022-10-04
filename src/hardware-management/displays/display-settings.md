# Configuring External Displays

Navigate to `Settings` ➞ `Displays` to adjust multi-monitor placement, resolution, and scaling.

![Display Settings Menu](/images/config-displays/display-settings.png)

---

## Night Light

Nightlight prevents eye strain and sleeplessness by reducing exposure to blue light.

![Nightlight Options](/images/config-displays/night-light-settings.png)

Toggle Nightlight to the right switch position to enable it.

<video autoplay loop>
    <source src="/images/config-displays/nightlight-toggle.webm" />
</video>

Set `Schedule` to `Sunrise to Sunset` to use Nightlight during evening hours. Use `Manual` to set a custom time period where Nightlight is enabled, then set the custom time period in the `Times` section.

Use the slider to adjust the Nightlight intensity.

<video autoplay loop>
    <source src="/images/config-displays/nightlight-adjust.webm" />
</video>

## Multi-Monitor Display Options

### Display Mode

#### Join Displays

The `Join Displays` option allows spanning content across connected displays.

![Joined Displays](/images/config-displays/join-displays.png)

#### Mirror

The `Mirror` option displays the same content to all displays. When this option is selected, you can select the orientation, resolution, and scale that will apply to both displays. Some resolution options may not be available if your displays have different resolutions.

![Mirrored Displays](/images/config-displays/mirror-displays.png)

#### Single Display

The `Single Display` option displays content to the display tab selected when enabling this option. All other displays are disabled.

![Single Display](/images/config-displays/single-display.png)

### Positioning Displays

Click and drag the display rectangles to position the displays so that they match their physical placement.

![Position Displays](/images/config-displays/position-displays.png)

## Display Options

If you are using a multi-monitor setup, you can assign the below settings to a specific monitor by selecting the tab with the desired monitor's label.

![Multi-monitor tabs in Display Settings]()

### Orientation

Landscape

![Landscape Orientation](/images/config-displays/landscape.png)

Portrait (Right)

![Portrait Right](/images/config-displays/portrait-right.png)

Portrait (Left)

![Portrait Left](/images/config-displays/portrait-left.png)

Landscape (Flipped)

![Landscape Flipped](/images/config-displays/landscape-flipped.png)

>**Note**: Opening the Terminal with `Super` + `T` and entering the `xrandr -o normal` command will return a display to `Lanscape` orientation. This can be useful if mouse clicks do not register correctly on a flipped display.

### Resolution

Resolution is the number of length-by-width pixels used to render content on a display. Higher resolution values provide finer image detail. The options available for this setting are dependant on the resolutions supported by your display. A display's native resolution (usually the maximum possible setting) is the actual number of pixels available on the display, and will provide the clearest possible image.

### Refresh Rate

Refresh rate refers to the number of times per second that the image is updated on the display. A higher refresh rate will make the motion of objects on the screen appear smoother. The available refresh rate options depend on the refresh rates supported by your display.Some displays or connectors support different refresh rates for different resolutions (e.g. a higher refresh rate can be achieved with a lower resolution.)

### Scale

Increasing the scale percentage will make visual elements larger, but use more screen real-estate. Decreasing the display percentage will make visual elements smaller, but allow more objects to be displayed on the screen. Default scaling options multiply by whole numbers.

Example of a display at 100% scale:

![100% Scale](/images/config-displays/100-scale.png)

Example of a display at 200% scale:

![200% Scale](/images/config-displays/200-scale.png)

>**Note**: [Accessibility features](/customize-pop/accessibility-seeing.md) allow you to zoom into sections of the screen using the mouse, make text bigger, and enable high contrast mode for better visibility.

### Fractional Scaling

Enable `Fractional Scaling` to access scaling options that do not multiply object scaling by whole numbers. This option is also necessary when setting different scale settings per display in a multi-display configuration.

![Fractional Scaling Options](/images/config-displays/fractional-scaling-options.png)

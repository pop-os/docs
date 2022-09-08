# Configuring External Displays

Navigate to `Settings` ➞ `Displays` to adjust multi-monitor placement, resolution, and scaling.

![Display Settings Menu](/images/config-displays/display-settings.png)

## Nightlight

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

## Display Options

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

Resolution is the number of length-by-width pixels used to render content on a display. Higher resolution values provide finer image detail. The options available for this setting are dependant on the resolutions supported by your display. A display's native resolution is the actual number of pixels available on the display, and will provide the clearest possible image.

### Refresh Rate

Refresh rate refers to the number of times per second that the image is updated on the display. A higher refresh rate will make the motion of objects on the screen appear smoother. The available refresh rate options depend on the refresh rates supported by your display.

### Scale

Increasing the scale percentage will make visual elements larger, but use more screen real-estate. Decreasing the display percentage will make visual elements smaller, but allow more objects to be displayed on the screen. Default scaling options multiply by whole numbers.

Example of a display at 100% scale:

![100% Scale](/images/config-displays/100-scale.png)

Example of a display at 200% scale:

![200% Scale](/images/config-displays/200-scale.png)

>**Note**: [Accessibility features](/customize-pop/accessibility-seeing.md) allow you to zoom into sections of the screen using the mouse, make text bigger, and enable high contrast mode for better visibility.

### Fractional Scaling

Enable `Fractional Scaling` to access scaling options that do not multiply object scaling by whole numbers.

![Fractional Scaling Options](/images/config-displays/fractional-scaling-options.png)

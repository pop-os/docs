# Audio Troubleshooting

If your speakers or microphone are not working, you can check various points in the audio stack to determine where the problem lies.

---

## Testing Audio

In `Settings` -> `Sound`, click `Test` to display the speakers in your audio configuration. Click a speaker to play a test sound that states the speaker's position.

![Test Output Device](/images/audio-mic/test-audio-output.png)

Microphones can be tested using the activity meter in the `Input` section.

If a sound device is not working, first steps include:

- Ensure the device is plugged in (and, if applicable, powered on).
- Ensure the device is selected as the output or input device in `Settings` -> `Sound`.
- Ensure the volume for the device and/or the application is not muted.

---

## AlsaMixer

AlsaMixer is a terminal user interface (TUI) program that directly interfaces with ALSA. Because ALSA works at a lower level than PipeWire, you usually do not need to use AlsaMixer, but it can be useful to troubleshoot a lack of sound or speaker options.

For example, if you find that you do not have any audio even though the Settings application shows that sound is not muted, you can check AlsaMixer to see if the output is muted at a lower leve.

### Launching AlsaMixer

Open the Terminal and type `alsamixer` to launch the program.

![Launch Alsamixer](/images/audio-mic/launch-alsamixer.png)

### Selecting a Sound Card

Press `F6` and use the arrow keys to highlight a sound card. Press `Enter` to select the sound card.

![Select Sound Card](/images/audio-mic/select-sound-card.png)

### Selecting an Input/Output

Use the `🠐` and `🠒` arrow keys to navigate between input/output devices. If you see an output labeled `MM`, the output is muted; it can be unmuted by selecting it and pressing `m`. You can also adjust the volume using the up and down arrow keys.

gif

### Exiting AlsaMixer

AlsaMixer can be exited by pressing `Esc` until the application closes (pressing `Esc` more than once may be necessary if a menu is open within AlsaMixer.) You can also press `Ctrl` - `C` to immediately exit AlsaMixer.

---

## Terminal Commands

### Show Sound Cards Detected by the Kernel

If ALSA doesn't list a sound card, it may not be physically detected by the system at all. If the Linux kernel sees a sound card, it will show up in your `lspci` output. This command will list every sound card your system detects, and show the driver being used for each one:

```bash
lspci -v | grep -A6 Audio
```

### Enumerate ALSA Information

ALSA commands can be used to view audio-related diagnostic information and to reset audio drivers.

View all devices detected by ALSA:

```bash
aplay -l
```

View all recording devices detected by ALSA:

```bash
arecord -l
```

Reload sound driver modules:

```bash
sudo alsa force-reload
```

The `alsa-info` command gathers a number of outputs, including some of the above-listed outputs, and packages them for convenient sharing.

```bash
alsa-info
```

Press `y` and hit `Enter` to upload this information too alsa-project.org. Once uploaded, you will receive a link that you can use to share your audio information with a community or support team.

### Check for PipeWire Errors

This command will check the status of PipeWire and show any error messages or automatic restart logs:

```bash
systemctl --user status pipewire
```

Use this command to view log history for `pipewire.service` (add `-b 0` to restrict log output to the current boot session):

```bash
journalctl -u pipewire --user
```

Note that `pipewire.service` is not the only PipeWire service. There is also:

- pipewire.socket
- pipewire-session-manager.service
- pipewire-media-session.service
- pipewire-pulse.service
- pipewire-pulse.socket

You can view all of these logs at once by running this command (add `-b 0` to restrict log output to the current boot session):

```bash
journalctl -u pipewire.service -u pipewire.socket -u pipewire-session-manager.service -u pipewire-media-session.service -u pipewire-pulse.service -u pipewire-pulse.socket --user
```

### Reset PipeWire to Defaults

Clearing the current user's settings for PipeWire reverts PipeWire to its default settings:

```bash
rm -r ~/.local/state/wireplumber/*
```

Additionally, `~/.config/pipewire/` and `~/.config/wireplumber/` can contain user settings, but are not present by default:

```bash
rm -r ~/.config/pipewire/
rm -r ~/.config/wireplumber/
```

>**Note**: These commands will not reset system-wide settings that may have been altered, such as settings saved in the `/etc` folder.

### Restarting the PipeWire Daemon

This command restarts the WirePlumber session manager, PipeWire sound daemon, and pipewire-pulse sound daemon:

```bash
systemctl --user restart wireplumber pipewire pipewire-pulse
```

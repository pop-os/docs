# Useful Audio Commands

Use Terminal commands to restart daemons and drivers that control audio streams.

---

## ALSA Commands

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

## Additional Audio Commands

### Listing Detected Sound Cards

If ALSA doesn't list a sound card, it may not be physically detected by the system at all. If the Linux kernel sees a sound card, it will show up in your `lspci` output. This command will list every sound card your system detects, and show the driver being used for each one:

```bash
lspci -v | grep -A6 Audio
```

### Checking PipeWire's Status

This command will check the status of PipeWire and show any error messages or automatic restart logs:

```bash
systemctl --user status pipewire
```

### Viewing PipeWire Logs

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

### Resetting PipeWire to Defaults

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

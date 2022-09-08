# Useful Audio Commands

Add intro<!--https://support.system76.com/articles/audio/-->

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

## Additional Audio Commands

### List Detected Sound Cards

If ALSA doesn't list a sound card, it may not be physically detected by the system at all. If the Linux kernel sees a sound card, it will show up in your `lspci` output. This command will list every sound card your system detects, and show the driver being used for each one:

```bash
lspci -v | grep -A6 Audio
```

### Check PipeWire's Status

This command will check the status of PipeWire and show any errors if automatic restarts raised any errors:

```bash
systemctl --user status pipewire
```

### Reset PipeWire to Defaults

Clearing the current settings for Pipewire  may allow the defaults to be used again. To revert to defaults and clear any current saved settings run the following commands:

```bash
rm -r ~/.local/state/wireplumber/*
```

### Reinstall PipeWire

```bash
sudo apt reinstall libpipewire-0.3-0 libpipewire-0.3-common libpipewire-0.3-modules pipewire pipewire-audio-client-libraries pipewire-bin pipewire-pulse
```

### Restart the PipeWire Daemon

This set of commands first restarts the sound daemon and removes the user's configuration for PulseAudio. On systems still using PulseAudio as a server, it restarts the PulseAudio server, which will create new default audio configuration files.

```bash
systemctl --user restart wireplumber pipewire pipewire-pulse
```

```bash
rm -r ~/.config/pulse
```
# Audio Applications & Extensions

These applications provide control and customization settings for audio devices beyond the `Settings` menu.

---

## EasyEffects

[EasyEffects](https://github.com/wwmm/easyeffects) is a third-party application that can apply audio effects and filters to audio input and output streams. You can download and install EasyEffects from the Pop!\_Shop.

![EasyEffects](/images/audio-mic/easyeffects.png)

IntThe `Output` tab, selecting `Players` at the bottom displays all applications currently playing audio to the output device. The source's audio stream is represented in the wave form at the top.

![Output Devices](/images/audio-mic/output-devices.png)

In the `Input` tab, selecting `Recorders` displays all applications currently recording audio from input device. The source's audio stream is represented in the wave form at the top.

![Input Devices](/images/audio-mic/input-devices.png)

### Include or Exclude Sources

Select `Enable` to enable applied effects to the source. Unchecking `Enable` will leave the source in the list, but will not apply effects. Selecting `Exclude` will exclude the source from applied effects and remove it from the list.

![Enable or Disable Source](/images/audio-mic/enable-source.png)

Excluded sources can be re-added by clicking the `Excluded Apps` button in the lower right corner.

![Show Excluded Apps](/images/audio-mic/show-excluded.png)

### Adding Effects to an Audio Source

Audio effects and filters are often used to modify audio streams in a way that improves or enhances the input or output. This can include increasing overall volume levels, eliminating background noise, and equalizing frequencies.

In this example, a background noise cancellation filter is added to the microphone input source.

1. Launch EasyEffects and click `Input` at the top. Make sure `Enabled` is checked for the input source.

    ![Select Input Tab](/images/audio-mic/select-input-tab.png)

2. Select the `Effects` button at the bottom. Click `Add Effect` on the left. Search for `noise` and click the `+` to add the `Noise Reduction` effect.

    ![Add Effect](/images/audio-mic/add-effect.png)

4. To test the effect, click the button the lower right corner to send the input stream to the output stream. Use the sliders to increase the `Input` (microphone) or `Output` (speakers).

    ![Testing Effects](/images/audio-mic/test-effect.png)

## Audio Output Switcher

[Audio Output Switcher](https://extensions.gnome.org/extension/751/audio-output-switcher/) is a GNOME extension that adds selectable audio input/output devices to the System menu. See [this section](/customize-pop/gnome-tweaks-extensions/gnome-extensions.md) for more information about installing GNOME Extensions.

![Audio Output Switcher](/images/audio-mic/output-switcher.png)

## AlsaMixer

AlsaMixer is a graphical command-line program that directly interfaces with the Advanced Linux Sound Architecture (ALSA) framework. AlsaMixer provides more advanced audio configuration options, like selecting sound cards and viewing all system audio devices. AlsaMixer comes preloaded in Pop!_OS and does not require installation.

### Launching AlsaMixer

Open the Terminal and type `alsamixer` to launch the program.

![Launch Alsamixer](/images/audio-mic/launch-alsamixer.png)

### AlsaMixer Controls

Many AlsaMixer functions are controlled using keyboard commands. Press `F1` to view all AlsaMixer controls.

![Alsamixer Keyboard Controls](/images/audio-mic/alsamixer-controls.png)

AlsaMixer communicates directly with system-level audio processes, which makes it useful for muting or unmuting audio streams at a low level. Use the `🠐` `🠒` keys to navigate between sources, and press `m` to mute or unmute a source.

### Selecting a Sound Card

Press `F6` and use the arrow keys to highlight a sound card. Press `Enter` to select the sound card.

![Select Sound Card](/images/audio-mic/select-sound-card.png)

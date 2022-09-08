# Audio & Microphone Settings

This section describes selection and configuration of audio input and output devices. Set system volume, volume levels per application, output devices, and input devices in `Settings` ➞ `Sound`.

Pop!\_OS 22.04 uses the [PipeWire](https://github.com/pop-os/pipewire) server to handle audio and video streams. Previous versions of Pop!\_OS use [PulseAudio](https://www.freedesktop.org/wiki/Software/PulseAudio/).

---

## Understanding Sound Servers in Linux

Explain what sound servers are and how they work.

## Setting Volume Levels

Drag the slider under `Volume Levels` right or left to increase or decrease the volume level.

![Sound Settings](/images/audio-mic/sound-settings.png)

### Over-Amplification

`Over-Amplification` allows you to raise the volume over 100%. This can result in loss of audio quality. As a best practice, it is recommended to increase the volume in the application's individual volume settings.

#### Over-Amplification Disabled

![Over Amp Disabled](/images/audio-mic/over-amp-disabled.png)

#### Over-Amplification Enabled

![Over Amp Enabled](/images/audio-mic/over-amp-enabled.png)

### Set Volume Levels Per Application

Adjust the sliders in the `Volume Levels` section for each application as desired.

![Per Application](/images/audio-mic/per-application.png)

## Choosing an Audio Output Device

Navigate to `Settings` ➞ `Sound`. Click the dropdown menu next to `Output Device`. Select the desired output device.

![Select Output Device](/images/audio-mic/select-output-device.png)

### Testing Output Devices

Click `Test`, then select the left and right speakers. An audible test will play through each speaker.

![Test Output Device](/images/audio-mic/test-audio-output.png)

## Choosing an Audio Input Device

Navigate to `Settings` ➞ `Sound`. Click the dropdown menu next to `Input` and select the desired input source.

![Select Input Device](/images/audio-mic/select-input-device.png)

### Adjust Input Device Volume

Move the volume slider to the right to increase microphone sensitivity, and slide to the left to decrease sensitivity.

![Mic Sensitivity](/images/audio-mic/mic-sensitivity.png)

### Testing Input Devices

Observe activity on the bar below the selected input device to confirm audio input is being detected.

<video autoplay loop>
    <source src="/images/audio-mic/detected-input.webm" />
</video>

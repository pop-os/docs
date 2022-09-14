# Speaker & Audio Settings

This section describes selection and configuration of audio input and output devices. Set system volume, volume levels per application, output devices, and input devices in `Settings` ➞ `Sound`.

Pop!\_OS 22.04 uses the [PipeWire](https://github.com/pop-os/pipewire) server to handle audio and video streams. Previous versions of Pop!\_OS use [PulseAudio](https://www.freedesktop.org/wiki/Software/PulseAudio/).

---

## PipeWire

Pop!\_OS 22.04 and above uses the PipeWire sound server. A sound server is a low-level service that controls communication of audio streams between the software and hardware.

## System Volume

Drag the slider under `Volume Levels` right or left to increase or decrease the volume level for all applications.

![Sound Settings](/images/audio-mic/sound-settings.png)

## Set Volume Levels Per Application

Adjust the sliders in the `Volume Levels` section for each application as desired. Note that some applications will only appear in the list when actively playing audio.

![Per Application](/images/audio-mic/per-application.png)

## Over-Amplification

`Over-Amplification` allows you to raise the volume over 100%. This allows the volume of media or applications that are too quiet to be digitally boosted.

**Over-Amplification Enabled:**

![Over Amp Enabled](/images/audio-mic/over-amp-enabled.png)

## Choosing an Audio Output Device

Navigate to `Settings` ➞ `Sound`. Click the dropdown menu next to `Output Device`. Select the desired output device.

>**Note:** A computer's sound card might only allow one of its outputs available at a time. For example, many laptops only make the headphone output available when headphones are plugged in.

![Select Output Device](/images/audio-mic/select-output-device.png)

## Testing Output Devices

Click `Test` to display the speakers in your audio setup. Click a speaker to play a test sound that states the configured position for that individual speaker.

![Test Output Device](/images/audio-mic/test-audio-output.png)

## Choosing an Audio Input Device

Navigate to `Settings` ➞ `Sound`. Click the dropdown menu next to `Input` and select the desired input source.

![Select Input Device](/images/audio-mic/select-input-device.png)

## Adjust Input Device Volume

Move the volume slider to the right to increase microphone sensitivity, and slide to the left to decrease sensitivity.

![Mic Sensitivity](/images/audio-mic/mic-sensitivity.png)

## Testing Input Devices

Observe activity on the bar below the selected input device to confirm audio input is being detected.

<video autoplay loop>
    <source src="/images/audio-mic/detected-mic-input.webm" />
</video>

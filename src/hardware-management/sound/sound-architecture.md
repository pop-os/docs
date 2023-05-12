# Sound Architecture

Audio in Pop!_OS is provided by a collection of interrelated components. These components include:

## Drivers

Drivers for specific hardware sound cards (or audio chipsets) are included in the Linux kernel. Special lines of configuration to handle specific sound hardware, referred to as "quirks" or "fixups," are sometimes required in the kernel. For System76 hardware, these quirks are placed in the [Pop!_OS kernel fork](https://github.com/pop-os/linux) first, then upstreamed for other distributions to use.

## Driver API (ALSA)

[ALSA](https://alsa-project.org) (the Advanced Linux Sound Architecture) provides an application programming interface for software to access sound devices without worrying about what specific hardware is in use. Some sound card parameters, such as sample rate, can be controlled by ALSA. However, you usually do not need to configure ALSA directly-- it primarily serves to support higher-level software.

## Sound Server (PipeWire)

A sound server is the service that controls communication of audio streams. This is the software that mixes multiple audio streams together (if multiple applications are playing sound at the same time), and that you usually use to control volume levels.

Pop!\_OS 22.04 uses the [PipeWire](https://pipewire.org/) sound server (which also handles video streams.) Previous versions of Pop!\_OS used the [PulseAudio](https://www.freedesktop.org/wiki/Software/PulseAudio/) sound server; PipeWire in Pop!_OS is able to emulate PulseAudio to support older applications.

[JACK](https://jackaudio.org/) is another sound server API that is useful for professional-grade audio applications which require low latency. Prior to PipeWire, using JACK required running a specific sound server (`jackd`) instead of PulseAudio. PipeWire implements the JACK API, so applications in Pop!_OS can use JACK out-of-the-box without needing to specifically run or configure JACK.

## Sound Server Session Manager (WirePlumber)

[WirePlumber](https://pipewire.pages.freedesktop.org/wireplumber/) is a session and policy manager for PipeWire. Applications will typically send their audio directly to PipeWire, but WirePlumber helps to configure both PipeWire and ALSA.
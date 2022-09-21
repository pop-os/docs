# Configuring Webcams

Pop!_OS will automatically detect any webcams or capture cards with drivers that implement the Video4Linux2 (V4L2) API. Most USB webcams are supported via the Universal Video Class (UVC) driver built into the Linux kernel. A non-exhaustive list of compatible webcams can be found on the [UVC driver's website](https://www.ideasonboard.org/uvc/).

---

## Disabling and Enabling Webcams

You can disable your webcam by pressing `Fn` + `F10`, which disables the webcam USB bus at the device level. Press `Fn` + `F10` to re-enable the webcam, and then restart any application(s) that were using the webcam at the time it was disabled.

## Installing Cheese

You can test your webcam functionality using [Cheese](https://github.com/GNOME/cheese). Cheese is an open-source webcam booth application for Linux available for installation in the [Pop!\_Shop](manage-apps/using-pop-shop.ingmd).

![Install Cheese](/images/config-webcams/install-cheese.png)

Use the Launcher start Cheese. Your webcam should be automatically detected.

![Cheese Launched](/images/config-webcams/launch-cheese.png)

## View Detected V4L2 Devices

Run the below command to view detected webcams and capture cards. Note that many devices will show up twice in the list as two separate entries. This will return `no such file or directory` if no video devices are detected.

```bash
ls -l /dev/video*
```

![List Video Devices](/images/config-webcams/list-video-devices.png)

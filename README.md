# Maska — releases

Maska puts masks, 3D avatars and new backgrounds on your webcam picture and changes your voice, for streams and
calls. It offers two virtual devices that OBS, Discord, Zoom or a browser use like ordinary ones:

- **Maska Camera** — the webcam picture with the mask, avatar or background;
- **Maska Microphone** — your voice with the chosen effects.

This repository only holds the release files (the app's interface is in Ukrainian). Linux for now (tested on
Ubuntu 26.04 with PipeWire); Windows is planned.

## Download

Get the newest files from **[Releases](https://github.com/nevidomyi/maska-releases/releases)**.

### .deb (Ubuntu, Debian) — recommended

```sh
sudo apt install ./maska-desktop_<version>_amd64.deb
```

Then start **Maska** from the applications menu. The app updates itself: «Оновлення» → «Оновити» (it asks for your
password to install the new package).

### AppImage (any distribution)

```sh
chmod +x Maska-<version>-x86_64.AppImage
./Maska-<version>-x86_64.AppImage
```

The AppImage replaces itself when you choose «Оновити».

## The virtual camera

The camera needs the v4l2loopback kernel module:

```sh
sudo apt install v4l2loopback-dkms
sudo modprobe v4l2loopback video_nr=42 card_label="Maska Camera" exclusive_caps=1
```

The microphone needs nothing extra: Maska creates it with PipeWire/PulseAudio while it runs.

## First start

The 3D avatars are downloaded from their original sources the first time the app starts (about 400 MB in total,
in the background); an avatar you pick is downloaded first.

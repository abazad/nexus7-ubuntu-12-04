# Ubuntu 12.04 for Nexus 7 (2012)

This is an ARM version of Ubuntu 12.04 (LTS) patched with the lastest NVIDIA Tegra Drivers.

To install, copy the MROM file (https://github.com/gabrielrcouto/nexus7-ubuntu-12-04/releases/download/v1.0/ubuntu-12-04.mrom) to you tablet and use MultiROM (http://forum.xda-developers.com/showthread.php?t=2011403).

You'll need an OTG cable to plug a keyboard on your tablet and setup it.

## First step

```sh
Username: ubuntu
Password: ubuntu
```

### Configure your wifi (WPA)

```sh
$ wpa_passphrase the_name_of_your_wifi_network the_passphrase > wpa.conf
$ wpa_supplicant -B -Dwext -iwlan0 -cwpa.conf
```

### Install desktop environment

```sh
$ sudo su
Password: ubuntu
$ apt-get update
$ apt-get install ubuntu-desktop gnome-session-fallback
```

After finishing, reboot and you'll see the LightDM screen.

## Using

I recommend you to use the "GNOME Classic (No effects)" session, it's light and doesn't have the touch bug, reported on https://bugs.launchpad.net/ubuntu-nexus7/+bug/1068994

![How to choose the session](http://4.bp.blogspot.com/-1uvXhmQZ5Ic/TzW7sfOJB3I/AAAAAAAAHuk/1NSdl4NJVZM/s1600/gnome-classic-login-screen.png)

## Drivers

If you want to patch your own Linux Distribution with NVIDIA Tegra drivers, look here: https://developer.nvidia.com/linux-tegra-rel-16. The Nexus 7 (2012) uses Cardhu drivers package.

## Author

Gabriel Couto - [@gabrielrcouto](http://www.twitter.com/gabrielrcouto)

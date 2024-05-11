# Set RPI as a WiFi Router

On initial imaging of the RPI, don't set the board to use WiFi connection.
Use the rapberry pi imager to upload the 64 bit lite OS. Enable SSH to the board.

### Install RaspAP

Connect to the board via ssh:
```
ssh username@rpiname.local
```

Follow the [RaspAP instruction of installation](https://raspap.com/):

Begin with a clean install of the latest release of a supported Linux distribution. In the example below, Raspberry Pi OS (64-bit) Lite is used. Update your OS to its latest version, including the kernel and firmware, followed by a reboot:.

```
sudo apt-get update
sudo apt-get full-upgrade
sudo reboot
```
Set the WiFi country in raspi-config's Localisation Options:
```
sudo raspi-config
```
Invoke RaspAP's Quick Installer:
```
curl -sL https://install.raspap.com | bash
```

The Quick Installer will complete the steps in the manual installation for you.

Following a reboot, the wireless AP network will be configured as follows:

* IP address: 10.3.141.1
* Username: admin
* Password: secret
* DHCP range: 10.3.141.50 — 10.3.141.254
* SSID: raspi-webgui
* Password: ChangeMe

It is strongly recommended that you change these default credentials in RaspAP's Authentication and Hotspot > Security panels.

Your AP's basic settings and many advanced options may now be modified by RaspAP.
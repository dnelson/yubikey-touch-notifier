# yubikey-touch-notifier 

This repository offers a reader daemon script for
[yubikey-touch-detector](https://github.com/maximbaz/yubikey-touch-detector), which uses `notify-send`,
so you can see if your YubiKey is waiting for a touch via a notification.

## Screenshots

When YubiKey is waiting for a touch:

![Touch Notification](media/notification.png)

## Installation

Make sure you have [yubikey-touch-detector](https://github.com/maximbaz/yubikey-touch-detector) installed and
running before proceeding. Also requires `rsvg-convert`

```sh
mkdir -p ~/.local/bin/
cp ./yubikey-touch-notifier ~/.local/bin/
mkdir -p ~/.config/systemd/user
cp ./yubikey-touch-notifier.service ~/.config/systemd/user/

systemctl --user daemon-reload
systemctl --user enable --now yubikey-touch-notifier.service
```

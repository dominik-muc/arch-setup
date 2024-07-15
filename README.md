# arch-setup

This setup covers in my opinion best utilities for creating simple, yet pleasant user-experience on linux.
I will include my config files and try to update them as I learn new things.

## Setup

* window manager: hyprland

* terminal: kitty (will write my own)

* runner: anyrun (anyrun-git on aur)

* screenshot: flameshot (don't use prebuild version as it is not compatible with wayland, use flameshot-git from aur) / hyprshot (?)

* rest: ags probably


## Config

### authentication
* install `gnome-keyring` for storing passwords
* and enable it `systemctl enable --user gnome-keyring-daemon.service`
* install `polkit-gnome` for redirecting password prompts to a nice gui
* install `seahorse` for a keyring gui (Passwords and secrets)
* enable gcr `systemctl enable --user gcr-ssh-agent.service`
* add `export SSH_AUTH_SOCK=$XDG_RUNTIME_DIR/gcr/ssh` in your shell
* for gpg: add `pinentry-program /usr/bin/pinentry-gnome3` to `~/.gnupg/gpg-agent.conf`
* reload gpg agent: `gpg-connect-agent reloadagent /bye`, you should see `OK`

### audio
* install `pipewire pipewire-pulse` and optionally `pipewire-jack pipewire-alsa`
* enable services: `systemctl enable --user pipewire.service pipewire-pulse.service`
* optionally install `easyeffects` for advanced audio settings like equalizer (it requires lv2 plugins listed in optional deps)
* to auto-start it as a daemon create following systemd unit in `/etc/systemd/user/`:
```
easyeffects.service
```
```ini
[Unit]
Description=Easyeffects service
After=pipewire.service

[Service]
Type=simple
ExecStart=/usr/bin/easyeffects --gapplication-service
Restart=always

[Install]
WantedBy=pipewire.service
```
and enable it: `systemctl enable --user --now easyeffects.service`


### shell
* install `fish`
* you can check where is it installed by using `which`
* use `chsh`, enter your password and change it to fish's path





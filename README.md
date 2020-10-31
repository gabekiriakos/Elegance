# Artix Backup
<i>Dotfiles in case a reinstallation is necessary!<br>
A clean and lightweight theme with minimal transparency for i3-gaps.</i>

---

<b>Overview:</b>
* OS: [Artix](https://artixlinux.org/)
* Init: [Runit](https://en.wikipedia.org/wiki/Runit)
* WM: [i3-gaps](https://github.com/Airblader/i3)
* Status: [py3status](https://github.com/ultrabug/py3status)
* Compositor: [Picom](https://github.com/yshui/picom)
* Terminal: [Terminator](https://terminator-gtk3.readthedocs.io/en/latest/)
* Menu: [Rofi](https://github.com/davatorium/rofi)

<br>

<b>Features:</b>
* System Menu (Shutdown, Suspend, etc.): `$mod+e`
* Screenshot (via Scrot): `$mod+p`
* Toggle Window Floating: `$mod+w`
* Seamlessly Switch Workspaces: `Mod1+tab`
* Exit Active Window: `Control+q`
* Rofi Menu: `$mod+d`
* Passthrough Mode: `$mod+q` <br>

---

<b>Official Repository Apps:</b><br>
<i>xorg (all), i3 (gaps, status, lock), py3status, python-pydbus, rofi, dunst, picom, lightdm, lightdm-gtk-greeter, git, terminator, networkmanager, network-manager-applet, udisks2, udiskie, ntfs-3g, reflector, nitrogen, gimp, firefox, vlc, ranger, pcmanfm, noto-fonts, noto-fonts-extra, noto-fonts-cjk, noto-fonts-emoji, ttf-font-awesome, nvidia, lib32-nvidia-utils (multilib), steam (multilib), lutris (multilib) wine (multilib), htop, grub-customizer, lxappearance, neofetch, powerline, pulseaudio, pavucontrol, fcitx (all), fcitx-configtool, fcitx-mozc, gtk-engines, gtk-engine-murrine, gnome-themes-extra, baobab, bluez, bluez-utils, blueman, papyrus-icon-theme, pasystray</i>

<b>AUR Apps:</b><br>
<i>yay, flat-remix-gtk, ttf-monaco, gotop, fcitx-skin-material</i>

---

<b>Note:</b><br>
MPRIS is used to display player status in py3status.  [python-pydbus](https://www.archlinux.org/packages/community/any/python-pydbus/) is the only required dependency.

dbus most likely needs to be wrapped in the session to work properly<br> 
(in this case, lightdm -> /etc/lightdm/XSession):

```c
# Load dbus
if test -z "$DBUS_SESSION_BUS_ADDRESS" ; then
    ## if not found, launch a new one
    eval `dbus-launch --sh-syntax`
fi
```
Gaming applications through Lutris will not load unless [esync limits are set](https://github.com/lutris/docs/blob/master/HowToEsync.md):<br>
> On Linux distributions not using Systemd or distributions using pam-limits.conf (Arch Linux, Fedora, Solus,... ), you (with root privileges or sudo) need to edit /etc/security/limits.conf.
> Change username to your actual username. Once the file is edited, reboot for the changes to take effect, and verify by running `ulimit -Hn` to see the new limit (524288).
> 
> ```c
> username hard nofile 524288
> ```
---

<i>Dotfiles should be added to their respective locations according to the framework of the distribution.  This installation guide assumes the user is on Arch Linux or a fork of it so [refer to the wiki](https://wiki.archlinux.org/) for details concerning each application.</i>

<br>

![GitHub Logo](/screenshot.png)

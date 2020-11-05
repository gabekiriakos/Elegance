# Elegance <img width="25" height="25" src="/logo.png">

<i>A clean and lightweight theme with minimal transparency for i3-gaps.</i>

---

<b>Overview:</b>
* Distro: [Artix](https://artixlinux.org/)
* Init: [runit](https://en.wikipedia.org/wiki/Runit)
* WM: [i3-gaps](https://github.com/Airblader/i3)
* Status: [py3status](https://github.com/ultrabug/py3status)
* Compositor: [picom](https://github.com/yshui/picom)
* Terminal: [Terminator](https://terminator-gtk3.readthedocs.io/en/latest/)
* Menu: [Rofi](https://github.com/davatorium/rofi)

<br>

<b>Noteable Features:</b>
* System Menu: <i>super+e</i>
* Programs Menu: <i>super+d</i>
* Screenshot (requires Scrot): <i>super+p</i>
* Toggle Window Floating: <i>super+w</i>
* Toggle Workspaces: <i>alt+tab</i>
* Exit Active Window: <i>ctrl+q</i>
* Passthrough Mode (lock all bindings): <i>super+q</i> <br>

Refer to i3 config for all other features and key bindings.

---
<b>Dependencies:</b>

<details>
<summary>
<b>Official Repository</b>
</summary>
<i>xorg (all), i3 (gaps, status, lock), py3status, python-pydbus, rofi, dunst, picom, lightdm, lightdm-gtk-greeter, git, terminator, networkmanager, network-manager-applet, udisks2, udiskie, ntfs-3g, reflector, nitrogen, gimp, firefox, vlc, ranger, pcmanfm, noto-fonts, noto-fonts-extra, noto-fonts-cjk, noto-fonts-emoji, ttf-font-awesome, nvidia, lib32-nvidia-utils (multilib), steam (multilib), lutris (multilib) wine (multilib), htop, grub-customizer, lxappearance, neofetch, powerline, pulseaudio, pavucontrol, fcitx (all), fcitx-configtool, fcitx-mozc, gtk-engines, gtk-engine-murrine, gnome-themes-extra, baobab, file-roller, bluez, bluez-utils, blueman, papyrus-icon-theme, pasystray</i>
</details>

<details>
<summary>
<b>AUR</b>
</summary>
<i>yay, flat-remix-gtk, ttf-monaco, gotop, fcitx-skin-material, downgrade</i>
</details>

---

<b>Note:</b><br>
MPRIS is used to display player status in py3status.  [python-pydbus](https://www.archlinux.org/packages/community/any/python-pydbus/) is the only required dependency.

dbus most likely needs to be wrapped in the session to work properly<br> 
(in this case, lightdm -> /etc/lightdm/XSession):

```bash
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

Dotfiles should be added to their respective locations according to the framework of the distribution.  Although these configurations could work within another distro running the same init system, it is assumed the user is on Artix or something close to Arch so [refer to the wiki](https://wiki.archlinux.org/) for details concerning each application.<br>

<b>Disclaimer:</b><br>
<i>It should go without saying that I am not responsible for anything YOU did to YOUR system.  This distro is targeted for power users willing to invest in the time and patience to build their own environment.</i>

![screenshot](/screenshot.png)

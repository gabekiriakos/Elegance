# Artix_Backup
Dotfiles in case a reinstallation is necessary

---

A clean and lightweight theme with minimal transparency for i3-gaps.

<br>

<b>Overview:</b>
* OS: [Artix](https://www.archlinux.org/)
* WM: [i3-gaps](https://github.com/Airblader/i3)
* Status: [py3status](https://github.com/ultrabug/py3status)
* Compositor: [Picom](https://github.com/yshui/picom)
* Terminal: [Termite](https://terminator-gtk3.readthedocs.io/en/latest/)
* Menu: [Rofi](https://github.com/davatorium/rofi)

<br>

<b>Features:</b>
* System Menu (Shutdown, Suspend, etc.): `$mod+e`
* Screenshot (via Scrot): `$mod+p`
* Toggle Window Floating: `$mod+w`
* Seamlessly Switch Workspaces: `Mod1+tab`
* Exit Active Window: `Control+q`
* Rofi Menu: `$mod+d`<br>
<i>Simple drop-down menu with minimal transparency.  Place `custom.rasi` in `/usr/share/rofi/themes/`. Enable by using config files or with `rofi-theme-selector`.</i>

User can modify these features and more in the i3 config.

---

<b>Official Repository Apps:</b><br>
<i>xorg (all), i3 (gaps, status, lock), py3status, python-pydbus, rofi, dunst, picom, lightdm, lightdm-gtk-greeter, git, terminator, networkmanager, network-manager-applet, udisks2, udiskie, ntfs-3g, reflector, nitrogen, gimp, firefox, vlc, ranger, pcmanfm, noto-fonts, noto-fonts-extra, noto-fonts-cjk, noto-fonts-emoji, ttf-font-awesome, nvidia, lib32-nvidia-utils (multilib), steam (multilib), wine (multilib), htop, grub-customizer, lxappearance, neofetch, powerline, pulseaudio, pavucontrol, fcitx (all), fcitx-configtool, fcitx-mozc, gtk-engines, gtk-engine-murrine, gnome-themes-extra, baobab, bluez, bluez-utils, blueman</i>

<b>AUR Apps:</b><br>
<i>yay, ttf-monaco, gotop, fcitx-skin-material</i>

---

<b>IMPORTANT:</b><br>
The custom `i3status.conf` needs to be placed in `/etc/` in order for py3status to work after it is installed.

MPRIS is used to display player status in py3status.  [python-pydbus](https://www.archlinux.org/packages/community/any/python-pydbus/) is the only required dependency.

---

<b>Suggestions:</b><br>
Dotfiles should be added to their respective locations according to the framework of the distribution.  This installation guide assumes the user is on Arch Linux or a fork of it so refer to the [wiki page](https://wiki.archlinux.org/) for details concerning each application.

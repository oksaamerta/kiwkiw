---
layout: post
slug: Install Dan Konfigurasi i3-wm ArchLinux
---

konfigurasi i3 windows manager simple, versi saya, kalau mau bagus bagus mending pake KDE puh sepuh ^_^


install driver VGA, disini saya memakai RX 580 8Gb GDDR5

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/i3.png" />

```
[tama@tamagochi ~]$ sudo pacman -S xf86-video-amdgpu mesa
warning: mesa-1:23.2.1-2 is up to date -- reinstalling
resolving dependencies...
looking for conflicting packages...

Packages (2) mesa-1:23.2.1-2  xf86-video-amdgpu-23.0.0-1

Total Download Size:    0,07 MiB
Total Installed Size:  93,17 MiB
Net Upgrade Size:       0,16 MiB

:: Proceed with installation? [Y/n] 
:: Retrieving packages...
 xf86-video-amdgp...    69,4 KiB  52,9 KiB/s 00:01 [######################] 100%
(2/2) checking keys in keyring                     [######################] 100%
(2/2) checking package integrity                   [######################] 100%
(2/2) loading package files                        [######################] 100%
(2/2) checking for file conflicts                  [######################] 100%
:: Processing package changes...
(1/2) reinstalling mesa                            [######################] 100%
(2/2) installing xf86-video-amdgpu                 [######################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
```

install graphical environment

>Xorg (juga disebut X.Org) merupakan implementasi perangkat lunak bebas dan sumber terbuka yang digunakan sebagai peladen layar sistem penjendelaan X11 (X Window System) yang dirilis oleh Yayasan X.Org.

```
[tama@tamagochi ~]$ sudo pacman -S xorg-server xorg-apps xorg-xinit
warning: xorg-server-21.1.9-1 is up to date -- reinstalling
:: There are 36 members in group xorg-apps:
:: Repository extra
   1) xorg-bdftopcf  2) xorg-iceauth  3) xorg-mkfontscale  4) xorg-sessreg  5) xorg-setxkbmap  6) xorg-smproxy
   7) xorg-x11perf  8) xorg-xauth  9) xorg-xbacklight  10) xorg-xcmsdb  11) xorg-xcursorgen  12) xorg-xdpyinfo
   13) xorg-xdriinfo  14) xorg-xev  15) xorg-xgamma  16) xorg-xhost  17) xorg-xinput  18) xorg-xkbcomp
   19) xorg-xkbevd  20) xorg-xkbprint  21) xorg-xkbutils  22) xorg-xkill  23) xorg-xlsatoms  24) xorg-xlsclients
   25) xorg-xmodmap  26) xorg-xpr  27) xorg-xprop  28) xorg-xrandr  29) xorg-xrdb  30) xorg-xrefresh  31) xorg-xset
   32) xorg-xsetroot  33) xorg-xvinfo  34) xorg-xwd  35) xorg-xwininfo  36) xorg-xwud

Enter a selection (default=all): 
warning: xorg-bdftopcf-1.1.1-1 is up to date -- reinstalling
warning: xorg-iceauth-1.0.9-1 is up to date -- reinstalling
warning: xorg-mkfontscale-1.2.2-1 is up to date -- reinstalling
warning: xorg-sessreg-1.1.3-1 is up to date -- reinstalling
warning: xorg-setxkbmap-1.3.4-1 is up to date -- reinstalling
warning: xorg-smproxy-1.0.7-1 is up to date -- reinstalling
warning: xorg-x11perf-1.6.2-1 is up to date -- reinstalling
warning: xorg-xauth-1.1.2-1 is up to date -- reinstalling
warning: xorg-xbacklight-1.2.3-3 is up to date -- reinstalling
warning: xorg-xcmsdb-1.0.6-1 is up to date -- reinstalling
warning: xorg-xcursorgen-1.0.8-1 is up to date -- reinstalling
warning: xorg-xdpyinfo-1.3.4-1 is up to date -- reinstalling
warning: xorg-xdriinfo-1.0.7-1 is up to date -- reinstalling
warning: xorg-xev-1.2.5-1 is up to date -- reinstalling
warning: xorg-xgamma-1.0.7-1 is up to date -- reinstalling
warning: xorg-xhost-1.0.9-1 is up to date -- reinstalling
warning: xorg-xinput-1.6.4-1 is up to date -- reinstalling
warning: xorg-xkbcomp-1.4.6-1 is up to date -- reinstalling
warning: xorg-xkbevd-1.1.5-1 is up to date -- reinstalling
warning: xorg-xkbutils-1.0.5-1 is up to date -- reinstalling
warning: xorg-xkill-1.0.6-1 is up to date -- reinstalling
warning: xorg-xlsatoms-1.1.4-1 is up to date -- reinstalling
warning: xorg-xlsclients-1.1.5-1 is up to date -- reinstalling
warning: xorg-xmodmap-1.0.11-1 is up to date -- reinstalling
warning: xorg-xpr-1.1.0-1 is up to date -- reinstalling
warning: xorg-xprop-1.2.6-1 is up to date -- reinstalling
warning: xorg-xrandr-1.5.2-1 is up to date -- reinstalling
warning: xorg-xrdb-1.2.2-1 is up to date -- reinstalling
warning: xorg-xrefresh-1.0.7-1 is up to date -- reinstalling
warning: xorg-xset-1.2.5-1 is up to date -- reinstalling
warning: xorg-xsetroot-1.1.3-1 is up to date -- reinstalling
warning: xorg-xvinfo-1.1.5-1 is up to date -- reinstalling
warning: xorg-xwd-1.0.9-1 is up to date -- reinstalling
warning: xorg-xwininfo-1.1.6-1 is up to date -- reinstalling
warning: xorg-xwud-1.0.6-1 is up to date -- reinstalling
warning: xorg-xinit-1.4.2-1 is up to date -- reinstalling
resolving dependencies...
looking for conflicting packages...

Packages (38) xorg-bdftopcf-1.1.1-1  xorg-iceauth-1.0.9-1  xorg-mkfontscale-1.2.2-1  xorg-server-21.1.9-1
              xorg-sessreg-1.1.3-1  xorg-setxkbmap-1.3.4-1  xorg-smproxy-1.0.7-1  xorg-x11perf-1.6.2-1
              xorg-xauth-1.1.2-1  xorg-xbacklight-1.2.3-3  xorg-xcmsdb-1.0.6-1  xorg-xcursorgen-1.0.8-1
              xorg-xdpyinfo-1.3.4-1  xorg-xdriinfo-1.0.7-1  xorg-xev-1.2.5-1  xorg-xgamma-1.0.7-1
              xorg-xhost-1.0.9-1  xorg-xinit-1.4.2-1  xorg-xinput-1.6.4-1  xorg-xkbcomp-1.4.6-1
              xorg-xkbevd-1.1.5-1  xorg-xkbprint-1.0.6-1  xorg-xkbutils-1.0.5-1  xorg-xkill-1.0.6-1
              xorg-xlsatoms-1.1.4-1  xorg-xlsclients-1.1.5-1  xorg-xmodmap-1.0.11-1  xorg-xpr-1.1.0-1
              xorg-xprop-1.2.6-1  xorg-xrandr-1.5.2-1  xorg-xrdb-1.2.2-1  xorg-xrefresh-1.0.7-1  xorg-xset-1.2.5-1
              xorg-xsetroot-1.1.3-1  xorg-xvinfo-1.1.5-1  xorg-xwd-1.0.9-1  xorg-xwininfo-1.1.6-1
              xorg-xwud-1.0.6-1

Total Download Size:   0,75 MiB
Total Installed Size:  5,45 MiB
Net Upgrade Size:      0,09 MiB

:: Proceed with installation? [Y/n] 
:: Retrieving packages...
 xorg-xpr-1.1.0-1-x86_64                   29,1 KiB  30,9 KiB/s 00:01 [#######################################] 100%
 xorg-x11perf-1.6.2-1-x86_64               66,3 KiB  57,7 KiB/s 00:01 [#######################################] 100%
 xorg-xrandr-1.5.2-1-x86_64                36,5 KiB  31,4 KiB/s 00:01 [#######################################] 100%
 xorg-xkbprint-1.0.6-1-x86_64              44,3 KiB  35,6 KiB/s 00:01 [#######################################] 100%
 xorg-xkbcomp-1.4.6-1-x86_64               89,9 KiB  65,2 KiB/s 00:01 [#######################################] 100%
 xorg-xinput-1.6.4-1-x86_64                28,2 KiB  86,4 KiB/s 00:00 [#######################################] 100%
 xorg-xprop-1.2.6-1-x86_64                 25,4 KiB  71,3 KiB/s 00:00 [#######################################] 100%
 xorg-xauth-1.1.2-1-x86_64                 24,5 KiB  79,9 KiB/s 00:00 [#######################################] 100%
 xorg-bdftopcf-1.1.1-1-x86_64              23,5 KiB  72,6 KiB/s 00:00 [#######################################] 100%
 xorg-xwininfo-1.1.6-1-x86_64              23,2 KiB  74,1 KiB/s 00:00 [#######################################] 100%
 xorg-mkfontscale-1.2.2-1-x86_64           23,1 KiB  67,8 KiB/s 00:00 [#######################################] 100%
 xorg-xmodmap-1.0.11-1-x86_64              22,1 KiB  84,2 KiB/s 00:00 [#######################################] 100%
 xorg-xrdb-1.2.2-1-x86_64                  20,2 KiB  63,3 KiB/s 00:00 [#######################################] 100%
 xorg-xset-1.2.5-1-x86_64                  19,1 KiB  62,1 KiB/s 00:00 [#######################################] 100%
 xorg-xkbutils-1.0.5-1-x86_64              19,0 KiB  63,4 KiB/s 00:00 [#######################################] 100%
 xorg-xkbevd-1.1.5-1-x86_64                18,0 KiB  63,0 KiB/s 00:00 [#######################################] 100%
 xorg-xwd-1.0.9-1-x86_64                   17,5 KiB  56,3 KiB/s 00:00 [#######################################] 100%
 xorg-xinit-1.4.2-1-x86_64                 17,2 KiB  48,7 KiB/s 00:00 [#######################################] 100%
 xorg-iceauth-1.0.9-1-x86_64               17,0 KiB  56,7 KiB/s 00:00 [#######################################] 100%
 xorg-xcmsdb-1.0.6-1-x86_64                16,7 KiB  47,6 KiB/s 00:00 [#######################################] 100%
 xorg-xdpyinfo-1.3.4-1-x86_64              16,2 KiB  55,7 KiB/s 00:00 [#######################################] 100%
 xorg-xwud-1.0.6-1-x86_64                  16,0 KiB  68,8 KiB/s 00:00 [#######################################] 100%
 xorg-xev-1.2.5-1-x86_64                   15,2 KiB  43,8 KiB/s 00:00 [#######################################] 100%
 xorg-setxkbmap-1.3.4-1-x86_64             14,0 KiB  41,6 KiB/s 00:00 [#######################################] 100%
 xorg-smproxy-1.0.7-1-x86_64               12,6 KiB  37,1 KiB/s 00:00 [#######################################] 100%
 xorg-xhost-1.0.9-1-x86_64                 12,0 KiB  36,1 KiB/s 00:00 [#######################################] 100%
 xorg-xsetroot-1.1.3-1-x86_64              11,3 KiB  43,3 KiB/s 00:00 [#######################################] 100%
 xorg-xlsclients-1.1.5-1-x86_64            10,1 KiB  32,3 KiB/s 00:00 [#######################################] 100%
 xorg-xcursorgen-1.0.8-1-x86_64             9,4 KiB  36,6 KiB/s 00:00 [#######################################] 100%
 xorg-xkill-1.0.6-1-x86_64                  9,2 KiB  29,2 KiB/s 00:00 [#######################################] 100%
 xorg-sessreg-1.1.3-1-x86_64                8,9 KiB  31,2 KiB/s 00:00 [#######################################] 100%
 xorg-xrefresh-1.0.7-1-x86_64               8,7 KiB  22,6 KiB/s 00:00 [#######################################] 100%
 xorg-xgamma-1.0.7-1-x86_64                 8,6 KiB  29,4 KiB/s 00:00 [#######################################] 100%
 xorg-xbacklight-1.2.3-3-x86_64             8,5 KiB  34,7 KiB/s 00:00 [#######################################] 100%
 xorg-xvinfo-1.1.5-1-x86_64                 8,4 KiB  23,8 KiB/s 00:00 [#######################################] 100%
 xorg-xlsatoms-1.1.4-1-x86_64               8,0 KiB  28,7 KiB/s 00:00 [#######################################] 100%
 xorg-xdriinfo-1.0.7-1-x86_64               6,8 KiB  22,5 KiB/s 00:00 [#######################################] 100%
 Total (37/37)                            764,8 KiB   137 KiB/s 00:06 [#######################################] 100%
(38/38) checking keys in keyring                                      [#######################################] 100%
(38/38) checking package integrity                                    [#######################################] 100%
(38/38) loading package files                                         [#######################################] 100%
(38/38) checking for file conflicts                                   [#######################################] 100%
:: Processing package changes...
( 1/38) reinstalling xorg-setxkbmap                                   [#######################################] 100%
( 2/38) reinstalling xorg-xkbcomp                                     [#######################################] 100%
( 3/38) reinstalling xorg-server                                      [#######################################] 100%
( 4/38) reinstalling xorg-bdftopcf                                    [#######################################] 100%
( 5/38) reinstalling xorg-iceauth                                     [#######################################] 100%
( 6/38) reinstalling xorg-mkfontscale                                 [#######################################] 100%
( 7/38) reinstalling xorg-sessreg                                     [#######################################] 100%
( 8/38) reinstalling xorg-smproxy                                     [#######################################] 100%
( 9/38) reinstalling xorg-x11perf                                     [#######################################] 100%
(10/38) reinstalling xorg-xauth                                       [#######################################] 100%
(11/38) reinstalling xorg-xbacklight                                  [#######################################] 100%
(12/38) reinstalling xorg-xcmsdb                                      [#######################################] 100%
(13/38) reinstalling xorg-xcursorgen                                  [#######################################] 100%
(14/38) reinstalling xorg-xdpyinfo                                    [#######################################] 100%
(15/38) reinstalling xorg-xdriinfo                                    [#######################################] 100%
(16/38) reinstalling xorg-xev                                         [#######################################] 100%
(17/38) reinstalling xorg-xgamma                                      [#######################################] 100%
(18/38) reinstalling xorg-xhost                                       [#######################################] 100%
(19/38) reinstalling xorg-xrandr                                      [#######################################] 100%
(20/38) reinstalling xorg-xinput                                      [#######################################] 100%
(21/38) reinstalling xorg-xkbevd                                      [#######################################] 100%
(22/38) installing xorg-xkbprint                                      [#######################################] 100%
(23/38) reinstalling xorg-xkbutils                                    [#######################################] 100%
(24/38) reinstalling xorg-xkill                                       [#######################################] 100%
(25/38) reinstalling xorg-xlsatoms                                    [#######################################] 100%
(26/38) reinstalling xorg-xlsclients                                  [#######################################] 100%
(27/38) reinstalling xorg-xmodmap                                     [#######################################] 100%
(28/38) reinstalling xorg-xpr                                         [#######################################] 100%
(29/38) reinstalling xorg-xprop                                       [#######################################] 100%
(30/38) reinstalling xorg-xrdb                                        [#######################################] 100%
(31/38) reinstalling xorg-xrefresh                                    [#######################################] 100%
(32/38) reinstalling xorg-xset                                        [#######################################] 100%
(33/38) reinstalling xorg-xsetroot                                    [#######################################] 100%
(34/38) reinstalling xorg-xvinfo                                      [#######################################] 100%
(35/38) reinstalling xorg-xwd                                         [#######################################] 100%
(36/38) reinstalling xorg-xwininfo                                    [#######################################] 100%
(37/38) reinstalling xorg-xwud                                        [#######################################] 100%
(38/38) reinstalling xorg-xinit                                       [#######################################] 100%
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
```


install i3-wm dan package kebutuhan lainnya, sesuaikan saja, kalau saya pake default aja

```
[tama@tamagochi ~]$ sudo pacman -S i3-wm i3-gaps i3blocks i3lock numlockx dmenu i3status nitrogen
```


install tema

```
[tama@tamagochi ~]$ sudo pacman -S arc-gtk-theme papirus-icon-theme lxapperance

```


applet tambahan

```
yay -S pa-applet-git
```

config simple untuk i3bar "~/.config/i3/i3config"

```
bar {
        status_command i3status
	position top
	i3bar_command i3bar --transparency
colors {
background #26323888
statusline #eceff1ff
separator #cfd8dcff
     
# colors                outline    background   number
focused_workspace #4c7899 #285577 #ffffff
active_workspace #333333 #5f676a #ffffff
inactive_workspace #333333 #222222 #888888
urgent_workspace #2f343a #900000 #ffffff
binding_mode #2f343a #900000 #ffffff
}
}
```

tambahan config untuk audio pada applet "/etc/i3status.conf", jangan lupa sesuaikan deviceNya

```
volume master {
        format = "♪: %volume"
        format_muted = "♪: muted (%volume)"
        device = "pulse:alsa_output.pci-0000_00_1f.3.analog-stereo"
}
```

done.

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/i31.png" />


<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/i33.png" />



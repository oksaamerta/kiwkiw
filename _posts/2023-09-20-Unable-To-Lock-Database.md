---
layout: post
slug: Root cause of "unable to lock database" issue
---


#### Root cause of "unable to lock database" issue

```
[tama@tamaoksa ~]$ sudo pacman -Syu
:: Synchronizing package databases...
error: failed to synchronize all databases (unable to lock database)
```



cara fix

```
[tama@tamaoksa ~]$ sudo rm /var/lib/pacman/db.lck
[tama@tamaoksa ~]$ sudo pacman -Syu
:: Synchronizing package databases...
 core                  127,6 KiB  65,3 KiB/s 00:02 [######################] 100%
 extra                   8,2 MiB  1652 KiB/s 00:05 [######################] 100%
 multilib              141,5 KiB  76,6 KiB/s 00:02 [######################] 100%
:: Starting full system upgrade...
resolving dependencies...
looking for conflicting packages...

Packages (33) archlinux-keyring-20230918-1  at-spi2-core-2.50.0-1
              bind-9.18.19-1  ffmpeg-2:6.0-11  glib-networking-1:2.78.0-1
              gvfs-1.52.0-1  harfbuzz-8.2.1-1  lib32-harfbuzz-8.2.1-1
              lib32-openssl-1:3.1.3-1  lib32-p11-kit-0.25.0-2
              libblockdev-3.0.3-4  libcups-1:2.4.7-1  libdeflate-1.19-1
              libdovi-3.2.0-2  libnvme-1.5-1  libp11-kit-0.25.0-2
              libplacebo-5.264.1-4  libsoup3-3.4.3-1  licenses-20230917-1
              lua-5.4.6-2  lua52-5.2.4-6  onevpl-2023.3.1-1  p11-kit-0.25.0-2
              procps-ng-4.0.4-2  python-typing_extensions-4.8.0-1
              tracker3-3.6.0-1  udisks2-2.10.1-1  vlc-3.0.18-16
              vte-common-0.74.0-1  vte3-0.74.0-1  wine-8.16-1
              xfce4-notifyd-0.9.1-1  xorg-xwayland-23.2.1-1

Total Download Size:   104,94 MiB
Total Installed Size:  684,32 MiB
Net Upgrade Size:        9,91 MiB

:: Proceed with installation? [Y/n] 
:: Retrieving packages...
```

Sekian.
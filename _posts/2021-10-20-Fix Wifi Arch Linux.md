---
layout: post
slug: Troubleshooting Wifi Arch Linux
---



#### Fix Wifi Icon Arch Linux de:XFCE4

banyak error, pantes gaboleh install debian based


installasi wifi dan icon wifi pada xfce4

```
~:sudo pacman -S networkmanager network-manager-applet xfce4-notifyd gnome-keyring
```



aktifkan servicenya & start service

```
~:systemctl enable NetworkManager.service
~:systemctl start NetworkManager.service
```


reboot system kembali, done

Note: Jika masih belum fix juga, coba install driver "broadcom-wl", sekian.

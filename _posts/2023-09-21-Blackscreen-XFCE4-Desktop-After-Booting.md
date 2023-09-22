---
layout: post
slug: Blank WM XFCE4 ArchLinux After Booting
---


setelah booting, berhasil sampe ke WM, namun hilang blank black scree, hanya tinggal panel saja. Setelah menyelam di forum akhirnya ketemu cara unutk memperbaiki, versi saya.


<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/black-screen-wm.png" />


#### cara saya memberbaiki

coba update

```
[tama@tamaoksa ~]$ sudo pacman -Syu
```



coba ngikut cara di forum

```
[tama@tamaoksa ~]$ xfdesktop --replace
```

bisa, tapi hanya sementara, setelah reboot balik black screen



tetep gabisa fix setelah reboot, lalu saya coba untuk hapus file log

```
[tama@tamaoksa ~]$ rm -rf /var/log/sessions
```

reboot, done <3
---
layout: post
slug: Troubleshooting Android File Transfer, Backup Data Arch Linux 
---


#### konteks

Ceritanya ingin membackup semua file yang ada di smartphone lama saya yang sudah jarang pakai, namun ada sedikit masalah ketika ingin membackup data, karena pake metode usb juga mengalami error, berikut output file ketika menggunakan cara sambungan langsung menggunakan USB




#### file transfer android menggunakan sambungan USB secara langsung




```
[tama@tamaoksa ~]$ sudo pacman -S android-file-transfer android-udev jmtpfs mtpfs gmtp gvfs-mtp gvfs-photo2 libmtp
```




coba run

```
[tama@tamaoksa ~]$ aft-mtp-cli
selected storage 65537  Penyimpanan internal bersama
android file transfer for linux version v4.2-snapshot
INFINIX Infinix X6817 1.0
extensions: microsoft.com: 1.0; android.com: 1.0;
```




sebenernya bisa pake jalur USB, tapi kok CLI, kurang srek kalo tampilang tidak GUI

```
[tama@tamaoksa ~]$ aft-mtp-cli
selected storage 65537  Penyimpanan internal bersama
android file transfer for linux version v4.2-snapshot
[MEREKHP] [Merekhp] [Seri] 1.0
extensions: microsoft.com: 1.0; android.com: 1.0;
[MEREKHP] [Merekhp] [Seri] / [MEREKHP] [Merekhp] [Seri] [51%]:Penyimpanan internal bersama> 

[MEREKHP] [Merekhp] [Seri] / [MEREKHP] [Merekhp] [Seri] [51%]:Penyimpanan internal bersama> ls
7          Pictures
15         MyAlbums
29         .SHAREit
19         epsxe
18         Subtitles
8          Movies
9          Download
20         .DataStorage
23         supercache
22         Document Reader
30         .system_config
12         Audiobooks
5          Alarms
33         GCam
24         itubego
25         Fonts
13         Recordings
1          Android
21         Unitube
31         sepolicy_extends
2          Music
11         Documents
3          Podcasts
17         .trashBin
14         PHXBrowser
26         .pmbackup
32         com.android.settings
10         DCIM
16         Collage
6          Notifications
27         .gs_fs0
34         MagicFonts
28         .gs_file
4          Ringtones
```




#### coba transfer lewat FTP pada folder server android FTP

menurutku ini paling cocok, kalo di versi saya, soalnya kalo pake windows tinggal colok doang langsung konek, kalo pake distro archLinux agak kudu ngatur dikit, tapi gapapa soalnya disekolah saya diwajibkan pake archLinux. Distro Ubuntu based keknya juga tinggal colok bisa dah perasaan, archLinux passwordNya "Mana sempat keburu telat"



```
[tama@tamaoksa ~]$ sudo pacman -S  vsftpd
[sudo] password for tama: 
resolving dependencies...
looking for conflicting packages...

Packages (1) vsftpd-3.0.3-8

Total Download Size:   0,11 MiB
Total Installed Size:  0,26 MiB

:: Proceed with installation? [Y/n] 
:: Retrieving packages...
 vsftpd-3.0.3-8-x...   114,6 KiB   141 KiB/s 00:01 [######################] 100%
(1/1) checking keys in keyring                     [######################] 100%
(1/1) checking package integrity                   [######################] 100%
(1/1) loading package files                        [######################] 100%
(1/1) checking for file conflicts                  [######################] 100%
:: Processing package changes...
(1/1) installing vsftpd                            [######################] 100%
Optional dependencies for vsftpd
    logrotate
:: Running post-transaction hooks...
(1/2) Reloading system manager configuration...
```




aktifin service

```
[tama@tamaoksa ~]$ systemctl start vsftpd.service
```



aktifin ftp service dari android

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/android-ftp2.png" />




konek FTP lewat browser file, kalo di XFCE sudah ada thunar, jadi tinggal ketik url yang udah dibuat dari android FTP tadi lewat browser file network, sebelah kiri bawah

```
ftp://xxx.xxx.xxx.xxx:port
```

Login pakai user dan pass






coba transfer file

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/android-ftp.png" />




Sekian.
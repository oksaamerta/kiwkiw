---
layout: post
slug: Surf Browser Terminal Based
---


udah banyak materi tentang terminal based, sekolah salah jurusan, tapi tetep hepi karena janji kalo naek kelas mau dibeliin mobo-storage-procie baru wkwk.


### Bahan
Download dulu dari sini => https://surf.suckless.org/


setelah di ekstrak

```
[tama@tamaoksa surf-2.1]$ ls
arg.h         config.h   Makefile  surf.c        TODO.md
common.h      config.mk  README    surf-open.sh  webext-surf.c
config.def.h  LICENSE    surf.1    surf.png
```



### Installasi
saat installasi mengalami error

```
[tama@tamaoksa surf-2.1]$ sudo make clean install
[sudo] password for tama: 
rm -f surf surf.o
rm -f webext-surf.so webext-surf.o
surf build options:
CC            = c99
Package webkit2gtk-4.0 was not found in the pkg-config search path.
Perhaps you should add the directory containing `webkit2gtk-4.0.pc'
to the PKG_CONFIG_PATH environment variable
Package 'webkit2gtk-4.0', required by 'virtual:world', not found
CFLAGS        = -fPIC   -DVERSION="2.1" -DGCR_API_SUBJECT_TO_CHANGE  -DLIBPREFIX="/usr/local/lib" -DWEBEXTDIR="/usr/local/lib/surf"  -D_DEFAULT_SOURCE -O1
Package webkit2gtk-4.0 was not found in the pkg-config search path.
Perhaps you should add the directory containing `webkit2gtk-4.0.pc'
to the PKG_CONFIG_PATH environment variable
Package 'webkit2gtk-4.0', required by 'virtual:world', not found
Package 'webkit2gtk-web-extension-4.0', required by 'virtual:world', not found
WEBEXTCFLAGS  = -fPIC  -O1
LDFLAGS       = 
c99 -fPIC `pkg-config --cflags x11` `pkg-config --cflags gtk+-3.0 gcr-3 webkit2gtk-4.0` -DVERSION=\"2.1\" -DGCR_API_SUBJECT_TO_CHANGE  -DLIBPREFIX=\"/usr/local/lib\" -DWEBEXTDIR=\"/usr/local/lib/surf\"  -D_DEFAULT_SOURCE -O1 -c surf.c
Package webkit2gtk-4.0 was not found in the pkg-config search path.
Perhaps you should add the directory containing `webkit2gtk-4.0.pc'
to the PKG_CONFIG_PATH environment variable
Package 'webkit2gtk-4.0', required by 'virtual:world', not found
surf.c:9:10: fatal error: glib.h: No such file or directory
    9 | #include <glib.h>
      |          ^~~~~~~~
compilation terminated.
make: *** [Makefile:31: surf.o] Error 1
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/surf-1.png" />


instal paket yang kurang

```
[tama@tamaoksa webkitgtk-2.42.1]$ sudo pacman -S webkit2gtk
[sudo] password for tama: 
resolving dependencies...
looking for conflicting packages...

Packages (12) enchant-2.6.0-1  gssdp-1.6.2-1  gst-plugins-bad-libs-1.22.6-1
              gupnp-1:1.6.5-1  gupnp-igd-1.6.0-1  harfbuzz-icu-8.2.1-1
              hyphen-2.8.8-5  libmanette-0.2.6-5  libnice-0.1.21-2
              libwpe-1.14.1-2  wpebackend-fdo-1.14.2-1  webkit2gtk-2.42.1-1

Total Download Size:    27,36 MiB
Total Installed Size:  121,71 MiB

:: Proceed with installation? [Y/n] 
:: Retrieving packages...
 enchant-2.6.0-1-...    59,3 KiB   154 KiB/s 00:00 [######################] 100%
 webkit2gtk-2.42....    27,3 MiB  1834 KiB/s 00:15 [######################] 100%
 Total (2/2)            27,4 MiB  1829 KiB/s 00:15 [######################] 100%
(12/12) checking keys in keyring                   [######################] 100%
(12/12) checking package integrity                 [######################] 100%
(12/12) loading package files                      [######################] 100%
(12/12) checking for file conflicts                [######################] 100%
:: Processing package changes...
( 1/12) installing enchant                         [######################] 100%
Optional dependencies for enchant
    aspell: for aspell based spell checking support
    hunspell: for hunspell based spell checking support [installed]
    libvoikko: for libvoikko based spell checking support
    hspell: for hspell based spell checking support
    nuspell: for nuspell based spell checking support
( 2/12) installing gssdp                           [######################] 100%
Optional dependencies for gssdp
    gtk4: gssdp-device-sniffer
( 3/12) installing gupnp                           [######################] 100%
Optional dependencies for gupnp
    python: gupnp-binding-tool [installed]
( 4/12) installing gupnp-igd                       [######################] 100%
( 5/12) installing libnice                         [######################] 100%
Optional dependencies for libnice
    gstreamer: "nice" GStreamer plugin [installed]
( 6/12) installing gst-plugins-bad-libs            [######################] 100%
( 7/12) installing harfbuzz-icu                    [######################] 100%
( 8/12) installing hyphen                          [######################] 100%
( 9/12) installing libmanette                      [######################] 100%
(10/12) installing libwpe                          [######################] 100%
(11/12) installing wpebackend-fdo                  [######################] 100%
(12/12) installing webkit2gtk                      [######################] 100%
Optional dependencies for webkit2gtk
    geoclue: Geolocation support [installed]
    gst-libav: nonfree media decoding
    gst-plugins-bad: media decoding
    gst-plugins-good: media decoding [installed]
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/surf-2.png" />


### Coba run

```
[tama@tamaoksa surf-2.1]$ surf oksaamerta.github.io
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/surf-3.png" />



Sekian.

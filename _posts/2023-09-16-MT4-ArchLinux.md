---
layout: post
slug: MT4 ArchLinux
---


#### sedikit edit sebelum build

sumber : https://wiki.archlinux.org/title/wine


edit file repo

```
/etc/pacman.conf
```

edit bagian


```
[multilib]
Include = /etc/pacman.d/mirrorlist
```

update paket repo

```
tama@tamaoksa ~]$ sudo pacman -Sy
[sudo] password for tama: 
:: Synchronizing package databases...
 core                  127,6 KiB  33,4 KiB/s 00:04 [######################] 100%
 extra                   8,2 MiB   304 KiB/s 00:28 [######################] 100%
 multilib              141,5 KiB  92,2 KiB/s 00:02 [######################] 100%
```


#### cek lib

```
[tama@tamaoksa ~]$ sudo pacman -Sl multilib
multilib cmucl 21d-3
multilib lib32-aalib 1.4rc5-4
multilib lib32-acl 2.3.1-2
multilib lib32-alsa-lib 1.2.10-1
multilib lib32-alsa-oss 1.1.8-4
multilib lib32-alsa-plugins 1.2.7.1-2
multilib lib32-amdvlk 2023.Q3.1-1
multilib lib32-apitrace 11.1-1
multilib lib32-at-spi2-core 2.48.4-1
multilib lib32-attr 2.5.1-1
multilib lib32-brotli 1.0.9-12
multilib lib32-bzip2 1.0.8-3
multilib lib32-cairo 1.17.8-2
multilib lib32-cdparanoia 10.2-4
multilib lib32-clang 16.0.6-1
multilib lib32-cmocka 1.1.7-1
multilib lib32-colord 1.4.6-1
multilib lib32-cracklib 2.9.11-1
multilib lib32-curl 8.3.0-1
multilib lib32-dbus 1.14.10-1
multilib lib32-dbus-glib 0.112-2
multilib lib32-dconf 0.40.0-3
multilib lib32-duktape 2.7.0-6
multilib lib32-e2fsprogs 1.47.0-1
multilib lib32-expat 2.5.0-2
multilib lib32-fakeroot 1.32.1-1
multilib lib32-faudio 23.07-1
multilib lib32-flac 1.4.3-1
multilib lib32-flex 2.6.4-4
multilib lib32-fluidsynth 2.3.3-1
multilib lib32-fontconfig 2:2.14.2-1
multilib lib32-freeglut 3.4.0-1
multilib lib32-freetype2 2.13.2-1
multilib lib32-fribidi 1.0.13-2
multilib lib32-gamemode 1.7-1
multilib lib32-gdk-pixbuf2 2.42.10-2
multilib lib32-gettext 0.21.1-1
multilib lib32-giflib 5.2.1-1
multilib lib32-glew 2.2.0-4
multilib lib32-glew1.10 1.10.0-5
multilib lib32-glib-networking 2.76.1-1
multilib lib32-glib2 2.78.0-2
multilib lib32-glu 9.0.3-1
multilib lib32-gmp 6.2.1-1
multilib lib32-gnutls 3.8.1-1
multilib lib32-gpm 1.20.7.r38.ge82d1a6-1
multilib lib32-gst-plugins-base 1.22.5-1
multilib lib32-gst-plugins-base-libs 1.22.5-1
multilib lib32-gst-plugins-good 1.22.5-1
multilib lib32-gstreamer 1.22.5-1
multilib lib32-gtk2 2.24.33-2
multilib lib32-gtk3 1:3.24.38-1
multilib lib32-harfbuzz 8.2.0-1
multilib lib32-harfbuzz-cairo 8.2.0-1
multilib lib32-harfbuzz-icu 8.2.0-1
multilib lib32-icu 73.2-1
multilib lib32-imlib2 1.12.0-1
multilib lib32-jack2 1.9.22-1
multilib lib32-jansson 2.14-1
multilib lib32-json-c 0.17-1
multilib lib32-json-glib 1.6.6-2
multilib lib32-keyutils 1.6.3-1
multilib lib32-krb5 1.20.1-1
multilib lib32-ladspa 1.17-2
multilib lib32-lcms2 2.15-1
multilib lib32-libaio 0.3.113-2
multilib lib32-libao 1.2.2-4
multilib lib32-libappindicator-gtk2 12.10.0-13
multilib lib32-libappindicator-gtk3 12.10.0-13
multilib lib32-libasyncns 1:0.8+r3+g68cd5af-2
multilib lib32-libavc1394 0.5.4-4
multilib lib32-libavtp 0.2.0-2
multilib lib32-libcaca 0.99.beta20-1
multilib lib32-libcanberra 1:0.30+r2+gc0620e4-2
multilib lib32-libcap 2.69-1
multilib lib32-libcroco 0.6.13-1
multilib lib32-libcups 2.4.6-1
multilib lib32-libcurl-compat 8.3.0-1
multilib lib32-libcurl-gnutls 8.3.0-1
multilib lib32-libdaemon 0.14-8
multilib lib32-libdatrie 0.2.13-2
multilib lib32-libdbusmenu-glib 16.04.0-5
multilib lib32-libdbusmenu-gtk2 16.04.0-5
multilib lib32-libdbusmenu-gtk3 16.04.0-5
multilib lib32-libdecor 0.1.1-1
multilib lib32-libdrm 2.4.116-1
multilib lib32-libdv 1.0.0-8
multilib lib32-libelf 0.189-1
multilib lib32-libepoxy 1.5.10-1
multilib lib32-libevent 2.1.12-3
multilib lib32-libffi 3.4.4-1
multilib lib32-libgcrypt 1.10.2-1
multilib lib32-libgcrypt15 1.5.6-7
multilib lib32-libglvnd 1.6.0-1
multilib lib32-libgpg-error 1.47-1
multilib lib32-libgudev 238-1
multilib lib32-libgusb 0.4.6-1
multilib lib32-libice 1.1.1-1
multilib lib32-libid3tag 0.15.1b-4
multilib lib32-libidn 1.41-1
multilib lib32-libidn11 1.33-2
multilib lib32-libidn2 2.3.4-2
multilib lib32-libiec61883 1.2.0-4
multilib lib32-libindicator-gtk2 12.10.1-9
multilib lib32-libindicator-gtk3 12.10.1-9
multilib lib32-libinstpatch 1.1.6-2
multilib lib32-libjpeg-turbo 3.0.0-1
multilib lib32-libjpeg6-turbo 1.5.3-2
multilib lib32-libldap 2.6.6-1
multilib lib32-libltdl 2.4.7-3
multilib lib32-libmikmod 3.3.11.1-6
multilib lib32-libmodplug 0.8.9.0-4
multilib lib32-libndp 1.8-1
multilib lib32-libnewt 0.52.23-1
multilib lib32-libnghttp2 1.56.0-1
multilib lib32-libnl 3.7.0-1
multilib lib32-libnm 1.44.0-1
multilib lib32-libnsl 2.0.0-2
multilib lib32-libogg 1.3.5-1
multilib lib32-libpcap 1.10.4-1
multilib lib32-libpciaccess 0.17-1
multilib lib32-libpgm 5.3.128-2
multilib lib32-libpipewire 1:0.3.79-1
multilib lib32-libpng 1.6.40-2
multilib lib32-libpng12 1.2.59-2
multilib lib32-libproxy 0.5.3-1
multilib lib32-libpsl 0.21.2-1
multilib lib32-libpulse 16.1-6
multilib lib32-libraw1394 2.1.2-4
multilib lib32-librsvg 2:2.57.0-1
multilib lib32-librtmp0 2.4-5
multilib lib32-libsamplerate 0.2.2-2
multilib lib32-libshout 2.4.6-3
multilib lib32-libsm 1.2.4-1
multilib lib32-libsndfile 1.2.2-1
multilib lib32-libsodium 1.0.18-2
multilib lib32-libsoup 2.74.3-1
multilib lib32-libsoup3 3.4.2-1
multilib lib32-libssh2 1.11.0-1
multilib lib32-libtasn1 4.19.0-1
multilib lib32-libteam 1.31-2
multilib lib32-libthai 0.1.29-2
multilib lib32-libtheora 1.1.1-13
multilib lib32-libtiff 4.6.0-1
multilib lib32-libtiff4 3.9.7-5
multilib lib32-libtirpc 1.3.3-2
multilib lib32-libudev0-shim 1-6
multilib lib32-libunistring 1.1-1
multilib lib32-libunwind 1.6.2-2
multilib lib32-libusb 1.0.26-2
multilib lib32-libva 2.19.0-2
multilib lib32-libva-intel-driver 2.4.1-1
multilib lib32-libva-mesa-driver 1:23.1.7-1
multilib lib32-libva-vdpau-driver 0.7.4-7
multilib lib32-libvdpau 1.5-2
multilib lib32-libvisual 0.4.2-1
multilib lib32-libvorbis 1.3.7-1
multilib lib32-libvpx 1.13.0-1
multilib lib32-libvpx1.3 1.3.0-3
multilib lib32-libwebp 1.3.2-1
multilib lib32-libx11 1.8.6-1
multilib lib32-libxau 1.0.11-1
multilib lib32-libxcb 1.16-1
multilib lib32-libxcomposite 0.4.6-1
multilib lib32-libxcrypt 4.4.36-1
multilib lib32-libxcrypt-compat 4.4.36-1
multilib lib32-libxcursor 1.2.1-2
multilib lib32-libxdamage 1.1.6-1
multilib lib32-libxdmcp 1.1.4-1
multilib lib32-libxext 1.3.5-1
multilib lib32-libxfixes 6.0.1-1
multilib lib32-libxft 2.3.8-1
multilib lib32-libxi 1.8.1-1
multilib lib32-libxinerama 1.1.5-1
multilib lib32-libxkbcommon 1.5.0-1
multilib lib32-libxkbcommon-x11 1.5.0-1
multilib lib32-libxml2 2.11.5-1
multilib lib32-libxmu 1.1.4-1
multilib lib32-libxrandr 1.5.3-1
multilib lib32-libxrender 0.9.11-1
multilib lib32-libxshmfence 1.3.2-1
multilib lib32-libxslt 1.1.38-1
multilib lib32-libxss 1.2.3-3
multilib lib32-libxt 1.3.0-1
multilib lib32-libxtst 1.2.4-1
multilib lib32-libxv 1.0.12-1
multilib lib32-libxvmc 1.0.13-1
multilib lib32-libxxf86vm 1.1.5-1
multilib lib32-llvm 16.0.6-2
multilib lib32-llvm-libs 16.0.6-2
multilib lib32-lm_sensors 1:3.6.0.r41.g31d1f125-2
multilib lib32-lz4 1.9.4-1
multilib lib32-mangohud 0.6.9.1-6
multilib lib32-mesa 1:23.1.7-1
multilib lib32-mesa-amber 21.3.9-5
multilib lib32-mesa-demos 9.0.0-1
multilib lib32-mesa-utils 9.0.0-1
multilib lib32-mesa-vdpau 1:23.1.7-1
multilib lib32-mpg123 1.31.3-1
multilib lib32-ncurses 6.4_20230520-1
multilib lib32-nettle 3.9.1-1
multilib lib32-nspr 4.35-1
multilib lib32-nss 3.93-1
multilib lib32-nvidia-cg-toolkit 3.1-8
multilib lib32-nvidia-utils 535.104.05-1
multilib lib32-ocl-icd 2.3.2-1
multilib lib32-openal 1.23.1-1
multilib lib32-opencl-clover-mesa 1:23.1.7-1
multilib lib32-opencl-nvidia 535.104.05-1
multilib lib32-opencl-rusticl-mesa 1:23.1.7-1
multilib lib32-openssl 1:3.1.2-1
multilib lib32-openssl-1.1 1.1.1.v-1
multilib lib32-opus 1.4-1
multilib lib32-orc 0.4.34-1
multilib lib32-p11-kit 0.25.0-1
multilib lib32-pam 1.5.3-1
multilib lib32-pango 1:1.50.14-1
multilib lib32-pcre 8.45-3
multilib lib32-pcre2 10.42-1
multilib lib32-pcsclite 2.0.0-1
multilib lib32-pipewire 1:0.3.79-1
multilib lib32-pipewire-jack 1:0.3.79-1
multilib lib32-pipewire-v4l2 1:0.3.79-1
multilib lib32-pixman 0.42.2-1
multilib lib32-polkit 123-1
multilib lib32-popt 1.19-1
multilib lib32-portaudio 1:19.7.0-2
multilib lib32-primus 20151110-5
multilib lib32-primus_vk 1.6.2-1
multilib lib32-procps-ng 4.0.4-1
multilib lib32-readline 8.2.001-2
multilib lib32-renderdoc 1.28-1
multilib lib32-rest 0.8.1-4
multilib lib32-sdl12-compat 1.2.64-1
multilib lib32-sdl2 2.28.3-1
multilib lib32-sdl2_image 2.6.3-1
multilib lib32-sdl2_mixer 2.6.3-1
multilib lib32-sdl2_ttf 2.20.2-1
multilib lib32-sdl_image 1.2.12-8
multilib lib32-sdl_mixer 1.2.12-5
multilib lib32-sdl_net 1.2.8-3
multilib lib32-sdl_ttf 2.0.11-8
multilib lib32-slang 2.3.3-1
multilib lib32-smpeg 2.0.0-1
multilib lib32-speex 1.2.1-1
multilib lib32-speexdsp 1.2.1-1
multilib lib32-spirv-llvm-translator 16.0.0.r9+g322fca5d-1
multilib lib32-spirv-tools 2022.4-1
multilib lib32-sqlite 3.43.0-1
multilib lib32-systemd 254.3-1
multilib lib32-taglib 1.13.1-1
multilib lib32-tcl 8.6.13-1
multilib lib32-tdb 1.4.8-1
multilib lib32-twolame 0.4.0-2
multilib lib32-util-linux 2.39.2-1
multilib lib32-v4l-utils 1.24.1-1
multilib lib32-virtualgl 3.1-1
multilib lib32-vkd3d 1.7.1-1
multilib lib32-vulkan-icd-loader 1.3.263-1
multilib lib32-vulkan-intel 1:23.1.7-1
multilib lib32-vulkan-mesa-layers 1:23.1.7-1
multilib lib32-vulkan-radeon 1:23.1.7-1
multilib lib32-vulkan-swrast 1:23.1.7-1
multilib lib32-vulkan-validation-layers 1.3.261.1-1
multilib lib32-vulkan-virtio 1:23.1.7-1
multilib lib32-wavpack 5.6.0-1
multilib lib32-wayland 1.22.0-1
multilib lib32-xcb-util 0.4.1-1
multilib lib32-xcb-util-keysyms 0.4.1-1
multilib lib32-xz 5.4.4-1
multilib lib32-zeromq 4.3.4-2
multilib lib32-zlib 1.3-1
multilib lib32-zstd 1.5.5-1
multilib multilib-devel 1-1
multilib nspluginwrapper 1.4.4-6
multilib steam 1.0.0.78-1
multilib steam-native-runtime 1.0.0.75-3
multilib wine 8.15-1
multilib wine-nine 0.8-4
multilib wine-staging 8.15-1
multilib winetricks 20230212-1
multilib yabridge 5.0.5-1
multilib yabridgectl 5.0.5-1
multilib zsnes 2.0.12-1
```

#### clone dari AUR

```
[tama@tamaoksa ~]$ git clone https://aur.archlinux.org/wine-stable.git
```

build

```
makepkg -si
```

#### install paket yang kurang

```
[tama@tamaoksa ~]$ sudo pacman -S lib32-vulkan-icd-loader
resolving dependencies...
looking for conflicting packages...

Packages (1) lib32-vulkan-icd-loader-1.3.263-1

Total Installed Size:  0,55 MiB

:: Proceed with installation? [Y/n] 
(1/1) checking keys in keyring                     [######################] 100%
(1/1) checking package integrity                   [######################] 100%
(1/1) loading package files                        [######################] 100%
(1/1) checking for file conflicts                  [######################] 100%
:: Processing package changes...
(1/1) installing lib32-vulkan-icd-loader           [######################] 100%
Optional dependencies for lib32-vulkan-icd-loader
    lib32-vulkan-driver: packaged vulkan driver [installed]
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
```

setting dikit

```
[tama@tamaoksa ~]$ WINEPREFIX=~/.wine32 WINEARCH=win32 wineboot
```

coba run

```
[tama@tamaoksa ~]$ winecfg
```

berhasil, sekian.

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/mt4-kiw.png" />


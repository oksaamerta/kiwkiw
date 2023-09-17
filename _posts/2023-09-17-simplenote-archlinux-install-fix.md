---
layout: post
slug: fix install simplenote archlinux
---


#### clone paket dari AUR

```
[tama@tamaoksa Downloads]$ git clone  https://aur.archlinux.org/simplenote-electron-bin.git
Cloning into 'simplenote-electron-bin'...
remote: Enumerating objects: 294, done.
remote: Counting objects: 100% (294/294), done.
remote: Compressing objects: 100% (190/190), done.
remote: Total 294 (delta 104), reused 294 (delta 104), pack-reused 0
Receiving objects: 100% (294/294), 61.15 KiB | 219.00 KiB/s, done.
Resolving deltas: 100% (104/104), done.
```


#### masuk dir, lalu build

```
[tama@tamaoksa Downloads]$ cd simplenote-electron-bin
[tama@tamaoksa simplenote-electron-bin]$ ls
PKGBUILD
```

#### build

```
[tama@tamaoksa simplenote-electron-bin]$ makepkg -si
```

output :

```
==> Making package: simplenote-electron-bin 2.21.0-1 (Min 17 Sep 2023 07:33:05 )
==> Checking runtime dependencies...
==> Checking buildtime dependencies...
==> Retrieving sources...
  -> Downloading Simplenote-linux-2.21.0-amd64.deb...
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
  0     0    0     0    0     0      0      0 --:--:-- --:--:-- --:--:--     0
100  103M  100  103M    0     0  1997k      0  0:00:53  0:00:53 --:--:-- 2636k
==> Validating source_x86_64 files with sha256sums...
    Simplenote-linux-2.21.0-amd64.deb ... Passed
==> Extracting sources...
  -> Extracting Simplenote-linux-2.21.0-amd64.deb with bsdtar
==> Entering fakeroot environment...
==> Starting package()...
x ./
x ./opt/
x ./opt/Simplenote/
x ./opt/Simplenote/LICENSE.electron.txt
x ./opt/Simplenote/LICENSES.chromium.html
x ./opt/Simplenote/chrome-sandbox
x ./opt/Simplenote/chrome_100_percent.pak
x ./opt/Simplenote/chrome_200_percent.pak
x ./opt/Simplenote/icudtl.dat
x ./opt/Simplenote/libEGL.so
x ./opt/Simplenote/libGLESv2.so
x ./opt/Simplenote/libffmpeg.so
x ./opt/Simplenote/libvk_swiftshader.so
x ./opt/Simplenote/libvulkan.so.1
x ./opt/Simplenote/locales/
x ./opt/Simplenote/locales/am.pak
x ./opt/Simplenote/locales/ar.pak
x ./opt/Simplenote/locales/bg.pak
x ./opt/Simplenote/locales/bn.pak
x ./opt/Simplenote/locales/ca.pak
x ./opt/Simplenote/locales/cs.pak
x ./opt/Simplenote/locales/da.pak
x ./opt/Simplenote/locales/de.pak
x ./opt/Simplenote/locales/el.pak
x ./opt/Simplenote/locales/en-GB.pak
x ./opt/Simplenote/locales/en-US.pak
x ./opt/Simplenote/locales/es-419.pak
x ./opt/Simplenote/locales/es.pak
x ./opt/Simplenote/locales/et.pak
x ./opt/Simplenote/locales/fa.pak
x ./opt/Simplenote/locales/fi.pak
x ./opt/Simplenote/locales/fil.pak
x ./opt/Simplenote/locales/fr.pak
x ./opt/Simplenote/locales/gu.pak
x ./opt/Simplenote/locales/he.pak
x ./opt/Simplenote/locales/hi.pak
x ./opt/Simplenote/locales/hr.pak
x ./opt/Simplenote/locales/hu.pak
x ./opt/Simplenote/locales/id.pak
x ./opt/Simplenote/locales/it.pak
x ./opt/Simplenote/locales/ja.pak
x ./opt/Simplenote/locales/kn.pak
x ./opt/Simplenote/locales/ko.pak
x ./opt/Simplenote/locales/lt.pak
x ./opt/Simplenote/locales/lv.pak
x ./opt/Simplenote/locales/ml.pak
x ./opt/Simplenote/locales/mr.pak
x ./opt/Simplenote/locales/ms.pak
x ./opt/Simplenote/locales/nb.pak
x ./opt/Simplenote/locales/nl.pak
x ./opt/Simplenote/locales/pl.pak
x ./opt/Simplenote/locales/pt-BR.pak
x ./opt/Simplenote/locales/pt-PT.pak
x ./opt/Simplenote/locales/ro.pak
x ./opt/Simplenote/locales/ru.pak
x ./opt/Simplenote/locales/sk.pak
x ./opt/Simplenote/locales/sl.pak
x ./opt/Simplenote/locales/sr.pak
x ./opt/Simplenote/locales/sv.pak
x ./opt/Simplenote/locales/sw.pak
x ./opt/Simplenote/locales/ta.pak
x ./opt/Simplenote/locales/te.pak
x ./opt/Simplenote/locales/th.pak
x ./opt/Simplenote/locales/tr.pak
x ./opt/Simplenote/locales/uk.pak
x ./opt/Simplenote/locales/vi.pak
x ./opt/Simplenote/locales/zh-CN.pak
x ./opt/Simplenote/locales/zh-TW.pak
x ./opt/Simplenote/resources/
x ./opt/Simplenote/resources/app.asar
x ./opt/Simplenote/resources.pak
x ./opt/Simplenote/simplenote
x ./opt/Simplenote/snapshot_blob.bin
x ./opt/Simplenote/swiftshader/
x ./opt/Simplenote/swiftshader/libEGL.so
x ./opt/Simplenote/swiftshader/libGLESv2.so
x ./opt/Simplenote/v8_context_snapshot.bin
x ./opt/Simplenote/vk_swiftshader_icd.json
x ./usr/
x ./usr/share/
x ./usr/share/icons/
x ./usr/share/icons/hicolor/
x ./usr/share/icons/hicolor/16x16/
x ./usr/share/icons/hicolor/16x16/apps/
x ./usr/share/icons/hicolor/16x16/apps/simplenote.png
x ./usr/share/icons/hicolor/32x32/
x ./usr/share/icons/hicolor/32x32/apps/
x ./usr/share/icons/hicolor/32x32/apps/simplenote.png
x ./usr/share/icons/hicolor/48x48/
x ./usr/share/icons/hicolor/48x48/apps/
x ./usr/share/icons/hicolor/48x48/apps/simplenote.png
x ./usr/share/icons/hicolor/64x64/
x ./usr/share/icons/hicolor/64x64/apps/
x ./usr/share/icons/hicolor/64x64/apps/simplenote.png
x ./usr/share/icons/hicolor/128x128/
x ./usr/share/icons/hicolor/128x128/apps/
x ./usr/share/icons/hicolor/128x128/apps/simplenote.png
x ./usr/share/icons/hicolor/256x256/
x ./usr/share/icons/hicolor/256x256/apps/
x ./usr/share/icons/hicolor/256x256/apps/simplenote.png
x ./usr/share/icons/hicolor/512x512/
x ./usr/share/icons/hicolor/512x512/apps/
x ./usr/share/icons/hicolor/512x512/apps/simplenote.png
x ./usr/share/icons/hicolor/1024x1024/
x ./usr/share/icons/hicolor/1024x1024/apps/
x ./usr/share/icons/hicolor/1024x1024/apps/simplenote.png
x ./usr/share/applications/
x ./usr/share/applications/simplenote.desktop
x ./usr/share/doc/
x ./usr/share/doc/simplenote/
x ./usr/share/doc/simplenote/changelog.gz
==> Tidying install...
  -> Removing libtool files...
  -> Purging unwanted files...
  -> Removing static library files...
  -> Stripping unneeded symbols from binaries and libraries...
  -> Compressing man and info pages...
==> Checking for packaging issues...
==> Creating package "simplenote-electron-bin"...
  -> Generating .PKGINFO file...
  -> Generating .BUILDINFO file...
  -> Generating .MTREE file...
  -> Compressing package...
==> Leaving fakeroot environment.
==> Finished making: simplenote-electron-bin 2.21.0-1 (Min 17 Sep 2023 07:34:07 )
==> Installing package simplenote-electron-bin with pacman -U...
[sudo] password for tama: 
loading packages...
warning: simplenote-electron-bin-2.21.0-1 is up to date -- reinstalling
resolving dependencies...
looking for conflicting packages...

Packages (1) simplenote-electron-bin-2.21.0-1

Total Installed Size:  314,23 MiB
Net Upgrade Size:        0,00 MiB

:: Proceed with installation? [Y/n] 
(1/1) checking keys in keyring                                                                                                 [#############################################################################] 100%
(1/1) checking package integrity                                                                                               [#############################################################################] 100%
(1/1) loading package files                                                                                                    [#############################################################################] 100%
(1/1) checking for file conflicts                                                                                              [#############################################################################] 100%
:: Processing package changes...
(1/1) reinstalling simplenote-electron-bin                                                                                     [#############################################################################] 100%
:: Running post-transaction hooks...
(1/3) Arming ConditionNeedsUpdate...
(2/3) Updating icon theme caches...
(3/3) Updating the desktop file MIME type cache...
```


#### masalah

ketika ingin membuka dari membuka dari menu - aplikasi - simplenote, mengalami error, alias tidak mau terbuka

```
[tama@tamaoksa simplenote-electron-bin]$ simplenote
[29736:0917/073434.710552:FATAL:gpu_data_manager_impl_private.cc(415)] GPU process isn't usable. Goodbye.
Trace/breakpoint trap (core dumped)
```


#### cara memperbaiki

dapet cara dari forum manjaro, work juga kalo buat arch
sumber : https://forum.manjaro.org/t/error-gpu-process-isnt-usable-goodbye/104611

edit "/usr/share/applications/simplenote.desktop"

```
[tama@tamaoksa applications]$ cat simplenote.desktop
[Desktop Entry]
Name=Simplenote
Exec=/opt/Simplenote/simplenote %U
Terminal=false
Type=Application
Icon=simplenote
StartupWMClass=Simplenote
Comment=Simplenote is an easy way to keep notes, lists, ideas and more. Your notes stay in sync with all your devices for free.
GenericName=Note Taking Application
StartupNotify=true
Categories=Utility;
MimeType=x-scheme-handler/simplenote;
```
edit bagian

```
Exec=/opt/Simplenote/simplenote %U
```

menjadi

```
Exec=/opt/Simplenote/simplenote %U --no-sandbox
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/blob/master/_screenshots/simplenote-arch-oksa.png" />

Sekian terimakasih

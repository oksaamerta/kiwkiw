---
layout: post
slug: Numix Theme Simple Circle Icon
---

#### Numix Theme & Icon Pack Install Arch Linux XFCE4

karna bagus pake icon pack ini saja, monoton banget kalo pake bawaan XFCE

Clone dulu dari aur, pake "git"

```
[ichiruby@tamrist Theme]$ git clone https://aur.archlinux.org/numix-circle-icon-theme-git.git
Cloning into 'numix-circle-icon-theme-git'...
remote: Enumerating objects: 98, done.
remote: Counting objects: 100% (98/98), done.
remote: Compressing objects: 100% (80/80), done.
remote: Total 98 (delta 14), reused 96 (delta 14), pack-reused 0
Unpacking objects: 100% (98/98), 18.09 KiB | 268.00 KiB/s, done.
```



Jika sudah lalu panggil script PKGBUILD-nya pake "mkepkg -si". Output perintahNya saya sertakan untuk disamakan ketika tahap installasi ada error atau tidak.

```
[ichiruby@tamrist numix-icon-theme-pack]$ makepkg -si
==> Making package: numix-icon-theme-pack r6086-1 (Sat 23 Oct 2021 03:13:59 PM WIB)
==> Checking runtime dependencies...
==> Checking buildtime dependencies...
==> Installing missing dependencies...
resolving dependencies...
looking for conflicting packages...

Packages (18) boost-libs-1.76.0-1  enchant-2.3.1-1  graphicsmagick-1.3.36-3  gsl-2.7-1  gspell-1.8.4-1  gtest-1.11.0-1  lib2geom-1.1-1  libcdr-0.1.7-2
              librevenge-0.0.4-3  libvisio-0.1.7-5  libwpd-0.10.3-3  libwpg-0.3.3-2  libxslt-1.1.34-6  poppler-21.10.0-1  poppler-glib-21.10.0-1
              potrace-1.16-2  ragel-6.10-3  inkscape-1.1.1-2

Total Download Size:    31.57 MiB
Total Installed Size:  241.03 MiB

:: Proceed with installation? [Y/n] 
:: Retrieving packages...
 inkscape-1.1.1-2-x86_64                                        18.5 MiB  1932 KiB/s 00:10 [#####################################################] 100%
 graphicsmagick-1.3.36-3-x86_64                                  2.3 MiB  1464 KiB/s 00:02 [#####################################################] 100%
 boost-libs-1.76.0-1-x86_64                                      2.3 MiB  1694 KiB/s 00:01 [#####################################################] 100%
 gsl-2.7-1-x86_64                                             1612.5 KiB  1936 KiB/s 00:01 [#####################################################] 100%
 poppler-21.10.0-1-x86_64                                     1394.5 KiB  1945 KiB/s 00:01 [#####################################################] 100%
 libwpd-0.10.3-3-x86_64                                        994.6 KiB  1666 KiB/s 00:01 [#####################################################] 100%
 libcdr-0.1.7-2-x86_64                                         906.9 KiB  1889 KiB/s 00:00 [#####################################################] 100%
 libvisio-0.1.7-5-x86_64                                       624.1 KiB  1366 KiB/s 00:00 [#####################################################] 100%
 ragel-6.10-3-x86_64                                           571.3 KiB   860 KiB/s 00:01 [#####################################################] 100%
 librevenge-0.0.4-3-x86_64                                     555.4 KiB  1399 KiB/s 00:00 [#####################################################] 100%
 lib2geom-1.1-1-x86_64                                         500.2 KiB  1429 KiB/s 00:00 [#####################################################] 100%
 gtest-1.11.0-1-x86_64                                         486.8 KiB  1475 KiB/s 00:00 [#####################################################] 100%
 libxslt-1.1.34-6-x86_64                                       348.4 KiB  1893 KiB/s 00:00 [#####################################################] 100%
 poppler-glib-21.10.0-1-x86_64                                 257.1 KiB  1749 KiB/s 00:00 [#####################################################] 100%
 libwpg-0.3.3-2-x86_64                                         133.5 KiB   927 KiB/s 00:00 [#####################################################] 100%
 gspell-1.8.4-1-x86_64                                         124.3 KiB  1680 KiB/s 00:00 [#####################################################] 100%
 potrace-1.16-2-x86_64                                          91.1 KiB   685 KiB/s 00:00 [#####################################################] 100%
 enchant-2.3.1-1-x86_64                                         53.2 KiB   700 KiB/s 00:00 [#####################################################] 100%
 Total (18/18)                                                  31.6 MiB  1610 KiB/s 00:20 [#####################################################] 100%
(18/18) checking keys in keyring                                                           [#####################################################] 100%
(18/18) checking package integrity                                                         [#####################################################] 100%
(18/18) loading package files                                                              [#####################################################] 100%
(18/18) checking for file conflicts                                                        [#####################################################] 100%
(18/18) checking available disk space                                                      [#####################################################] 100%
:: Processing package changes...
( 1/18) installing graphicsmagick                                                          [#####################################################] 100%
Optional dependencies for graphicsmagick
    jasper: jp2 module [installed]
    libwmf: wmf module
    libxml2: msl, svg, url modules [installed]
    ghostscript: pdf, ps modules
( 2/18) installing gsl                                                                     [#####################################################] 100%
( 3/18) installing enchant                                                                 [#####################################################] 100%
Optional dependencies for enchant
    aspell: for aspell based spell checking support
    hunspell: for hunspell based spell checking support [installed]
    libvoikko: for libvoikko based spell checking support
    hspell: for hspell based spell checking support
    nuspell: for nuspell based spell checking support
( 4/18) installing gspell                                                                  [#####################################################] 100%
( 5/18) installing ragel                                                                   [#####################################################] 100%
( 6/18) installing gtest                                                                   [#####################################################] 100%
Optional dependencies for gtest
    python: gmock generator [installed]
( 7/18) installing lib2geom                                                                [#####################################################] 100%
( 8/18) installing boost-libs                                                              [#####################################################] 100%
Optional dependencies for boost-libs
    openmpi: for mpi support
( 9/18) installing librevenge                                                              [#####################################################] 100%
(10/18) installing libwpd                                                                  [#####################################################] 100%
(11/18) installing libcdr                                                                  [#####################################################] 100%
(12/18) installing libwpg                                                                  [#####################################################] 100%
(13/18) installing libvisio                                                                [#####################################################] 100%
(14/18) installing libxslt                                                                 [#####################################################] 100%
(15/18) installing poppler                                                                 [#####################################################] 100%
Optional dependencies for poppler
    poppler-data: highly recommended encoding data to display PDF documents with certain encodings and characters
(16/18) installing poppler-glib                                                            [#####################################################] 100%
(17/18) installing potrace                                                                 [#####################################################] 100%
(18/18) installing inkscape                                                                [#####################################################] 100%
Optional dependencies for inkscape
    fig2dev: xfig input
    gvfs: import clip art
    pstoedit: latex formulas
    python-lxml: some extensions
    python-numpy: some extensions
    scour: optimized SVG output, some extensions
    texlive-core: latex formulas
:: Running post-transaction hooks...
(1/5) Arming ConditionNeedsUpdate...
(2/5) Warn about old perl modules
(3/5) Updating icon theme caches...
(4/5) Updating the info directory file...
(5/5) Updating the desktop file MIME type cache...
==> Retrieving sources...
  -> Cloning numix-core git repo...
Cloning into bare repository '/home/ichiruby/Theme/numix-icon-theme-pack/numix-core'...
remote: Enumerating objects: 113977, done.
remote: Counting objects: 100% (4739/4739), done.
remote: Compressing objects: 100% (2211/2211), done.
remote: Total 113977 (delta 2646), reused 3416 (delta 1708), pack-reused 109238
Receiving objects: 100% (113977/113977), 72.13 MiB | 1.40 MiB/s, done.
Resolving deltas: 100% (68782/68782), done.
  -> Cloning numix-icon-theme git repo...
Cloning into bare repository '/home/ichiruby/Theme/numix-icon-theme-pack/numix-icon-theme'...
remote: Enumerating objects: 107098, done.
remote: Counting objects: 100% (1093/1093), done.
remote: Compressing objects: 100% (579/579), done.
remote: Total 107098 (delta 904), reused 649 (delta 501), pack-reused 106005
Receiving objects: 100% (107098/107098), 53.84 MiB | 1.34 MiB/s, done.
Resolving deltas: 100% (77035/77035), done.
  -> Cloning numix-icon-circle git repo...
Cloning into bare repository '/home/ichiruby/Theme/numix-icon-theme-pack/numix-icon-circle'...
remote: Enumerating objects: 9517, done.
remote: Counting objects: 100% (1402/1402), done.
remote: Compressing objects: 100% (544/544), done.
remote: Total 9517 (delta 664), reused 1103 (delta 450), pack-reused 8115
Receiving objects: 100% (9517/9517), 47.11 MiB | 1.46 MiB/s, done.
Resolving deltas: 100% (3840/3840), done.
  -> Cloning numix-icon-square git repo...
Cloning into bare repository '/home/ichiruby/Theme/numix-icon-theme-pack/numix-icon-square'...
remote: Enumerating objects: 14536, done.
remote: Counting objects: 100% (1409/1409), done.
remote: Compressing objects: 100% (668/668), done.
remote: Total 14536 (delta 525), reused 1075 (delta 334), pack-reused 13127
Receiving objects: 100% (14536/14536), 11.65 MiB | 1.25 MiB/s, done.
Resolving deltas: 100% (4850/4850), done.
==> Validating source files with sha256sums...
    numix-core ... Skipped
    numix-icon-theme ... Skipped
    numix-icon-circle ... Skipped
    numix-icon-square ... Skipped
==> Extracting sources...
  -> Creating working copy of numix-core git repo...
Cloning into 'numix-core'...
done.
Updating files: 100% (8822/8822), done.
  -> Creating working copy of numix-icon-theme git repo...
Cloning into 'numix-icon-theme'...
done.
Updating files: 100% (31841/31841), done.
  -> Creating working copy of numix-icon-circle git repo...
Cloning into 'numix-icon-circle'...
done.
Updating files: 100% (8329/8329), done.
  -> Creating working copy of numix-icon-square git repo...
Cloning into 'numix-icon-square'...
done.
Updating files: 100% (8329/8329), done.
==> Starting prepare()...

Generating Linux theme...
Done!


Generating Linux theme...
Done!

==> Starting pkgver()...
==> Updated version: numix-icon-theme-pack r7941-1
==> Entering fakeroot environment...
==> Starting package_numix-icon-theme-pack-git()...
==> Tidying install...
  -> Removing libtool files...
  -> Purging unwanted files...
  -> Removing static library files...
  -> Compressing man and info pages...
==> Checking for packaging issues...
==> Creating package "numix-icon-theme-pack-git"...
  -> Generating .PKGINFO file...
  -> Generating .BUILDINFO file...
  -> Generating .MTREE file...
  -> Compressing package...
==> Leaving fakeroot environment.
==> Finished making: numix-icon-theme-pack r7941-1 (Sat 23 Oct 2021 03:19:27 PM WIB)
==> Installing numix-icon-theme-pack package group with pacman -U...
[sudo] password for ichiruby: 
loading packages...
resolving dependencies...
looking for conflicting packages...

Packages (1) numix-icon-theme-pack-git-r7941-1

Total Installed Size:  48.37 MiB

:: Proceed with installation? [Y/n] 
(1/1) checking keys in keyring                                                             [#####################################################] 100%
(1/1) checking package integrity                                                           [#####################################################] 100%
(1/1) loading package files                                                                [#####################################################] 100%
(1/1) checking for file conflicts                                                          [#####################################################] 100%
(1/1) checking available disk space                                                        [#####################################################] 100%
:: Processing package changes...
(1/1) installing numix-icon-theme-pack-git                                                 [#####################################################] 100%
:: Running post-transaction hooks...
(1/2) Arming ConditionNeedsUpdate...
(2/2) Updating icon theme caches...
```

Done, no error.

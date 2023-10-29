untuk nge-game di linux emg ga segampang di windows, sedikit kompleks, tapi lancar.
saya memakai "bottles" untuk memainkanNya karna lumayan komplit daripada konfigurasi wine satu-persatu agak rumit untuk user awam seperti saya.


pastikan ter-update versi baru, khusus ubuntu

```
tama@tamagochi:~$ sudo apt update
[sudo] password for tama: 
Hit:1 http://id.archive.ubuntu.com/ubuntu jammy InRelease
Hit:2 http://id.archive.ubuntu.com/ubuntu jammy-updates InRelease                                  
Hit:3 http://id.archive.ubuntu.com/ubuntu jammy-backports InRelease                                
Hit:4 http://security.ubuntu.com/ubuntu jammy-security InRelease                                   
Hit:5 https://repo.radeon.com/amdgpu/23.20/amdgpu/ubuntu jammy InRelease
Hit:6 https://repo.radeon.com/amdgpu/23.20/rocm/apt/5.7 jammy InRelease
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
529 packages can be upgraded. Run 'apt list --upgradable' to see them.
```

```
tama@tamagochi:~$ sudo apt upgrade
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
Calculating upgrade... Done
The following packages were automatically installed and are no longer required:
  libflashrom1 libftdi1-2 libllvm13
Use 'sudo apt autoremove' to remove them.
The following NEW packages will be installed:
  firefox libatomic1 libllvm15 libwpe-1.0-1 libwpebackend-fdo-1.0-1 linux-headers-6.2.0-35-generic
  linux-hwe-6.2-headers-6.2.0-35 linux-image-6.2.0-35-generic linux-modules-6.2.0-35-generic
  linux-modules-extra-6.2.0-35-generic systemd-hwe-hwdb
The following packages will be upgraded:
  accountsservice alsa-ucm-conf amd64-microcode apparmor apport apport-gtk apt apt-utils
  avahi-autoipd avahi-daemon avahi-utils base-files bind9-dnsutils bind9-host bind9-libs brltty
  ca-certificates cpp-11 cups cups-browsed cups-bsd cups-client cups-common cups-core-drivers
  cups-daemon cups-filters cups-filters-core-drivers cups-ipp-utils cups-ppdc cups-server-common
  dbus dbus-user-session deja-dup dirmngr distro-info distro-info-data dmidecode dnsmasq-base dpkg
  e2fsprogs evince evince-common evolution-data-server evolution-data-server-common file
  firmware-sof-signed fonts-noto-color-emoji fonts-opensymbol fprintd fwupd fwupd-signed
  gcc-11-base gcc-12-base gdb gdm3 ghostscript ghostscript-x gir1.2-accountsservice-1.0
  gir1.2-adw-1 gir1.2-gdkpixbuf-2.0 gir1.2-gdm-1.0 gir1.2-gnomedesktop-3.0
  gir1.2-gst-plugins-base-1.0 gir1.2-gstreamer-1.0 gir1.2-gtk-3.0 gir1.2-gtk-4.0
  gir1.2-harfbuzz-0.0 gir1.2-javascriptcoregtk-4.0 gir1.2-mutter-10 gir1.2-nm-1.0
  gir1.2-notify-0.7 gir1.2-pango-1.0 gir1.2-rsvg-2.0 gir1.2-webkit2-4.0 gnome-control-center
  gnome-control-center-data gnome-control-center-faces gnome-desktop3-data gnome-initial-setup
  gnome-keyring gnome-keyring-pkcs11 gnome-remote-desktop gnome-session-canberra
  gnome-settings-daemon gnome-settings-daemon-common gnome-shell gnome-shell-common
  gnome-shell-extension-desktop-icons-ng gnome-shell-extension-ubuntu-dock gnupg gnupg-l10n
  gnupg-utils gpg gpg-agent gpg-wks-client gpg-wks-server gpgconf gpgsm gpgv grub-common
  grub-efi-amd64-bin grub-efi-amd64-signed grub-pc grub-pc-bin grub2-common gstreamer1.0-alsa
  gstreamer1.0-clutter-3.0 gstreamer1.0-gl gstreamer1.0-gtk3 gstreamer1.0-pipewire
  gstreamer1.0-plugins-base gstreamer1.0-plugins-base-apps gstreamer1.0-plugins-good
  gstreamer1.0-pulseaudio gstreamer1.0-tools gstreamer1.0-x gtk-update-icon-cache gvfs
  gvfs-backends gvfs-common gvfs-daemons gvfs-fuse gvfs-libs gzip im-config initramfs-tools
  initramfs-tools-bin initramfs-tools-core intel-microcode ipp-usb iptables irqbalance
  isc-dhcp-client isc-dhcp-common kbd language-pack-en language-pack-en-base
  language-pack-gnome-en language-pack-gnome-en-base language-selector-common
  language-selector-gnome less libaccountsservice0 libadwaita-1-0 libapparmor1 libapt-pkg6.0
  libavahi-client3 libavahi-common-data libavahi-common3 libavahi-core7 libavahi-glib1
  libavahi-ui-gtk3-0 libbpf0 libbrlapi0.8 libc-bin libc6 libc6-dbg libcamel-1.2-63
  libcanberra-gtk3-0 libcanberra-gtk3-module libcanberra-pulse libcanberra0 libcap2 libcap2-bin
  libclutter-gst-3.0-0 libcom-err2 libcryptsetup12 libcue2 libcups2 libcupsfilters1 libcupsimage2
  libcurl3-gnutls libcurl4 libdbus-1-3 libdrm-amdgpu1 libdrm-common libdrm-intel1 libdrm-nouveau2
  libdrm-radeon1 libdrm2 libebackend-1.2-10 libebook-1.2-20 libebook-contacts-1.2-3 libecal-2.0-1
  libedata-book-1.2-26 libedata-cal-2.0-1 libedataserver-1.2-26 libedataserverui-1.2-3
  libegl-mesa0 libevdocument3-4 libevview3-3 libexempi8 libexpat1 libext2fs2 libflac8
  libfontembed1 libfprint-2-2 libfreerdp-client2-2 libfreerdp-server2-2 libfreerdp2-2 libfreetype6
  libfribidi0 libfwupd2 libfwupdplugin5 libgbm1 libgcc-s1 libgdk-pixbuf-2.0-0 libgdk-pixbuf2.0-bin
  libgdk-pixbuf2.0-common libgdm1 libgl1-amber-dri libgl1-mesa-dri libglapi-mesa libglib2.0-0
  libglib2.0-bin libglib2.0-data libglx-mesa0 libgnome-bg-4-1 libgnome-desktop-3-19
  libgnome-desktop-4-1 libgnutls30 libgomp1 libgpgme11 libgpgmepp6 libgs9 libgs9-common
  libgssapi-krb5-2 libgstreamer-gl1.0-0 libgstreamer-plugins-base1.0-0
  libgstreamer-plugins-good1.0-0 libgstreamer1.0-0 libgtk-3-0 libgtk-3-bin libgtk-3-common
  libgtk-4-1 libgtk-4-bin libgtk-4-common libharfbuzz-icu0 libharfbuzz0b libhttp-daemon-perl
  libidn12 libinput-bin libinput10 libip4tc2 libip6tc2 libjavascriptcoregtk-4.0-18 libjbig0
  libjson-c5 libk5crypto3 libkpathsea6 libkrb5-3 libkrb5support0 libksba8 libldap-2.5-0
  libldap-common libldb2 libllvm13 liblouis-data liblouis20 libmagic-mgc libmagic1 libmbim-glib4
  libmbim-proxy libmm-glib0 libmozjs-91-0 libmutter-10-0 libnautilus-extension1a libncurses6
  libncursesw6 libnetplan0 libnftables1 libnm0 libnotify-bin libnotify4 libnss-systemd libnss3
  libntfs-3g89 libpam-cap libpam-fprintd libpam-gnome-keyring libpam-modules libpam-modules-bin
  libpam-runtime libpam-sss libpam-systemd libpam0g libpango-1.0-0 libpangocairo-1.0-0
  libpangoft2-1.0-0 libpangoxft-1.0-0 libpcre2-32-0 libpcre2-8-0 libpcre3 libpcsclite1 libperl5.34
  libpipewire-0.3-0 libpipewire-0.3-common libpipewire-0.3-modules libpixman-1-0 libpkcs11-helper1
  libpoppler-cpp0v5 libpoppler-glib8 libpoppler118 libprotobuf23 libpulse-mainloop-glib0 libpulse0
  libpulsedsp libpython3-stdlib libpython3.10 libpython3.10-minimal libpython3.10-stdlib
  libqmi-glib5 libqmi-proxy libraw20 libreoffice-base-core libreoffice-calc libreoffice-common
  libreoffice-core libreoffice-draw libreoffice-gnome libreoffice-gtk3 libreoffice-help-common
  libreoffice-help-en-us libreoffice-impress libreoffice-math libreoffice-ogltrans
  libreoffice-pdfimport libreoffice-style-breeze libreoffice-style-colibre
  libreoffice-style-elementary libreoffice-style-yaru libreoffice-writer librsvg2-2
  librsvg2-common libsasl2-2 libsasl2-modules libsasl2-modules-db libsasl2-modules-gssapi-mit
  libsgutils2-2 libsmbclient libsnmp-base libsnmp40 libspa-0.2-modules libspeechd2 libsqlite3-0
  libss2 libssh-4 libssl3 libstdc++6 libsynctex2 libsystemd0 libtiff5 libtinfo6 libtirpc-common
  libtirpc3 libudev1 libuno-cppu3 libuno-cppuhelpergcc3-3 libuno-purpenvhelpergcc3-3 libuno-sal3
  libuno-salhelpergcc3-3 libunwind8 libusb-1.0-0 libvpx7 libwayland-client0 libwayland-cursor0
  libwayland-egl1 libwayland-server0 libwbclient0 libwebkit2gtk-4.0-37 libwebp7 libwebpdemux2
  libwebpmux3 libwinpr2-2 libx11-6 libx11-data libx11-xcb1 libxatracker2 libxml2 libxpm4
  libxslt1.1 libxtables12 linux-firmware linux-generic-hwe-22.04 linux-headers-generic-hwe-22.04
  linux-image-generic-hwe-22.04 locales login logrotate logsave mesa-vulkan-drivers modemmanager
  mokutil mutter-common nautilus nautilus-data ncurses-base ncurses-bin netplan.io network-manager
  network-manager-config-connectivity-ubuntu networkd-dispatcher nftables ntfs-3g openssh-client
  openssl openvpn orca passwd perl perl-base perl-modules-5.34 pipewire pipewire-bin poppler-utils
  printer-driver-foo2zjs printer-driver-foo2zjs-common printer-driver-splix pulseaudio
  pulseaudio-module-bluetooth pulseaudio-utils python-apt-common python3 python3-apport
  python3-apt python3-brlapi python3-debian python3-distro-info python3-distupgrade python3-future
  python3-gdbm python3-gi python3-gi-cairo python3-jwt python3-ldb python3-lib2to3 python3-louis
  python3-macaroonbakery python3-mako python3-minimal python3-oauthlib python3-pil
  python3-pkg-resources python3-problem-report python3-protobuf python3-renderpm python3-reportlab
  python3-reportlab-accel python3-requests python3-software-properties python3-speechd python3-tz
  python3-uno python3-update-manager python3.10 python3.10-minimal remmina remmina-common
  remmina-plugin-rdp remmina-plugin-secret remmina-plugin-vnc rsync rsyslog samba-libs shim-signed
  shotwell shotwell-common snapd software-properties-common software-properties-gtk
  speech-dispatcher speech-dispatcher-audio-plugins speech-dispatcher-espeak-ng sudo systemd
  systemd-oomd systemd-sysv systemd-timesyncd tar tcpdump thermald thunderbird
  thunderbird-gnome-support thunderbird-locale-en thunderbird-locale-en-us tzdata
  ubuntu-advantage-desktop-daemon ubuntu-advantage-tools ubuntu-desktop ubuntu-desktop-minimal
  ubuntu-docs ubuntu-drivers-common ubuntu-minimal ubuntu-release-upgrader-core
  ubuntu-release-upgrader-gtk ubuntu-standard udev ufw uno-libs-private unzip update-manager
  update-manager-core update-notifier update-notifier-common ure vim-common vim-tiny
  wireless-regdb wpasupplicant xbrlapi xdg-desktop-portal xdg-desktop-portal-gnome xdg-utils
  xserver-common xserver-xephyr xserver-xorg-core xserver-xorg-legacy xserver-xorg-video-amdgpu
  xserver-xorg-video-ati xserver-xorg-video-radeon xwayland xxd yaru-theme-gnome-shell
  yaru-theme-gtk yaru-theme-icon yaru-theme-sound zenity zenity-common zlib1g
529 upgraded, 11 newly installed, 0 to remove and 0 not upgraded.
277 standard security updates
Need to get 939 MB of archives.
After this operation, 1.056 MB of additional disk space will be used.
Do you want to continue? [Y/n]
```




install flatpak

```
tama@tamagochi:~$ sudo apt install flatpak
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  libappstream-glib8 libfuse2 libmalcontent-0-0 libostree-1-1
Suggested packages:
  malcontent-gui
The following NEW packages will be installed:
  flatpak libappstream-glib8 libfuse2 libmalcontent-0-0 libostree-1-1
0 upgraded, 5 newly installed, 0 to remove and 5 not upgraded.
Need to get 1.918 kB of archives.
After this operation, 6.700 kB of additional disk space will be used.
Do you want to continue? [Y/n]
```

```
tama@tamagochi:~$ sudo apt install gnome-software-plugin-flatpak
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following additional packages will be installed:
  gnome-software gnome-software-common gnome-software-plugin-snap libflatpak0
The following NEW packages will be installed:
  gnome-software gnome-software-common gnome-software-plugin-flatpak gnome-software-plugin-snap
  libflatpak0
0 upgraded, 5 newly installed, 0 to remove and 5 not upgraded.
Need to get 1.006 kB of archives.
After this operation, 4.251 kB of additional disk space will be used.
Do you want to continue? [Y/n]
```

```
tama@tamagochi:~$ flatpak remote-add --if-not-exists flathub https://dl.flathub.org/repo/flathub.flatpakrepo

Note that the directories 

'/var/lib/flatpak/exports/share'
'/home/tama/.local/share/flatpak/exports/share'

are not in the search path set by the XDG_DATA_DIRS environment variable, so
applications installed by Flatpak may not appear on your desktop until the
session is restarted.
```

mulai ulang setelah installasi 

```
tama@tamagochi:~$ reboot
```




install bottles dari flatpak

```
tama@tamagochi:~$ flatpak install flathub com.usebottles.bottles
Looking for matches…
Required runtime for com.usebottles.bottles/x86_64/stable (runtime/org.gnome.Platform/x86_64/44) found in remote flathub
Do you want to install it? [Y/n]: 

com.usebottles.bottles permissions:
    ipc                     network                 pulseaudio                     wayland
    x11                     devices                 devel                          multiarch
    per-app-dev-shm         file access [1]         system dbus access [2]

    [1] xdg-download
    [2] org.freedesktop.UDisks2


        ID                                         Branch        Op  Remote   Download
 1.     com.usebottles.bottles.Locale              stable        i   flathub  < 957,0 kB (partial)
 2.     org.freedesktop.Platform.GL.default        22.08         i   flathub  < 143,1 MB
 3.     org.freedesktop.Platform.GL.default        22.08-extra   i   flathub  < 143,1 MB
 4.     org.freedesktop.Platform.GL32.default      22.08         i   flathub  < 153,1 MB
 5.     org.freedesktop.Platform.ffmpeg-full       22.08         i   flathub    < 4,0 MB
 6.     org.freedesktop.Platform.ffmpeg_full.i386  22.08         i   flathub    < 4,1 MB
 7.     org.freedesktop.Platform.openh264          2.2.0         i   flathub  < 944,3 kB
 8.     org.gnome.Platform.Compat.i386             44            i   flathub  < 202,4 MB
 9.     org.gnome.Platform.Locale                  44            i   flathub  < 340,6 MB (partial)
10.     org.gtk.Gtk3theme.Yaru-dark                3.22          i   flathub  < 196,5 kB
11.     org.gnome.Platform                         44            i   flathub  < 326,9 MB
12.     org.winehq.Wine.DLLs.dxvk                  stable-22.08  i   flathub    < 7,9 MB
13.     org.winehq.Wine.gecko                      stable-22.08  i   flathub  < 109,9 MB
14.     org.winehq.Wine.mono                       stable-22.08  i   flathub   < 85,9 MB
15.     com.usebottles.bottles                     stable        i   flathub  < 156,0 MB

Proceed with these changes to the system installation? [Y/n]:
```




install amdgpu

```
tama@tamagochi:~/Downloads$ ls
amdgpu-install_5.7.50700-1_all.deb  firefox.tmp
tama@tamagochi:~/Downloads$ sudo dpkg -i amdgpu-install_5.7.50700-1_all.deb
[sudo] password for tama: 
Selecting previously unselected package amdgpu-install.
(Reading database ... 200724 files and directories currently installed.)
Preparing to unpack amdgpu-install_5.7.50700-1_all.deb ...
Unpacking amdgpu-install (5.7.50700-1653597.22.04) ...
Setting up amdgpu-install (5.7.50700-1653597.22.04) ...
```

```
tama@tamagochi:~$ amdgpu-install
Hit:1 http://id.archive.ubuntu.com/ubuntu jammy InRelease
Get:2 http://id.archive.ubuntu.com/ubuntu jammy-updates InRelease [119 kB]
Get:3 http://security.ubuntu.com/ubuntu jammy-security InRelease [110 kB]
Get:4 http://id.archive.ubuntu.com/ubuntu jammy-backports InRelease [109 kB]
Get:5 http://id.archive.ubuntu.com/ubuntu jammy-updates/main amd64 Packages [1.104 kB]
Get:6 http://id.archive.ubuntu.com/ubuntu jammy-updates/main i386 Packages [516 kB]
Get:7 http://security.ubuntu.com/ubuntu jammy-security/main amd64 DEP-11 Metadata [43,0 kB]
Get:8 http://id.archive.ubuntu.com/ubuntu jammy-updates/main amd64 DEP-11 Metadata [101 kB]
Get:9 http://id.archive.ubuntu.com/ubuntu jammy-updates/universe i386 Packages [660 kB]
Get:10 http://security.ubuntu.com/ubuntu jammy-security/universe amd64 DEP-11 Metadata [55,1 kB]
Get:11 http://id.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 Packages [995 kB]
Get:12 http://id.archive.ubuntu.com/ubuntu jammy-updates/universe amd64 DEP-11 Metadata [305 kB]
Get:13 http://id.archive.ubuntu.com/ubuntu jammy-updates/multiverse amd64 DEP-11 Metadata [940 B]
Get:14 http://id.archive.ubuntu.com/ubuntu jammy-backports/main amd64 DEP-11 Metadata [4.928 B]
Get:15 http://id.archive.ubuntu.com/ubuntu jammy-backports/universe amd64 DEP-11 Metadata [17,7 kB]
Hit:16 https://repo.radeon.com/amdgpu/23.20/amdgpu/ubuntu jammy InRelease
Hit:17 https://repo.radeon.com/amdgpu/23.20/rocm/apt/5.7 jammy InRelease                           
Fetched 4.140 kB in 7s (620 kB/s)                                                                  
Reading package lists... Done
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
linux-headers-6.2.0-35-generic is already the newest version (6.2.0-35.35~22.04.1).
linux-headers-6.2.0-35-generic set to manually installed.
The following additional packages will be installed:
  amdgpu-core amdgpu-dkms-firmware autoconf automake autotools-dev binutils binutils-common
  binutils-x86-64-linux-gnu build-essential comgr cpp-12 dctrl-tools dkms dpkg-dev fakeroot g++
  g++-11 g++-11-multilib g++-multilib gcc gcc-11 gcc-11-multilib gcc-12 gcc-12-base:i386
  gcc-multilib gst-omx-amdgpu hip-dev hip-runtime-amd hipcc hsa-rocr hsa-rocr-dev hsakmt-roct-dev
  krb5-locales lib32asan6 lib32atomic1 lib32gcc-11-dev lib32gcc-s1 lib32gomp1 lib32itm1
  lib32quadmath0 lib32stdc++-11-dev lib32stdc++6 lib32ubsan1 libalgorithm-diff-perl
  libalgorithm-diff-xs-perl libalgorithm-merge-perl libasan6 libasan8 libatomic1:i386 libbinutils
  libbsd0:i386 libc-dev-bin libc-devtools libc6:i386 libc6-dev libc6-dev-i386 libc6-dev-x32
  libc6-i386 libc6-x32 libcc1-0 libcom-err2:i386 libcrypt-dev libcrypt1:i386 libctf-nobfd0 libctf0
  libdpkg-perl libdrm-amdgpu-amdgpu1 libdrm-amdgpu-amdgpu1:i386 libdrm-amdgpu-common
  libdrm-amdgpu-dev libdrm-amdgpu-radeon1 libdrm-amdgpu-radeon1:i386 libdrm-amdgpu1:i386
  libdrm-intel1:i386 libdrm-nouveau2:i386 libdrm-radeon1:i386 libdrm2:i386 libdrm2-amdgpu
  libdrm2-amdgpu:i386 libedit2:i386 libegl-mesa0:i386 libegl1:i386 libegl1-amdgpu-mesa
  libegl1-amdgpu-mesa:i386 libegl1-amdgpu-mesa-drivers libegl1-amdgpu-mesa-drivers:i386 libelf-dev
  libelf1:i386 libexpat1:i386 libfakeroot libffi8:i386 libfile-copy-recursive-perl
  libfile-fcntllock-perl libfile-which-perl libgbm1:i386 libgbm1-amdgpu libgbm1-amdgpu:i386
  libgcc-11-dev libgcc-12-dev libgcc-s1:i386 libgl1:i386 libgl1-amdgpu-mesa-dri
  libgl1-amdgpu-mesa-dri:i386 libgl1-amdgpu-mesa-glx libgl1-amdgpu-mesa-glx:i386
  libgl1-mesa-dri:i386 libglapi-amdgpu-mesa libglapi-amdgpu-mesa:i386 libglapi-mesa:i386
  libglvnd0:i386 libglx-mesa0:i386 libglx0:i386 libgssapi-krb5-2:i386 libicu70:i386 libidn2-0:i386
  libitm1 libk5crypto3:i386 libkeyutils1:i386 libkrb5-3:i386 libkrb5support0:i386 libllvm15:i386
  libllvm16.0.50700-amdgpu libllvm16.0.50700-amdgpu:i386 liblsan0 liblzma5:i386 libmd0:i386
  libncurses-dev libnsl-dev libnsl2:i386 libnss-nis:i386 libnss-nisplus:i386 libomxil-bellagio-bin
  libomxil-bellagio0 libpciaccess0:i386 libquadmath0 libsensors5:i386 libsigsegv2 libssl3:i386
  libstdc++-11-dev libstdc++6:i386 libtinfo-dev libtinfo6:i386 libtirpc-dev libtirpc3:i386
  libtsan0 libtsan2 libubsan1 libudev1:i386 libunistring2:i386 liburi-encode-perl libva2
  libva2:i386 libvdpau1 libvdpau1:i386 libwayland-amdgpu-client0 libwayland-amdgpu-client0:i386
  libwayland-amdgpu-egl1:i386 libwayland-amdgpu-server0 libwayland-amdgpu-server0:i386
  libwayland-client0:i386 libwayland-server0:i386 libx11-6:i386 libx11-xcb1:i386 libx32asan6
  libx32atomic1 libx32gcc-11-dev libx32gcc-s1 libx32gomp1 libx32itm1 libx32quadmath0
  libx32stdc++-11-dev libx32stdc++6 libx32ubsan1 libxatracker2-amdgpu libxatracker2-amdgpu:i386
  libxau6:i386 libxcb-dri2-0:i386 libxcb-dri3-0:i386 libxcb-glx0:i386 libxcb-present0:i386
  libxcb-randr0:i386 libxcb-shm0:i386 libxcb-sync1:i386 libxcb-xfixes0:i386 libxcb1:i386
  libxdmcp6:i386 libxext6:i386 libxfixes3:i386 libxml2:i386 libxshmfence1:i386 libxxf86vm1:i386
  libzstd1:i386 linux-libc-dev lto-disabled-list m4 make manpages-dev mesa-amdgpu-omx-drivers
  mesa-amdgpu-va-drivers mesa-amdgpu-va-drivers:i386 mesa-amdgpu-vdpau-drivers
  mesa-amdgpu-vdpau-drivers:i386 mesa-vdpau-drivers mesa-vdpau-drivers:i386 openmp-extras-runtime
  rocm-core rocm-language-runtime rocm-llvm rocm-ocl-icd rocm-opencl rocminfo rpcsvc-proto
  valgrind vdpau-driver-all vdpau-driver-all:i386 xserver-xorg-amdgpu-video-amdgpu zlib1g:i386
  zlib1g-dev
Suggested packages:
  autoconf-archive gnu-standards autoconf-doc libtool gettext binutils-doc gcc-12-locales
  cpp-12-doc debtags menu debian-keyring gcc-11-doc lib32stdc++6-11-dbg libx32stdc++6-11-dbg flex
  bison gcc-doc gcc-11-locales gcc-12-multilib gcc-12-doc glibc-doc:i386 locales:i386 glibc-doc
  git bzr libglide3 libglide3:i386 krb5-doc:i386 krb5-user:i386 ncurses-doc
  libomxil-bellagio0-components-base lm-sensors:i386 libstdc++-11-doc m4-doc make-doc valgrind-dbg
  valgrind-mpi kcachegrind alleyoop valkyrie libvdpau-va-gl1 libvdpau-va-gl1:i386
Recommended packages:
  libtxc-dxtn-s2tc0 | libtxc-dxtn0 libtxc-dxtn-s2tc0:i386 | libtxc-dxtn0:i386
  libgl1-amber-dri:i386
The following NEW packages will be installed:
  amdgpu-core amdgpu-dkms amdgpu-dkms-firmware amdgpu-lib amdgpu-lib32 autoconf automake
  autotools-dev binutils binutils-common binutils-x86-64-linux-gnu build-essential comgr cpp-12
  dctrl-tools dkms dpkg-dev fakeroot g++ g++-11 g++-11-multilib g++-multilib gcc gcc-11
  gcc-11-multilib gcc-12 gcc-12-base:i386 gcc-multilib gst-omx-amdgpu hip-dev hip-runtime-amd
  hipcc hsa-rocr hsa-rocr-dev hsakmt-roct-dev krb5-locales lib32asan6 lib32atomic1 lib32gcc-11-dev
  lib32gcc-s1 lib32gomp1 lib32itm1 lib32quadmath0 lib32stdc++-11-dev lib32stdc++6 lib32ubsan1
  libalgorithm-diff-perl libalgorithm-diff-xs-perl libalgorithm-merge-perl libasan6 libasan8
  libatomic1:i386 libbinutils libbsd0:i386 libc-dev-bin libc-devtools libc6:i386 libc6-dev
  libc6-dev-i386 libc6-dev-x32 libc6-i386 libc6-x32 libcc1-0 libcom-err2:i386 libcrypt-dev
  libcrypt1:i386 libctf-nobfd0 libctf0 libdpkg-perl libdrm-amdgpu-amdgpu1
  libdrm-amdgpu-amdgpu1:i386 libdrm-amdgpu-common libdrm-amdgpu-dev libdrm-amdgpu-radeon1
  libdrm-amdgpu-radeon1:i386 libdrm-amdgpu1:i386 libdrm-intel1:i386 libdrm-nouveau2:i386
  libdrm-radeon1:i386 libdrm2:i386 libdrm2-amdgpu libdrm2-amdgpu:i386 libedit2:i386
  libegl-mesa0:i386 libegl1:i386 libegl1-amdgpu-mesa libegl1-amdgpu-mesa:i386
  libegl1-amdgpu-mesa-drivers libegl1-amdgpu-mesa-drivers:i386 libelf-dev libelf1:i386
  libexpat1:i386 libfakeroot libffi8:i386 libfile-copy-recursive-perl libfile-fcntllock-perl
  libfile-which-perl libgbm1:i386 libgbm1-amdgpu libgbm1-amdgpu:i386 libgcc-11-dev libgcc-12-dev
  libgcc-s1:i386 libgl1:i386 libgl1-amdgpu-mesa-dri libgl1-amdgpu-mesa-dri:i386
  libgl1-amdgpu-mesa-glx libgl1-amdgpu-mesa-glx:i386 libgl1-mesa-dri:i386 libglapi-amdgpu-mesa
  libglapi-amdgpu-mesa:i386 libglapi-mesa:i386 libglvnd0:i386 libglx-mesa0:i386 libglx0:i386
  libgssapi-krb5-2:i386 libicu70:i386 libidn2-0:i386 libitm1 libk5crypto3:i386 libkeyutils1:i386
  libkrb5-3:i386 libkrb5support0:i386 libllvm15:i386 libllvm16.0.50700-amdgpu
  libllvm16.0.50700-amdgpu:i386 liblsan0 liblzma5:i386 libmd0:i386 libncurses-dev libnsl-dev
  libnsl2:i386 libnss-nis:i386 libnss-nisplus:i386 libomxil-bellagio-bin libomxil-bellagio0
  libpciaccess0:i386 libquadmath0 libsensors5:i386 libsigsegv2 libssl3:i386 libstdc++-11-dev
  libstdc++6:i386 libtinfo-dev libtinfo6:i386 libtirpc-dev libtirpc3:i386 libtsan0 libtsan2
  libubsan1 libudev1:i386 libunistring2:i386 liburi-encode-perl libva2 libva2:i386 libvdpau1
  libvdpau1:i386 libwayland-amdgpu-client0 libwayland-amdgpu-client0:i386
  libwayland-amdgpu-egl1:i386 libwayland-amdgpu-server0 libwayland-amdgpu-server0:i386
  libwayland-client0:i386 libwayland-server0:i386 libx11-6:i386 libx11-xcb1:i386 libx32asan6
  libx32atomic1 libx32gcc-11-dev libx32gcc-s1 libx32gomp1 libx32itm1 libx32quadmath0
  libx32stdc++-11-dev libx32stdc++6 libx32ubsan1 libxatracker2-amdgpu libxatracker2-amdgpu:i386
  libxau6:i386 libxcb-dri2-0:i386 libxcb-dri3-0:i386 libxcb-glx0:i386 libxcb-present0:i386
  libxcb-randr0:i386 libxcb-shm0:i386 libxcb-sync1:i386 libxcb-xfixes0:i386 libxcb1:i386
  libxdmcp6:i386 libxext6:i386 libxfixes3:i386 libxml2:i386 libxshmfence1:i386 libxxf86vm1:i386
  libzstd1:i386 linux-libc-dev lto-disabled-list m4 make manpages-dev mesa-amdgpu-omx-drivers
  mesa-amdgpu-va-drivers mesa-amdgpu-va-drivers:i386 mesa-amdgpu-vdpau-drivers
  mesa-amdgpu-vdpau-drivers:i386 mesa-vdpau-drivers mesa-vdpau-drivers:i386 openmp-extras-runtime
  rocm-core rocm-hip-runtime rocm-language-runtime rocm-llvm rocm-ocl-icd rocm-opencl
  rocm-opencl-runtime rocminfo rpcsvc-proto valgrind vdpau-driver-all vdpau-driver-all:i386
  xserver-xorg-amdgpu-video-amdgpu zlib1g:i386 zlib1g-dev
0 upgraded, 223 newly installed, 0 to remove and 5 not upgraded.
Need to get 1.784 MB of archives.
After this operation, 2.259 MB of additional disk space will be used.
Do you want to continue? [Y/n]
```




reboot jangan lupa

```
tama@tamagochi:~$ reboot
```




installasi dari file iso

```
tama@tamagochi:~/Downloads$ sudo mount ~/Downloads/sekiro.iso ~/Downloads -o loop
[sudo] password for tama: 
mount: /home/tama/Downloads: WARNING: source write-protected, mounted read-only.
```

```
tama@tamagochi:~/Downloads$ sudo umount ~/Downloads
```

installasi file dari boottles,

```
create new bottle
```

pilih running exe dari file iso - install, tinggal install seperti biasa lalu jalankan

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/sekirolinux.png" />


Sekian.

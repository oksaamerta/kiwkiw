---
layout: post
slug: Manual Install Arch Linux Console
---


#### Catatan, pas dapet tugas install arch linux

Download iso dulu sih kek biasa

cek booting pake bios / efi

```
~: ls /sys/firmware/efi/efivars
```



list partisi sebelum install

```
~: fdisk -l
```



buat partisi di partisu yg di tentukan

```
~: cfdisk /dev/sda
```



Partisi pilih GPT

Kalau tipeNya efi, mending partisi tambahin boot

swap = setengah dari kapasitas ram
filesystem = pake semua ajg, sisanya buat swap

Cek kembali partisi yg sudah dibuat

```
~: fdisk -l
```



buat partisi file system

```
~: mkfs.ext4 /dev/sda1
```



sesuaikan filesystemNya dimana

mounting direktori hdd ke dir /mnt

```
~: mount /dev/sda1  /mnt
```



buat partisi booting efi

```
~: mkfs.ext2 /dev/sda3
```



mounting direktori booting ke dir boot

```
~: mount /dev/sda3 /mnt/boot/efi
```



kalau belum ada buat dulu

```
~: mkdir /mnt/boot/efi
```



buat partisi swap

```
~: mkswap /dev/sda2
```



aktifin swapNya

```
~: swapon /dev/sda2
```



install system arch

```
~: pacstrap /mnt base base-devel
```



masuk ke chroot

```
~: arch-chroot /mnt
```

#### SAMPEK DISINI DAH BERHASIL INSTALL, TINGGAL ATUR ATUR DIKIT AJA BOOTLOADER BIAR BISA BOOTING WAKTU PC / KOMPUTER NYALA


setting password root

```
~: passwd
```



pilih bahasa sistem

```
~: nano /etc/locale.gen
```



lalu generate bahasanya biar aktip

```
~: locale-gen
```



masuk ke direktori untuk memilih zona waktu

```
~: cd /usr/share/zoneinfo/Asia
```



List zona pake LS kek biasa

```
~: ls
```



Pastikan zona wilayhmu ada kawan

select zona

```
~: ln - s /usr/share/zoneinfo/Asia/Jakarta /etclocaltime
```



jika sudah ada localtime "fileexist" dihapus dulu localtimeNya pake : rm /etc/localtime

kalau sudah ketikan perintah select zona tadi

buat hostname / nama root dari sistem arch linuxMu

```
~: echo AsmDay > /etc/hostname
```



installasi grub untuk booting

```
~: pacman -S grub-bios
```



install grub ke direktori harddisk

```
~: grub-install --efi-directory=/boot
```



install linux preset

```
~: pacman -S linux mkinitcpio
```



konfigurasi file file yg sudah di install tadi

```
~: mkinitcpio -p linux
```



konfigurasi untuk grub

```
~: grub-mkconfig -o /boot/grub/grub.cfg
```



gen boot ke mount direktori

```
~: genfstab /mnt >> /mnt/etc/fstab
```



exit dari chroot

```
~: exit
```



umount dir mnt

```
~: umount /mnt
```



restart sistem

```
~: reboot
```

Done, sekolah salah ngambil jurusan -__
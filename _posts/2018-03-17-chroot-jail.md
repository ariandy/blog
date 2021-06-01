---
layout: post
title: chroot Jail (Repair GRUB)
category: linux debian ubuntu elementaryos grub
date: 2018-03-17 12:00:00
permalink: /:year/:month/:day/:title:output_ext
---
### Case
* OS terinstall. Namun Grub tidak ada.

### Requirement
* Debian-based Live-USB

### Installation
* Buka GParted untuk melihat partisi mana yang terpasang Linux (Debian-based)
* Mounting partisi tersebut ke `/mnt`. (Misal: Linux ditemukan terinstall pada `sda1`)

```
sudo mount /dev/sda1 /mnt
```
* Lakukan binding

```
sudo mount --bind /dev /mnt/dev
sudo mount --bind /dev/pts /mnt/dev/pts
sudo mount --bind /proc /mnt/proc
sudo mount --bind /sys /mnt/sys
```
* Gunakan `chroot`

```
sudo chroot
```

* Install Grub. Hanya gunakan huruv drive, tanpa angka partisi.

```
grub-install /dev/sda
grub-install --recheck /dev/sda
update-grub
```

* `umount` semuanya dan `poweroff`

```
exit
sudo umount /mnt/sys
sudo umount /mnt/proc
sudo umount /mnt/dev/pts
sudo umount /mnt/dev
sudo umount /mnt/
sudo poweroff
```

### Notes
* Kasus : Dual-boot Windows dan Linux. Namun Windows tidak tertera pada Grub.  
Apabila sudah berhasil masuk ke dalam Linux, namun tidak ditemui Windows pada Grub, kembali install Grub saat di dalam Linux.

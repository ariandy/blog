---
layout: post
title: "elementary OS (Loki 0.4.1)"
category: elementaryos linux
date: 2018-03-16 11:00:00
permalink: /:year/:month/:day/:title:output_ext
---
### Case
* Grub rusak
* Partisi Linux Ext4 hilang

### Must-do
* Perlu ganti distribusi

### Requirements
* PC / Laptop yang akan di reinstall
* elementary OS (Loki 0.4.1)
* Flashdisk 8GB
* PC / Laptop yang tidak rusak (untuk membuat USB Boot)
* Etcher

### Instalation
* Buat Bootable USB dengan Etcher
* Karena elementary OS mirip dengan Ubuntu, maka install selayaknya menginstall Ubuntu
* Di saat penginstalan berlangsung, jangan centang pilihan "Third Party"
* Tunggu hingga selesai

### What If...
* Grub masih hilang :  
Repair Grub dengan metode [chroot jail][chroot]
* Instalasi berhasil :  
Periksa Wi-Fi signal strength. Jika buruk, [reinstall driver Realtek][realtek]

### Notes
Instalasi dilakukan pada Asus E202S

[chroot]:  {{ site.baseurl }}{% post_url 2018-03-17-chroot-jail %}
[realtek]: {{ site.baseurl }}{% post_url 2018-03-17-realtek-repair %}

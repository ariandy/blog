---
layout: post
title: Realtek RTL8821AE on Debian
category: linux debian ubuntu elementaryos grub
date: 2018-03-17 13:00:00
permalink: /:year/:month/:day/:title:output_ext
---
### Case
* Wi-Fi signal pada Asus E202S lemah

### Analyze
Pada beberapa kasus, Wi-Fi card dilengkapi dengan 2 antena, namun yang diaktifkan oleh drivernya adalah antena yang lemah. Maka driver Realtek harus diinstall kembali dengan memilih antena yang lebih kuat.

Untuk mengetahui driver yang digunakan, gunakan perintah :

```
lsmod | grep rtl[0-9]
```
Output dengan angka tersebut merupakan nama dari driver yang kita perlukan.
### Installation
* Download driver Realtek dari `git`. Dan install driver tersebut.

```
git clone https://github.com/lwfinger/rtlwifi_new
cd rtlwifi_new
sudo make install
sudo modprobe -rv rtl8821ae
sudo modprobe -v rtl8821ae ant_sel=2
```
Jika tidak ada perubahan, ubah `ant_sel=2` ke `ant_sel=1`

```
sudo modprobe -v rtl8821ae ant_sel=1
```

Jika telah berhasil, (misal dengan `ant_sel=2`), buat perintah agar menjadi permanen.

```
echo "options rtl8821ae ant_sel=2" | sudo tee /etc/modprobe.d/50-rtl8821ae.conf
```
### Notes
* Ubah nilai `ant_sel` sesuai antena yang kuat.
* Update sistem operasi dapat menghilangkan konfigurasi. Untuk itu, buat Bash script (tanpa baris `git`) untuk dijalankan setelah update sistem operasi dijalankan.
* Pada beberapa kasus, Wi-Fi tidak bisa digunakan di saat bluetooth aktif.

---
lang: id-ID
layout: wiki
section: twilightmenu
category: installing
title: Pemasangan (3DS)
long_title: Pemasangan TWiLight Menu++ (3DS)
description: Cara memasang TWiLight Menu++ pada Nintendo 3DS
tabs:
  - 
    working-camera: Dengan kamera
    non-working-camera: Tanpa kamera
    manual: Urus sendiri
---

Sebelumnya harus punya *custom firmware* di 3DS, ikuti [3ds.hacks.guide](https://3ds.hacks.guide) untuk memasangnya
{:.alert .alert-info}

{% capture tab-working-camera %}
1. Buka FBI dan pilih `Remote Install`, lalu `Scan QR Code`
1. Pindai kode QR berikut untuk memasang [Universal-Updater](https://github.com/Universal-Team/Universal-Updater) versi terkini<br> ![Kode QR Universal-Updater](https://db.universal-team.net/assets/images/qr/universal-updater-cia.png)
1. Tutup FBI dan luncurkan Universal-Updater
    - Jika tidak muncul di HOME Menu, nyalakan ulang 3DS
1. Cari TWiLight Menu++ di kisi layar aplikasi, gunakan tab ketiga pada bilah sisi jika kesusahan mencari
    - Ikon seperti ini: ![Ikon TWiLight Menu++](https://raw.githubusercontent.com/DS-Homebrew/TWiLightMenu/master/booter/icon.bmp)
1. Tekan <kbd class="face">A</kbd> atau ketuk ikon unduh di bilah sisi dan pilih `TWiLight Menu++` untuk memasangnya
    - Ini akan lumayan lama
    - Jika gagal memasang, pastikan konsol sudah tersambung internet. Jika tidak, pencet tab `Urus sendiri`
{% endcapture %}
{% assign tab-working-camera = tab-working-camera | split: "////////" %}

{% capture tab-non-working-camera %}
1. Unduh [`Universal-Updater.cia`](https://github.com/Universal-Team/Universal-Updater/releases/latest/download/Universal-Updater.cia) yang terkini
1. Taruh berkas `Universal-Updater.cia` di mana saja di kartu SD
1. Luncurkan FBI di Nintendo 3DS
1. Saat di FBI, masuk ke tempat ditaruhnya berkas `Universal-Updater.cia`
1. Pilih berkas `Universal-Updater.cia` dan tekan "Install & Delete"
1. Tutup FBI dan luncurkan Universal-Updater
    - Jika tidak muncul di HOME Menu, nyalakan ulang 3DS
1. Cari TWiLight Menu++ di kisi layar aplikasi, gunakan tab ketiga pada bilah sisi jika kesusahan mencari
    - Ikon seperti ini: ![Ikon TWiLight Menu++](https://raw.githubusercontent.com/DS-Homebrew/TWiLightMenu/master/booter/icon.bmp)
1. Tekan <kbd class="face">A</kbd> atau ketuk ikon unduh di bilah sisi dan pilih `TWiLight Menu++` untuk memasangnya
    - Ini akan lumayan lama
    - Jika gagal memasang, pastikan konsol sudah tersambung internet. Jika tidak, pencet tab `Urus sendiri`
{% endcapture %}
{% assign tab-non-working-camera = tab-non-working-camera | split: "////////" %}

{% capture tab-manual %}
1. Unduh [`TWiLightMenu-3DS.7z`](https://github.com/DS-Homebrew/TWiLightMenu/releases/latest/download/TWiLightMenu-3DS.7z) yang terkini
    - Jika tidak terunduh, buka [laman *release*](https://github.com/DS-Homebrew/TWiLightMenu/releases/latest)
1. Ekstrak `TWiLightMenu-3DS.7z`
1. Salin folder `_nds` ke akar kartu SD
1. Salin berkas `BOOT.NDS` ke akar kartu SD
1. Salin folder `roms` ke akar kartu SD
1. Salin berkas `.cia` ke akar kartu SD
1. Di konsol 3DS, pasang CIA tadi dengan FBI
{% endcapture %}
{% assign tab-manual = tab-manual | split: "////////" %}

### Pemasangan

{% assign tabs = tab-working-camera | concat: tab-non-working-camera | concat: tab-manual %}
{% include tabs.html index=0 tabs=tabs %}

### Mengakses isi *flashcart*

*Flashcart* adalah perangkat dengan lubang microSD yang disisipkan ke slot kartrid. Jika tidak punya *flashcart*, panduan ini selesai di sini.
{:.alert .alert-warning}

#### Jika punya R4(i) Ultra

1. Ikuti [panduan ini](installing-flashcard) mulai dari `Memuat permainan lewat kernel flashcart`
    - Peringatan yang ada boleh diabaikan
1. Buka Pengaturan TWLMenu++
1. Pindah ke halaman `Pengaturan lain`
1. Nyalakan `Akses microSD Slot-1`
1. Keluar dari Pengaturan TWLMenu++ dengan tombol `B`
    - Jika masuk ke Menu DS Klasik, tekan `B` lagi

#### Jika tidak punya R4(i) Ultra

1. Buat berkas atau folder bernama `primary` di `sd:/_nds/` (bukan di *flashcart*), ini agar TWiLight Menu++ pada *flashcart* membaca pengaturan dari kartu SD konsol
1. Ikuti [panduan ini](installing-flashcard) mulai dari `Memuat langsung TWiLight Menu++`
1. Salin berkas `BOOT.NDS` dari `TWiLightMenu-Flashcard.7z` ke akar kartu microSD *flashcart*
1. Buka Pengaturan TWLMenu++
1. Pindah ke halaman `Pengaturan lain`
1. Nyalakan `Akses SD di Slot-1`
1. Nyalakan `Akses SCFG di Slot-1`
1. Nyalakan `Langsung mulai Slot-1`
1. Keluar dari Pengaturan TWLMenu++ dengan tombol `B`
    - Jika masuk ke Menu DS Klasik, luncurkan *flashcart*
    - Jika tidak, mulai ulang TWiLight Menu++

#### Beralih ke kartu SD konsol atau *flashcart*
- Tekan `SELECT`+`Atas` atau `SELECT`+`Bawah` untuk ke isi kartu SD konsol atau *flashcart*
    - Jika menu SELECT diaktifkan, boleh dilakukan dari situ
    - Jika menggunakan tema 3DS, sentuh ikon Kartrid/Kartu SD
    - Jika menggunakan tema Wood, R4, atau GBC; tekan tombol `R`

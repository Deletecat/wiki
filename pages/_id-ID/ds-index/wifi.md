---
lang: id-ID
layout: wiki
section: ds-index
category: reference
title: Wi-Fi
description: Informasi penggunaan Wi-Fi di Nintendo DS
---

- Di aplikasi Nintendo DS, hanya bisa disambung ke Wi-Fi keamanan WEP atau *Open*
- Di aplikasi Nintendo DSi-*Enhanced/Exclusive* saat di Mode DSi, bisa disambung ke Wi-Fi keamanan WPA dan WPA2
- Jika di konsol DSi atau 3DS, pastikan persetujuan jejaring internet disetujui

*Hotspot* juga bisa digunakan, jadi tidak usah mengubah setelan perute.

### Membuat *hotspot*
Di GBAtemp terdapat panduan membuat *hotspot* kompatibel untuk DS lewat komputer macOS dan Linux.
- [macOS](https://gbatemp.net/threads/571658)
- [Linux](https://gbatemp.net/threads/543283)

Untuk di Android, keamanan *hotspot* harus diatur ke *Open* (tanpa sandi).

Windows tidak bisa membuat *hotspot* kompatibel, jadi pengguna Windows harus ke Linux untuk menyiapkannya.
#### Metode lain
Jika tidak bisa membuat *hotspot* kompatibel untuk DS dengan metode di atas, coba metode lain berikut ini.
- Nintendo Wi-Fi USB Connector
    - Walaupun masih bisa digunakan, ini sangat tidak dianjurkan karena perlu Windows XP atau Vista versi 32-bit
    - Untuk informasi cara mengatur Nintendo Wi-Fi USB Connector, baca Bagian 3 laman [Wiimmfi Guide](https://docs.google.com/document/d/1f3PChwQig40UaiPXlh-Gi5CggGiBPzyrpiecLZlT8ZE/edit?usp=sharing) ini oleh anggota [Mario Kart DS Network](https://discord.gg/pa9bea6)
- Mengubah pengaturan perute agar kompatibel untuk DS
    - Cara ini tidak dianjurkan karena jejaring akan terbuka dan mudah disusup, bahkan dengan WEP. Ini juga bisa bermasalah untuk pengguna jejaring tersebut. Jika cara ini tetap dilakukan, gunakan perute cadangan atau jejaringan tamu, jika ada
    - Tidak semua perute mendukung jejaringan tamu atau tanpa keamanan
- *Wi-Fi extenders* (peluas Wi-Fi)

#### Pengaturan
Jika ingin mengatur jejaring agar kompatibel untuk DS, harus sesuai spesifikasi berikut:
- Keamanan WEP atau *Open* (tanpa sandi)
- Frekuensi nirkabel 2,4 GHz
- Mode nirkabel 802.11b
    - Yang ini mungkin ada di "*Legacy mode*" atau sejenisnya

### Memulihkan Nintendo DS WFC
1. Masuk ke Nintendo Wi-Fi Connection Setup
1. Sambungkan ke titik akses
1. Atur nilai *Primary DNS* ke salah satu nilai di bawah ini, sesuai layanan yang ingin digunakan:
    - **[Wiimmfi](https://wiimmfi.de)** - `178.62.43.212`
    - **[AltWFC/WFCZwei](https://save-nintendo-wifi.com/) ([daftar pemain daring](http://zwei.moe:9001))** - `172.104.88.237`
1. Atur `1.1.1.1` sebagai *secondary DNS*
1. Mungkin ROM juga perlu ditambal NoSSL, tergantung permainan

### Menambal sendiri ROM DS
Ikuti panduan di bawah ini jika ISP Wi-Fi memblokir server DNS kustom, jika tidak, *disarankan* ikuti saja panduan di atas.

- Pengguna GNU/Linux dan macOS boleh mengikuti arahan serupa, tapi harus dengan Mono
- WfcPatcher saat ini belum bisa untuk DSiWare

1. Unduh [WfcPatcher](https://github.com/AdmiralCurtiss/WfcPatcher/releases)
1. Salin ROM yang ingin ditambal ke folder tempat WfcPatcher diunduh dan buka foldernya
1. Buat berkas teks
1. Buka berkasnya, tulis `wfcpatcher.exe %1 --domain wiimmfi.de` lalu simpan dengan nama `patch.bat` dan tutup jendelanya
    - Tulisan `wiimmfi.de` boleh diganti URL lain, jika ingin menggunakan server lain
    - Jika berkas masih dianggap dokumen teks, [aktifkan ekstensi berkas](https://dsi.cfw.guide/file-extensions-%28windows%29) dan hapus `.txt` dari nama berkas
1. Sekarang seret semua ROM yang ingin ditambal ke patch.bat
1. Selesai! ROM yang sudah ditambal akan ada akhiran (wiimmfi)

Jangan lupa hapus DNS kustom jika masih ada di pengaturan Wi-Fi sebelum menyambung ke internet dengan ROM yang ditambal.

### Sidik gangguan dan bacaan lanjut
Jika muncul galat, ketik kode galatnya di [penyidik gangguan](https://wiimmfi.de/error) Wiimmfi untuk cara mengatasinya.

Untuk sidik gangguan spesifik dan informasi lanjut, seperti cara menyambung internet di emulator atau dengan Nintendo Wi-Fi USB Connector, baca laman [Wiimmfi Guide](https://docs.google.com/document/d/1f3PChwQig40UaiPXlh-Gi5CggGiBPzyrpiecLZlT8ZE/edit?usp=sharing) ini oleh anggota [Mario Kart DS Network](https://discord.gg/pa9bea6).

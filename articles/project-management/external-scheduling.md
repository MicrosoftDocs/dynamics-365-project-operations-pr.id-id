---
title: Penjadwalan eksternal
description: Artikel ini menyediakan informasi tentang penjadwalan eksternal.
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736987"
---
# <a name="external-scheduling"></a>Penjadwalan eksternal

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Mode penjadwalan eksternal memungkinkan Anda membuat, memperbarui, dan menghapus entitas asli yang terkait dengan struktur perincian kerja (WBS), namun tanpa batas saat ini yang dijalankan oleh Microsoft Project for the Web. Validasi terbatas juga tersedia. Mode ini harus digunakan hanya oleh pelanggan berikut:

- Pelanggan yang memiliki alat yang diperlukan untuk menentukan WBS di luar logika penjadwalan yang diberikan oleh Project Operations
- Pelanggan yang harus mengelola hierarki jadwal, dependensi, atau durasi tugas

> [!IMPORTANT]
> Data yang tidak dimasukkan dengan benar di entitas yang terkait dengan WBS mungkin tidak dirender di kisi rekonsiliasi sumber daya, kisi estimasi, kisi pelacakan, atau kisi penugasan sumber daya.

## <a name="configuration"></a>Konfigurasi

Fitur ini diaktifkan secara default. Akan tetapi, pada halaman utama yang dapat digunakan untuk proyek, bidang terkait tidak dapat dilihat secara default. Untuk mengaktifkan bidang, di Maker Portal, buka halaman utama untuk entitas proyek, pilih bidang **Mesin Penjadwalan**, lalu ubah bidang ke **Terlihat secara Default**. Jika Anda tidak menggunakan halaman utama proyek out-of-box, edit halaman yang ada, dan tambahkan kolom **Mesin Penjadwalan** ke dalamnya.

## <a name="settings"></a>Pengaturan

Untuk menggunakan mode penjadwalan eksternal, Anda harus membuat proyek baru terlebih dahulu dan memilih mesin penjadwalan **Terjadwal Eksternal** dalam daftar drop-down pada halaman utama proyek. Setelah mode ini dibuat untuk proyek, mode tidak dapat diubah.

## <a name="viewing-the-wbs"></a>Melihat WBS

Jika proyek dijadwalkan secara eksternal, akses ke Project for the Web dibatasi untuk proyek tersebut. Untuk melihat WBS, Anda harus membuka kisi pelacakan, tempat WBS lengkap ditampilkan.

## <a name="creating-and-editing-the-wbs"></a>Membuat dan mengedit WBS

Jika penjadwalan eksternal diaktifkan untuk proyek, Anda harus mendefinisikan data untuk semua entitas terkait WBS, termasuk tugas, anggota tim, penugasan sumber daya, dan dependensi.

Ilustrasi berikut menampilkan model data untuk perencanaan proyek.

![Model data perencanaan proyek.](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>Batasan fungsional

Operasi berikut tidak diizinkan pada proyek terjadwal eksternal.

### <a name="project-planning"></a>Perencanaan proyek

- **Salin proyek** – Operasi ini tidak didukung pada proyek terjadwal eksternal.
- **Pindahkan proyek** – Perubahan pada tanggal mulai proyek tidak akan memindahkan awal tugas atau penugasan sumber daya di WBS.
- **Memperbarui Manajer Proyek** – Perubahan untuk manajer proyek pada halaman utama proyek tidak akan secara otomatis membuat anggota tim proyek baru hingga proyek dikonversi.
- **Memperbarui template jam kerja proyek** – Perubahan pada template jam kerja proyek tidak akan menghitung ulang jadwal proyek.
- **Kontur Penugasan Sumber Daya** – Pembuatan penugasan sumber daya tidak akan secara otomatis memperbarui bidang **mdyn\_PlannedWork**. Bidang ini digunakan untuk menyimpan kontur untuk upaya penugasan sumber daya. Jika Anda menunjukkan upaya fase waktu dalam kisi penugasan sumber daya atau kisi rekonsiliasi sumber daya, Anda harus menentukan kontur penugasan sumber daya. Konstur ini harus diformat dengan benar sehingga memicu perhitungan kontur biaya dan kontur harga penjualan. Sebaiknya buat proyek uji yang dijadwalkan oleh Project for the Web, lalu tinjau data terkait untuk mengonfirmasi persyaratan dan pemformatan.

### <a name="resource-management"></a>Manajemen sumber daya

- **Terpenuhinya sumber daya generik** – Terpenuhinya sumber daya generik tidak didukung untuk proyek terjadwal eksternal. Upaya memenuhi persyaratan terbuka aktif akan membuat anggota tim proyek baru, namun tidak akan menghapus anggota tim generik atau mengganti anggota tim generik pada penugasan sumber daya yang ada.
- **Menghapus Anggota Tim** – Penghapusan anggota tim tidak akan secara otomatis menghapus penugasan sumber daya.

### <a name="quoting-and-contracting"></a>Kuotasi dan kontrak

- **Mengimpor rincian Baris Kuotasi dan Baris Kontrak** – Bila rincian kuotasi atau baris kontrak diimpor dari proyek, aplikasi ini telah diuji untuk mendukung maksimum hanya 500 tugas di WBA, berdasarkan batas 20 penugasan per tugas.

### <a name="actuals-and-invoicing"></a>Aktual dan faktur

- Meskipun tidak ada perubahan pada validasi yang ada antara WBS dan transaksi keuangan, Anda harus menyesuaikan diri dengan model data siap kerja out-of-box, untuk memastikan semua transaksi hilir berjalan sesuai harapan.

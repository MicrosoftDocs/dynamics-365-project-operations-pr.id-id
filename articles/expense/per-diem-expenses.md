---
title: Pengeluaran uang saku
description: Artikel ini memberikan informasi tentang bagaimana bekerja dengan pengeluaran uang saku.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923192"
---
# <a name="per-diem-expenses"></a>Pengeluaran uang saku

> [!IMPORTANT] 
> Fungsi yang dideskripsikan dalam artikel ini tersedia untuk pengguna yang ditargetkan sebagai bagian dari rilis pratinjau.

Pembayaran per diem adalah penyisihan harian tetap yang ditetapkan sebelumnya yang harus dibayar perusahaan kepada karyawannya untuk tempat tinggal (hotel), makan dan pengeluaran tak terduga yang dikeluarkan karyawan saat mereka melakukan perjalanan kerja. Perusahaan membayar biaya tambahan ini kepada karyawan daripada membayar biaya perjalanan yang sebenarnya. Karyawan dapat menggunakan penyisihan uang saku **insidental/lainnya** untuk mencakup tips, layanan kamar, layanan laundry, atau cuci kering muntuk pertemuan bisnis yang penting. Tarif uang saku dapat berbeda, tergantung apakah pemberi kerja memilih untuk mengganti biaya gabungan tempat tinggal dan makan, atau hanya untuk biaya makan dan insidental.

Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya. Saat membuat aturan uang saku, Anda dapat menentukan bahwa persentase tingkat uang saku diabaikan jika karyawan menerima makanan, atau layanan gratis. Anda juga dapat menetapkan jumlah jam minimum dan maksimum yang dapat diterapkan dalam tarif uang saku untuk diterapkan pada perjalanan pekerja.

Uang saku dihitung sebagai total alokasi yang ditawarkan per hari dikurangi pengurangan makan (biaya makan gratis) yang diberikan kepada karyawan.

## <a name="configure-per-diems"></a>Mengkonfigurasi uang saku

Untuk mengkonfigurasi pengeluaran uang saku, ikuti langkah berikut.

1. Buka parameter **manajemen Pengeluaran** \> **Konfigurasi** \> **Umum** \> **manajemen Pengeluaran Umum**.
2. Pada tab **uang saku**, dalam bidang **hitung pengurangan makan**, pilih cara menghitung per uang saku:

    - **Jenis makan per perjalanan** – Hitung uang saku berdasarkan jenis makan yang dimasukkan (makan pagi, makan siang, atau makan malam) dan pada pengurangan makan malam yang ditentukan untuk setiap jenis makan untuk uang saku selama durasi perjalanan.
    - **Jenis makan per hari** – Hitung uang saku berdasarkan jenis makan yang dimasukkan (makan pagi, makan siang, atau makan malam) dan pada pengurangan makan malam yang ditentukan untuk setiap jenis makan untuk uang saku per hari.
    - **Jumlah makan per hari** – Menghitung uang saku berdasarkan jumlah makan yang dimasukkan per hari dan pengurangan makan untuk jumlah makan yang disediakan setiap hari.

3. Buka **Manajemen pengeluaran** \> **konfigurasi** \> **Perhitungan dan kode** \> **lokasi uang saku**.
4. Tambahkan lokasi dengan uang saku dapat digunakan.
5. Untuk setiap lokasi yang ditambahkan, di tab **Uang saku**, pilih tingkat uang saku dan mata uang yang berlaku antara tanggal mulai dan berakhir tertentu untuk akomodasi, makan, dan biaya lainnya. Untuk mengonfigurasikan tarif uang saku dan mata uang, buka **Manajemen pengeluaran** \> **konfigurasi** \> **Perhitungan dan kode** \> **uang saku**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Uang saku di antarmuka pengeluaran konsep ulang

Fitur uang saku didukung dalam ruang kerja **Manajemen Pengeluaran** konsep ulang di Microsoft Dynamics 365 Finance versi 10.0.25 dan versi lebih baru.

Untuk mengaktifkan uang saku, ikuti langkah-langkah berikut.

1. Di ruang kerja **Manajemen Fitur**, cari dan pilih fitur **Laporan Pengeluaran Konsep Ulang** dalam daftar, lalu pilih **Aktifkan sekarang**.
2. Cari dan pilih fitur **Uang saku untuk antarmuka Laporan Pengeluaran Konsep Ulang** dalam daftar, lalu pilih **Aktifkan sekarang**.

## <a name="how-the-feature-works"></a>Cara kerja fitur

Bagian ini memberikan contoh untuk tiga skenario konfigurasi. Untuk setiap contoh, bidang **Hitung pengurangan makan berdasarkan** diatur ke nilai yang berbeda. Untuk ketiga contoh, jumlah total yang harus dibayar adalah sama hingga pengurangan makan diterapkan. Setelah poin tersebut, jumlah total untuk setiap contoh berbeda.

Untuk membuat pengeluaran uang saku yang digunakan untuk ketiga contoh, ikuti langkah-langkah berikut.

1. Buka **Ruang kerja** \> **Manajemen pengeluaran**.
2. Pilih **laporan pengeluaran baru**, atau pilih laporan pengeluaran yang ada.
3. Tambah pengeluaran baru. Pada bidang **Kategori**, pilih **Uang saku**. Pilih lokasi, serta tanggal mulai dan berakhir perjalanan Anda. Uang saku untuk tempat tinggal, makan, dan insidental (pengeluaran lain) dihitung berdasarkan alokasi harian yang ditetapkan untuk lokasi yang dipilih.

    Misalnya, Anda memilih **Redmond (AS)** sebagai lokasi. Alokasi harian untuk lokasi tersebut adalah 150 dolar AS (USD 150) untuk tempat tinggal, USD 75 untuk makan siang, USD 5 untuk insiden insidental. Tanggal mulai adalah 10 Januari dan tanggal berakhir adalah 14 Januari. Oleh karena itu, durasi yang dipilih adalah lima hari saat konfigurasi yang dipilih adalah hari kalender bersamaan dengan waktu, serta waktu yang dipilih dimulai dan berakhir pukul 12.00 pada tanggal mulai dan berakhir. Berikut adalah perhitungannya:

    - Jumlah total dibayar = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
    - Bagian dari makan dan tak terduga dari total jumlah = 5 × (75 + 5) = USD 400

Jika makan pagi, makan siang, dan makan malam disediakan selama perjalanan, maka makan siang dan makan malam harus diperhitungkan sebagai pengurangan makan malam.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Contoh 1: uang saku dengan pengurangan makan berdasarkan jenis makan per perjalanan

Di contoh ini, pengurangan makan malam adalah 30 persen untuk makan pagi, 30 persen untuk makan siang, dan 40 persen untuk makan malam. Pada halaman **Parameter manajemen pengeluaran**, bidang **Hitung pengurangan makan berdasarkan** diatur ke **jenis Makan per perjalanan**. Berikut adalah perhitungan jika tiga kali makan pagi, dua makan siang, dan nol makan malam diberikan kepada karyawan:

- Pengurangan makan = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112,50
- Makan dan insidental = 400 – 112,50 = USD 287,50
- Jumlah total biaya dibayar = Total alokasi – Pengurangan makan = 1.150 – 112.50 = USD 1037,50

![Pengeluaran Uang saku dengan pengurangan makan berdasarkan jenis makan per perjalanan.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Contoh 2: uang saku dengan pengurangan makan berdasarkan jenis makan per hari

Di contoh ini, pengurangan makan malam adalah 30 persen untuk makan pagi, 30 persen untuk makan siang, dan 40 persen untuk makan malam. Pada halaman **Parameter manajemen pengeluaran**, bidang **Hitung pengurangan makan berdasarkan** diatur ke **jenis Makan per hari**. Dalam kasus ini, dalam kisi **Makan** di kotak dialog **Edit pengeluaran**, Anda mengosongkan kotak centang untuk menunjukkan makan yang diberikan kepada Anda selama perjalanan.

Misalnya, berikut adalah perhitungan jika makan pagi disediakan untuk tiga hari pertama perjalanan:

- Pengurangan makan harian untuk setiap tiga hari pertama = 75 × 30% = USD 22,50
- Total pengurangan makan = 3 × 22,50 = USD 67,50
- Makan dan insidental selama hari 1 hingga 3 = 75 – 22,50 = USD 57,50
- Total makan dan insidental = Jumlah makan dan insidental selama lima hari = 400 – 67,50 = USD 332,50
- Jumlah total biaya dibayar = Total jumlah – Pengurangan makan = 1.150 – 67,50 = USD 1.082,50

![Pengeluaran Uang saku dengan pengurangan makan berdasarkan jenis makan per hari.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Contoh 3: uang saku dengan pengurangan makan berdasarkan jumlah makan per hari

Dalam contoh ini, pengurangan makan dihitung berdasarkan jumlah makan yang disediakan per hari (misalnya, bidang **Hitung pengurangan makan berdasarkan** pada halaman **Parameter manajemen Pengeluaran** diatur ke **Jumlah makan per hari**). Dalam kisi **Makan** di kotak dialog **Edit pengeluaran**, Anda mengosongkan kotak centang untuk menunjukkan makan yang diberikan.
Dalam hal ini, pengurangan makan hanya didasarkan pada # makan yang disediakan, dan tidak pada jenis makan (Pagi/makan siang/makan malam) yang disediakan.

Berikut adalah perhitungan untuk uang saku ketika alokasi harian adalah USD 150 untuk akomodasi, USD 75 untuk makan, dan USD 5 untuk insidental:

- **Jumlah total dibayar** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
- **Satu makan:** Pengurangan makan = 20% = USD 15
- **Dua makan:** Pengurangan makan = 50% = USD 37.50
- **Tiga makan:** Pengurangan makan = 100% = USD 75

Berikut adalah perhitungan untuk **alokasi makan dan insidental**, yaitu mencakup USD 5 untuk insidental:

- Hari 1 - Dua kali makan disediakan = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Hari 2 - Dua kali makan disediakan = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Hari 3 - Satu makan disediakan = (75 – 15) + 5 = 60 + 5 = USD 65
- Hari 4 - Nol kali makan disediakan = (75 – 0) + 5 = 75 + 5 = USD 80
- Hari 5 - Tiga kali makan disediakan = (75 – 75) + 5 = 0 + 5 = USD 5

- Total makan dan biaya tak terduga = Makan dan Insidental untuk Hari 1+ Hari 2 +Hari 3+Hari 4+ Hari 5 = USD 235
- Pengurangan total makan = Pengurangan makan untuk Hari 1+ Hari 2 +Hari 3+Hari 4+ Hari 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Jumlah total biaya dibayar = Total alokasi – Total Pengurangan makan = USD 1.150 – USD 165 = USD 985

![Pengeluaran Uang saku dengan pengurangan makan berdasarkan jumlah makan per hari.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Mulai dari Finance versi 10.0.23, jika Anda menggunakan antarmuka pengeluaran konsep ulang, Anda tidak dapat membuat pengeluaran uang saku yang memiliki tanggal tumpang tindih. Jika mencobanya, Anda akan menerima pesan kesalahan.

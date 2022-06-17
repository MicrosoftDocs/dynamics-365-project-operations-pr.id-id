---
title: Pengeluaran uang saku
description: Artikel ini memberikan informasi tentang cara bekerja dengan biaya per diem.
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
> Fungsionalitas yang dijelaskan dalam artikel ini tersedia untuk pengguna yang ditargetkan sebagai bagian dari rilis pratinjau.

Pembayaran per diem adalah tunjangan harian tetap yang telah ditentukan yang dibayarkan perusahaan kepada karyawannya untuk penginapan (hotel), makanan, dan biaya insidental yang dikeluarkan karyawan tersebut saat mereka bepergian untuk bekerja. Perusahaan membayar tunjangan ini kepada karyawan alih-alih membayar biaya perjalanan yang sebenarnya. Karyawan dapat menggunakan tunjangan Insidental/Lainnya **per diem untuk** mencakup tip, layanan kamar, binatu, atau layanan dry-cleaning untuk pertemuan bisnis penting. Tarif per diem dapat bervariasi, tergantung pada apakah majikan memilih untuk mengganti biaya gabungan penginapan dan makanan, atau hanya untuk biaya makan dan insidental.

Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya. Saat Anda membuat aturan per diem, Anda dapat menentukan bahwa persentase dari tarif per diem akan ditahan jika seorang karyawan menerima makanan atau layanan gratis. Anda juga dapat mengatur jumlah jam minimum dan jumlah jam maksimum yang dapat diterapkan pada tarif per diem untuk perjalanan karyawan.

Per diem dihitung sebagai total tunjangan yang ditawarkan per hari dikurangi pengurangan makanan (biaya makan gratis) yang diberikan kepada karyawan.

## <a name="configure-per-diems"></a>Mengonfigurasi per diem

Untuk mengonfigurasi biaya per diem, ikuti langkah-langkah berikut.

1. Buka **Manajemen** \> **biaya Pengaturan** \> **Parameter** manajemen pengeluaran umum.\>**·**
2. Pada tab **Per diem**, di **bidang Hitung pengurangan makanan menurut**, pilih bagaimana per diem harus dihitung:

    - **Jenis makanan per perjalanan** – Hitung per diem berdasarkan jenis makanan yang dimasukkan (sarapan, makan siang, atau makan malam) dan pada pengurangan makanan yang ditentukan untuk setiap jenis makanan untuk tunjangan per diem selama perjalanan.
    - **Jenis makanan per hari** – Hitung per diem berdasarkan jenis makanan yang dimasukkan dan pada pengurangan makanan yang ditentukan untuk setiap jenis makanan untuk tunjangan per diem per hari.
    - **Jumlah makanan per hari** – Hitung per diem berdasarkan jumlah makanan yang dimasukkan per hari dan pengurangan makanan untuk jumlah makanan yang disediakan setiap hari.

3. Buka **Perhitungan dan kode** \> **Penyiapan** \> **manajemen** \> **pengeluaran Per lokasi** diem.
4. Tambahkan lokasi di mana per diem dapat digunakan.
5. Untuk setiap lokasi yang Anda tambahkan, pada **tab Per diem, pilih kurs** per diem dan mata uang yang berlaku antara tanggal mulai dan berakhir tertentu untuk penginapan, makan, dan pengeluaran lainnya. Untuk mengonfigurasi tarif dan mata uang per diem, buka **Perhitungan dan kode** \> **Penyiapan** \> **manajemen** \> **pengeluaran Per diem.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Per diem di antarmuka pengeluaran yang dirancang ulang

Fitur per diem didukung di ruang kerja Manajemen **Pengeluaran yang dirancang** ulang di Microsoft Dynamics 365 Finance versi 10.0.25 dan yang lebih baru.

Untuk mengaktifkan per diem, ikuti langkah-langkah berikut.

1. Di ruang **kerja Manajemen** Fitur, temukan dan pilih **fitur Rencana Pengeluaran yang Dirancang** Ulang laporan dalam daftar, lalu pilih **Aktifkan sekarang**.
2. Temukan dan pilih **fitur antarmuka** yang dibayangkan ulang laporan per-diem untuk pengeluaran dalam daftar, lalu pilih **Aktifkan sekarang**.

## <a name="how-the-feature-works"></a>Cara kerja fitur ini

Bagian ini menyediakan contoh untuk tiga skenario konfigurasi. Untuk setiap contoh, **bidang Hitung pengurangan makanan menurut** diatur ke nilai yang berbeda. Untuk ketiga contoh tersebut, jumlah total yang harus dibayarkan adalah sama sampai pengurangan makanan diterapkan. Setelah titik itu, jumlah total yang harus dibayarkan berbeda untuk setiap contoh.

Untuk membuat biaya per diem yang digunakan untuk ketiga contoh, ikuti langkah-langkah berikut.

1. Buka **Manajemen Pengeluaran Ruang Kerja** \> **.**
2. Pilih **Laporan pengeluaran baru**, atau pilih laporan pengeluaran yang sudah ada.
3. Tambahkan biaya baru. Di **bidang Kategori**, pilih **Per diem**. Pilih lokasi, serta tanggal mulai dan berakhir perjalanan Anda. Per diem untuk penginapan, makan, dan insidental (biaya lainnya) dihitung berdasarkan tunjangan harian yang ditetapkan untuk lokasi yang dipilih.

    Misalnya, Anda memilih **Redmond (AS)** sebagai lokasi. Tunjangan harian untuk lokasi itu adalah 150 dolar AS (USD 150) untuk penginapan, USD 75 untuk makan, dan USD 5 untuk insidental. Tanggal mulainya adalah 10 Januari, dan tanggal akhir adalah 14 Januari. Oleh karena itu, durasi yang dipilih adalah lima hari ketika konfigurasi yang dipilih adalah hari kalender dengan waktu, dan waktu yang dipilih dimulai dan berakhir pada pukul 12:00 pagi pada tanggal mulai dan berakhir. Berikut perhitungannya:

    - Jumlah total yang harus dibayar = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Porsi makanan dan insidental dari jumlah total = 5 × (75 + 5) = USD 400

Jika sarapan, makan siang, dan makan malam disediakan selama perjalanan, makanan tersebut harus diperhitungkan sebagai pengurangan makanan.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Contoh 1: Per diem di mana pengurangan makanan didasarkan pada jenis makanan per perjalanan

Dalam contoh ini, pengurangan makanan adalah 30 persen untuk sarapan, 30 persen untuk makan siang, dan 40 persen untuk makan malam. **Pada halaman Parameter** manajemen pengeluaran, **bidang Hitung pengurangan makanan menurut** diatur ke **Jenis makanan per perjalanan**. Berikut adalah perhitungan jika tiga sarapan, dua makan siang, dan nol makan malam diberikan kepada karyawan:

- Pengurangan makanan = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Makanan dan insidental = 400 – 112,50 = USD 287.50
- Jumlah total yang harus dibayarkan = Total tunjangan – Pengurangan makanan = 1.150 – 112,50 = USD 1,037.50

![Biaya per diem di mana pengurangan makanan didasarkan pada jenis makanan per perjalanan.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Contoh 2: Per diem di mana pengurangan makanan didasarkan pada jenis makanan per hari

Dalam contoh ini, pengurangan makanan adalah 30 persen untuk sarapan, 30 persen untuk makan siang, dan 40 persen untuk makan malam. **Pada halaman Parameter** manajemen pengeluaran, **bidang Hitung pengurangan makanan menurut** diatur ke **Jenis makanan per hari**. Dalam hal ini, dalam **kisi Makanan** dalam **kotak dialog Edit pengeluaran**, Anda mengosongkan kotak centang untuk menunjukkan makanan mana yang diberikan kepada Anda selama perjalanan Anda.

Misalnya, berikut adalah perhitungan jika sarapan disediakan selama tiga hari pertama perjalanan:

- Pengurangan makan harian untuk masing-masing dari tiga hari pertama = 75 × 30% = USD 22.50
- Total pengurangan makanan = 3 × 22,50 = USD 67.50
- Makanan dan insidental untuk hari ke-1 sampai 3 = 75 – 22,50 = USD 57.50
- Total makanan dan insidental = Jumlah makanan dan insidental selama lima hari = 400 – 67,50 = USD 332.50
- Jumlah total yang harus dibayarkan = Jumlah total – Pengurangan makanan = 1.150 – 67,50 = USD 1,082.50

![Biaya per diem dimana pengurangan makanan didasarkan pada jenis makanan per hari.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Contoh 3: Per diem di mana pengurangan makanan didasarkan pada jumlah makanan per hari

Dalam contoh ini, pengurangan makanan dihitung berdasarkan jumlah makanan yang disediakan per hari (yaitu, **hitung pengurangan makanan berdasarkan** bidang pada **halaman Parameter** manajemen pengeluaran diatur ke **Jumlah makanan per hari**). **Dalam kisi Makanan** dalam kotak **dialog Edit pengeluaran**, Anda mengosongkan kotak centang untuk menunjukkan makanan mana yang disediakan.
Dalam hal ini, pengurangan makanan hanya didasarkan pada # makanan yang disediakan, dan bukan pada jenis makanan ( Sarapan / makan siang / makan malam) yang disediakan.

Berikut adalah perhitungan untuk per diem ketika tunjangan harian USD 150 untuk penginapan, USD 75 untuk makan, dan USD 5 untuk insidental:

- **Jumlah total yang harus** dibayarkan = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Satu kali makan:** Pengurangan makan = 20% = USD 15
- **Dua kali makan:** Pengurangan makanan = 50% = USD 37.50
- **Tiga kali makan:** Pengurangan makan = 100% = USD 75

Berikut adalah perhitungan untuk **makanan dan tunjangan** insidental, yang mencakup USD 5 untuk insidental:

- Hari 1 - Dua kali makan disediakan = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- Hari 2 - Dua kali makan disediakan = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- Hari 3 - Satu kali makan disediakan = (75 – 15) + 5 = 60 + 5 = USD 65
- Hari 4 - Nol makanan yang disediakan = (75-0) + 5 = 75 + 5 = USD 80
- Hari 5 - Tiga kali makan disediakan = (75 – 75) + 5 = 0 + 5 = USD 5

- Total makanan dan insidental = Makanan dan Insidental untuk Hari 1+ Hari 2 +Hari 3+Hari 4+ Hari 5 = USD 235
- Total pengurangan makanan = Pengurangan makan untuk Hari 1+ Hari 2 +Hari 3+Hari 4+ Hari 5= 37.5+ 37.5+ 15 + 0+ 75 = USD 165
- Jumlah total yang harus dibayarkan = Total tunjangan – Total pengurangan makanan = USD 1,150 - USD 165 = USD 985

![Biaya per diem di mana pengurangan makanan didasarkan pada jumlah makanan per hari.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Pada Finance versi 10.0.23, jika Anda menggunakan antarmuka pengeluaran yang dirancang ulang, Anda tidak dapat membuat pengeluaran per diem yang memiliki tanggal yang tumpang tindih. Jika Anda mencoba, Anda akan menerima pesan kesalahan.

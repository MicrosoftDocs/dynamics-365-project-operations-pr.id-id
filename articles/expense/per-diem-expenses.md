---
title: Biaya per diem
description: Ini topik memberikan informasi tentang cara bekerja dengan biaya per diem.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596054"
---
# <a name="per-diem-expenses"></a>Biaya per diem

> [!IMPORTANT] 
> Fungsionalitas yang dijelaskan dalam topik ini tersedia untuk pengguna yang ditargetkan sebagai bagian dari rilis pratinjau.

Pembayaran per diem adalah tunjangan harian tetap yang telah ditentukan sebelumnya yang dibayarkan perusahaan kepada karyawannya untuk penginapan (hotel), makanan, dan biaya tak terduga yang dikenakan karyawan tersebut saat mereka bepergian untuk bekerja. Perusahaan membayar tunjangan ini kepada karyawan alih-alih membayar biaya perjalanan yang sebenarnya. Karyawan dapat menggunakan biaya tak terduga / **Tunjangan per diem lainnya** untuk menutupi tip, layanan kamar, binatu, atau layanan dry-cleaning untuk pertemuan bisnis penting. Tarif per diem dapat bervariasi, tergantung pada apakah majikan memilih untuk mengganti biaya gabungan penginapan dan makanan, atau hanya untuk biaya makan dan biaya tak terduga.

Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya. Saat Anda membuat aturan per diem, Anda dapat menentukan bahwa persentase dari tarif per diem akan ditahan jika seorang karyawan menerima makanan atau layanan gratis. Anda juga dapat menetapkan jumlah jam minimum dan jumlah jam maksimum yang tarif per diem dapat diterapkan untuk perjalanan karyawan.

Per diem dihitung sebagai total tunjangan yang ditawarkan per hari dikurangi pengurangan makan (biaya makanan gratis) yang diberikan kepada karyawan.

## <a name="configure-per-diems"></a>Konfigurasi per diem

Untuk mengonfigurasi pengeluaran per diem, ikuti langkah-langkah berikut.

1. **Buka Pengaturan manajemen** \> **·** \> **pengeluaran Parameter** manajemen Biaya Umum.\>**·**
2. **Pada tab Per diem**, di **bidang Hitung pengurangan makan menurut**, pilih bagaimana per diem harus dihitung:

    - **Jenis makanan per perjalanan** – Hitung per diem berdasarkan jenis makanan yang dimasukkan (sarapan, makan siang, atau makan malam) dan pada pengurangan makan yang ditentukan untuk setiap jenis makanan untuk tunjangan per diem selama perjalanan.
    - **Jenis makanan per hari** – Hitung per diem berdasarkan jenis makanan yang dimasukkan dan pada pengurangan makan yang ditentukan untuk setiap jenis makanan untuk tunjangan per diem per hari.
    - **Jumlah makanan per hari** – Hitung per diem berdasarkan jumlah makanan yang dimasukkan per hari dan pada pengurangan makan untuk jumlah makanan yang disediakan setiap hari.

3. **Buka Perhitungan Penyiapan** \> **manajemen** \> **pengeluaran dan kode** \> **Lokasi Per diem.**
4. Tambahkan lokasi di mana per diem dapat digunakan.
5. Untuk setiap lokasi yang Anda tambahkan, pada **tab Per diems**, pilih tarif per diem dan mata uang yang berlaku antara tanggal mulai dan akhir tertentu untuk penginapan, makanan, dan biaya lainnya. Untuk mengonfigurasi tarif dan mata uang per diem, buka **Perhitungan Penyiapan** \> **manajemen** \> **pengeluaran dan kode** \> **Per diem.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Per diem dalam antarmuka biaya yang ditata ulang

Fitur per diem didukung di ruang kerja Expense Management **yang** ditata ulang di Microsoft Dynamics 365 Finance versi 10.0.25 dan yang lebih baru.

Untuk mengaktifkan per diem, ikuti langkah-langkah ini.

1. **Di ruang kerja Manajemen** Fitur, temukan dan pilih **fitur Estimasi Laporan Yang Ditata Ulang** dalam daftar, lalu pilih **Aktifkan sekarang**.
2. Temukan dan pilih **fitur antarmuka** per-diem untuk laporan pengeluaran yang dibayangkan ulang dalam daftar, lalu pilih **Aktifkan sekarang**.

## <a name="how-the-feature-works"></a>Cara kerja fitur

Bagian ini memberikan contoh untuk tiga skenario konfigurasi. Untuk setiap contoh, **menghitung pengurangan makan berdasarkan** bidang diatur ke nilai yang berbeda. Untuk ketiga contoh, jumlah total yang harus dibayar adalah sama sampai pengurangan makan diterapkan. Setelah itu, jumlah total yang harus dibayarkan berbeda untuk setiap contoh.

Untuk membuat biaya per diem yang digunakan untuk ketiga contoh tersebut, ikuti langkah-langkah ini.

1. Buka Manajemen Pengeluaran Ruang **Kerja**\>.**·**
2. Pilih **Laporan pengeluaran baru**, atau pilih laporan pengeluaran yang sudah ada.
3. Tambahkan biaya baru. Di **bidang Kategori**, pilih **Per diem**. Pilih lokasi, dan tanggal mulai dan akhir perjalanan Anda. Per diem untuk penginapan, makanan, dan biaya tak terduga (biaya lainnya) dihitung berdasarkan tunjangan harian yang ditetapkan untuk lokasi yang dipilih.

    Misalnya, Anda memilih **Redmond (AS)** sebagai lokasi. Tunjangan harian untuk lokasi itu adalah 150 dolar AS (Rp 150) untuk penginapan, USD 75 untuk makan, dan USD 5 untuk biaya tak terduga. Tanggal mulai adalah 10 Januari, dan tanggal akhirnya adalah 14 Januari. Oleh karena itu, durasi yang dipilih adalah lima hari ketika konfigurasi yang dipilih adalah hari kalender dengan waktu, dan waktu yang dipilih dimulai dan berakhir pada pukul 12:00 pagi pada tanggal mulai dan akhir. Berikut perhitungannya:

    - Jumlah total yang harus dibayarkan = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Makanan dan porsi insidental dari jumlah total = 5 × (75 + 5) = USD 400

Jika sarapan, makan siang, dan makan malam disediakan selama perjalanan, makanan tersebut harus diperhitungkan sebagai pengurangan makanan.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Contoh 1: Per diem di mana pengurangan makan didasarkan pada jenis makanan per perjalanan

Dalam contoh ini, pengurangan makan adalah 30 persen untuk sarapan, 30 persen untuk makan siang, dan 40 persen untuk makan malam. **Pada halaman Parameter** manajemen pengeluaran, **kotak Hitung pengurangan makan menurut** bidang diatur ke **Jenis makanan per perjalanan**. Berikut adalah perhitungan jika tiga sarapan, dua makan siang, dan nol makan malam diberikan kepada karyawan:

- Pengurangan makan = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Makanan dan biaya tak terduga = 400 – 112,50 = USD 287.50
- Jumlah total yang harus dibayarkan = Total tunjangan – Pengurangan makan = 1.150 – 112,50 = USD 1,037.50

![Biaya per diem di mana pengurangan makan didasarkan pada jenis makanan per perjalanan.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Contoh 2: Per diem di mana pengurangan makan didasarkan pada jenis makanan per hari

Dalam contoh ini, pengurangan makan adalah 30 persen untuk sarapan, 30 persen untuk makan siang, dan 40 persen untuk makan malam. **Pada halaman Parameter** manajemen pengeluaran, **kolom Hitung pengurangan makan menurut** diatur ke **jenis Makanan per hari**. Dalam hal ini, di **kisi Makanan** di **kotak dialog Edit biaya**, Anda menghapus kotak centang untuk menunjukkan makanan mana yang diberikan kepada Anda selama perjalanan Anda.

Sebagai contoh, berikut adalah perhitungan jika sarapan disediakan untuk tiga hari pertama perjalanan:

- Pengurangan makan harian untuk masing-masing tiga hari pertama = 75 × 30% = USD 22.50
- Total pengurangan makan = 3 × 22,50 = USD 67.50
- Makanan dan biaya tak terduga untuk hari 1 sampai 3 = 75 - 22,50 = USD 57.50
- Total makanan dan biaya tak terduga = Jumlah makanan dan biaya tak terduga selama lima hari = 400 – 67,50 = USD 332.50
- Jumlah total yang harus dibayar = Jumlah total – Pengurangan makanan = 1.150 – 67,50 = USD 1,082.50

![Biaya per diem di mana pengurangan makan didasarkan pada jenis makanan per hari.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Contoh 3: Per diem di mana pengurangan makan didasarkan pada jumlah makanan per hari

Dalam contoh ini, pengurangan makan dihitung berdasarkan jumlah makanan yang disediakan per hari (yaitu, **Hitung pengurangan makan berdasarkan** bidang pada **halaman Parameter** manajemen pengeluaran diatur ke **Jumlah makanan per hari**). **Di kisi Makanan** di **kotak dialog Edit biaya**, Anda menghapus kotak centang untuk menunjukkan makanan mana yang disediakan.
Dalam hal ini, pengurangan makanan hanya didasarkan pada # makanan yang disediakan, dan bukan pada jenis makanan (Sarapan / makan siang / makan malam) yang disediakan.

Berikut adalah perhitungan untuk per diem ketika tunjangan harian USD 150 untuk penginapan, USD 75 untuk makanan, dan USD 5 untuk biaya tak terduga:

- **Jumlah total yang harus dibayarkan** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Satu kali makan:** Pengurangan makan = 20% = USD 15
- **Dua kali makan:** Pengurangan makan = 50% = USD 37.50
- **Tiga kali makan:** Pengurangan makan = 100% = USD 75

Berikut adalah perhitungan untuk **makanan dan tunjangan** insidental, yang mencakup USD 5 untuk biaya tak terduga:

- Hari 1 - Dua kali makan yang disediakan = (75 – 37.50) + 5 = 37.50 + 5 = USD 42.50
- Hari 2 - Dua kali makan yang disediakan = (75 – 37.50) + 5 = 37.50 + 5 = USD 42.50
- Hari 3 - Satu kali makan yang disediakan = (75 – 15) + 5 = 60 + 5 = USD 65
- Hari 4 - Nol makanan yang disediakan = (75-0) + 5 = 75 + 5 = USD 80
- Hari 5 - Tiga kali makan yang disediakan = (75 – 75) + 5 = 5 = 0 + 5 = USD 5

- Total makanan dan biaya tak terduga = Makanan dan Biaya Tak Terduga untuk Hari 1+ Hari 2 +Hari 3+Hari 3+Hari 4+ Hari 5 = USD 235
- Pengurangan total makan = Pengurangan makan untuk Hari 1 + Hari 2 + Hari 3 + Hari 4 + Hari 4 + Hari 5 = 37,5 + 37,5 + 15 + 0 + 75 = USD 165
- Jumlah total yang harus dibayarkan = Total tunjangan – Total pengurangan makan = USD 1,150 - USD 165 = USD 985

![Biaya per diem di mana pengurangan makan didasarkan pada jumlah makanan per hari.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Mulai Keuangan versi 10.0.23, jika Anda menggunakan antarmuka pengeluaran yang ditata ulang, Anda tidak dapat membuat pengeluaran per diem yang memiliki tanggal tumpang tindih. Jika Anda mencoba, Anda akan menerima pesan kesalahan.

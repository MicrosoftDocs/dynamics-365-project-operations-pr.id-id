---
title: Konsep estimasi keuangan
description: Laporan topik memberikan informasi tentang estimasi keuangan proyek di Project Operations.
author: rumant
ms.date: 03/22/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 338d2924f0e2a4a7fb943686eaad421a892dce70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597756"
---
# <a name="financial-estimation-concepts"></a>Konsep estimasi keuangan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dalam Dynamics 365 Project Operations, Anda dapat memperkirakan proyek secara keuangan dalam dua tahapan: 
1. Selama tahapan pra penjualan sebelum transaksi dimenangkan. 
2. Selama tahapan eksekusi setelah kontrak proyek dibuat. 

Anda dapat membuat perkiraan keuangan untuk pekerjaan berbasis proyek menggunakan salah satu dari 3 halaman berikut:
- Halaman **baris kuotasi**, menggunakan rincian baris kuotasi.  
- Halaman **baris kontrak proyek**, menggunakan rincian baris kontrak. 
- Halaman **Proyek**, menggunakan halaman tab **Tugas**  atau **Estimasi Pengeluaran**.

## <a name="use-a-project-quote-to-create-an-estimate"></a>Gunakan kuotasi proyek untuk membuat estimasi
Pada kuotasi berbasis proyek, Anda dapat menggunakan entitas **detail baris kuotasi** untuk memperkirakan pekerjaan yang diperlukan untuk melaksanakan proyek. Selanjutnya Anda dapat berbagi perkiraan dengan pelanggan.

Baris kuotasi berbasis proyek tidak boleh memiliki nol pada banyak detail baris kuotasi. Rincian baris kuotasi digunakan untuk memperkirakan waktu, pengeluaran, atau biaya. Microsoft Dynamics 365 Project Operations tidak memungkinkan perkiraan material pada rincian baris kuotasi. Ini disebut kelas transaksi. Jumlah perkiraan pajak juga dapat dimasukkan pada kelas transaksi.

Selain kelas transaksi, rincian baris kuotasi memiliki jenis transaksi. Dua jenis transaksi didukung untuk rincian baris kuotasi: **biaya** dan **kontrak proyek**.

## <a name="use-a-project-contract-to-create-an-estimate"></a>Gunakan kontrak proyek untuk membuat estimasi

Jika Anda menggunakan kuotasi saat membuat kontrak berbasis proyek, perkiraan yang Anda lakukan untuk setiap baris kuotasi pada kuotasi disalin ke kontrak proyek. Struktur kontrak proyek itu seperti struktur kuotasi proyek yang memiliki baris, rincian baris, dan jadwal faktur.

Perkiraan dapat dilakukan secara langsung dalam kontrak proyek, seperti dalam kuotasi proyek. Untuk kuotasi proyek, perkiraan dilakukan dengan menggunakan baris kontrak dan rincian baris kontrak. Rincian baris kontrak juga dapat dibuat dari rencana proyek yang dibuat dengan menggunakan pendekatan perkiraan bottom-up.

Rincian baris kontrak dapat digunakan untuk memperkirakan waktu, pengeluaran, atau biaya. Jumlah perkiraan pajak juga dapat dimasukkan pada rincian baris kontrak.

Estimasi material tidak diizinkan pada rincian baris kontrak.

## <a name="use-a-project-to-create-an-estimate"></a>Gunakan proyek untuk membuat estimasi 

Anda dapat memperkirakan waktu dan biaya pada proyek. Project Operations tidak mendukung estimasi bahan atau ongkos pada proyek.

Perkiraan waktu dihasilkan saat Anda membuat tugas dan mengidentifikasi atribut sumber daya umum yang diperlukan untuk melakukan tugas. Perkiraan waktu dihasilkan dari tugas jadwal. Perkiraan waktu tidak dibuat jika Anda membuat anggota tim generik di luar konteks jadwal.

Perkiraan biaya dimasukkan di kisi pada halaman **Estimasi Pengeluaran**.

Membuat estimasi untuk proyek dianggap sebagai praktik terbaik karena Anda dapat membangun estimasi terperinci dari bawah untuk tenaga kerja atau waktu dan pengeluaran pada setiap tugas dalam rencana proyek. Selanjutnya Anda dapat menggunakan perkiraan terperinci ini untuk membuat estimasi untuk setiap baris kuotasi dan membangun kuotasi yang lebih kredibel untuk pelanggan. Saat Anda mengimpor atau membuat estimasi terperinci pada baris kuotasi menggunakan rencana proyek, Project Operations mengimpor nilai penjualan dan nilai biaya dari estimasi ini. Setelah mengimpor, Anda dapat melihat metrik profitabilitas, margin, dan kelayakan pada kuotasi proyek.

## <a name="understanding-estimates"></a>Memahami estimasi

Gunakan tabel berikut sebagai panduan untuk memahami logika bisnis dalam fase estimasi.

| Skenario                                                                                                                                                                                                                                                                                                                                          | Rekaman entitas                                                                                                                                                                                                       | Jenis Transaksi | Kelas Transaksi | Informasi tambahan                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Bila Anda perlu memperkirakan nilai penjualan waktu pada kuotasi                                                                                                                                                                                                                                                                                    | Rekaman detail baris kuotasi (QLD) dibuat                                                                                                                                                                               | Kontrak proyek | Time        | Bidang asal transaksi pada baris QLD sisi penjualan merujuk pada sisi biaya QLD |
|                                                                                                                                                                                                                                                                                     | Rekaman QLD kedua dibuat oleh sistem untuk menyimpan nilai biaya yang terkait. Semua bidang non-uang disalin dari penjualan QLD ke QLD biaya oleh sistem.                                                                                                                                                                               | Biaya | Time        | Bidang asal transaksi pada baris detail baris kuotasi (QLD) sisi penjualan merujuk pada sisi biaya QLD |
| Bila Anda perlu memperkirakan nilai penjualan waktu pada kontrak                                                                                                                                                                                                                                                                                 | Rekaman detail baris kontrak proyek (CLD) dibuat                                                                                                                                                                    | Kontrak Proyek | Time        | Bidang asal transaksi pada baris CLD sisi penjualan merujuk pada CLD biaya      |
|                                                                                                                                                                                                                                                                                  | Rekaman CLD kedua dibuat oleh sistem untuk menyimpan nilai biaya yang terkait. Semua bidang non-uang disalin dari penjualan CLD ke CLD biaya oleh sistem.                                                                                                                                                                    | Biaya | Time        | Bidang asal transaksi pada baris CLD sisi penjualan merujuk pada CLD biaya      |
| Bila pengguna menjelaskan sumber daya pada tugas proyek                                                                                                                                                                                                                                                                                            | Rekaman baris perkiraan untuk menampilkan nilai penjualan tugas dibuat saat tugas dibuat dengan semua dimensi harga yang diperlukan. Peran dan unit organisasi adalah dimensi harga | Kontrak Proyek | Waktu        |                                                                                   |
|     | Rekaman baris perkiraan untuk menampilkan nilai biaya tugas dibuat saat tugas dibuat dengan semua dimensi harga yang diperlukan. Semua bidang non-uang disalin dari baris perkiraan penjualan ke baris perkiraan biaya oleh sistem. Peran dan unit organisasi adalah dimensi harga baik untuk biaya maupun tarif tagihan.                                                                                                                                                                                                                | Biaya             | Waktu           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Menyesuaikan detail baris kuotasi dan entitas detail baris kontrak

Jika Anda menambahkan bidang kustom pada detail baris kuotasi dan ingin sistem memasukkan nilai bidang sebagai nilai default pada baris biaya terkait yang dibuat, gunakan Alat registrasi plug-in **PreOperationContractLineDetailUpdate** dan **PreOperationQuoteLineDetailUpdate**. Plug-in ini harus didaftarkan ulang setelah detail baris kuotasi atau detail baris kontrak diubah. Untuk menyelesaikan proses ini, ikuti langkah berikut ini.

1. Buka PluginRegistrationTool, dan Sambungkan ke instans online Anda.
2. Pilih **pencarian**, dan Cari plug-in untuk memperbarui.
3. Pilih plug-in, lalu, di halaman utama, klik **pilih**.
4. Pilih langkah plug-in untuk memperbarui, klik kanan, lalu pilih **Perbarui**.
5. Di kotak dialog **Perbarui langkah yang ada**, di bidang **atribut filter**, pilih tombol elipsis (**...**):
6. Di kotak dialog **Pilih atribut**, pilih kotak centang untuk atribut kustom.
7. Pilih **OK** untuk menutup kotak dialog, lalu pilih **Perbarui langkah**.
8. Ulangi langkah 1 hingga 7 untuk plug-in kedua.
9. Tutup **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

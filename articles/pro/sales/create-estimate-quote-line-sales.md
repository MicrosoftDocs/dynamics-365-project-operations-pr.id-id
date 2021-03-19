---
title: Mengestimasi baris kuotasi berbasis proyek
description: Topik ini menyediakan informasi tentang cara membuat perkiraan pada baris kuotasi berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dbd3876e555ee6bc70308ef11a3528a5dd8b6a32
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273517"
---
# <a name="estimating-a-project-based-quote-line"></a>Mengestimasi baris kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Baris kuotasi berbasis proyek memiliki rincian yang membantu memperkirakan biaya dan potensi pendapatan pekerjaan yang terlibat untuk menyampaikan baris kuotasi.

Untuk memperkirakan baris kuotasi berbasis proyek, pada baris kuotasi berbasis proyek, pilih tab **detail baris kuotasi**. Ada dua cara untuk membuat perkiraan pada baris kuotasi berbasis proyek:

- Buat secara manual estimasi secara langsung pada baris kuotasi menggunakan detail baris kuotasi 
- Buat proyek dan rencana proyek, lalu kaitkan proyek dan tugas pada proyek ke baris kuotasi. Proses untuk mengimpor estimasi pada rencana proyek ke baris kuotasi berdasarkan informasi yang Anda berikan akan diaktifkan.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Membuat estimasi langsung di baris kuotasi berbasis proyek

Untuk membuat perkiraan pada baris kuotasi berbasis proyek, pilih tab **rincian baris kuotasi**. Item baris yang Anda buat pada tab ini akan meringkas nilai yang dikutip untuk baris kuotasi ini. 

Untuk membuat rincian baris kuotasi, pilih **+ detail baris kuotasi baru** di subkisi **rincian baris kuotasi**. Slider buat cepat akan terbuka. Bidang berikut pada formulir **baris kuotasi**:

| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| KETERANGAN | Buat cepat | Deskripsi estimasi tertentu. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Kelas Transaksi | Buat cepat | Daftar drop-down ini menyediakan kelas transaksi yang disertakan pada tab **Umum** baris kuotasi berbasis proyek.  | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Peran | Buat cepat | Orang yang akan melakukan pekerjaan ini atau menimbulkan pengeluaran ini. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Kategori | Buat cepat | Kategori pekerjaan atau Pengeluaran. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Tanggal Mulai | Buat cepat | Tanggal pekerjaan dimulai. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Tanggal Akhir | Buat cepat | Dan tanggal akhir pekerjaan. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Unit Sumber Daya | Buat cepat | Unit sumber daya yang akan mengeluarkan biaya ini dan menyediakan sumber daya untuk mengerjakannya. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. Bidang ini juga digunakan dalam pengambilan harga biaya. |
| Jadwal Unit | Buat cepat | Grup unit pekerjaan atau pengeluaran. Unit milik jadwal unit atau grup unit. Misalnya, mil dan km adalah unit milik Grup unit yang menjelaskan jarak. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Unit | Buat cepat | Unit pekerjaan atau pengeluaran. | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Quantity | Buat cepat | Kuantitas pekerjaan atau pengeluaran | Bidang ini default untuk detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Harga unit | Buat cepat | Tarif tagihan peran yang melakukan pekerjaan atau harga penjualan dari kategori pengeluaran. Bidang ini default untuk waktu berdasarkan kombinasi peran dan sumber daya pada daftar harga proyek yang efektif untuk tanggal mulai. Untuk pengeluaran, bidang ini default dari konfigurasi harga untuk kategori transaksi dalam daftar harga proyek yang efektif untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan harga per unit, tidak ada default, dan bidang ini akan dibiarkan kosong. | Tarif biaya peran yang melakukan pekerjaan atau biaya per unit dari kategori pengeluaran. Bidang ini default untuk waktu berdasarkan kombinasi peran dan sumber daya pada harga unit kontrak daftar harga kuotasi yang efektif untuk tanggal mulai. Untuk pengeluaran, bidang ini default dari konfigurasi harga untuk kategori transaksi dalam daftar harga biaya unit kontrak yang efektif untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan harga per unit, tidak ada default, dan bidang ini akan dibiarkan kosong. |
| Perkiraan Pajak | Buat cepat | Anda dapat memasukkan perkiraan pajak untuk pekerjaan atau pengeluaran ini secara manual. | Tidak ada dampak hilir dari bidang ini. |
| Jumlah | Buat cepat | Anda dapat secara manual memasukkan informasi ke bidang ini jika bidang **kuantitas** dan **harga** dibiarkan kosong. Jika bidang ini tidak kosong, bidang ini menjadi hanya baca dan dihitung sebagai (kuantitas \* harga satuan) + pajak. | Tidak ada dampak hilir dari bidang ini. |

## <a name="update-prices-on-quote-line-details"></a>Memperbarui harga pada detail baris kuotasi

Jika Anda telah mengubah harga pada daftar harga proyek yang dilampirkan ke kuotasi, atau pada daftar harga biaya unit kontrak, Anda dapat memilih **hitung ulang** pada **halaman kuotasi**, untuk me-refresh harga pada rincian baris kuotasi individual untuk mencerminkan perubahan ini. Bila Anda memilih **hitung ulang**, terjadi peringatan yang menginformasikan pada Anda bahwa harga pada detail baris kuotasi untuk semua baris kuotasi pada kuotasi ini akan diatur ulang. Pilih **ya**, untuk menyegarkan harga untuk detail baris penjualan dan kuotasi biaya.

## <a name="access-quote-line-details-for-cost"></a>Akses Rincian baris kuotasi untuk biaya

Pada tab **rincian baris kuotasi**, pilih baris di kisi untuk mengaktifkan beberapa tindakan di toolbar subkisi. Tindakan pertama pada bilah alat subkisi bila detail baris kuotasi dipilih adalah **Buka rincian biaya**. Pilih **Buka detail biaya** untuk melihat tingkat biaya dan jumlah yang terkait untuk baris kuotasi ini.

> [!NOTE]
> Mengubah unit sumber daya, kuantitas, tanggal, peran, atau nilai kategori pada detail baris kuotasi untuk biaya akan mengubah nilai yang sesuai pada rincian baris kuotasi untuk penjualan.
## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mata uang pada detail baris kuotasi untuk biaya dan penjualan

Mata uang pada detail baris kuotasi untuk default penjualan dari daftar harga proyek yang efektif untuk tanggal mulai detail baris kuotasi.

Mata uang pada detail baris kuotasi untuk biaya adalah default dari daftar harga unit kontrak kuotasi yang efektif untuk tanggal mulai detail baris kuotasi untuk biaya.

Perhitungan profitabilitas mengkonversi jumlah rincian baris kuotasi untuk biaya dan penjualan ke mata uang dasar lingkungan untuk melaporkan perkiraan margin secara keseluruhan pada kuotasi.

Hal ini dapat mengakibatkan kesalahan pembulatan mata uang dan perubahan margin karena kurangnya nilai tukar efektif tanggal. Gunakan penghitungan ini pada kuotasi proyek hanya sebagai perkiraan dan bukan aktual dan resmi atau pelaporan lainnya yang memerlukan ketepatan lebih tinggi dalam pembulatan dan kesadaran efektivitas tanggal untuk nilai tukar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
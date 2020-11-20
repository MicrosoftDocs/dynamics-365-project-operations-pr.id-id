---
title: Mengestimasi baris kontrak berbasis proyek
description: Topik ini menyediakan informasi tentang estimasi pada baris kontrak berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24299d997074efcff3776168652809d490c81b17
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180466"
---
# <a name="estimate-a-projectbased-contract-line"></a>Mengestimasi baris kontrak berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_ 

Di Dynamics 365 Project Operations, baris kontrak berbasis proyek memiliki rincian yang membantu memperkirakan biaya, dan pendapatan potensial dari pekerjaan yang terlibat untuk melaksanakan baris kontrak.

Untuk memperkirakan baris kontrak berbasis proyek, buka tab **rincian baris kontrak** pada **baris kontrak** berbasis proyek.  Ada dua cara untuk membuat estimasi pada baris kontrak berbasis proyek:

   - Buat estimasi secara langsung pada baris kontrak dengan menambahkan rincian baris kontrak secara manual.
   - Membuat proyek dan rencana proyek, lalu kaitkan proyek dan tugas ke baris kontrak proyek. Hal ini memungkinkan proses dengan mana Anda dapat mengimpor estimasi rencana proyek ke baris kontrak berdasarkan komponen yang disertakan pada baris kontrak.

## <a name="create-an-estimate-directly-on-a-projectbased-contract-line"></a>Membuat estimasi langsung di baris kontrak berbasis proyek

1. Buka baris kontrak, lalu pilih tab **rincian baris kontrak**. Baris yang Anda buat pada tab ini diringkas dan ditampilkan sebagai **nilai kontrak** untuk **baris kontrak** ini. 
2. Di subkisi **rincian baris kontrak**, pilih **+ detail baris kontrak baru**. Penggeser buat cepat terbuka. Bidang berikut tersedia pada formulir **rincian baris kontrak**:

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| **Keterangan** | **Buat Cepat** | Deskripsi estimasi tertentu. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Kelas Transaksi** | **Buat Cepat** | Drop-down ini adalah daftar kelas transaksi yang disertakan pada tab **Umum** baris kontrak berbasis proyek. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Peran** | **Buat Cepat** | Peran orang yang melakukan pekerjaan ini atau memikul pengeluaran ini. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Kategori** | **Buat Cepat** | Kategori pekerjaan atau pengeluaran. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Tanggal Mulai** | **Buat Cepat** | Tanggal pekerjaan dimulai. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Tanggal Akhir** | **Buat Cepat** | Tanggal akhir pekerjaan. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Perusahaan Sumber Daya** | **Buat Cepat** | Perusahaan sumber daya atau entitas hukum yang memikul biaya ini dan menyediakan sumber daya untuk mengerjakannya. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. Bidang ini juga digunakan dalam pengambilan harga biaya. |
| **Unit Sumber Daya** | **Buat Cepat** | Unit sumber daya yang memikul biaya ini dan memberikan sumber daya untuk mengerjakannya. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. Bidang ini juga digunakan dalam pengambilan harga biaya. |
| **Jadwal Unit** | **Buat cepat** | Grup unit pekerjaan atau pengeluaran. Unit milik jadwal unit atau grup unit. Contohnya, *Mil* dan *kilometer (km)* adalah unit yang tergabung dalam grup unit yang menjelaskan jarak. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Unit** | **Buat Cepat** | Unit pekerjaan atau pengeluaran. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Kuantitas** | **Buat Cepat** | Kuantitas pekerjaan atau pengeluaran. | Bidang ini ter-default untuk detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Harga unit** | **Buat Cepat** | Tingkat tagihan peran yang melakukan pekerjaan atau harga penjualan dari kategori pengeluaran. Bidang ini default untuk **waktu** berdasarkan kombinasi peran dan sumber daya pada daftar harga proyek yang efektif untuk tanggal mulai. Untuk pengeluaran, default bidang ini adalah dari konfigurasi harga untuk kategori transaksi dalam daftar harga proyek yang efektif untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan **harga per unit**, tidak ada default, dan bidang ini akan dibiarkan kosong. | Tingkat biaya peran yang melakukan pekerjaan atau biaya per unit dari kategori pengeluaran. Bidang ini ter-default untuk **waktu berdasarkan peran** dan kombinasi unit sumber daya pada baris harga peran dari daftar harga biaya yang dilampirkan ke unit kontrak yang efektif untuk tanggal mulai. Untuk pengeluaran, default bidang ini didasarkan pada baris harga kategori dari daftar harga biaya yang terlampir pada unit kontrak yang efektif untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan harga per unit, tidak ada default, dan bidang ini akan dibiarkan kosong. |
| **Perkiraan Pajak** | **Buat Cepat** | Perkiraan pajak untuk pekerjaan atau pengeluaran ini seperti yang diinput oleh pengguna. | Perkiraan pajak untuk pekerjaan atau pengeluaran ini seperti yang diinput oleh pengguna. |
| **Jumlah** | **Buat Cepat** | Nilai di bidang ini dapat ditambahkan oleh pengguna jika bidang **kuantitas** dan **harga** dibiarkan kosong. Jika **kuantitas** dan **harga** diisi, bidang **Juta** hanya bisa dibaca dan dihitung sebagai **(Kuantitas \* harga satuan) + pajak**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Memperbarui harga pada rincian baris kontrak

Jika Anda mengubah harga pada daftar harga proyek yang dilampirkan ke kontrak atau daftar harga biaya unit kontrak, Anda dapat menyegarkan harga pada rincian baris kontrak individual untuk mencerminkan perubahan. Pada halaman **kontrak**, pilih **hitung ulang**. Peringatan akan terbuka untuk menginformasikan Anda bahwa harga untuk semua baris kontrak pada kontrak ini diatur ulang. Pilih **ya** untuk menyegarkan harga untuk rincian baris kontrak penjualan dan biaya.

## <a name="access-contract-line-details-for-cost"></a>Akses rincian baris kontrak untuk biaya

Pada tab **rincian baris kontrak**, pilih baris di kisi untuk menampilkan tindakan di toolbar subkisi. Tindakan pertama pada bilah alat subkisi adalah **buka rincian biaya**. Untuk melihat jumlah biaya dan tingkat biaya yang terkait dengan detail baris kontrak ini, pilih **Buka rincian biaya**. 

> [!NOTE]
> Mengubah perusahaan sumber daya, unit sumber daya, kuantitas, tanggal, peran, atau nilai kategori pada detail baris kontrak untuk **biaya** juga akan mengubah nilai yang terkait pada detail baris kontrak untuk **penjualan**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Mata uang pada rincian baris kontrak untuk biaya dan penjualan

Rincian baris kontrak untuk **penjualan** menetapkan mata uang default dari daftar harga proyek yang efektif untuk tanggal mulai detail baris kontrak.

Rincian baris kontrak untuk **Biaya** menetapkan mata uang default dari daftar harga unit kontrak dari kontrak yang efektif untuk tanggal mulai detail baris kontrak untuk **Biaya**.

Perhitungan profitabilitas mengkonversi jumlah rincian baris kontrak untuk **biaya** dan **penjualan** ke dalam mata uang dasar lingkungan untuk melaporkan keseluruhan margin aktual dan perkiraan pada kontrak.

> [!NOTE]
> Kesalahan membulatkan mata uang dan margin yang berubah dapat terjadi karena tidak ada nilai tukar efektif tanggal. Gunakan penghitungan ini pada kontrak proyek hanya sebagai perkiraan dan bukan untuk peraturan aktual atau pelaporan lainnya yang memerlukan ketepatan lebih tinggi dalam pembulatan dan kesadaran efektivitas tanggal untuk nilai tukar.

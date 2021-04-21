---
title: Mengestimasi baris kontrak berbasis proyek - lite
description: Topik ini menyediakan informasi tentang estimasi pada baris kontrak berbasis proyek.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bf7941a627375604dca778ab293756bed2536049
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858090"
---
# <a name="estimate-a-projectbased-contract-line---lite"></a>Mengestimasi baris kontrak berbasis proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Di Dynamics 365 Project Operations, baris kontrak berbasis proyek memiliki rincian yang membantu memperkirakan biaya, dan pendapatan potensial dari pekerjaan yang terlibat untuk melaksanakan baris kontrak.

Untuk memperkirakan baris kontrak berbasis proyek, buka tab **rincian baris kontrak** pada **baris kontrak** berbasis proyek.  Ada dua cara untuk membuat estimasi pada baris kontrak berbasis proyek:

   - Buat estimasi secara langsung pada baris kontrak dengan menambahkan rincian baris kontrak secara manual.
   - Membuat proyek dan rencana proyek, lalu kaitkan proyek dan tugas ke baris kontrak proyek. Hal ini memungkinkan proses dengan mana Anda dapat mengimpor estimasi rencana proyek ke baris kontrak berdasarkan komponen yang disertakan pada baris kontrak.

## <a name="create-an-estimation-directly-on-a-projectbased-contract-line"></a>Membuat estimasi langsung di baris kontrak berbasis proyek

Untuk membuat estimasi langsung di baris kontrak berbasis proyek, ikuti langkah-langkah ini:

1. Buka baris kontrak, lalu pilih tab **rincian baris kontrak**. Baris yang Anda buat pada tab ini diringkas dan ditampilkan sebagai **nilai kontrak** untuk **baris kontrak** ini. 
2. Di subkisi **rincian baris kontrak**, pilih **detail baris kontrak baru**. Penggeser buat cepat terbuka. Bidang berikut tersedia di halaman **Rincian Baris Kontrak**.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| **Deskripsi** | **Buat Cepat** | Deskripsi estimasi tertentu. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Kelas Transaksi** | **Buat Cepat** | Ini adalah daftar kelas transaksi yang tercakup di tab **Umum** pada baris kontrak berbasis proyek. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Pilih Produk** | **Buat cepat** | Berlaku bila kelas transaksi adalah **Bahan**. Anda dapat menentukan apakah baris estimasi ini adalah untuk produk **yang Ada** (katalog) atau produk **pilihan**. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Produk** | **Buat cepat** | ID produk dari katalog produk. Bidang ini hanya diaktifkan bila Anda memilih **produk yang ada** dalam bidang **pilih Produk**. ID tersebut digunakan untuk mengambil harga penjualan dari daftar harga proyek pada kontrak. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Produk Pilihan** | **Buat cepat** | Bidang teks untuk memasukkan nama produk. Bidang ini hanya diaktifkan bila Anda memilih **Pilihan** dalam bidang **pilih Produk**.| Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Peran** | **Buat Cepat** | Peran orang yang melakukan pekerjaan ini atau memikul pengeluaran ini. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis.|
| **Kategori** | **Buat Cepat** | Kategori pekerjaan atau pengeluaran. |Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis.|
| **Tanggal Mulai** | **Buat Cepat** | Tanggal pekerjaan dimulai. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Tanggal Akhir** | **Buat Cepat** | Tanggal akhir pekerjaan. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Unit Sumber Daya** | **Buat Cepat** | Unit sumber daya yang mengenakan biaya ini dan menyediakan sumber daya untuk mengerjakannya. |Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis dan digunakan dalam pengambilan harga biaya. |
| **Jadwal Unit** | **Buat cepat** | Grup unit kerja, produk, atau pengeluaran. Unit milik jadwal unit atau grup unit. Contohnya, *Mil* dan *kilometer (km)* adalah unit yang tergabung dalam grup unit yang menjelaskan jarak. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Unit** | **Buat Cepat** | Unit kerja, produk, atau pengeluaran. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Quantity** | **Buat Cepat** | Kuantitas kerja, produk, atau pengeluaran. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Harga unit** | **Buat Cepat** | Tingkat tagihan peran yang melakukan pekerjaan, harga unit produk, atau harga penjualan produk atau kategori pengeluaran. Bidang ini diatur default-nya untuk **Waktu** yang didasarkan pada kombinasi nilai dimensi harga pada baris harga peran pada daftar harga proyek yang berlaku untuk tanggal mulai. Untuk **pengeluaran**, default bidang ini adalah dari konfigurasi harga untuk kategori transaksi dalam daftar harga proyek yang efektif untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan **harga per unit**, tidak ada default, dan bidang ini akan dibiarkan kosong. Untuk produk, default bidang ini didasarkan pada baris **item Daftar harga**  dalam daftar harga proyek yang berlaku untuk tanggal mulai.| Tingkat biaya peran yang melakukan pekerjaan, atau biaya per unit kategori pengeluaran atau biaya per unit dari produk. Bidang ini di-default untuk **Waktu** yang didasarkan pada kombinasi nilai dimensi harga pada baris harga peran pada daftar harga biaya yang dilaporkan ke unit kontrak yang berlaku untuk tanggal mulai. Untuk pengeluaran, default bidang ini didasarkan pada baris harga kategori dari daftar harga biaya yang terlampir pada unit kontrak yang efektif untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan harga per unit, tidak ada default, dan bidang ini akan dibiarkan kosong. Untuk produk, default untuk bidang ini didasarkan pada baris **Item daftar harga**  dari daftar harga biaya yang dilampirkan ke unit kontrak yang berlaku untuk tanggal mulai.|
| **Perkiraan Pajak** | **Buat Cepat** | Estimasi pajak untuk pekerjaan atau pengeluaran ini. | Estimasi pajak untuk pekerjaan atau pengeluaran ini. |
| **Jumlah** | **Buat Cepat** | Anda dapat menambahkan nilai di bidang ini jika bidang **Kuantitas** dan **Harga** dibiarkan kosong. Jika **kuantitas** dan **harga** diisi, bidang **Juta** hanya bisa dibaca dan dihitung sebagai **(Kuantitas \* harga satuan) + pajak**. | &nbsp; |

## <a name="update-prices-on-contract-line-details"></a>Memperbarui harga pada rincian baris kontrak

Jika Anda mengubah harga pada daftar harga proyek yang dilampirkan ke kontrak atau daftar harga biaya unit kontrak, Anda dapat menyegarkan harga pada rincian baris kontrak individual untuk mencerminkan perubahan. Pada halaman **kontrak**, pilih **hitung ulang**. Peringatan muncul untuk memberi tahu Anda bahwa harga untuk semua baris kontrak di kontrak ini diatur ulang. Pilih **ya** untuk menyegarkan harga untuk rincian baris kontrak penjualan dan biaya.

## <a name="access-contract-line-details-for-cost"></a>Akses rincian baris kontrak untuk biaya

Pada tab **rincian baris kontrak**, pilih baris di kisi untuk menampilkan tindakan di toolbar subkisi. Tindakan pertama pada bilah alat subkisi adalah **buka rincian biaya**. Untuk melihat jumlah biaya dan tingkat biaya yang terkait dengan detail baris kontrak ini, pilih **Buka rincian biaya**. 

> [!NOTE]
> Mengubah perusahaan sumber daya, unit sumber daya, kuantitas, tanggal, peran, atau nilai kategori pada detail baris kontrak untuk **biaya** juga akan mengubah nilai yang terkait pada detail baris kontrak untuk **penjualan**.

## <a name="currency-on-contract-line-details-for-cost-and-sales"></a>Mata uang pada rincian baris kontrak untuk biaya dan penjualan

Rincian baris kontrak untuk **penjualan** menetapkan mata uang default dari daftar harga proyek yang efektif untuk tanggal mulai detail baris kontrak.

Rincian baris kontrak untuk **Biaya** menetapkan mata uang default dari daftar harga unit kontrak dari kontrak yang efektif untuk tanggal mulai detail baris kontrak untuk **Biaya**.

Perhitungan profitabilitas mengkonversi jumlah rincian baris kontrak untuk **biaya** dan **penjualan** ke dalam mata uang dasar lingkungan untuk melaporkan keseluruhan margin aktual dan perkiraan pada kontrak.

> [!NOTE]
> Kesalahan membulatkan mata uang dan margin yang berubah dapat terjadi karena tidak ada nilai tukar efektif tanggal. Gunakan perhitungan ini hanya pada kontrak proyek karena ini merupakan perkiraan dan bukan untuk pelaporan resmi aktual atau laporan lainnya yang memerlukan presisi pembulatan yang lebih tinggi dan kesadaran terhadap efektivitas tanggal untuk nilai tukar.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

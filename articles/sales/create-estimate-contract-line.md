---
title: Mengestimasi baris kontrak proyek
description: Artikel ini memberikan informasi tentang perkiraan pada jalur kontrak proyek.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 553f7e4a9e9f57732267a48da2b299c1751b0c0e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932024"
---
# <a name="estimate-a-project-contract-line"></a>Mengestimasi baris kontrak proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_ 

Di Dynamics 365 Project Operations, baris kontrak berbasis proyek memiliki rincian yang membantu memperkirakan biaya, dan pendapatan potensial dari pekerjaan yang terlibat untuk melaksanakan baris kontrak.

Untuk memperkirakan baris kontrak berbasis proyek, buka tab **rincian baris kontrak** pada **baris kontrak** berbasis proyek.  Ada dua cara untuk membuat estimasi pada baris kontrak berbasis proyek:

   - Buat estimasi secara langsung pada baris kontrak dengan menambahkan rincian baris kontrak secara manual.
   - Membuat proyek dan rencana proyek, lalu kaitkan proyek dan tugas ke baris kontrak proyek. Hal ini memungkinkan proses dengan mana Anda dapat mengimpor estimasi rencana proyek ke baris kontrak berdasarkan komponen yang disertakan pada baris kontrak.

## <a name="create-an-estimate-directly-on-a-project-contract-line"></a>Membuat estimasi langsung di baris kontrak proyek

Untuk membuat estimasi langsung di baris kontrak proyek, ikuti langkah-langkah ini:

1. Buka baris kontrak, lalu pilih tab **rincian baris kontrak**. Baris yang Anda buat pada tab ini diringkas dan ditampilkan sebagai **nilai kontrak** untuk **baris kontrak** ini. 
2. Di subkisi **rincian baris kontrak**, pilih **detail baris kontrak baru**. Penggeser buat cepat terbuka. Bidang berikut tersedia di halaman **Rincian Baris Kontrak**.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| **Deskripsi** | **Buat Cepat** | Deskripsi estimasi tertentu. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Kelas Transaksi** | **Buat Cepat** | Daftar kelas transaksi ini tercakup di tab **Umum** pada baris kontrak berbasis proyek. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Pilih Produk** | **Buat cepat** | Berlaku bila kelas transaksi adalah **Bahan**. Anda dapat memilih untuk menentukan baris estimasi ini adalah untuk produk **yang Ada** (katalog) atau produk **pilihan**. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Produk** | **Buat cepat** | ID produk dari katalog produk. Bidang ini hanya diaktifkan bila Anda memilih **produk yang ada** dalam bidang **pilih Produk**. ID tersebut digunakan untuk mengambil harga penjualan dari daftar harga proyek pada kontrak. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Produk Pilihan** | **Buat cepat** | Bidang teks untuk memasukkan nama produk. Bidang ini hanya diaktifkan bila Anda memilih **Pilihan** dalam bidang **pilih Produk**.| Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Peran** | **Buat Cepat** | Peran orang yang melakukan pekerjaan ini atau memikul pengeluaran ini. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis.|
| **Kategori** | **Buat Cepat** | Kategori pekerjaan atau pengeluaran. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis.|
| **Tanggal Mulai** | **Buat Cepat** | Tanggal pekerjaan dimulai. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Tanggal Akhir** | **Buat Cepat** | Tanggal akhir pekerjaan. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Perusahaan Sumber Daya** | **Buat Cepat** | Perusahaan sumber daya atau entitas hukum yang mengenakan biaya ini dan menyediakan sumber daya untuk mengerjakannya. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis dan digunakan dalam pengambilan harga biaya. |
| **Unit Sumber Daya** | **Buat Cepat** | Unit sumber daya yang mengenakan biaya ini dan menyediakan sumber daya untuk mengerjakannya. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis dan digunakan dalam pengambilan harga biaya. |
| **Jadwal Unit** | **Buat cepat** | Grup unit kerja, produk, atau pengeluaran. Unit milik jadwal unit atau grup unit. Contohnya, *Mil* dan *kilometer (km)* adalah unit yang tergabung dalam grup unit yang menjelaskan jarak. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Unit** | **Buat Cepat** | Unit kerja, produk, atau pengeluaran. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Quantity** | **Buat Cepat** | Kuantitas kerja, produk, atau pengeluaran. | Nilai ini diatur default ke detail baris kontrak terkait untuk biaya yang dibuat secara otomatis. |
| **Harga unit** | **Buat Cepat** | Tingkat tagihan peran yang melakukan pekerjaan, harga unit produk, atau harga penjualan produk atau kategori pengeluaran. Default untuk **Waktu** didasarkan pada kombinasi nilai dimensi harga pada baris harga peran pada daftar harga proyek yang berlaku untuk tanggal mulai. Untuk **Pengeluaran**, default untuk bidang ini adalah dari konfigurasi harga untuk kategori transaksi dalam daftar harga proyek yang berlaku untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan **harga per unit**, tidak ada default, dan bidang ini akan dibiarkan kosong. Untuk produk, default bidang ini didasarkan pada baris **item Daftar harga**  dalam daftar harga proyek yang berlaku untuk tanggal mulai.| Tingkat biaya peran yang melakukan pekerjaan, atau biaya per unit kategori pengeluaran atau biaya per unit dari produk. Default untuk **Waktu** didasarkan pada kombinasi nilai dimensi harga pada baris harga peran pada daftar harga biaya yang dilaporkan ke unit kontrak yang berlaku untuk tanggal mulai. Untuk **Pengeluaran**, default untuk bidang ini didasarkan pada baris harga kategori dari daftar harga biaya yang dilampirkan ke unit kontrak yang berlaku untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan harga per unit, tidak ada default, dan bidang ini akan dibiarkan kosong. Untuk produk, default untuk bidang ini didasarkan pada baris **Item daftar harga** dari daftar harga biaya yang dilampirkan ke unit kontrak yang berlaku untuk tanggal mulai.|
| **Perkiraan Pajak** | **Buat Cepat** | Perkiraan pajak untuk pekerjaan atau pengeluaran ini seperti yang diinput oleh pengguna. | &nbsp; |
| **Jumlah** | **Buat Cepat** | Nilai di bidang ini dapat ditambahkan jika bidang **Kuantitas** dan **Harga** dibiarkan kosong. Jika bidang **Kuantitas** dan **Harga** diisi, bidang **Jumlah** hanya bisa dibaca dan dihitung sebagai **(Kuantitas \* Harga Per Unit) + Pajak**. | &nbsp; |

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]

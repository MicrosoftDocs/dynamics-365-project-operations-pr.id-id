---
title: Mengestimasi baris kuotasi proyek
description: Halaman topik ini menyediakan informasi tentang bagaimana membuat estimasi pada baris kuotasi proyek.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 84283ac055aea802fadbd6814ea65a6d3dc01d29e1e3c6290ef11f72f6a75692
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003955"
---
# <a name="estimate-a-project-quote-line"></a>Mengestimasi baris kuotasi proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Baris kuotasi berbasis proyek memiliki rincian yang membantu memperkirakan biaya dan potensi pendapatan pekerjaan yang terlibat untuk menyampaikan baris kuotasi.

Untuk memperkirakan baris kuotasi berbasis proyek, pada baris kuotasi, pilih tab **Detail Baris Kuotasi**. Ada dua cara untuk membuat estimasi pada baris kuotasi berbasis proyek:

   - Buat secara manual estimasi secara langsung pada baris kuotasi menggunakan detail baris kuotasi. 
   - Buat proyek dan rencana proyek, lalu kaitkan proyek dan tugas pada proyek ke baris kuotasi. Proses untuk mengimpor estimasi pada rencana proyek ke baris kuotasi berdasarkan informasi yang Anda berikan akan diaktifkan.

## <a name="create-estimates-directly-on-a-project-based-quote-line"></a>Membuat estimasi langsung di baris kuotasi berbasis proyek

Untuk membuat estimasi langsung di baris kuotasi berbasis proyek, ikuti langkah-langkah ini:

1. Untuk membuat perkiraan pada baris kuotasi berbasis proyek, pilih tab **rincian baris kuotasi**. Item baris yang Anda buat pada tab ini akan meringkas nilai yang dikutip untuk baris kuotasi ini. 
2. Untuk membuat rincian baris kuotasi, pilih **detail baris kuotasi baru** di subkisi **rincian baris kuotasi**. Slider buat cepat akan terbuka. Bidang berikut pada halaman **Baris Kuotasi**.

| **Bidang** | **Lokasi** | **Deskripsi** | **Dampak hilir** |
| --- | --- | --- | --- |
| KETERANGAN | Buat cepat | Deskripsi estimasi tertentu. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Kelas Transaksi | Buat cepat | Daftar drop-down ini menyediakan kelas transaksi yang disertakan pada tab **Umum** baris kuotasi berbasis proyek.  | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Pilih Produk | Buat cepat | Berlaku bila kelas transaksi adalah **Bahan**. Anda dapat memilih untuk menentukan baris estimasi ini adalah untuk produk **yang Ada** (katalog) atau produk **pilihan**. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Produk | Buat cepat | ID produk dari katalog produk. Bidang ini hanya diaktifkan bila Anda memilih **yang ada** dalam bidang **pilih Produk**. ID tersebut digunakan untuk mengambil harga penjualan dari daftar harga proyek pada kuotasi. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Produk Pilihan | Buat cepat | Kotak teks untuk menulis nama produk. Bidang ini hanya diaktifkan bila Anda memilih **Pilihan** dalam bidang **pilih Produk**.| Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Peran | Buat cepat | Peran orang yang akan melakukan pekerjaan ini atau menimbulkan pengeluaran ini. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Kategori | Buat cepat | Kategori pekerjaan atau pengeluaran. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Tanggal Mulai | Buat cepat | Tanggal pekerjaan dimulai. | Bidang ini diatur default ke detail baris kuotasi untuk biaya yang dibuat secara otomatis. |
| Tanggal Akhir | Buat cepat | Tanggal akhir pekerjaan. | Bidang ini diatur default ke detail baris kuotasi untuk biaya yang dibuat secara otomatis. |
| Perusahaan Sumber Daya | Buat Cepat | Perusahaan sumber daya atau entitas hukum yang mengenakan biaya ini dan menyediakan sumber daya untuk mengerjakannya. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis dan digunakan dalam pengambilan harga biaya. |
| Unit Sumber Daya | Buat cepat | Unit sumber daya yang mengenakan biaya ini dan menyediakan sumber daya untuk mengerjakannya. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis dan digunakan dalam pengambilan harga biaya. |
| Jadwal Unit | Buat cepat | Grup unit kerja, produk, atau pengeluaran. Unit milik jadwal unit atau grup unit. Contohnya, Mil dan kilometer adalah unit yang tergabung dalam grup unit yang mendeskripsikan jarak. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Unit | Buat cepat | Unit kerja, produk, atau pengeluaran. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Quantity | Buat cepat | Kuantitas kerja, produk, atau pengeluaran. | Nilai ini diatur default ke detail baris kuotasi terkait untuk biaya yang dibuat secara otomatis. |
| Harga unit | Buat Cepat |Tingkat tagihan peran yang melakukan pekerjaan, harga unit produk, atau harga penjualan produk atau kategori pengeluaran. Default untuk **Waktu** didasarkan pada kombinasi nilai dimensi harga pada baris harga peran pada daftar harga proyek yang berlaku untuk tanggal mulai. Untuk **pengeluaran**, default-nya adalah dari konfigurasi harga untuk kategori transaksi dalam daftar harga proyek yang efektif untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan harga per unit, tidak ada default, dan bidang ini akan dibiarkan kosong. Untuk produk, default bidang ini didasarkan pada baris **item Daftar harga**  dalam daftar harga proyek yang berlaku untuk tanggal mulai.| Tingkat biaya peran yang melakukan pekerjaan, biaya per unit kategori pengeluaran atau biaya per unit dari produk. Default untuk **Waktu** didasarkan pada kombinasi nilai dimensi harga pada baris harga peran pada daftar harga biaya yang dilaporkan ke unit kontrak yang berlaku untuk tanggal mulai. Untuk Pengeluaran, default-nya didasarkan pada baris harga kategori dari daftar harga biaya yang dilampirkan ke unit kontrak yang berlaku untuk tanggal mulai. Jika metode harga untuk kategori transaksi bukan harga per unit, maka tidak ada default dan bidang ini dibiarkan kosong. Untuk produk, default untuk bidang ini didasarkan pada baris **Item daftar harga**  dari daftar harga biaya yang dilampirkan ke unit kontrak yang berlaku untuk tanggal mulai.|
| Perkiraan Pajak | Buat cepat | Anda dapat memasukkan perkiraan pajak untuk pekerjaan atau pengeluaran ini secara manual. | Tidak ada dampak hilir untuk bidang ini. |
| Jumlah | Buat cepat | Anda dapat secara manual memasukkan informasi ke bidang ini jika bidang **kuantitas** dan **harga** dibiarkan kosong. Jika bidang ini tidak kosong, bidang ini menjadi hanya baca dan dihitung sebagai (kuantitas \* harga satuan) + pajak. | Tidak ada dampak hilir untuk bidang ini. |

## <a name="update-prices-on-quote-line-details"></a>Memperbarui harga pada detail baris kuotasi

Jika Anda telah mengubah harga pada daftar harga proyek yang dilampirkan ke kuotasi, atau pada daftar harga biaya unit kontrak, Anda dapat memilih **hitung ulang** pada **halaman kuotasi**, untuk me-refresh harga pada rincian baris kuotasi individual untuk mencerminkan perubahan ini. Bila Anda memilih **Hitung Ulang**, peringatan muncul yang memberi tahu Anda bahwa harga pada detail baris kuotasi untuk semua baris kuotasi pada kuotasi ini akan diatur ulang. Pilih **ya** untuk menyegarkan harga untuk detail baris penjualan dan kuotasi biaya.

## <a name="access-quote-line-details-for-cost"></a>Akses Rincian baris kuotasi untuk biaya

Untuk mengakses rincian baris kuotasi mengenai biaya, ikuti langkah berikut:

1. Pada tab **Rincian Baris Kuotasi**, pilih baris di kisi untuk mengaktifkan tindakan di toolbar subkisi. 
2. Pilih **Buka detail biaya** untuk melihat tingkat biaya dan jumlah yang terkait untuk baris kuotasi ini.

> [!NOTE]
> Mengubah unit sumber daya, kuantitas, tanggal, peran, atau nilai kategori pada detail baris kuotasi untuk biaya akan mengubah nilai yang sesuai pada rincian baris kuotasi untuk penjualan.

## <a name="currency-on-quote-line-details-for-cost-and-sales"></a>Mata uang pada detail baris kuotasi untuk biaya dan penjualan

Mata uang pada detail baris kuotasi untuk default penjualan dari daftar harga proyek yang berlaku untuk tanggal mulai detail baris kuotasi.

Mata uang pada detail baris kuotasi untuk default biaya dari daftar harga unit kontrak kuotasi yang berlaku untuk tanggal mulai detail baris kuotasi untuk biaya.

> [!NOTE]
> Perhitungan profitabilitas mengkonversi jumlah rincian baris kuotasi untuk biaya dan penjualan ke mata uang dasar lingkungan untuk melaporkan perkiraan margin secara keseluruhan pada kuotasi. Kesalahan membulatkan mata uang dan margin yang berubah dapat terjadi karena tidak ada nilai tukar efektif tanggal. Gunakan perhitungan ini hanya pada kuotasi proyek karena ini merupakan perkiraan dan bukan pelaporan resmi aktual atau laporan lainnya yang memerlukan presisi pembulatan yang lebih tinggi dan kesadaran terhadap efektivitas tanggal untuk nilai tukar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

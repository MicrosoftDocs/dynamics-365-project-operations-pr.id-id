---
title: Baris Subkontrak untuk produk
description: Artikel ini menjelaskan cara merekam baris subkontrak untuk produk dan menggunakan berbagai bidang untuk mencatat pembelian produk dari vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b5852df1876eff591ae6a131b229d979eacf5aad
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262120"
---
# <a name="subcontract-lines-for-products"></a>Baris Subkontrak untuk produk

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Subkontrak dalam Dynamics 365 Project Operations dapat memiliki baris subkontrak untuk produk. Baris ini memungkinkan Manajer Proyek membeli produk dari vendor yang kemudian dapat mereka gunakan pada tugas proyek.

selesaikan langkah-langkah berikut ini untuk membuat baris subkontrak untuk produk di Project Operations.

1. Di halaman navigasi, pilih **Subkontrak**, dan buka Subkontrak yang ingin Anda kerjakan. 
2. Pada tab **Baris Subkontrak**, pilih **+ Baru** untuk membuat baris subkontrak baru.
3. Pada halaman **Buat Cepat**, pada bidang **Kelas Transaksi**, pilih **Bahan** dan masukkan informasi bidang lainnya yang diperlukan. 
4. Pilih **Simpan**.

Tabel berikut menyediakan informasi tentang bidang pada halaman **rincian baris Subkontrak** dan halaman **Buat Cepat** karena relevan untuk pembelian produk.

| Bidang | KETERANGAN | Dampak Fungsional|
| ----- | ----------- | ----------- |
| Nama | Nama baris subkontrak untuk membantu identifikasi. |Ini akan ditampilkan sebagai kolom pertama di semua pencarian berdasarkan baris subkontrak.
| KETERANGAN | Deskripsi singkat tentang produk yang dipesan pada baris subkontrak. | Tidak Ada |
| Jenis Baris | Bidang ini memiliki nilai default **berbasis Kuantitas**. |Tidak Ada |
| Metode Penagihan | Ini adalah rangkaian pilihan yang menunjukkan dua model kontrak utama yang didukung oleh Project Operations: **Harga Tetap** dan **waktu dan bahan**. | Berdasarkan metode penagihan yang dipilih, jadwal faktur berbasis tahapan disediakan untuk baris subkontrak dengan metode penagihan Harga Tetap. |
| Kelas Transaksi |Bidang ini memiliki nilai default  **waktu**. Untuk membuat baris subkontrak untuk pembelian produk, atur bidang  **Kelas Transaksi**  ke  **Bahan**.  | Ini menunjukkan bahwa baris subkontrak sedang digunakan untuk merekam pembelian produk yang akan digunakan pada proyek. |
| Pilih Produk | Pilih apakah produk yang dibeli dikelola dalam katalog produk atau merupakan produk pilihan. |Tidak Ada |
| Produk | Pilih produk aktif dari katalog. Bidang ini tersedia hanya bila **Pilih Produk** diatur ke **yang Ada**. |Kombinasi **Produk** dan **Unit** akan digunakan sebagai default atau dihitung untuk harga unit untuk baris subkontrak.
| Produk Pilihan | Masukkan nama produk pilihan. Bidang ini tersedia hanya bila **Pilih Produk** diatur ke **pilihan**.  |Harga pembelian tidak akan secara otomatis diisi untuk produk pilihan.|
| Tanggal Pengiriman yang Diminta | Masukkan tanggal pengiriman yang diperlukan untuk produk.| Tanggal ini juga digunakan untuk memilih daftar harga proyek dari daftar harga proyek yang dilampirkan ke subkontrak. Biaya produk pada baris subkontrak kemudian di-default dari daftar harga tersebut. |
| Tanggal Pengiriman yang Dikontrak | Masukkan tanggal pengiriman produk yang disetujui secara kontraktual.  |Tidak Ada|
| Kuantitas yang Dipesan | Masukkan kuantitas produk yang dibeli dari vendor.| Ini akan digunakan untuk menunjukkan peringatan ketika manajer proyek terlalu banyak menarik dari kuantitas ini.|
| Grup Unit | Nilai ini di-default untuk produk katalog saja. |Bila **Produk** dan **tanggal pengiriman yang Diminta** dipilih, sistem akan memilih daftar harga yang berlaku berdasarkan tanggal pengiriman. Item daftar harga terkait dikueri untuk produk yang cocok. Nilai unit dan grup unit diatur default dari konfigurasi pada rekaman item daftar harga. |
| Unit | Nilai ini diatur default ke unit yang diatur pada rekaman item daftar harga. Anda dapat mengubahnya ke unit lain bila diperlukan.| Kombinasi produk dan unit digunakan untuk men-default harga unit pada baris subkontrak untuk produk katalog yang ada. |
| Harga Unit | Harga unit di-default dengan kombinasi kategori produk dan unit dari item daftar harga yang terkait dengan daftar harga proyek yang berlaku untuk tanggal pengiriman yang diminta dari baris subkontrak.  |Tidak Ada |
| Subtotal | Bidang hanya baca ini dihitung sebagai Kuantitas x Harga Unit jika nilai kedua bidang dimasukkan. Jika salah satu bidang **Kuantitas**, bidang **Harga per unit**, atau kedua bidang kosong, Anda dapat secara manual memasukkan nilainya.  |Tidak Ada |
| Pajak Penjualan | Masukkan nilai pajak penjualan. |Tidak Ada |
| Jumlah Total | Data bidang terhitung ini menunjukkan jumlah total baris subkontrak setelah pajak disertakan. Nilai dalam bidang ini dihitung sebagai subtotal + pajak. |Tidak Ada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

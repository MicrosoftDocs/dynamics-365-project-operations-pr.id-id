---
title: Baris Subkontrak untuk produk
description: Topik ini menjelaskan cara merekam baris subkontrak untuk produk dan menggunakan berbagai bidang untuk merekam pembelian produk vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323690"
---
# <a name="subcontract-lines-for-products"></a>Baris Subkontrak untuk produk

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Subkontrak dalam Dynamics 365 Project Operations dapat memiliki baris subkontrak untuk produk. Baris ini memungkinkan Manajer Proyek membeli produk dari vendor yang kemudian dapat mereka gunakan pada tugas proyek.

selesaikan langkah-langkah berikut ini untuk membuat baris subkontrak untuk produk di Project Operations.

1. Di halaman navigasi, pilih **Subkontrak**, dan buka Subkontrak yang ingin Anda kerjakan. 
2. Pada tab **Baris Subkontrak**, pilih **+ Baru** untuk membuat baris subkontrak baru.
3. Pada halaman **Buat Cepat**, pada bidang **Kelas Transaksi**, pilih **Bahan** dan masukkan informasi bidang lainnya yang diperlukan. 
4. Pilih **Simpan**.

Tabel berikut menyediakan informasi tentang bidang pada halaman **rincian baris Subkontrak** dan halaman **Buat Cepat** karena relevan untuk pembelian produk.

| Bidang | KETERANGAN |
| ----- | ----------- |
| Nama | Nama Baris Subkontrak. |
| KETERANGAN | Deskripsi singkat tentang produk yang dipesan pada baris subkontrak. |
| Jenis Baris | Bidang ini di-default ke **berbasis Kuantitas**. |
| Metode Penagihan |  Metode penagihan Baris Subkontrak. Untuk metode penagihan harga tetap, jadwal faktur berbasis tahapan sudah tersedia. |
| Kelas Transaksi | Bidang ini di-default ke **waktu**. Untuk membuat baris subkontrak untuk pembelian produk, di bidang **Kelas Transaksi**, pilih **Bahan**. Pilihan ini menunjukkan bahwa baris subkontrak sedang digunakan untuk merekam pembelian produk yang akan digunakan pada proyek. |
| Pilih Produk | Pilih apakah produk yang dibeli dikelola dalam katalog produk atau merupakan produk pilihan. |
| Produk | Pilih produk aktif dari katalog. Bidang ini tersedia hanya bila **Pilih Produk** diatur ke **yang Ada**. |
| Produk Pilihan | Masukkan nama produk pilihan. Bidang ini tersedia hanya bila **Pilih Produk** diatur ke **pilihan**.  |
| Tanggal Pengiriman yang Diminta | Pilih tanggal pengiriman yang diperlukan untuk produk. Tanggal ini juga digunakan untuk memilih daftar harga proyek dari daftar harga proyek yang dilampirkan ke subkontrak. Biaya produk pada baris subkontrak kemudian di-default dari daftar harga tersebut. |
| Tanggal Pengiriman yang Dikontrak | Pilih tanggal pengiriman produk yang disepakati secara kontrak.  |
| Kuantitas yang Dipesan | Masukkan kuantitas produk yang dibeli dari vendor. Ketika manajer proyek mengambil berlebihan kuantitas ini, peringatan akan terjadi. |
| Grup Unit | Nilai ini di-default untuk produk katalog saja. Bila **Produk** dan **tanggal pengiriman yang Diminta** dipilih, sistem akan memilih daftar harga yang berlaku berdasarkan tanggal pengiriman. Item daftar harga terkait dikueri untuk produk yang cocok. Nilai unit dan grup unit diatur default dari konfigurasi pada rekaman item daftar harga. |
| Unit | Nilai ini diatur default ke konfigurasi unit pada rekaman item daftar harga. Anda dapat mengubahnya ke unit lain bila diperlukan. Kombinasi produk dan unit digunakan untuk men-default harga unit pada baris subkontrak untuk produk katalog yang ada. |
| Harga Unit | Harga unit di-default dengan kombinasi kategori produk dan unit dari item daftar harga yang terkait dengan daftar harga proyek yang berlaku untuk tanggal pengiriman yang diminta dari baris subkontrak.  |
| Subtotal | Bidang hanya baca ini dihitung sebagai Kuantitas x Harga Unit jika nilai kedua bidang dimasukkan. Jika salah satu bidang **Kuantitas**, bidang **Harga per unit**, atau kedua bidang kosong, Anda dapat secara manual memasukkan nilainya.  |
| Pajak Penjualan | Masukkan nilai pajak penjualan. |
| Jumlah Total | Data bidang terhitung ini menunjukkan jumlah total baris subkontrak setelah pajak disertakan. Nilai dalam bidang ini dihitung sebagai subtotal + pajak. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Baris subkontrak untuk kategori pengeluaran
description: Topik ini menjelaskan cara merekam baris subkontrak untuk pengeluaran dan menggunakan bidang untuk merekam pembelian waktu dari vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323825"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Baris subkontrak untuk kategori pengeluaran

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Subkontrak dalam Dynamics 365 Project Operations dapat memiliki baris untuk kategori pengeluaran. Baris subkontrak untuk kategori pengeluaran memungkinkan Manajer Proyek membeli kategori layanan atau produk dari vendor yang dapat mereka tagih pada proyek.

Untuk membuat baris subkontrak untuk kategori pengeluaran di Project Operations, selesaikan langkah-langkah berikut.

1. Di panel navigasi, pilih **Subkontrak**, dan buka Subkontrak yang ingin Anda kerjakan.
2. Pada tab **Baris Subkontrak**, pilih **Baru** untuk membuat baris baru.
3. Pada halaman **Buat Cepat**, pada bidang **Kelas Transaksi**, pilih **Pengeluaran** dan masukkan atau pilih informasi bidang lainnya yang diperlukan.

Tabel berikut menyediakan informasi tentang bidang pada halaman rincian **baris Subkontrak** dan halaman **Buat Cepat**.

| **Bidang** |  **Deskripsi** |
| ----------| ---------------- |
| Nama | Nama Baris Subkontrak. |
| KETERANGAN | Deskripsi singkat kategori produk atau layanan yang dibeli pada subkontrak. |
| Jenis Baris | Bidang ini memiliki nilai default **berbasis Kuantitas**.  |
| Metode Penagihan | Metode penagihan Baris Subkontrak. Berdasarkan metode penagihan baris, jadwal faktur berbasis tahapan tersedia untuk metode penagihan harga tetap.  |
| Kelas Transaksi | Bidang ini memiliki nilai default **waktu**. Untuk membuat baris subkontrak untuk pembelian produk, atur bidang **Kelas Transaksi** ke **Pengeluaran**. Nilai bidang ini menunjukkan bahwa baris subkontrak sedang digunakan untuk merekam pembelian kategori produk atau layanan yang akan digunakan pada proyek. |
| Kategori Transaksi | Pilih kategori transaksi. |
| Awalan yang Diminta | Tanggal saat kategori pembelian harus tersedia dari vendor. Awal yang diminta digunakan untuk memilih daftar harga proyek dari daftar harga proyek yang dilampirkan ke subkontrak. Biaya kategori pada baris subkontrak di-default dari daftar harga tersebut. |
| Akhir yang Diminta | Tanggal saat kategori pembelian tidak lagi diperlukan. Tanggal ini memanggil peringatan bila manajer proyek mengaitkan baris subkontrak ini dengan estimasi pengeluaran tertentu pada proyek yang memiliki tanggal setelah tanggal ini. |
| Kuantitas yang Dipesan | Kuantitas kategori yang dibeli dari vendor. Ketika manajer proyek mengambil berlebihan dari kuantitas yang dibeli, peringatan akan terjadi.  |
| Grup Unit | Nilai bidang ini diatur secara default berdasarkan grup unit default yang disiapkan untuk kategori yang dipilih. |
| Unit | Nilai bidang ini diatur secara default berdasarkan unit default yang disiapkan untuk kategori yang dipilih. Kombinasi kategori dan unit digunakan untuk men-default harga unit pada baris subkontrak. |
| Harga Unit | Nilai bidang harga unit di-default dari kombinasi kategori dan unit dari harga kategori yang terkait dengan daftar harga proyek yang berlaku untuk awalan yang diminta dari baris subkontrak.  |
| Subtotal | Bidang hanya baca ini secara otomatis dihitung sebagai harga unit kuantitas jika nilai kuantitas dan harga unit dimasukkan. Jika salah satu atau kedua bidang kosong, Anda dapat secara manual memasukkan nilai di bidang ini.  |
| Pajak Penjualan | Masukkan jumlah pajak penjualan.  |
| Jumlah Total | Jumlah total baris Subkontrak termasuk pajak. Bidang ini dihitung sebagai subtotal + pajak penjualan.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

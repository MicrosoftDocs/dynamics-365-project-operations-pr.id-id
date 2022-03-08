---
title: Baris Subkontrak untuk waktu
description: Topik ini menjelaskan cara merekam baris subkontrak untuk waktu dan merekam pembelian waktu dari vendor.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323870"
---
# <a name="subcontract-lines-for-time"></a>Baris Subkontrak untuk waktu

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Subkontrak dalam Dynamics 365 Project Operations dapat memiliki baris subkontrak untuk waktu. Baris subkontrak untuk waktu memungkinkan Manajer Proyek membeli waktu sumber daya vendor untuk mengadakan staf tugas proyek dan persyaratan sumber daya.

Selesaikan langkah-langkah berikut ini untuk membuat baris subkontrak untuk waktu di Project Operations.

1. Di panel navigasi, pilih **Subkontrak**, dan buka Subkontrak.
2. Pada tab **Baris Subkontrak**, pilih **Baru** untuk membuat baris subkontrak baru.
3. Pada halaman **Buat Cepat**, pada bidang **Kelas Transaksi**, pilih **Waktu**.
4. Masukkan informasi bidang tersisa dan kemudian pilih **Simpan**.

  Tabel berikut menyediakan informasi tentang bidang pada halaman **baris Subkontrak** dan halaman **Buat Cepat**.

| **Bidang** | **Deskripsi** |
| --- | --- |
| Nama | Nama Baris Subkontrak. |
| KETERANGAN | Deskripsi singkat tentang layanan yang dibeli pada baris subkontrak. | 
| Jenis Baris | Bidang ini adalah Nilai default.  |
| Metode Penagihan | Pilih metode penagihan. Berdasarkan metode baris subkontrak yang dirujuk, jadwal faktur berbasis tahapan disediakan untuk metode penagihan harga tetap. |
| Kelas Transaksi | Bidang ini adalah nilai default yang menunjukkan apakah baris subkontrak sedang digunakan untuk merekam pembelian waktu subkontraktor. |
| Peran | Peran sumber daya subkontrak yang waktunya dibeli. Peran yang ditetapkan ke sumber daya subkontrak menentukan biaya pembelian. |
| Awalan yang Diminta | Tanggal saat sumber daya subkontraktor diperlukan untuk mulai bekerja. Awal yang diminta digunakan untuk memilih daftar harga proyek dari daftar harga proyek yang dilampirkan ke subkontrak. Biaya peran pada baris subkontrak kemudian di-default dari daftar harga tersebut. |
| Akhir yang Diminta | Tanggal berakhirnya penugasan sumber daya subkontraktor. Tanggal ini digunakan untuk menunjukkan peringatan ketika Manajer Proyek menarik dari kapasitas ini untuk persyaratan sumber daya yang terjadi setelah tanggal ini. |
| Kuantitas yang Dipesan | Jumlah jam peran yang dibeli dari vendor. Nilai ini digunakan untuk menunjukkan peringatan ketika Manajer Proyek menarik berlebihan dari kapasitas ini untuk persyaratan sumber daya. |
| Grup Unit | Nilai bidang ini di-default ke grup Unit waktu dan tidak dapat diubah.  |
| Unit | Bidang ini di-default ke unit dasar jam dari grup Unit waktu. Anda dapat mengubah nilai ini untuk membeli unit grup unit Waktu, seperti hari atau pekan. Kombinasi peran dan unit digunakan untuk menghitung harga unit untuk baris subkontrak. |
| Harga Unit | Harga unit di-default dari kombinasi peran dan unit dari daftar harga proyek yang berlaku untuk tanggal awal yang diminta dari baris subkontrak. Bila daftar harga proyek yang berlaku memiliki harga yang diatur dalam unit yang berbeda dari unit pada baris subkontrak, sistem akan menggunakan konversi unit untuk menghitung per harga unit. |
| Subtotal | Bidang hanya bisa dibaca ini secara otomatis dihitung sebagai **kuantitas x harga unit** jika nilai kuantitas dan harga unit dimasukkan. Jika salah satu kuantitas, Harga per unit, atau keduanya kosong, Anda dapat memasukkan nilai di bidang. |
| Pajak Penjualan |  Masukkan jumlah pajak penjualan. |
| Jumlah Total | Jumlah total baris Subkontrak setelah pajak disertakan. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

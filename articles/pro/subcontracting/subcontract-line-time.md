---
title: Baris Subkontrak untuk waktu
description: Artikel ini menjelaskan cara merekam baris subkontrak untuk waktu dan merekam pembelian waktu dari vendor.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ba013dd7ad023acc4f0cf077099c8c2c8d5bcd8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522236"
---
# <a name="subcontract-lines-for-time"></a>Baris Subkontrak untuk waktu

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Subkontrak dalam Dynamics 365 Project Operations dapat memiliki baris subkontrak untuk waktu. Baris subkontrak untuk waktu memungkinkan Manajer Proyek membeli waktu sumber daya vendor untuk mengadakan staf tugas proyek dan persyaratan sumber daya.

Selesaikan langkah-langkah berikut ini untuk membuat baris subkontrak untuk waktu di Project Operations.

1. Di panel navigasi, pilih **Subkontrak**, dan buka Subkontrak.
2. Pada tab **Baris Subkontrak**, pilih **Baru** untuk membuat baris subkontrak baru.
3. Pada halaman **Buat Cepat**, pada bidang **Kelas Transaksi**, pilih **Waktu**.
4. Masukkan informasi bidang tersisa dan kemudian pilih **Simpan**.

  Tabel berikut menyediakan informasi tentang bidang pada halaman **baris Subkontrak** dan halaman **Buat Cepat**.

| **Bidang** | **Deskripsi** | **Dampak Fungsional** |
| --- | --- | --- |
| Nama | Nama baris subkontrak untuk membantu identifikasi. | Ini akan ditampilkan sebagai kolom pertama di semua pencarian berdasarkan baris subkontrak. |
| KETERANGAN | Deskripsi singkat tentang layanan yang dibeli pada baris subkontrak. |Tidak Ada |
| Jenis Baris |   Bidang ini memiliki nilai default **berbasis Kuantitas**.| Tidak Ada |
| Metode Penagihan | Ini adalah rangkaian pilihan yang menunjukkan dua model kontrak utama yang didukung oleh Project Operations: **Harga Tetap** dan **waktu dan bahan**. | Berdasarkan metode penagihan yang dipilih, jadwal faktur berbasis tahapan disediakan untuk baris subkontrak dengan metode penagihan Harga Tetap. |
| Kelas Transaksi | Secara default, nilainya adalah **waktu**. | Ini menunjukkan bahwa baris subkontrak sedang digunakan untuk merekam pembelian waktu subkontraktor. |
| Peran | Pilih peran sumber daya subkontrak yang waktunya dibeli. | Peran yang dilakukan oleh sumber daya subkontrak menentukan biaya pembelian. |
| Awalan yang Diminta | Masukkan tanggal saat sumber daya subkontraktor diperlukan untuk mulai bekerja. | Ini digunakan untuk memilih daftar harga proyek dari daftar harga proyek yang dilampirkan ke subkontrak. Biaya peran pada baris subkontrak berasal dari daftar harga itu. |
| Akhir yang Diminta | Masukkan tanggal berakhirnya penetapan sumber daya subkontraktor. | Ini akan digunakan untuk menunjukkan peringatan ketika manajer proyek menarik dari kapasitas untuk persyaratan sumber daya yang terjadi setelah tanggal ini. |
| Kuantitas yang Dipesan | Masukkan jumlah jam peran yang dibeli dari vendor. | Ini akan digunakan untuk menunjukkan peringatan ketika manajer proyek terlalu banyak menarik kapasitas ini untuk persyaratan sumber daya. |
| Grup Unit | Nilai default adalah **Grup unit Waktu** yang tidak dapat diubah. | Tidak Ada|
| Unit | Default untuk bidang ini adalah unit dasar jam dari **grup Unit waktu**. Anda dapat mengubah nilai ini untuk membeli unit dari **grup unit Waktu**, seperti hari atau pekan. | Kombinasi **Peran** dan **Unit** akan digunakan sebagai default atau dihitung untuk harga unit untuk baris subkontrak. |
| Harga Unit | Harga unit default menggunakan kombinasi **Peran** dan **Unit** dari daftar harga proyek, yang berlaku untuk tanggal **Awal yang Diminta** baris subkontrak. | Bila daftar harga proyek yang berlaku memiliki harga yang diatur dalam unit yang berbeda dari unit pada baris subkontrak, sistem akan menggunakan konversi unit untuk menghitung per harga unit. |
| Subtotal |    Bidang ini bersifat hanya baca yang dihitung sebagai Kuantitas x harga Unit, jika nilai kuantitas dan harga unit dimasukkan. Jika salah satu kuantitas, Harga per unit, atau keduanya kosong, Anda dapat memasukkan nilai di bidang. | Tidak Ada|
| Pajak Penjualan |   Masukkan jumlah pajak penjualan. |Tidak Ada |
| Jumlah Total | Jumlah total baris Subkontrak termasuk pajak. Bidang ini dihitung sebagai subtotal + pajak penjualan.|Tidak Ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

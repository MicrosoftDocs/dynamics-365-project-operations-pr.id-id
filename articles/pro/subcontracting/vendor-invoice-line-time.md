---
title: Baris faktur vendor untuk waktu
description: Artikel ini menjelaskan cara mencatat baris faktur vendor untuk biaya waktu yang dimasukkan oleh subkontraktor.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262016"
---
# <a name="vendor-invoice-lines-for-time"></a>Baris faktur vendor untuk waktu

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk waktu yang tepat waktu. Manajer proyek dapat menggunakan baris faktur vendor untuk waktu guna mencatat biaya waktu subkontraktor pada proyek.

Baris faktur vendor untuk waktu mungkin atau mungkin tidak mereferensikan baris subkontrak untuk waktu. Jika baris faktur vendor untuk waktu mereferensikan subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi waktu yang ditagih oleh baris faktur vendor terhadap waktu yang dicatat oleh subkontraktor dan disetujui oleh manajer proyek pada proyek.

Tabel berikut ini menyediakan informasi tentang bidang pada baris faktur vendor untuk waktu.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor, untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Deskripsi | Deskripsi singkat tentang layanan yang sedang ditagih oleh vendor di baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak tempat layanan awalnya dipesan. | Ketika subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan tersebut. Faktur vendor tidak dapat memiliki baris faktur vendor yang mereferensikan subkontrak yang berbeda. |
| Baris subkontrak | Jalur subkontrak tempat layanan dipesan. Daftar baris subkontrak yang dapat dipilih terbatas pada baris pada subkontrak yang dipilih. | Ketika baris subkontrak dipilih pada baris faktur vendor untuk waktu, nilai default untuk **bidang sumber daya** Proyek **,** Peran **, dan** Dapat Dipesan dimasukkan dari bidang terkait pada baris subkontrak. Jika baris subkontrak yang dipilih memiliki nilai di **bidang Proyek**, **Peran**, dan **Dapat** Dipesan, nilai bidang terkait pada baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal ketika biaya aktual dari baris faktur vendor akan dicatat pada proyek. | Tidak ada |
| Kelas Transaksi | Secara default, nilainya adalah **waktu**. | Nilai **Waktu** menunjukkan bahwa baris faktur vendor sedang digunakan untuk mencatat jumlah faktur waktu subkontraktor. |
| Project | Nama proyek tempat layanan yang sedang ditagih digunakan. | Bidang ini diperlukan dan tidak dapat dibiarkan kosong. |
| Tugas | Nama tugas proyek tempat layanan yang sedang ditagih digunakan. Bidang ini hanya tersedia jika proyek dipilih. Pemilihan tugas proyek bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan waktu yang dicatat oleh sumber daya subkontraktor pada tugas proyek apa pun. Jika baris faktur vendor tidak mereferensikan baris subkontrak, dan bidang ini dibiarkan kosong, aktual biaya yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan yang tidak ditagih. Dalam hal ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagih ke pelanggan akhir. |
| Peran | Peran sumber daya subkontrak yang waktunya sedang ditagih. | Bidang ini menentukan peran yang dilakukan oleh sumber daya subkontrak yang waktunya ditagih pada faktur vendor. |
| Sumber daya yang dapat dipesan | Nama subkontraktor yang waktunya sedang ditagih. Pemilihan sumber daya yang dapat dipesan bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan waktu yang dicatat oleh sumber daya apa pun yang dimiliki oleh vendor pada baris faktur vendor. |
| Jumlah | Masukkan jumlah jam waktu yang sedang ditagih oleh vendor di baris faktur. |Tidak ada |
| Grup Unit | Nilai defaultnya adalah **Grup** unit waktu dan tidak dapat diubah. | Tidak ada |
| Unit | Nilai default adalah unit dasar jam dari grup unit waktu. Anda dapat mengubah nilai ini untuk dibeli di unit mana pun dari grup unit waktu, seperti hari atau minggu. | Kombinasi **nilai Peran** dan **Unit** akan digunakan sebagai nilai default atau komputasi untuk bidang Harga **satuan** pada baris faktur vendor. |
| Harga unit | Harga satuan **default menggunakan kombinasi nilai Peran** dan **Unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Jika harga untuk daftar harga proyek yang berlaku diatur dalam unit yang berbeda dari unit pada baris faktur vendor, sistem menggunakan konversi unit untuk menghitung harga per unit. |
| Subtotal | Bidang baca-saja ini dihitung sebagai *harga* Satuan Kuantitas&times;*·*, jika nilai dimasukkan dalam **bidang Kuantitas** dan **bidang Harga** satuan. Jika salah satu atau kedua bidang tersebut kosong, Anda bisa memasukkan nilai di bidang ini. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *pajak* + *Penjualan Subtotal*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

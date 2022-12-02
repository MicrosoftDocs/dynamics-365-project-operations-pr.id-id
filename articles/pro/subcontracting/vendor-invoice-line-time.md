---
title: Baris faktur vendor untuk waktu
description: Artikel ini menjelaskan cara merekam baris faktur vendor untuk biaya waktu yang dimasukkan subkontraktor.
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

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk waktu. Manajer proyek dapat menggunakan baris faktur vendor untuk waktu merekam biaya waktu subkontraktor pada proyek.

Baris faktur vendor untuk waktu tertentu belum tentu mereferensikan baris subkontrak untuk waktu. Jika baris faktur vendor untuk waktu mereferensikan subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi waktu yang ditagih oleh baris faktur vendor terhadap waktu yang direkam oleh subkontraktor dan disetujui oleh manajer proyek pada proyek.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk waktu.

| Bidang | Description | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Description | Deskripsi singkat tentang layanan yang ditagih oleh vendor di baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak tempat layanan awalnya dipesan. | Bila subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan tersebut. Faktur vendor tidak dapat memiliki baris faktur vendor yang mereferensikan subkontrak yang berbeda. |
| Baris subkontrak | Baris Subkontrak tempat layanan dipesan. Daftar baris subkontrak yang dapat dipilih terbatas pada baris pada subkontrak yang dipilih. | Bila baris subkontrak dipilih pada baris faktur vendor untuk waktu, nilai default untuk bidang **Proyek**, **Peran**, dan **sumber daya yang dapat dipesan** dimasukkan dari bidang yang berhubungan pada baris subkontrak. Jika baris subkontrak yang dipilih memiliki nilai di bidang **Proyek**, **Peran**, dan **Dapat Dipesan**, nilai bidang yang terkait di baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal saat biaya aktual baris faktur vendor akan direkam pada proyek. | Tidak ada |
| Kelas Transaksi | Secara default, nilainya adalah **waktu**. | Nilai **waktu** menunjukkan bahwa baris faktur vendor sedang digunakan untuk merekam jumlah faktur waktu subkontraktor. |
| Project | Nama proyek yang digunakan untuk layanan yang ditagih. | Bidang ini wajib dan tidak boleh dikosongkan. |
| Tugas | Nama tugas proyek yang digunakan untuk layanan yang ditagih. Bidang ini tersedia hanya jika proyek dipilih. Pilihan tugas proyek bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan waktu yang direkam oleh sumber daya subkontraktor pada tugas proyek apa pun. Jika baris faktur vendor tidak mereferensikan baris subkontrak dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan belum ditagih. Dalam kasus ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagihkan ke pelanggan akhir. |
| Peran | Peran sumber daya subkontrak yang waktunya ditagih. | Bidang ini menentukan peran yang dilakukan oleh sumber daya subkontrak yang waktunya ditagih pada faktur vendor. |
| Sumber daya yang dapat dipesan | Nama subkontraktor yang waktunya ditagih. Pilihan sumber daya yang dapat dipesan bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan waktu yang direkam oleh sumber daya milik vendor pada baris faktur vendor. |
| Jumlah | Masukkan jumlah jam waktu yang ditagihkan oleh vendor pada baris faktur. |Tidak ada |
| Grup Unit | Nilai default adalah **Grup unit Waktu** dan tidak dapat diubah. | Tidak ada |
| Unit | nilai defaultnya adalah unit dasar jam dari grup Unit waktu. Anda dapat mengubah nilai ini untuk membeli unit grup unit Waktu, seperti hari atau pekan. | Kombinasi nilai **Peran** dan **Unit** akan digunakan sebagai default atau nilai yang dihitung untuk bidang **harga unit** untuk baris faktur vendor. |
| Harga unit | Harga unit default menggunakan kombinasi nilai **peran** dan **unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Jika harga untuk daftar harga proyek diatur yang berbeda dari unit pada baris faktur vendor, sistem akan menggunakan konversi unit untuk menghitung per harga unit. |
| Subtotal | Bidang hanya baca ini dihitung sebagai *harga unit* &times; *kuantitas* jika nilai dimasukkan di bidang **Kuantitas** maupun bidang **Harga unit**. salah satu atau kedua bidang kosong, Anda dapat memasukkan nilai di bidang ini. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah Total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *subtotal* + *pajak penjualan*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

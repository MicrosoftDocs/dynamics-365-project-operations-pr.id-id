---
title: Baris faktur vendor untuk kategori pengeluaran
description: Artikel ini menjelaskan cara merekam baris faktur vendor untuk kategori pengeluaran.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261686"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Baris faktur vendor untuk kategori pengeluaran

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk kategori pengeluaran. Manajer proyek dapat menggunakan baris faktur vendor untuk kategori pengeluaran untuk merekam biaya layanan yang diperoleh sebagai kategori pengeluaran.

Baris faktur vendor untuk kategori pengeluaran belum tentu mereferensikan baris subkontrak untuk kategori pengeluaran. Jika baris faktur vendor untuk kategori pengeluaran mereferensikan subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi pengeluaran yang ditagih oleh baris faktur vendor terhadap pengeluaran yang direkam di kategori pengeluaran ini dan disetujui oleh manajer proyek pada proyek.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk kategori pengeluaran.

| Bidang | Description | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Description | Deskripsi singkat tentang layanan yang ditagih oleh vendor di baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak tempat layanan awalnya dipesan. | Bila subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan tersebut. Faktur vendor tidak dapat memiliki baris faktur vendor yang mereferensikan subkontrak yang berbeda. |
| Baris subkontrak | Baris Subkontrak tempat layanan dipesan. Daftar baris subkontrak yang dapat dipilih terbatas pada baris pada subkontrak yang dipilih. | Bila baris subkontrak dipilih pada baris faktur vendor untuk kategori pengeluaran, nilai default untuk bidang **Proyek**, **tugas**, dan **kategori transaksi** dimasukkan dari bidang yang berhubungan pada baris subkontrak. Jika baris subkontrak yang dipilih memiliki nilai di bidang **Proyek**, **tugas proyek**, dan **kategori transaksi**, nilai bidang yang terkait di baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal saat biaya aktual baris faktur vendor akan direkam pada proyek. |Tidak ada |
| Kelas Transaksi | Pilih **Pengeluaran** untuk merekam faktur vendor untuk kategori pengeluaran. | Nilai **Pengeluaran** menunjukkan bahwa baris faktur vendor sedang digunakan untuk merekam jumlah faktur untuk layanan yang diperoleh sebagai kategori pengeluaran. |
| Project | Nama proyek yang digunakan untuk layanan yang ditagih. | Bidang ini wajib dan tidak boleh dikosongkan. |
| Tugas | Nama tugas proyek yang digunakan untuk layanan yang ditagih. Bidang ini tersedia hanya jika proyek dipilih. Pilihan tugas proyek bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur dengan pengeluaran yang direkam pada tugas proyek apa pun. Jika baris faktur vendor tidak mereferensikan baris subkontrak dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan belum ditagih. Dalam kasus ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagihkan ke pelanggan akhir. |
| Kategori Transaksi | Kategori transaksi yang sedang ditagih. Kategori pengeluaran yang sesuai harus dibuat untuk kategori transaksi yang dipilih. | Kombinasi nilai **kategori transaksi** dan **Unit** akan digunakan sebagai default atau nilai yang dihitung untuk bidang **harga unit** untuk baris faktur vendor. |
| Jumlah | Masukkan kuantitas yang sedang ditagih oleh vendor di baris faktur. |Tidak ada|
| Grup Unit | Nilai default dimasukkan berdasarkan grup unit kategori transaksi yang dipilih. | Tidak ada |
| Unit | nilai defaultnya adalah unit dasar dari grup Unit yang dipilih. Anda dapat mengubah nilai ini untuk membeli unit grup unit. | Kombinasi nilai **kategori transaksi** dan **Unit** akan digunakan sebagai default atau nilai yang dihitung untuk bidang **harga unit** untuk baris faktur vendor. |
| Harga unit | Harga unit default menggunakan kombinasi nilai **kategori transaksi** dan **unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Jika harga untuk daftar harga proyek diatur yang berbeda dari unit pada baris faktur vendor, sistem akan menggunakan konversi unit untuk menghitung per harga unit. |
| Subtotal | Bidang hanya baca ini dihitung sebagai *harga unit* &times; *kuantitas* jika nilai dimasukkan di bidang **Kuantitas** maupun bidang **Harga unit**. salah satu atau kedua bidang kosong, Anda dapat memasukkan nilai di bidang ini.| Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah Total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *subtotal* + *pajak penjualan*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Baris faktur vendor untuk kategori pengeluaran
description: Ini topik menjelaskan cara merekam baris faktur vendor untuk kategori pengeluaran.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579540"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Baris faktur vendor untuk kategori pengeluaran

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk kategori pengeluaran. Manajer proyek dapat menggunakan jalur faktur vendor untuk kategori pengeluaran untuk mencatat biaya layanan yang diperoleh sebagai kategori pengeluaran.

Baris faktur vendor untuk kategori pengeluaran mungkin atau mungkin tidak merujuk jalur subkontrak untuk kategori pengeluaran. Jika baris faktur vendor untuk kategori pengeluaran merujuk pada subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi biaya yang ditagih oleh baris faktur vendor terhadap biaya yang dicatat pada kategori pengeluaran ini dan disetujui oleh manajer proyek pada proyek.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk kategori pengeluaran.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor, untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Deskripsi | Deskripsi singkat tentang layanan yang ditagih oleh vendor pada baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak yang awalnya dipesan oleh layanan. | Ketika subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan itu. Faktur vendor tidak dapat memiliki baris faktur vendor yang merujuk pada subkontrak yang berbeda. |
| Jalur subkontrak | Jalur subkontrak tempat layanan dipesan. Daftar jalur subkontrak yang dapat dipilih terbatas pada garis pada subkontrak yang dipilih. | Ketika garis subkontrak dipilih pada baris faktur vendor untuk kategori pengeluaran, nilai default untuk **bidang kategori** Proyek **,** Tugas **, dan** Transaksi dimasukkan dari bidang yang sesuai pada baris subkontrak. Jika baris subkontrak yang dipilih memiliki nilai di **bidang Proyek**, **tugas** Proyek, dan **kategori** Transaksi, nilai bidang yang sesuai pada baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal ketika biaya aktual dari baris faktur vendor akan dicatat pada proyek. |Tidak ada |
| Kelas Transaksi | Pilih **Biaya** untuk mencatat faktur vendor untuk kategori pengeluaran. | Nilai **Biaya** menunjukkan bahwa baris faktur vendor sedang digunakan untuk mencatat jumlah faktur untuk layanan yang diperoleh sebagai kategori pengeluaran. |
| Project | Nama proyek tempat layanan yang ditagih digunakan. | Bidang ini diperlukan dan tidak dapat dibiarkan kosong. |
| Tugas | Nama tugas proyek tempat layanan yang ditagih digunakan. Bidang ini hanya tersedia jika proyek dipilih. Pemilihan tugas proyek adalah opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan biaya yang dicatat pada tugas apa pun dari proyek. Jika baris faktur vendor tidak merujuk pada jalur subkontrak, dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan yang tidak ditagih. Dalam hal ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagih ke pelanggan akhir. |
| Kategori Transaksi | Kategori transaksi yang sedang ditagih. Kategori pengeluaran yang sesuai harus dibuat untuk kategori transaksi yang dipilih. | Kombinasi **kategori Transaksi dan** nilai Unit **akan digunakan sebagai nilai default atau dihitung untuk** bidang Harga **satuan pada** baris faktur vendor. |
| Jumlah | Masukkan jumlah yang ditagih oleh vendor pada baris faktur. |Tidak ada|
| Grup Unit | Nilai default dimasukkan berdasarkan grup unit dari kategori transaksi yang dipilih. | Tidak ada |
| Unit | Nilai default adalah unit dasar dari grup unit yang dipilih. Anda dapat mengubah nilai ini untuk membeli di unit mana pun dari grup unit. | Kombinasi **kategori Transaksi dan** nilai Unit **akan digunakan sebagai nilai default atau dihitung untuk** bidang Harga **satuan pada** baris faktur vendor. |
| Harga unit | Harga satuan default menggunakan kombinasi **kategori** Transaksi dan **nilai Unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Jika harga untuk daftar harga proyek yang berlaku diatur dalam unit yang berbeda dari unit pada baris faktur vendor, sistem menggunakan konversi unit untuk menghitung harga per unit. |
| Subtotal | Bidang baca-saja ini dihitung sebagai *harga* Satuan Kuantitas&times;*·*, jika nilai dimasukkan di **bidang Kuantitas** dan **bidang Harga** satuan. Jika salah satu atau kedua bidang tersebut kosong, Anda dapat memasukkan nilai di bidang ini.| Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *pajak* + *Penjualan Subtotal*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

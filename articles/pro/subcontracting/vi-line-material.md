---
title: Baris faktur vendor untuk produk
description: Ini topik menjelaskan cara merekam baris faktur vendor untuk produk dan menggunakan bidang yang berbeda untuk merekam pembelian produk dari vendor.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599182"
---
# <a name="vendor-invoice-lines-for-products"></a>Baris faktur vendor untuk produk

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki jalur faktur vendor untuk produk (juga disebut sebagai materi). Manajer proyek dapat menggunakan jalur faktur vendor untuk produk untuk mencatat biaya produk yang dibeli pada proyek.

Baris faktur vendor untuk produk mungkin atau mungkin tidak merujuk garis subkontrak untuk bahan. Jika baris faktur vendor untuk produk merujuk subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi produk yang ditagih oleh baris faktur vendor terhadap penggunaan produk yang dibeli yang dicatat dan disetujui oleh manajer proyek.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk produk.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor, untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Deskripsi | Deskripsi singkat tentang produk yang ditagih oleh vendor pada baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak tempat produk awalnya dipesan. | Ketika subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan itu. Faktur vendor tidak dapat memiliki baris faktur vendor yang merujuk pada subkontrak yang berbeda. |
| Jalur subkontrak | Garis subkontrak tempat produk dipesan. Daftar jalur subkontrak yang dapat dipilih terbatas pada garis pada subkontrak yang dipilih. | Ketika garis subkontrak dipilih pada baris faktur vendor untuk produk, nilai default untuk **bidang Proyek**, **Tugas**, dan **Produk** dimasukkan dari bidang yang sesuai pada jalur subkontrak. Jika baris subkontrak yang dipilih memiliki nilai di **bidang Proyek**, **Tugas**, dan **Produk**, nilai bidang yang sesuai pada baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal ketika biaya aktual dari baris faktur vendor akan dicatat pada proyek. | Tidak ada|
| Kelas Transaksi | Saat produk ditagih, bidang ini harus diatur ke **Materi**. | Nilai **Material** menunjukkan bahwa baris faktur vendor sedang digunakan untuk mencatat jumlah faktur untuk materi yang dibeli. |
| Project | Nama proyek tempat produk yang ditagih digunakan. | Bidang ini diperlukan dan tidak dapat dibiarkan kosong. |
| Tugas | Nama tugas proyek tempat produk yang ditagih digunakan. Bidang ini hanya tersedia jika proyek dipilih. Pemilihan tugas proyek adalah opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan produk yang dibeli yang digunakan pada tugas proyek apa pun. Jika baris faktur vendor tidak merujuk pada jalur subkontrak, dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan yang tidak ditagih. Dalam hal ini, jika penagihan berbasis tugas disiapkan, biaya tidak akan dapat ditagih ke pelanggan akhir. |
| Pilih produk | Pilih apakah produk yang ditagih adalah produk yang sudah ada dari katalog atau produk tertulis. | Nilai default dimasukkan dari garis subkontrak ketika garis subkontrak dipilih. |
| Produk | Pilih produk dari katalog. Jika produk adalah produk write-in, masukkan nama produk. | Bidang ini digunakan untuk memasukkan harga pembelian default untuk produk yang sudah ada. |
| Jumlah | Masukkan jumlah materi yang ditagih oleh vendor pada baris faktur ini. | Tidak ada |
| Grup Unit | Pilih grup unit unit tempat jumlah yang ditagih dinyatakan. | Tidak ada |
| Unit | Nilai default adalah unit dasar dari grup unit yang dipilih. Anda dapat mengubah nilai ini untuk membayar di unit mana pun dari grup unit yang dipilih. | Kombinasi nilai **Produk** dan **Unit** akan digunakan sebagai nilai default atau dihitung untuk **bidang Harga** satuan pada baris faktur vendor. |
| Harga unit | Harga satuan default menggunakan kombinasi **nilai Produk** dan **Unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Tidak ada |
| Subtotal | Bidang baca-saja ini dihitung sebagai *harga* Satuan Kuantitas&times;*·*, jika nilai dimasukkan di **bidang Kuantitas** dan **bidang Harga** satuan. Jika salah satu atau kedua bidang tersebut kosong, Anda dapat memasukkan nilai di bidang ini. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *pajak* + *Penjualan Subtotal*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

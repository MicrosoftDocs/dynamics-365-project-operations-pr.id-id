---
title: Baris faktur vendor untuk produk
description: Artikel ini menjelaskan cara mencatat baris faktur vendor untuk produk dan menggunakan bidang yang berbeda untuk mencatat pembelian produk dari vendor.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261562"
---
# <a name="vendor-invoice-lines-for-products"></a>Baris faktur vendor untuk produk

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk produk (juga disebut sebagai materi). Manajer proyek dapat menggunakan baris faktur vendor untuk produk guna mencatat biaya produk yang dibeli pada proyek.

Baris faktur vendor untuk produk mungkin atau mungkin tidak merujuk pada baris subkontrak untuk materi. Jika baris faktur vendor untuk produk mereferensikan subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi produk yang sedang ditagih oleh baris faktur vendor terhadap penggunaan produk yang dibeli yang dicatat dan disetujui oleh manajer proyek.

Tabel berikut ini menyediakan informasi tentang bidang pada baris faktur vendor untuk produk.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor, untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Deskripsi | Deskripsi singkat tentang produk yang sedang ditagih oleh vendor di baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak tempat produk awalnya dipesan. | Ketika subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan tersebut. Faktur vendor tidak dapat memiliki baris faktur vendor yang mereferensikan subkontrak yang berbeda. |
| Baris subkontrak | Jalur subkontrak tempat produk dipesan. Daftar baris subkontrak yang dapat dipilih terbatas pada baris pada subkontrak yang dipilih. | Ketika baris subkontrak dipilih pada baris faktur vendor untuk produk, nilai default untuk **bidang Proyek**, **Tugas**, dan **Produk** dimasukkan dari bidang yang sesuai pada baris subkontrak. Jika baris subkontrak yang dipilih memiliki nilai di **bidang Proyek**, **Tugas**, dan **Produk**, nilai bidang terkait pada baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal ketika biaya aktual dari baris faktur vendor akan dicatat pada proyek. | Tidak ada|
| Kelas Transaksi | Ketika produk ditagih, bidang ini harus diatur ke **Materi**. | Materi nilai **menunjukkan** bahwa baris faktur vendor digunakan untuk mencatat jumlah faktur untuk materi yang dibeli. |
| Project | Nama proyek tempat produk yang sedang ditagih digunakan. | Bidang ini diperlukan dan tidak dapat dibiarkan kosong. |
| Tugas | Nama tugas proyek tempat produk yang sedang ditagih digunakan. Bidang ini hanya tersedia jika proyek dipilih. Pemilihan tugas proyek bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan produk yang dibeli yang digunakan pada tugas proyek apa pun. Jika baris faktur vendor tidak mereferensikan baris subkontrak, dan bidang ini dibiarkan kosong, aktual biaya yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan yang tidak ditagih. Dalam hal ini, jika penagihan berbasis tugas disiapkan, biaya tidak akan dapat ditagih ke pelanggan akhir. |
| Pilih Produk | Pilih apakah produk yang sedang ditagih adalah produk yang sudah ada dari katalog atau produk tulis-masuk. | Nilai default dimasukkan dari baris subkontrak saat baris subkontrak dipilih. |
| Produk | Pilih produk dari katalog. Jika produk tersebut adalah produk yang masuk, masukkan nama produk. | Bidang ini digunakan untuk memasukkan harga pembelian default untuk produk yang ada. |
| Jumlah | Masukkan jumlah materi yang sedang ditagih oleh vendor pada baris faktur ini. | Tidak ada |
| Grup Unit | Pilih grup unit unit tempat jumlah yang sedang ditagih dinyatakan. | Tidak ada |
| Unit | Nilai default adalah unit dasar dari grup unit yang dipilih. Anda dapat mengubah nilai ini untuk membayar di unit mana pun dari grup unit yang dipilih. | Kombinasi **nilai Produk** dan **Unit** akan digunakan sebagai nilai default atau komputasi untuk **bidang Harga** satuan pada baris faktur vendor. |
| Harga unit | Harga satuan **default menggunakan kombinasi nilai Produk** dan **Unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Tidak ada |
| Subtotal | Bidang baca-saja ini dihitung sebagai *harga* Satuan Kuantitas&times;*·*, jika nilai dimasukkan dalam **bidang Kuantitas** dan **bidang Harga** satuan. Jika salah satu atau kedua bidang tersebut kosong, Anda bisa memasukkan nilai di bidang ini. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *pajak* + *Penjualan Subtotal*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

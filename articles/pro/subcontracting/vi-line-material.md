---
title: Baris faktur vendor untuk produk
description: Artikel ini menjelaskan cara merekam baris faktur vendor produk dan menggunakan bidang berbeda untuk merekam pembelian produk vendor.
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

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk produk (juga disebut sebagai bahan). Manajer proyek dapat menggunakan baris faktur vendor untuk produk untuk merekam biaya produk yang dibeli pada proyek.

Baris faktur vendor untuk produk belum tentu mereferensikan baris subkontrak untuk bahan. Jika baris faktur vendor untuk produk mereferensikan subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi produk yang ditagih oleh baris faktur vendor terhadap penggunaan produk yang dibeli yang direkam oleh subkontraktor dan disetujui oleh manajer proyek.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk produk.

| Bidang | Description | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Description | Deskripsi singkat tentang produk yang ditagih oleh vendor di baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak yang produknya awalnya dipesan. | Bila subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan tersebut. Faktur vendor tidak dapat memiliki baris faktur vendor yang mereferensikan subkontrak yang berbeda. |
| Baris subkontrak | Baris Subkontrak tempat produk dipesan. Daftar baris subkontrak yang dapat dipilih terbatas pada baris pada subkontrak yang dipilih. | Bila baris subkontrak dipilih pada baris faktur vendor untuk produk, nilai default untuk bidang **Proyek**, **tugas**, dan **produk** dimasukkan dari bidang yang berhubungan pada baris subkontrak. Jika baris subkontrak yang dipilih memiliki nilai di bidang **Proyek**, **tugas**, dan **Produk**, nilai bidang yang terkait di baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal saat biaya aktual baris faktur vendor akan direkam pada proyek. | Tidak ada|
| Kelas Transaksi | Bila produk ditagih, bidang ini harus diatur ke **bahan**. | Nilai **Bahan** menunjukkan bahwa baris faktur vendor sedang digunakan untuk merekam jumlah faktur untuk bahan yang dibeli. |
| Project | Nama proyek yang digunakan untuk produk yang ditagih. | Bidang ini wajib dan tidak boleh dikosongkan. |
| Tugas | Nama tugas proyek yang digunakan untuk produk yang ditagih. Bidang ini tersedia hanya jika proyek dipilih. Pilihan tugas proyek bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur dengan produk yang dibeli yang digunakan pada tugas proyek apa pun. Jika baris faktur vendor tidak mereferensikan baris subkontrak dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan belum ditagih. Dalam kasus ini, jika penagihan berbasis tugas disiapkan, biaya tidak akan dapat ditagihkan ke pelanggan akhir. |
| Pilih Produk | Pilih apakah produk yang ditagih adalah produk yang sudah ada dari katalog atau produk pilihan. | Nilai default dimasukkan dari baris subkontrak saat baris subkontrak dipilih. |
| Produk | Pilih produk dari katalog. Jika produk adalah produk pilihan, masukkan nama produk. | Bidang ini digunakan untuk memasukkan harga pembelian default untuk produk yang ada. |
| Jumlah | Masukkan kuantitas bahan yang sedang ditagih oleh vendor di baris faktur ini. | Tidak ada |
| Grup Unit | Pilih grup unit dari unit yang kuantitas ditagihnya diekspresikan. | Tidak ada |
| Unit | nilai defaultnya adalah unit dasar dari grup Unit yang dipilih. Anda dapat mengubah nilai ini untuk membayar unit grup yang dipilih. | Kombinasi nilai **produk** dan **Unit** akan digunakan sebagai default atau nilai yang dihitung untuk bidang **harga unit** untuk baris faktur vendor. |
| Harga unit | Harga unit default menggunakan kombinasi nilai **Produk** dan **unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Tidak ada |
| Subtotal | Bidang hanya baca ini dihitung sebagai *harga unit* &times; *kuantitas* jika nilai dimasukkan di bidang **Kuantitas** maupun bidang **Harga unit**. salah satu atau kedua bidang kosong, Anda dapat memasukkan nilai di bidang ini. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah Total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *subtotal* + *pajak penjualan*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

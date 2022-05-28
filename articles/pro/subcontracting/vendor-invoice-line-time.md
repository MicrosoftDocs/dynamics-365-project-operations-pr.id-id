---
title: Baris faktur vendor untuk waktu
description: Ini topik menjelaskan cara merekam jalur faktur vendor untuk biaya waktu yang dimasukkan subkontraktor.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597204"
---
# <a name="vendor-invoice-lines-for-time"></a>Baris faktur vendor untuk waktu

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk waktu tertentu. Manajer proyek dapat menggunakan jalur faktur vendor untuk waktu untuk mencatat biaya waktu subkontraktor pada proyek.

Baris faktur vendor untuk waktu mungkin atau mungkin tidak merujuk garis subkontrak untuk waktu. Jika baris faktur vendor untuk referensi waktu subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi waktu yang ditagih oleh baris faktur vendor terhadap waktu yang dicatat oleh subkontraktor dan disetujui oleh manajer proyek pada proyek.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk waktu.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor, untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Deskripsi | Deskripsi singkat tentang layanan yang ditagih oleh vendor pada baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak yang awalnya dipesan oleh layanan. | Ketika subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan itu. Faktur vendor tidak dapat memiliki baris faktur vendor yang merujuk pada subkontrak yang berbeda. |
| Jalur subkontrak | Jalur subkontrak tempat layanan dipesan. Daftar jalur subkontrak yang dapat dipilih terbatas pada garis pada subkontrak yang dipilih. | Ketika garis subkontrak dipilih pada baris faktur vendor untuk waktu, nilai default untuk **bidang Proyek**, **Peran**, dan **Sumber daya** yang dapat dipesan dimasukkan dari bidang yang sesuai pada baris subkontrak. Jika garis subkontrak yang dipilih memiliki nilai di **bidang Proyek**, **Peran**, dan **Dapat** Dipesan, nilai bidang yang sesuai pada baris faktur vendor tidak dapat berbeda dari nilai tersebut. |
| Tanggal transaksi | Tanggal ketika biaya aktual dari baris faktur vendor akan dicatat pada proyek. | Tidak ada |
| Kelas Transaksi | Secara default, nilainya adalah **waktu**. | Nilai **Waktu** menunjukkan bahwa baris faktur vendor sedang digunakan untuk mencatat jumlah faktur waktu subkontraktor. |
| Project | Nama proyek tempat layanan yang ditagih digunakan. | Bidang ini diperlukan dan tidak dapat dibiarkan kosong. |
| Tugas | Nama tugas proyek tempat layanan yang ditagih digunakan. Bidang ini hanya tersedia jika proyek dipilih. Pemilihan tugas proyek adalah opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan waktu yang dicatat oleh sumber daya subkontraktor pada tugas proyek apa pun. Jika baris faktur vendor tidak merujuk pada jalur subkontrak, dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan yang tidak ditagih. Dalam hal ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagih ke pelanggan akhir. |
| Peran | Peran sumber daya subkontrak yang waktunya ditagih. | Bidang ini menentukan peran yang dilakukan oleh sumber daya subkontrak yang waktunya ditagih pada faktur vendor. |
| Sumber daya yang dapat dipesan | Nama subkontraktor yang waktunya ditagih. Pemilihan sumber daya yang dapat dipesan adalah opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan waktu yang dicatat oleh sumber daya apa pun milik vendor pada baris faktur vendor. |
| Jumlah | Masukkan jumlah jam waktu yang ditagih oleh vendor pada baris faktur. |Tidak ada |
| Grup Unit | Nilai default adalah **grup** unit Waktu dan tidak dapat diubah. | Tidak ada |
| Unit | Nilai default adalah unit dasar jam dari grup unit waktu. Anda dapat mengubah nilai ini untuk membeli di unit mana pun dari grup unit waktu, seperti hari atau minggu. | Kombinasi nilai **Peran** dan **Unit** akan digunakan sebagai nilai default atau dihitung untuk **bidang Harga** satuan pada baris faktur vendor. |
| Harga unit | Harga satuan default menggunakan kombinasi **nilai Peran** dan **Unit** dari daftar harga proyek yang berlaku untuk tanggal transaksi baris faktur vendor. | Jika harga untuk daftar harga proyek yang berlaku diatur dalam unit yang berbeda dari unit pada baris faktur vendor, sistem menggunakan konversi unit untuk menghitung harga per unit. |
| Subtotal | Bidang baca-saja ini dihitung sebagai *harga* Satuan Kuantitas&times;*·*, jika nilai dimasukkan di **bidang Kuantitas** dan **bidang Harga** satuan. Jika salah satu atau kedua bidang tersebut kosong, Anda dapat memasukkan nilai di bidang ini. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *pajak* + *Penjualan Subtotal*. | Tidak ada |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

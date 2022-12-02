---
title: Baris faktur vendor untuk tahapan
description: Artikel ini menjelaskan cara membuat baris faktur vendor untuk tahapan pada subkontrak.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261031"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Baris faktur vendor untuk tahapan

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk tahapan yang ditentukan pada baris subkontrak. Manajer proyek dapat menggunakan baris faktur vendor pada tahapannya untuk merekam biaya layanan yang diperoleh sebagai biaya berbasis tahapan yang dikeluarkan pada layanan atau produk yang diperoleh untuk proyek.

Baris faktur vendor untuk tahapan harus selalu mereferensikan baris subkontrak yang memiliki metode penagihan harga tetap. Jika baris faktur vendor untuk tahapan mereferensikan baris subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi biaya yang mendasari dari waktu, pengeluaran, atau bahan yang mereferensikan baris subkontrak itu terhadap tahapan yang ditagih oleh vendor.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk tahapan.

| Bidang | Description | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Description | Deskripsi singkat tentang layanan yang ditagih oleh vendor di baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak tempat layanan awalnya dipesan. | Bila subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan tersebut. Faktur vendor tidak dapat memiliki baris faktur vendor yang mereferensikan subkontrak yang berbeda. |
| Baris subkontrak | Baris Subkontrak tempat layanan dipesan. Daftar baris subkontrak yang dapat dipilih terbatas pada baris pada subkontrak yang dipilih. | Bila baris subkontrak dipilih pada baris faktur vendor untuk tahapan, bidang **Peran** dan **kategori Transaksi**, dan bidang terkait produk, tidak relevan dan tidak tersedia. Bidang **Kuantitas**, **Unit**, dan **Grup Unit** juga tidak relevan untuk baris faktur vendor berbasis tahapan. |
| Tanggal transaksi | Tanggal saat biaya aktual baris faktur vendor akan direkam pada proyek. | Tidak ada |
| Kelas Transaksi | Pilih **Tahapan** untuk merekam faktur vendor untuk prestasi yang telah selesai dan ditentukan pada baris subkontrak. | Tidak ada |
| Tahap | Pilih tahapan yang didefinisikan pada baris subkontrak terkait yang ditandai sebagai **Siap untuk Faktur**. | Tahapan Baris subkontrak yang telah memiliki status **Siap untuk Faktur** dapat dipilih di baris faktur vendor. |
| Project | Nama proyek yang digunakan untuk layanan yang ditagih. | Bidang ini wajib dan tidak boleh dikosongkan. |
| Tugas | Nama tugas proyek yang digunakan untuk layanan yang ditagih. Bidang ini tersedia hanya jika proyek dipilih. Pilihan tugas proyek bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan kelas transaksi di baris subkontrak yang direkam oleh sumber daya subkontraktor pada tugas proyek apa pun. Jika baris faktur vendor tidak mereferensikan baris subkontrak dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan belum ditagih. Dalam kasus ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagihkan ke pelanggan akhir. |
| Jumlah tonggak | Masukkan nilai tahapan yang didefinisikan pada baris subkontrak yang siap untuk Faktur. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah Total | Jumlah total baris faktur vendor, termasuk pajak. Bidang hanya baca ini dihitung *Jumlah tahapan* + *Pajak penjualan*. | Tidak ada |

> [!NOTE]
> Ketika baris faktur vendor yang mereferensikan tahapan baris subkontrak dibuat, status tahapan subkontrak diperbarui ke **faktur Vendor dibuat**. Kemudian, ketika faktur vendor dikonfirmasi, status tahapan baris subkontrak diperbarui ke **faktur Vendor dikonfirmasi**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

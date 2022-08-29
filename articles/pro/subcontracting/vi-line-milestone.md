---
title: Baris faktur vendor untuk tahapan
description: Artikel ini menjelaskan cara membuat baris faktur vendor untuk pencapaian pada subkontrak.
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

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk pencapaian yang ditentukan pada baris subkontrak. Manajer proyek dapat menggunakan baris faktur vendor untuk tonggak sejarah untuk mencatat biaya layanan yang diperoleh sebagai biaya berbasis tonggak sejarah yang dikeluarkan pada layanan atau produk yang diperoleh untuk proyek.

Baris faktur vendor untuk pencapaian harus selalu mereferensikan baris subkontrak yang memiliki metode penagihan harga Tetap. Ketika baris faktur vendor untuk tonggak pencapaian mereferensikan baris subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi biaya waktu, pengeluaran, atau materi yang mendasarinya yang mereferensikan baris subkontrak tersebut terhadap tonggak pencapaian yang sedang ditagih oleh vendor.

Tabel berikut ini menyediakan informasi tentang bidang pada baris faktur vendor untuk pencapaian.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor, untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Deskripsi | Deskripsi singkat tentang layanan yang sedang ditagih oleh vendor di baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak tempat layanan awalnya dipesan. | Ketika subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan tersebut. Faktur vendor tidak dapat memiliki baris faktur vendor yang mereferensikan subkontrak yang berbeda. |
| Baris subkontrak | Jalur subkontrak tempat layanan dipesan. Daftar baris subkontrak yang dapat dipilih terbatas pada baris pada subkontrak yang dipilih. | Ketika baris subkontrak dipilih pada baris faktur vendor untuk pencapaian, **bidang kategori** Peran **dan** Transaksi, dan bidang terkait produk, tidak relevan dan tidak tersedia. Bidang **Kuantitas**, **Unit**, dan **grup** Unit juga tidak relevan untuk baris faktur vendor berbasis pencapaian. |
| Tanggal transaksi | Tanggal ketika biaya aktual dari baris faktur vendor akan dicatat pada proyek. | Tidak ada |
| Kelas Transaksi | Pilih **Milestone** untuk merekam faktur vendor untuk milestone yang telah selesai yang ditentukan pada baris subkontrak. | Tidak ada |
| Tahap | Pilih tonggak pencapaian yang ditentukan pada baris subkontrak terkait yang ditandai sebagai **Siap Untuk Faktur**. | Subkontrakkan tonggak baris yang memiliki status **Siap untuk faktur** dapat dipilih pada baris faktur vendor. |
| Project | Nama proyek tempat layanan yang sedang ditagih digunakan. | Bidang ini diperlukan dan tidak dapat dibiarkan kosong. |
| Tugas | Nama tugas proyek tempat layanan yang sedang ditagih digunakan. Bidang ini hanya tersedia jika proyek dipilih. Pemilihan tugas proyek bersifat opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan kelas transaksi pada baris subkontrak terkait yang dicatat pada tugas apa pun dari proyek. Jika baris faktur vendor tidak mereferensikan baris subkontrak, dan bidang ini dibiarkan kosong, aktual biaya yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan yang tidak ditagih. Dalam hal ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagih ke pelanggan akhir. |
| Jumlah tonggak | Masukkan nilai tonggak pencapaian yang ditentukan pada baris subkontrak yang siap untuk ditagih. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *Jumlah* + *milestone Pajak* penjualan. | Tidak ada |

> [!NOTE]
> Ketika baris faktur vendor yang mereferensikan tonggak baris subkontrak dibuat, status tonggak subkontrak diperbarui ke **faktur Vendor yang dibuat**. Kemudian, ketika faktur vendor tersebut dikonfirmasi, status tonggak baris subkontrak diperbarui ke **faktur Vendor yang dikonfirmasi**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

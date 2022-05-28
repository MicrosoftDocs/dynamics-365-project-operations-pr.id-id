---
title: Baris faktur vendor untuk tonggak sejarah
description: Ini topik menjelaskan cara membuat baris faktur vendor untuk tonggak pada subkontrak.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590626"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Baris faktur vendor untuk tonggak sejarah

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Faktur vendor di Microsoft Dynamics 365 Project Operations dapat memiliki baris faktur vendor untuk tonggak yang ditentukan pada jalur subkontrak. Manajer proyek dapat menggunakan jalur faktur vendor untuk tonggak sejarah untuk mencatat biaya layanan yang diperoleh sebagai biaya berbasis tonggak yang dikeluarkan pada layanan atau produk yang diperoleh untuk proyek tersebut.

Baris faktur vendor untuk tonggak sejarah harus selalu merujuk garis subkontrak yang memiliki metode penagihan harga tetap. Ketika garis faktur vendor untuk tonggak referensi garis subkontrak, manajer proyek akan dapat mencocokkan dan memverifikasi biaya yang mendasari waktu, pengeluaran, atau bahan yang referensi yang referensi yang subkontrak baris terhadap tonggak yang sedang ditagih oleh vendor.

Tabel berikut memberikan informasi tentang bidang pada baris faktur vendor untuk tonggak sejarah.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama baris faktur vendor, untuk membantu identifikasi. | Nama ini akan ditampilkan sebagai kolom pertama di semua pencarian yang didasarkan pada baris faktur vendor. |
| Deskripsi | Deskripsi singkat tentang layanan yang ditagih oleh vendor pada baris faktur vendor. | Tidak ada |
| Subkontrak | Subkontrak yang awalnya dipesan oleh layanan. | Ketika subkontrak dipilih untuk faktur vendor, semua baris pada faktur vendor akan mewarisi pilihan itu. Faktur vendor tidak dapat memiliki baris faktur vendor yang merujuk pada subkontrak yang berbeda. |
| Jalur subkontrak | Jalur subkontrak tempat layanan dipesan. Daftar jalur subkontrak yang dapat dipilih terbatas pada garis pada subkontrak yang dipilih. | Ketika garis subkontrak dipilih pada baris faktur vendor untuk tonggak sejarah, **bidang kategori** Peran **dan** Transaksi, dan bidang terkait produk, tidak relevan dan tidak tersedia. Bidang **Grup** Kuantitas **,** Unit **, dan** Unit juga tidak relevan untuk jalur faktur vendor berbasis tonggak sejarah. |
| Tanggal transaksi | Tanggal ketika biaya aktual dari baris faktur vendor akan dicatat pada proyek. | Tidak ada |
| Kelas Transaksi | Pilih **Milestone** untuk merekam faktur vendor untuk tonggak pencapaian yang telah selesai yang ditentukan pada jalur subkontrak. | Tidak ada |
| Tahap | Pilih tonggak yang ditentukan pada baris subkontrak terkait yang ditandai sebagai **Ready to Invoice**. | Tonggak jalur subkontrak yang memiliki status **Siap faktur** dapat dipilih pada baris faktur vendor. |
| Project | Nama proyek tempat layanan yang ditagih digunakan. | Bidang ini diperlukan dan tidak dapat dibiarkan kosong. |
| Tugas | Nama tugas proyek tempat layanan yang ditagih digunakan. Bidang ini hanya tersedia jika proyek dipilih. Pemilihan tugas proyek adalah opsional. | Jika bidang ini dibiarkan kosong, manajer proyek dapat mencocokkan baris faktur vendor dengan kelas transaksi pada jalur subkontrak terkait yang dicatat pada tugas proyek apa pun. Jika baris faktur vendor tidak merujuk pada jalur subkontrak, dan bidang ini dibiarkan kosong, biaya aktual yang dibuat oleh baris faktur vendor tidak akan ditautkan ke aktual penjualan yang tidak ditagih. Dalam hal ini, jika penagihan berbasis tugas disiapkan, biaya mungkin tidak dapat ditagih ke pelanggan akhir. |
| Jumlah tonggak | Masukkan nilai tonggak yang ditentukan pada garis subkontrak yang siap ditagih. | Tidak ada |
| Pajak penjualan | Masukkan jumlah pajak penjualan. | Tidak ada |
| Jumlah total | Jumlah total baris faktur vendor, termasuk pajak. Bidang ini dihitung sebagai *Jumlah tonggak* + *pajak* penjualan. | Tidak ada |

> [!NOTE]
> Saat baris faktur vendor yang merujuk pada tonggak garis subkontrak dibuat, status tonggak subkontrak diperbarui ke **faktur Penjual yang dibuat**. Kemudian, ketika faktur vendor tersebut dikonfirmasi, status tonggak jalur subkontrak diperbarui ke **faktur Vendor dikonfirmasi**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

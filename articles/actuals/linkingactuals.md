---
title: Asal transaksi - Tautkan aktual ke sumbernya
description: Artikel ini menjelaskan bagaimana konsep asal transaksi digunakan untuk menautkan aktual ke rekaman sumber asli seperti entri waktu, entri pengeluaran, atau log penggunaan bahan.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921306"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Asal transaksi - Tautkan aktual ke sumbernya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Rekaman asal transaksi dibuat untuk menautkan aktual ke sumbernya, entri waktu, entri pengeluaran, log penggunaan bahan, dan faktur proyek.

Contoh berikut menunjukkan pemrosesan tipikal waktu entri dalam siklus hidup proyek Project Operations.

> ![Memproses entri waktu di Project Operations.](media/basic-guide-17.png)
 
1. Pengajuan entri waktu menyebabkan dua baris jurnal dibuat: satu untuk biaya dan satu untuk penjualan yang belum ditagih.
2. Persetujuan akhir entri waktu menyebabkan dua nilai aktual dibuat: satu untuk biaya dan satu untuk penjualan yang belum ditagih.
3. Saat pengguna membuat faktur proyek, transaksi baris faktur dibuat menggunakan data dari nilai aktual penjualan yang belum ditagih.
4. Setelah faktur dikonfirmasi, dua aktual baru dibuat: pembalikan aktual penjualan yang belum ditagih dan penjualan tertagih.

Setiap aktivitas dalam alur kerja pemrosesan ini memicu pembuatan rekaman di entitas asal transaksi untuk membantu membuat jejak Relasi antara rekaman yang dibuat sepanjang waktu masuk, baris jurnal, aktual, dan rincian baris faktur.

Tabel berikut Menampilkan rekaman di entitas asal transaksi untuk alur kerja sebelumnya.

| Aktivitas                        | Asal                   | Jenis Asal                       | Transaksi                       | Jenis Transaksi         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Pengajuan entri waktu        | GUID Rekaman Entri Waktu   | Entri Waktu                        | GUID Rekaman baris jurnal (biaya)   | Lini Jurnal             |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman baris jurnal (penjualan)  | Lini Jurnal                      |                          |
| Persetujuan Waktu                | GUID Rekaman baris jurnal | Lini Jurnal                      | GUID Rekaman Penjualan Belum Tertagih        | Aktual                   |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman Penjualan Belum Tertagih        | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Rekaman Aktual Biaya           | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman Aktual Biaya           | Aktual                            |                          |
| Pembuatan Faktur             | GUID Rekaman Entri Waktu   | Entri Waktu                        | GUID Transaksi Baris Faktur     | Transaksi Baris Faktur |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Transaksi Baris Faktur     | Transaksi Baris Faktur          |                          |
| Konfirmasi Faktur         | GUID Baris Faktur        | Baris Faktur                      | GUID Rekaman Penjualan Tertagih          | Aktual                   |
| GUID faktur                 | Faktur                  | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rincian Baris Faktur     | Rincian Baris Faktur      | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Rekaman Penjualan Tertagih          | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Pembalikan penjualan yang tidak ditagih      | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Pembalikan penjualan yang tidak ditagih      | Aktual                            |                          |
| Koreksi faktur draft     | GUID ILD lama             | Transaksi Baris Faktur          | GUID ILD Koreksi               | Transaksi Baris Faktur |
| GUID IL Lama                  | Baris Faktur             | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| GUID faktur lama             | Faktur                  | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID ILD Koreksi               | Transaksi Baris Faktur          |                          |
| Koreksi faktur dikonfirmasi | GUID ILD lama             | Transaksi Baris Faktur          | GUID aktual penjualan ditagih terbalik | Aktual                   |
| GUID IL Lama                  | Baris Faktur             | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID faktur lama             | Faktur                  | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID aktual penjualan ditagih terbalik | Aktual                            |                          |
| GUID ILD lama                 | Transaksi Baris Faktur | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID IL Lama                  | Baris Faktur             | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID faktur lama             | Faktur                  | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID Rekaman Entri Waktu       | Entri Waktu               | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID Rekaman baris jurnal     | Lini Jurnal             | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID ILD Koreksi          | Transaksi Baris Faktur | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID IL Koreksi           | Baris Faktur             | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |
| GUID faktur Koreksi      | Faktur                  | GUID Aktual penjualan Belum Tertagih Baru    | Aktual                            |                          |


Ilustrasi berikut menampilkan tautan yang dibuat antara berbagai jenis aktual dan sumbernya pada berbagai aktivitas menggunakan contoh entri waktu di Project Operations.

> ![Cara aktual ditautkan ke rekaman sumber di Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Mengimpor estimasi untuk proyek pada baris kuotasi proyek
description: Artikel ini menyediakan informasi tentang mengimpor perkiraan dari proyek ke baris kutipan proyek.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: dc5b6279a2123604291da35c9da2bf63dbe475b7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915050"
---
# <a name="import-estimates-for-a-project-to-a-project-quote-line"></a>Mengimpor estimasi untuk proyek pada baris kuotasi proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Jika proyek dibuat selama tahap pra-penjualan, Anda dapat memilih untuk mengimpor perkiraan keuangan dari proyek ke baris kuotasi berbasis proyek.

1. Pastikan baris kuotasi berbasis proyek memiliki informasi proyek di bidang **proyek**.
2. Di tab **detail baris kuotasi**, pilih **Impor dari Estimasi Proyek**.
3. Di halaman dialog terbuka, pilih salah satu pilihan ringkasan berikut:

  - **Kelas Transaksi**
  - **Kategori**
  - **Peran** 
  - **Tugas proyek**

Berdasarkan pilihan Anda, perkiraan dari proyek untuk semua kelas transaksi yang tercakup dalam baris kuotasi ini disalin. Untuk memeriksa jenis kelas transaksi yang disertakan, pilih tab **Umum** pada baris kuotasi berbasis proyek, dan periksa nilai untuk **mencakup waktu**, **mencakup pengeluaran**, dan **mencakup biaya**.

Bila Anda mengimpor perkiraan, sistem akan default ke harga berdasarkan daftar harga proyek yang dilampirkan ke kuotasi dan jenis penagihan yang diatur pada baris kuotasi berbasis proyek. Jika peran atau kategori diatur pada baris kuotasi berbasis proyek sebagai tidak dikenakan biaya, baris estimasi impor akan ditetapkan sebagai tidak dikenai biaya dan tidak akan menambahkan hingga nilai baris kuotasi yang dikutip.

Bila baris kuotasi memiliki detail baris, **nilai kuotasi** dan bidang **perkiraan pajak** pada baris kuotasi diringkas dan tidak dapat diedit.

Bila pilihan beberapa ringkasan dipilih, sistem akan mencoba meringkas semua pilihan yang dipilih. Hasilnya adalah bahwa output baris kuotasi impor akan lebih dari jika Anda memilih hanya satu pilihan ringkasan.

Misalnya, jika proyek memiliki baris estimasi berikut untuk pengeluaran.

| Tugas | Kategori | Tanggal | Quantity | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tiket pesawat | 1/10/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Bila pengguna memilih untuk meringkas berdasarkan kelas transaksi, informasi berikut akan diimpor.

| Tugas | Kategori | Tanggal | Quantity | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| | | 1/10/2020 | 3.34 | 840 | 2800 |

Bila pengguna memilih untuk meringkas berdasarkan kelas transaksi dan Kategori, informasi berikut akan diimpor.

| Tugas | Kategori | Tanggal | Quantity | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tiket pesawat | 1/10/2020 | 4 | 400 | 1600 |
| | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Bila pengguna memilih untuk meringkas berdasarkan kelas transaksi, Kategori, dan tugas Leaf Node, informasi berikut akan diimpor. Perhatikan bahwa hasil ini sama dengan yang ada pada proyek.

| Tugas | Kategori | Tanggal | Quantity | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tiket pesawat | 1/10/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 1/11/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]

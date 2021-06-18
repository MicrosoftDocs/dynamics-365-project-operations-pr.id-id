---
title: Mengimpor estimasi ke baris kontrak berbasis proyek
description: Topik ini menyediakan informasi tentang cara mengimpor estimasi dari proyek ke baris kontrak.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f8d9637e4a8bd09664c43ccc2b02514dc825997e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010250"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Mengimpor estimasi ke baris kontrak berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Di Dynamics 365 Project Operations, Anda dapat mengimpor estimasi dari proyek pada baris kontrak berbasis proyek.

1. Verifikasi bahwa bidang **proyek** pada baris kontrak berbasis proyek diisi.
2. Pada tab **rincian baris kontrak**, pada subkisi, pilih **impor dari estimasi proyek**. Halaman dialog dengan pilihan ringkasan terbuka. Pilihan ringkasan yang tersedia adalah, **kelas transaksi**, **kategori**, **peran**, dan **tugas proyek**. Berdasarkan pilihan untuk peringkasan, estimasi dari proyek untuk semua kelas transaksi yang tercakup dalam baris kontrak ini disalin. 
3. Untuk memeriksa jenis kelas transaksi yang disertakan, di tab **Umum** baris kontrak, dan periksa nilai di bidang **mencakup waktu**, **mencakup pengeluaran**, dan **mencakup biaya**.

Bila Anda mengimpor estimasi, aplikasi akan default ke harga berdasarkan daftar harga proyek yang dilampirkan ke kontrak dan jenis penagihan yang diatur pada baris kontrak. Jika peran atau kategori diatur pada baris kontrak sebagai tidak dikenakan biaya, baris estimasi impor untuk peran atau kategori itu tidak dikenai biaya dan tidak akan sama dengan nilai kontrak dari baris kontrak.

Bila baris kontrak memiliki detail baris, **nilai kontrak** dan bidang **estimasi pajak** pada baris kontrak diringkas dan tidak dapat diedit.

Bila pilihan beberapa ringkasan dipilih, sistem akan mencoba meringkas semua pilihan yang dipilih. Output ringkasan menghasilkan baris kontrak impor lebih banyak daripada jika Anda memilih hanya satu pilihan ringkasan.

Misalnya, jika proyek memiliki baris estimasi berikut untuk pengeluaran:

| Tugas | Kategori | Tanggal | Jumlah | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tiket pesawat | 1/10/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 1/11/2020 | 2 | 200 | 400 |

Bila pengguna memilih untuk meringkas berdasarkan **kelas transaksi**, informasi berikut akan diimpor:

| Tugas | Kategori | Tanggal | Jumlah | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 1/10/2020 | 3.34 | 840 | 2800 |

Bila pengguna memilih untuk meringkas berdasarkan **kelas transaksi** dan **Kategori**, informasi berikut akan diimpor:

| Tugas | Kategori | Tanggal | Jumlah | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tiket pesawat | 1/10/2020 | 4 | 400 | 1600 |
| &nbsp;  | Hotel | 1/10/2020 | 6 | 200 | 1200 |

Bila pengguna memilih untuk meringkas berdasarkan **kelas transaksi**, **Kategori**, dan **tugas Leaf Node**, yang berikut akan diimpor. Perhatikan bahwa hasil ini sama dengan yang ada pada proyek:

| Tugas | Kategori | Tanggal | Jumlah | Harga unit | Jumlah |
| --- | --- | --- | --- | --- | --- |
| Tugas A | Tiket pesawat | 1/10/2020 | 4 | 400 | 1600 |
| Tugas B | Hotel | 1/10/2020 | 4 | 200 | 800 |
| Tugas C | Hotel | 1/11/2020 | 2 | 200 | 400 |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
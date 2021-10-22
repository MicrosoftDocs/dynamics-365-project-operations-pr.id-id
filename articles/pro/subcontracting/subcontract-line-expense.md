---
title: Baris subkontrak untuk kategori pengeluaran
description: Topik ini menjelaskan cara merekam baris subkontrak untuk pengeluaran dan menggunakan bidang untuk merekam pembelian waktu dari vendor.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0c32bf2ac54de98a921d338e436ecd089e68a759
ms.sourcegitcommit: cd4e81f129681a12f2efe63ec2bb14e611cf88ba
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/20/2021
ms.locfileid: "7506103"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Baris subkontrak untuk kategori pengeluaran

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Subkontrak dalam Dynamics 365 Project Operations dapat memiliki baris untuk kategori pengeluaran. Baris subkontrak untuk kategori pengeluaran memungkinkan Manajer Proyek membeli kategori layanan atau produk dari vendor yang dapat mereka tagih pada proyek.

Untuk membuat baris subkontrak untuk kategori pengeluaran di Project Operations, selesaikan langkah-langkah berikut.

1. Di panel navigasi, pilih **Subkontrak**, dan buka Subkontrak yang ingin Anda kerjakan.
2. Pada tab **Baris Subkontrak**, pilih **Baru** untuk membuat baris baru.
3. Pada halaman **Buat Cepat**, pada bidang **Kelas Transaksi**, pilih **Pengeluaran** dan masukkan atau pilih informasi bidang lainnya yang diperlukan.

Tabel berikut menyediakan informasi tentang bidang pada halaman rincian **baris Subkontrak** dan halaman **Buat Cepat**.

| **Bidang** | **Deskripsi** | **Dampak Fungsional** |
| --- | --- | --- |
| Nama | Nama baris subkontrak untuk membantu identifikasi. | Ini akan ditampilkan sebagai kolom pertama di semua pencarian berdasarkan baris subkontrak. |
| KETERANGAN | Deskripsi singkat tentang kategori pengeluaran yang dibeli pada baris subkontrak. | Tidak Ada |
|Jenis Baris | Bidang ini memiliki nilai default  **berbasis Kuantitas**. |Tidak Ada |
| Metode Penagihan | Ini adalah rangkaian pilihan yang menunjukkan dua model kontrak utama yang didukung oleh Project Operations: **Harga Tetap** dan **waktu dan bahan**. | Jadwal faktur berbasis tahapan disediakan untuk baris subkontrak jika metode penagihan Harga Tetap dipilih. |
| Kelas Transaksi | Bidang ini memiliki nilai default  **waktu**. Untuk membuat baris subkontrak untuk pembelian produk, atur bidang  **Kelas Transaksi**  ke  **Pengeluaran**.  | Ini menunjukkan bahwa baris subkontrak sedang digunakan untuk merekam pembelian kategori pengeluaran yang akan digunakan pada proyek. |
| Kategori Transaksi | Menampilkan daftar kategori transaksi aktif dalam sistem. |Tidak Ada |
| Awalan yang Diminta | Masukkan tanggal saat kategori pembelian harus tersedia dari vendor. | Start yang diminta digunakan untuk memilih daftar harga proyek dari daftar harga proyek yang dilampirkan ke subkontrak. Biaya kategori pada baris subkontrak berasal dari daftar harga itu. |
| Akhir yang Diminta | Masukkan tanggal saat kategori pembelian tidak akan lagi diperlukan. | Ini akan digunakan untuk menampilkan peringatan saat manajer proyek mengaitkan baris subkontrak ini ke estimasi pengeluaran tertentu pada proyek yang diperlukan setelah tanggal ini. |
| Kuantitas yang Dipesan | Kuantitas kategori yang dibeli dari vendor. | Ini akan digunakan untuk menunjukkan peringatan ketika manajer proyek terlalu banyak menarik dari kuantitas ini.|
| Grup Unit | Nilai default didasarkan pada grup unit default yang disiapkan untuk kategori yang dipilih. |Tidak Ada |
| Unit | Default didasarkan pada unit default yang disiapkan untuk kategori yang dipilih.  | Kombinasi **Kategori** dan **Unit** akan digunakan sebagai default atau dihitung untuk harga unit untuk baris subkontrak.  |
| Harga Unit | Nilai default menggunakan kombinasi **Kategori** dan **Unit** dari harga kategori yang terkait dengan daftar harga proyek, yang berlaku untuk awal baris subkontrak yang diminta. |Tidak Ada |
| Subtotal | Bidang ini bersifat hanya baca yang dihitung sebagai Kuantitas x harga Unit, jika nilai kuantitas dan harga unit dimasukkan. Jika salah satu atau kedua bidang kosong, Anda dapat memasukkan nilai di bidang ini. |Tidak Ada |
| Pajak Penjualan | Masukkan jumlah pajak penjualan. |Tidak Ada |
| Jumlah Total | Jumlah total baris Subkontrak termasuk pajak. Bidang ini dihitung sebagai subtotal + pajak penjualan. |Tidak Ada |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

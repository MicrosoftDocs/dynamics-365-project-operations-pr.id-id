---
title: Estimasi keuangan untuk pengeluaran pada proyek
description: Topik ini memberikan informasi tentang mendefinisikan atau memperkirakan biaya berdasarkan proyek.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 18d8568fae35fc251d9cf48d900b8a436e2e4500
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014165"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Estimasi keuangan untuk pengeluaran pada proyek
_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations memungkinkan manajer proyek menentukan pengeluaran berbasis proyek untuk setiap proyek atau tugas. Setiap item pengeluaran dapat dikaitkan dengan tugas proyek tertentu. Pengeluaran dikategorikan ke dalam berbagai kategori pengeluaran, yang ditentukan pada tingkat organisasional. Harga dan biaya untuk setiap kategori pengeluaran ditentukan dalam daftar harga. 

Selesaikan langkah berikut untuk melihat, menambah, atau menghapus biaya proyek.

1. Buka **proyek**, dan pilih proyek yang ingin Anda kerjakan.
2. Pilih tab **estimasi proyek** dan lihat daftar pengeluaran proyek.
3. Pilih **pengeluaran baru** untuk menambahkan pengeluaran. Atau, pilih pengeluaran untuk dihapus, lalu pilih **Hapus pengeluaran**.

Tabel berikut memberikan informasi tentang bidang pada **baris estimasi Pengeluaran** di Proyek. 

| **Bidang** | **Deskripsi** | **Dampak hilir** |
| --- | --- | --- |
| Tugas | Semua tugas dalam proyek. Ini mencakup tugas node leaf dan ringkasan. | Memilih tugas untuk baris estimasi pengeluaran akan mempengaruhi estimasi biaya pengeluaran dan estimasi penjualan pengeluaran untuk tugas. Jika bidang ini dibiarkan kosong, perkiraan pengeluaran dilacak dan diringkas hanya pada tingkat proyek. |
| Kategori | Daftar kategori transaksi yang memiliki kategori pengeluaran tertaut pada aplikasi. | Memilih kategori akan mendorong harga dan biaya pada baris estimasi pengeluaran. |
| Tanggal mulai | Tanggal perkiraan pengeluaran akan terjadi. | Tidak ada dampak hilir untuk bidang ini. |
| Grup Unit | Nilai default pada bidang ini berasal dari grup unit yang disiapkan sebagai default pada kategori yang dipilih. Anda dapat memperbarui bidang ini untuk memilih grup unit lain. | Tidak ada dampak hilir untuk bidang ini. |
| Unit | Nilai di bidang ini akan default ke unit default dari kategori yang dipilih. Anda dapat memperbarui bidang ini untuk memilih unit lain. | Mengubah unit menghasilkan biaya dan harga per unit default yang berbeda. |
| Quantity | Kuantitas estimasi pengeluaran yang akan Anda kenakan. | Tidak ada dampak hilir untuk bidang ini. |
| Biaya Unit | Biaya kategori dan kombinasi unit yang dipilih sebagaimana diatur dalam daftar harga biaya yang berlaku | Biaya unit selalu ditampilkan dalam mata uang biaya proyek. |
| Harga Unit | Harga kategori dan kombinasi unit yang dipilih sebagaimana diatur dalam daftar harga penjualan yang berlaku. | Harga per unit selalu ditampilkan dalam mata uang penjualan proyek. |
| Biaya Total | Jumlah biaya yang dihitung sebagai kuantitas \* biaya per unit.| Jumlah Biaya selalu ditampilkan dalam mata uang biaya proyek. |
| Penjualan Total | Jumlah penjualan yang dihitung sebagai kuantitas \* harga per unit. | Jumlah penjualan selalu ditampilkan dalam mata uang penjualan proyek. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]

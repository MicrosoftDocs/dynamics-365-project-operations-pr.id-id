---
title: Mengelola unit kompleks seperti per-pengguna, per bulan untuk baris kuotasi berbasis produk
description: Topik ini memberikan informasi tentang mengeluarkan unit kompleks untuk baris kuotasi berbasis produk.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078416"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a>Mengelola unit kompleks seperti per-pengguna, per bulan untuk baris kuotasi berbasis produk

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Dynamics 365 Project Operations menggunakan faktor kuantitas untuk mendukung penjualan produk berbasis langganan. Untuk produk berbasis langganan, kuantitas pada kuotasi atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.

Biasanya, harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan. Selama proses penjualan, harga pada baris kuotasi biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan TI. Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda. Kuantitas yang digunakan untuk menghitung baris kuotasi adalah produk dari jumlah pengguna dan jumlah bulan langganan.

Untuk mendukung jenis penjualan, Project Operations memperkenalkan konsep faktor kuantitas. Faktor kuantitas mengandalkan atribut produk di Dynamics 365. Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, Project Operations memungkinkan Anda menandai subset, atau semua properti, sebagai faktor kuantitas.

Project Operations memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas. Bila Anda menambahkan produk dengan faktor kuantitas ke baris kuotasi, bidang **kuantitas** menjadi hanya baca. Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, Project Operations menghitung kuantitas baris kuotasi.

Misalnya, Dynamics 365 Sales mungkin memiliki properti berikut:

- **Jumlah pengguna** : jumlah pengguna
- **Jumlah bulan** : jumlah bulan langganan
- **SKU Produk**

Anda dapat menandai **Jumlah pengguna** dan **Jumlah bulan** sebagai faktor kuantitas dengan mengedit properti lini produk.

Untuk membuat faktor kuantitas dari properti produk, ikuti langkah-langkah berikut:

1. Di panel navigasi kiri Project Operations, buka **penjualan** > **produk**.
2. Buka produk yang Anda perlukan untuk mengkonfigurasikan faktor kuantitas. Pastikan produk memiliki properti yang telah dikonfigurasi.
3. Pada halaman **informasi proyek** untuk produk, pilih tab **faktor kuantitas**.
4. Di subkisi, pilih **+ perhitungan Bidang baru**.
5. Masukkan nama faktor kuantitas, lalu pilih nilai properti yang dipetakan ke penghitungan bidang.
6. Simpan dan tutup formulir. Ulangi langkah ini untuk semua properti yang akan digunakan untuk menghitung kuantitas untuk baris kuotasi berdasarkan produk.

Bila Anda membuat baris kuotasi berbasis produk untuk produk, kuantitas baris kuotasi akan dikunci. Kuantitas akan dihitung sebagai produk dari nilai properti yang Anda masukkan untuk baris kuotasi.

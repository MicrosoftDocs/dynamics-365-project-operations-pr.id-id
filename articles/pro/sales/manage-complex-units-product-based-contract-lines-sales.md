---
title: Mengelola unit yang kompleks untuk baris kontrak berbasis produk - lite
description: Topik ini menyediakan informasi tentang cara mendukung penjualan produk berbasis langganan.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177380"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Mengelola unit yang kompleks untuk baris kontrak berbasis produk - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Dynamics 365 Project Operations menggunakan faktor kuantitas untuk mendukung penjualan produk berbasis langganan. Untuk produk berbasis langganan, kuantitas pada kontrak atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.

Harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan. Selama proses penjualan, harga pada baris kontrak biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan. Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda. Kuantitas yang digunakan untuk menghitung jumlah baris kontrak adalah produk dari jumlah pengguna dan jumlah bulan langganan.

Untuk mendukung jenis penjualan, Project Operations mendukung konsep *faktor kuantitas*. Faktor kuantitas mengandalkan atribut produk. Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, Anda dapat menandai subset properti tersebut, atau semua properti, sebagai faktor kuantitas.

Project Operations memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas. Bila produk dengan faktor kuantitas yang dikonfigurasi ditambahkan ke baris kontrak, bidang **kuantitas** menjadi hanya baca. Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, Project Operations menghitung kuantitas baris kontrak.

Misalnya, Dynamics 365 Sales mungkin memiliki properti berikut:

- **Jumlah pengguna**: jumlah pengguna.
- **Jumlah bulan**: jumlah bulan langganan.
- **SKU produk**: unit penyimpanan stok (SKU) untuk produk.

Properti **Jumlah pengguna** dan **Jumlah bulan** dapat ditandai sebagai faktor kuantitas dengan mengedit properti lini produk.

Untuk membuat faktor kuantitas dari properti produk, selesaikan langkah berikut.

1. Pada **Project Operations**, pilih **produk penjualan**.
2. Buka produk yang harus Anda konfigurasikan faktor kuantitasnya. Pastikan bahwa produk memiliki properti yang telah diatur.
3. Pada halaman **informasi proyek**, pilih tab **faktor kuantitas**.
4. Di subkisi, pilih **+ perhitungan Bidang baru**.
5. Masukkan nama **faktor kuantitas**, lalu pilih nilai properti yang dipetakan ke penghitungan bidang.
6. Simpan dan tutup formulir.
7. Ulangi langkah 2-6 untuk semua properti yang bersama-sama akan membuat kuantitas untuk baris kontrak berbasis produk.

Dengan mengatur faktor kuantitas, saat pengguna membuat baris kontrak untuk produk ini, kuantitas baris kontrak terkunci. Kuantitas kemudian dihitung sebagai produk dari nilai properti untuk baris kontrak tersebut.

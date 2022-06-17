---
title: Mengelola unit kompleks seperti per-pengguna, per bulan untuk baris kuotasi berbasis produk - lite
description: Artikel ini menyediakan informasi tentang mengelola unit kompleks untuk garis kutipan berbasis produk.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929908"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Mengelola unit kompleks seperti per-pengguna, per bulan untuk baris kuotasi berbasis produk - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Dynamics 365 Project Operations menggunakan faktor kuantitas untuk mendukung penjualan produk berbasis langganan. Untuk produk berbasis langganan, kuantitas pada kuotasi atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.

Biasanya, harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan. Selama proses penjualan, harga pada baris kuotasi biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan TI. Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda. Kuantitas yang digunakan untuk menghitung baris kuotasi adalah produk dari jumlah pengguna dan jumlah bulan langganan.

Untuk mendukung jenis penjualan, Project Operations memperkenalkan konsep faktor kuantitas. Faktor kuantitas mengandalkan atribut produk di Dynamics 365. Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, Project Operations memungkinkan Anda menandai subset, atau semua properti, sebagai faktor kuantitas.

Project Operations memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas. Bila Anda menambahkan produk dengan faktor kuantitas ke baris kuotasi, bidang **kuantitas** menjadi hanya baca. Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, Project Operations menghitung kuantitas baris kuotasi.

Misalnya, Dynamics 365 Sales mungkin memiliki properti berikut:

- **Jumlah pengguna**: jumlah pengguna
- **Jumlah bulan**: jumlah bulan langganan
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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
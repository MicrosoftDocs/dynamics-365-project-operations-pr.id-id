---
title: Rincian header untuk faktur vendor
description: Artikel ini menjelaskan fungsi yang diberikan pada header faktur vendor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261660"
---
# <a name="header-details-for-vendor-invoices"></a>Rincian header untuk faktur vendor

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini menjelaskan fungsi yang diberikan pada header faktur vendor di Microsoft Dynamics 365 Project Operations.

Saat Manajer Proyek merencanakan dan mengeksekusi proyek, mereka mungkin mempekerjakan subkontraktor dan membeli produk maupun layanan dari vendor. Selama eksekusi proyek, biaya dikeluarkan dari layanan, materi, dan kategori pengeluaran yang diperoleh pada subkontrak dengan vendor. Vendor memfaktur biaya ini ke proyek dengan membuat faktur vendor.

Tabel berikut menyediakan informasi tentang bidang pada header faktur vendor di Project Operations.

| Bidang | Description | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama Faktur Vendor. | Di semua daftar drop-down faktur, nama faktur vendor tercantum di kolom pertama untuk membantu Anda mengidentifikasi faktur vendor. Secara default, bila faktur vendor dibuat dari subkontrak, bidang **Nama** faktur vendor diatur ke nilai yang terdiri dari nama subkontrak ditambah tanggal saat ini. |
| Description | Deskripsi singkat tentang layanan dan produk yang ditagih di faktur vendor. | Tidak ada |
| Vendor | Nama perusahaan yang memfaktur produk dan layanan. Perusahaan ini harus merupakan Rekaman Akun yang memiliki jenis relasi **Vendor** atau **Pemasok**. | <p>Berdasarkan vendor yang dipilih, nilai default akan secara otomatis dimasukkan di bidang berikut:</p><ul><li>Mata uang</li><li>Daftar Harga</li><li>Syarat Pembayaran</li><li>Alamat Pembayaran</li></ul> |
| Subkontrak | Referensi ke subkontrak untuk faktur vendor. | <p>Berdasarkan subkontrak yang dipilih, nilai default akan secara otomatis dimasukkan di bidang berikut:</p><ul><li>Mata uang</li><li>Daftar Harga</li><li>Syarat Pembayaran</li><li>Alamat Pembayaran</li></ul><p>Subkontrak yang dipilih pada header faktur vendor dimasukkan secara default di baris faktur vendor dan tidak dapat diubah di sana.</p> |
| Tanggal faktur | Tanggal untuk aktual biaya yang akan dibuat saat faktur vendor dikonfirmasi. | Tanggal faktur juga digunakan untuk memilih daftar harga pembelian yang benar, baik dari daftar harga yang dilampirkan ke vendor terkait maupun dari parameter proyek. |
| Alasan status | Status Faktur Vendor. | <p>Status menentukan lokasi faktur vendor dalam proses bisnis dan apakah dapat diedit. Di sini adalah beberapa format yang tersedia:</p><ul><li>**Draf** – Faktur vendor dapat diedit.</li><li>**Terkonfirmasi** – Faktur vendor diverifikasi dan terkonfirmasi. Faktur Vendor dalam status ini tidak dapat diedit atau dihapus.</li><li>**Dalam proses** – Faktur vendor sedang ditinjau. Faktur Vendor dalam status tidak diedit tetapi tidak dapat dihapus.</li><li>**Dibatalkan** – Faktur vendor dibatalkan. Faktur Vendor dalam status ini tidak dapat diedit atau dihapus.</li></ul> |
| Mata uang | Mata uang yang ditagihkan vendor untuk produk dan layanan pada faktur vendor. | Pada faktur vendor yang mereferensikan subkontrak, mata uang subkontrak dimasukkan secara default sebagai mata uang faktur vendor. Pada faktur vendor yang tidak mereferensikan subkontrak, nilai default dimasukkan dari rekaman akun vendor dan dapat diubah. Setelah faktur vendor disimpan, mata uang tidak dapat lagi diedit. |
| Unit Kontrak | Divisi perusahaan yang bertanggung jawab menerima layanan dan/atau produk dari vendor. | Tidak ada |
| Syarat Pembayaran | Persyaratan pembayaran pada faktur vendor yang dikeluarkan. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Persyaratan pembayaran dari subkontrak disalin ke semua faktur vendor yang terkait dengan subkontrak ini. Persyaratan pembayaran dapat diperbarui jika faktur vendor memiliki status **Draf**. |
| Alamat Pembayaran | Alamat vendor untuk pengiriman pembayaran. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Alamat pembayaran dari subkontrak disalin sebagai alamat pembayaran untuk semua faktur vendor yang dibuat untuk subkontrak itu. Alamat pembayaran dapat diperbarui jika faktur vendor memiliki status **Draf**. |
| Subtotal | Jika faktur vendor tidak memiliki baris, masukkan subtotal faktur sebelum pajak. Jika faktur vendor memiliki baris, bidang ini hanya dapat dibaca. Jika demikian, Jumlah yang ditampilkan adalah jumlah subtotal dari semua baris pada faktur vendor. | Tidak ada |
| Total Pajak | Jika faktur vendor tidak memiliki baris, masukkan total pajak di subkontrak. Jika faktur vendor memiliki baris, bidang ini hanya dapat dibaca. Jika demikian, Jumlah yang ditampilkan adalah jumlah nilai pajak dari semua baris pada faktur vendor. | Tidak ada |
| Jumlah Total | Data bidang terhitung ini menunjukkan jumlah total faktur vendor setelah pajak disertakan. | Tidak ada |

> [!NOTE]
> Bidang berikut di faktur vendor tidak dapat diubah setelah faktur vendor disimpan: **Vendor**, **Subkontrak**, **Mata Uang**, **Unit Kontrak**, dan **Persyaratan pembayaran**. Jika perubahan apa pun diperlukan pada bidang ini pada faktur vendor, Anda harus menghapus faktur vendor dan membuat faktur vendor baru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

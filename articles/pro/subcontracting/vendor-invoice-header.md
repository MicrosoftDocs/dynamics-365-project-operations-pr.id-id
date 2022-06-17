---
title: Rincian header untuk faktur vendor
description: Artikel ini menjelaskan fungsionalitas yang disediakan pada header faktur vendor di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929862"
---
# <a name="header-details-for-vendor-invoices"></a>Rincian header untuk faktur vendor

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini menjelaskan fungsionalitas yang disediakan pada header faktur vendor di Microsoft Dynamics 365 Project Operations.

Saat manajer proyek merencanakan dan melaksanakan proyek, mereka mungkin mempekerjakan subkontraktor dan membeli produk dan layanan dari vendor. Selama pelaksanaan proyek, biaya dikeluarkan dari kategori layanan, bahan, dan biaya yang diperoleh pada subkontrak dengan vendor. Vendor menagih biaya ini ke proyek dengan membuat faktur vendor.

Tabel berikut ini menyediakan informasi tentang bidang pada header faktur vendor di Operasi Proyek.

| Bidang | Deskripsi | Dampak Fungsional |
| --- | --- | --- |
| Nama | Nama faktur vendor. | Di semua daftar drop-down faktur vendor, nama faktur vendor tercantum di kolom pertama untuk membantu Anda mengidentifikasi faktur vendor. Secara default, ketika faktur vendor dibuat dari subkontrak, **bidang Nama** faktur vendor diatur ke nilai yang terdiri dari nama subkontrak ditambah tanggal saat ini. |
| Deskripsi | Deskripsi singkat tentang layanan dan produk yang sedang ditagih pada faktur vendor. | Tidak ada |
| Vendor | Nama perusahaan yang menagih produk dan layanan. Perusahaan ini harus menjadi catatan akun yang memiliki jenis **hubungan Vendor** atau **Pemasok**. | <p>Berdasarkan vendor yang dipilih, nilai default secara otomatis dimasukkan di bidang berikut:</p><ul><li>Mata uang</li><li>Daftar Harga</li><li>Syarat Pembayaran</li><li>Alamat pembayaran</li></ul> |
| Subkontrak | Referensi ke subkontrak untuk faktur vendor. | <p>Berdasarkan subkontrak yang dipilih, nilai default secara otomatis dimasukkan dalam bidang berikut:</p><ul><li>Mata uang</li><li>Daftar Harga</li><li>Syarat Pembayaran</li><li>Alamat pembayaran</li></ul><p>Subkontrak yang dipilih pada header faktur vendor dimasukkan secara default pada baris faktur vendor dan tidak dapat diubah di sana.</p> |
| Tanggal faktur | Tanggal aktual biaya yang akan dibuat saat faktur vendor dikonfirmasi. | Tanggal faktur juga digunakan untuk memilih daftar harga pembelian yang benar baik dari daftar harga yang dilampirkan ke vendor terkait atau dari parameter proyek. |
| Alasan status | Status faktur vendor. | <p>Status menentukan di mana faktur vendor berada dalam proses bisnis dan apakah faktur tersebut dapat diedit. Berikut adalah beberapa nilai yang tersedia:</p><ul><li>**Draf** – Faktur vendor dapat diedit.</li><li>**Dikonfirmasi** – Faktur vendor telah diverifikasi dan dikonfirmasi. Faktur vendor dalam status ini tidak dapat diedit atau dihapus.</li><li>**Dalam prosesnya** – Faktur vendor sedang ditinjau. Faktur vendor dalam status ini dapat diedit, tetapi tidak dapat dihapus.</li><li>**Dibatalkan** – Faktur vendor dibatalkan. Faktur vendor dalam status ini tidak dapat diedit atau dihapus.</li></ul> |
| Mata uang | Mata uang yang digunakan vendor untuk produk dan layanan pada faktur vendor. | Pada faktur vendor yang mereferensikan subkontrak, mata uang subkontrak dimasukkan secara default sebagai mata uang faktur vendor. Pada faktur vendor yang tidak mereferensikan subkontrak, nilai default dimasukkan dari catatan akun vendor dan dapat diubah. Setelah faktur vendor disimpan, mata uang tidak dapat lagi diedit. |
| Unit Kontrak | Divisi perusahaan yang bertanggung jawab untuk menerima layanan dan/atau produk dari vendor. | Tidak ada |
| Syarat Pembayaran | Ketentuan pembayaran pada faktur vendor yang diterbitkan. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Ketentuan pembayaran dari subkontrak disalin ke semua faktur vendor yang terkait dengan subkontrak. Ketentuan pembayaran dapat diperbarui jika faktur vendor memiliki status **Draf**. |
| Alamat pembayaran | Alamat vendor untuk pengiriman pembayaran. Nilai default akan secara otomatis dimasukkan dari rekaman akun vendor. | Alamat pembayaran dari subkontrak disalin sebagai alamat pembayaran ke semua faktur vendor yang dibuat untuk subkontrak tersebut. Alamat pembayaran dapat diperbarui jika faktur vendor memiliki status **Draf**. |
| Subtotal | Jika faktur vendor tidak memiliki baris, masukkan subtotal faktur sebelum pajak. Jika faktur vendor memiliki baris, bidang ini hanya dapat dibaca. Dalam hal ini, jumlah yang ditampilkan adalah jumlah subtotal dari semua baris pada faktur vendor. | Tidak ada |
| Total pajak | Jika faktur vendor tidak memiliki baris, masukkan total pajak pada subkontrak. Jika faktur vendor memiliki baris, bidang ini hanya dapat dibaca. Dalam hal ini, jumlah yang ditampilkan adalah jumlah jumlah pajak dari semua baris pada faktur vendor. | Tidak ada |
| Jumlah total | Ini bidang terhitung menunjukkan jumlah total faktur vendor setelah pajak disertakan. | Tidak ada |

> [!NOTE]
> Bidang berikut pada faktur vendor tidak dapat diubah setelah faktur vendor disimpan: **Vendor, Subkontrak**, **Mata Uang**, **Unit** **kontrak, dan** Ketentuan **pembayaran**. Jika ada perubahan yang diperlukan pada bidang ini pada faktur vendor, Anda harus menghapus faktur vendor dan membuat faktur vendor baru.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Header peluang
description: Topik ini menyediakan informasi tentang keseluruhan informasi tentang penawaran berbasis proyek dan baris peluang berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f08de54767f49c308d0ccc7f2e1c6ef880b7f99
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906207"
---
# <a name="opportunity-header"></a>Header peluang

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Header peluang akan menangkap keseluruhan informasi tentang kesepakatan berbasis proyek yang berlaku untuk semua baris pada peluang berbasis proyek.

Peluang proyek berbasis di Dynamics 365 Project Operations adalah ekstensi peluang di Dynamics 365 Sales. Ekstensi ini menyediakan fungsi tambahan yang spesifik dan diperlukan untuk peluang berbasis proyek. Ekstensi ini dapat mencakup bidang baru dan tindakan pita yang tersedia di peluang berbasis proyek. Anda mungkin menemukan beberapa bidang, fungsi, dan logika default yang tersedia dalam Sales tidak tersedia dalam Project Operations.

Tabel berikut mencakup bidang dalam peluang berbasis proyek yang unik untuk Project Operations atau memiliki beberapa perubahan penting dalam perilaku dari peluang dalam Sales.

| **Bidang** | **Lokasi** | **Relevansi, tujuan, dan panduan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Tipe | Tab Umum (tersembunyi) | Bidang rangkaian pilihan ini memiliki pilihan berikut:</br>- berbasis Pekerjaan (tersedia hanya dengan Project Operations)</br>- berbasis item (tersedia hanya bila Project Operations dan Sales diinstal)</br>- Berbasis pemeliharaan layanan (tersedia saat Field Service diinstal) | Bila Anda menggunakan Project Operations, nilai bidang ini secara otomatis diatur ke **berbasis pekerjaan** yang mengelompokkan peluang sebagai berbasis proyek. Sebuah Peluang harus berbasis proyek untuk mengaktifkan semua ekstensi dan fungsi khusus proyek di proses penjualan hilir untuk transaksi ini. |
| Kontak | Tab Umum | Merujuk pada kontak utama pelanggan untuk transaksi ini. | |
| Akun | Tab Umum | Merujuk pada perusahaan atau rekaman akun pelanggan. | |
| Manajer Akun | Tab Umum | Nama manajer akun untuk peluang berbasis proyek ini. | Manajer akun bertanggung jawab untuk mengelola hubungan dengan pelanggan melalui penyelesaian proyek ini. Berdasarkan rekaman sumber daya yang dapat dipesan terkait dengan manajer akun, unit kontrak menjadi default. |
| Unit Kontrak | Tab Umum | Unit organisasi yang bertanggung jawab atas pelaksanaan proyek atau proyek-proyek yang terkait dengan transaksi ini. | Unit kontrak adalah divisi perusahaan yang akan menyelesaikan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang, dan mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang timbul selama proyek. |

Untuk semua bidang dan bagian lain di tab **ringkasan** peluang, lihat [membuat atau mengedit peluang (Pusat penjualan dan Sales)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)

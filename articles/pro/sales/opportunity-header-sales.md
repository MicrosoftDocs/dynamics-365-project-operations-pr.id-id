---
title: Pengaturan peluang - lite
description: Topik ini menyediakan informasi tentang penawaran berbasis proyek dan baris peluang berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6631e136572b958ca616d708a5e3c3c2d9f2675c
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663823"
---
# <a name="header-details-for-project-opportunities"></a>Rincian header untuk peluang proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Header peluang akan menangkap keseluruhan informasi tentang kesepakatan berbasis proyek yang berlaku untuk semua baris pada peluang berbasis proyek.

Peluang berbasis proyek di Dynamics 365 Project Operations adalah ekstensi peluang di Dynamics 365 Sales. Ekstensi ini menyediakan fungsi tambahan yang spesifik dan diperlukan untuk peluang berbasis proyek. Ekstensi ini dapat mencakup bidang baru dan tindakan pita yang tersedia di peluang berbasis proyek. Anda mungkin menemukan beberapa bidang, fungsi, dan logika default yang tersedia dalam Sales tidak tersedia dalam Project Operations.

Tabel berikut mencakup bidang dalam peluang berbasis proyek yang unik untuk Project Operations atau memiliki beberapa perubahan penting dalam perilaku dari peluang dalam Sales.

| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Tipe | Tab Umum (tersembunyi) | Bidang rangkaian pilihan ini memiliki pilihan berikut:</br>- berbasis Pekerjaan (tersedia hanya dengan Project Operations)</br>- berbasis item (tersedia hanya bila Project Operations dan Sales diinstal)</br>- Berbasis pemeliharaan layanan (tersedia saat Field Service diinstal) | Bila Anda menggunakan Project Operations, nilai bidang ini secara otomatis diatur ke **berbasis pekerjaan** yang mengelompokkan peluang sebagai berbasis proyek. Sebuah Peluang harus berbasis proyek untuk mengaktifkan semua ekstensi dan fungsi khusus proyek di proses penjualan hilir untuk transaksi ini. |
| Kontak | Tab Umum | Merujuk pada kontak utama pelanggan untuk transaksi ini. | |
| Akun | Tab Umum | Merujuk pada perusahaan atau rekaman akun pelanggan. | |
| Manajer Akun | Tab Umum | Nama manajer akun untuk peluang berbasis proyek ini. | Manajer akun bertanggung jawab untuk mengelola hubungan dengan pelanggan melalui penyelesaian proyek ini. Berdasarkan rekaman sumber daya yang dapat dipesan terkait dengan manajer akun, unit kontrak menjadi default. |
| Unit Kontrak | Tab Umum | Unit organisasi yang bertanggung jawab atas pelaksanaan proyek atau proyek-proyek yang terkait dengan transaksi ini. | Unit kontrak adalah divisi perusahaan yang akan menyelesaikan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang, dan mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang timbul selama proyek. |

Untuk semua bidang dan bagian lain di tab **ringkasan** peluang, lihat [membuat atau mengedit peluang (Pusat penjualan dan Sales)](https://docs.microsoft.com/dynamics365/sales-enterprise/create-edit-opportunity-sales)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

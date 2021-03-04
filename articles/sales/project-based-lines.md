---
title: Baris peluang berbasis proyek
description: Topik ini menyediakan informasi tentang menangani baris peluang berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ede474e3d8830b420dc5b183f14327206c10288
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181951"
---
# <a name="project-based-opportunity-lines"></a>Baris peluang berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Baris peluang berbasis proyek hanya tersedia dalam peluang berbasis proyek. Rekaman Peluang berbasis proyek memiliki nilai bidang **Jenis** yang diatur ke **berbasis pekerjaan**.

Baris peluang berbasis proyek adalah item baris yang akan dikirim kepada pelanggan yang menggunakan proyek. Namun, proyek tidak dapat dihubungkan ke baris peluang berbasis proyek. Proyek dapat dikaitkan ke item baris dari tahap **kuotasi** dan seterusnya karena biasanya peluang terjadi pada tahap awal perjanjian. Penentuan berapa banyak proyek yang akan digunakan untuk memberikan pekerjaan untuk pelanggan adalah keputusan yang dibuat nanti dalam fase penjualan. Gunakan fase peluang untuk mengidentifikasi komponen pengiriman diskrit untuk pelanggan. Keputusan seputar jumlah aktual proyek yang digunakan untuk memberikan komponen ini dapat didorong keluar hingga informasi lebih lanjut diketahui tentang pekerjaan itu sendiri.

Di bawah ini adalah bidang pada baris peluang berbasis proyek:

| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Jenis Produk | Tab Umum (tersembunyi) | Ini adalah bidang rangkaian pilihan. Jika Anda memiliki Dynamics 365 Operations terinstal, salah satu pilihan yang tersedia adalah, **layanan berbasis proyek**.  | Nilai bidang ini diatur ke **layanan berbasis proyek** saat Anda membuat baris peluang berbasis proyek dari kisi baris berbasis proyek pada peluang. <br> Jika Anda mengubah atau mengganti nilai ini, fungsi proyek tidak akan diaktifkan pada item baris berbasis proyek. |
| Peluang | Tab Umum | Bidang ini hanya baca dan merujuk rekaman peluang induk yang dimiliki item baris ini. | Tidak ada dampak hilir dari bidang ini. |
| Nama | Tab Umum | Ini adalah bidang teks yang dapat diedit yang dapat digunakan untuk memberikan identitas singkat ke item baris ini | Nilai ini dibawa ke baris kuotasi saat Anda membuat kuotasi dari peluang ini |
| Anggaran Pelanggan | Tab Umum | Bidang mata uang yang dapat diedit ini dapat digunakan untuk melacak jumlah yang bersedia dikeluarkan oleh pelanggan untuk item baris ini. | Nilai ini dibawa ke bidang terkait di baris kuotasi saat Anda membuat kuotasi dari peluang ini |
| Metode Penagihan | Tab Umum | Bidang yang dapat diedit ini memiliki kemungkinan nilai:</br>- Waktu dan bahan</br>- Harga tetap | Nilai ini dibawa ke bidang terkait di baris kuotasi saat Anda membuat kuotasi dari peluang ini. Setelah baris kuotasi dibuat, bidang akan dikunci dan tidak dapat diubah. Tetapkan nilai bidang ini seakurat mungkin. Jika Anda perlu mengubah nilai bidang ini pada baris kuotasi, Hapus dan buat ulang baris kuotasi. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
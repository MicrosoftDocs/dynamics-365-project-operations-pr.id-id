---
title: Baris peluang berbasis proyek - lite
description: Artikel ini menyediakan informasi tentang lini peluang berbasis proyek. (Pro)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8b5a8fc32ca903d7da2e090137bed358b364902a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914268"
---
# <a name="project-based-opportunity-lines---lite"></a>Baris peluang berbasis proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Baris peluang berbasis proyek hanya tersedia dalam peluang berbasis proyek. Rekaman Peluang berbasis proyek memiliki nilai bidang **Jenis** yang diatur ke **berbasis pekerjaan**.

Baris peluang berbasis proyek adalah item baris yang akan dikirim kepada pelanggan yang menggunakan proyek. Namun, proyek tidak dapat dihubungkan ke baris peluang berbasis proyek. Proyek dapat dikaitkan ke item baris dari tahap **kuotasi** dan seterusnya karena biasanya peluang terjadi pada tahap awal perjanjian dalam siklus hidup penawaran. Penentuan berapa banyak proyek yang akan digunakan untuk memberikan pekerjaan untuk pelanggan adalah keputusan yang dibuat nanti dalam fase penjualan. Anda dapat menggunakan fase peluang untuk mengidentifikasi komponen pengiriman diskrit untuk pelanggan. Keputusan seputar jumlah aktual proyek yang digunakan untuk memberikan komponen ini dapat didorong keluar hingga informasi lebih lanjut diketahui tentang pekerjaan itu sendiri.

Di bawah ini adalah bidang pada baris peluang berbasis proyek:

| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Jenis Produk | Tab Umum (tersembunyi) | Anda dapat memilih salah satu dari opsi berikut ini:</br>- Layanan berbasis proyek (hanya tersedia bila Dynamics 365 Project Operations diinstal)</br>- Produk (tersedia hanya bila Project Operations dan Dynamics 365 Sales diinstal) | Nilai bidang ini diatur ke **layanan berbasis proyek** saat Anda membuat baris peluang berbasis proyek dari kisi baris berbasis proyek pada peluang. <br> Jika Anda mengubah atau mengganti nilai ini, fungsi proyek tidak akan diaktifkan pada item baris berbasis proyek. |
| Peluang | Tab Umum | Bidang ini hanya baca dan merujuk rekaman peluang induk yang dimiliki item baris ini. | Tidak ada dampak hilir dari bidang ini. |
| Nama | Tab Umum | Ini adalah bidang teks yang dapat diedit yang dapat digunakan untuk memberikan identitas singkat ke item baris ini. | Nilai ini dibawa ke baris kuotasi saat Anda membuat kuotasi dari peluang ini. |
| Anggaran Pelanggan | Tab Umum | Bidang mata uang yang dapat diedit ini dapat digunakan untuk melacak jumlah yang bersedia dikeluarkan oleh pelanggan untuk item baris ini. | Nilai ini dibawa ke bidang terkait di baris kuotasi saat Anda membuat kuotasi dari peluang ini. |
| Metode Penagihan | Tab Umum | Bidang yang dapat diedit ini memiliki kemungkinan nilai:</br>- Waktu dan bahan</br>- Harga tetap | Nilai ini dibawa ke bidang terkait di baris kuotasi saat Anda membuat kuotasi dari peluang ini. Setelah baris kuotasi dibuat, bidang akan dikunci dan tidak dapat diubah. Tetapkan nilai bidang ini seakurat mungkin. Jika Anda perlu mengubah nilai bidang ini pada baris kuotasi, Hapus dan buat ulang baris kuotasi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
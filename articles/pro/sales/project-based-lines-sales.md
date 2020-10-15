---
title: Baris peluang berbasis proyek (Pro)
description: Topik ini menyediakan informasi tentang baris peluang berbasis proyek. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a688b9bed5a38e7b5947cbcee1e3cb8ab211e98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896375"
---
# <a name="project-based-opportunity-lines-pro"></a>Baris peluang berbasis proyek (Pro)

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Baris peluang berbasis proyek hanya tersedia dalam peluang berbasis proyek. Rekaman Peluang berbasis proyek memiliki nilai bidang **Jenis** yang diatur ke **berbasis pekerjaan**.

Baris peluang berbasis proyek adalah item baris yang akan dikirim kepada pelanggan yang menggunakan proyek. Namun, proyek tidak dapat dihubungkan ke baris peluang berbasis proyek. Proyek dapat dikaitkan ke item baris dari tahap **kuotasi** dan seterusnya karena biasanya peluang terjadi pada tahap awal perjanjian dalam siklus hidup penawaran. Penentuan berapa banyak proyek yang akan digunakan untuk memberikan pekerjaan untuk pelanggan adalah keputusan yang dibuat nanti dalam fase penjualan. Anda dapat menggunakan fase peluang untuk mengidentifikasi komponen pengiriman diskrit untuk pelanggan. Keputusan seputar jumlah aktual proyek yang digunakan untuk memberikan komponen ini dapat didorong keluar hingga informasi lebih lanjut diketahui tentang pekerjaan itu sendiri.

Di bawah ini adalah bidang pada baris peluang berbasis proyek:

| **Bidang** | **Lokasi** | **Relevansi, tujuan, dan panduan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Jenis Produk | Tab Umum (tersembunyi) | Anda dapat memilih salah satu dari opsi berikut ini:</br>- Layanan berbasis proyek (tersedia hanya Jika Dynamics 365 Operations terinstal)</br>- Produk (tersedia hanya bila Project Operations dan Dynamics 365 Sales diinstal) | Nilai bidang ini diatur ke **layanan berbasis proyek** saat Anda membuat baris peluang berbasis proyek dari kisi baris berbasis proyek pada peluang. <br> Jika Anda mengubah atau mengganti nilai ini, fungsi proyek tidak akan diaktifkan pada item baris berbasis proyek. |
| Peluang | Tab Umum | Bidang ini hanya baca dan merujuk rekaman peluang induk yang dimiliki item baris ini. | Tidak ada dampak hilir dari bidang ini. |
| Nama | Tab Umum | Ini adalah bidang teks yang dapat diedit yang dapat digunakan untuk memberikan identitas singkat ke item baris ini. | Nilai ini dibawa ke baris kuotasi saat Anda membuat kuotasi dari peluang ini. |
| Anggaran Pelanggan | Tab Umum | Bidang mata uang yang dapat diedit ini dapat digunakan untuk melacak jumlah yang bersedia dikeluarkan oleh pelanggan untuk item baris ini. | Nilai ini dibawa ke bidang terkait di baris kuotasi saat Anda membuat kuotasi dari peluang ini. |
| Metode Penagihan | Tab Umum | Bidang yang dapat diedit ini memiliki kemungkinan nilai:</br>- Waktu dan bahan</br>- Harga tetap | Nilai ini dibawa ke bidang terkait di baris kuotasi saat Anda membuat kuotasi dari peluang ini. Setelah baris kuotasi dibuat, bidang akan dikunci dan tidak dapat diubah. Tetapkan nilai bidang ini seakurat mungkin. Jika Anda perlu mengubah nilai bidang ini pada baris kuotasi, Hapus dan buat ulang baris kuotasi. |

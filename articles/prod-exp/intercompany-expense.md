---
title: Pengeluaran antarperusahaan
description: Artikel ini memberikan informasi tentang cara menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan.
author: suvaidya
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c58fb1510c9ba75bc81a4dc07b91f1b6a60355d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932392"
---
# <a name="intercompany-expenses"></a>Pengeluaran antarperusahaan

Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama. Anda dapat menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan. Badan hukum yang mempekerjakan pekerja disebut entitas hukum pemberi pinjaman. Badan hukum tempat pekerja mengalami pengeluaran disebut entitas hukum peminjam. 

Sebelum pekerja dapat membuat dan mengirimkan pengeluaran antarperusahaan, Anda harus mengaktifkan baris pengeluaran antarperusahaan. Di entitas hukum yang meminjamkan, pada halaman **Parameter manajemen pengeluaran**, pilih **izinkan baris pengeluaran antarperusahaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Posting pajak untuk pengeluaran antarperusahaan

[!include [banner](../includes/banner.md)]

Sebelum Anda dapat menggunakan grup pajak yang terkait dengan entitas hukum yang meminjamkan (sumber), bukan entitas hukum peminjam (tujuan) dalam laporan pengeluaran, Anda harus mengaktifkan fungsi dalam konfigurasi pajak penjualan buku besar umum. Bila **entitas hukum untuk parameter posting pajak antarperusahaan** diatur ke **Sumber** dan **Terapkan aturan perpajakan pajak penjualan** diatur ke **Tidak**, kombinasi pajak untuk entitas hukum yang meminjamkan digunakan. Bila parameter yang sama diatur ke **tujuan**, kombinasi pajak untuk entitas hukum peminjam akan digunakan. Untuk entitas hukum di Amerika Serikat, bila parameter diatur ke **sumber**, bidang **piutang pajak penjualan** juga harus dikonfigurasi pada halaman **grup posting buku besar** baru. Mesin akuntansi akan menggunakan informasi dari bidang ini untuk entri akuntansi terkait pajak.   
Perilaku ini sesuai untuk baris pengeluaran yang diposting dengan atau tanpa proyek.  

## <a name="new-expense-expression-builder"></a>Pembuat ekspresi pengeluaran baru

Pembuat ekspresi pengeluaran baru mengatasi masalah dengan skenario pengeluaran antar perusahaan yang menggunakan proyek. Fitur ini memastikan bahwa, ketika Anda membuat biaya antarperusahaan, kebijakan pengeluaran divalidasi dengan benar terhadap proyek yang dipilih pada lini pengeluaran, dan bahwa laporan pengeluaran dapat berhasil dikirimkan.

Agar fitur pembuat ekspresi pengeluaran berfungsi, fitur tersebut harus diaktifkan. Selain itu, kebijakan pengeluaran yang memiliki ID proyek harus disiapkan.

Jika Anda telah mengonfigurasi kebijakan yang memvalidasi ID proyek di lini pengeluaran, kebijakan tersebut harus dihentikan. Anda kemudian dapat mengaktifkan fitur dan mengonfigurasi ulang kebijakan.

Untuk mengaktifkan fitur, ikuti langkah di bawah ini.

1. Buka **Ruang kerja** \> **Manajemen Fitur**.
2. Di daftar, pilih **Pembuat ekspresi pengeluaran baru untuk mengatasi masalah dengan skenario pengeluaran antar perusahaan yang menggunakan proyek**. Lalu pilih **Aktifkan sekarang**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

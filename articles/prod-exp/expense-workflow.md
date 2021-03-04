---
title: Alur kerja manajemen pengeluaran
description: Topik ini menjelaskan cara menggunakan sistem alur kerja di Microsoft Dynamics 365 Finance, untuk mengkonfigurasi proses peninjauan untuk laporan pengeluaran dalam manajemen pengeluaran.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bbee90450749c89f643d96e4d41a387c45e9abc5
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960566"
---
# <a name="expense-management-workflow"></a>Alur kerja manajemen pengeluaran

Anda dapat menggunakan sistem alur kerja untuk mengkonfigurasi proses peninjauan untuk laporan pengeluaran dalam manajemen pengeluaran. Anda dapat mengkonfigurasi alur kerja yang menggunakan kriteria berikut untuk menentukan orang yang menyetujui laporan pengeluaran:

- Hierarki pelaporan karyawan dan batas persetujuan yang telah ditetapkan sebelumnya
- Persetujuan multi-level yang mendukung pemberi persetujuan dan pemberi persetujuan akhir
- Dimensi keuangan dan tanggung jawab proyek
- Penetapan ke pengguna atau grup pengguna tertentu

Persetujuan alur kerja dapat dibuat untuk laporan pengeluaran, permintaan perjalanan, uang tunai, dan pemulihan pajak pertambahan nilai (PPN).

**Contoh**

Proses berikut ini adalah contoh alur kerja manajemen pengeluaran untuk laporan pengeluaran.

1. Karyawan membuat dan menyimpan laporan pengeluaran.
2. Karyawan mengajukan laporan pengeluaran untuk persetujuan. Pemberi persetujuan diidentifikasi berdasarkan aturan yang ditentukan saat alur kerja disiapkan.
3. Pemberi persetujuan menerima pemberitahuan bahwa laporan pengeluaran siap untuk disetujui. Pemberi persetujuan akan memeriksa laporan pengeluaran dan memverifikasi bahwa kondisi berikut terpenuhi:

    - pengeluaran tidak melanggar kebijakan pengeluaran. Jika pengeluaran melanggar kebijakan, pemberi izin memverifikasi bahwa laporan pengeluaran mencakup pembenaran bisnis yang valid.
    - Tanda terima elektronik dilampirkan ke laporan pengeluaran.

4. Pemberi persetujuan menyetujui laporan pengeluaran.
5. Laporan pengeluaran ditetapkan ke Koordinator utang dagang untuk posting.
6. Salah satu langkah berikut terjadi, tergantung pada apakah posting otomatis dikonfigurasi:

    - Jika posting otomatis dikonfigurasi, laporan pengeluaran diproses untuk pembayaran, dan status laporan pengeluaran diperbarui.
    - Jika posting otomatis tidak dikonfigurasi, Koordinator utang dagang akan memverifikasi bahwa semua tanda terima asli telah dikirim dan bahwa tanda terima disesuaikan dengan pengeluaran di laporan pengeluaran. Semua kode pajak yang dimasukkan pada laporan pengeluaran juga harus diverifikasi sebagai benar.

Setelah persyaratan ini diverifikasi, laporan pengeluaran akan dikirim.

Setelah laporan pengeluaran dikirim, pembayaran disahkan untuk laporan pengeluaran, dan uang karyawan akan diganti.

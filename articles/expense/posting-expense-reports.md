---
title: Memposting laporan pengeluaran
description: Artikel ini menjelaskan cara memposting laporan pengeluaran.
author: ramagadu
ms.date: 08/12/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: d0ae4559a08553236158a663513401cb38cbe28f
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524873"
---
# <a name="post-expense-reports"></a>Memposting laporan pengeluaran

Setelah laporan pengeluaran disetujui dan ditransfer ke jurnal umum, dapat diposting. Ketika Anda memposting laporan pengeluaran, pengeluaran yang memenuhi syarat untuk pemulihan pajak pertambahan nilai (PPN) diidentifikasi. Tugas memverifikasi dan memulihkan pembayaran PPN ditetapkan ke karyawan yang bertanggung jawab untuk memverifikasi laporan pengeluaran.

Jika pengeluaran pada laporan pengeluaran dibebankan kepada perusahaan selain perusahaan yang mempekerjakan karyawan, Anda harus memverifikasi kedua perusahaan tentang pengeluaran tersebut terutang pada perusahaan mana dan harus dibayar oleh perusahaan mana. Misalnya, karyawan yang mengirimkan laporan pengeluaran bekerja untuk perusahaan DAT namun pengeluaran dibebankan ke perusahaan DIR. Dalam kasus ini, DAT adalah perusahaan yang berpiutang, dan DIR adalah perusahaan yang berutang. Setelah Anda memverifikasi baris jurnal ini, Anda dapat mengirim baris pengeluaran ke buku besar.

Untuk memposting laporan pengeluaran, pada halaman **laporan pengeluaran yang disetujui**, pilih laporan pengeluaran, lalu di panel tindakan, pilih **posting**.

Anda juga dapat memposting semua laporan pengeluaran dalam daftar secara bersamaan. Pilih Semua laporan pengeluaran, lalu pilih **posting**.

## <a name="enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature"></a>Mengaktifkan Kemampuan untuk memposting tanggung jawab pengeluaran dalam mata uang vendor untuk fitur metode pembayaran tunai

Fitur **Kemampuan untuk memposting tanggung jawab pengeluaran dalam mata uang vendor untuk metode pembayaran tunai** memungkinkan laporan pengeluaran diposting dalam mata uang vendor untuk metode pembayaran tunai.

Saat ini, saat Anda mengirimkan pengeluaran tunai, laporan pengeluaran diposting dalam mata uang akuntansi. Karena konversi jumlah di antara mata uang transaksi, mata uang akuntansi, dan mata uang vendor, jumlah yang salah dibayar ke vendor jika tanggal transaksi pengeluaran dan tanggal pembayaran aktual memiliki nilai tukar yang berbeda.

Fitur ini akan memastikan bahwa saldo vendor dicatat dalam mata uang vendor saat laporan pengeluaran diposting.

1. Buka **Ruang kerja** \> **Manajemen Fitur**.
2. Dalam daftar, cari dan pilih **Kemampuan untuk memposting tanggung jawab pengeluaran dalam mata uang vendor untuk metode pembayaran tunai**, lalu pilih **Aktifkan sekarang**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

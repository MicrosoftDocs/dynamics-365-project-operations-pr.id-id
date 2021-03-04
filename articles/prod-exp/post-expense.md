---
title: Memposting laporan pengeluaran
description: Topik ini menjelaskan cara posting laporan pengeluaran untuk buku besar.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 982b7621c35547448b5d756f77f3873b9fbbcb9d
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960116"
---
# <a name="post-an-expense-report"></a>Memposting laporan pengeluaran

Setelah laporan pengeluaran disetujui dan ditransfer ke jurnal umum, dapat diposting ke buku besar. Ketika Anda memposting laporan pengeluaran, pengeluaran yang memenuhi syarat untuk pemulihan pajak pertambahan nilai (PPN) diidentifikasi. Tugas memverifikasi dan memulihkan pembayaran PPN ditetapkan ke karyawan yang bertanggung jawab untuk memverifikasi laporan pengeluaran.

Jika pengeluaran pada laporan pengeluaran dibebankan kepada perusahaan selain perusahaan yang mempekerjakan karyawan, Anda harus memverifikasi perusahaan tentang pengeluaran tersebut terutang pada perusahaan mana dan pengeluaran harus dibayar oleh perusahaan mana. Misalnya, karyawan yang mengirimkan laporan pengeluaran bekerja untuk perusahaan DAT namun pengeluaran dibebankan ke perusahaan DIR. Dalam kasus ini, DAT adalah perusahaan yang berpiutang, dan DIR adalah perusahaan yang berutang. Setelah Anda memverifikasi baris jurnal ini, Anda dapat mengirim baris pengeluaran ke buku besar.

Untuk memposting laporan pengeluaran, pada halaman **laporan pengeluaran yang disetujui**, pilih laporan pengeluaran, lalu di panel tindakan, pilih **posting**.

Anda juga dapat memposting semua laporan pengeluaran dalam daftar secara bersamaan. Pilih Semua laporan pengeluaran, lalu pilih **posting**.

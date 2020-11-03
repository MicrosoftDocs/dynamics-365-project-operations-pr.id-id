---
title: Laporan pengeluaran dan beberapa pemberi izin
description: Topik ini menyediakan informasi tentang laporan pengeluaran yang memerlukan persetujuan dari lebih dari satu orang.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 548673541cee5ce598721f94415c0444995c8325
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078487"
---
# <a name="expense-reports-and-multiple-approvers"></a>Laporan pengeluaran dan beberapa pemberi izin

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Tergantung pada kebijakan persetujuan pengeluaran organisasi Anda, lebih dari satu orang mungkin harus menyetujui laporan pengeluaran yang diajukan. Bila Anda mengkonfigurasi proses alur kerja untuk persetujuan laporan pengeluaran, Anda dapat menambahkan elemen alur kerja yang mencakup tugas atau langkah-langkah untuk satu pemberi izin laporan pengeluaran. Misalnya, Anda mungkin mengharuskan semua laporan biaya disetujui oleh dua orang terpisah, manajer karyawan yang mengajukan laporan dan koordinator utang dagang.

Jika Anda memutuskan untuk meminta beberapa penyetuju laporan pengeluaran, Anda dapat menambahkan elemen alur kerja dengan salah satu cara berikut:

- Tambahkan satu elemen persetujuan yang memiliki satu langkah. Misalnya, langkah ini mungkin memerlukan laporan pengeluaran yang ditetapkan ke grup pengguna, dan bahwa laporan tersebut disetujui oleh 50 persen dari anggota grup pengguna.
- Tambahkan satu elemen persetujuan yang memiliki beberapa langkah. Misalnya, elemen persetujuan mungkin memiliki langkah berikut:

    1. Manajer karyawan yang mengajukan laporan pengeluaran menyetujuinya.
    2. Petugas utang dagang memverifikasi tanda terima dan item laporan pengeluaran.
    3. Pemilik anggaran menyetujui laporan pengeluaran.

- Tambahkan beberapa elemen persetujuan, yang masing-masing memiliki satu langkah. Misalnya, Anda dapat menambahkan elemen persetujuan terpisah untuk setiap langkah berikut:

    1. Manajer karyawan menyetujui laporan pengeluaran.
    2. Pemilik anggaran menyetujui laporan pengeluaran.

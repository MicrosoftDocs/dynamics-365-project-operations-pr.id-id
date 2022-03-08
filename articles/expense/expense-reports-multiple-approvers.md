---
title: Laporan pengeluaran dan beberapa pemberi izin
description: Topik ini menyediakan informasi tentang laporan pengeluaran yang memerlukan persetujuan dari lebih dari satu orang.
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2acae2d518a02539f01d5498450236999fe609d1e8f26b5f90e18b986b83cab1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988430"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
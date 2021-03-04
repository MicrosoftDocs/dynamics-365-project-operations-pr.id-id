---
title: Beberapa pemberi persetujuan pada laporan pengeluaran
description: Topik ini menyediakan informasi tentang laporan pengeluaran yang memerlukan persetujuan dari beberapa orang.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960611"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Beberapa pemberi persetujuan pada laporan pengeluaran

Tergantung pada kebijakan persetujuan pengeluaran organisasi Anda, lebih dari satu orang mungkin harus menyetujui laporan pengeluaran yang diajukan oleh seorang karyawan. Bila Anda mengkonfigurasi proses alur kerja untuk persetujuan laporan pengeluaran, Anda dapat menambahkan elemen alur kerja yang mencakup tugas atau langkah-langkah untuk satu pemberi izin laporan pengeluaran. Misalnya, Anda mungkin mengharuskan semua laporan biaya disetujui pertama oleh manajer karyawan yang mengajukan laporan dan kemudian oleh koordinator utang dagang.

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
---
title: Pengeluaran antarperusahaan
description: Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama. Dalam situasi ini, Anda dapat menggunakan fitur biaya antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum pekerjaan yang dilakukan.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078635"
---
# <a name="intercompany-expenses"></a>Pengeluaran antarperusahaan

[!include [banner](../includes/banner.md)]

Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama. Dalam situasi ini, Anda dapat menggunakan fitur biaya antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum pekerjaan yang dilakukan. Badan hukum yang mempekerjakan pekerja disebut entitas hukum pemberi pinjaman. Badan hukum tempat pekerja mengalami pengeluaran disebut entitas hukum peminjam. 

Sebelum pekerja dapat membuat dan mengajukan pengeluaran untuk pekerjaan yang dilakukan untuk entitas hukum yang berbeda, di entitas hukum pemberi pinjaman, pada halaman **parameter manajemen pengeluaran** , pilih opsi **Izinkan baris pengeluaran antarperusahaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Posting pajak untuk pengeluaran antarperusahaan

[!include [banner](../includes/banner.md)]

Jika Anda ingin menggunakan grup pajak yang terkait dengan entitas hukum pemberi pinjaman (sumber) alih-alih entitas hukum peminjam (tujuan) dalam laporan pengeluaran Anda, Anda harus mengkonfigurasi ini di konfigurasi pajak penjualan buku besar umum. Bila parameter buku besar, **entitas hukum untuk posting pajak antarperusahaan** diatur ke **sumber** dan **menerapkan aturan pajak pajak penjualan** diatur ke **tidak** , kombinasi pajak untuk entitas hukum pemberi pinjaman akan digunakan. Bila parameter yang sama diatur ke **tujuan** , kombinasi pajak untuk entitas hukum peminjam akan digunakan. Untuk entitas hukum di Amerika Serikat, bila parameter diatur ke **sumber** , bidang **piutang pajak penjualan** juga harus dikonfigurasi pada halaman **grup posting buku besar** baru. Mesin akuntansi akan menggunakan informasi dari bidang ini untuk entri akuntansi terkait pajak.   
Perilaku ini sesuai untuk baris pengeluaran yang diposting dengan atau tanpa proyek.  

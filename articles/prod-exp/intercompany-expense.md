---
title: Pengeluaran antarperusahaan
description: Topik ini memberikan informasi tentang cara menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960836"
---
# <a name="intercompany-expenses"></a>Pengeluaran antarperusahaan

Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama. Anda dapat menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan. Badan hukum yang mempekerjakan pekerja disebut entitas hukum pemberi pinjaman. Badan hukum tempat pekerja mengalami pengeluaran disebut entitas hukum peminjam. 

Sebelum pekerja dapat membuat dan mengirimkan pengeluaran antarperusahaan, Anda harus mengaktifkan baris pengeluaran antarperusahaan. Di entitas hukum yang meminjamkan, pada halaman **Parameter manajemen pengeluaran**, pilih **izinkan baris pengeluaran antarperusahaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Posting pajak untuk pengeluaran antarperusahaan

[!include [banner](../includes/banner.md)]

Sebelum Anda dapat menggunakan grup pajak yang terkait dengan entitas hukum yang meminjamkan (sumber), bukan entitas hukum peminjam (tujuan) dalam laporan pengeluaran, Anda harus mengaktifkan fungsi dalam konfigurasi pajak penjualan buku besar umum. Bila **entitas hukum untuk parameter posting pajak antarperusahaan** diatur ke **Sumber** dan **Terapkan aturan perpajakan pajak penjualan** diatur ke **Tidak**, kombinasi pajak untuk entitas hukum yang meminjamkan digunakan. Bila parameter yang sama diatur ke **tujuan**, kombinasi pajak untuk entitas hukum peminjam akan digunakan. Untuk entitas hukum di Amerika Serikat, bila parameter diatur ke **sumber**, bidang **piutang pajak penjualan** juga harus dikonfigurasi pada halaman **grup posting buku besar** baru. Mesin akuntansi akan menggunakan informasi dari bidang ini untuk entri akuntansi terkait pajak.   
Perilaku ini sesuai untuk baris pengeluaran yang diposting dengan atau tanpa proyek.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]
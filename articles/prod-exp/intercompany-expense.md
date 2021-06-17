---
title: Pengeluaran antarperusahaan
description: Topik ini memberikan informasi tentang cara menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan.
author: ShylaThompson
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d2cdba8d5368a8b26bf4d98226bda76a58261cf0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005075"
---
# <a name="intercompany-expenses"></a>Pengeluaran antarperusahaan

Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama. Anda dapat menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan. Badan hukum yang mempekerjakan pekerja disebut entitas hukum pemberi pinjaman. Badan hukum tempat pekerja mengalami pengeluaran disebut entitas hukum peminjam. 

Sebelum pekerja dapat membuat dan mengirimkan pengeluaran antarperusahaan, Anda harus mengaktifkan baris pengeluaran antarperusahaan. Di entitas hukum yang meminjamkan, pada halaman **Parameter manajemen pengeluaran**, pilih **izinkan baris pengeluaran antarperusahaan**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Posting pajak untuk pengeluaran antarperusahaan

[!include [banner](../includes/banner.md)]

Sebelum Anda dapat menggunakan grup pajak yang terkait dengan entitas hukum yang meminjamkan (sumber), bukan entitas hukum peminjam (tujuan) dalam laporan pengeluaran, Anda harus mengaktifkan fungsi dalam konfigurasi pajak penjualan buku besar umum. Bila **entitas hukum untuk parameter posting pajak antarperusahaan** diatur ke **Sumber** dan **Terapkan aturan perpajakan pajak penjualan** diatur ke **Tidak**, kombinasi pajak untuk entitas hukum yang meminjamkan digunakan. Bila parameter yang sama diatur ke **tujuan**, kombinasi pajak untuk entitas hukum peminjam akan digunakan. Untuk entitas hukum di Amerika Serikat, bila parameter diatur ke **sumber**, bidang **piutang pajak penjualan** juga harus dikonfigurasi pada halaman **grup posting buku besar** baru. Mesin akuntansi akan menggunakan informasi dari bidang ini untuk entri akuntansi terkait pajak.   
Perilaku ini sesuai untuk baris pengeluaran yang diposting dengan atau tanpa proyek.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]
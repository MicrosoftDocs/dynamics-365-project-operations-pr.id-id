---
title: Kesalahan ketidakcocokan mata uang
description: Ini topik memberikan informasi pemecahan masalah tentang kesalahan ketidakcocokan mata uang yang terjadi saat Anda menyimpan jenis rekaman tertentu.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bb54a121f0dc22f1c0ea88ada9c922c1d4c6544
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589752"
---
# <a name="currency-mismatch-error"></a>Kesalahan ketidakcocokan mata uang 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Saat Anda menyimpan proyek, kontrak, penawaran, atau sumber daya yang dapat dipesan, Anda mungkin menerima kesalahan, **Memiliki mata uang perusahaan tidak cocok dengan mata uang unit kontrak. Pilih perusahaan pemilik atau unit kontraktor yang berbeda untuk melanjutkan**. Ini karena ada ketidakcocokan mata uang antara mata uang unit kontrak untuk catatan dan mata uang perusahaan pemilik.


## <a name="resolution"></a>Resolusi

Untuk mengatasi masalah ini, lakukan hal berikut:
- Verifikasi mata uang unit kontraktor untuk catatan ini. Anda dapat melihat mata uang dengan membuka catatan unit organisasi dan memverifikasi nilai pada **tab Umum** di **bidang Mata Uang**.
- Verifikasi mata uang perusahaan pemilik. Anda dapat melihat mata uang dengan membuka **Buku Besar** > **Terkait** dalam catatan perusahaan. Klik dua kali catatan buku besar yang terkait dengan perusahaan dan verifikasi nilai pada **tab Umum** di **bidang Mata Uang** akuntansi.

Jika mata uang yang ditetapkan dalam unit kontrak dan catatan buku besar tidak cocok, sesuaikan konfigurasi atau pilih nilai yang berbeda saat Anda menyimpan catatan. Sistem mengharuskan catatan-catatan ini untuk dicocokkan untuk memastikan aliran faktur antar kompanan yang benar. Untuk informasi selengkapnya tentang konfigurasi antar perusahaan, lihat [Membuat transaksi](../../project-accounting/create-intercompany-transactions.md) antar perusahaan.

Jika catatan perusahaan tidak memiliki catatan buku besar terkait, ini menunjukkan bahwa ada konfigurasi yang hilang saat menyiapkan lingkungan. Konfigurasi harus diperbaiki oleh administrator sistem. Administrator sistem harus pergi ke **konfigurasi** Dual-write dan menghentikan dan me-restart **Ledgers dual-write map** dengan sinkronisasi awal peta ini dan prasyaratnya. Untuk informasi lebih lanjut, lihat [versi peta tulis ganda Project Operations](../../environment/resource-dual-write-maps.md).

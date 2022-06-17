---
title: Kesalahan ketidakcocokan mata uang
description: Artikel ini menyediakan informasi pemecahan masalah tentang kesalahan ketidakcocokan mata uang yang terjadi saat Anda menyimpan jenis catatan tertentu.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5b0973a340dec8e68f326803d75bea9803e19791
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914728"
---
# <a name="currency-mismatch-error"></a>Kesalahan ketidakcocokan mata uang 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Saat Anda menyimpan proyek, kontrak, kutipan, atau sumber daya yang dapat dipesan, Anda mungkin menerima kesalahan, **Memiliki mata uang perusahaan tidak cocok dengan mata uang unit kontrak. Pilih perusahaan pemilik atau unit kontraktor yang berbeda untuk melanjutkan**. Ini karena ada ketidakcocokan mata uang antara mata uang unit kontrak untuk catatan dan mata uang perusahaan pemilik.


## <a name="resolution"></a>Resolusi

Untuk mengatasi masalah ini, lakukan hal berikut:
- Verifikasi mata uang unit kontrak untuk catatan ini. Anda dapat melihat mata uang dengan membuka data unit organisasi dan memverifikasi nilai pada tab **Umum** di **bidang Mata Uang**.
- Verifikasi mata uang perusahaan pemilik. Anda dapat melihat mata uang dengan membuka **Buku Besar** > **Terkait** di catatan perusahaan. Klik ganda catatan buku besar yang terkait dengan perusahaan dan verifikasi nilai pada tab **Umum** di **bidang mata uang** Akuntansi.

Jika mata uang yang ditetapkan dalam unit kontrak dan catatan buku besar tidak cocok, sesuaikan konfigurasi atau pilih nilai yang berbeda saat Anda menyimpan catatan. Sistem memerlukan catatan ini agar sesuai untuk memastikan alur faktur antar perusahaan yang benar. Untuk informasi selengkapnya tentang konfigurasi antar perusahaan, lihat [Membuat transaksi](../../project-accounting/create-intercompany-transactions.md) antar perusahaan.

Jika catatan perusahaan tidak memiliki catatan buku besar terkait, ini menunjukkan bahwa ada konfigurasi yang hilang saat menyiapkan lingkungan. Konfigurasi harus diperbaiki oleh administrator sistem. Administrator sistem harus pergi ke **konfigurasi** Dual-write dan menghentikan dan memulai ulang **peta** tulis ganda Ledgers dengan sinkronisasi awal peta ini dan prasyaratnya. Untuk informasi lebih lanjut, lihat [versi peta tulis ganda Project Operations](../../environment/resource-dual-write-maps.md).

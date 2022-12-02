---
title: Kesalahan Ketidakcocokan mata uang
description: Artikel ini memberikan informasi pemecahan masalah tentang kesalahan ketidakcocokan mata uang yang terjadi saat Anda menyimpan jenis. rekaman tertentu.
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
# <a name="currency-mismatch-error"></a>Kesalahan Ketidakcocokan mata uang 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Jika Anda menyimpan suatu proyek, kontrak, kuotasi, atau sumber daya yang dapat dipesan, Anda mungkin menerima kesalahan, **Mata uang Perusahaan pemilik tidak cocok dengan mata uang unit. Pilih perusahaan pemilik atau unit kontrak yang berbeda untuk melanjutkan**. Hal ini dikarenakan terdapat ketidakcocokan mata uang antara mata uang unit kontrak untuk rekaman dan mata uang perusahaan pemilik.


## <a name="resolution"></a>Resolusi

Untuk menyelesaikan masalah ini, lakukan langkah berikut:
- Verifikasikan mata uang unit kontrak untuk rekaman ini. Anda dapat melihat mata uang dengan membuka rekaman unit organisasional dan memverifikasi nilai pada tab **Umum** pada bidang **Mata Uang**.
- Pastikan mata uang perusahaan pemilik. Anda dapat melihat mata uang dengan masuk ke **Terkait** > **Buku Besar** di rekaman perusahaan. Klik dua kali rekaman buku besar yang terkait dengan perusahaan dan verifikasikan nilai pada tab **Umum** pada bidang **Mata Uang Akuntansi**.

Jika mata uang yang diatur di unit kontrak dan rekaman buku besar tidak cocok, sesuaikan konfigurasi atau pilih nilai yang berbeda saat Anda menyimpan rekaman. Sistem memerlukan rekaman ini agar sesuai untuk memastikan aliran faktur antarperusahaan yang benar. Untuk informasi lebih lanjut tentang konfigurasi antarperusahaan, lihat [Membuat transaksi antarperusahaan](../../project-accounting/create-intercompany-transactions.md).

Jika rekaman perusahaan tidak memiliki rekaman buku besar yang terkait, hal ini menunjukkan bahwa konfigurasi tidak ada saat mengatur lingkungan. Konfigurasi harus diperbaiki oleh administrator sistem. Administrator sistem harus membuka **konfigurasi Penulisan ganda** dan menghentikan dan memulai ulang **peta penulisan ganda buku besar** dengan sinkronisasi awal peta ini dan prasyaratnya. Untuk informasi lebih lanjut, lihat [versi peta tulis ganda Project Operations](../../environment/resource-dual-write-maps.md).

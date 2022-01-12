---
title: Kesalahan ketidakcocokan mata uang
description: Ini topik memberikan informasi pemecahan masalah tentang kesalahan ketidakcocokan mata uang yang terjadi ketika Anda menyimpan jenis catatan tertentu.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 52e33ad3728e1a393e8c7e3ca4e0a4b506d0b774
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903696"
---
# <a name="currency-mismatch-error"></a>Kesalahan ketidakcocokan mata uang 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Ketika Anda menyimpan proyek, kontrak, kutipan, atau sumber daya yang dapat dipesan, Anda mungkin menerima kesalahan, **Memiliki mata uang perusahaan tidak sesuai dengan mata uang unit kontraktor. Pilih perusahaan pemilik yang berbeda atau unit kontraktor untuk melanjutkan**. Ini karena ada ketidakcocokan mata uang antara mata uang unit kontrak untuk catatan dan mata uang perusahaan yang memiliki.


## <a name="resolution"></a>Resolusi

Untuk mengatasi masalah ini, lakukan hal berikut:
- Verifikasi mata uang unit kontraktor untuk catatan ini. Anda dapat melihat mata uang dengan membuka catatan unit organisasi dan memverifikasi nilai pada **tab Umum di bidang Mata** **Uang**.
- Verifikasi mata uang perusahaan pemilik. Anda dapat melihat mata uang dengan pergi ke **Buku Besar Terkait dalam catatan** > **perusahaan**. Klik dua kali catatan buku besar yang terkait dengan perusahaan dan verifikasi nilai pada **tab Umum di bidang mata uang** **Akuntansi**.

Jika mata uang yang ditetapkan dalam unit kontrak dan catatan buku besar tidak cocok, sesuaikan konfigurasi atau pilih nilai yang berbeda saat Anda menyimpan catatan. Sistem ini membutuhkan catatan ini untuk mencocokkan untuk memastikan aliran faktur antarkompeti yang benar. Untuk informasi selengkapnya tentang konfigurasi antar komplotany, lihat [Membuat transaksi antar](../../project-accounting/create-intercompany-transactions.md) perusahaan.

Jika catatan perusahaan tidak memiliki catatan buku besar terkait, ini menunjukkan bahwa ada konfigurasi yang hilang saat menyiapkan lingkungan. Konfigurasi harus diperbaiki oleh administrator sistem. Administrator sistem harus pergi ke **konfigurasi Dual-write** dan menghentikan dan memulai ulang peta penulisan ganda **Ledgers** dengan sinkronisasi awal peta ini dan prasyaratnya. Untuk informasi lebih lanjut, lihat [versi peta tulis ganda Project Operations](../../environment/resource-dual-write-maps.md).

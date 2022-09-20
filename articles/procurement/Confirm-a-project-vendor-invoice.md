---
title: Mengonfirmasi faktur vendor proyek
description: Artikel ini menjelaskan cara mengonfirmasi faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan menjelaskan dampak keuangan dari konfirmasi faktur vendor proyek.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475479"
---
# <a name="confirm-project-vendor-invoices"></a>Mengonfirmasi faktur vendor proyek

**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok

**Ketika parameter Manual confirmation by PM is required** diaktifkan, faktur vendor yang dibuat memiliki Microsoft Dataverse **status Draf**. Faktur vendor yang dibuat dengan cara ini harus ditinjau dan dikonfirmasi secara manual. **Ketika parameter Manual confirmation by PM is required** dinonaktifkan, faktur vendor yang dibuat di Dataverse akan dikonfirmasi secara otomatis. Tidak diperlukan tindakan lebih lanjut. 

Setelah Anda memverifikasi semua baris pada faktur vendor, Dynamics 365 Project Operations pilih **Konfirmasi** untuk mengonfirmasi faktur vendor.

Ketika Anda memilih **Konfirmasi** pada faktur vendor, perilaku berikut terjadi:

1. Status faktur vendor diperbarui menjadi **Dikonfirmasi**.
1. Faktur vendor yang dikonfirmasi dan catatan terkaitnya menjadi baca-saja, dan tidak dapat diedit atau dihapus.
1. Jika ada aktual biaya yang mereferensikan baris faktur vendor sebagai bagian dari proses pencocokan, semua aktual biaya yang terkait dengan baris faktur vendor yang dirujuk akan dibatalkan.
1. Aktual biaya baru dibuat dengan menggunakan informasi pada baris faktur vendor.
1. Anda tidak dapat lagi membuat jurnal koreksi, memproses penarikan kembali entri waktu, atau membatalkan persetujuan waktu, pengeluaran, atau aktual material asli yang dibalik.
1. Dalam Dynamics 365 Finance, **nilai biaya** Proyek diperbarui dengan menggunakan jurnal integrasi Proyek, dan akun *integrasi Pengadaan dibalik* setelah jurnal integrasi Proyek diposting.

> [!NOTE]
> Jika ada baris pada faktur vendor yang memiliki status verifikasi selain **Selesai**, faktur vendor tidak dapat dikonfirmasi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

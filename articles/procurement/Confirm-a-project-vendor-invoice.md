---
title: Mengonfirmasi faktur vendor proyek
description: Artikel ini menjelaskan cara mengonfirmasikan faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan mend dampak keuangan dari mengonfirmasikan faktur vendor proyek.
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

Bila **diperlukan konfirmasi Manual oleh PM parameter** diaktifkan, faktur vendor yang dibuat di Microsoft Dataverse memiliki status **Draf**. Faktur vendor yang dibuat dengan cara ini harus ditinjau dan dikonfirmasi secara manual. Bila parameter **diperlukan konfirmasi Manual oleh PM** dinonaktifkan, faktur vendor yang dibuat di Dataverse otomatis dikonfirmasi. Tidak diperlukan tindakan lebih lanjut. 

Setelah Anda memverifikasi semua baris pada faktur vendor di Dynamics 365 Project Operations, pilih **Konfirmasikan** untuk mengkonfirmasikan faktur vendor.

Ketika Anda memilih **Konfirmasi** pada faktur vendor, perilaku berikut terjadi:

1. Status faktur vendor diperbarui ke **Dikonfirmasi**.
1. Faktur vendor yang dikonfirmasi dan rekaman terkaitnya menjadi hanya baca dan tidak dapat diedit atau dihapus.
1. Jika aktual biaya apa pun mereferensikan baris faktur vendor sebagai bagian dari proses pencocokan, semua aktual biaya yang terkait dengan baris faktur vendor referensi akan dibalik.
1. Aktual biaya baru dibuat menggunakan informasi pada baris faktur vendor.
1. Anda tidak dapat lagi membuat jurnal koreksi, memproses penarikan entri waktu, dan membatalkan persetujuan waktu, pengeluaran, atau aktual bahan asli yang telah dibalik.
1. Di Dynamics 365 Finance, nilai **biaya proyek** diperbarui menggunakan jurnal integrasi Proyek, dan akun integrasi Pengadaan akan *dibalik* setelah jurnal integrasi Proyek diposting.

> [!NOTE]
> Jika baris di faktur vendor memiliki status verifikasi selain **Selesai**, faktur vendor tidak dapat dikonfirmasi.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

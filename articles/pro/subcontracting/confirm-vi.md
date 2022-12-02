---
title: Mengonfirmasi faktur vendor proyek
description: Artikel ini menjelaskan cara mengonfirmasikan faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan dampak keuangan dari mengonfirmasikan faktur vendor proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261515"
---
# <a name="confirm-a-project-vendor-invoice"></a>Mengonfirmasi faktur vendor proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Setelah Anda memverifikasi semua baris pada faktur vendor di Microsoft Dynamics 365 Project Operations, Anda dapat menggunakan tindakan Konfirmasikan untuk mengkonfirmasikan faktur vendor.

Ketika Anda memilih **Konfirmasi** pada faktur vendor, perilaku berikut terjadi:

1. Status faktur vendor diperbarui ke **Dikonfirmasi**.
2. Faktur vendor yang dikonfirmasi dan rekaman terkaitnya menjadi hanya baca dan tidak dapat diedit atau dihapus.
3. Jika aktual biaya apa pun mereferensikan baris faktur vendor sebagai bagian dari proses pencocokan, semua aktual biaya yang terkait dengan baris faktur vendor referensi akan dibalik.
4. Aktual biaya baru dibuat menggunakan informasi pada baris faktur vendor.
5. Setelah faktur vendor dikonfirmasi, Anda tidak dapat lagi membuat jurnal koreksi, memproses penarikan entri waktu, atau membatalkan persetujuan waktu, pengeluaran, atau aktual bahan asli yang dibalik.

> [!NOTE]
> Jika baris di faktur vendor memiliki status verifikasi selain **Selesai**, faktur vendor tidak dapat dikonfirmasi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

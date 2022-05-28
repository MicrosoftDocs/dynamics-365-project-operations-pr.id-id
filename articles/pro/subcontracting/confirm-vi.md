---
title: Mengonfirmasi faktur vendor proyek
description: Ini topik menjelaskan cara mengonfirmasi faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan dampak keuangan dari mengonfirmasi faktur vendor proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c248b3baec6d3f14a020e4fa93f3dad50c65b263
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8595732"
---
# <a name="confirm-a-project-vendor-invoice"></a>Mengonfirmasi faktur vendor proyek

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Setelah memverifikasi semua baris pada faktur vendor di Microsoft Dynamics 365 Project Operations, Anda dapat menggunakan tindakan Konfirmasi untuk mengonfirmasi faktur vendor.

Saat Anda memilih **Konfirmasi** pada faktur vendor, perilaku berikut terjadi:

1. Status faktur vendor diperbarui ke **Dikonfirmasi**.
2. Faktur vendor yang dikonfirmasi dan catatan terkaitnya menjadi hanya-baca, dan tidak dapat diedit atau dihapus.
3. Jika ada aktual biaya yang mereferensikan baris faktur vendor sebagai bagian dari proses pencocokan, semua aktual biaya yang terkait dengan baris faktur vendor yang dirujuk dibalik.
4. Aktual biaya baru dibuat dengan menggunakan informasi pada baris faktur vendor.
5. Setelah faktur vendor dikonfirmasi, Anda tidak dapat lagi membuat jurnal koreksi, memproses penarikan waktu masuk, atau membatalkan persetujuan waktu asli, biaya, atau aktual material yang dibalik.

> [!NOTE]
> Jika ada baris pada faktur vendor yang memiliki status verifikasi selain **Selesai**, faktur vendor tidak dapat dikonfirmasi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

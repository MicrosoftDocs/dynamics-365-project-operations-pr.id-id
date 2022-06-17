---
title: Mengonfirmasi faktur vendor proyek
description: Artikel ini menjelaskan cara mengonfirmasi faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan dampak finansial dari konfirmasi faktur vendor proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932438"
---
# <a name="confirm-a-project-vendor-invoice"></a>Mengonfirmasi faktur vendor proyek

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Setelah memverifikasi semua baris pada faktur vendor di Microsoft Dynamics 365 Project Operations, Anda dapat menggunakan tindakan Konfirmasi untuk mengonfirmasi faktur vendor.

Ketika Anda memilih **Konfirmasi** pada faktur vendor, perilaku berikut terjadi:

1. Status faktur vendor diperbarui ke **Dikonfirmasi**.
2. Faktur vendor yang dikonfirmasi dan catatan terkaitnya menjadi baca-saja, dan tidak dapat diedit atau dihapus.
3. Jika ada aktual biaya yang mereferensikan baris faktur vendor sebagai bagian dari proses pencocokan, semua aktual biaya yang terkait dengan baris faktur vendor yang dirujuk akan dibatalkan.
4. Aktual biaya baru dibuat dengan menggunakan informasi pada baris faktur vendor.
5. Setelah faktur vendor dikonfirmasi, Anda tidak dapat lagi membuat jurnal koreksi, memproses penarikan entri waktu, atau membatalkan persetujuan waktu, pengeluaran, atau aktual material asli yang dibalik.

> [!NOTE]
> Jika ada baris pada faktur vendor yang memiliki status verifikasi selain **Selesai**, faktur vendor tidak dapat dikonfirmasi.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

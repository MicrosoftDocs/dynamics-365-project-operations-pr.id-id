---
title: Membatalkan faktur vendor proyek
description: Ini topik menjelaskan cara membatalkan faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan dampak keuangan dari pembatalan faktur vendor proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580644"
---
# <a name="cancel-a-project-vendor-invoice"></a>Membatalkan faktur vendor proyek

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Setelah faktur vendor dikonfirmasi, faktur tersebut tidak dapat diedit atau dihapus. Jika ada kesalahan pada faktur vendor yang dikonfirmasi, Anda dapat menggunakan tindakan Batalkan untuk membalikkan dampak faktur vendor dan membuat faktur vendor baru.

Saat Anda memilih **Batalkan** pada faktur vendor, perilaku berikut akan terjadi:

1. Status faktur vendor diperbarui ke **Dibatalkan**.
2. Faktur vendor yang dibatalkan dan catatan terkaitnya menjadi hanya-baca, dan tidak dapat diedit atau dihapus.
3. Setiap aktual biaya yang dibuat berdasarkan baris faktur vendor sebagai bagian dari konfirmasi faktur vendor dibalik.
4. Jika ada aktual biaya yang ditautkan ke baris faktur vendor sebagai bagian dari proses pencocokan, konfirmasi faktur vendor asli membalikkannya. Selama pembatalan faktur vendor, aktual biaya tersebut dibuat ulang. Asal-usul menunjuk ke waktu, biaya, atau entri penggunaan material.
5. Setelah faktur vendor dibatalkan, Anda dapat sekali lagi membuat jurnal koreksi, memproses penarikan entri waktu, dan membatalkan persetujuan waktu, pengeluaran, atau aktual material asli.

> [!NOTE]
> Hanya faktur vendor proyek yang dikonfirmasi yang dapat dibatalkan. Faktur vendor di negara bagian lain tidak dapat dibatalkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

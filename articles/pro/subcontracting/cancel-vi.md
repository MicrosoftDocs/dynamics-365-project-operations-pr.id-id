---
title: Membatalkan faktur vendor proyek
description: Artikel ini menjelaskan cara membatalkan faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan dampak finansial dari pembatalan faktur vendor proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911554"
---
# <a name="cancel-a-project-vendor-invoice"></a>Membatalkan faktur vendor proyek

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Setelah faktur vendor dikonfirmasi, faktur tersebut tidak dapat diedit atau dihapus. Jika ada kesalahan pada faktur vendor yang dikonfirmasi, Anda dapat menggunakan tindakan Batalkan untuk membalikkan dampak faktur vendor dan membuat faktur vendor baru.

Ketika Anda memilih **Batalkan** pada faktur vendor, perilaku berikut terjadi:

1. Status faktur vendor diperbarui menjadi **Dibatalkan**.
2. Faktur vendor yang dibatalkan dan catatan terkaitnya menjadi baca-saja, dan tidak dapat diedit atau dihapus.
3. Setiap aktual biaya yang dibuat berdasarkan baris faktur vendor sebagai bagian dari konfirmasi faktur vendor akan dibatalkan.
4. Jika ada aktual biaya yang ditautkan ke baris faktur vendor sebagai bagian dari proses pencocokan, konfirmasi faktur vendor asli akan membalikkannya. Selama pembatalan faktur vendor, aktual biaya tersebut dibuat ulang. Asal-usulnya menunjuk pada entri waktu, pengeluaran, atau penggunaan materi.
5. Setelah faktur vendor dibatalkan, Anda dapat sekali lagi membuat jurnal koreksi, memproses penarikan entri waktu, dan membatalkan persetujuan waktu asli, pengeluaran, atau aktual materi.

> [!NOTE]
> Hanya faktur vendor proyek yang dikonfirmasi yang dapat dibatalkan. Faktur vendor di negara bagian lain tidak dapat dibatalkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

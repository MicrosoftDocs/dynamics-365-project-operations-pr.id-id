---
title: Membatalkan faktur vendor proyek
description: Artikel ini menjelaskan cara membatalkan faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan dampak finansial dari pembatalan faktur vendor proyek.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261094"
---
# <a name="cancel-a-project-vendor-invoice"></a>Membatalkan faktur vendor proyek

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

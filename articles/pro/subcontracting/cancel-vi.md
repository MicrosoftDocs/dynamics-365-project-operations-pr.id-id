---
title: Membatalkan faktur vendor proyek
description: Artikel ini menjelaskan cara membatalkan faktur vendor proyek di Microsoft Dynamics 365 Project Operations dan dampak keuangan dari membatalkan faktur vendor proyek.
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

Setelah dikonfirmasi, faktur vendor dapat diedit atau dihapus. Jika terjadi kesalahan pada faktur vendor yang dikonfirmasi, Anda dapat menggunakan tindakan Batal untuk membalikkan dampak faktur vendor dan membuat faktur vendor baru.

Ketika Anda memilih **Batal** pada faktur vendor, perilaku berikut terjadi:

1. Status faktur vendor diperbarui ke **Dibatalkan**.
2. Faktur vendor yang dibatalkan dan rekaman terkaitnya menjadi hanya baca dan tidak dapat diedit atau dihapus.
3. Aktual biaya yang dibuat berdasarkan baris faktur vendor sebagai bagian dari konfirmasi faktur vendor akan dibalik.
4. Jika aktual biaya apa pun ditautkan ke baris faktur vendor sebagai bagian dari proses pencocokan, konfirmasi faktur vendor asli akan membatalkannya. Selama pembatalan faktur vendor, aktual biaya tersebut dibuat ulang. Asal menunjukkan entri waktu, pengeluaran, atau penggunaan bahan.
5. Setelah faktur vendor dibatalkan, Anda dapat sekali lagi membuat jurnal koreksi, memproses penarikan entri waktu, dan membatalkan persetujuan waktu, pengeluaran, atau aktual bahan asli.

> [!NOTE]
> Hanya faktur vendor proyek yang telah dikonfirmasi yang dapat dibatalkan. Faktur vendor di negara bagian lain tidak dapat dibatalkan.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

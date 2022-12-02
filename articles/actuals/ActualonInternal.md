---
title: Dampak aktual untuk proyek internal
description: Artikel ini memberikan informasi tentang dampak pada tabel Aktual pada berbagai aktivitas untuk proyek internal di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921352"
---
# <a name="actuals-impact-for-an-internal-project"></a>Dampak aktual untuk proyek internal

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Tabel berikut mencantumkan aktual dari berbagai jenis transaksi yang dibuat pada berbagai aktivitas dalam keterlibatan proyek internal.

| Kejadian | Biaya Aktual | Contoh |
|---|---|---|
| Waktu dibuat. | Tidak berlaku | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang memiliki tingkat biaya 100 dolar AS (USD 100) per jam, sedang mengerjakan proyek yang diberi nama "Penginstalan Lengan di Adatum." Proyek ini dipetakan ke metode penagihan harga tetap pada baris kontrak. Berikut adalah contoh entri waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Waktu Dikirim. | Tidak berlaku | Baris jurnal biaya dibuat untuk entri waktu. Tingkat biaya default dimasukkan dalam entri jurnal. |
| Entri waktu ditarik sebelum disetujui. | Tidak berlaku | |
| Waktu disetujui. | Biaya aktual dibuat. | <p>Aktual baru yang dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Persetujuan waktu dibatalkan. | <p>Status penyesuaian dari biaya asli aktual diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status penyesuaian **Tidak Dapat disesuaikan**.</p> | <p>Aktual yang ada dan diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalik dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam) (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Entri waktu ditarik setelah disetujui. | <p>Status penyesuaian dari biaya asli aktual diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status penyesuaian **Tidak Dapat disesuaikan**.</p> | <p>Aktual yang ada dan diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalik dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam) (USD 800), *Tidak dapat disesuaikan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

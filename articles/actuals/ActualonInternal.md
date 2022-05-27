---
title: Dampak aktual untuk proyek internal
description: Ini topik memberikan informasi tentang dampak pada tabel Aktual di berbagai acara untuk proyek internal di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579770"
---
# <a name="actuals-impact-for-an-internal-project"></a>Dampak aktual untuk proyek internal

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Tabel berikut mencantumkan aktual dari berbagai jenis transaksi yang dibuat di berbagai acara dalam keterlibatan proyek internal.

| Kejadian | Biaya Aktual | Contoh |
|---|---|---|
| Waktu diciptakan. | Tidak berlaku | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang memiliki tingkat biaya 100 dolar AS (Usd 100) per jam, sedang mengerjakan proyek yang diberi nama "Arm Installation at Adatum." Proyek ini dipetakan ke metode penagihan harga tetap pada garis kontrak. Berikut adalah contoh entri waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Waktu sudah ditentukan. | Tidak berlaku | Garis jurnal biaya dibuat untuk entri waktu. Tarif biaya default dimasukkan dalam entri jurnal. |
| Entri waktu ditarik kembali sebelum disetujui. | Tidak berlaku | |
| Waktu disetujui. | Biaya yang sebenarnya dibuat. | <p>Aktual baru yang dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Persetujuan waktu dibatalkan. | <p>Status penyesuaian aktual biaya asli diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Entri waktu ditarik kembali setelah disetujui. | <p>Status penyesuaian aktual biaya asli diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

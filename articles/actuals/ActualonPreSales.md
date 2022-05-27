---
title: Dampak aktual selama tahap pra-penjualan keterlibatan
description: Ini topik memberikan informasi tentang dampak pada tabel Aktual di berbagai acara sementara engagment sedang dalam tahap pra-penjualan di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577240"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Dampak aktual selama tahap pra-penjualan keterlibatan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Tabel berikut mencantumkan aktual dari berbagai jenis transaksi yang dibuat di berbagai acara selama tahap pra-penjualan keterlibatan proyek.

| Kejadian | Biaya Aktual | Contoh |
|---|---|---|
| Waktu diciptakan. | Tidak berlaku | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang memiliki tingkat biaya 100 dolar AS (Usd 100) per jam, sedang mengerjakan proyek yang diberi nama "Arm Installation at Adatum." Proyek ini dipetakan ke metode penagihan harga tetap pada garis kontrak. Berikut adalah contoh entri waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Waktu sudah ditentukan. | Tidak berlaku | Garis jurnal biaya dibuat untuk entri waktu. Tarif biaya default dimasukkan dalam entri jurnal. |
| Entri waktu ditarik kembali sebelum disetujui. | Tidak berlaku | |
| Waktu disetujui. | Biaya yang sebenarnya dibuat. | <p>Aktual baru yang dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Persetujuan waktu dibatalkan. | <p>Status penyesuaian aktual biaya asli diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Entri waktu ditarik kembali setelah disetujui. | <p>Status penyesuaian aktual biaya asli diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Kutipan dimenangkan, dan kontrak dibuat. | <p>Status penyesuaian aktual biaya lama diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status **penyesuaian Tidak Dapat** Disesuaikan.</p><p>Aktual biaya baru dibuat setelah aturan kontrak dievaluasi kembali.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk dampak keuangan yang dievaluasi kembali ketika kutipan dimenangkan dan kontrak dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li><li>**Penjualan yang tidak ditagih sebenarnya:** Bob Kozack, 8 jam, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

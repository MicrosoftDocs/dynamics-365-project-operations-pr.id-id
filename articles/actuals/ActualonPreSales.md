---
title: Dampak aktual selama tahap pra-penjualan keterlibatan
description: Artikel ini memberikan informasi tentang dampak pada tabel Aktual di berbagai acara saat keterlibatan berada dalam tahap pra-penjualan di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922364"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Dampak aktual selama tahap pra-penjualan keterlibatan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Tabel berikut mencantumkan aktual dari berbagai jenis transaksi yang dibuat di berbagai acara selama tahap pra-penjualan keterlibatan proyek.

| Kejadian | Biaya Aktual | Contoh |
|---|---|---|
| Waktu diciptakan. | Tidak berlaku | <p>Bob Kozack, dari unit organisasi AS Fabrikam yang memiliki tingkat biaya 100 dolar AS (USD 100) per jam, sedang mengerjakan proyek yang diberi nama "Instalasi Lengan di Adatum." Proyek ini dipetakan ke metode penagihan harga tetap pada garis kontrak. Berikut adalah contoh entri waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Waktu diserahkan. | Tidak berlaku | Baris jurnal biaya dibuat untuk entri waktu. Tingkat biaya default dimasukkan dalam entri jurnal. |
| Entri waktu ditarik kembali sebelum disetujui. | Tidak berlaku | |
| Waktu disetujui. | Biaya aktual dibuat. | <p>Aktual baru yang dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Persetujuan waktu dibatalkan. | <p>Status penyesuaian biaya asli aktual diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Entri waktu ditarik kembali setelah disetujui. | <p>Status penyesuaian biaya asli aktual diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Kutipan dimenangkan, dan kontrak dibuat. | <p>Status penyesuaian aktual biaya lama diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p><p>Aktual biaya baru dibuat setelah aturan kontrak dievaluasi kembali.</p> | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk dampak keuangan yang dievaluasi kembali ketika kutipan dimenangkan dan kontrak dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li><li>**Penjualan yang belum ditagih sebenarnya:** Bob Kozack, 8 jam, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

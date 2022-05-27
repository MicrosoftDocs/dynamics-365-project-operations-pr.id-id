---
title: Dampak aktual dalam keterlibatan harga tetap
description: Ini topik memberikan informasi tentang dampak pada tabel Aktual di berbagai peristiwa selama siklus hidup keterlibatan harga tetap di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579232"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Dampak aktual dalam keterlibatan harga tetap

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Tabel berikut mencantumkan aktual dari berbagai jenis transaksi yang dibuat di berbagai acara dalam keterlibatan harga tetap.

| Kejadian | Biaya Aktual | Aktual Penjualan Belum Tertagih | Penjualan yang ditagih aktual | Contoh |
|---|---|---|---|---|
| Waktu diciptakan. | Tidak berlaku | Tidak berlaku | Tidak berlaku | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang memiliki tingkat biaya 100 dolar AS (Usd 100) per jam, sedang mengerjakan proyek yang diberi nama "Arm Installation at Adatum." Proyek ini dipetakan ke metode penagihan harga tetap pada garis kontrak. Berikut adalah contoh entri waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Waktu sudah ditentukan. | Tidak berlaku | Tidak berlaku | Tidak berlaku | Garis jurnal biaya dibuat untuk entri waktu. Tarif biaya default dimasukkan dalam entri jurnal. |
| Entri waktu ditarik kembali sebelum disetujui. | Tidak berlaku | Tidak berlaku | Tidak berlaku | |
| Waktu disetujui. | Biaya yang sebenarnya dibuat. | Tidak berlaku | Tidak berlaku | <p>Aktual baru yang dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Persetujuan waktu dibatalkan. | <p>Status penyesuaian aktual biaya asli diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | Tidak berlaku | Tidak berlaku | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Entri waktu ditarik kembali setelah disetujui. | <p>Status penyesuaian aktual biaya asli diperbarui ke **Disesuaikan**.</p><p>Biaya pembalikan aktual dibuat yang memiliki status **penyesuaian Tidak dapat disesuaikan**.</p> | Tidak berlaku | Tidak berlaku | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Kontrak dikonfirmasi. | <p>Status penyesuaian aktual biaya lama diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status **penyesuaian Tidak Dapat** Disesuaikan.</p><p>Aktual biaya baru dibuat setelah aturan kontrak dievaluasi kembali.</p> | Tidak berlaku | Tidak berlaku | <p>Aktual yang ada yang diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalikkan dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam), (USD 800), *Tidak dapat disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk dampak keuangan yang dievaluasi kembali:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Faktur dibuat. | Tidak berlaku | Tidak berlaku | Tidak berlaku | |
| Faktur dikonfirmasi dengan tonggak sejarah. | Tidak berlaku | Tidak berlaku | Aktual penjualan ditagih berbasis tonggak baru dibuat. | <p>Aktual yang ada yang tetap tidak berubah:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul><p>Aktual baru yang dibuat untuk mencatat nilai penjualan yang ditagih:</p><ul><li>**Penjualan yang ditagih aktual:** Milestone, USD 5,000</li></ul> |
| Faktur dikoreksi untuk mengkredit tonggak sejarah. | Tidak berlaku | Tidak berlaku | Pembalikan ditagih penjualan aktual dibuat. | <p>Aktual yang ada yang tetap tidak berubah:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, 800 USD</li></ul><p>Aktual yang ada yang diperbarui:</p><ul><li>**Penjualan yang ditagih aktual:** Milestone, USD 5,000, *Adjusted*</li></ul><p>Aktual baru yang dibuat untuk membalikkan nilai penjualan yang ditagih sebelumnya:</p><ul><li>**Penjualan yang ditagih aktual:** Milestone, (USD 5.000), *Tidak dapat disesuaikan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

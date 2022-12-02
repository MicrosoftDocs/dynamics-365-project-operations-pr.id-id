---
title: Dampak aktual dalam keterlibatan harga tetap
description: Artikel ini memberikan informasi tentang dampak pada tabel Aktual pada berbagai aktivitas selama siklus hidup keterlibatan harga tetap di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918132"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Dampak aktual dalam keterlibatan harga tetap

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Tabel berikut mencantumkan aktual dari berbagai jenis transaksi yang dibuat pada berbagai aktivitas dalam keterlibatan harga tetap.

| Kejadian | Biaya Aktual | Aktual Penjualan Belum Tertagih | Aktual Penjualan Tertagih | Contoh |
|---|---|---|---|---|
| Waktu dibuat. | Tidak berlaku | Tidak berlaku | Tidak berlaku | <p>Bob Kozack, dari unit organisasi Fabrikam AS yang memiliki tingkat biaya 100 dolar AS (USD 100) per jam, sedang mengerjakan proyek yang diberi nama "Penginstalan Lengan di Adatum." Proyek ini dipetakan ke metode penagihan harga tetap pada baris kontrak. Berikut adalah contoh entri waktu dari Bob Kozak:</p><p>Bob Kozack - 8 jam</p> |
| Waktu Dikirim. | Tidak berlaku | Tidak berlaku | Tidak berlaku | Baris jurnal biaya dibuat untuk entri waktu. Tingkat biaya default dimasukkan dalam entri jurnal. |
| Entri waktu ditarik sebelum disetujui. | Tidak berlaku | Tidak berlaku | Tidak berlaku | |
| Waktu disetujui. | Biaya aktual dibuat. | Tidak berlaku | Tidak berlaku | <p>Aktual baru yang dibuat:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Persetujuan waktu dibatalkan. | <p>Status penyesuaian dari biaya asli aktual diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status penyesuaian **Tidak Dapat disesuaikan**.</p> | Tidak berlaku | Tidak berlaku | <p>Aktual yang ada dan diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalik dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam) (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Entri waktu ditarik setelah disetujui. | <p>Status penyesuaian dari biaya asli aktual diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status penyesuaian **Tidak Dapat disesuaikan**.</p> | Tidak berlaku | Tidak berlaku | <p>Aktual yang ada dan diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalik dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam) (USD 800), *Tidak dapat disesuaikan*</li></ul> |
| Kontrak dikonfirmasi. | <p>Status penyesuaian dari aktual biaya lama diperbarui ke **Disesuaikan**.</p><p>Aktual biaya pembalikan dibuat yang memiliki status penyesuaian **Tidak Dapat disesuaikan**.</p><p>Aktual biaya baru dibuat setelah aturan kontraktual dievaluasi ulang.</p> | Tidak berlaku | Tidak berlaku | <p>Aktual yang ada dan diperbarui:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalik dampak keuangan sebelumnya:</p><ul><li>**Biaya aktual:** Bob Kozack, (8 jam) (USD 800), *Tidak dapat disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk dampak keuangan yang dievaluasi ulang.</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul> |
| Faktur dibuat. | Tidak berlaku | Tidak berlaku | Tidak berlaku | |
| Faktur dikonfirmasi dengan tahapan. | Tidak berlaku | Tidak berlaku | Aktual penjualan tertagih berbasis tahapan baru dibuat. | <p>Aktual yang ada dan tetap tidak diubah:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul><p>Aktual baru yang dibuat untuk merekam nilai penjualan ditagih:</p><ul><li>**Aktual penjualan ditagih:** tahapan, USD 5.000</li></ul> |
| Faktur dikoreksi untuk mengkredit tahapan. | Tidak berlaku | Tidak berlaku | Aktual penjualan Pembalikan yang ditagih kembali dibuat. | <p>Aktual yang ada dan tetap tidak diubah:</p><ul><li>**Biaya aktual:** Bob Kozack, 8 jam, USD 800</li></ul><p>Aktual yang ada dan diperbarui:</p><ul><li>**Aktual penjualan ditagih:** tahapan, USD 5.000, *Disesuaikan*</li></ul><p>Aktual baru yang dibuat untuk membalik nilai penjualan ditagih sebelumnya:</p><ul><li>**Aktual penjualan ditagih:** tahapan, (USD 5.000),*Tidak dapat Disesuaikan*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

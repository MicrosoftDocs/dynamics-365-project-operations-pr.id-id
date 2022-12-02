---
title: Aktual
description: Artikel ini menyediakan informasi tentang cara bekerja dengan aktual di Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924802"
---
# <a name="actuals"></a>Aktual

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Aktual menunjukkan progres keuangan dan jadwal yang ditinjau dan disetujui pada proyek. Entri dibuat ketika waktu, pengeluaran, entri penggunaan bahan, serta entri jurnal dan faktur disetujui.

> [!IMPORTANT]
> Aktual tidak boleh diedit atau dihapus dari sistem. Jika tidak, integritas keuangan dan integrasi dengan sistem keuangan dan akuntansi lain mungkin akan terpengaruh. Microsoft Dynamics 365 Project Operations memungkinkan Anda menggunakan membalikkan dan mengganti aktual untuk mengedit aktual pada berbagai titik dalam siklus hidup proses bisnis proyek Anda.

## <a name="recording-actuals-based-on-project-events"></a>Aktual rekaman berdasarkan aktivitas proyek

Project Operations mencatat transaksi keuangan yang terjadi selama siklus hidup keterlibatan proyek sebagai aktual. Pembuatan aktual pada berbagai aktivitas dalam siklus hidup bervariasi, tergantung pada apakah keterlibatan proyek menggunakan model penagihan waktu dan bahan atau model penagihan harga tetap, dan baik dalam tahapan pra penjualan maupun proyek internal.

Artikel berikut menjelaskan dampak pada tabel Aktual di berbagai aktivitas untuk variasi yang berbeda:

- [Dampak aktual dalam waktu dan keterlibatan bahan](ActualsonTM.md)
- [Dampak aktual dalam keterlibatan harga tetap](ActualonFP.md)
- [Dampak aktual selama tahapan pra-penjualan suatu keterlibatan](ActualonPreSales.md)
- [Dampak aktual untuk proyek internal](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Estimasi sumber daya
description: Topik ini memberikan informasi tentang cara estimasi sumber daya dihitung dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286522"
---
# <a name="resource-estimates"></a>Estimasi sumber daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Perkiraan sumber daya berasal dari upaya bertahap waktu yang ditentukan dalam struktur rincian kerja beserta dimensi harga yang berlaku. Biasanya, penghitungan adalah **tarif/jam untuk setiap peran x jam.** Upaya bertahap waktu untuk setiap sumber daya disimpan dalam rekaman penetapan sumber daya. Harga disimpan dalam daftar harga yang telah ditentukan sebelumnya. Konversi unit diterapkan berdasarkan daftar harga yang berlaku.

![Estimasi sumber daya](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Harga biaya dan mata uang biaya default

Harga biaya di-default dari unit organisasi.

## <a name="default-bill-rate-and-sales-currency"></a>Default tarif tagihan dan mata uang penjualan

Harga penjualan diterapkan sekali per transaksi. Hierarki untuk daftar harga penjualan yang di-default sebagai berikut:

1. Organisasi
2. Pelanggan
3. Kuotasi/Kontrak


[!INCLUDE[footer-include](../includes/footer-banner.md)]
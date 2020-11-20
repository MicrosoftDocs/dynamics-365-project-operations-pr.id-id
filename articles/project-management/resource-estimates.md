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
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127368"
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

---
title: Estimasi sumber daya
description: Topik ini memberikan informasi tentang cara estimasi sumber daya dihitung dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928576"
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

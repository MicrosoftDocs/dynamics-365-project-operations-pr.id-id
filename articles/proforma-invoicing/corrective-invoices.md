---
title: Faktur yang dikoreksi
description: Topik ini menyediakan informasi tentang faktur yang dikoreksi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122392"
---
# <a name="corrected-invoices"></a>Faktur yang dikoreksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Faktur yang Dikonfirmasi dapat diedit. Setelah Anda mengedit faktur yang telah dikonfirmasi, draf faktur yang dikoreksi akan dibuat. Karena asumsi adalah bahwa Anda ingin membalikkan semua transaksi dan kuantitas dari faktur asli, faktur yang dikoreksi ini mencakup semua transaksi dari faktur asli, dan semua kuantitas di atasnya adalah 0 (nol).

Ketika transaksi tidak memerlukan koreksi, Anda dapat menghapusnya dari draf faktur perbaikan. Untuk membalikkan atau mengembalikan hanya kuantitas parsial, Anda dapat mengedit bidang kuantitas pada detail baris. Jika Anda membuka detail baris faktur, Anda dapat melihat jumlah faktur asli. Selanjutnya, Anda dapat mengedit kuantitas faktur saat ini sehingga lebih kecil atau lebih besar dari kuantitas faktur asli.

Setelah Anda mengonfirmasikan faktur koreksi, aktual penjualan yang belum ditagih asli dibalik, dan aktual penjualan baru yang ditagih dibuat. Jika kuantitas dikurangi, perbedaannya akan menyebabkan penjualan baru yang belum ditagih juga dibuat. Misalnya, jika penjualan tagihan asli selama delapan jam, dan detail baris faktur perbaikan memiliki kuantitas kurang dari enam jam, baris penjualan asli yang ditagih dibalikkan dan dua aktual baru dibuat:

- Penjualan yang ditagih untuk enam jam.
- Tagihan penjualan yang belum ditagih untuk dua jam yang tersisa. Transaksi ini dapat ditagih nanti atau ditandai sebagai tidak dikenakan biaya, tergantung pada negosiasi dengan pelanggan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
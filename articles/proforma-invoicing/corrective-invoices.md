---
title: Faktur yang dikoreksi
description: Topik ini menyediakan informasi tentang faktur yang dikoreksi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898085"
---
# <a name="corrected-invoices"></a>Faktur yang dikoreksi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Faktur yang Dikonfirmasi dapat diedit. Setelah Anda mengedit faktur yang telah dikonfirmasi, draf faktur yang dikoreksi akan dibuat. Karena asumsi adalah bahwa Anda ingin membalikkan semua transaksi dan kuantitas dari faktur asli, faktur yang dikoreksi ini mencakup semua transaksi dari faktur asli, dan semua kuantitas di atasnya adalah 0 (nol).

Ketika transaksi tidak memerlukan koreksi, Anda dapat menghapusnya dari draf faktur perbaikan. Untuk membalikkan atau mengembalikan hanya kuantitas parsial, Anda dapat mengedit bidang kuantitas pada detail baris. Jika Anda membuka detail baris faktur, Anda dapat melihat jumlah faktur asli. Selanjutnya, Anda dapat mengedit kuantitas faktur saat ini sehingga lebih kecil atau lebih besar dari kuantitas faktur asli.

Setelah Anda mengonfirmasikan faktur koreksi, aktual penjualan yang belum ditagih asli dibalik, dan aktual penjualan baru yang ditagih dibuat. Jika kuantitas dikurangi, perbedaannya akan menyebabkan penjualan baru yang belum ditagih juga dibuat. Misalnya, jika penjualan tagihan asli selama delapan jam, dan detail baris faktur perbaikan memiliki kuantitas kurang dari enam jam, baris penjualan asli yang ditagih dibalikkan dan dua aktual baru dibuat:

- Penjualan yang ditagih untuk enam jam.
- Tagihan penjualan yang belum ditagih untuk dua jam yang tersisa. Transaksi ini dapat ditagih nanti atau ditandai sebagai tidak dikenakan biaya, tergantung pada negosiasi dengan pelanggan.

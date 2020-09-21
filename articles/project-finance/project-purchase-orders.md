---
title: Pesanan pembelian untuk proyek
description: Artikel ini menjelaskan berbagai metode yang dapat Anda gunakan untuk membuat pesanan pembelian untuk proyek. Metode yang Anda gunakan bergantung pada tujuan pesanan pembelian, dan ketika item yang dibeli dikonsumsi dan ditagih pada proyek.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752423"
---
# <a name="purchase-orders-for-a-project"></a>Pesanan pembelian untuk proyek

[!include [banner](../includes/banner.md)]

Artikel ini menjelaskan berbagai metode yang dapat Anda gunakan untuk membuat pesanan pembelian untuk proyek. Metode yang Anda gunakan bergantung pada tujuan pesanan pembelian, dan ketika item yang dibeli dikonsumsi dan ditagih pada proyek.

### <a name="methods-for-creating-a-purchase-order"></a>Metode pembuatan pesanan pembelian

Anda dapat menggunakan salah satu dari metode berikut untuk membuat pesanan pembelian dalam manajemen proyek dan akuntansi. Tujuan pesanan pembelian menentukan kapan pesanan pembelian dikonsumsi dan, oleh karena itu, kapan item dibebankan pada proyek.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Metode</th>
<th>Tujuan</th>
<th>Konsumsi item</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Buat Pesanan Pembelian secara langsung dari proyek.</td>
<td>Gunakan metode ini untuk membeli item dari vendor eksternal untuk konsumsi pada proyek. Anda dapat membuat pesanan pembelian dengan dua cara:
<ul>
<li>Dari proyek itu sendiri. Dalam kasus ini, proyek sudah ditentukan untuk pesanan pembelian.</li>
<li>Dengan menavigasi pesanan pembelian proyek. Anda harus memilih vendor dan proyek untuk membuat pesanan pembelian.</li>
</ul></td>
<td>Item yang dikonsumsi saat faktur vendor diperbarui.</td>
</tr>
<tr class="even">
<td>Buat Pesanan Pembelian dari pesanan Penjualan.</td>
<td>Gunakan metode ini untuk membeli item saat membuat pesanan penjualan dari proyek.</td>
<td>Item yang dikonsumsi ketika pesanan penjualan ditagih ke pelanggan.</td>
</tr>
<tr class="odd">
<td>Buat pesanan pembelian dari persyaratan item.</td>
<td>Gunakan metode ini untuk membeli item saat membuat persyaratan item dari proyek.</td>
<td>Item dikonsumsi saat slip kemasan persyaratan item diperbarui.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Ketika Anda memperbarui faktur vendor atau slip Kemasan, Anda akan diminta untuk memperbarui slip Kemasan pada persyaratan item.

Untuk informasi lebih lanjut, lihat [menerima item pesanan pembelian dari persyaratan item](tasks/receive-items-purchase-order-item-requirement.md).


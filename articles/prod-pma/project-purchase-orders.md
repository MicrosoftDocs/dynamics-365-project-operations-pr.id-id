---
title: Pesanan pembelian untuk proyek
description: Artikel ini menjelaskan berbagai metode yang dapat Anda gunakan untuk membuat pesanan pembelian untuk proyek. Metode yang Anda gunakan bergantung pada tujuan pesanan pembelian, dan ketika item yang dibeli dikonsumsi dan ditagih pada proyek.
author: Yowelle
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3c3ce2d0c0fb3cecf22157db5cb37eb744027d0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999360"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="5be47-104">Pesanan pembelian untuk proyek</span><span class="sxs-lookup"><span data-stu-id="5be47-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5be47-105">Artikel ini menjelaskan berbagai metode yang dapat Anda gunakan untuk membuat pesanan pembelian untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="5be47-106">Metode yang Anda gunakan bergantung pada tujuan pesanan pembelian, dan ketika item yang dibeli dikonsumsi dan ditagih pada proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="5be47-107">Metode pembuatan pesanan pembelian</span><span class="sxs-lookup"><span data-stu-id="5be47-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="5be47-108">Anda dapat menggunakan salah satu dari metode berikut untuk membuat pesanan pembelian dalam manajemen proyek dan akuntansi.</span><span class="sxs-lookup"><span data-stu-id="5be47-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="5be47-109">Tujuan pesanan pembelian menentukan kapan pesanan pembelian dikonsumsi dan, oleh karena itu, kapan item dibebankan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5be47-110">Metode</span><span class="sxs-lookup"><span data-stu-id="5be47-110">Method</span></span></th>
<th><span data-ttu-id="5be47-111">Tujuan</span><span class="sxs-lookup"><span data-stu-id="5be47-111">Purpose</span></span></th>
<th><span data-ttu-id="5be47-112">Konsumsi item</span><span class="sxs-lookup"><span data-stu-id="5be47-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5be47-113">Buat Pesanan Pembelian secara langsung dari proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="5be47-114">Gunakan metode ini untuk membeli item dari vendor eksternal untuk konsumsi pada proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="5be47-115">Anda dapat membuat pesanan pembelian dengan dua cara:</span><span class="sxs-lookup"><span data-stu-id="5be47-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="5be47-116">Dari proyek itu sendiri.</span><span class="sxs-lookup"><span data-stu-id="5be47-116">From the project itself.</span></span> <span data-ttu-id="5be47-117">Dalam kasus ini, proyek sudah ditentukan untuk pesanan pembelian.</span><span class="sxs-lookup"><span data-stu-id="5be47-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="5be47-118">Dengan menavigasi pesanan pembelian proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="5be47-119">Anda harus memilih vendor dan proyek untuk membuat pesanan pembelian.</span><span class="sxs-lookup"><span data-stu-id="5be47-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="5be47-120">Item yang dikonsumsi saat faktur vendor diperbarui.</span><span class="sxs-lookup"><span data-stu-id="5be47-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5be47-121">Buat Pesanan Pembelian dari pesanan Penjualan.</span><span class="sxs-lookup"><span data-stu-id="5be47-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="5be47-122">Gunakan metode ini untuk membeli item saat membuat pesanan penjualan dari proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="5be47-123">Item yang dikonsumsi ketika pesanan penjualan ditagih ke pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5be47-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5be47-124">Buat pesanan pembelian dari persyaratan item.</span><span class="sxs-lookup"><span data-stu-id="5be47-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="5be47-125">Gunakan metode ini untuk membeli item saat membuat persyaratan item dari proyek.</span><span class="sxs-lookup"><span data-stu-id="5be47-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="5be47-126">Item dikonsumsi saat slip kemasan persyaratan item diperbarui.</span><span class="sxs-lookup"><span data-stu-id="5be47-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="5be47-127">Ketika Anda memperbarui faktur vendor atau slip Kemasan, Anda akan diminta untuk memperbarui slip Kemasan pada persyaratan item.</span><span class="sxs-lookup"><span data-stu-id="5be47-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="5be47-128">Untuk informasi lebih lanjut, lihat [menerima item pesanan pembelian dari persyaratan item](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="5be47-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
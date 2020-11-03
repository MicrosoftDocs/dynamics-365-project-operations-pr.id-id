---
title: Menerima item pesanan pembelian dari persyaratan item
description: Topik ini menjelaskan cara menerima item pada pesanan pembelian dari persyaratan item.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078651"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="f9abc-103">Menerima item pesanan pembelian dari persyaratan item</span><span class="sxs-lookup"><span data-stu-id="f9abc-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f9abc-104">Topik ini menjelaskan cara menerima item pada pesanan pembelian dari persyaratan item.</span><span class="sxs-lookup"><span data-stu-id="f9abc-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="f9abc-105">Dengan menggunakan persyaratan item dan bukan transaksi item, Anda dapat merencanakan pengiriman tepat sebelum item benar-benar digunakan, membuat pesanan pembelian, menyertakan item dalam kerangka perjanjian perdagangan, dan menyertakan persyaratan item dalam perencanaan produksi.</span><span class="sxs-lookup"><span data-stu-id="f9abc-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="f9abc-106">Tugas ini menggunakan himpunan data USSI.</span><span class="sxs-lookup"><span data-stu-id="f9abc-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f9abc-107">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > Proyek > Semua proyek**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="f9abc-108">Dalam daftar, pilih tautan di baris yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="f9abc-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="f9abc-109">Pada panel tindakan, pilih **Rencana**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="f9abc-110">Pilih **persyaratan item**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="f9abc-111">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-111">Select **New**.</span></span>
6. <span data-ttu-id="f9abc-112">Di baris baru, masukkan atau pilih nilai pada bidang **nomor item**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="f9abc-113">Di bidang **Kuantitas** , masukkan angka.</span><span class="sxs-lookup"><span data-stu-id="f9abc-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="f9abc-114">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-114">Select **Save**.</span></span>
9. <span data-ttu-id="f9abc-115">Pada panel tindakan, pilih **Kelola**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="f9abc-116">Pilih **Fungsi**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-116">Select **Functions**.</span></span>
11. <span data-ttu-id="f9abc-117">Pilih **Buat Pesanan Pembelian**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="f9abc-118">Pilih kotak centang **sertakan semua**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="f9abc-119">Di bidang **Akun vendor** , masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="f9abc-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="f9abc-120">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-120">Select **OK**.</span></span>
15. <span data-ttu-id="f9abc-121">Di panel navigasi, buka **modul > piutang > Pesanan pembelian > Semua pesanan pembelian**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="f9abc-122">Dalam daftar, pilih tautan di baris yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="f9abc-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="f9abc-123">Pada panel tindakan, pilih **Pembelian**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="f9abc-124">Pilih **Konfirmasi**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="f9abc-125">Pada panel tindakan, pilih **Tanda terima**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="f9abc-126">Pilih **Resi produk**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="f9abc-127">Di bidang **Resi produk** , masukkan nilai.</span><span class="sxs-lookup"><span data-stu-id="f9abc-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="f9abc-128">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="f9abc-128">Select **OK**.</span></span>


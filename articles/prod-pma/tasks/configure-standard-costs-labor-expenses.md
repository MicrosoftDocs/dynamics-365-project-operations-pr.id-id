---
title: Konfigurasikan biaya standar untuk tenaga kerja dan pengeluaran
description: Topik ini menjelaskan cara menyiapkan biaya standar untuk tenaga kerja dan pengeluaran untuk proyek.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288338"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="ab19e-103">Konfigurasikan biaya standar untuk tenaga kerja dan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="ab19e-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ab19e-104">Topik ini menjelaskan cara menyiapkan biaya standar untuk tenaga kerja dan pengeluaran untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="ab19e-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="ab19e-105">Tugas ini menggunakan himpunan data USSI.</span><span class="sxs-lookup"><span data-stu-id="ab19e-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="ab19e-106">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Harga > Harga biaya (jam)**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="ab19e-107">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-107">Select **New**.</span></span>
3. <span data-ttu-id="ab19e-108">Di bidang **Tanggal efektif**, masukkan tanggal.</span><span class="sxs-lookup"><span data-stu-id="ab19e-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="ab19e-109">Di bidang **harga biaya**, masukkan angka.</span><span class="sxs-lookup"><span data-stu-id="ab19e-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="ab19e-110">Anda dapat mengkonfigurasi harga standar untuk kategori proyek, atau Anda dapat mengkonfigurasi harga dengan jumlah pekerja, nomor proyek, kategori, tanggal, atau kombinasi ini.</span><span class="sxs-lookup"><span data-stu-id="ab19e-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="ab19e-111">Harga biaya yang diterapkan adalah harga dengan tingkat detail tertinggi.</span><span class="sxs-lookup"><span data-stu-id="ab19e-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="ab19e-112">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-112">Select **Save**.</span></span>
6. <span data-ttu-id="ab19e-113">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Harga > Harga Penjualan (jam)**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="ab19e-114">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-114">Select **New**.</span></span>
8. <span data-ttu-id="ab19e-115">Di bidang **Tanggal efektif**, masukkan tanggal.</span><span class="sxs-lookup"><span data-stu-id="ab19e-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="ab19e-116">Pilih pilihan di bidang **Valid hingga**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="ab19e-117">Di bidang **harga**, masukkan angka.</span><span class="sxs-lookup"><span data-stu-id="ab19e-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="ab19e-118">Anda dapat mengkonfigurasi harga penjualan standar untuk transaksi jam atau untuk kategori proyek.</span><span class="sxs-lookup"><span data-stu-id="ab19e-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="ab19e-119">Anda juga dapat menyiapkan harga penjualan berdasarkan jumlah pekerja, nomor proyek, kategori, tanggal transaksi, atau kombinasi ini.</span><span class="sxs-lookup"><span data-stu-id="ab19e-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="ab19e-120">Harga penjualan aktual, yang diterapkan saat pekerja memasukkan transaksi dalam jurnal jam, adalah harga penjualan dengan tingkat detail tertinggi.</span><span class="sxs-lookup"><span data-stu-id="ab19e-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="ab19e-121">Misalnya, jika harga penjualan Umum dan harga penjualan khusus pekerja ditetapkan, harga penjualan khusus pekerja digunakan.</span><span class="sxs-lookup"><span data-stu-id="ab19e-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="ab19e-122">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-122">Select **Save**.</span></span>
12. <span data-ttu-id="ab19e-123">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="ab19e-123">Close the page.</span></span>
13. <span data-ttu-id="ab19e-124">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Harga > Harga biaya (pengeluaran)**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="ab19e-125">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-125">Select **New**.</span></span>
15. <span data-ttu-id="ab19e-126">Di bidang **Tanggal efektif**, masukkan tanggal.</span><span class="sxs-lookup"><span data-stu-id="ab19e-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="ab19e-127">Di bidang **harga biaya**, masukkan angka.</span><span class="sxs-lookup"><span data-stu-id="ab19e-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="ab19e-128">Beberapa bidang dapat diisi, namun ini adalah minimum yang diperlukan untuk menyimpan rekaman.</span><span class="sxs-lookup"><span data-stu-id="ab19e-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="ab19e-129">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-129">Select **Save**.</span></span>
18. <span data-ttu-id="ab19e-130">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Harga > Harga Penjualan (pengeluaran)**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="ab19e-131">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-131">Select **New**.</span></span>
20. <span data-ttu-id="ab19e-132">Di bidang **Tanggal efektif**, masukkan tanggal.</span><span class="sxs-lookup"><span data-stu-id="ab19e-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="ab19e-133">Pilih pilihan di bidang **Valid hingga**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="ab19e-134">Di bidang **harga**, masukkan angka.</span><span class="sxs-lookup"><span data-stu-id="ab19e-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="ab19e-135">Harga penjualan aktual, yang diterapkan saat pekerja memasukkan transaksi dalam jurnal pengeluaran, adalah harga penjualan dengan tingkat detail tertinggi.</span><span class="sxs-lookup"><span data-stu-id="ab19e-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="ab19e-136">Misalnya, jika harga penjualan Umum dan khusus pekerja ditetapkan, harga penjualan khusus pekerja digunakan.</span><span class="sxs-lookup"><span data-stu-id="ab19e-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="ab19e-137">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="ab19e-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
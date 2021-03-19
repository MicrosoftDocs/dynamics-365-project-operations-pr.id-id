---
title: Mengonfigurasi kategori pengeluaran
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi kategori pengeluaran dan kategori bersama untuk laporan pengeluaran.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 1589cf82626e744d35f31fef8e8437a5ad71360d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276127"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="60f60-103">Mengonfigurasi kategori pengeluaran</span><span class="sxs-lookup"><span data-stu-id="60f60-103">Set up expense categories</span></span>

<span data-ttu-id="60f60-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="60f60-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="60f60-105">Bila karyawan membuat laporan pengeluaran, setiap biaya yang direkam harus dikaitkan dengan kategori pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="60f60-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="60f60-106">Kategori pengeluaran berasal dari kategori bersama yang dapat dibagikan di seluruh entitas hukum di organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="60f60-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="60f60-107">Tergantung pada bagaimana organisasi Anda didefinisikan, kategori pengeluaran ini juga dapat dibagikan di area lain.</span><span class="sxs-lookup"><span data-stu-id="60f60-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="60f60-108">Berdasarkan definisi organisasi dan panduan dari tim penerapan, Anda harus menentukan apakah kategori yang digunakan dalam manajemen pengeluaran hanya akan digunakan di manajemen pengeluaran atau harus dibagikan di area lain.</span><span class="sxs-lookup"><span data-stu-id="60f60-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="60f60-109">Kategori ini dapat dibagi antara manajemen proyek dan manajemen akuntansi dan pengeluaran, atau antara manajemen proyek dan akuntansi dan produksi.</span><span class="sxs-lookup"><span data-stu-id="60f60-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="60f60-110">Namun, mereka tidak dapat dibagi antara manajemen pengeluaran dan produksi.</span><span class="sxs-lookup"><span data-stu-id="60f60-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="60f60-111">Sebelum Anda dapat memulai proses konfigurasi, keputusan berikut harus dibuat untuk setiap kategori pengeluaran:</span><span class="sxs-lookup"><span data-stu-id="60f60-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="60f60-112">Apa itu kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="60f60-112">What is the expense category?</span></span> <span data-ttu-id="60f60-113">Contohnya mencakup kategori untuk penerbangan, Hotel, atau jarak tempuh.</span><span class="sxs-lookup"><span data-stu-id="60f60-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="60f60-114">Dapatkah kategori pengeluaran juga dapat digunakan dalam manajemen proyek dan akuntansi?</span><span class="sxs-lookup"><span data-stu-id="60f60-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="60f60-115">Jika bisa, Anda juga harus membuat keputusan berikut:</span><span class="sxs-lookup"><span data-stu-id="60f60-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="60f60-116">Biaya akun apa yang akan digunakan untuk biaya berikut?</span><span class="sxs-lookup"><span data-stu-id="60f60-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="60f60-117">Biaya</span><span class="sxs-lookup"><span data-stu-id="60f60-117">Cost</span></span>
        - <span data-ttu-id="60f60-118">Alokasi penggajian</span><span class="sxs-lookup"><span data-stu-id="60f60-118">Payroll allocation</span></span>
        - <span data-ttu-id="60f60-119">WIP-Nilai biaya</span><span class="sxs-lookup"><span data-stu-id="60f60-119">WIP-cost value</span></span>
        - <span data-ttu-id="60f60-120">Item biaya</span><span class="sxs-lookup"><span data-stu-id="60f60-120">Cost-item</span></span>
        - <span data-ttu-id="60f60-121">Item-Nilai biaya-WIP</span><span class="sxs-lookup"><span data-stu-id="60f60-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="60f60-122">Rugi akrual</span><span class="sxs-lookup"><span data-stu-id="60f60-122">Accrued loss</span></span>
        - <span data-ttu-id="60f60-123">Rugi akrual-WIP</span><span class="sxs-lookup"><span data-stu-id="60f60-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="60f60-124">Akun pendapatan apa yang akan digunakan untuk sumber pendapatan berikut?</span><span class="sxs-lookup"><span data-stu-id="60f60-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="60f60-125">Pendapatan yang ditagih</span><span class="sxs-lookup"><span data-stu-id="60f60-125">Invoiced revenue</span></span>
        - <span data-ttu-id="60f60-126">pendapatan akrual – nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="60f60-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="60f60-127">WIP-nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="60f60-127">WIP-sales value</span></span>
        - <span data-ttu-id="60f60-128">Pendapatan akrual-produksi</span><span class="sxs-lookup"><span data-stu-id="60f60-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="60f60-129">WIP-Produksi</span><span class="sxs-lookup"><span data-stu-id="60f60-129">WIP-production</span></span>
        - <span data-ttu-id="60f60-130">Pendapatan akrual-laba</span><span class="sxs-lookup"><span data-stu-id="60f60-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="60f60-131">WIP-Laba</span><span class="sxs-lookup"><span data-stu-id="60f60-131">WIP-profit</span></span>
        - <span data-ttu-id="60f60-132">Pendapatan akrual-langganan</span><span class="sxs-lookup"><span data-stu-id="60f60-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="60f60-133">WIP-Langganan</span><span class="sxs-lookup"><span data-stu-id="60f60-133">WIP-subscription</span></span>

- <span data-ttu-id="60f60-134">Apa itu jenis pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="60f60-134">What is the expense type?</span></span>
- <span data-ttu-id="60f60-135">Apa yang dimaksud dengan metode pembayaran default untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="60f60-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="60f60-136">Apakah pengeluaran dalam kategori pengeluaran harus diitemkan?</span><span class="sxs-lookup"><span data-stu-id="60f60-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="60f60-137">Apa yang dimaksud akun default utama untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="60f60-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="60f60-138">Apa yang dimaksud dengan grup pajak penjualan item default untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="60f60-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="60f60-139">Apakah metode pembayaran tambahan diizinkan untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="60f60-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="60f60-140">Jika demikian, apa saja?</span><span class="sxs-lookup"><span data-stu-id="60f60-140">If so, what are they?</span></span>
- <span data-ttu-id="60f60-141">Apakah ada subkategori dalam kategori pengeluaran ini?</span><span class="sxs-lookup"><span data-stu-id="60f60-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="60f60-142">Jika ada subkategori, Anda juga harus membuat keputusan berikut:</span><span class="sxs-lookup"><span data-stu-id="60f60-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="60f60-143">Apakah ada subkategori yang dikecualikan dari pemulihan pajak?</span><span class="sxs-lookup"><span data-stu-id="60f60-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="60f60-144">Apa yang dimaksud dengan grup pajak penjualan item dari subkategori?</span><span class="sxs-lookup"><span data-stu-id="60f60-144">What is the item sales tax group of the subcategories?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
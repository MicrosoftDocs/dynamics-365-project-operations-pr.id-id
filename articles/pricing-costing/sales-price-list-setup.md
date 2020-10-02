---
title: Mengatur daftar harga penjualan
description: Topik ini menyediakan informasi topik tentang daftar harga penjualan untuk penentuan harga proyek.
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896465"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="d913e-103">Mengatur daftar harga penjualan</span><span class="sxs-lookup"><span data-stu-id="d913e-103">Sales price list setup</span></span>

<span data-ttu-id="d913e-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="d913e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d913e-105">Untuk kuotasi dan kontrak proyek, daftar harga proyek memiliki pola penggantian harga yang berbeda dari daftar harga produk.</span><span class="sxs-lookup"><span data-stu-id="d913e-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="d913e-106">Pada baris kuotasi Katalog Produk, Anda dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi, karena setiap baris kuotasi mengarah ke satu item Katalog.</span><span class="sxs-lookup"><span data-stu-id="d913e-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="d913e-107">Namun, pada baris kuotasi berbasis proyek, Anda tidak dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d913e-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="d913e-108">Anda dapat menggunakan daftar harga proyek untuk bekerja dengan dua pola timpa yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="d913e-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="d913e-109">Sebaiknya Anda memiliki daftar harga terpisah untuk sumber daya proyek dan item Katalog Anda, karena perbedaan perilaku antara keduanya saat Anda mengganti harga.</span><span class="sxs-lookup"><span data-stu-id="d913e-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="d913e-110">Setiap entitas berikut dapat memiliki satu atau beberapa daftar harga penjualan terkait untuk harga proyek:</span><span class="sxs-lookup"><span data-stu-id="d913e-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="d913e-111">Pelanggan (Akun)</span><span class="sxs-lookup"><span data-stu-id="d913e-111">Customer (account)</span></span> 
- <span data-ttu-id="d913e-112">Peluang</span><span class="sxs-lookup"><span data-stu-id="d913e-112">Opportunity</span></span> 
- <span data-ttu-id="d913e-113">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="d913e-113">Quote</span></span> 
- <span data-ttu-id="d913e-114">Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="d913e-114">Project Contract</span></span>

<span data-ttu-id="d913e-115">Asosiasi entitas ini dengan daftar harga ditunjukkan oleh daftar harga proyek.</span><span class="sxs-lookup"><span data-stu-id="d913e-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="d913e-116">Anda dapat mengaitkan satu atau beberapa daftar harga dengan entitas pelanggan, peluang, kuotasi, dan entitas penjualan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="d913e-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="d913e-117">Daftar harga proyek default tidak secara otomatis dimasukkan ke rekaman pelanggan.</span><span class="sxs-lookup"><span data-stu-id="d913e-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="d913e-118">Namun, Anda dapat melampirkan daftar harga proyek secara manual ke rekaman pelanggan.</span><span class="sxs-lookup"><span data-stu-id="d913e-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="d913e-119">Namun demikian, Anda harus melampirkan daftar harga proyek secara manual hanya bila Anda memiliki perjanjian harga kustom dengan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="d913e-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="d913e-120">Bila daftar harga proyek dilampirkan ke entitas penjualan, informasi berikut divalidasi:</span><span class="sxs-lookup"><span data-stu-id="d913e-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="d913e-121">Daftar harga memiliki konteks **penjualan**.</span><span class="sxs-lookup"><span data-stu-id="d913e-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="d913e-122">Mata uang daftar harga cocok dengan mata uang pelanggan.</span><span class="sxs-lookup"><span data-stu-id="d913e-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="d913e-123">Pada kontrak proyek, urutan prioritas berikut digunakan untuk secara otomatis mengatur daftar harga proyek yang terkait:</span><span class="sxs-lookup"><span data-stu-id="d913e-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="d913e-124">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="d913e-124">Quote</span></span>
2. <span data-ttu-id="d913e-125">Peluang</span><span class="sxs-lookup"><span data-stu-id="d913e-125">Opportunity</span></span>
3. <span data-ttu-id="d913e-126">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="d913e-126">Customer</span></span> 
4. <span data-ttu-id="d913e-127">Pengaturan global</span><span class="sxs-lookup"><span data-stu-id="d913e-127">Global settings</span></span> 

<span data-ttu-id="d913e-128">Bila daftar harga proyek dimasukkan secara default, sistem memvalidasi bahwa mata uang cocok dengan mata uang pelanggan, dan bahwa daftar harga default yang telah dimasukkan memiliki konteks **penjualan**.</span><span class="sxs-lookup"><span data-stu-id="d913e-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="d913e-129">Anda dapat mengaitkan beberapa daftar harga proyek dengan entitas pelanggan, peluang, kuotasi, dan entitas kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="d913e-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="d913e-130">Kemampuan ini mendukung harga default spesifik tanggal untuk kontrak proyek berjalan lama, di mana Anda memerlukan lebih dari satu daftar harga untuk menjelaskan pembaruan harga yang terjadi karena inflasi.</span><span class="sxs-lookup"><span data-stu-id="d913e-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="d913e-131">Namun, jika daftar harga yang Anda kaitkan dengan pelanggan, peluang, kuotasi, atau entitas kontrak proyek memiliki efektivitas tanggal tumpang tindih, harga default mungkin salah.</span><span class="sxs-lookup"><span data-stu-id="d913e-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="d913e-132">Oleh karena itu, Anda harus memastikan bahwa daftar harga proyek yang memiliki efektivitas tanggal tumpang tindih tidak terkait dengan entitas tersebut.</span><span class="sxs-lookup"><span data-stu-id="d913e-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>

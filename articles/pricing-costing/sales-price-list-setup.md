---
title: Mengatur daftar harga penjualan
description: Topik ini menyediakan informasi topik tentang daftar harga penjualan untuk penentuan harga proyek.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004895"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="bed36-103">Mengatur daftar harga penjualan</span><span class="sxs-lookup"><span data-stu-id="bed36-103">Set up a sales price list</span></span>

<span data-ttu-id="bed36-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="bed36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bed36-105">Untuk kuotasi dan kontrak proyek, daftar harga proyek memiliki pola penggantian harga yang berbeda dari daftar harga produk.</span><span class="sxs-lookup"><span data-stu-id="bed36-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="bed36-106">Pada baris kuotasi Katalog Produk, Anda dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi, karena setiap baris kuotasi mengarah ke satu item Katalog.</span><span class="sxs-lookup"><span data-stu-id="bed36-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="bed36-107">Namun, pada baris kuotasi berbasis proyek, Anda tidak dapat menimpa harga ke peran dan kategori secara langsung pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bed36-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="bed36-108">Anda dapat menggunakan daftar harga proyek untuk bekerja dengan dua pola timpa yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="bed36-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="bed36-109">Sebaiknya Anda memiliki daftar harga terpisah untuk sumber daya proyek dan item Katalog Anda, karena perbedaan perilaku antara keduanya saat Anda mengganti harga.</span><span class="sxs-lookup"><span data-stu-id="bed36-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="bed36-110">Setiap entitas berikut dapat memiliki satu atau beberapa daftar harga penjualan terkait untuk harga proyek:</span><span class="sxs-lookup"><span data-stu-id="bed36-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="bed36-111">Pelanggan (Akun)</span><span class="sxs-lookup"><span data-stu-id="bed36-111">Customer (account)</span></span> 
- <span data-ttu-id="bed36-112">Peluang</span><span class="sxs-lookup"><span data-stu-id="bed36-112">Opportunity</span></span> 
- <span data-ttu-id="bed36-113">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="bed36-113">Quote</span></span> 
- <span data-ttu-id="bed36-114">Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="bed36-114">Project Contract</span></span>

<span data-ttu-id="bed36-115">Asosiasi entitas ini dengan daftar harga ditunjukkan oleh daftar harga proyek.</span><span class="sxs-lookup"><span data-stu-id="bed36-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="bed36-116">Anda dapat mengaitkan satu atau beberapa daftar harga dengan entitas pelanggan, peluang, kuotasi, dan entitas penjualan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="bed36-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="bed36-117">Daftar harga proyek default tidak secara otomatis dimasukkan ke rekaman pelanggan.</span><span class="sxs-lookup"><span data-stu-id="bed36-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="bed36-118">Namun, Anda dapat melampirkan daftar harga proyek secara manual ke rekaman pelanggan.</span><span class="sxs-lookup"><span data-stu-id="bed36-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="bed36-119">Namun demikian, Anda harus melampirkan daftar harga proyek secara manual hanya bila Anda memiliki perjanjian harga kustom dengan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="bed36-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="bed36-120">Bila daftar harga proyek dilampirkan ke entitas penjualan, informasi berikut divalidasi:</span><span class="sxs-lookup"><span data-stu-id="bed36-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="bed36-121">Daftar harga memiliki konteks **penjualan**.</span><span class="sxs-lookup"><span data-stu-id="bed36-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="bed36-122">Mata uang daftar harga cocok dengan mata uang pelanggan.</span><span class="sxs-lookup"><span data-stu-id="bed36-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="bed36-123">Pada kontrak proyek, urutan prioritas berikut digunakan untuk secara otomatis mengatur daftar harga proyek yang terkait:</span><span class="sxs-lookup"><span data-stu-id="bed36-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="bed36-124">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="bed36-124">Quote</span></span>
2. <span data-ttu-id="bed36-125">Peluang</span><span class="sxs-lookup"><span data-stu-id="bed36-125">Opportunity</span></span>
3. <span data-ttu-id="bed36-126">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="bed36-126">Customer</span></span> 
4. <span data-ttu-id="bed36-127">Pengaturan global</span><span class="sxs-lookup"><span data-stu-id="bed36-127">Global settings</span></span> 

<span data-ttu-id="bed36-128">Bila daftar harga proyek dimasukkan secara default, sistem memvalidasi bahwa mata uang cocok dengan mata uang pelanggan, dan bahwa daftar harga default yang telah dimasukkan memiliki konteks **penjualan**.</span><span class="sxs-lookup"><span data-stu-id="bed36-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="bed36-129">Anda dapat mengaitkan beberapa daftar harga proyek dengan entitas pelanggan, peluang, kuotasi, dan entitas kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="bed36-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="bed36-130">Kemampuan ini mendukung harga default spesifik tanggal untuk kontrak proyek berjalan lama, di mana Anda memerlukan lebih dari satu daftar harga untuk menjelaskan pembaruan harga yang terjadi karena inflasi.</span><span class="sxs-lookup"><span data-stu-id="bed36-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="bed36-131">Namun, jika daftar harga yang Anda kaitkan dengan pelanggan, peluang, kuotasi, atau entitas kontrak proyek memiliki efektivitas tanggal tumpang tindih, harga default mungkin salah.</span><span class="sxs-lookup"><span data-stu-id="bed36-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="bed36-132">Oleh karena itu, Anda harus memastikan bahwa daftar harga proyek yang memiliki efektivitas tanggal tumpang tindih tidak terkait dengan entitas tersebut.</span><span class="sxs-lookup"><span data-stu-id="bed36-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
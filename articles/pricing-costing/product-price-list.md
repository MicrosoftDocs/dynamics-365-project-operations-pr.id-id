---
title: Daftar harga produk
description: Topik ini menyediakan informasi tentang daftar harga dalam harga katalog yang digunakan untuk kuotasi dan kontrak proyek.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
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
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877494"
---
# <a name="product-price-lists"></a><span data-ttu-id="24224-103">Daftar harga produk</span><span class="sxs-lookup"><span data-stu-id="24224-103">Product price lists</span></span>

<span data-ttu-id="24224-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="24224-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="24224-105">Dalam Project Operations, **Daftar harga produk** dan entitas item daftar harga terkait mendukung fungsi untuk produk penetapan harga pada kuotasi berbasis produk dan baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="24224-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="24224-106">Untuk produk yang digunakan pada proyek, rekaman item daftar harga untuk daftar harga proyek digunakan.</span><span class="sxs-lookup"><span data-stu-id="24224-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="24224-107">Produk harus diatur sehingga mereka memiliki biaya default dan daftar harga dalam Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="24224-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="24224-108">Gunakan harga banderol, biaya standar, dan biaya saat ini untuk mengkonfigurasi biaya default dan harga banderol.</span><span class="sxs-lookup"><span data-stu-id="24224-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="24224-109">Harga banderol default digunakan pada baris kuotasi atau baris kontrak proyek hanya bila sistem tidak dapat menemukan baris daftar harga untuk produk tersebut dalam daftar harga produk untuk kuotasi atau kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="24224-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="24224-110">Harga biaya baris Katalog Produk dapat diubah antara kuotasi.</span><span class="sxs-lookup"><span data-stu-id="24224-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="24224-111">Kemampuan ini penting, karena jika Anda tidak melacak secara akurat biaya, Anda tidak dapat menentukan keuntungan operasional pada keterlibatan proyek.</span><span class="sxs-lookup"><span data-stu-id="24224-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="24224-112">Per default, biaya standar produk digunakan sebagai harga biaya.</span><span class="sxs-lookup"><span data-stu-id="24224-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="24224-113">Namun, harga default dapat diperbarui pada baris kuotasi jika ada harga yang berbeda untuk kuotasi tersebut.</span><span class="sxs-lookup"><span data-stu-id="24224-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="24224-114">Item Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="24224-114">Price list items</span></span>

<span data-ttu-id="24224-115">Anda dapat menambahkan produk dari Katalog Produk ke daftar harga yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="24224-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="24224-116">Baris daftar harga untuk produk selalu merujuk unit tertentu.</span><span class="sxs-lookup"><span data-stu-id="24224-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="24224-117">Harga untuk produk pada item daftar harga dapat dikonfigurasi sebagai jumlah mata uang.</span><span class="sxs-lookup"><span data-stu-id="24224-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="24224-118">Atau, dapat dikonfigurasi sebagai fungsi dari daftar harga, biaya saat ini, atau biaya standar.</span><span class="sxs-lookup"><span data-stu-id="24224-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="24224-119">Fungsi penetapan harga mendukung berbagai pilihan pembulatan saat harga produk dikonfigurasi sebagai fungsi dari daftar harga, biaya standar, atau biaya saat ini.</span><span class="sxs-lookup"><span data-stu-id="24224-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="24224-120">Selain mengambil keuntungan dari beberapa metode harga dan pilihan pembulatan, Anda dapat mengaitkan daftar diskon dengan item daftar harga.</span><span class="sxs-lookup"><span data-stu-id="24224-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="24224-121">Daftar Harga produk Default</span><span class="sxs-lookup"><span data-stu-id="24224-121">Default product price list</span></span>
<span data-ttu-id="24224-122">Setiap rekaman pelanggan memiliki bidang **daftar harga default**, di mana Anda dapat menentukan daftar harga yang sesuai dengan mata uang pelanggan.</span><span class="sxs-lookup"><span data-stu-id="24224-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="24224-123">Nilai default tidak secara otomatis dimasukkan dalam bidang ini.</span><span class="sxs-lookup"><span data-stu-id="24224-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="24224-124">Bila ada perjanjian harga kustom dengan pelanggan tertentu, Anda dapat menggunakan bidang ini untuk mengaitkan daftar harga dengan pelanggan tersebut.</span><span class="sxs-lookup"><span data-stu-id="24224-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="24224-125">Entitas kontrak proyek, peluang, dan kuotasi menggunakan urutan berikut untuk memasukkan daftar harga produk default.</span><span class="sxs-lookup"><span data-stu-id="24224-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="24224-126">Urutan yang sama digunakan untuk daftar harga proyek.</span><span class="sxs-lookup"><span data-stu-id="24224-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="24224-127">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="24224-127">Quote</span></span>
2.  <span data-ttu-id="24224-128">Peluang</span><span class="sxs-lookup"><span data-stu-id="24224-128">Opportunity</span></span>
3.  <span data-ttu-id="24224-129">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="24224-129">Customer</span></span>
4.  <span data-ttu-id="24224-130">Pengaturan global</span><span class="sxs-lookup"><span data-stu-id="24224-130">Global settings</span></span> 

<span data-ttu-id="24224-131">Secara default, bidang **produk** pada baris kuotasi mencantumkan semua produk aktif dalam daftar harga produk kuotasi.</span><span class="sxs-lookup"><span data-stu-id="24224-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="24224-132">Jika produk telah diaktifasi, atau jika produk tersebut adalah produk draf, maka produk tersebut tidak terdaftar, meskipun di dalam daftar harga.</span><span class="sxs-lookup"><span data-stu-id="24224-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="24224-133">Baris Katalog Produk ditambahkan sebagai baris faktur pada faktur pertama yang dibuat untuk kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="24224-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="24224-134">Pada faktur draf, baris faktur tersebut dapat dihapus.</span><span class="sxs-lookup"><span data-stu-id="24224-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="24224-135">Dalam kasus tersebut, baris akan muncul pada faktur berikutnya hingga ditagih, atau hingga faktur dikirim ke pelanggan.</span><span class="sxs-lookup"><span data-stu-id="24224-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="24224-136">Anda tidak dapat menagih kuantitas parsial baris faktur produk.</span><span class="sxs-lookup"><span data-stu-id="24224-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="24224-137">Saat lini produk dari kontrak proyek ditagih, nilai aktual dibuat.</span><span class="sxs-lookup"><span data-stu-id="24224-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="24224-138">Namun, aktual tersebut tidak ditautkan ke entitas proyek terkait.</span><span class="sxs-lookup"><span data-stu-id="24224-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="24224-139">Dengan kata lain, baris kontrak proyek berbasis produk terlepas dari penggunaan berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="24224-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

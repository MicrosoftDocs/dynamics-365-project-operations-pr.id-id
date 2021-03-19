---
title: Sekilas baris kuotasi berbasis produk - lite
description: Topik ini menyediakan informasi tentang bekerja dengan baris kuotasi berbasis produk.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272572"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="4263f-103">Sekilas baris kuotasi berbasis produk - lite</span><span class="sxs-lookup"><span data-stu-id="4263f-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="4263f-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="4263f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4263f-105">Anda dapat membuat baris kuotasi berbasis produk di Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="4263f-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="4263f-106">Anda Baris kuotasi berbasis produk dapat ditambahkan secara manual, atau dapat berupa item dari Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="4263f-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="4263f-107">Katalog produk</span><span class="sxs-lookup"><span data-stu-id="4263f-107">Product catalog</span></span>

<span data-ttu-id="4263f-108">Setiap produk dalam Katalog Produk memiliki unit default dan grup unit.</span><span class="sxs-lookup"><span data-stu-id="4263f-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="4263f-109">Jika beberapa produk memiliki rangkaian atribut yang sama, Anda dapat membuat rangkaian produk yang juga memiliki atribut serupa.</span><span class="sxs-lookup"><span data-stu-id="4263f-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="4263f-110">Misalnya, perusahaan menjual lisensi langganan untuk berbagai jenis perangkat lunak.</span><span class="sxs-lookup"><span data-stu-id="4263f-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="4263f-111">Semua perangkat lunak langganan memiliki dua atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="4263f-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="4263f-112">Jumlah pengguna</span><span class="sxs-lookup"><span data-stu-id="4263f-112">Number of users</span></span>
- <span data-ttu-id="4263f-113">Durasi langganan yang diukur dalam bulan</span><span class="sxs-lookup"><span data-stu-id="4263f-113">A subscription duration measured in months</span></span>

<span data-ttu-id="4263f-114">Untuk mengelola Katalog jenis, buat rangkaian produk yang diberi nama **perangkat lunak langganan**, dan tambahkan jumlah pengguna dan durasi langganan sebagai atribut.</span><span class="sxs-lookup"><span data-stu-id="4263f-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="4263f-115">Selanjutnya, Anda dapat menambahkan produk individual ke keluarga produk **perangkat lunak langganan**.</span><span class="sxs-lookup"><span data-stu-id="4263f-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="4263f-116">Tambahkan item Katalog Produk ke kuotasi proyek</span><span class="sxs-lookup"><span data-stu-id="4263f-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="4263f-117">Halaman **kuotasi proyek** dan **kontrak proyek** memiliki bagian untuk baris berbasis proyek dan baris berbasis produk.</span><span class="sxs-lookup"><span data-stu-id="4263f-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="4263f-118">Untuk baris berbasis produk, daftar drop-down pada baris kuotasi atau baris kontrak proyek mencakup semua produk dan unit dalam daftar harga produk.</span><span class="sxs-lookup"><span data-stu-id="4263f-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="4263f-119">Anda juga dapat menambahkan produk yang bukan bagian dari daftar harga produk.</span><span class="sxs-lookup"><span data-stu-id="4263f-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="4263f-120">Selain itu, Anda dapat memilih produk dari daftar harga lain atau langsung dari Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="4263f-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="4263f-121">Bila Anda memilih produk secara langsung dari Katalog Produk, daftar harga default produk tersebut digunakan untuk mendapatkan harga penjualan produk.</span><span class="sxs-lookup"><span data-stu-id="4263f-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="4263f-122">Jika daftar harga default tidak diatur, harga diatur ke 0 (nol).</span><span class="sxs-lookup"><span data-stu-id="4263f-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="4263f-123">Jika baris kuotasi didasarkan pada Katalog Produk, Anda dapat menimpa harga penjualan secara langsung pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="4263f-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="4263f-124">Baris kuotasi dalam bidang **harga** dengan dua nilai yang tersedia:</span><span class="sxs-lookup"><span data-stu-id="4263f-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="4263f-125">**Timpa Harga**</span><span class="sxs-lookup"><span data-stu-id="4263f-125">**Override Pricing**</span></span>
- <span data-ttu-id="4263f-126">**Gunakan Default**</span><span class="sxs-lookup"><span data-stu-id="4263f-126">**Use Default**</span></span>

<span data-ttu-id="4263f-127">Jika Anda memilih **Timpa Harga**, harga default tidak diatur.</span><span class="sxs-lookup"><span data-stu-id="4263f-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="4263f-128">Namun, Anda harus memasukkan harga untuk produk pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="4263f-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="4263f-129">Jika Anda memilih **gunakan default**, harga penjualan default akan digunakan dan bidang terkunci untuk pengeditan.</span><span class="sxs-lookup"><span data-stu-id="4263f-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="4263f-130">Harga penjualan default dimasukkan pada baris berbasis produk pada kuotasi.</span><span class="sxs-lookup"><span data-stu-id="4263f-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="4263f-131">Bidang **harga** kemudian diatur ke **Timpa Harga** sehingga Anda dapat mengedit harga default pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="4263f-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="4263f-132">Ini adalah penimpaan khusus Project Operations pada perilaku baris berbasis produk di Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="4263f-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
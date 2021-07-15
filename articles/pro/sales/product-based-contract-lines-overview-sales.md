---
title: Ikhtisar baris kontrak berbasis produk - lite
description: Topik ini menyediakan informasi tentang baris kontrak berbasis produk.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 8464eefbce9ba266360e10039e2a0be78982d8fa
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369740"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="52e5c-103">Ikhtisar baris kontrak berbasis produk - lite</span><span class="sxs-lookup"><span data-stu-id="52e5c-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="52e5c-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="52e5c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="52e5c-105">Anda dapat membuat baris kontrak berbasis produk di Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="52e5c-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="52e5c-106">Baris kontrak berbasis produk dapat berupa baris yang dibuat secara manual, atau dapat berupa item dari Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="52e5c-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="52e5c-107">Katalog produk</span><span class="sxs-lookup"><span data-stu-id="52e5c-107">Product catalog</span></span>

<span data-ttu-id="52e5c-108">Produk dalam Katalog Produk memiliki unit default dan grup unit.</span><span class="sxs-lookup"><span data-stu-id="52e5c-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="52e5c-109">Jika beberapa produk memiliki rangkaian atribut yang sama, Anda dapat membuat rangkaian produk yang juga memiliki atribut tersebut.</span><span class="sxs-lookup"><span data-stu-id="52e5c-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="52e5c-110">Semua produk dalam satu rangkaian produk mewarisi rangkaian atribut yang sama.</span><span class="sxs-lookup"><span data-stu-id="52e5c-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="52e5c-111">Misalnya, perusahaan menjual lisensi langganan untuk berbagai jenis perangkat lunak.</span><span class="sxs-lookup"><span data-stu-id="52e5c-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="52e5c-112">Semua perangkat lunak langganan memiliki dua atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="52e5c-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="52e5c-113">Jumlah pengguna</span><span class="sxs-lookup"><span data-stu-id="52e5c-113">Number of users</span></span>
- <span data-ttu-id="52e5c-114">Durasi langganan (dalam bulan)</span><span class="sxs-lookup"><span data-stu-id="52e5c-114">Subscription duration (in months)</span></span>

<span data-ttu-id="52e5c-115">Untuk mengelola jenis Katalog ini, buat rangkaian produk yang diberi nama **perangkat lunak langganan**.</span><span class="sxs-lookup"><span data-stu-id="52e5c-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="52e5c-116">Tambahkan atribut, **jumlah pengguna,** dan **durasi langganan** ke rangkaian produk.</span><span class="sxs-lookup"><span data-stu-id="52e5c-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="52e5c-117">Selanjutnya, tambahkan produk individual ke rangkaian produk **perangkat lunak langganan**.</span><span class="sxs-lookup"><span data-stu-id="52e5c-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="52e5c-118">Tambahkan item Katalog Produk ke kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="52e5c-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="52e5c-119">Kontrak proyek memiliki bagian untuk dua jenis baris: berbasis proyek dan produk.</span><span class="sxs-lookup"><span data-stu-id="52e5c-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="52e5c-120">Baris berbasis produk mencakup semua produk dan unit dalam daftar harga produk pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="52e5c-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="52e5c-121">Produk yang bukan bagian dari daftar harga produk kontrak dapat ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="52e5c-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="52e5c-122">Anda dapat memilih produk dari daftar harga lainnya, atau langsung dari Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="52e5c-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="52e5c-123">Bila Anda memilih produk secara langsung dari Katalog Produk, daftar harga default produk tersebut digunakan untuk harga penjualan produk.</span><span class="sxs-lookup"><span data-stu-id="52e5c-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="52e5c-124">Jika daftar harga default tidak diatur, harga diatur ke 0 (nol).</span><span class="sxs-lookup"><span data-stu-id="52e5c-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="52e5c-125">Jika baris kontrak didasarkan pada Katalog Produk, Anda dapat menimpa harga penjualan secara langsung pada baris tersebut.</span><span class="sxs-lookup"><span data-stu-id="52e5c-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="52e5c-126">Baris kontrak memiliki bidang **harga** dengan dua nilai:</span><span class="sxs-lookup"><span data-stu-id="52e5c-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="52e5c-127">**Timpa Harga**</span><span class="sxs-lookup"><span data-stu-id="52e5c-127">**Override pricing**</span></span>
- <span data-ttu-id="52e5c-128">**Gunakan default**</span><span class="sxs-lookup"><span data-stu-id="52e5c-128">**Use default**</span></span>

<span data-ttu-id="52e5c-129">Jika Anda menetapkan bidang **Harga** ke **Timpa Harga**, harga default tidak ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="52e5c-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="52e5c-130">Masukkan harga untuk produk pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="52e5c-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="52e5c-131">Jika Anda mengatur bidang ke **Gunakan default**, harga penjualan default akan digunakan dan bidang tidak dapat diedit.</span><span class="sxs-lookup"><span data-stu-id="52e5c-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="52e5c-132">Setelah Anda menginstal Project Operations, harga penjualan default dimasukkan pada baris berbasis produk pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="52e5c-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="52e5c-133">Bidang **harga** kemudian diatur ke **Timpa Harga** sehingga Anda dapat mengedit harga default pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="52e5c-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="52e5c-134">Ini adalah penimpaan spesifik Project Operations pada perilaku baris berbasis produk di Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="52e5c-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Baris kuotasi berbasis produk
description: Topik ini menyediakan informasi tentang kuotasi berbasis produk.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151257"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="fd14d-103">Baris kuotasi berbasis produk</span><span class="sxs-lookup"><span data-stu-id="fd14d-103">Product-based quote lines</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="fd14d-104">Anda dapat membuat baris kuotasi berbasis produk di Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="fd14d-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="fd14d-105">Baris kuotasi berbasis produk dapat berupa baris "tulis", atau dapat berupa item dari Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="fd14d-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="fd14d-106">Katalog produk</span><span class="sxs-lookup"><span data-stu-id="fd14d-106">Product catalog</span></span>

<span data-ttu-id="fd14d-107">Produk dalam Katalog Produk Dynamics 365 memiliki unit default dan grup unit.</span><span class="sxs-lookup"><span data-stu-id="fd14d-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="fd14d-108">Jika beberapa produk memiliki rangkaian atribut yang sama, Anda dapat membuat rangkaian produk yang juga memiliki atribut tersebut.</span><span class="sxs-lookup"><span data-stu-id="fd14d-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="fd14d-109">Semua produk dalam satu rangkaian produk mewarisi rangkaian atribut yang sama.</span><span class="sxs-lookup"><span data-stu-id="fd14d-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="fd14d-110">Misalnya, perusahaan menjual lisensi langganan untuk berbagai perangkat lunak.</span><span class="sxs-lookup"><span data-stu-id="fd14d-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="fd14d-111">Semua perangkat lunak langganan memiliki dua atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="fd14d-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="fd14d-112">Jumlah Pengguna</span><span class="sxs-lookup"><span data-stu-id="fd14d-112">Number of users</span></span> 
- <span data-ttu-id="fd14d-113">Durasi langganan (dalam bulan)</span><span class="sxs-lookup"><span data-stu-id="fd14d-113">Subscription duration (in months)</span></span>

<span data-ttu-id="fd14d-114">Cara yang baik untuk mempertahankan Katalog jenis ini adalah dengan membuat rangkaian produk yang diberi nama **perangkat lunak langganan**, dan memiliki **jumlah pengguna** dan **durasi langganan** sebagai atribut.</span><span class="sxs-lookup"><span data-stu-id="fd14d-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software**, and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="fd14d-115">Selanjutnya, Anda dapat menambahkan produk individual, seperti **Dynamics 365 Sales** atau **Dynamics 365 Field Service** ke rangkaian produk **perangkat lunak langganan**.</span><span class="sxs-lookup"><span data-stu-id="fd14d-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="fd14d-116">Menambahkan item Katalog Produk ke kuotasi proyek</span><span class="sxs-lookup"><span data-stu-id="fd14d-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="fd14d-117">Halaman kuotasi proyek dan kontrak proyek memiliki bagian untuk dua jenis baris: baris berbasis proyek dan lini produk.</span><span class="sxs-lookup"><span data-stu-id="fd14d-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="fd14d-118">Untuk baris berbasis produk, Dynamics 365 digunakan untuk menambahkan item dari Katalog Produk ke kuotasi.</span><span class="sxs-lookup"><span data-stu-id="fd14d-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="fd14d-119">Daftar drop-down pada baris kuotasi atau kontrak proyek mencakup semua produk dan unit dalam daftar harga produk yang dilampirkan pada kuotasi atau kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="fd14d-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="fd14d-120">Anda juga dapat menambahkan produk yang bukan bagian dari daftar harga produk kuotasi.</span><span class="sxs-lookup"><span data-stu-id="fd14d-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="fd14d-121">Selain itu, Anda dapat memilih produk dari daftar harga lain, atau Anda dapat memilih produk langsung dari Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="fd14d-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="fd14d-122">Bila Anda memilih produk secara langsung dari Katalog Produk, daftar harga default produk tersebut digunakan untuk mendapatkan harga penjualan produk.</span><span class="sxs-lookup"><span data-stu-id="fd14d-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="fd14d-123">Jika daftar harga default tidak diatur, harga diatur ke 0 (nol).</span><span class="sxs-lookup"><span data-stu-id="fd14d-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="fd14d-124">Jika baris kuotasi didasarkan pada Katalog Produk, Anda dapat menimpa harga penjualan secara langsung pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="fd14d-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="fd14d-125">Perhatikan bahwa baris kuotasi di Dynamics 365 memiliki bidang **harga**.</span><span class="sxs-lookup"><span data-stu-id="fd14d-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="fd14d-126">Tersedia dua nilai:</span><span class="sxs-lookup"><span data-stu-id="fd14d-126">Two values are available:</span></span>

- <span data-ttu-id="fd14d-127">Timpa Harga</span><span class="sxs-lookup"><span data-stu-id="fd14d-127">Override pricing</span></span>  
- <span data-ttu-id="fd14d-128">Gunakan default</span><span class="sxs-lookup"><span data-stu-id="fd14d-128">Use default</span></span>

<span data-ttu-id="fd14d-129">Jika Anda menetapkan bidang ini ke **Timpa Harga**, Dynamics 365 tidak menetapkan harga default.</span><span class="sxs-lookup"><span data-stu-id="fd14d-129">If you set this field to **Override pricing**, Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="fd14d-130">Anda harus memasukkan harga untuk produk pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="fd14d-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="fd14d-131">Jika Anda menetapkan bidang ini ke **Gunakan default**, maka Dynamics 365 menggunakan harga penjualan default dan mengunci bidang untuk mencegah pengeditan.</span><span class="sxs-lookup"><span data-stu-id="fd14d-131">If you set this field to **Use default**, Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="fd14d-132">Setelah Anda menginstal PSA, harga penjualan default dimasukkan pada baris berbasis produk pada kuotasi.</span><span class="sxs-lookup"><span data-stu-id="fd14d-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="fd14d-133">Bidang **harga** kemudian diatur ke **Timpa Harga** sehingga Anda dapat mengedit harga default pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="fd14d-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Mengatur Timpa Harga](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="fd14d-135">Faktor kuantitas untuk produk</span><span class="sxs-lookup"><span data-stu-id="fd14d-135">Quantity factors for products</span></span>

<span data-ttu-id="fd14d-136">PSA menggunakan faktor kuantitas untuk mendukung penjualan produk berbasis langganan.</span><span class="sxs-lookup"><span data-stu-id="fd14d-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="fd14d-137">Untuk produk berbasis langganan, kuantitas pada kuotasi atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="fd14d-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="fd14d-138">Biasanya, harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan.</span><span class="sxs-lookup"><span data-stu-id="fd14d-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="fd14d-139">Namun, Anda dapat menggunakan Deskripsi waktu lain.</span><span class="sxs-lookup"><span data-stu-id="fd14d-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="fd14d-140">Selama proses penjualan, harga pada baris kuotasi biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan TI.</span><span class="sxs-lookup"><span data-stu-id="fd14d-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="fd14d-141">Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="fd14d-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="fd14d-142">Kuantitas yang digunakan untuk menghitung jumlah baris kuotasi adalah produk dari jumlah pengguna dan jumlah bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="fd14d-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="fd14d-143">Untuk mendukung jenis penjualan, PSA memperkenalkan konsep faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="fd14d-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="fd14d-144">Faktor kuantitas mengandalkan atribut produk di Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fd14d-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="fd14d-145">Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, PSA memungkinkan Anda menandai subset properti tersebut, atau semua properti, sebagai faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="fd14d-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="fd14d-146">PSA memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="fd14d-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="fd14d-147">Bila produk yang memiliki faktor kuantitas dikonfigurasi untuk ditambahkan ke baris kuotasi, bidang **kuantitas** pada baris kuotasi menjadi bidang hanya baca.</span><span class="sxs-lookup"><span data-stu-id="fd14d-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="fd14d-148">Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, PSA menghitung kuantitas baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="fd14d-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="fd14d-149">Misalnya, Dynamics 365 mungkin memiliki properti berikut:</span><span class="sxs-lookup"><span data-stu-id="fd14d-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="fd14d-150">**Jumlah pengguna** -jumlah pengguna</span><span class="sxs-lookup"><span data-stu-id="fd14d-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="fd14d-151">**Jumlah bulan** -jumlah bulan langganan</span><span class="sxs-lookup"><span data-stu-id="fd14d-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="fd14d-152">**SKU Produk**</span><span class="sxs-lookup"><span data-stu-id="fd14d-152">**Product SKU**</span></span> 

<span data-ttu-id="fd14d-153">Properti **Jumlah pengguna** dan **Jumlah bulan** dapat ditandai sebagai faktor kuantitas dengan mengedit properti lini produk.</span><span class="sxs-lookup"><span data-stu-id="fd14d-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Menandai Jumlah pengguna dan Jumlah bulan sebagai faktor kualitas](media/basic-guide-11.png)
 

---
title: Mengelola unit kompleks seperti per-pengguna, per bulan untuk baris kuotasi berbasis produk
description: Topik ini memberikan informasi tentang mengeluarkan unit kompleks untuk baris kuotasi berbasis produk.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 741230e69302138cce8f7379f520f7178e1c80af
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078416"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines"></a><span data-ttu-id="b406f-103">Mengelola unit kompleks seperti per-pengguna, per bulan untuk baris kuotasi berbasis produk</span><span class="sxs-lookup"><span data-stu-id="b406f-103">Managing complex units such as per-user, per-month for product-based quote lines</span></span>

<span data-ttu-id="b406f-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b406f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b406f-105">Dynamics 365 Project Operations menggunakan faktor kuantitas untuk mendukung penjualan produk berbasis langganan.</span><span class="sxs-lookup"><span data-stu-id="b406f-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="b406f-106">Untuk produk berbasis langganan, kuantitas pada kuotasi atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="b406f-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="b406f-107">Biasanya, harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan.</span><span class="sxs-lookup"><span data-stu-id="b406f-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="b406f-108">Selama proses penjualan, harga pada baris kuotasi biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan TI.</span><span class="sxs-lookup"><span data-stu-id="b406f-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="b406f-109">Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="b406f-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="b406f-110">Kuantitas yang digunakan untuk menghitung baris kuotasi adalah produk dari jumlah pengguna dan jumlah bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="b406f-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="b406f-111">Untuk mendukung jenis penjualan, Project Operations memperkenalkan konsep faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b406f-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="b406f-112">Faktor kuantitas mengandalkan atribut produk di Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b406f-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="b406f-113">Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, Project Operations memungkinkan Anda menandai subset, atau semua properti, sebagai faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b406f-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="b406f-114">Project Operations memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b406f-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="b406f-115">Bila Anda menambahkan produk dengan faktor kuantitas ke baris kuotasi, bidang **kuantitas** menjadi hanya baca.</span><span class="sxs-lookup"><span data-stu-id="b406f-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="b406f-116">Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, Project Operations menghitung kuantitas baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b406f-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="b406f-117">Misalnya, Dynamics 365 Sales mungkin memiliki properti berikut:</span><span class="sxs-lookup"><span data-stu-id="b406f-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="b406f-118">**Jumlah pengguna** : jumlah pengguna</span><span class="sxs-lookup"><span data-stu-id="b406f-118">**No of users** : The number of users</span></span>
- <span data-ttu-id="b406f-119">**Jumlah bulan** : jumlah bulan langganan</span><span class="sxs-lookup"><span data-stu-id="b406f-119">**No of Months** : The number of subscription months</span></span>
- <span data-ttu-id="b406f-120">**SKU Produk**</span><span class="sxs-lookup"><span data-stu-id="b406f-120">**Product SKU**</span></span>

<span data-ttu-id="b406f-121">Anda dapat menandai **Jumlah pengguna** dan **Jumlah bulan** sebagai faktor kuantitas dengan mengedit properti lini produk.</span><span class="sxs-lookup"><span data-stu-id="b406f-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="b406f-122">Untuk membuat faktor kuantitas dari properti produk, ikuti langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="b406f-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="b406f-123">Di panel navigasi kiri Project Operations, buka **penjualan** > **produk**.</span><span class="sxs-lookup"><span data-stu-id="b406f-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="b406f-124">Buka produk yang Anda perlukan untuk mengkonfigurasikan faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b406f-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="b406f-125">Pastikan produk memiliki properti yang telah dikonfigurasi.</span><span class="sxs-lookup"><span data-stu-id="b406f-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="b406f-126">Pada halaman **informasi proyek** untuk produk, pilih tab **faktor kuantitas**.</span><span class="sxs-lookup"><span data-stu-id="b406f-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="b406f-127">Di subkisi, pilih **+ perhitungan Bidang baru**.</span><span class="sxs-lookup"><span data-stu-id="b406f-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="b406f-128">Masukkan nama faktor kuantitas, lalu pilih nilai properti yang dipetakan ke penghitungan bidang.</span><span class="sxs-lookup"><span data-stu-id="b406f-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="b406f-129">Simpan dan tutup formulir.</span><span class="sxs-lookup"><span data-stu-id="b406f-129">Save and close the form.</span></span> <span data-ttu-id="b406f-130">Ulangi langkah ini untuk semua properti yang akan digunakan untuk menghitung kuantitas untuk baris kuotasi berdasarkan produk.</span><span class="sxs-lookup"><span data-stu-id="b406f-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="b406f-131">Bila Anda membuat baris kuotasi berbasis produk untuk produk, kuantitas baris kuotasi akan dikunci.</span><span class="sxs-lookup"><span data-stu-id="b406f-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="b406f-132">Kuantitas akan dihitung sebagai produk dari nilai properti yang Anda masukkan untuk baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b406f-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>

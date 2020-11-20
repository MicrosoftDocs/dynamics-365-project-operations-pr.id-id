---
title: Mengelola unit yang kompleks untuk baris kontrak berbasis produk - lite
description: Topik ini menyediakan informasi tentang cara mendukung penjualan produk berbasis langganan.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177380"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="cb72c-103">Mengelola unit yang kompleks untuk baris kontrak berbasis produk - lite</span><span class="sxs-lookup"><span data-stu-id="cb72c-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="cb72c-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="cb72c-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb72c-105">Dynamics 365 Project Operations menggunakan faktor kuantitas untuk mendukung penjualan produk berbasis langganan.</span><span class="sxs-lookup"><span data-stu-id="cb72c-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="cb72c-106">Untuk produk berbasis langganan, kuantitas pada kontrak atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.</span><span class="sxs-lookup"><span data-stu-id="cb72c-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="cb72c-107">Harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan.</span><span class="sxs-lookup"><span data-stu-id="cb72c-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="cb72c-108">Selama proses penjualan, harga pada baris kontrak biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan.</span><span class="sxs-lookup"><span data-stu-id="cb72c-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="cb72c-109">Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="cb72c-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="cb72c-110">Kuantitas yang digunakan untuk menghitung jumlah baris kontrak adalah produk dari jumlah pengguna dan jumlah bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="cb72c-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="cb72c-111">Untuk mendukung jenis penjualan, Project Operations mendukung konsep *faktor kuantitas*.</span><span class="sxs-lookup"><span data-stu-id="cb72c-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="cb72c-112">Faktor kuantitas mengandalkan atribut produk.</span><span class="sxs-lookup"><span data-stu-id="cb72c-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="cb72c-113">Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, Anda dapat menandai subset properti tersebut, atau semua properti, sebagai faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="cb72c-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="cb72c-114">Project Operations memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas.</span><span class="sxs-lookup"><span data-stu-id="cb72c-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="cb72c-115">Bila produk dengan faktor kuantitas yang dikonfigurasi ditambahkan ke baris kontrak, bidang **kuantitas** menjadi hanya baca.</span><span class="sxs-lookup"><span data-stu-id="cb72c-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="cb72c-116">Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, Project Operations menghitung kuantitas baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="cb72c-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="cb72c-117">Misalnya, Dynamics 365 Sales mungkin memiliki properti berikut:</span><span class="sxs-lookup"><span data-stu-id="cb72c-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="cb72c-118">**Jumlah pengguna**: jumlah pengguna.</span><span class="sxs-lookup"><span data-stu-id="cb72c-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="cb72c-119">**Jumlah bulan**: jumlah bulan langganan.</span><span class="sxs-lookup"><span data-stu-id="cb72c-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="cb72c-120">**SKU produk**: unit penyimpanan stok (SKU) untuk produk.</span><span class="sxs-lookup"><span data-stu-id="cb72c-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="cb72c-121">Properti **Jumlah pengguna** dan **Jumlah bulan** dapat ditandai sebagai faktor kuantitas dengan mengedit properti lini produk.</span><span class="sxs-lookup"><span data-stu-id="cb72c-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="cb72c-122">Untuk membuat faktor kuantitas dari properti produk, selesaikan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="cb72c-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="cb72c-123">Pada **Project Operations**, pilih **produk penjualan**.</span><span class="sxs-lookup"><span data-stu-id="cb72c-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="cb72c-124">Buka produk yang harus Anda konfigurasikan faktor kuantitasnya.</span><span class="sxs-lookup"><span data-stu-id="cb72c-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="cb72c-125">Pastikan bahwa produk memiliki properti yang telah diatur.</span><span class="sxs-lookup"><span data-stu-id="cb72c-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="cb72c-126">Pada halaman **informasi proyek**, pilih tab **faktor kuantitas**.</span><span class="sxs-lookup"><span data-stu-id="cb72c-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="cb72c-127">Di subkisi, pilih **+ perhitungan Bidang baru**.</span><span class="sxs-lookup"><span data-stu-id="cb72c-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="cb72c-128">Masukkan nama **faktor kuantitas**, lalu pilih nilai properti yang dipetakan ke penghitungan bidang.</span><span class="sxs-lookup"><span data-stu-id="cb72c-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="cb72c-129">Simpan dan tutup formulir.</span><span class="sxs-lookup"><span data-stu-id="cb72c-129">Save and close the form.</span></span>
7. <span data-ttu-id="cb72c-130">Ulangi langkah 2-6 untuk semua properti yang bersama-sama akan membuat kuantitas untuk baris kontrak berbasis produk.</span><span class="sxs-lookup"><span data-stu-id="cb72c-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="cb72c-131">Dengan mengatur faktor kuantitas, saat pengguna membuat baris kontrak untuk produk ini, kuantitas baris kontrak terkunci.</span><span class="sxs-lookup"><span data-stu-id="cb72c-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="cb72c-132">Kuantitas kemudian dihitung sebagai produk dari nilai properti untuk baris kontrak tersebut.</span><span class="sxs-lookup"><span data-stu-id="cb72c-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>

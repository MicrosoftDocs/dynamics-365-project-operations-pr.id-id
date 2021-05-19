---
title: Estimasi keuangan untuk bahan pada proyek
description: Laporan topik memberikan informasi tentang mendefinisikan atau memperkirakan bahan berbasis proyek.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788865"
---
# <a name="financial-estimates-for-materials-on-projects"></a><span data-ttu-id="c5512-103">Estimasi keuangan untuk bahan pada proyek</span><span class="sxs-lookup"><span data-stu-id="c5512-103">Financial estimates for materials on projects</span></span>

<span data-ttu-id="c5512-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="c5512-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c5512-105">Dynamics 365 Project Operations memungkinkan manajer proyek menentukan biaya bahan berbasis proyek untuk setiap proyek atau tugas.</span><span class="sxs-lookup"><span data-stu-id="c5512-105">Dynamics 365 Project Operations allows Project managers to define project-based material costs for each project or task.</span></span> <span data-ttu-id="c5512-106">Setiap estimasi bahan dapat dikaitkan dengan tugas proyek tertentu.</span><span class="sxs-lookup"><span data-stu-id="c5512-106">Each material estimate can be associated with a specific project task.</span></span> <span data-ttu-id="c5512-107">Pengeluaran dikategorikan ke dalam berbagai kategori pengeluaran, yang ditentukan pada tingkat organisasional.</span><span class="sxs-lookup"><span data-stu-id="c5512-107">Expenses are categorized into different expense categories, which are defined at the organizational level.</span></span> <span data-ttu-id="c5512-108">Harga dan biaya untuk setiap kategori pengeluaran ditentukan dalam daftar harga.</span><span class="sxs-lookup"><span data-stu-id="c5512-108">Pricing and costing for each expense category is defined in the price list.</span></span> 

<span data-ttu-id="c5512-109">Lengkapi langkah-langkah berikut untuk melihat, menambah, atau menghapus estimasi bahan proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-109">Complete the following steps to view, add, or delete a project material estimate.</span></span>

1. <span data-ttu-id="c5512-110">Buka **Proyek**, lalu pilih proyek yang akan diperbarui.</span><span class="sxs-lookup"><span data-stu-id="c5512-110">Go to **Projects**, and select the project you want to update.</span></span>
2. <span data-ttu-id="c5512-111">Pada tab **Estimasi Bahan**, lihat daftar estimasi bahan proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-111">On the **Material Estimates** tab, view the list of project material estimates.</span></span>
3. <span data-ttu-id="c5512-112">Pilih **Estimasi Bahan Baru** untuk membuat perkiraan bahan baru.</span><span class="sxs-lookup"><span data-stu-id="c5512-112">Select **New Material estimate** to create a new material estimate.</span></span> <span data-ttu-id="c5512-113">Atau, pilih estimasi bahan untuk dihapus, lalu pilih **Hapus Perkiraan Bahan**.</span><span class="sxs-lookup"><span data-stu-id="c5512-113">Or, select a material estimate to delete, and then select **Delete Material Estimate**.</span></span>

<span data-ttu-id="c5512-114">Tabel berikut memberikan informasi tentang bidang pada **baris estimasi bahan** di Proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-114">The following table provides information about the fields on the **Material Estimate line** on a project.</span></span> 

| <span data-ttu-id="c5512-115">**Bidang**</span><span class="sxs-lookup"><span data-stu-id="c5512-115">**Field**</span></span> | <span data-ttu-id="c5512-116">**Deskripsi**</span><span class="sxs-lookup"><span data-stu-id="c5512-116">**Description**</span></span> | <span data-ttu-id="c5512-117">**Dampak hilir**</span><span class="sxs-lookup"><span data-stu-id="c5512-117">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c5512-118">Tugas</span><span class="sxs-lookup"><span data-stu-id="c5512-118">Task</span></span> | <span data-ttu-id="c5512-119">Semua tugas dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-119">A list of tasks in the project.</span></span> <span data-ttu-id="c5512-120">Ini mencakup tugas node leaf dan ringkasan.</span><span class="sxs-lookup"><span data-stu-id="c5512-120">This includes summary and leaf node tasks.</span></span> | <span data-ttu-id="c5512-121">Bila Anda memilih tugas untuk baris estimasi bahan, perkiraan biaya bahandan perkiraan penjualan bahan untuk tugas akan terpengaruh.</span><span class="sxs-lookup"><span data-stu-id="c5512-121">When you select a task for a material estimate line, the estimated material cost and estimated material sales for a task are impacted.</span></span> <span data-ttu-id="c5512-122">Jika bidang ini kosong, perkiraan bahan dilacak dan diringkas hanya pada tingkat proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-122">If this field is empty, the material estimate is tracked and summarized only at the project level.</span></span> |
| <span data-ttu-id="c5512-123">Pilih Produk</span><span class="sxs-lookup"><span data-stu-id="c5512-123">Select Product</span></span> |  <span data-ttu-id="c5512-124">Anda dapat menentukan apakah baris estimasi ini adalah untuk produk yang Ada (katalog) atau produk pilihan.</span><span class="sxs-lookup"><span data-stu-id="c5512-124">You can specify whether the estimate line is for an existing (catalog) or write-in product.</span></span> | <span data-ttu-id="c5512-125">Bidang ini menentukan apakah Anda memilih produk dari katalog atau produk pilihan.</span><span class="sxs-lookup"><span data-stu-id="c5512-125">This field determines if you select a product from the catalog or a write in product.</span></span> |
| <span data-ttu-id="c5512-126">Produk</span><span class="sxs-lookup"><span data-stu-id="c5512-126">Product</span></span> | <span data-ttu-id="c5512-127">ID produk dari katalog produk.</span><span class="sxs-lookup"><span data-stu-id="c5512-127">The ID of the product from the product catalog.</span></span> <span data-ttu-id="c5512-128">Bila Anda memilih ID produk, nilai di bidang **Pilih Produk** akan secara otomatis diperbarui ke **produk yang ada**.</span><span class="sxs-lookup"><span data-stu-id="c5512-128">When you select a product ID, the value in the **Select Product** field is automatically updated to **Existing product**.</span></span> <span data-ttu-id="c5512-129">ID tersebut digunakan untuk mengambil harga biaya dan penjualan dari daftar harga.</span><span class="sxs-lookup"><span data-stu-id="c5512-129">The ID is used to retrieve the cost and sales prices from the price list.</span></span> | <span data-ttu-id="c5512-130">Tidak ada dampak hilir untuk bidang ini.</span><span class="sxs-lookup"><span data-stu-id="c5512-130">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="c5512-131">Deskripsi Produk Pilihan</span><span class="sxs-lookup"><span data-stu-id="c5512-131">Write In Product Description</span></span> | <span data-ttu-id="c5512-132">Bidang teks untuk menulis nama produk.</span><span class="sxs-lookup"><span data-stu-id="c5512-132">A text field to write in the name of the product.</span></span> <span data-ttu-id="c5512-133">Bidang harus digunakan jika **Pilihan** dipilih dalam bidang **pilih Produk**.</span><span class="sxs-lookup"><span data-stu-id="c5512-133">This field should be used when **Write In** is selected in the **Select Product** field.</span></span>| <span data-ttu-id="c5512-134">Tidak ada dampak hilir untuk bidang ini.</span><span class="sxs-lookup"><span data-stu-id="c5512-134">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="c5512-135">Tanggal mulai</span><span class="sxs-lookup"><span data-stu-id="c5512-135">Start date</span></span> | <span data-ttu-id="c5512-136">Tanggal perkiraan untuk digunakannya bahan.</span><span class="sxs-lookup"><span data-stu-id="c5512-136">The forecasted date on which the material is expected to be used.</span></span> | <span data-ttu-id="c5512-137">Tidak ada dampak hilir untuk bidang ini.</span><span class="sxs-lookup"><span data-stu-id="c5512-137">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="c5512-138">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="c5512-138">Unit group</span></span> | <span data-ttu-id="c5512-139">Nilai default pada bidang ini berasal dari grup unit default pada produk katalog.</span><span class="sxs-lookup"><span data-stu-id="c5512-139">The default value in this field comes from the default unit group on the catalog product.</span></span> <span data-ttu-id="c5512-140">Anda dapat memperbarui bidang ini untuk memilih grup unit lain.</span><span class="sxs-lookup"><span data-stu-id="c5512-140">You can update this field to select another unit group.</span></span> | <span data-ttu-id="c5512-141">Tidak ada dampak hilir untuk bidang ini.</span><span class="sxs-lookup"><span data-stu-id="c5512-141">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="c5512-142">Unit</span><span class="sxs-lookup"><span data-stu-id="c5512-142">Unit</span></span> | <span data-ttu-id="c5512-143">Nilai di bidang ini akan berasal dari unit default dari produk yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="c5512-143">The value in this field comes from the default unit of the selected product.</span></span> <span data-ttu-id="c5512-144">Anda dapat memperbarui bidang ini untuk memilih unit lain.</span><span class="sxs-lookup"><span data-stu-id="c5512-144">You can update this field to select another unit.</span></span> | <span data-ttu-id="c5512-145">Mengubah unit menghasilkan biaya dan harga per unit default yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="c5512-145">Changing the unit results in a different default unit price and cost.</span></span> |
| <span data-ttu-id="c5512-146">Quantity</span><span class="sxs-lookup"><span data-stu-id="c5512-146">Quantity</span></span> | <span data-ttu-id="c5512-147">Estimasi kuantitas produk yang akan digunakan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-147">The estimated quantity of the product that will be used on the project.</span></span> | <span data-ttu-id="c5512-148">Tidak ada dampak hilir untuk bidang ini.</span><span class="sxs-lookup"><span data-stu-id="c5512-148">There is no downstream impact for this field.</span></span> |
| <span data-ttu-id="c5512-149">Biaya Unit</span><span class="sxs-lookup"><span data-stu-id="c5512-149">Unit Cost</span></span> | <span data-ttu-id="c5512-150">Biaya per unit dari kombinasi produk dan unit yang dipilih sebagaimana diatur dalam daftar harga biaya yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="c5512-150">The unit cost of the selected product and unit combination as set up in the applicable cost price list.</span></span> | <span data-ttu-id="c5512-151">Biaya unit selalu ditampilkan dalam mata uang biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-151">The unit cost is always shown in the project's cost currency.</span></span> <span data-ttu-id="c5512-152">Jika tidak ada konfigurasi biaya per unit untuk kombinasi produk dan konfigurasi unit dalam daftar harga, maka biaya unit akan diatur default ke 0,00.</span><span class="sxs-lookup"><span data-stu-id="c5512-152">If there is no set up of unit cost for the combination of the product and unit setup in the price list, the unit cost will default to 0.00.</span></span> |
| <span data-ttu-id="c5512-153">Harga Unit</span><span class="sxs-lookup"><span data-stu-id="c5512-153">Unit Price</span></span> | <span data-ttu-id="c5512-154">Harga produk dan kombinasi unit yang dipilih sebagaimana diatur dalam daftar harga penjualan yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="c5512-154">The price of the selected product and unit combination as set up in the applicable sales price list.</span></span> | <span data-ttu-id="c5512-155">Harga per unit selalu ditampilkan dalam mata uang penjualan proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-155">The unit price is always shown in the project's sales currency.</span></span> <span data-ttu-id="c5512-156">Jika tidak ada konfigurasi harga per unit untuk kombinasi produk dan konfigurasi unit dalam daftar harga, maka harga per unit akan diatur default ke 0,00.</span><span class="sxs-lookup"><span data-stu-id="c5512-156">If there is no setup of unit price  for the combination of the product and unit setup in the price list, then unit price will default to 0.00.</span></span>|
| <span data-ttu-id="c5512-157">Biaya Total</span><span class="sxs-lookup"><span data-stu-id="c5512-157">Total Cost</span></span> | <span data-ttu-id="c5512-158">Jumlah biaya yang dihitung sebagai kuantitas \* biaya per unit.</span><span class="sxs-lookup"><span data-stu-id="c5512-158">The cost amount that is calculated as quantity \* unit cost.</span></span>| <span data-ttu-id="c5512-159">Jumlah Biaya selalu ditampilkan dalam mata uang biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-159">The cost amount is always shown in the project's cost currency.</span></span> |
| <span data-ttu-id="c5512-160">Penjualan Total</span><span class="sxs-lookup"><span data-stu-id="c5512-160">Total Sales</span></span> | <span data-ttu-id="c5512-161">Jumlah penjualan yang dihitung sebagai kuantitas \* harga per unit.</span><span class="sxs-lookup"><span data-stu-id="c5512-161">The sales amount that is calculated as quantity \* unit price.</span></span> | <span data-ttu-id="c5512-162">Jumlah penjualan selalu ditampilkan dalam mata uang penjualan proyek.</span><span class="sxs-lookup"><span data-stu-id="c5512-162">The sales amount is always shown in the project's sales currency.</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
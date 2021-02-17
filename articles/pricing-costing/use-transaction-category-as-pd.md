---
title: Menggunakan Kategori Transaksi sebagai dimensi harga
description: Topik ini berisi informasi tentang cara menggunakan bidang Kategori Transaksi sebagai dimensi harga.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513994"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="717c5-103">Menggunakan Kategori Transaksi sebagai dimensi harga</span><span class="sxs-lookup"><span data-stu-id="717c5-103">Use Transaction Category as a pricing dimension</span></span>


<span data-ttu-id="717c5-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="717c5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="717c5-105">Topik ini menjelaskan cara menggunakan bidang **Kategori Transaksi** sebagai dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="717c5-105">This topic explains how to use the **Transaction Category** field as a pricing dimension.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="717c5-106">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="717c5-106">Prerequisites</span></span>
<span data-ttu-id="717c5-107">Sebelum menyelesaikan prosedur di topik ini, Anda harus memiliki solusi dimensi harga baru untuk organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="717c5-107">Before you complete the procedures in this topic, you must have a new pricing dimension solution for your organization.</span></span> <span data-ttu-id="717c5-108">Jika Anda belum membuatnya, lihat [Membuat bidang dan entitas kustom sebagai dimensi harga](create-custom-fields-entities-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="717c5-108">If you haven't already created one, see [Create custom fields and entities as pricing dimensions](create-custom-fields-entities-pricing-dimensions.md).</span></span>

## <a name="add-the-transaction-category-field-to-forms-and-views"></a><span data-ttu-id="717c5-109">Menambahkan bidang Kategori Transaksi ke formulir dan tampilan</span><span class="sxs-lookup"><span data-stu-id="717c5-109">Add the Transaction Category field to forms and views</span></span>
<span data-ttu-id="717c5-110">Agar bidang **Kategori Transaksi** terlihat di solusi dimensi harga, Anda harus menambahkan bidang ke semua formulir dan tampilan sebagai entitas.</span><span class="sxs-lookup"><span data-stu-id="717c5-110">To make the **Transaction Category** field visible in the pricing dimension solution, you need to add the field to all the forms and views as an entity.</span></span>

<span data-ttu-id="717c5-111">Tabel berikut mencantumkan semua formulir dan tampilan siap pakai, berdasarkan entitas.</span><span class="sxs-lookup"><span data-stu-id="717c5-111">The following table lists all of the out-of-the box forms and views, by entity.</span></span> <span data-ttu-id="717c5-112">Anda juga harus menambahkan bidang baru pada formulir atau tampilan tambahan di entitas yang disesuaikan.</span><span class="sxs-lookup"><span data-stu-id="717c5-112">You will also need to add the new field to any additional forms or views in your customized entities.</span></span>

|  <span data-ttu-id="717c5-113">Entity</span><span class="sxs-lookup"><span data-stu-id="717c5-113">Entity</span></span>        | <span data-ttu-id="717c5-114">Formlir</span><span class="sxs-lookup"><span data-stu-id="717c5-114">Forms</span></span>     |<span data-ttu-id="717c5-115">Tampilan</span><span class="sxs-lookup"><span data-stu-id="717c5-115">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="717c5-116">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="717c5-116">Role Price</span></span>| <span data-ttu-id="717c5-117">Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-117">Information</span></span> |<span data-ttu-id="717c5-118">- Harga Kategori Sumber Daya Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-118">- Active Resource Category Prices</span></span><br> <span data-ttu-id="717c5-119">- Terkait Harga Kategori Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="717c5-119">- Resource Category Price Associated</span></span> |
|  <span data-ttu-id="717c5-120">Markup Harga Peran</span><span class="sxs-lookup"><span data-stu-id="717c5-120">Role Price Markup</span></span>| <span data-ttu-id="717c5-121">Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-121">Information</span></span>|<span data-ttu-id="717c5-122">- Markup Harga Peran Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-122">- Active Role Price Markup</span></span><br><span data-ttu-id="717c5-123">- Terkait Markup Harga Peran</span><span class="sxs-lookup"><span data-stu-id="717c5-123">- Role Price Markup Associated</span></span> |
|  <span data-ttu-id="717c5-124">Rincian Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="717c5-124">Quote Line Detail</span></span>|<span data-ttu-id="717c5-125">- Informasi Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-125">- Project Information</span></span><br><span data-ttu-id="717c5-126">- Pembuatan Cepat Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-126">- Project Quick Create</span></span>| <span data-ttu-id="717c5-127">- Rincian Baris Kuotasi Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-127">- Active Quote Line Detail</span></span><br><span data-ttu-id="717c5-128">- Gabungan Rincian Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="717c5-128">- Combined Quote Line Details</span></span><br><span data-ttu-id="717c5-129">- Terkait Rincian Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="717c5-129">- Quote Line Detail Associated</span></span> |
|  <span data-ttu-id="717c5-130">Rincian Baris Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-130">Project Contract Line Detail</span></span>|<span data-ttu-id="717c5-131">- Informasi Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-131">- Project Information</span></span><br><span data-ttu-id="717c5-132">- Pembuatan Cepat Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-132">- Project Quick Create</span></span>|<span data-ttu-id="717c5-133">- Rincian Baris Kontrak Gabungan</span><span class="sxs-lookup"><span data-stu-id="717c5-133">- Combined Contract Line Details</span></span><br><span data-ttu-id="717c5-134">- Rincian Baris Kontrak Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-134">- Active Contract Line Details</span></span><br><span data-ttu-id="717c5-135">- Terkait Rincian Baris Kontrak</span><span class="sxs-lookup"><span data-stu-id="717c5-135">- Contract Line Detail Associated</span></span> |
|  <span data-ttu-id="717c5-136">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-136">Project Task</span></span>|<span data-ttu-id="717c5-137">- Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-137">- Information</span></span><br><span data-ttu-id="717c5-138">- Formulir Baru</span><span class="sxs-lookup"><span data-stu-id="717c5-138">- New Form</span></span>| &nbsp; |
|  <span data-ttu-id="717c5-139">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-139">Project Team Member</span></span>|<span data-ttu-id="717c5-140">- Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-140">- Information</span></span><br><span data-ttu-id="717c5-141">- Formulir Baru</span><span class="sxs-lookup"><span data-stu-id="717c5-141">- New Form</span></span>|<span data-ttu-id="717c5-142">- Anggota Tim Proyek Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-142">- Active Project Team Members</span></span><br><span data-ttu-id="717c5-143">- Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-143">- Project Team Members</span></span><br><span data-ttu-id="717c5-144">- Terkait Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="717c5-144">- Project Team Members Associated</span></span> |
|  <span data-ttu-id="717c5-145">Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="717c5-145">Time Entry</span></span>|<span data-ttu-id="717c5-146">- Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-146">- Information</span></span><br><span data-ttu-id="717c5-147">- Buat Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="717c5-147">- Create Time Entry</span></span>|<span data-ttu-id="717c5-148">- Entri Waktu Saya Menurut Tanggal</span><span class="sxs-lookup"><span data-stu-id="717c5-148">- My Time Entries By Date</span></span><br><span data-ttu-id="717c5-149">- Entri Waktu Saya untuk Pekan Ini</span><span class="sxs-lookup"><span data-stu-id="717c5-149">- My Time Entries for this Week</span></span><br><span data-ttu-id="717c5-150">- Entri Waktu untuk Persetujuan</span><span class="sxs-lookup"><span data-stu-id="717c5-150">- Time entries for Approval</span></span>|
|  <span data-ttu-id="717c5-151">Lini Jurnal</span><span class="sxs-lookup"><span data-stu-id="717c5-151">Journal Line</span></span>|<span data-ttu-id="717c5-152">- Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-152">- Information</span></span><br><span data-ttu-id="717c5-153">- Buat Cepat</span><span class="sxs-lookup"><span data-stu-id="717c5-153">- Quick Create</span></span>|<span data-ttu-id="717c5-154">- Lini Jurnal Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-154">- Active Journal Lines</span></span><br><span data-ttu-id="717c5-155">- Terkait Lini Jurnal</span><span class="sxs-lookup"><span data-stu-id="717c5-155">- Journal Line Associated</span></span>|
|  <span data-ttu-id="717c5-156">Rincian Baris Faktur</span><span class="sxs-lookup"><span data-stu-id="717c5-156">Invoice Line Detail</span></span>|<span data-ttu-id="717c5-157">- Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-157">- Information</span></span><br><span data-ttu-id="717c5-158">- Buat Cepat</span><span class="sxs-lookup"><span data-stu-id="717c5-158">- Quick Create</span></span>|<span data-ttu-id="717c5-159">- Rincian Baris Faktur Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-159">- Active Invoice Line Details</span></span><br><span data-ttu-id="717c5-160">- Transaksi Faktur Kena Biaya</span><span class="sxs-lookup"><span data-stu-id="717c5-160">- Chargeable Invoice Transactions</span></span><br><span data-ttu-id="717c5-161">- Transaksi Faktur Gratis</span><span class="sxs-lookup"><span data-stu-id="717c5-161">- Complimentary Invoice Transactions</span></span><br><span data-ttu-id="717c5-162">- Terkait Rincian Baris Faktur</span><span class="sxs-lookup"><span data-stu-id="717c5-162">- Invoice Line Detail Associated</span></span> <br><span data-ttu-id="717c5-163">- Transaksi Faktur Tidak Kena Biaya</span><span class="sxs-lookup"><span data-stu-id="717c5-163">- Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="717c5-164">Aktual</span><span class="sxs-lookup"><span data-stu-id="717c5-164">Actual</span></span>|<span data-ttu-id="717c5-165">- Informasi</span><span class="sxs-lookup"><span data-stu-id="717c5-165">- Information</span></span><br><span data-ttu-id="717c5-166">- Aktual Aktif</span><span class="sxs-lookup"><span data-stu-id="717c5-166">- Active Actuals</span></span>| <span data-ttu-id="717c5-167">Aktual Terkait</span><span class="sxs-lookup"><span data-stu-id="717c5-167">Actual Associated</span></span> |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a><span data-ttu-id="717c5-168">Mengonfigurasikan bidang Kategori Transaksi sebagai dimensi harga</span><span class="sxs-lookup"><span data-stu-id="717c5-168">Set up the Transaction Category field as a pricing dimension</span></span>

1. <span data-ttu-id="717c5-169">Buka **Pengaturan** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="717c5-169">Go to **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="717c5-170">Pada halaman **Parameter**, di tab **Dimensi Harga Berbasis Jumlah**, pastikan kisi menampilkan record di entitas **Dimensi Harga**.</span><span class="sxs-lookup"><span data-stu-id="717c5-170">On the **Parameters** page, on the **Amount-Based Pricing Dimensions** tab, verify that the grid shows the records in the **Pricing Dimensions** entity.</span></span>
3. <span data-ttu-id="717c5-171">Tambahkan **Kategori Transaksi** ke daftar ini dan atur bidang **Berlaku untuk Biaya** dan **Berlaku untuk Penjualan** ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="717c5-171">Add **Transaction Category** to this list and set the **Applicable to Cost** and **Applicable to Sale** fields to **Yes**.</span></span>
4. <span data-ttu-id="717c5-172">Di bidang **Jenis Dimensi**, pilih **Berbasis jumlah**, lalu pilih prioritas untuk **Kategori Transaksi** yang terkait dengan biaya dan penjualan.</span><span class="sxs-lookup"><span data-stu-id="717c5-172">In the **Dimension Type** field, select **Amount-based**, and then select the priority for **Transaction Category** as it relates to cost and sales.</span></span>
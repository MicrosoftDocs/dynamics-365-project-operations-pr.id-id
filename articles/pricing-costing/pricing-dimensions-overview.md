---
title: Ikhtisar dimensi harga
description: Topik ini menyediakan informasi tentang dimensi harga di Dynamics 365 Project operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078591"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="6c067-103">Ikhtisar dimensi harga</span><span class="sxs-lookup"><span data-stu-id="6c067-103">Pricing dimensions overview</span></span>

<span data-ttu-id="6c067-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="6c067-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c067-105">Dimensi yang digunakan dalam sumber daya manusia untuk mengatur harga dan biaya jatuh ke dalam dua Kategori:</span><span class="sxs-lookup"><span data-stu-id="6c067-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="6c067-106">Sosial</span><span class="sxs-lookup"><span data-stu-id="6c067-106">People</span></span>
- <span data-ttu-id="6c067-107">Pekerjaan Terencana</span><span class="sxs-lookup"><span data-stu-id="6c067-107">Planned work</span></span>

<span data-ttu-id="6c067-108">Oleh karena itu, ada dua jenis nilai dimensi harga yang tersedia:</span><span class="sxs-lookup"><span data-stu-id="6c067-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="6c067-109">**Rangkaian pilihan** : dimensi yang merupakan enumerasi tetap untuk rangkaian nilai.</span><span class="sxs-lookup"><span data-stu-id="6c067-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="6c067-110">**Nilai berdasarkan entitas** : dimensi yang dapat berupa rangkaian nilai bervariasi.</span><span class="sxs-lookup"><span data-stu-id="6c067-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="6c067-111">Dimensi harga</span><span class="sxs-lookup"><span data-stu-id="6c067-111">Pricing dimensions</span></span>

<span data-ttu-id="6c067-112">Dynamics 365 Project Operations dikirim dengan seperangkat default dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="6c067-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="6c067-113">Anda dapat melihat dimensi harga ini dengan membuka **Project Operations** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="6c067-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="6c067-114">Pada rekaman parameter, pada tab **Dimensi harga berbasis jumlah** , Verifikasikan bahwa peran , **msdyn_resourcecategory** , dan unit organisasi sumber daya, **msdyn_organizationalunit** memiliki bidang **Berlaku untuk penjualan** dan **berlaku untuk biaya** yang ditetapkan ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="6c067-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="6c067-115">Dengan mengaktifkan bidang ini, Anda dapat mengkonfigurasi harga dan biaya untuk setiap peran dan kombinasi unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="6c067-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="6c067-116">Jika Anda perlu harga atau biaya untuk sumber daya menggunakan atribut tambahan, Anda dapat membuat bidang kustom, entitas, dan dimensi.</span><span class="sxs-lookup"><span data-stu-id="6c067-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="6c067-117">Waktu sumber daya manusia</span><span class="sxs-lookup"><span data-stu-id="6c067-117">Pricing human resource time</span></span>
<span data-ttu-id="6c067-118">Bagaimana organisasi menghargai waktu sumber daya manusia sering merupakan pertimbangan strategis penting yang secara langsung mempengaruhi profitabilitas organisasi.</span><span class="sxs-lookup"><span data-stu-id="6c067-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="6c067-119">Bekerja dengan tim keuangan dan pimpinan praktik ketika organisasi Anda siap untuk mengidentifikasi bagaimana cara mengkonfigurasi tagihan dan tarif biaya untuk waktu sumber daya manusia.</span><span class="sxs-lookup"><span data-stu-id="6c067-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="6c067-120">Pertimbangan lain untuk harga mencakup apakah akan menggunakan ulang bidang atau entitas yang tidak memiliki dimensi harga namun berlaku sebagai dimensi harga untuk organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="6c067-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="6c067-121">Bidang seperti **kategori transaksi** ( **msdyn_transactioncategory** ) dan **sumber daya dapat dipesan** ( **bookableresource** ) adalah contoh dimensi kandidat.</span><span class="sxs-lookup"><span data-stu-id="6c067-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="6c067-122">Bayangkan apakah dimensi harga anda harus berupa tabel atau rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="6c067-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="6c067-123">Jika anda memperkirakan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda dapat membuat entitas dan bukan rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="6c067-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="6c067-124">Mengelola rangkaian pilihan, seperti menambah atau menghilangkan nilai, memerlukan admin atau pengembang sedangkan menambahkan baris baru ke tabel dapat dilakukan oleh sebagian besar pengguna.</span><span class="sxs-lookup"><span data-stu-id="6c067-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="6c067-125">Contoh berikut menunjukkan tarif tagihan yang diatur berdasarkan peran dan unit organisasi sumber daya yang dimiliki sumber daya.</span><span class="sxs-lookup"><span data-stu-id="6c067-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="6c067-126">Tarif biaya biasanya didasarkan pada kisaran gaji karyawan dan unit organisasi milik mereka.</span><span class="sxs-lookup"><span data-stu-id="6c067-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="6c067-127">Dalam contoh ini, tabel tingkat tagihan dan tingkat biaya akan terlihat seperti berikut ini.</span><span class="sxs-lookup"><span data-stu-id="6c067-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="6c067-128">**Tarif tagihan sampel**</span><span class="sxs-lookup"><span data-stu-id="6c067-128">**Sample bill rates**</span></span>

| <span data-ttu-id="6c067-129">Peran</span><span class="sxs-lookup"><span data-stu-id="6c067-129">Role</span></span>        | <span data-ttu-id="6c067-130">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="6c067-130">Org Unit</span></span>    |<span data-ttu-id="6c067-131">Unit</span><span class="sxs-lookup"><span data-stu-id="6c067-131">Unit</span></span>      |<span data-ttu-id="6c067-132">Harga</span><span class="sxs-lookup"><span data-stu-id="6c067-132">Price</span></span>      |<span data-ttu-id="6c067-133">Mata Uang</span><span class="sxs-lookup"><span data-stu-id="6c067-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="6c067-134">Pengembang</span><span class="sxs-lookup"><span data-stu-id="6c067-134">Developer</span></span>   | <span data-ttu-id="6c067-135">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="6c067-135">Contoso US</span></span>  |<span data-ttu-id="6c067-136">Hour</span><span class="sxs-lookup"><span data-stu-id="6c067-136">Hour</span></span> | <span data-ttu-id="6c067-137">200</span><span class="sxs-lookup"><span data-stu-id="6c067-137">200</span></span>|<span data-ttu-id="6c067-138">USD</span><span class="sxs-lookup"><span data-stu-id="6c067-138">USD</span></span>     |
| <span data-ttu-id="6c067-139">Pengembang</span><span class="sxs-lookup"><span data-stu-id="6c067-139">Developer</span></span>   | <span data-ttu-id="6c067-140">Aswono India</span><span class="sxs-lookup"><span data-stu-id="6c067-140">Contoso India</span></span> |<span data-ttu-id="6c067-141">Hour</span><span class="sxs-lookup"><span data-stu-id="6c067-141">Hour</span></span>|   <span data-ttu-id="6c067-142">112</span><span class="sxs-lookup"><span data-stu-id="6c067-142">112</span></span>|<span data-ttu-id="6c067-143">USD</span><span class="sxs-lookup"><span data-stu-id="6c067-143">USD</span></span>     |


<span data-ttu-id="6c067-144">**Sampel tarif biaya**</span><span class="sxs-lookup"><span data-stu-id="6c067-144">**Sample cost rates**</span></span>

| <span data-ttu-id="6c067-145">Kisaran gaji</span><span class="sxs-lookup"><span data-stu-id="6c067-145">Salary Band</span></span>     | <span data-ttu-id="6c067-146">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="6c067-146">Org Unit</span></span>    |<span data-ttu-id="6c067-147">Unit</span><span class="sxs-lookup"><span data-stu-id="6c067-147">Unit</span></span>      |<span data-ttu-id="6c067-148">Harga</span><span class="sxs-lookup"><span data-stu-id="6c067-148">Price</span></span>      |<span data-ttu-id="6c067-149">Mata Uang</span><span class="sxs-lookup"><span data-stu-id="6c067-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="6c067-150">Perusahaan saya_Band1</span><span class="sxs-lookup"><span data-stu-id="6c067-150">My company_Band1</span></span> | <span data-ttu-id="6c067-151">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="6c067-151">Contoso US</span></span>  |<span data-ttu-id="6c067-152">Hour</span><span class="sxs-lookup"><span data-stu-id="6c067-152">Hour</span></span> | <span data-ttu-id="6c067-153">145</span><span class="sxs-lookup"><span data-stu-id="6c067-153">145</span></span>|<span data-ttu-id="6c067-154">USD</span><span class="sxs-lookup"><span data-stu-id="6c067-154">USD</span></span>     |
| <span data-ttu-id="6c067-155">Perusahaan saya_Band2</span><span class="sxs-lookup"><span data-stu-id="6c067-155">My company_Band2</span></span> | <span data-ttu-id="6c067-156">Aswono India</span><span class="sxs-lookup"><span data-stu-id="6c067-156">Contoso India</span></span> |<span data-ttu-id="6c067-157">Hour</span><span class="sxs-lookup"><span data-stu-id="6c067-157">Hour</span></span>|   <span data-ttu-id="6c067-158">67</span><span class="sxs-lookup"><span data-stu-id="6c067-158">67</span></span>|<span data-ttu-id="6c067-159">USD</span><span class="sxs-lookup"><span data-stu-id="6c067-159">USD</span></span>     |

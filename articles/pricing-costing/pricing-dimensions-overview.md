---
title: Ikhtisar dimensi harga
description: Topik ini memberikan informasi tentang dimensi harga di Dynamics 365 Project Operations.
author: rumant
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: e8d62dcf9975e5427926210a881dec2c256f1b8b
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368480"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="68bf3-103">Ikhtisar dimensi harga</span><span class="sxs-lookup"><span data-stu-id="68bf3-103">Pricing dimensions overview</span></span>

<span data-ttu-id="68bf3-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="68bf3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="68bf3-105">Dimensi yang digunakan dalam sumber daya manusia untuk mengatur harga dan biaya jatuh ke dalam dua Kategori:</span><span class="sxs-lookup"><span data-stu-id="68bf3-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="68bf3-106">Sosial</span><span class="sxs-lookup"><span data-stu-id="68bf3-106">People</span></span>
- <span data-ttu-id="68bf3-107">Pekerjaan Terencana</span><span class="sxs-lookup"><span data-stu-id="68bf3-107">Planned work</span></span>

<span data-ttu-id="68bf3-108">Oleh karena itu, ada dua jenis nilai dimensi harga yang tersedia:</span><span class="sxs-lookup"><span data-stu-id="68bf3-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="68bf3-109">**Rangkaian pilihan**: dimensi yang merupakan enumerasi tetap untuk rangkaian nilai.</span><span class="sxs-lookup"><span data-stu-id="68bf3-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="68bf3-110">**Nilai berdasarkan entitas**: dimensi yang dapat berupa rangkaian nilai bervariasi.</span><span class="sxs-lookup"><span data-stu-id="68bf3-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="68bf3-111">Dimensi harga</span><span class="sxs-lookup"><span data-stu-id="68bf3-111">Pricing dimensions</span></span>

<span data-ttu-id="68bf3-112">Dynamics 365 Project Operations dikirim dengan seperangkat dimensi harga default.</span><span class="sxs-lookup"><span data-stu-id="68bf3-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="68bf3-113">Anda dapat melihat dimensi harga ini dengan membuka **Project Operations** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="68bf3-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="68bf3-114">Pada rekaman parameter, pada tab **Dimensi harga berbasis jumlah**, Verifikasikan bahwa peran , **msdyn_resourcecategory**, dan unit organisasi sumber daya, **msdyn_organizationalunit** memiliki bidang **Berlaku untuk penjualan** dan **berlaku untuk biaya** yang ditetapkan ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="68bf3-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="68bf3-115">Dengan mengaktifkan bidang ini, Anda dapat mengkonfigurasi harga dan biaya untuk setiap peran dan kombinasi unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="68bf3-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Tangkapan layar dari parameter Project Service dengan "berlaku for penjualan" disorot](media/PS-OOB-parameters.png)

<span data-ttu-id="68bf3-117">Jika Anda perlu harga atau biaya untuk sumber daya menggunakan atribut tambahan, Anda dapat membuat bidang kustom, entitas, dan dimensi.</span><span class="sxs-lookup"><span data-stu-id="68bf3-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="68bf3-118">Untuk informasi lebih lanjut, lihat topik berikut.</span><span class="sxs-lookup"><span data-stu-id="68bf3-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="68bf3-119">Prosedur harus diselesaikan dalam urutan sebagaimana tercantum.</span><span class="sxs-lookup"><span data-stu-id="68bf3-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="68bf3-120">Membuat solusi untuk dimensi harga kustom</span><span class="sxs-lookup"><span data-stu-id="68bf3-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="68bf3-121">Membuat bidang dan entitas kustom</span><span class="sxs-lookup"><span data-stu-id="68bf3-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="68bf3-122">Menambahkan bidang kustom ke pengaturan harga dan entitas transaksi </span><span class="sxs-lookup"><span data-stu-id="68bf3-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="68bf3-123">Mengonfigurasikan bidang kustom sebagai dimensi harga </span><span class="sxs-lookup"><span data-stu-id="68bf3-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="68bf3-124">Perbarui atribut plug-in untuk menyertakan dimensi harga baru</span><span class="sxs-lookup"><span data-stu-id="68bf3-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="68bf3-125">Waktu sumber daya manusia</span><span class="sxs-lookup"><span data-stu-id="68bf3-125">Pricing human resource time</span></span>
<span data-ttu-id="68bf3-126">Bagaimana organisasi menghargai waktu sumber daya manusia sering merupakan pertimbangan strategis penting yang secara langsung mempengaruhi profitabilitas organisasi.</span><span class="sxs-lookup"><span data-stu-id="68bf3-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="68bf3-127">Bekerja dengan tim keuangan dan pimpinan praktik ketika organisasi Anda siap untuk mengidentifikasi bagaimana cara mengkonfigurasi tagihan dan tarif biaya untuk waktu sumber daya manusia.</span><span class="sxs-lookup"><span data-stu-id="68bf3-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="68bf3-128">Pertimbangan lain untuk harga mencakup apakah akan menggunakan ulang bidang atau entitas yang tidak memiliki dimensi harga namun berlaku sebagai dimensi harga untuk organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="68bf3-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="68bf3-129">Bidang seperti **kategori transaksi** (**msdyn_transactioncategory**) dan **sumber daya dapat dipesan** (**bookableresource**) adalah contoh dimensi kandidat.</span><span class="sxs-lookup"><span data-stu-id="68bf3-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="68bf3-130">Bayangkan apakah dimensi harga anda harus berupa tabel atau rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="68bf3-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="68bf3-131">Jika anda memperkirakan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, anda dapat membuat entitas dan bukan rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="68bf3-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="68bf3-132">Mengelola rangkaian pilihan, seperti menambah atau menghilangkan nilai, memerlukan admin atau pengembang sedangkan menambahkan baris baru ke tabel dapat dilakukan oleh sebagian besar pengguna.</span><span class="sxs-lookup"><span data-stu-id="68bf3-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="68bf3-133">Contoh berikut menunjukkan tarif tagihan yang diatur berdasarkan peran dan unit organisasi sumber daya yang dimiliki sumber daya.</span><span class="sxs-lookup"><span data-stu-id="68bf3-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="68bf3-134">Tarif biaya biasanya didasarkan pada kisaran gaji karyawan dan unit organisasi milik mereka.</span><span class="sxs-lookup"><span data-stu-id="68bf3-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="68bf3-135">Dalam contoh ini, tabel tingkat tagihan dan tingkat biaya akan terlihat seperti berikut ini.</span><span class="sxs-lookup"><span data-stu-id="68bf3-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="68bf3-136">**Tarif tagihan sampel**</span><span class="sxs-lookup"><span data-stu-id="68bf3-136">**Sample bill rates**</span></span>

| <span data-ttu-id="68bf3-137">Peran</span><span class="sxs-lookup"><span data-stu-id="68bf3-137">Role</span></span>        | <span data-ttu-id="68bf3-138">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="68bf3-138">Org Unit</span></span>    |<span data-ttu-id="68bf3-139">Unit</span><span class="sxs-lookup"><span data-stu-id="68bf3-139">Unit</span></span>      |<span data-ttu-id="68bf3-140">Harga</span><span class="sxs-lookup"><span data-stu-id="68bf3-140">Price</span></span>      |<span data-ttu-id="68bf3-141">Mata uang</span><span class="sxs-lookup"><span data-stu-id="68bf3-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="68bf3-142">Pengembang</span><span class="sxs-lookup"><span data-stu-id="68bf3-142">Developer</span></span>   | <span data-ttu-id="68bf3-143">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="68bf3-143">Contoso US</span></span>  |<span data-ttu-id="68bf3-144">Jam</span><span class="sxs-lookup"><span data-stu-id="68bf3-144">Hour</span></span> | <span data-ttu-id="68bf3-145">200</span><span class="sxs-lookup"><span data-stu-id="68bf3-145">200</span></span>|<span data-ttu-id="68bf3-146">USD</span><span class="sxs-lookup"><span data-stu-id="68bf3-146">USD</span></span>     |
| <span data-ttu-id="68bf3-147">Pengembang</span><span class="sxs-lookup"><span data-stu-id="68bf3-147">Developer</span></span>   | <span data-ttu-id="68bf3-148">Contoso India</span><span class="sxs-lookup"><span data-stu-id="68bf3-148">Contoso India</span></span> |<span data-ttu-id="68bf3-149">Jam</span><span class="sxs-lookup"><span data-stu-id="68bf3-149">Hour</span></span>|   <span data-ttu-id="68bf3-150">112</span><span class="sxs-lookup"><span data-stu-id="68bf3-150">112</span></span>|<span data-ttu-id="68bf3-151">USD</span><span class="sxs-lookup"><span data-stu-id="68bf3-151">USD</span></span>     |


<span data-ttu-id="68bf3-152">**Sampel tarif biaya**</span><span class="sxs-lookup"><span data-stu-id="68bf3-152">**Sample cost rates**</span></span>

| <span data-ttu-id="68bf3-153">Kisaran gaji</span><span class="sxs-lookup"><span data-stu-id="68bf3-153">Salary Band</span></span>     | <span data-ttu-id="68bf3-154">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="68bf3-154">Org Unit</span></span>    |<span data-ttu-id="68bf3-155">Unit</span><span class="sxs-lookup"><span data-stu-id="68bf3-155">Unit</span></span>      |<span data-ttu-id="68bf3-156">Harga</span><span class="sxs-lookup"><span data-stu-id="68bf3-156">Price</span></span>      |<span data-ttu-id="68bf3-157">Mata uang</span><span class="sxs-lookup"><span data-stu-id="68bf3-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="68bf3-158">Perusahaan saya_Band1</span><span class="sxs-lookup"><span data-stu-id="68bf3-158">My company_Band1</span></span> | <span data-ttu-id="68bf3-159">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="68bf3-159">Contoso US</span></span>  |<span data-ttu-id="68bf3-160">Jam</span><span class="sxs-lookup"><span data-stu-id="68bf3-160">Hour</span></span> | <span data-ttu-id="68bf3-161">145</span><span class="sxs-lookup"><span data-stu-id="68bf3-161">145</span></span>|<span data-ttu-id="68bf3-162">USD</span><span class="sxs-lookup"><span data-stu-id="68bf3-162">USD</span></span>     |
| <span data-ttu-id="68bf3-163">Perusahaan saya_Band2</span><span class="sxs-lookup"><span data-stu-id="68bf3-163">My company_Band2</span></span> | <span data-ttu-id="68bf3-164">Contoso India</span><span class="sxs-lookup"><span data-stu-id="68bf3-164">Contoso India</span></span> |<span data-ttu-id="68bf3-165">Jam</span><span class="sxs-lookup"><span data-stu-id="68bf3-165">Hour</span></span>|   <span data-ttu-id="68bf3-166">67</span><span class="sxs-lookup"><span data-stu-id="68bf3-166">67</span></span>|<span data-ttu-id="68bf3-167">USD</span><span class="sxs-lookup"><span data-stu-id="68bf3-167">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
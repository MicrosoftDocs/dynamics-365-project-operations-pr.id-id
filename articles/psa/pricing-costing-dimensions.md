---
title: Laman beranda harga dan dimensi biaya
description: Topik ini memberikan ikhtisar tentang dimensi harga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 65516784c6787fa5f3c08297f4d161d52c2ea4a9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151302"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="b9780-103">Laman beranda harga dan dimensi biaya</span><span class="sxs-lookup"><span data-stu-id="b9780-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b9780-104">Dimensi yang digunakan untuk menetapkan harga tenaga kerja dan penetapan biaya dalam organisasi berbasis proyek dipengaruhi oleh atribut berikut:</span><span class="sxs-lookup"><span data-stu-id="b9780-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="b9780-105">Orang yang bekerja sama dengan pengalaman, peran, atau geografi mereka</span><span class="sxs-lookup"><span data-stu-id="b9780-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="b9780-106">Pekerjaan yang akan dilakukan mirip dalam hal kompleksitas atau waktu dalam sehari</span><span class="sxs-lookup"><span data-stu-id="b9780-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="b9780-107">Mengingat sifat umum atribut ini dari pekerjaan dan orang-orang yang diperlukan untuk melakukan pekerjaan, ada dua jenis nilai dimensi harga yang tersedia di Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="b9780-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="b9780-108">**Rangkaian pilihan** - Atribut yang merupakan enumerasi tetap untuk rangkaian nilai.</span><span class="sxs-lookup"><span data-stu-id="b9780-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="b9780-109">**Nilai berdasarkan entitas** -atribut yang dapat memiliki rangkaian nilai bervariasi yang terbatas namun dapat berubah seiring waktu.</span><span class="sxs-lookup"><span data-stu-id="b9780-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="b9780-110">Dimensi harga</span><span class="sxs-lookup"><span data-stu-id="b9780-110">Pricing dimensions</span></span>

<span data-ttu-id="b9780-111">PSA dikirim dengan seperangkat dimensi harga default.</span><span class="sxs-lookup"><span data-stu-id="b9780-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="b9780-112">Anda dapat melihat ini dengan membuka **Project Service** > **Parameter**.</span><span class="sxs-lookup"><span data-stu-id="b9780-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="b9780-113">Pada rekaman parameter, pada tab **Dimensi harga berbasis jumlah**, Verifikasikan bahwa peran , **msdyn_resourcecategory**, dan unit organisasi sumber daya, **msdyn_organizationalunit** memiliki bidang **Berlaku untuk penjualan** dan **berlaku untuk biaya** yang ditetapkan ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="b9780-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="b9780-114">Ini akan memungkinkan Anda mengkonfigurasi harga dan biaya untuk setiap peran dan kombinasi unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="b9780-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Tangkapan layar dari parameter Project Service dengan "berlaku for penjualan" disorot](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="b9780-116">Jika Anda telah menggunakan bidang bawaan peran dan unit organisasi sebagai dimensi harga sebelum versi 3 dari PSA, tidak akan ada perubahan yang dapat diamati.</span><span class="sxs-lookup"><span data-stu-id="b9780-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="b9780-117">Anda dapat terus menggunakan project service seperti biasa.</span><span class="sxs-lookup"><span data-stu-id="b9780-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="b9780-118">Jika Anda perlu harga atau biaya untuk sumber daya menggunakan atribut tambahan, Anda dapat membuat bidang kustom, entitas, dan dimensi.</span><span class="sxs-lookup"><span data-stu-id="b9780-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="b9780-119">Untuk informasi lebih lanjut, lihat topik berikut, Namun perhatikan bahwa Anda harus menyelesaikan prosedur dalam urutan yang tercantum di bawah ini:</span><span class="sxs-lookup"><span data-stu-id="b9780-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="b9780-120">Membuat bidang dan entitas kustom</span><span class="sxs-lookup"><span data-stu-id="b9780-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="b9780-121">Menambahkan bidang kustom ke pengaturan harga dan entitas transaksi</span><span class="sxs-lookup"><span data-stu-id="b9780-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="b9780-122">Mengonfigurasikan bidang kustom sebagai dimensi harga </span><span class="sxs-lookup"><span data-stu-id="b9780-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="b9780-123">Perbarui atribut plug-in untuk menyertakan dimensi harga baru</span><span class="sxs-lookup"><span data-stu-id="b9780-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="b9780-124">Waktu sumber daya manusia</span><span class="sxs-lookup"><span data-stu-id="b9780-124">Pricing human resource time</span></span>
<span data-ttu-id="b9780-125">Bagaimana organisasi menghargai waktu sumber daya manusia sering merupakan pertimbangan strategis penting yang secara langsung mempengaruhi profitabilitas organisasi.</span><span class="sxs-lookup"><span data-stu-id="b9780-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="b9780-126">Bekerja dengan tim keuangan dan pimpinan praktik ketika organisasi Anda siap untuk mengidentifikasi bagaimana cara mengkonfigurasi tagihan dan tarif biaya untuk waktu sumber daya manusia.</span><span class="sxs-lookup"><span data-stu-id="b9780-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="b9780-127">Pertimbangan lain untuk harga mencakup apakah akan menggunakan ulang bidang atau entitas yang tidak memiliki dimensi harga namun berlaku sebagai dimensi harga untuk organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="b9780-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="b9780-128">Bidang seperti **kategori transaksi** (**msdyn_transactioncategory**) dan **sumber daya dapat dipesan** (**bookableresource**) adalah contoh dimensi kandidat.</span><span class="sxs-lookup"><span data-stu-id="b9780-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="b9780-129">Bayangkan apakah dimensi harga anda harus berupa tabel atau rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="b9780-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="b9780-130">Jika anda memperkirakan perubahan pada nilai dimensi yang akan melebihi 10 atau 12 dan anda memerlukan atribut tambahan pada nilai ini, buat entitas dan bukan rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="b9780-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="b9780-131">Mengelola rangkaian pilihan, seperti menambah atau menghilangkan nilai, memerlukan admin atau pengembang sedangkan menambahkan baris baru ke tabel dapat dilakukan oleh sebagian besar pengguna bisnis.</span><span class="sxs-lookup"><span data-stu-id="b9780-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="b9780-132">Contoh berikut menunjukkan tarif tagihan yang diatur berdasarkan peran dan unit organisasi sumber daya yang dimiliki sumber daya.</span><span class="sxs-lookup"><span data-stu-id="b9780-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="b9780-133">Tarif biaya biasanya didasarkan pada kisaran gaji karyawan dan unit organisasi milik mereka.</span><span class="sxs-lookup"><span data-stu-id="b9780-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="b9780-134">Dalam contoh ini, tabel tingkat tagihan dan tingkat biaya akan terlihat seperti berikut ini.</span><span class="sxs-lookup"><span data-stu-id="b9780-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="b9780-135">**Tarif tagihan sampel**</span><span class="sxs-lookup"><span data-stu-id="b9780-135">**Sample bill rates**</span></span>

| <span data-ttu-id="b9780-136">Peran</span><span class="sxs-lookup"><span data-stu-id="b9780-136">Role</span></span>        | <span data-ttu-id="b9780-137">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="b9780-137">Org Unit</span></span>    |<span data-ttu-id="b9780-138">Unit</span><span class="sxs-lookup"><span data-stu-id="b9780-138">Unit</span></span>      |<span data-ttu-id="b9780-139">Harga</span><span class="sxs-lookup"><span data-stu-id="b9780-139">Price</span></span>      |<span data-ttu-id="b9780-140">Mata Uang</span><span class="sxs-lookup"><span data-stu-id="b9780-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="b9780-141">Pengembang</span><span class="sxs-lookup"><span data-stu-id="b9780-141">Developer</span></span>   | <span data-ttu-id="b9780-142">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="b9780-142">Contoso US</span></span>  |<span data-ttu-id="b9780-143">Hour</span><span class="sxs-lookup"><span data-stu-id="b9780-143">Hour</span></span> | <span data-ttu-id="b9780-144">200</span><span class="sxs-lookup"><span data-stu-id="b9780-144">200</span></span>|<span data-ttu-id="b9780-145">USD</span><span class="sxs-lookup"><span data-stu-id="b9780-145">USD</span></span>     |
| <span data-ttu-id="b9780-146">Pengembang</span><span class="sxs-lookup"><span data-stu-id="b9780-146">Developer</span></span>   | <span data-ttu-id="b9780-147">Aswono India</span><span class="sxs-lookup"><span data-stu-id="b9780-147">Contoso India</span></span> |<span data-ttu-id="b9780-148">Hour</span><span class="sxs-lookup"><span data-stu-id="b9780-148">Hour</span></span>|   <span data-ttu-id="b9780-149">112</span><span class="sxs-lookup"><span data-stu-id="b9780-149">112</span></span>|<span data-ttu-id="b9780-150">USD</span><span class="sxs-lookup"><span data-stu-id="b9780-150">USD</span></span>     |


<span data-ttu-id="b9780-151">**Sampel tarif biaya**</span><span class="sxs-lookup"><span data-stu-id="b9780-151">**Sample cost rates**</span></span>

| <span data-ttu-id="b9780-152">Kisaran gaji</span><span class="sxs-lookup"><span data-stu-id="b9780-152">Salary Band</span></span>     | <span data-ttu-id="b9780-153">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="b9780-153">Org Unit</span></span>    |<span data-ttu-id="b9780-154">Unit</span><span class="sxs-lookup"><span data-stu-id="b9780-154">Unit</span></span>      |<span data-ttu-id="b9780-155">Harga</span><span class="sxs-lookup"><span data-stu-id="b9780-155">Price</span></span>      |<span data-ttu-id="b9780-156">Mata Uang</span><span class="sxs-lookup"><span data-stu-id="b9780-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="b9780-157">Perusahaan saya_Band1</span><span class="sxs-lookup"><span data-stu-id="b9780-157">My company_Band1</span></span> | <span data-ttu-id="b9780-158">Contoso AS</span><span class="sxs-lookup"><span data-stu-id="b9780-158">Contoso US</span></span>  |<span data-ttu-id="b9780-159">Hour</span><span class="sxs-lookup"><span data-stu-id="b9780-159">Hour</span></span> | <span data-ttu-id="b9780-160">145</span><span class="sxs-lookup"><span data-stu-id="b9780-160">145</span></span>|<span data-ttu-id="b9780-161">USD</span><span class="sxs-lookup"><span data-stu-id="b9780-161">USD</span></span>     |
| <span data-ttu-id="b9780-162">Perusahaan saya_Band2</span><span class="sxs-lookup"><span data-stu-id="b9780-162">My company_Band2</span></span> | <span data-ttu-id="b9780-163">Aswono India</span><span class="sxs-lookup"><span data-stu-id="b9780-163">Contoso India</span></span> |<span data-ttu-id="b9780-164">Hour</span><span class="sxs-lookup"><span data-stu-id="b9780-164">Hour</span></span>|   <span data-ttu-id="b9780-165">67</span><span class="sxs-lookup"><span data-stu-id="b9780-165">67</span></span>|<span data-ttu-id="b9780-166">USD</span><span class="sxs-lookup"><span data-stu-id="b9780-166">USD</span></span>     |

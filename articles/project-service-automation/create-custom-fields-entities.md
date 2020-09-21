---
title: Membuat bidang dan entitas kustom
description: Topik ini menjelaskan cara membuat rangkaian pilihan dan entitas dalam solusi anda sendiri di platform Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752501"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="19a66-103">Membuat bidang dan entitas kustom</span><span class="sxs-lookup"><span data-stu-id="19a66-103">Create custom fields and entities</span></span> 

<span data-ttu-id="19a66-104">Selesaikan langkah-langkah berikut saat anda ingin membuat rangkaian pilihan kustom atau entitas pada platform Power Apps.</span><span class="sxs-lookup"><span data-stu-id="19a66-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="19a66-105">Prosedur dalam topik ini harus diselesaikan menggunakan antarmuka web dari Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="19a66-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="19a66-106">Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah.</span><span class="sxs-lookup"><span data-stu-id="19a66-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="19a66-107">Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya.</span><span class="sxs-lookup"><span data-stu-id="19a66-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="19a66-108">Setelah anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.</span><span class="sxs-lookup"><span data-stu-id="19a66-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="19a66-109">Membuat solusi kustom untuk dimensi harga</span><span class="sxs-lookup"><span data-stu-id="19a66-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="19a66-110">Dalam PSA, klik **pengaturan** > **solusi**, lalu klik **baru** untuk membuat solusi baru.</span><span class="sxs-lookup"><span data-stu-id="19a66-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="19a66-111">Namai solusi, **\<nama organisasi Anda >dimensi harga**, masukkan informasi yang diperlukan lainnya, lalu klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="19a66-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Membuat solusi kustom untuk dimensi harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="19a66-113">Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="19a66-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="19a66-114">Dimensi harga dapat berupa rangkaian pilihan atau entitas.</span><span class="sxs-lookup"><span data-stu-id="19a66-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="19a66-115">Keduanya harus dibuat dalam solusi harga.</span><span class="sxs-lookup"><span data-stu-id="19a66-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="19a66-116">Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="19a66-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="19a66-117">Dimensi berdasarkan entitas</span><span class="sxs-lookup"><span data-stu-id="19a66-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="19a66-118">Dalam PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **\<nama organisasi > dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="19a66-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="19a66-119">Di penelusur solusi, di panel navigasi kiri, pilih **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="19a66-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="19a66-120">Klik **baru** untuk membuat entitas baru yang disebut **judul standar**.</span><span class="sxs-lookup"><span data-stu-id="19a66-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="19a66-121">Masukkan informasi tersisa yang diperlukan dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="19a66-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definisi entitas judul standar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="19a66-123">Dimensi berbasis rangkaian pilihan</span><span class="sxs-lookup"><span data-stu-id="19a66-123">Option set-based dimensions</span></span> 
<span data-ttu-id="19a66-124">Anda dapat membuat dua dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="19a66-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="19a66-125">Gunakan **lokasi kerja sumber daya** untuk melacak harga lokasi kerja **Awal** dan pekerjaan **di lokasi** serta gunakan **jam kerja sumber daya** dengan nilai **reguler** dan **lembur** untuk menerapkan markup saat pekerjaan selesai.</span><span class="sxs-lookup"><span data-stu-id="19a66-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="19a66-126">Dalam PSA, klik **pengaturan** > **solusi**, lalu klik dua kali  **\<nama organisasi > dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="19a66-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="19a66-127">Di penelusur solusi, di panel navigasi kiri, pilih  **rangkaian pilihan**.</span><span class="sxs-lookup"><span data-stu-id="19a66-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="19a66-128">Klik **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu klik **simpan**.</span><span class="sxs-lookup"><span data-stu-id="19a66-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="19a66-129">Dimensi harga berdasarkan rangkaian pilihan disebut lokasi kerja sumber daya</span><span class="sxs-lookup"><span data-stu-id="19a66-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="19a66-130">Dimensi harga berdasarkan rangkaian pilihan disebut jam kerja sumber daya</span><span class="sxs-lookup"><span data-stu-id="19a66-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="19a66-131">Membuat data untuk dimensi berbasis entitas</span><span class="sxs-lookup"><span data-stu-id="19a66-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="19a66-132">Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan.</span><span class="sxs-lookup"><span data-stu-id="19a66-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="19a66-133">Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**.</span><span class="sxs-lookup"><span data-stu-id="19a66-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="19a66-134">Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.</span><span class="sxs-lookup"><span data-stu-id="19a66-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="19a66-135">Di PSA, Klik **Pencarian Tingkat Lanjut**.</span><span class="sxs-lookup"><span data-stu-id="19a66-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="19a66-136">Pilih entitas **judul standar**, lalu klik **hasil**.</span><span class="sxs-lookup"><span data-stu-id="19a66-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="19a66-137">Semua baris di entitas **judul standar** akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="19a66-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="19a66-138">Klik **Baru**.</span><span class="sxs-lookup"><span data-stu-id="19a66-138">Click **New**.</span></span> <span data-ttu-id="19a66-139">Di bidang **Nama**, masukkan "Systems Engineer", lalu klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="19a66-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="19a66-140">Tutup formulir.</span><span class="sxs-lookup"><span data-stu-id="19a66-140">Close the form.</span></span> 
4. <span data-ttu-id="19a66-141">Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".</span><span class="sxs-lookup"><span data-stu-id="19a66-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="19a66-142">Data sampel untuk entitas judul standar</span><span class="sxs-lookup"><span data-stu-id="19a66-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="19a66-143">Tambahkan semua entitas PSA yang diperlukan dan komponen terkait ke solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="19a66-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="19a66-144">Anda harus menambahkan entitas Project Service berikut ke solusi harga.</span><span class="sxs-lookup"><span data-stu-id="19a66-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="19a66-145">Gunakan langkah-langkah dalam prosedur ini untuk membuat beberapa perubahan skema penting dalam solusi harga sehingga entitas mengetahui dimensi harga baru.</span><span class="sxs-lookup"><span data-stu-id="19a66-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="19a66-146">Dalam PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **\<nama organisasi > dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="19a66-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="19a66-147">Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="19a66-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="19a66-148">Di kotak dialog **komponen solusi**, pilih entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="19a66-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="19a66-149">Aktual</span><span class="sxs-lookup"><span data-stu-id="19a66-149">Actual</span></span>
- <span data-ttu-id="19a66-150">Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="19a66-150">Bookable Resource</span></span>
- <span data-ttu-id="19a66-151">Baris Perkiraan</span><span class="sxs-lookup"><span data-stu-id="19a66-151">Estimate Line</span></span>
- <span data-ttu-id="19a66-152">Rincian Baris Faktur</span><span class="sxs-lookup"><span data-stu-id="19a66-152">Invoice Line Detail</span></span>
- <span data-ttu-id="19a66-153">Lini Jurnal</span><span class="sxs-lookup"><span data-stu-id="19a66-153">Journal Line</span></span>
- <span data-ttu-id="19a66-154">Rincian Baris Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="19a66-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="19a66-155">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="19a66-155">Project Team Member</span></span>
- <span data-ttu-id="19a66-156">Rincian Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="19a66-156">Quote Line Detail</span></span>
- <span data-ttu-id="19a66-157">Markup Harga Peran</span><span class="sxs-lookup"><span data-stu-id="19a66-157">Role Price Markup</span></span>
- <span data-ttu-id="19a66-158">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="19a66-158">Role Price</span></span> 
- <span data-ttu-id="19a66-159">Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="19a66-159">Time Entry</span></span> 

> ![Menambahkan entitas yang ada ke solusi dimensi harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen solusi](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="19a66-162">Pastikan untuk menyertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="19a66-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="19a66-163">Bila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih di atas, klik **tidak**.</span><span class="sxs-lookup"><span data-stu-id="19a66-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Jangan sertakan semua komponen terkait](media/Do-not-include-required.png)



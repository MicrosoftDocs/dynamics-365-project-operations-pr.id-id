---
title: Membuat entitas dan bidang kustom sebagai dimensi harga
description: Topik ini menyediakan informasi tentang cara membuat rangkaian pilihan kustom atau entitas.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898265"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="4459b-103">Membuat entitas dan bidang kustom sebagai dimensi harga</span><span class="sxs-lookup"><span data-stu-id="4459b-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="4459b-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="4459b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4459b-105">Selesaikan langkah-langkah berikut saat anda ingin membuat rangkaian pilihan kustom atau entitas.</span><span class="sxs-lookup"><span data-stu-id="4459b-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4459b-106">Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah.</span><span class="sxs-lookup"><span data-stu-id="4459b-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="4459b-107">Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya.</span><span class="sxs-lookup"><span data-stu-id="4459b-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="4459b-108">Setelah anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.</span><span class="sxs-lookup"><span data-stu-id="4459b-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="4459b-109">Membuat solusi kustom untuk dimensi harga</span><span class="sxs-lookup"><span data-stu-id="4459b-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="4459b-110">Buka **pengaturan** > **solusi**, lalu pilih **baru** untuk membuat solusi baru.</span><span class="sxs-lookup"><span data-stu-id="4459b-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="4459b-111">Namai solusi, **\<your organization name> dimensi harga**, masukkan informasi yang diperlukan lainnya, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="4459b-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="4459b-112">Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="4459b-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="4459b-113">Dimensi harga dapat berupa rangkaian pilihan atau entitas.</span><span class="sxs-lookup"><span data-stu-id="4459b-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="4459b-114">Keduanya harus dibuat dalam solusi harga.</span><span class="sxs-lookup"><span data-stu-id="4459b-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="4459b-115">Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="4459b-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="4459b-116">Dimensi berdasarkan entitas</span><span class="sxs-lookup"><span data-stu-id="4459b-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="4459b-117">Buka **pengaturan** > **solusi**, lalu klik dua kali **\<your organization name> dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="4459b-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="4459b-118">Di penelusur solusi, di panel navigasi kiri, pilih **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="4459b-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="4459b-119">Pilih **baru** untuk membuat entitas baru yang disebut **judul standar**.</span><span class="sxs-lookup"><span data-stu-id="4459b-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="4459b-120">Masukkan informasi tersisa yang diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="4459b-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="4459b-121">Dimensi berbasis rangkaian pilihan</span><span class="sxs-lookup"><span data-stu-id="4459b-121">Option set-based dimensions</span></span> 
<span data-ttu-id="4459b-122">Anda dapat membuat dua dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="4459b-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="4459b-123">Gunakan **lokasi kerja sumber daya** untuk melacak harga lokasi kerja **Awal** dan pekerjaan **di lokasi** serta gunakan **jam kerja sumber daya** dengan nilai **reguler** dan **lembur** untuk menerapkan markup saat pekerjaan selesai.</span><span class="sxs-lookup"><span data-stu-id="4459b-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="4459b-124">Buka **pengaturan** > **solusi**, dan klik dua kali  **\<your organization name> dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="4459b-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="4459b-125">Di penelusur solusi, di panel navigasi kiri, pilih  **rangkaian pilihan**.</span><span class="sxs-lookup"><span data-stu-id="4459b-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="4459b-126">Pilih **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu pilih **simpan**.</span><span class="sxs-lookup"><span data-stu-id="4459b-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="4459b-127">Membuat data untuk dimensi berbasis entitas</span><span class="sxs-lookup"><span data-stu-id="4459b-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="4459b-128">Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan.</span><span class="sxs-lookup"><span data-stu-id="4459b-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="4459b-129">Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**.</span><span class="sxs-lookup"><span data-stu-id="4459b-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="4459b-130">Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.</span><span class="sxs-lookup"><span data-stu-id="4459b-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="4459b-131">Pilih **pencarian tingkat lanjut**, pilih **judul standar** entitas, lalu pilih **hasil**.</span><span class="sxs-lookup"><span data-stu-id="4459b-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="4459b-132">Semua baris di entitas **judul standar** akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="4459b-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="4459b-133">Pilih **Baru**, Di bidang **Nama**, masukkan "Systems Engineer", lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="4459b-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="4459b-134">Tutup formulir.</span><span class="sxs-lookup"><span data-stu-id="4459b-134">Close the form.</span></span> 
4. <span data-ttu-id="4459b-135">Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".</span><span class="sxs-lookup"><span data-stu-id="4459b-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="4459b-136">Tambahkan semua entitas yang diperlukan dan komponen terkait ke solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="4459b-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="4459b-137">Anda harus menambahkan entitas berikut ke solusi harga.</span><span class="sxs-lookup"><span data-stu-id="4459b-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="4459b-138">Gunakan langkah-langkah dalam prosedur ini untuk membuat beberapa perubahan skema penting dalam solusi harga sehingga entitas mengetahui dimensi harga baru.</span><span class="sxs-lookup"><span data-stu-id="4459b-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="4459b-139">Pilih **pengaturan** > **solusi**, dan klik dua kali **\<your organization name> dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="4459b-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="4459b-140">Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="4459b-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="4459b-141">Di kotak dialog **komponen solusi**, pilih entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="4459b-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="4459b-142">Aktual</span><span class="sxs-lookup"><span data-stu-id="4459b-142">Actual</span></span>
  - <span data-ttu-id="4459b-143">Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="4459b-143">Bookable Resource</span></span>
  - <span data-ttu-id="4459b-144">Baris Perkiraan</span><span class="sxs-lookup"><span data-stu-id="4459b-144">Estimate Line</span></span>
  - <span data-ttu-id="4459b-145">Rincian Baris Faktur</span><span class="sxs-lookup"><span data-stu-id="4459b-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="4459b-146">Lini Jurnal</span><span class="sxs-lookup"><span data-stu-id="4459b-146">Journal Line</span></span>
  - <span data-ttu-id="4459b-147">Rincian Baris Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="4459b-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="4459b-148">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="4459b-148">Project Team Member</span></span>
  - <span data-ttu-id="4459b-149">Detail Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="4459b-149">Quote Line Detail</span></span>
  - <span data-ttu-id="4459b-150">Markup Harga Peran</span><span class="sxs-lookup"><span data-stu-id="4459b-150">Role Price Markup</span></span>
  - <span data-ttu-id="4459b-151">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="4459b-151">Role Price</span></span> 
  - <span data-ttu-id="4459b-152">Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="4459b-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="4459b-153">Pastikan untuk menyertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="4459b-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="4459b-154">Bila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih di atas, pilih **tidak**.</span><span class="sxs-lookup"><span data-stu-id="4459b-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>


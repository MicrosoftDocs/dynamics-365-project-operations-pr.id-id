---
title: Membuat entitas dan bidang kustom sebagai dimensi harga
description: Topik ini menyediakan informasi tentang cara membuat rangkaian pilihan kustom atau entitas.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275632"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="3cc68-103">Membuat entitas dan bidang kustom sebagai dimensi harga</span><span class="sxs-lookup"><span data-stu-id="3cc68-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="3cc68-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="3cc68-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3cc68-105">Lakukan langkah-langkah berikut apabila Anda ingin membuat rangkaian pilihan kustom atau entitas untuk menggunakannya sebagai dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="3cc68-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="3cc68-106">Untuk informasi lebih lanjut, lihat [Ringkasan dimensi harga](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cc68-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3cc68-107">Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah.</span><span class="sxs-lookup"><span data-stu-id="3cc68-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="3cc68-108">Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="3cc68-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="3cc68-109">Hal ini juga akan membantu untuk menggunakan kembali karya Anda dan lebih memudahkan untuk memindahkan perubahan tersebut ke instans lain. Setelah Anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **Solusi terkelola** dan impor ke instans lain untuk menggunakan kembali pengaturan harga Anda.</span><span class="sxs-lookup"><span data-stu-id="3cc68-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="3cc68-110">Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="3cc68-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="3cc68-111">Dimensi harga dapat berupa rangkaian pilihan atau entitas.</span><span class="sxs-lookup"><span data-stu-id="3cc68-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="3cc68-112">Keduanya harus dibuat dalam solusi harga.</span><span class="sxs-lookup"><span data-stu-id="3cc68-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="3cc68-113">Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="3cc68-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="3cc68-114">Dimensi berdasarkan entitas</span><span class="sxs-lookup"><span data-stu-id="3cc68-114">Entity-based dimensions</span></span>
<span data-ttu-id="3cc68-115">Untuk membuat dimensi berbasis entitas, ikuti langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="3cc68-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="3cc68-116">Buka **pengaturan** > **solusi**, lalu klik dua kali **\<your organization name> dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="3cc68-117">Di Penelusur Solusi, di panel navigasi kiri, pilih **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="3cc68-118">Pilih **baru** untuk membuat entitas baru yang disebut **judul standar**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="3cc68-119">Masukkan informasi tersisa yang diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definisi entitas judul standar](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="3cc68-121">Dimensi berbasis rangkaian pilihan</span><span class="sxs-lookup"><span data-stu-id="3cc68-121">Option set-based dimensions</span></span> 
<span data-ttu-id="3cc68-122">Anda dapat membuat dua dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="3cc68-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="3cc68-123">Gunakan **Lokasi Kerja Sumber Daya** untuk melacak harga pekerjaan lokasi **Rumah** dan pekerjaan **Di Tempat Kerja**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="3cc68-124">Gunakan **Jam Kerja Sumber Daya** dengan nilai **Reguler** dan **Lembur** untuk menerapkan markup saat pekerjaan selesai.</span><span class="sxs-lookup"><span data-stu-id="3cc68-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="3cc68-125">Grafik berikut memberikan tampilan dimensi **Lokasi Kerja Sumber Daya**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Dimensi harga berdasarkan rangkaian pilihan disebut lokasi kerja sumber daya](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="3cc68-127">Grafik berikut memberikan tampilan dimensi **Jam Kerja Sumber Daya**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Dimensi harga berdasarkan rangkaian pilihan disebut jam kerja sumber daya](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="3cc68-129">Buka **pengaturan** > **solusi**, dan klik dua kali  **\<your organization name> dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3cc68-130">Di Penelusur Solusi, pada panel navigasi kiri, pilih **Rangkaian Pilihan**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="3cc68-131">Pilih **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu pilih **simpan**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="3cc68-132">Membuat data untuk dimensi berbasis entitas</span><span class="sxs-lookup"><span data-stu-id="3cc68-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="3cc68-133">Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan.</span><span class="sxs-lookup"><span data-stu-id="3cc68-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="3cc68-134">Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="3cc68-135">Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.</span><span class="sxs-lookup"><span data-stu-id="3cc68-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="3cc68-136">Pilih **Pencarian Tingkat Lanjut**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="3cc68-137">Pilih entitas **Judul Standar**, lalu pilih **Hasil**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="3cc68-138">Semua baris di entitas **judul standar** akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="3cc68-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="3cc68-139">Pilih **Baru**, Di bidang **Nama**, masukkan "Systems Engineer", lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="3cc68-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="3cc68-140">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="3cc68-140">Close the page.</span></span> 
5. <span data-ttu-id="3cc68-141">Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".</span><span class="sxs-lookup"><span data-stu-id="3cc68-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Data sampel untuk entitas Judul Standar](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
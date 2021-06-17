---
title: Membuat bidang dan entitas kustom
description: Topik ini menjelaskan cara membuat rangkaian pilihan dan entitas dalam solusi anda sendiri di platform Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998955"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="b0a60-103">Membuat bidang dan entitas kustom</span><span class="sxs-lookup"><span data-stu-id="b0a60-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b0a60-104">Selesaikan langkah-langkah berikut saat anda ingin membuat rangkaian pilihan kustom atau entitas pada platform Power Apps.</span><span class="sxs-lookup"><span data-stu-id="b0a60-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="b0a60-105">Prosedur dalam topik ini harus diselesaikan menggunakan antarmuka web dari Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="b0a60-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b0a60-106">Sebaiknya buat semua perubahan dimensi harga kustom dalam solusi terpisah.</span><span class="sxs-lookup"><span data-stu-id="b0a60-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b0a60-107">Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya.</span><span class="sxs-lookup"><span data-stu-id="b0a60-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b0a60-108">Setelah anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.</span><span class="sxs-lookup"><span data-stu-id="b0a60-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b0a60-109">Buat bidang kustom dan rangkaian pilihan pada solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="b0a60-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b0a60-110">Dimensi harga dapat berupa rangkaian pilihan atau entitas.</span><span class="sxs-lookup"><span data-stu-id="b0a60-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b0a60-111">Keduanya harus dibuat dalam solusi harga.</span><span class="sxs-lookup"><span data-stu-id="b0a60-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b0a60-112">Langkah-langkah dalam prosedur ini menjelaskan cara membuat dimensi berbasis entitas dan dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="b0a60-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b0a60-113">Dimensi berdasarkan entitas</span><span class="sxs-lookup"><span data-stu-id="b0a60-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="b0a60-114">Di PSA, klik **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b0a60-115">Di penelusur solusi, di panel navigasi kiri, pilih **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b0a60-116">Klik **baru** untuk membuat entitas baru yang disebut **judul standar**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="b0a60-117">Masukkan informasi tersisa yang diperlukan dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definisi entitas judul standar](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="b0a60-119">Dimensi berbasis rangkaian pilihan</span><span class="sxs-lookup"><span data-stu-id="b0a60-119">Option set-based dimensions</span></span> 
<span data-ttu-id="b0a60-120">Anda dapat membuat dua dimensi berbasis rangkaian pilihan.</span><span class="sxs-lookup"><span data-stu-id="b0a60-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="b0a60-121">Gunakan **lokasi kerja sumber daya** untuk melacak harga lokasi kerja **Awal** dan pekerjaan **di lokasi** serta gunakan **jam kerja sumber daya** dengan nilai **reguler** dan **lembur** untuk menerapkan markup saat pekerjaan selesai.</span><span class="sxs-lookup"><span data-stu-id="b0a60-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="b0a60-122">Di PSA, klik **pengaturan** > **solusi**, lalu klik dua kali  **dimensi harga \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b0a60-123">Di penelusur solusi, di panel navigasi kiri, pilih  **rangkaian pilihan**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b0a60-124">Klik **baru** untuk membuat rangkaian pilihan baru, masukkan informasi yang diperlukan lainnya, lalu klik **simpan**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="b0a60-125">Dimensi harga berdasarkan rangkaian pilihan disebut lokasi kerja sumber daya</span><span class="sxs-lookup"><span data-stu-id="b0a60-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="b0a60-126">Dimensi harga berdasarkan rangkaian pilihan disebut jam kerja sumber daya</span><span class="sxs-lookup"><span data-stu-id="b0a60-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b0a60-127">Membuat data untuk dimensi berbasis entitas</span><span class="sxs-lookup"><span data-stu-id="b0a60-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b0a60-128">Anda dapat membuat data untuk dimensi berbasis entitas secara manual atau dengan menggunakan impor Microsoft Excel atau panggilan layanan.</span><span class="sxs-lookup"><span data-stu-id="b0a60-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b0a60-129">Gunakan langkah-langkah dalam prosedur ini untuk membuat dua judul standar , **Insinyur Sistem** dan **Insinyur Sistem Senior** dari dimensi berbasis entitas, yakni **Judul Standar**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b0a60-130">Jika data yang ingin Anda buat kecil, seperti dalam contoh berikut, Anda dapat menggunakan formulir standar.</span><span class="sxs-lookup"><span data-stu-id="b0a60-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b0a60-131">Di PSA, Klik **Pencarian Tingkat Lanjut**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="b0a60-132">Pilih entitas **judul standar**, lalu klik **hasil**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="b0a60-133">Semua baris di entitas **judul standar** akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="b0a60-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="b0a60-134">Klik **Baru**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-134">Click **New**.</span></span> <span data-ttu-id="b0a60-135">Di bidang **Nama**, masukkan "Systems Engineer", lalu klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="b0a60-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="b0a60-136">Tutup formulir.</span><span class="sxs-lookup"><span data-stu-id="b0a60-136">Close the form.</span></span> 
4. <span data-ttu-id="b0a60-137">Ulangi langkah 1-3 untuk membuat judul standar lain untuk "senior Systems Engineer".</span><span class="sxs-lookup"><span data-stu-id="b0a60-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="b0a60-138">Data sampel untuk entitas judul standar</span><span class="sxs-lookup"><span data-stu-id="b0a60-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
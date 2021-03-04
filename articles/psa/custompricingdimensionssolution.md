---
title: Membuat solusi kustom untuk dimensi harga
description: Topik ini menjelaskan cara membuat solusi kustom saat membuat dimensi harga kustom.
author: Rumant
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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144643"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="26509-103">Membuat solusi kustom untuk dimensi harga</span><span class="sxs-lookup"><span data-stu-id="26509-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="26509-104">Semua perubahan dimensi harga kustom harus dalam solusi terpisah.</span><span class="sxs-lookup"><span data-stu-id="26509-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="26509-105">Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya.</span><span class="sxs-lookup"><span data-stu-id="26509-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="26509-106">Setelah anda membuat perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.</span><span class="sxs-lookup"><span data-stu-id="26509-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="26509-107">Pilih **Pengaturan** > **Solusi**, lalu pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="26509-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="26509-108">Namai solusi, **\<your organization name> dimensi harga**, masukkan informasi yang diperlukan lainnya, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="26509-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Membuat solusi kustom untuk dimensi harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="26509-110">Tambahkan semua entitas yang diperlukan dan komponen terkait ke solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="26509-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="26509-111">Anda harus menambahkan entitas Project Service berikut ke solusi harga.</span><span class="sxs-lookup"><span data-stu-id="26509-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="26509-112">Selesaikan langkah-langkah dalam prosedur ini untuk membuat beberapa perubahan skema penting dalam solusi harga sehingga entitas mengetahui dimensi harga baru.</span><span class="sxs-lookup"><span data-stu-id="26509-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="26509-113">Pilih **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="26509-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="26509-114">Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="26509-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="26509-115">Di kotak dialog **komponen solusi**, pilih entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="26509-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="26509-116">Aktual</span><span class="sxs-lookup"><span data-stu-id="26509-116">Actual</span></span>
- <span data-ttu-id="26509-117">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="26509-117">Bookable Resource</span></span>
- <span data-ttu-id="26509-118">Baris Perkiraan</span><span class="sxs-lookup"><span data-stu-id="26509-118">Estimate Line</span></span>
- <span data-ttu-id="26509-119">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="26509-119">Project Task</span></span>
- <span data-ttu-id="26509-120">Detail Baris Faktur</span><span class="sxs-lookup"><span data-stu-id="26509-120">Invoice Line Detail</span></span>
- <span data-ttu-id="26509-121">Lini Jurnal</span><span class="sxs-lookup"><span data-stu-id="26509-121">Journal Line</span></span>
- <span data-ttu-id="26509-122">Detail Baris Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="26509-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="26509-123">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="26509-123">Project Team Member</span></span>
- <span data-ttu-id="26509-124">Rincian Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="26509-124">Quote Line Detail</span></span>
- <span data-ttu-id="26509-125">Markup Harga Peran</span><span class="sxs-lookup"><span data-stu-id="26509-125">Role Price Markup</span></span>
- <span data-ttu-id="26509-126">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="26509-126">Role Price</span></span> 
- <span data-ttu-id="26509-127">Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="26509-127">Time Entry</span></span> 

> ![Menambahkan entitas yang ada ke solusi dimensi harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen solusi](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="26509-130">Pastikan untuk menyertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="26509-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="26509-131">Bila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih, pilih **tidak**.</span><span class="sxs-lookup"><span data-stu-id="26509-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Jangan sertakan semua komponen terkait](media/Do-not-include-required.png)



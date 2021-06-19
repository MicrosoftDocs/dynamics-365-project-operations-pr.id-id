---
title: Membuat solusi kustom untuk dimensi harga
description: Topik ini menjelaskan cara membuat solusi kustom saat membuat dimensi harga kustom.
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
ms.openlocfilehash: ae7f22b9cb092e956d0f1eaf1f1997c8e97392f4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012320"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="d044b-103">Membuat solusi kustom untuk dimensi harga</span><span class="sxs-lookup"><span data-stu-id="d044b-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="d044b-104">Semua perubahan dimensi harga kustom harus dalam solusi terpisah.</span><span class="sxs-lookup"><span data-stu-id="d044b-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="d044b-105">Praktik terbaik yang penting ini memberikan fleksibilitas di masa mendatang untuk memperbarui atau menghapus perubahan yang diperlukan, akan membantu penggunaan ulang pekerjaan Anda, dan membuatnya lebih mudah untuk memindahkan perubahan ini ke instans lainnya.</span><span class="sxs-lookup"><span data-stu-id="d044b-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="d044b-106">Setelah anda membuat perubahan yang diperlukan, ekspor solusi ini sebagai **solusi terkelola** dan impor ke instans lain untuk menggunakan kembali konfigurasi harga anda.</span><span class="sxs-lookup"><span data-stu-id="d044b-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="d044b-107">Pilih **Pengaturan** > **Solusi**, lalu pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="d044b-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="d044b-108">Namai solusi, **\<your organization name> dimensi harga**, masukkan informasi yang diperlukan lainnya, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="d044b-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![Membuat solusi kustom untuk dimensi harga](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="d044b-110">Tambahkan semua entitas yang diperlukan dan komponen terkait ke solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="d044b-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="d044b-111">Anda harus menambahkan entitas Project Service berikut ke solusi harga.</span><span class="sxs-lookup"><span data-stu-id="d044b-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="d044b-112">Selesaikan langkah-langkah dalam prosedur ini untuk membuat beberapa perubahan skema penting dalam solusi harga sehingga entitas mengetahui dimensi harga baru.</span><span class="sxs-lookup"><span data-stu-id="d044b-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="d044b-113">Pilih **pengaturan** > **solusi**, lalu klik dua kali **dimensi harga \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="d044b-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="d044b-114">Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="d044b-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="d044b-115">Di kotak dialog **komponen solusi**, pilih entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="d044b-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="d044b-116">Aktual</span><span class="sxs-lookup"><span data-stu-id="d044b-116">Actual</span></span>
- <span data-ttu-id="d044b-117">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d044b-117">Bookable Resource</span></span>
- <span data-ttu-id="d044b-118">Baris Perkiraan</span><span class="sxs-lookup"><span data-stu-id="d044b-118">Estimate Line</span></span>
- <span data-ttu-id="d044b-119">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="d044b-119">Project Task</span></span>
- <span data-ttu-id="d044b-120">Detail Baris Faktur</span><span class="sxs-lookup"><span data-stu-id="d044b-120">Invoice Line Detail</span></span>
- <span data-ttu-id="d044b-121">Lini Jurnal</span><span class="sxs-lookup"><span data-stu-id="d044b-121">Journal Line</span></span>
- <span data-ttu-id="d044b-122">Detail Baris Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="d044b-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="d044b-123">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="d044b-123">Project Team Member</span></span>
- <span data-ttu-id="d044b-124">Rincian Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="d044b-124">Quote Line Detail</span></span>
- <span data-ttu-id="d044b-125">Markup Harga Peran</span><span class="sxs-lookup"><span data-stu-id="d044b-125">Role Price Markup</span></span>
- <span data-ttu-id="d044b-126">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="d044b-126">Role Price</span></span> 
- <span data-ttu-id="d044b-127">Entri Waktu</span><span class="sxs-lookup"><span data-stu-id="d044b-127">Time Entry</span></span> 

> ![Menambahkan entitas yang ada ke solusi dimensi harga](media/Existing-entities-to-PD-solution.png)

> ![Pilih komponen solusi](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="d044b-130">Pastikan untuk menyertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="d044b-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="d044b-131">Bila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih, pilih **tidak**.</span><span class="sxs-lookup"><span data-stu-id="d044b-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Jangan sertakan semua komponen terkait](media/Do-not-include-required.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]
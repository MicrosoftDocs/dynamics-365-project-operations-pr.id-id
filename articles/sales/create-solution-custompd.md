---
title: Membuat solusi untuk dimensi harga kustom
description: Topik ini berisi informasi tentang cara membuat solusi untuk dimensi harga kustom.
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86f4cd2c26ebfca621d1b226b571d220d3b2441e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010340"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="c28bf-103">Membuat solusi untuk dimensi harga kustom</span><span class="sxs-lookup"><span data-stu-id="c28bf-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="c28bf-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="c28bf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="c28bf-105">Semua perubahan dimensi harga kustom harus dalam solusi terpisah.</span><span class="sxs-lookup"><span data-stu-id="c28bf-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="c28bf-106">Praktik terbaik yang penting ini memberikan fleksibilitas untuk memperbarui atau menghapus perubahan yang diperlukan, sehingga membantu dalam menggunakan kembali karya Anda, dan akan lebih memudahkan saat memindahkan perubahan ke berbagai instans lainnya.</span><span class="sxs-lookup"><span data-stu-id="c28bf-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="c28bf-107">Setelah Anda membuat semua perubahan yang diperlukan, ekspor solusi ini sebagai solusi **Terkelola**, dan kemudian impor ke instans lain untuk digunakan kembali.</span><span class="sxs-lookup"><span data-stu-id="c28bf-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="c28bf-108">Membuat solusi untuk dimensi harga kustom</span><span class="sxs-lookup"><span data-stu-id="c28bf-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="c28bf-109">Pilih **Pengaturan** > **Solusi**, lalu pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="c28bf-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="c28bf-110">Beri nama untuk solusi tersebut, *dimensi harga <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="c28bf-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="c28bf-111">Masukkan informasi tersisa yang diperlukan dan kemudian pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="c28bf-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Membuat solusi untuk dimensi harga kustom](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="c28bf-113">Tambahkan semua entitas yang diperlukan dan komponen terkait ke solusi dimensi harga</span><span class="sxs-lookup"><span data-stu-id="c28bf-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="c28bf-114">Tambahkan entitas Project Service berikut ke solusi harga Anda untuk membuat perubahan skema yang penting dalam solusi harga.</span><span class="sxs-lookup"><span data-stu-id="c28bf-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="c28bf-115">Setelah Anda menyelesaikan prosedur ini, entitas akan mengenali dimensi harga yang baru.</span><span class="sxs-lookup"><span data-stu-id="c28bf-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="c28bf-116">Pilih **Pengaturan** > **Solusi**, lalu klik dua kali **<*nama organisasi Anda*> dimensi harga**.</span><span class="sxs-lookup"><span data-stu-id="c28bf-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="c28bf-117">Di penelusur solusi, di panel navigasi kiri, pilih **Tambahkan yang Ada** > **Entitas**.</span><span class="sxs-lookup"><span data-stu-id="c28bf-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="c28bf-118">Di kotak dialog **komponen solusi**, pilih entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="c28bf-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="c28bf-119">**Aktual**</span><span class="sxs-lookup"><span data-stu-id="c28bf-119">**Actual**</span></span>
   - <span data-ttu-id="c28bf-120">**Sumber Daya Dapat Dipesan**</span><span class="sxs-lookup"><span data-stu-id="c28bf-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="c28bf-121">**Baris Perkiraan**</span><span class="sxs-lookup"><span data-stu-id="c28bf-121">**Estimate Line**</span></span>
   - <span data-ttu-id="c28bf-122">**Tugas Proyek**</span><span class="sxs-lookup"><span data-stu-id="c28bf-122">**Project Task**</span></span>
   - <span data-ttu-id="c28bf-123">**Rincian Baris Faktur**</span><span class="sxs-lookup"><span data-stu-id="c28bf-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="c28bf-124">**Lini Jurnal**</span><span class="sxs-lookup"><span data-stu-id="c28bf-124">**Journal Line**</span></span>
   - <span data-ttu-id="c28bf-125">**Rincian Baris Kontrak Proyek**</span><span class="sxs-lookup"><span data-stu-id="c28bf-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="c28bf-126">**Anggota Tim Proyek**</span><span class="sxs-lookup"><span data-stu-id="c28bf-126">**Project Team Member**</span></span>
   - <span data-ttu-id="c28bf-127">**Rincian Baris Kuotasi**</span><span class="sxs-lookup"><span data-stu-id="c28bf-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="c28bf-128">**Markup Harga Peran**</span><span class="sxs-lookup"><span data-stu-id="c28bf-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="c28bf-129">**Harga Peran**</span><span class="sxs-lookup"><span data-stu-id="c28bf-129">**Role Price**</span></span>
   - <span data-ttu-id="c28bf-130">**Entri Waktu**</span><span class="sxs-lookup"><span data-stu-id="c28bf-130">**Time Entry**</span></span>
 
   ![Menambahkan solusi dimensi harga kustom berbagai entitas yang ada](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="c28bf-132">Untuk setiap entitas, tinjau komponen yang ditambahkan dan daftar akhir aset entitas untuk setiap entitas.</span><span class="sxs-lookup"><span data-stu-id="c28bf-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="c28bf-133">Sertakan semua formulir dan tampilan untuk setiap entitas yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="c28bf-133">Include all forms and views for each of the selected entities.</span></span>

  ![Entitas ditambahkan](./media/solution-component-selection.png)


5.  <span data-ttu-id="c28bf-135">Apabila diminta untuk menyertakan entitas dependen untuk entitas yang dipilih, pilih **Tidak, jangan sertakan komponen yang diperlukan.**</span><span class="sxs-lookup"><span data-stu-id="c28bf-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Termasuk entitas dependen](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
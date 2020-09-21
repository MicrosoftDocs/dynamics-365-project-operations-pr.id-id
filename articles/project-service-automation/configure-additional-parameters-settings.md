---
title: Mengkonfigurasi pengaturan parameter tambahan
description: Bagaimana mengkonfigurasi pengaturan parameter tambahan dalam Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752529"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="829c0-103">Mengkonfigurasi pengaturan parameter tambahan (Project Service)</span><span class="sxs-lookup"><span data-stu-id="829c0-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="829c0-104">Setelah Anda mengkonfigurasi item dalam topik-topik sebelumnya, Anda perlu mengatur parameter proyek tambahan yang digunakan untuk proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="829c0-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="829c0-105">Ketika Anda pertama kali memasang [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], Anda membuat pengaturan parameter untuk pertama kali membuat semua rekaman yang diperlukan agar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bekerja.</span><span class="sxs-lookup"><span data-stu-id="829c0-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="829c0-106">Sekarang saatnya untuk kembali dan mengkonfigurasikan bidang tambahan untuk pengaturan ini.</span><span class="sxs-lookup"><span data-stu-id="829c0-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="829c0-107">Anda perlu mengkonfigurasi pengaturan berikut:</span><span class="sxs-lookup"><span data-stu-id="829c0-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="829c0-108">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="829c0-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="829c0-109">Frekuensi faktur</span><span class="sxs-lookup"><span data-stu-id="829c0-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="829c0-110">Template Jam Kerja</span><span class="sxs-lookup"><span data-stu-id="829c0-110">Work hours template</span></span>  
  
-   <span data-ttu-id="829c0-111">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="829c0-111">Price list</span></span>  
 
<span data-ttu-id="829c0-112">Dalam langkah ini, Anda juga akan menunjukkan jenis alokasi sumber daya yang Anda inginkan:</span><span class="sxs-lookup"><span data-stu-id="829c0-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="829c0-113">**Pusat**.</span><span class="sxs-lookup"><span data-stu-id="829c0-113">**Central**.</span></span> <span data-ttu-id="829c0-114">Manajer sumber daya hanya dapat mengalokasikan sumber daya untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="829c0-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="829c0-115">**Hibrid**.</span><span class="sxs-lookup"><span data-stu-id="829c0-115">**Hybrid**.</span></span> <span data-ttu-id="829c0-116">Manajer sumber daya, manajer proyek dan manajer akun dapat mengalokasikan sumber daya untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="829c0-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="829c0-117">Untuk mengatur Parameter Proyek:</span><span class="sxs-lookup"><span data-stu-id="829c0-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="829c0-118">Lihat **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="829c0-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="829c0-119">Klik pengaturan parameter yang ingin Anda konfigurasi (yang Anda buat ketika Anda pertama kali menginstal [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), atau klik **baru** untuk membuat yang baru.</span><span class="sxs-lookup"><span data-stu-id="829c0-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="829c0-120">Dalam area **umum**, atur semua pilihan parameter proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="829c0-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="829c0-121">Dalam area daftar **harga**, klik **+** untuk menambah daftar harga, memilih daftar harga di daftar drop-down **daftar harga Parameter proyek**, dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="829c0-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="829c0-122">Klik tombol **Simpan** di sudut kanan bawah layar.</span><span class="sxs-lookup"><span data-stu-id="829c0-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="829c0-123">Rekaman parameter proyek harus dipertahankan agar Project Service berfungsi secara tepat.</span><span class="sxs-lookup"><span data-stu-id="829c0-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="829c0-124">Rekaman ini tidak boleh dihapus.</span><span class="sxs-lookup"><span data-stu-id="829c0-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="829c0-125">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="829c0-125">See Also</span></span>  
 [<span data-ttu-id="829c0-126">Konfigurasi Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="829c0-126">Set up resources</span></span>](../project-service/set-up-resources.md)

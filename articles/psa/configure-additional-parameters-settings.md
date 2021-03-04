---
title: Mengkonfigurasi pengaturan parameter tambahan
description: Bagaimana mengkonfigurasi pengaturan parameter tambahan dalam Project Service
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 73264845808e12950a48eea2b79e54c393d9c024
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151572"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="de5ed-103">Mengkonfigurasi pengaturan parameter tambahan (Project Service)</span><span class="sxs-lookup"><span data-stu-id="de5ed-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="de5ed-104">Setelah Anda mengkonfigurasi item dalam topik-topik sebelumnya, Anda perlu mengatur parameter proyek tambahan yang digunakan untuk proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="de5ed-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="de5ed-105">Ketika Anda pertama kali memasang [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], Anda membuat pengaturan parameter untuk pertama kali membuat semua rekaman yang diperlukan agar [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bekerja.</span><span class="sxs-lookup"><span data-stu-id="de5ed-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="de5ed-106">Sekarang saatnya untuk kembali dan mengkonfigurasikan bidang tambahan untuk pengaturan ini.</span><span class="sxs-lookup"><span data-stu-id="de5ed-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="de5ed-107">Anda perlu mengkonfigurasi pengaturan berikut:</span><span class="sxs-lookup"><span data-stu-id="de5ed-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="de5ed-108">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="de5ed-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="de5ed-109">Frekuensi faktur</span><span class="sxs-lookup"><span data-stu-id="de5ed-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="de5ed-110">Template Jam Kerja</span><span class="sxs-lookup"><span data-stu-id="de5ed-110">Work hours template</span></span>  
  
-   <span data-ttu-id="de5ed-111">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="de5ed-111">Price list</span></span>  
 
<span data-ttu-id="de5ed-112">Dalam langkah ini, Anda juga akan menunjukkan jenis alokasi sumber daya yang Anda inginkan:</span><span class="sxs-lookup"><span data-stu-id="de5ed-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="de5ed-113">**Pusat**.</span><span class="sxs-lookup"><span data-stu-id="de5ed-113">**Central**.</span></span> <span data-ttu-id="de5ed-114">Manajer sumber daya hanya dapat mengalokasikan sumber daya untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="de5ed-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="de5ed-115">**Hibrid**.</span><span class="sxs-lookup"><span data-stu-id="de5ed-115">**Hybrid**.</span></span> <span data-ttu-id="de5ed-116">Manajer sumber daya, manajer proyek dan manajer akun dapat mengalokasikan sumber daya untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="de5ed-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="de5ed-117">Untuk mengatur Parameter Proyek:</span><span class="sxs-lookup"><span data-stu-id="de5ed-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="de5ed-118">Lihat **Project Service > Parameter**.</span><span class="sxs-lookup"><span data-stu-id="de5ed-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="de5ed-119">Klik pengaturan parameter yang ingin Anda konfigurasi (yang Anda buat ketika Anda pertama kali menginstal [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), atau klik **baru** untuk membuat yang baru.</span><span class="sxs-lookup"><span data-stu-id="de5ed-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="de5ed-120">Dalam area **umum**, atur semua pilihan parameter proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="de5ed-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="de5ed-121">Dalam area daftar **harga**, klik **+** untuk menambah daftar harga, memilih daftar harga di daftar drop-down **daftar harga Parameter proyek**, dan kemudian klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="de5ed-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="de5ed-122">Klik tombol **Simpan** di sudut kanan bawah layar.</span><span class="sxs-lookup"><span data-stu-id="de5ed-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="de5ed-123">Rekaman parameter proyek harus dipertahankan agar Project Service berfungsi secara tepat.</span><span class="sxs-lookup"><span data-stu-id="de5ed-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="de5ed-124">Rekaman ini tidak boleh dihapus.</span><span class="sxs-lookup"><span data-stu-id="de5ed-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="de5ed-125">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="de5ed-125">See Also</span></span>  
 [<span data-ttu-id="de5ed-126">Konfigurasi Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="de5ed-126">Set up resources</span></span>](../psa/set-up-resources.md)

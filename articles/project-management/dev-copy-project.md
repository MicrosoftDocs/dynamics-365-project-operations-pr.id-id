---
title: Mengembangkan template proyek dengan Salinan Proyek
description: Topik ini menyediakan informasi tentang cara membuat template proyek menggunakan tindakan kustom menyalin proyek.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642412"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="c5ad2-103">Mengembangkan template proyek dengan Salinan Proyek</span><span class="sxs-lookup"><span data-stu-id="c5ad2-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="c5ad2-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="c5ad2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c5ad2-105">Dynamics 365 Project Operations mendukung kemampuan untuk menyalin proyek dan mengembalikan tugas apa pun ke sumber daya umum yang menunjukkan peran.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="c5ad2-106">Pelanggan dapat menggunakan fungsi ini untuk membuat template proyek dasar.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="c5ad2-107">Bila Anda memilih **Salin proyek**, status proyek target diperbarui.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="c5ad2-108">Gunakan **alasan status** untuk menentukan kapan tindakan penyalinan selesai.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="c5ad2-109">Memilih **Salin proyek** juga memperbarui tanggal mulai proyek ke tanggal mulai saat ini jika tidak ada target tanggal terdeteksi di entitas proyek target.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="c5ad2-110">Tindakan kustom Salin proyek</span><span class="sxs-lookup"><span data-stu-id="c5ad2-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="c5ad2-111">Nama</span><span class="sxs-lookup"><span data-stu-id="c5ad2-111">Name</span></span> 

<span data-ttu-id="c5ad2-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="c5ad2-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="c5ad2-113">Parameter input</span><span class="sxs-lookup"><span data-stu-id="c5ad2-113">Input parameters</span></span>
<span data-ttu-id="c5ad2-114">Terdapat tiga parameter input:</span><span class="sxs-lookup"><span data-stu-id="c5ad2-114">There are three input parameters:</span></span>

| <span data-ttu-id="c5ad2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c5ad2-115">Parameter</span></span>          | <span data-ttu-id="c5ad2-116">Tipe</span><span class="sxs-lookup"><span data-stu-id="c5ad2-116">Type</span></span>   | <span data-ttu-id="c5ad2-117">Values</span><span class="sxs-lookup"><span data-stu-id="c5ad2-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="c5ad2-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="c5ad2-118">ProjectCopyOption</span></span>  | <span data-ttu-id="c5ad2-119">String</span><span class="sxs-lookup"><span data-stu-id="c5ad2-119">String</span></span> | <span data-ttu-id="c5ad2-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="c5ad2-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="c5ad2-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="c5ad2-121">SourceProject</span></span>      | <span data-ttu-id="c5ad2-122">Referensi Entitas</span><span class="sxs-lookup"><span data-stu-id="c5ad2-122">Entity Reference</span></span> | <span data-ttu-id="c5ad2-123">Proyek Sumber</span><span class="sxs-lookup"><span data-stu-id="c5ad2-123">Source Project</span></span> |
| <span data-ttu-id="c5ad2-124">Target</span><span class="sxs-lookup"><span data-stu-id="c5ad2-124">Target</span></span>             | <span data-ttu-id="c5ad2-125">Referensi Entitas</span><span class="sxs-lookup"><span data-stu-id="c5ad2-125">Entity Reference</span></span> | <span data-ttu-id="c5ad2-126">Proyek target</span><span class="sxs-lookup"><span data-stu-id="c5ad2-126">Target Project</span></span> |


- <span data-ttu-id="c5ad2-127">**{"clearTeamsAndAssignments":true}**: perilaku default Anda untuk proyek untuk web, dan akan menghapus semua tugas dan anggota tim.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="c5ad2-128">**{"removeNamedResources":true}** perilaku default untuk Project Operations, dan akan mengembalikan tugas ke sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="c5ad2-129">Untuk default lebih lanjut tentang tindakan, lihat [menggunakan tindakan API Web](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="c5ad2-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="c5ad2-130">Menentukan bidang yang akan disalin</span><span class="sxs-lookup"><span data-stu-id="c5ad2-130">Specify fields to copy</span></span> 
<span data-ttu-id="c5ad2-131">Saat tindakan dipanggil, **Salin proyek** akan melihat tampilan proyek **Kolom Salin proyek** untuk menentukan bidang yang akan disalin saat proyek disalin.</span><span class="sxs-lookup"><span data-stu-id="c5ad2-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>

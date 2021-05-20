---
title: Mengembangkan template proyek dengan Salinan Proyek
description: Topik ini menyediakan informasi tentang cara membuat template proyek menggunakan tindakan kustom menyalin proyek.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949818"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="77362-103">Mengembangkan template proyek dengan Salinan Proyek</span><span class="sxs-lookup"><span data-stu-id="77362-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="77362-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="77362-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="77362-105">Dynamics 365 Project Operations mendukung kemampuan untuk menyalin proyek dan mengembalikan tugas apa pun ke sumber daya umum yang menunjukkan peran.</span><span class="sxs-lookup"><span data-stu-id="77362-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="77362-106">Pelanggan dapat menggunakan fungsi ini untuk membuat template proyek dasar.</span><span class="sxs-lookup"><span data-stu-id="77362-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="77362-107">Bila Anda memilih **Salin proyek**, status proyek target diperbarui.</span><span class="sxs-lookup"><span data-stu-id="77362-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="77362-108">Gunakan **alasan status** untuk menentukan kapan tindakan penyalinan selesai.</span><span class="sxs-lookup"><span data-stu-id="77362-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="77362-109">Memilih **Salin proyek** juga memperbarui tanggal mulai proyek ke tanggal mulai saat ini jika tidak ada target tanggal terdeteksi di entitas proyek target.</span><span class="sxs-lookup"><span data-stu-id="77362-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="77362-110">Tindakan kustom Salin proyek</span><span class="sxs-lookup"><span data-stu-id="77362-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="77362-111">Nama</span><span class="sxs-lookup"><span data-stu-id="77362-111">Name</span></span> 

<span data-ttu-id="77362-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="77362-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="77362-113">Parameter input</span><span class="sxs-lookup"><span data-stu-id="77362-113">Input parameters</span></span>
<span data-ttu-id="77362-114">Terdapat tiga parameter input:</span><span class="sxs-lookup"><span data-stu-id="77362-114">There are three input parameters:</span></span>

| <span data-ttu-id="77362-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="77362-115">Parameter</span></span>          | <span data-ttu-id="77362-116">Tipe</span><span class="sxs-lookup"><span data-stu-id="77362-116">Type</span></span>   | <span data-ttu-id="77362-117">Values</span><span class="sxs-lookup"><span data-stu-id="77362-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="77362-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="77362-118">ProjectCopyOption</span></span>  | <span data-ttu-id="77362-119">String</span><span class="sxs-lookup"><span data-stu-id="77362-119">String</span></span> | <span data-ttu-id="77362-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="77362-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="77362-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="77362-121">SourceProject</span></span>      | <span data-ttu-id="77362-122">Referensi Entitas</span><span class="sxs-lookup"><span data-stu-id="77362-122">Entity Reference</span></span> | <span data-ttu-id="77362-123">Proyek Sumber</span><span class="sxs-lookup"><span data-stu-id="77362-123">Source Project</span></span> |
| <span data-ttu-id="77362-124">Target</span><span class="sxs-lookup"><span data-stu-id="77362-124">Target</span></span>             | <span data-ttu-id="77362-125">Referensi Entitas</span><span class="sxs-lookup"><span data-stu-id="77362-125">Entity Reference</span></span> | <span data-ttu-id="77362-126">Proyek target</span><span class="sxs-lookup"><span data-stu-id="77362-126">Target Project</span></span> |


- <span data-ttu-id="77362-127">**{"clearTeamsAndAssignments":true}**: perilaku default Anda untuk proyek untuk web, dan akan menghapus semua tugas dan anggota tim.</span><span class="sxs-lookup"><span data-stu-id="77362-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="77362-128">**{"removeNamedResources":true}** perilaku default untuk Project Operations, dan akan mengembalikan tugas ke sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="77362-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="77362-129">Untuk default lebih lanjut tentang tindakan, lihat [menggunakan tindakan API Web](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="77362-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="77362-130">Menentukan bidang yang akan disalin</span><span class="sxs-lookup"><span data-stu-id="77362-130">Specify fields to copy</span></span> 
<span data-ttu-id="77362-131">Saat tindakan dipanggil, **Salin proyek** akan melihat tampilan proyek **Kolom Salin proyek** untuk menentukan bidang yang akan disalin saat proyek disalin.</span><span class="sxs-lookup"><span data-stu-id="77362-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="77362-132">Contoh</span><span class="sxs-lookup"><span data-stu-id="77362-132">Example</span></span>
<span data-ttu-id="77362-133">Contoh berikut menunjukkan cara memanggil tindakan kustom **CopyProject** dengan rangkaian parameter **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="77362-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]
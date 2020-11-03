---
title: Menggunakan Add-in Project Service untuk merencanakan pekerjaan Anda di Microsoft Project | MicrosoftDocs
description: Topik ini menyediakan informasi tentang cara menambah, mengkonfigurasikan, dan menggunakan add-in Microsoft project untuk Microsoft project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
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
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078614"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="baff8-103">Menggunakan Add-in Project Service Automation untuk merencanakan pekerjaan Anda di Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="baff8-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="baff8-104">membuatnya lebih mudah bagi Anda untuk melakukan perencanaan proyek, termasuk perkiraan.</span><span class="sxs-lookup"><span data-stu-id="baff8-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="baff8-105">Anda bisa mendefinisikan pekerjaan sehingga biaya, tenaga, dan nilai penjualan jelas saat proposal final diajukan.</span><span class="sxs-lookup"><span data-stu-id="baff8-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="baff8-106">Sekarang Anda dapat menginstal [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] dan melakukan pekerjaan perencanaan Anda di lingkungan akrab dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="baff8-107">Gunakan kemampuan perencanaan dan manajemen yang kuat dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan kemudian memperbarui rencana proyek Anda di Project service automation.</span><span class="sxs-lookup"><span data-stu-id="baff8-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="baff8-108">Untuk menggunakan manajemen dokumen SharePoint untuk menyimpan file [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Anda untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], admin [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Anda akan perlu untuk mengaktifkan manajemen dokumen.</span><span class="sxs-lookup"><span data-stu-id="baff8-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="baff8-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] hanya kompatibel dengan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="baff8-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="baff8-110">Men-download dan menginstal pengaya</span><span class="sxs-lookup"><span data-stu-id="baff8-110">Download and install the add-in</span></span>  
 <span data-ttu-id="baff8-111">Siapkan informasi masuk [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Anda.</span><span class="sxs-lookup"><span data-stu-id="baff8-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="baff8-112">Anda akan memerlukan informasi ini untuk menghubungkan dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="baff8-113">Dari pusat Unduhan, unduh add-in untuk versi project service yang didukung, baik [v2.X](https://go.microsoft.com/fwlink/?linkid=828268) atau [v3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="baff8-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="baff8-114">Klik tautan download.</span><span class="sxs-lookup"><span data-stu-id="baff8-114">Click the download link.</span></span>  

3.  <span data-ttu-id="baff8-115">Jika download selesai, klik **ya** untuk menginstal pengaya (add-in).</span><span class="sxs-lookup"><span data-stu-id="baff8-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="baff8-116">Mengkonfigurasi pengaya</span><span class="sxs-lookup"><span data-stu-id="baff8-116">Configure the add-in</span></span>  

1. <span data-ttu-id="baff8-117">Buka [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan klik tab **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="baff8-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="baff8-118">Klik **Hubungkan**.</span><span class="sxs-lookup"><span data-stu-id="baff8-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="baff8-119">Masukkan informasi masuk Anda dan kemudian klik **masuk**.</span><span class="sxs-lookup"><span data-stu-id="baff8-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="baff8-120">Sekarang Anda dapat mulai menggunakan pengaya.</span><span class="sxs-lookup"><span data-stu-id="baff8-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="baff8-121">Membaca dari template</span><span class="sxs-lookup"><span data-stu-id="baff8-121">Read from a template</span></span>  
 <span data-ttu-id="baff8-122">Baca dari template yang Anda buat dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] dan salin ke [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] untuk memulai perencanaan proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="baff8-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="baff8-123">[Membuat template proyek (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="baff8-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="baff8-124">Dari tab **Project service** , klik **Baca** > **Template proyek Project service automation**.</span><span class="sxs-lookup"><span data-stu-id="baff8-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="baff8-125">Pilih template proyek dari daftar dan kemudian klik **buka**.</span><span class="sxs-lookup"><span data-stu-id="baff8-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="baff8-126">Secara default, tugas-tugas yang disalin dari template ke dalam proyek ditetapkan seperti dijadwalkan secara manual.</span><span class="sxs-lookup"><span data-stu-id="baff8-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="baff8-127">Menetapkan peran [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] ke sumber daya proyek</span><span class="sxs-lookup"><span data-stu-id="baff8-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="baff8-128">Buka sebuah proyek dan klik pita **tugas**.</span><span class="sxs-lookup"><span data-stu-id="baff8-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="baff8-129">Klik menu **Gantt Chart** menu dan kemudian pilih **lembar sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="baff8-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="baff8-130">Pada lembar sumber daya, klik menu drop-down **peran Project Service Resource** dan pilih peran Project service automation.</span><span class="sxs-lookup"><span data-stu-id="baff8-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="baff8-131">Lengkapi proyek Anda dengan sumber daya</span><span class="sxs-lookup"><span data-stu-id="baff8-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="baff8-132">Dari tab Project Service pilih baris dan klik **Temukan sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="baff8-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="baff8-133">Pada layar **Pesan sumber daya** , pilih sumber daya yang ingin Anda gunakan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="baff8-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="baff8-134">Klik **Buku** dan kemudian klik **OK**.</span><span class="sxs-lookup"><span data-stu-id="baff8-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="baff8-135">Publikasikan proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="baff8-135">Publish your project</span></span>  
<span data-ttu-id="baff8-136">Setelah perencanaan proyek Anda selesai, langkah berikutnya adalah untuk mengimpor dan mempublikasikan proyek di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="baff8-137">Proyek akan diimpor ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="baff8-138">Harga dan proses pembuatan tim diterapkan.</span><span class="sxs-lookup"><span data-stu-id="baff8-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="baff8-139">Buka proyek di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] untuk melihat bahwa tim, perkiraan proyek, dan struktur rincian kerja telah dihasilkan.</span><span class="sxs-lookup"><span data-stu-id="baff8-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="baff8-140">Tabel berikut menunjukkan lokasi untuk mencari hasil:</span><span class="sxs-lookup"><span data-stu-id="baff8-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="baff8-141">**Diagram Gantt**</span><span class="sxs-lookup"><span data-stu-id="baff8-141">**Gantt Chart**</span></span>   | <span data-ttu-id="baff8-142">Impor ke layar **struktur rincian kerja** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| <span data-ttu-id="baff8-143">**Lembar sumber daya** [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="baff8-143">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Resource Sheet**</span></span> |   <span data-ttu-id="baff8-144">Impor ke layar **anggota tim proyek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   <span data-ttu-id="baff8-145">**Menggunakan penggunaan** [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="baff8-145">[!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Use Usage**</span></span>    |    <span data-ttu-id="baff8-146">Impor ke layar **estimasi proyek** [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="baff8-147">**Untuk mengimpor dan mempublikasikan proyek Anda**</span><span class="sxs-lookup"><span data-stu-id="baff8-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="baff8-148">Dari tab **Project service** , klik **Terbitkan** > **proyek Project Service Automation baru**.</span><span class="sxs-lookup"><span data-stu-id="baff8-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="baff8-149">Pada kotak dialog **Terbitkan ke sebuah proyek baru dalam Project Service** , masukkan **nama proyek** dan pilih **pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="baff8-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="baff8-150">Bisa juga periksa **tautkan rencana proyek ke Project service automation** untuk menautkan file rencana proyek ke Project service automation.</span><span class="sxs-lookup"><span data-stu-id="baff8-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="baff8-151">Klik **Terbitkan**.</span><span class="sxs-lookup"><span data-stu-id="baff8-151">Click **Publish**.</span></span>  

   <span data-ttu-id="baff8-152">Menghubungkan file proyek ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] membuat file proyek sebagai master dan menetapkan struktur rincian kerja dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadi baca-saja.</span><span class="sxs-lookup"><span data-stu-id="baff8-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="baff8-153">Untuk membuat perubahan rencana proyek, Anda harus membuat mereka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan mempublikasikan mereka sebagai pembaruan kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="baff8-154">Mengedit sebuah proyek yang telah diimpor</span><span class="sxs-lookup"><span data-stu-id="baff8-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="baff8-155">Untuk membuat perubahan ke rencana proyek yang telah diimpor ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], Anda memiliki dua pilihan:</span><span class="sxs-lookup"><span data-stu-id="baff8-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="baff8-156">Buka master file dan edit di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="baff8-157">Batalkan tautan file dan edit langsung di Project Service.</span><span class="sxs-lookup"><span data-stu-id="baff8-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="baff8-158">Secara default, sebuah proyek yang telah di-upload dari [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] terkunci dan hanya bisa diedit dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="baff8-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="baff8-159">Untuk mengedit file dalam [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], file tersebut harus tidak tertaut.</span><span class="sxs-lookup"><span data-stu-id="baff8-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="baff8-160">Edit di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="baff8-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="baff8-161">Dari menu utama, klik **Project Service** > **Proyek**.</span><span class="sxs-lookup"><span data-stu-id="baff8-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="baff8-162">Dari daftar proyek, buka satu yang dibuat di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="baff8-163">Klik **buka di MS Project** dari pita.</span><span class="sxs-lookup"><span data-stu-id="baff8-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="baff8-164">Ini akan membuka master file yang tertaut di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="baff8-165">Batalkan tautan file dan edit di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="baff8-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="baff8-166">Dari menu utama, klik **Project Service** > **Proyek**.</span><span class="sxs-lookup"><span data-stu-id="baff8-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="baff8-167">Dari daftar proyek, buka satu yang dibuat di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="baff8-168">Klik **hapus tautan dari MS Project** dari pita.</span><span class="sxs-lookup"><span data-stu-id="baff8-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="baff8-169">Mengunggah berkas proyek ke SharePoint atau Office Groups</span><span class="sxs-lookup"><span data-stu-id="baff8-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="baff8-170">Anda bisa mengupload file proyek ke SharePoint dan menemukannya di bawah dokumen yang terkait untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] Anda.</span><span class="sxs-lookup"><span data-stu-id="baff8-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="baff8-171">Anda perlu meminta administrator Anda mengkonfigurasi manajemen dokumen SharePoint dan menyalakannya untuk entitas proyek.</span><span class="sxs-lookup"><span data-stu-id="baff8-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="baff8-172">Anda juga dapat mengunggah berkas proyek untuk [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] jika Anda telah mengonfigurasikan Office Groups.</span><span class="sxs-lookup"><span data-stu-id="baff8-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="baff8-173">Unggah file untuk SharePoint</span><span class="sxs-lookup"><span data-stu-id="baff8-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="baff8-174">Dari menu utama, klik **Project Service** > **Unggah**.</span><span class="sxs-lookup"><span data-stu-id="baff8-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="baff8-175">Pilih **Ke Dokumen Proyek Project service automation**.</span><span class="sxs-lookup"><span data-stu-id="baff8-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="baff8-176">Pada dialog **Aktifkan buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , pilih **ya** atau **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="baff8-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="baff8-177">Jika Anda mengklik **ya** Anda akan dapat memilih tombol **buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** di Project Service Automation, meluncurkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuat file proyek dari perpustakaan dokumen SharePoint.</span><span class="sxs-lookup"><span data-stu-id="baff8-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="baff8-178">Jika Anda mengklik **Tidak** , tautan **Buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan aktif.</span><span class="sxs-lookup"><span data-stu-id="baff8-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="baff8-179">File [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dapat ditemukan di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **dokumen** untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] spesifik.</span><span class="sxs-lookup"><span data-stu-id="baff8-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="baff8-180">Unggah file untuk Office Groups</span><span class="sxs-lookup"><span data-stu-id="baff8-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="baff8-181">Dari menu utama, klik **Project Service** > **Unggah**.</span><span class="sxs-lookup"><span data-stu-id="baff8-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="baff8-182">Pilih **Ke Dokumen Proyek Project service automation**.</span><span class="sxs-lookup"><span data-stu-id="baff8-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="baff8-183">Pada dialog **Aktifkan buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** , pilih **ya** atau **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="baff8-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="baff8-184">Jika Anda mengklik **ya** Anda akan dapat memilih tombol **buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** di Project Service Automation, meluncurkan [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan memuat file proyek dari perpustakaan dokumen SharePoint.</span><span class="sxs-lookup"><span data-stu-id="baff8-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="baff8-185">Jika Anda mengklik **Tidak** , tautan **Buka di [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** tidak akan aktif.</span><span class="sxs-lookup"><span data-stu-id="baff8-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="baff8-186">File [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dapat ditemukan di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di bawah **dokumen** untuk proyek [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] spesifik.</span><span class="sxs-lookup"><span data-stu-id="baff8-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="baff8-187">Mempublikasikan proyek Anda sebagai template</span><span class="sxs-lookup"><span data-stu-id="baff8-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="baff8-188">Anda dapat menyimpan proyek Anda dan menggunakannya kembali dengan menyimpannya sebagai template proyek di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="baff8-189">Template proyek adalah rencana proyek yang dapat digunakan kembali di [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="baff8-190">[Membuat template proyek (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="baff8-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="baff8-191">Dari tab **Project service** , klik **Terbitkan** > **Template proyek Project service automation baru**.</span><span class="sxs-lookup"><span data-stu-id="baff8-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="baff8-192">Di kotak dialog **Terbitkan ke sebuah proyek baru dalam template Project Service** , masukkan **nama template proyek**.</span><span class="sxs-lookup"><span data-stu-id="baff8-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="baff8-193">Bisa juga periksa **tautkan rencana proyek ke Project service automation** untuk menautkan file proyek ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="baff8-194">Klik **Terbitkan**.</span><span class="sxs-lookup"><span data-stu-id="baff8-194">Click **Publish**.</span></span>  

<span data-ttu-id="baff8-195">Menghubungkan file proyek ke [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] membuat file proyek sebagai master dan menetapkan struktur rincian kerja dalam template [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] menjadi baca-saja.</span><span class="sxs-lookup"><span data-stu-id="baff8-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="baff8-196">Untuk membuat perubahan rencana proyek, Anda harus membuat mereka dalam [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] dan mempublikasikan mereka sebagai pembaruan kepada [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="baff8-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="baff8-197">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="baff8-197">See Also</span></span>  
 [<span data-ttu-id="baff8-198">Panduan Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="baff8-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)

---
title: Memberikan estimasi kerja untuk sebuah proyek selama proses penjualan
description: Bagaimana memberikan estimasi kerja untuk sebuah proyek selama proses penjualan di Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ddb7f8c0ff8c7fd7e51edb42f9d227f2b91a811b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078534"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="d6b06-103">Memberikan estimasi kerja untuk sebuah proyek selama proses penjualan (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d6b06-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d6b06-104">Selama proses penjualan, Anda dapat melaksanakan perkiraan penjualan dari bawah dengan baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d6b06-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="d6b06-105">Kemampuan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] memberikan cara yang lebih ilmiah dan deterministik mendapatkan perkiraan penjualan dengan memecah item pekerjaan dan mengasosiasikan atribut relevan yang berkontribusi terhadap perkiraan untuk proyek dalam struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="d6b06-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="d6b06-106">Setelah Anda mendapatkan penjualan, Anda dapat menggunakan struktur rincian kerja terkait dalam rencana proyek Anda, menyempurnakannya sesuai kebutuhan untuk berhasil menyelesaikan proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="d6b06-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="d6b06-107">Tautkan proyek ke baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="d6b06-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="d6b06-108">Ketika membuat baris kuotasi berbasis proyek, Anda dapat membuat sebuah proyek baru dari baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d6b06-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="d6b06-109">Anda dapat menggunakan template proyek, yang adalah rencana proyek standar pra-konfigurasi maupun perkiraan keuangan yang umum untuk organisasi Anda, atau salinan rencana proyek dan perkiraan dari proyek masa lalu.</span><span class="sxs-lookup"><span data-stu-id="d6b06-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="d6b06-110">Ketika Anda membuat sebuah proyek, memilih template proyek menyediakan dasar untuk memperbaiki rencana proyek, perkiraan, dan persyaratan peran.</span><span class="sxs-lookup"><span data-stu-id="d6b06-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="d6b06-111">Dengan membuat proyek Anda dari kuotasi, proyek ini otomatis dikaitkan dengan baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d6b06-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="d6b06-112">Komponen perkiraan proyek</span><span class="sxs-lookup"><span data-stu-id="d6b06-112">Project estimate components</span></span>  
 <span data-ttu-id="d6b06-113">Struktur rincian kerja dalam proyek menyediakan cara untuk memecah kerja ke dalam tugas-tugas, mempertahankan hirarki tugas, dan menetapkan perkiraan usaha yang dibutuhkan untuk menyelesaikan setiap tugas.</span><span class="sxs-lookup"><span data-stu-id="d6b06-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="d6b06-114">Anda juga dapat mengaitkan peran dengan tugas untuk menunjukkan perkiraan jenis sumber daya yang diperlukan untuk menyelesaikan tugas dan jadwal.</span><span class="sxs-lookup"><span data-stu-id="d6b06-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="d6b06-115">Struktur rincian kerja membantu Anda menentukan usaha kerja dan perkiraan jadwal.</span><span class="sxs-lookup"><span data-stu-id="d6b06-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="d6b06-116">Secara default, proyek menggunakan daftar harga standar yang Anda tetapkan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="d6b06-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="d6b06-117">Harga penjualan dan biaya yang didefinisikan dalam daftar harga membantu menentukan perkiraan keuangan untuk rincian kerja proyek.</span><span class="sxs-lookup"><span data-stu-id="d6b06-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="d6b06-118">Jika proyek Anda terkait dengan kuotasi, dan kuotasi memiliki daftar harga yang berbeda dari default, daftar harga kuotasi itu digunakan untuk perkiraan keuangan.</span><span class="sxs-lookup"><span data-stu-id="d6b06-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="d6b06-119">Impor perkiraan dari sebuah proyek ke kuotasi</span><span class="sxs-lookup"><span data-stu-id="d6b06-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="d6b06-120">Setelah Anda memiliki perkiraan proyek dalam proyek, Anda dapat mengimpor perkiraan ini ke dalam baris kuotasi:</span><span class="sxs-lookup"><span data-stu-id="d6b06-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="d6b06-121">Dalam **rincian baris kuotasi** , klik **impor dari perkiraan**.</span><span class="sxs-lookup"><span data-stu-id="d6b06-121">In **Quote Line Details** , click **Import from estimates**.</span></span> 

-   <span data-ttu-id="d6b06-122">Pilih apakah mengimpor perkiraan proyek yang diringkas menurut jenis transaksi, peran atau tingkat node struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="d6b06-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="d6b06-123">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="d6b06-123">See Also</span></span>  
 [<span data-ttu-id="d6b06-124">Panduan Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="d6b06-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)

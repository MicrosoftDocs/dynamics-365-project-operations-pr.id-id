---
title: Panduan Manajer Sumber Daya
description: Panduan untuk manajemen sumber daya di Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752511"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="6f001-103">Panduan Manajer sumber daya (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6f001-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="6f001-104">Kemampuan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] membantu Anda menemukan sumber daya yang tepat pada waktu yang tepat untuk proyek yang benar dan memastikan semua sumber daya digunakan secara efisien.</span><span class="sxs-lookup"><span data-stu-id="6f001-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="6f001-105">Sebarkan konsultan perusahaan Anda secara efisien dan efektif dengan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="6f001-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="6f001-106">Ini menyediakan untuk Anda alat yang Anda butuhkan untuk menjadwalkan sumber daya berdasarkan persyaratan dan jadwal consulting proyek dan pada keterampilan dan ketersediaan konsultan Anda.</span><span class="sxs-lookup"><span data-stu-id="6f001-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="6f001-107">Anda dapat segera menemukan konsultan paling memenuhi syarat yang tersedia untuk bekerja pada proyek-proyek, dan Anda dapat dengan mudah melihat bagaimana lebih baik menjadwalkan mereka selama setiap proyek.</span><span class="sxs-lookup"><span data-stu-id="6f001-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="6f001-108">Penjadwalan sumber daya membantu Anda melakukan hal berikut:</span><span class="sxs-lookup"><span data-stu-id="6f001-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="6f001-109">Mencocokkan sumber daya untuk proyek-proyek, berdasarkan seberapa baik tingkat keterampilan dan kemahiran mereka sesuai dengan kebutuhan sumber daya proyek.</span><span class="sxs-lookup"><span data-stu-id="6f001-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="6f001-110">Menyesuaikan jadwal sumber daya untuk kalender proyek, berdasarkan ketersediaan dan waktu nonaktif yang dijadwalkan.</span><span class="sxs-lookup"><span data-stu-id="6f001-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="6f001-111">Kalendar berkode warna memberikan isyarat visual tentang ketersediaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="6f001-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="6f001-112">Kaji ulang kemampuan masing-masing konsultan dan tentukan bagaimana kapasitas saat ini digunakan.</span><span class="sxs-lookup"><span data-stu-id="6f001-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="6f001-113">Ini dapat membantu Anda menemukan mana konsultan yang mungkin kurang atau terlalu banyak digunakan, atau jika mereka bekerja pada kapasitas.</span><span class="sxs-lookup"><span data-stu-id="6f001-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="6f001-114">Tetapkan persentase atau jumlah tertentu jam untuk kapasitas pekerja untuk sebuah proyek.</span><span class="sxs-lookup"><span data-stu-id="6f001-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="6f001-115">Buat pemesanan sumber daya grup.</span><span class="sxs-lookup"><span data-stu-id="6f001-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="6f001-116">Pesan dengan pasti atau tentatif sumber daya, dan konversi jam pesanan tentatif menjadi jam pasti dalam satu langkah.</span><span class="sxs-lookup"><span data-stu-id="6f001-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="6f001-117">Secara otomatis bentuk tim proyek berdasarkan sumber daya yang didefinisikan dalam struktur rincian kerja untuk sebuah proyek.</span><span class="sxs-lookup"><span data-stu-id="6f001-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="6f001-118">Penuhi permintaan sumber daya (memesan, mengusulkan, menemukan pengganti sumber daya).</span><span class="sxs-lookup"><span data-stu-id="6f001-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="6f001-119">Tetapkan sumber daya menurut model Pusat (manajer sumber daya menetapkan) atau model hibrida (manajer sumber daya dan manajer lain dapat menetapkan).</span><span class="sxs-lookup"><span data-stu-id="6f001-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="6f001-120">Untuk informasi lebih lanjut tentang cara mengatur model manajemen sumber daya sentral dibandingkan hibrida, lihat [mengkonfigurasi pengaturan parameter tambahan (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="6f001-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="6f001-121">Anda dapat mengelola sumber daya secara efisien di seluruh proyek dan memastikan bahwa proyek dikelola dengan tepat.</span><span class="sxs-lookup"><span data-stu-id="6f001-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="6f001-122">Anda harus melakukan tugas berikut:</span><span class="sxs-lookup"><span data-stu-id="6f001-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="6f001-123">[Kelola Permintaan Sumber Daya](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="6f001-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="6f001-124">Menyesuaikan keahlian dan kemahiran konsultan Anda untuk proyek-proyek yang tepat.</span><span class="sxs-lookup"><span data-stu-id="6f001-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="6f001-125">[Lihat ketersediaan sumber daya](../project-service/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="6f001-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="6f001-126">Memeriksa ketersediaan konsultan dalam tampilan kalender.</span><span class="sxs-lookup"><span data-stu-id="6f001-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="6f001-127">[Lihat Pemanfaatan Sumber Daya](../project-service/view-resource-utilization.md).</span><span class="sxs-lookup"><span data-stu-id="6f001-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="6f001-128">Melihat persentase waktu konsultan Anda yang sedang dipesan.</span><span class="sxs-lookup"><span data-stu-id="6f001-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="6f001-129">[Jadwalkan sumber daya untuk sebuah proyek](../project-service/schedule-resources-project.md).</span><span class="sxs-lookup"><span data-stu-id="6f001-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="6f001-130">Jadwalkan konsultan untuk sebuah proyek.</span><span class="sxs-lookup"><span data-stu-id="6f001-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="6f001-131">Untuk informasi lebih lanjut tentang mengirimkan permintaan sumber daya untuk proyek-proyek individu, lihat [Ajukan permintaan sumber daya](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="6f001-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="6f001-132">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="6f001-132">See Also</span></span>  
 <span data-ttu-id="6f001-133">[Ikhtisar Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="6f001-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="6f001-134">[Panduan Administrator](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6f001-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="6f001-135">[Panduan Manajer Akun](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6f001-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="6f001-136">[Panduan Manajer Proyek](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="6f001-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="6f001-137">Panduan Waktu, biaya dan kolaborasi</span><span class="sxs-lookup"><span data-stu-id="6f001-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)

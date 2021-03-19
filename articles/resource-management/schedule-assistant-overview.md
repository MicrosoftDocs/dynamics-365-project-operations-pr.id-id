---
title: Sekilas asisten jadwal
description: Topik ini menyediakan informasi tentang cara menangani asisten jadwal untuk memesan sumber daya.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279232"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="90215-103">Sekilas asisten jadwal</span><span class="sxs-lookup"><span data-stu-id="90215-103">Schedule assistant overview</span></span>

<span data-ttu-id="90215-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="90215-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="90215-105">Asisten jadwal digunakan untuk memesan sumber daya berdasarkan persyaratan yang ditentukan oleh manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="90215-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="90215-106">Asisten jadwal bergantung pada parameter yang diberikan dalam persyaratan sumber daya untuk menemukan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="90215-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="90215-107">Asisten jadwal merekomendasikan sumber daya yang sesuai dengan persyaratan yang relevan, seperti periode waktu atau keterampilan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="90215-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="90215-108">Setelah sumber daya yang sesuai diidentifikasi, manajer sumber daya atau proyek dapat memesan sumber daya untuk pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="90215-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="90215-109">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="90215-109">Prerequisites</span></span>

<span data-ttu-id="90215-110">Asisten jadwal adalah bagian dari solusi Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="90215-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="90215-111">Solusi ini disertakan dan diinstal dengan Dynamics 365 Project Operations, Dynamics 365 Field Service, dan Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="90215-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="90215-112">Menyesuaikan persyaratan dengan sumber daya</span><span class="sxs-lookup"><span data-stu-id="90215-112">Matching requirements and resources</span></span>

<span data-ttu-id="90215-113">Persyaratan sumber daya yang dihasilkan didasarkan pada rincian seperti:</span><span class="sxs-lookup"><span data-stu-id="90215-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="90215-114">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="90215-114">Characteristics</span></span>
-   <span data-ttu-id="90215-115">Peran</span><span class="sxs-lookup"><span data-stu-id="90215-115">Roles</span></span>
-   <span data-ttu-id="90215-116">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="90215-116">Business units</span></span>
-   <span data-ttu-id="90215-117">Preferensi Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="90215-117">Resource preferences</span></span>
-   <span data-ttu-id="90215-118">Kontur usaha</span><span class="sxs-lookup"><span data-stu-id="90215-118">Effort contours</span></span>
-   <span data-ttu-id="90215-119">Zona waktu</span><span class="sxs-lookup"><span data-stu-id="90215-119">Time zone</span></span>

<span data-ttu-id="90215-120">Asisten jadwal menggunakan rincian ini untuk memfilter sumber daya.</span><span class="sxs-lookup"><span data-stu-id="90215-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="90215-121">Luncurkan Asisten Jadwal</span><span class="sxs-lookup"><span data-stu-id="90215-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="90215-122">Ada dua cara di mana asisten jadwal diluncurkan.</span><span class="sxs-lookup"><span data-stu-id="90215-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="90215-123">Jika Anda menggunakan mode hibrida, di kisi anggota tim, Anda dapat memilih anggota tim dengan persyaratan sumber daya yang tidak terpenuhi, lalu memilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="90215-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="90215-124">Jika Anda menggunakan mode pusat, manajer sumber daya mencari dan memilih sumber daya.</span><span class="sxs-lookup"><span data-stu-id="90215-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="90215-125">Filter Asisten Jadwal</span><span class="sxs-lookup"><span data-stu-id="90215-125">Schedule assistant filters</span></span>

<span data-ttu-id="90215-126">Setelah menjalankan asisten jadwal, rincian dari persyaratan sumber daya ditampilkan sebagai nilai terfilter di panel kiri.</span><span class="sxs-lookup"><span data-stu-id="90215-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="90215-127">Manajer sumber daya atau manajer proyek dapat menyempurnakan hasil dengan menyesuaikan filter untuk memenuhi kebutuhan penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="90215-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="90215-128">Panel filter menampilkan pilihan yang terkait dengan pekerjaan, termasuk:</span><span class="sxs-lookup"><span data-stu-id="90215-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="90215-129">Awal dan akhir kerja</span><span class="sxs-lookup"><span data-stu-id="90215-129">Work start and end</span></span>
-   <span data-ttu-id="90215-130">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="90215-130">Characteristics</span></span>
-   <span data-ttu-id="90215-131">Peran</span><span class="sxs-lookup"><span data-stu-id="90215-131">Roles</span></span>
-   <span data-ttu-id="90215-132">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="90215-132">Organizational units</span></span>
-   <span data-ttu-id="90215-133">Perusahaan Pencari Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="90215-133">Resourcing company</span></span>
-   <span data-ttu-id="90215-134">Jenis Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="90215-134">Resource types</span></span>
-   <span data-ttu-id="90215-135">Sumber Daya Pilihan</span><span class="sxs-lookup"><span data-stu-id="90215-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
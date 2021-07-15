---
title: Sekilas asisten jadwal
description: Topik ini menyediakan informasi tentang cara menangani asisten jadwal untuk memesan sumber daya.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 83583c97e4ecb5f1fdc0d8d98098afe8e12d27e4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368120"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="70cb2-103">Sekilas asisten jadwal</span><span class="sxs-lookup"><span data-stu-id="70cb2-103">Schedule assistant overview</span></span>

<span data-ttu-id="70cb2-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="70cb2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70cb2-105">Asisten jadwal digunakan untuk memesan sumber daya berdasarkan persyaratan yang ditentukan oleh manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="70cb2-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="70cb2-106">Asisten jadwal bergantung pada parameter yang diberikan dalam persyaratan sumber daya untuk menemukan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="70cb2-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="70cb2-107">Asisten jadwal merekomendasikan sumber daya yang sesuai dengan persyaratan yang relevan, seperti periode waktu atau keterampilan yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="70cb2-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="70cb2-108">Setelah sumber daya yang sesuai diidentifikasi, manajer sumber daya atau proyek dapat memesan sumber daya untuk pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="70cb2-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="70cb2-109">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="70cb2-109">Prerequisites</span></span>

<span data-ttu-id="70cb2-110">Asisten jadwal adalah bagian dari solusi Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="70cb2-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="70cb2-111">Solusi ini disertakan dan diinstal dengan Dynamics 365 Project Operations, Dynamics 365 Field Service, dan Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="70cb2-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="70cb2-112">Menyesuaikan persyaratan dengan sumber daya</span><span class="sxs-lookup"><span data-stu-id="70cb2-112">Matching requirements and resources</span></span>

<span data-ttu-id="70cb2-113">Persyaratan sumber daya yang dihasilkan didasarkan pada rincian seperti:</span><span class="sxs-lookup"><span data-stu-id="70cb2-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="70cb2-114">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="70cb2-114">Characteristics</span></span>
-   <span data-ttu-id="70cb2-115">Peran</span><span class="sxs-lookup"><span data-stu-id="70cb2-115">Roles</span></span>
-   <span data-ttu-id="70cb2-116">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="70cb2-116">Business units</span></span>
-   <span data-ttu-id="70cb2-117">Preferensi Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="70cb2-117">Resource preferences</span></span>
-   <span data-ttu-id="70cb2-118">Kontur usaha</span><span class="sxs-lookup"><span data-stu-id="70cb2-118">Effort contours</span></span>
-   <span data-ttu-id="70cb2-119">Zona waktu</span><span class="sxs-lookup"><span data-stu-id="70cb2-119">Time zone</span></span>

<span data-ttu-id="70cb2-120">Asisten jadwal menggunakan rincian ini untuk memfilter sumber daya.</span><span class="sxs-lookup"><span data-stu-id="70cb2-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="70cb2-121">Luncurkan Asisten Jadwal</span><span class="sxs-lookup"><span data-stu-id="70cb2-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="70cb2-122">Ada dua cara di mana asisten jadwal diluncurkan.</span><span class="sxs-lookup"><span data-stu-id="70cb2-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="70cb2-123">Jika Anda menggunakan mode hibrida, di kisi anggota tim, Anda dapat memilih anggota tim dengan persyaratan sumber daya yang tidak terpenuhi, lalu memilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="70cb2-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="70cb2-124">Jika Anda menggunakan mode pusat, manajer sumber daya mencari dan memilih sumber daya.</span><span class="sxs-lookup"><span data-stu-id="70cb2-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="70cb2-125">Filter Asisten Jadwal</span><span class="sxs-lookup"><span data-stu-id="70cb2-125">Schedule assistant filters</span></span>

<span data-ttu-id="70cb2-126">Setelah menjalankan asisten jadwal, rincian dari persyaratan sumber daya ditampilkan sebagai nilai terfilter di panel kiri.</span><span class="sxs-lookup"><span data-stu-id="70cb2-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="70cb2-127">Manajer sumber daya atau manajer proyek dapat menyempurnakan hasil dengan menyesuaikan filter untuk memenuhi kebutuhan penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="70cb2-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="70cb2-128">Panel filter menampilkan pilihan yang terkait dengan pekerjaan, termasuk:</span><span class="sxs-lookup"><span data-stu-id="70cb2-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="70cb2-129">Awal dan akhir kerja</span><span class="sxs-lookup"><span data-stu-id="70cb2-129">Work start and end</span></span>
-   <span data-ttu-id="70cb2-130">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="70cb2-130">Characteristics</span></span>
-   <span data-ttu-id="70cb2-131">Peran</span><span class="sxs-lookup"><span data-stu-id="70cb2-131">Roles</span></span>
-   <span data-ttu-id="70cb2-132">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="70cb2-132">Organizational units</span></span>
-   <span data-ttu-id="70cb2-133">Perusahaan Pencari Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="70cb2-133">Resourcing company</span></span>
-   <span data-ttu-id="70cb2-134">Jenis Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="70cb2-134">Resource types</span></span>
-   <span data-ttu-id="70cb2-135">Sumber Daya Pilihan</span><span class="sxs-lookup"><span data-stu-id="70cb2-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
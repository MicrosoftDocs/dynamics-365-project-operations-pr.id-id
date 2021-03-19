---
title: Buat tim proyek
description: Topik ini menyediakan informasi tentang cara membuat dan mengeluarkan tim proyek.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270862"
---
# <a name="create-a-project-team"></a><span data-ttu-id="04fc6-103">Membuat tim proyek</span><span class="sxs-lookup"><span data-stu-id="04fc6-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04fc6-104">Untuk menggunakan peran yang sebelumnya diatur dalam proyek, manajer proyek harus mengaitkan peran dengan proyek.</span><span class="sxs-lookup"><span data-stu-id="04fc6-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="04fc6-105">Peran ganda dapat ditetapkan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="04fc6-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="04fc6-106">Untuk mencegah kebingungan, peran ini akan secara otomatis dilabeli saat reservasi.</span><span class="sxs-lookup"><span data-stu-id="04fc6-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="04fc6-107">Misalnya, jika manajer proyek memerlukan tiga insinyur perangkat lunak, tiga peran insinyur perangkat lunak yang memiliki label **insinyur perangkat lunak 1**, **insinyur perangkat lunak 2**, dan **insinyur perangkat lunak 3** yang akan dibuat secara otomatis.</span><span class="sxs-lookup"><span data-stu-id="04fc6-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="04fc6-108">Jika karakteristik peran sebelumnya diatur untuk peran, peran akan diterapkan sebagai filter selama pencarian untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="04fc6-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="04fc6-109">Karakteristik tambahan dapat ditambahkan sebagaimana diperlukan untuk lebih menyempurnakan pencarian.</span><span class="sxs-lookup"><span data-stu-id="04fc6-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="04fc6-110">Pengaturan tampilan juga dapat disesuaikan untuk memberikan tampilan yang lebih baik ketersediaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="04fc6-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="04fc6-111">Tersedia pilihan untuk menampilkan ketersediaan per jam, harian, mingguan, bulanan, kuartalan, dan tahunan.</span><span class="sxs-lookup"><span data-stu-id="04fc6-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="04fc6-112">Ada juga pilihan untuk menunjukkan kapasitas yang tersedia dan tersisa pada sumber daya.</span><span class="sxs-lookup"><span data-stu-id="04fc6-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="04fc6-113">Pilihan ini berguna untuk manajemen waktu, saat Anda memperkirakan waktu yang tersedia untuk aktivitas atau ketersediaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="04fc6-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="04fc6-114">Manajer proyek dapat memilih peran pada halaman dan kemudian, jika ada sumber daya yang tersedia yang sesuai dengan persyaratan, pilih untuk mencadangkan sumber daya untuk mengisi peran.</span><span class="sxs-lookup"><span data-stu-id="04fc6-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="04fc6-115">Perhatikan bahwa sumber daya tidak harus dicadangkan pada saat ini dalam tahap perencanaan.</span><span class="sxs-lookup"><span data-stu-id="04fc6-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="04fc6-116">Bila Anda membuat WBS, Anda dapat mengganti peran dengan sumber daya staf untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="04fc6-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="04fc6-117">Jika peran diganti dengan sumber daya staf di WBS, pengaturan sumber daya secara otomatis memperbarui daftar tim proyek dan penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="04fc6-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="04fc6-118">[![Daftar tim proyek yang mencakup peran dan sumber daya aktual](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="04fc6-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="04fc6-119">Manajer Proyek memiliki berbagai pilihan untuk memesan sumber daya untuk proyek, seperti **kapasitas yang tersisa**, **kapasitas penuh**, **persentase kapasitas**, dan **Tentukan jam**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="04fc6-120">Pilihan Pemesanan ini dapat dibatalkan sewaktu-waktu jika tugas sumber daya berubah.</span><span class="sxs-lookup"><span data-stu-id="04fc6-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="04fc6-121">Dua jenis Pemesanan yang didukung:</span><span class="sxs-lookup"><span data-stu-id="04fc6-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="04fc6-122">**Definitif** -sumber daya reservasi disetujui dan dikonfirmasi untuk bekerja pada keterlibatan untuk durasi yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="04fc6-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="04fc6-123">**Tentatif** - Reservasi sumber daya diatur secara tentatif untuk bekerja pada keterlibatan untuk durasi yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="04fc6-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="04fc6-124">Prosedur berikut menjelaskan cara membuat tim proyek.</span><span class="sxs-lookup"><span data-stu-id="04fc6-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="04fc6-125">Membuat tim proyek</span><span class="sxs-lookup"><span data-stu-id="04fc6-125">Create a project team</span></span>

1. <span data-ttu-id="04fc6-126">Pada halaman daftar **semua proyek**, pilih proyek, lalu pilih **Edit**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="04fc6-127">Pada tab **tim proyek dan penjadwalan**, di bidang **tanggal akhir jadwal**, masukkan tanggal mulai jadwal ditambah satu bulan.</span><span class="sxs-lookup"><span data-stu-id="04fc6-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="04fc6-128">Misalnya, jika tanggal mulai jadwal adalah 24 Juni 2017 (24/06/2017), masukkan **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="04fc6-129">Pilih **Tambahkan**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-129">Select **Add**.</span></span>
4. <span data-ttu-id="04fc6-130">Di panel **Tambah peran ke proyek**, di bidang **peran**, pilih **manajer proyek senior**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="04fc6-131">Pilih **kompetensi yang diperlukan**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="04fc6-132">Pada halaman **Pilih karakteristik**, karakteristik yang telah Anda atur untuk peran senior manajer proyek dipilih secara default.</span><span class="sxs-lookup"><span data-stu-id="04fc6-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="04fc6-133">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-133">Select **OK**.</span></span>
7. <span data-ttu-id="04fc6-134">Pada halaman **Tambah peran ke proyek**, di bidang **jumlah sumber daya**, masukkan **1**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="04fc6-135">Di bidang **sumber daya**, pencarian menampilkan semua sumber daya yang memiliki kompetensi yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="04fc6-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="04fc6-136">Pilih **Daniel Goldschmidt**, lalu pilih **buat**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="04fc6-137">Pada halaman **Proyek**, pilih **Tambah**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="04fc6-138">Di panel **Tambah peran ke proyek**, di bidang **peran**, pilih **Anggota tim**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="04fc6-139">Di bidang **Jumlah sumber daya**, masukkan **5**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="04fc6-140">Pilih **Buat**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-140">Select **Create**.</span></span>
12. <span data-ttu-id="04fc6-141">Pada halaman **proyek**, pilih **penuhi sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="04fc6-142">Memantau tim proyek</span><span class="sxs-lookup"><span data-stu-id="04fc6-142">Monitor project teams</span></span>
1. <span data-ttu-id="04fc6-143">Pada halaman **semua proyek**, pilih tautan **ID proyek** untuk proyek **peningkatan XYZ fase 2**.</span><span class="sxs-lookup"><span data-stu-id="04fc6-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="04fc6-144">Pada FastTab **tim proyek dan penjadwalan**, Verifikasikan bahwa sumber daya proyek yang tercantum sudah benar.</span><span class="sxs-lookup"><span data-stu-id="04fc6-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Buat proyek baru
description: Topik ini menyediakan informasi tentang cara membuat proyek baru.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b29340dc88aea888ea2f5ea975eaea59d014279
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270727"
---
# <a name="create-a-new-project"></a><span data-ttu-id="b5c1d-103">Buat proyek baru</span><span class="sxs-lookup"><span data-stu-id="b5c1d-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5c1d-104">Selesaikan langkah-langkah berikut untuk membuat proyek baru.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="b5c1d-105">Di **Manajemen proyek**, pilih **Proyek baru** dan masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="b5c1d-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="b5c1d-106">**Jenis proyek:** waktu dan material</span><span class="sxs-lookup"><span data-stu-id="b5c1d-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="b5c1d-107">**Nama proyek:** Peningkatan XYZ fase 2</span><span class="sxs-lookup"><span data-stu-id="b5c1d-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="b5c1d-108">**Grup proyek:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="b5c1d-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="b5c1d-109">**ID Kontrak Proyek:** 00000002</span><span class="sxs-lookup"><span data-stu-id="b5c1d-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="b5c1d-110">Pilih **Buat proyek baru**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="b5c1d-111">Menetapkan sumber daya untuk proyek</span><span class="sxs-lookup"><span data-stu-id="b5c1d-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="b5c1d-112">Pada halaman **pekerja**, dalam **Daftar pekerja**, pilih rekaman untuk pekerja yang sebelumnya Anda konfigurasikan kompetensinya, dan buka rekaman pekerja.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="b5c1d-113">Pada panel tindakan, pada tab **Proyek**, di grup **Konfigurasi**, pilih **tetapkan proyek**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="b5c1d-114">Pada halaman **penugasan proyek validasi sumber daya**, pada tab **proyek**, di bidang **Tambah proyek ke proyek yang dipilih**, filter proyek **Peningkatan XYZ fase 2**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="b5c1d-115">Di panel **proyek lainnya**, pilih proyek, lalu pilih tombol panah untuk menambahkannya ke panel **proyek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="b5c1d-116">Anda juga dapat menetapkan kategori untuk sumber daya sesuai kebutuhan.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="b5c1d-117">Jenis kategori adalah **biaya** atau **pendapatan**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="b5c1d-118">Jenis kategori ditentukan oleh organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-118">The category type is determined by your organization.</span></span> <span data-ttu-id="b5c1d-119">Jika tidak ada kategori yang ditetapkan untuk sumber daya, Finance akan mencari kategori default pada harga jam untuk biaya dan pendapatan.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="b5c1d-120">Konfigurasi sumber daya proyek dan karakteristik peran</span><span class="sxs-lookup"><span data-stu-id="b5c1d-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="b5c1d-121">Manajer proyek dapat menggunakan fungsi sumber daya proyek untuk membuat peran yang diperlukan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="b5c1d-122">Peran dapat digunakan jika sumber daya terkonfirmasi masih belum diketahui saat sumber daya dicadangkan.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="b5c1d-123">Peran dapat sementara dicadangkan sebagai sumber daya yang direncanakan, sehingga Anda dapat melanjutkan tahapan Perencanaan proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="b5c1d-124">[![Contoh peran](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="b5c1d-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="b5c1d-125">**Skenario:** Aswono dipekerjakan untuk menyelesaikan proyek waktu dan material yang memiliki Piagam proyek disetujui.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="b5c1d-126">Manajer Proyek Junior masih menyelesaikan cakupan proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="b5c1d-127">Manajer sumber daya saat ini mengidentifikasi sumber daya tertentu yang akan dicadangkan untuk mengerjakan proyek baru.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="b5c1d-128">Karena sifat penting proyek, sponsor proyek meminta manajer proyek senior sebagai salah satu peran.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="b5c1d-129">Manajer sumber daya harus mendapatkan sumber daya baru dan menentukan peran dalam sistem seandainya manajer proyek Junior memerlukan informasi sumber daya selama perencanaan proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="b5c1d-130">Langkah-langkah berikut ini menunjukkan cara manajer sumber daya dapat mengkonfigurasi peran manajer proyek senior dan mengaitkan karakteristik sumber daya dengannya.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="b5c1d-131">Selanjutnya, peran dapat digunakan untuk mencari sumber daya yang tersedia yang sesuai dengan kompetensi sumber daya yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="b5c1d-132">Di **Konfigurasi Peran**, pilih **baru** dan masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="b5c1d-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b5c1d-133">**ID peran:** manajer proyek senior</span><span class="sxs-lookup"><span data-stu-id="b5c1d-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="b5c1d-134">**Deskripsi:** manajer proyek senior</span><span class="sxs-lookup"><span data-stu-id="b5c1d-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="b5c1d-135">Pilih **Buat**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-135">Select **Create**.</span></span>
3. <span data-ttu-id="b5c1d-136">Pilih peran **manajer proyek senior**, lalu pilih **Konfigurasikan karakteristik**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="b5c1d-137">Di bidang **Jenis karakteristik**, pilih **Keterampilan**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="b5c1d-138">Di bidang **Karakteristik yang tersedia**, masukkan keterampilan yang akan dicari.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="b5c1d-139">Di bidang **Jenis karakteristik**, pilih **sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="b5c1d-140">Di bidang **Karakteristik yang tersedia**, masukkan jenis sertifikat yang akan dicari.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="b5c1d-141">Menetapkan sumber daya proyek untuk proyek</span><span class="sxs-lookup"><span data-stu-id="b5c1d-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="b5c1d-142">Pada halaman **semua proyek**, pilih proyek **peningkatan XYZ fase 2**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="b5c1d-143">Pada tab **tim proyek dan penjadwalan**, pilih **Tambah**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="b5c1d-144">Di bidang **peran**, pilih **anggota tim**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="b5c1d-145">Pilih **Pesan dari kalender**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="b5c1d-146">Pada halaman **ketersediaan sumber daya**, pilih **lihat pengaturan**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="b5c1d-147">Pada halaman **Atur pengaturan tampilan**, masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="b5c1d-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="b5c1d-148">**Format untuk tampilan rentang tanggal:** Hari</span><span class="sxs-lookup"><span data-stu-id="b5c1d-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="b5c1d-149">**Tampilkan deskripsi ketersediaan:** ya</span><span class="sxs-lookup"><span data-stu-id="b5c1d-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="b5c1d-150">**Menampilkan kapasitas tersisa:** ya</span><span class="sxs-lookup"><span data-stu-id="b5c1d-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="b5c1d-151">Di daftar sumber daya, pilih sumber daya.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="b5c1d-152">Pilih **Definitif** dan **kapasitas penuh**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="b5c1d-153">Menetapkan sumber daya ke peran keamanan</span><span class="sxs-lookup"><span data-stu-id="b5c1d-153">Assign a resource to a default role</span></span>

<span data-ttu-id="b5c1d-154">Untuk membantu manajer proyek atau sumber daya dapat menelusuri dengan detail lebih lanjut tentang sumber daya yang dapat dicadangkan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="b5c1d-155">Anda dapat mengaitkan peran default dengan sumber daya yang ada atau sumber daya yang baru diperoleh.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="b5c1d-156">Misalnya, ketika Daniel dipekerjakan, dia memiliki pengalaman dan keterampilan untuk mengisi peran analis bisnis.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="b5c1d-157">Manajer sumber daya menetapkan peran ini sebagai peran default Daniel.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="b5c1d-158">Oleh karena itu, manajer sumber daya menambahkan Daniel ke kumpulan analis bisnis yang tersedia untuk bekerja pada proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="b5c1d-159">Selama reservasi sumber daya, manajer proyek dapat memfilter sumber daya peran yang tersedia untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="b5c1d-160">Mereka dapat menggunakan informasi ini sebagai salah satu kriteria saat mereka melakukan analisis keputusan multi-kriteria selama pemenuhan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="b5c1d-161">Mereka juga dapat menambahkan karakteristik sumber daya lain ke filter untuk mencari sumber daya yang memiliki keterampilan khusus, pendidikan, dan pengalaman untuk proyek tertentu.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="b5c1d-162">**Skenario:** proyek yang disetujui telah dimulai, dan peran manajer proyek senior dicadangkan sebagai sumber daya yang direncanakan selama tahap perencanaan proyek.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="b5c1d-163">Manajer sumber daya sekarang memperoleh sumber daya untuk memenuhi peran manajer proyek senior.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="b5c1d-164">Pada halaman **daftar sumber daya**, pilih **Daniel goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="b5c1d-165">Di **Peran sumber daya**, pilih **baru** dan masukkan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="b5c1d-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b5c1d-166">**Efektif:** masukkan tanggal saat ini.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="b5c1d-167">**Kedaluwarsa:** Masukkan **tidak pernah**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="b5c1d-168">**Peran:** Masukkan **manajer proyek senior**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="b5c1d-169">Pilih **Simpan**, lalu tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="b5c1d-170">Pada tab **kompetensi**, tambahkan Keterampilan **projectmgmt** dan sertifikat **PMP**.</span><span class="sxs-lookup"><span data-stu-id="b5c1d-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Konfigurasi sumber daya proyek
description: Topik ini menyediakan informasi tentang konfigurasi atau permintaan sumber daya proyek.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997695"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="e0df0-103">Konfigurasi sumber daya proyek</span><span class="sxs-lookup"><span data-stu-id="e0df0-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e0df0-104">Anda harus mengkonfigurasi kalender dan mengaitkannya dengan karyawan atau pekerja.</span><span class="sxs-lookup"><span data-stu-id="e0df0-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="e0df0-105">Kalender digunakan untuk menjadwalkan proyek dan waktu kerja sumber daya yang dicadangkan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="e0df0-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="e0df0-106">Selama pengaturan kalender, manajer proyek dapat melakukan perataan sumber daya sebagai bagian dari pengoptimalan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e0df0-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="e0df0-107">Berdasarkan jadwal kalender, pembatasan dapat diletakkan pada sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e0df0-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="e0df0-108">Anda dapat mengkonfigurasi kalender di halaman **kalender**.</span><span class="sxs-lookup"><span data-stu-id="e0df0-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="e0df0-109">Bila Anda mengkonfigurasi pekerja sebagai sumber daya proyek, Anda dapat memilih dari pekerja yang bekerja di perusahaan yang akan Anda siapkan sumber dayanya.</span><span class="sxs-lookup"><span data-stu-id="e0df0-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="e0df0-110">Atau, Anda dapat memilih pekerja dari perusahaan lain di organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="e0df0-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="e0df0-111">Pekerja ini disebut sebagai sumber daya antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="e0df0-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="e0df0-112">Prosedur berikut menjelaskan cara mengkonfigurasi pekerja sebagai sumber daya proyek di perusahaan Anda dan cara mengkonfigurasi sumber daya proyek antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="e0df0-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="e0df0-113">Mengkonfigurasi pekerja sebagai sumber daya proyek</span><span class="sxs-lookup"><span data-stu-id="e0df0-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="e0df0-114">Pada halaman **pekerja**, dalam **Daftar pekerja**, pilih pekerja yang Anda tambahkan sebagai sumber daya proyek, dan buka rekaman pekerja.</span><span class="sxs-lookup"><span data-stu-id="e0df0-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="e0df0-115">Pada panel tindakan, pilih **proyek** &gt; **konfigurasi** &gt; **Konfigurasi proyek**.</span><span class="sxs-lookup"><span data-stu-id="e0df0-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="e0df0-116">Pilih kalender, lalu tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="e0df0-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="e0df0-117">Anda juga dapat menentukan proyek default untuk sumber daya sebagai jenis pra-penugasan.</span><span class="sxs-lookup"><span data-stu-id="e0df0-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="e0df0-118">Pra-penugasan dapat digunakan saat manajer sumber daya atau manajer proyek mengetahui proyek yang akan dikerjakan oleh sumber daya sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e0df0-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="e0df0-119">Pra-penugasan juga dapat didasarkan pada permintaan sponsor proyek atau pelanggan.</span><span class="sxs-lookup"><span data-stu-id="e0df0-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="e0df0-120">Untuk melakukan pra-penugasan proyek, pada halaman **Tugaskan proyek**, pada tab **proyek**, dalam **Daftar proyek yang tersisa**, pilih proyek yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="e0df0-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="e0df0-121">Mengkonfigurasi sumber daya Antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="e0df0-121">Set up an intercompany resource</span></span>

<span data-ttu-id="e0df0-122">Bila Anda mengkonfigurasi pekerja sebagai sumber daya antar, Anda harus menyelesaikan konfigurasi di perusahaan pemberi yang eminjamkan dan perusahaan yang meminjam.</span><span class="sxs-lookup"><span data-stu-id="e0df0-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="e0df0-123">Di perusahaan yang meminjamkan</span><span class="sxs-lookup"><span data-stu-id="e0df0-123">In the lending company</span></span>

1. <span data-ttu-id="e0df0-124">Dalam Finance, verifikasikan bahwa perusahaan yang meminjamkan dipilih, lalu selesaikan prosedur di bagian sebelumnya, "Atur pekerja sebagai sumber daya proyek."</span><span class="sxs-lookup"><span data-stu-id="e0df0-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="e0df0-125">Pada halaman **Akuntansi antarperusahaan**, pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="e0df0-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="e0df0-126">Di bidang **id entitas hukum**, pilih perusahaan yang meminjamkan.</span><span class="sxs-lookup"><span data-stu-id="e0df0-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="e0df0-127">Isi bidang tersisa sebagaimana dibutuhkan, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e0df0-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="e0df0-128">Pada halaman **Transfer harga**, pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="e0df0-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="e0df0-129">Di bidang **Entitas hukum yang meminjam**, pilih perusahaan yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="e0df0-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="e0df0-130">Untuk meminjamkan pada perusahaan yang meminjam, hanya sumber daya yang Anda buat di awal bagian ini, di bidang **sumber daya**, pilih nama sumber daya yang Anda buat.</span><span class="sxs-lookup"><span data-stu-id="e0df0-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="e0df0-131">Untuk membuat semua sumber daya di perusahaan pinjaman yang tersedia untuk perusahaan pinjaman, biarkan bidang **sumber daya** kosong.</span><span class="sxs-lookup"><span data-stu-id="e0df0-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="e0df0-132">Pada halaman **manajemen proyek dan parameter akuntansi**, pada tab **Antarperusahaan**, atur pilihan **Aktifkan penjadwalan sumber daya dan lembar waktu** ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="e0df0-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="e0df0-133">Di perusahaan yang meminjam</span><span class="sxs-lookup"><span data-stu-id="e0df0-133">In the borrowing company</span></span>

- <span data-ttu-id="e0df0-134">Pada halaman **daftar sumber daya**, di filter pencarian, masukkan nama sumber daya yang Anda buat untuk perusahaan yang eminjamkan, untuk memverifikasi bahwa nama tersebut tercakup dalam daftar sumber daya untuk perusahaan yang meminjam.</span><span class="sxs-lookup"><span data-stu-id="e0df0-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="e0df0-135">Meminta sumber daya proyek</span><span class="sxs-lookup"><span data-stu-id="e0df0-135">Request project resources</span></span>
<span data-ttu-id="e0df0-136">Fungsi untuk penjadwalan sumber daya proyek hanya memungkinkan manajer sumber daya mendistribusikan sumber daya pada keterlibatan atau proyek.</span><span class="sxs-lookup"><span data-stu-id="e0df0-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="e0df0-137">Untuk mengaktifkan fungsi ini, selesaikan tugas berikut, atau Verifikasikan bahwa mereka telah selesai:</span><span class="sxs-lookup"><span data-stu-id="e0df0-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="e0df0-138">Atur urutan nomor.</span><span class="sxs-lookup"><span data-stu-id="e0df0-138">Set up number sequences.</span></span>
- <span data-ttu-id="e0df0-139">Konfigurasikan manajemen proyek dan alur kerja akuntansi.</span><span class="sxs-lookup"><span data-stu-id="e0df0-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="e0df0-140">Aktifkan alur kerja permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e0df0-140">Enable resource request workflows.</span></span>

<span data-ttu-id="e0df0-141">Setelah tugas sebelumnya selesai, Anda dapat menyelesaikan tugas berikut saat memerlukan:</span><span class="sxs-lookup"><span data-stu-id="e0df0-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="e0df0-142">Buat permintaan sumber daya dari sumber daya staf yang dipesan dengan tentatif.</span><span class="sxs-lookup"><span data-stu-id="e0df0-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="e0df0-143">Memantau permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e0df0-143">Monitor resource requests.</span></span>
- <span data-ttu-id="e0df0-144">Memenuhi permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e0df0-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="e0df0-145">Meminta staf sumber daya dari WBS.</span><span class="sxs-lookup"><span data-stu-id="e0df0-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="e0df0-146">Memesan sumber daya ke proyek tanpa meminta sumber daya staf.</span><span class="sxs-lookup"><span data-stu-id="e0df0-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
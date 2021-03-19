---
title: Kinerja penjadwalan sumber daya proyek
description: Topik ini menyediakan informasi tentang cara meningkatkan kinerja penjadwalan sumber daya untuk sejumlah besar proyek.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289013"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="e7070-103">Kinerja penjadwalan sumber daya proyek</span><span class="sxs-lookup"><span data-stu-id="e7070-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="e7070-104">Masalah performa yang terkait dengan penjadwalan sumber daya dapat terjadi saat jumlah proyek mencapai ribuan.</span><span class="sxs-lookup"><span data-stu-id="e7070-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="e7070-105">Untuk meningkatkan performa penjadwalan sumber daya, tersedia fitur yang memungkinkan pengguna mengurangi waktu yang diperlukan untuk meluncurkan formulir ketersediaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e7070-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="e7070-106">Khususnya, ini akan menghapus proses sinkronisasi peningkatan kapasitas sumber daya dan menggunakan tabel **resprojectresource** untuk mempercepat pencarian sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e7070-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="e7070-107">Perhatikan bahwa tabel **resrollup** tidak akan lagi digunakan.</span><span class="sxs-lookup"><span data-stu-id="e7070-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e7070-108">Jika ada ketergantungan pada proses sinkronisasi peningkatan kapasitas sumber daya atau tabel **resprojectresource**, jangan gunakan fitur ini.</span><span class="sxs-lookup"><span data-stu-id="e7070-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="e7070-109">Aktifkan peningkatan performa penjadwalan sumber daya</span><span class="sxs-lookup"><span data-stu-id="e7070-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="e7070-110">Untuk mengaktifkan peningkatan performa penjadwalan sumber daya, selesaikan langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="e7070-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="e7070-111">Buka **manajemen fitur** > **semua**, dan dalam daftar fitur, Cari **Aktifkan fitur peningkatan kinerja penjadwalan sumber daya proyek**.</span><span class="sxs-lookup"><span data-stu-id="e7070-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="e7070-112">Klik **Aktifkan sekarang**.</span><span class="sxs-lookup"><span data-stu-id="e7070-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="e7070-113">Jika Anda tidak dapat menemukan fitur dalam daftar, pilih **Periksa pembaruan** untuk me-refresh daftar.</span><span class="sxs-lookup"><span data-stu-id="e7070-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="e7070-114">Refresh browser Anda, lalu buka **manajemen proyek dan akuntansi** > **periodik** > **sumber daya proyek** > **sinkronisasikan kapasitas kalender sumber daya di semua perusahaan**.</span><span class="sxs-lookup"><span data-stu-id="e7070-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="e7070-115">Atur **Hapus rekaman kapasitas yang ada** ke **ya** untuk menghapus data sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e7070-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="e7070-116">Jika Anda ingin menghasilkan data inkremental, atur ke **tidak**.</span><span class="sxs-lookup"><span data-stu-id="e7070-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="e7070-117">Di bidang **kode periode**, pilih periode saat data harus dibuat.</span><span class="sxs-lookup"><span data-stu-id="e7070-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="e7070-118">Jika Anda memilih kode periode, tanggal mulai dan berakhir tidak perlu ditentukan.</span><span class="sxs-lookup"><span data-stu-id="e7070-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="e7070-119">Jika Anda membiarkan bidang **kode periode** kosong, pilih tanggal mulai dan berakhir yang spesifik untuk menghasilkan data.</span><span class="sxs-lookup"><span data-stu-id="e7070-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="e7070-120">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7070-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e7070-121">Ini akan mendistribusikan data umum ke tabel **rescalendarcapacity** di semua perusahaan di lingkungan Anda, sehingga pekerjaan batch hanya perlu dijalankan di satu entitas hukum.</span><span class="sxs-lookup"><span data-stu-id="e7070-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="e7070-122">Data dalam pekerjaan batch ini diperlukan untuk menghitung kapasitas sumber daya melalui kalender terkait.</span><span class="sxs-lookup"><span data-stu-id="e7070-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="e7070-123">Buka **manajemen proyek akuntansi** > **periodik** > **sumber daya proyek** > **isi sumber daya proyek di semua perusahaan**, lalu pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7070-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="e7070-124">Ini adalah skrip peningkatan data untuk data umum di tabel **ResProjectResource**, **ResCalendarDateTimeRange**, dan **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="e7070-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="e7070-125">Nilai untuk bidang **PSAPRojSchedRole.RootActivity** juga diperbarui.</span><span class="sxs-lookup"><span data-stu-id="e7070-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="e7070-126">Jika ini tidak dijalankan, Anda akan menerima peringatan saat Anda mencoba menjalankan operasi penjadwalan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="e7070-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="e7070-127">Nonaktifkan peningkatan performa penjadwalan sumber daya</span><span class="sxs-lookup"><span data-stu-id="e7070-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="e7070-128">Buka **manajemen fitur** > **semua**, dan cari **Aktifkan fitur peningkatan kinerja penjadwalan sumber daya proyek**.</span><span class="sxs-lookup"><span data-stu-id="e7070-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="e7070-129">Pilih fitur, lalu pilih tombol **Nonaktifkan**.</span><span class="sxs-lookup"><span data-stu-id="e7070-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="e7070-130">Refresh browser Anda.</span><span class="sxs-lookup"><span data-stu-id="e7070-130">Refresh your browser.</span></span>
4. <span data-ttu-id="e7070-131">Buka **manajemen proyek dan akuntansi** > **Periodik** > **Sinkronisasi kapasitas** > **Sinkronisasi peningkatan kapasitas sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="e7070-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="e7070-132">Pada halaman **sinkronisasi peningkatan kapasitas**, atur **penghapusan rekaman kapasitas yang ada** ke **ya** untuk menghapus data sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e7070-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="e7070-133">Jika Anda ingin menghasilkan data inkremental, atur ke **tidak**.</span><span class="sxs-lookup"><span data-stu-id="e7070-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="e7070-134">Di bidang **kode periode**, pilih periode saat data harus dibuat.</span><span class="sxs-lookup"><span data-stu-id="e7070-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="e7070-135">Jika Anda memilih kode periode, tanggal mulai dan berakhir tidak perlu ditentukan.</span><span class="sxs-lookup"><span data-stu-id="e7070-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="e7070-136">Jika Anda membiarkan bidang **kode periode** kosong, pilih tanggal mulai dan berakhir yang spesifik untuk menghasilkan data.</span><span class="sxs-lookup"><span data-stu-id="e7070-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="e7070-137">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7070-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="e7070-138">Ini akan mendistribusikan data umum ke tabel **ResRollup** di semua perusahaan di lingkungan Anda, sehingga pekerjaan batch hanya perlu dijalankan di satu entitas hukum.</span><span class="sxs-lookup"><span data-stu-id="e7070-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="e7070-139">Pekerjaan batch ini diperlukan untuk semua tampilan **ketersediaan sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="e7070-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="e7070-140">Jika pekerjaan batch ini tidak berjalan, data **ResRollup** akan dibuat sambil berjalan, yang dapat memakan waktu.</span><span class="sxs-lookup"><span data-stu-id="e7070-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
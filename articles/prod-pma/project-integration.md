---
title: Integrasi Microsoft Project client
description: Merencanakan dan memelihara jadwal proyek dapat menjadi rumit, sehingga manajer proyek harus menggunakan alat bantu yang membantu mereka mengelola tugas ini. Integrasi dengan Microsoft Project Client memberikan dukungan untuk membuka dan mengelola struktur rincian kerja proyek.
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999450"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="8a466-104">Integrasi Microsoft Project client</span><span class="sxs-lookup"><span data-stu-id="8a466-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8a466-105">Merencanakan dan memelihara jadwal proyek dapat menjadi rumit, sehingga manajer proyek harus menggunakan alat bantu yang membantu mereka mengelola tugas ini.</span><span class="sxs-lookup"><span data-stu-id="8a466-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="8a466-106">Integrasi dengan Microsoft Project Client memberikan dukungan untuk membuka dan mengelola struktur rincian kerja proyek.</span><span class="sxs-lookup"><span data-stu-id="8a466-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="8a466-107">Manajer proyek dapat mempublikasikan perubahan apa pun kembali ke struktur rincian kerja proyek Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="8a466-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="8a466-108">Jika Anda menggunakan Pembaruan bulan Juli (versi 10.0.4), Anda harus menginstal KB 4054797 dan 4055884.</span><span class="sxs-lookup"><span data-stu-id="8a466-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="8a466-109">Mengkonfigurasi Add-in Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8a466-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="8a466-110">Untuk mengaktifkan integrasi dengan Microsoft Project Client, Add-in Microsoft Dynamics 365 diperlukan untuk diinstal di aplikasi Microsoft Project Client pengguna.</span><span class="sxs-lookup"><span data-stu-id="8a466-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="8a466-111">Hal ini dilakukan dengan membuka **ruang kerja manajemen proyek**.</span><span class="sxs-lookup"><span data-stu-id="8a466-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="8a466-112">•   Klik **Konfigurasikan Add-in klien proyek** dari bagian **Tautan** > **Konfigurasi** di ruang kerja.</span><span class="sxs-lookup"><span data-stu-id="8a466-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="8a466-113">•   Klik **buka**, lalu klik **Jalankan** saat diminta.</span><span class="sxs-lookup"><span data-stu-id="8a466-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="8a466-114">Membuka dan mengedit struktur rincian kerja konsep yang ada di Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8a466-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="8a466-115">Jika proyek di Dynamics 365 Finance sudah memiliki struktur rincian kerja yang dibuat, struktur rincian kerja dapat dibuka di aplikasi Microsoft Project Client jika struktur rincian kerja berada dalam status draf.</span><span class="sxs-lookup"><span data-stu-id="8a466-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="8a466-116">Untuk membuka dari halaman **proyek**, klik tautan **buka di Microsoft Project** dari tab **Paket**. Halaman ini juga dapat dibuka dari dalam aplikasi Microsoft Project Client dengan mengklik tab **buka** di **Microsoft Dynamics 365.** Pilih **entitas hukum** dan **proyek** dari daftar.</span><span class="sxs-lookup"><span data-stu-id="8a466-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="8a466-117">Jika Anda menggunakan Internet Explorer sebagai browser, Anda harus mengklik **Simpan** untuk membuka secara manual dari lokasi yang akan diunduh file-nya.</span><span class="sxs-lookup"><span data-stu-id="8a466-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="8a466-118">Atau, klik **Simpan dan buka** untuk membuka file di Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8a466-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="8a466-119">Jangan Namai ulang file saat menyimpan.</span><span class="sxs-lookup"><span data-stu-id="8a466-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="8a466-120">Sebelum membuat pengeditan apa pun ke file menggunakan Microsoft Project Client, Anda harus memeriksanya. Klik **Check-out** di tab **Microsoft Dynamics 365**. Hal ini akan mencegah pengguna lain mengedit struktur rincian kerja dari dalam Finance pada waktu yang sama.</span><span class="sxs-lookup"><span data-stu-id="8a466-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="8a466-121">Untuk mempublikasikan struktur rincian kerja setelah menyelesaikan pengeditan apa pun, klik **Check-in** pada tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8a466-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="8a466-122">Jika tim proyek telah ditambahkan ke proyek di Finance, daftar sumber daya akan diisi dengan anggota tim.</span><span class="sxs-lookup"><span data-stu-id="8a466-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="8a466-123">Jika tim proyek belum ditambahkan ke proyek, Anda dapat memilih sumber daya dan membuat tim dalam Microsoft Project Client dengan mengklik tombol **sumber daya** pada tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8a466-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="8a466-124">Data berikut akan disinkronisasikan kembali ke Finance sebagai bagian dari proses Check-In:</span><span class="sxs-lookup"><span data-stu-id="8a466-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="8a466-125">•   Nama tugas</span><span class="sxs-lookup"><span data-stu-id="8a466-125">•   Task name</span></span>

<span data-ttu-id="8a466-126">•   Tanggal Mulai</span><span class="sxs-lookup"><span data-stu-id="8a466-126">•   Start date</span></span>

<span data-ttu-id="8a466-127">•   Tanggal Berakhir</span><span class="sxs-lookup"><span data-stu-id="8a466-127">•   Finish date</span></span>

<span data-ttu-id="8a466-128">•   Pendahulu</span><span class="sxs-lookup"><span data-stu-id="8a466-128">•   Predecessors</span></span>

<span data-ttu-id="8a466-129">•   Nama sumber daya</span><span class="sxs-lookup"><span data-stu-id="8a466-129">•   Resource names</span></span>

<span data-ttu-id="8a466-130">•   Kategori</span><span class="sxs-lookup"><span data-stu-id="8a466-130">•   Category</span></span>

<span data-ttu-id="8a466-131">•   Kategori Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="8a466-131">•   Resource category</span></span>

<span data-ttu-id="8a466-132">•   Jam Kerja</span><span class="sxs-lookup"><span data-stu-id="8a466-132">•   Work hours</span></span>

<span data-ttu-id="8a466-133">•   Catatan</span><span class="sxs-lookup"><span data-stu-id="8a466-133">•   Notes</span></span>

<span data-ttu-id="8a466-134">•   Prioritas</span><span class="sxs-lookup"><span data-stu-id="8a466-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="8a466-135">Jika Anda menambahkan bidang lain ke file Microsoft Project Client, mereka tidak akan disimpan ke file, dan tidak akan ditampilkan saat file dibuka kembali.</span><span class="sxs-lookup"><span data-stu-id="8a466-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="8a466-136">Buat struktur rincian kerja untuk proyek yang ada menggunakan Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8a466-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="8a466-137">Untuk membuat struktur rincian kerja menggunakan Microsoft Project Client, ikuti langkah-langkah berikut ini:</span><span class="sxs-lookup"><span data-stu-id="8a466-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="8a466-138">Buka Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8a466-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="8a466-139">Di tab **Microsoft Dynamics 365**, klik **Buka**.</span><span class="sxs-lookup"><span data-stu-id="8a466-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="8a466-140">Pilih **entitas hukum** untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="8a466-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="8a466-141">Pilih **proyek**.</span><span class="sxs-lookup"><span data-stu-id="8a466-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="8a466-142">Klik **Check out** di tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8a466-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="8a466-143">Bila siap untuk dipublikasikan ke Finance, klik **Check-in** pada tab **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="8a466-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="8a466-144">Ganti struktur rincian kerja yang ada untuk proyek yang ada menggunakan Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="8a466-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="8a466-145">Untuk membuat struktur rincian kerja baru menggunakan Microsoft Project Client dan mengganti struktur rincian kerja yang ada untuk proyek yang ada, ikuti langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="8a466-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="8a466-146">Buka Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8a466-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="8a466-147">Buat jadwal di Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8a466-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="8a466-148">Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **ganti proyek yang ada**.</span><span class="sxs-lookup"><span data-stu-id="8a466-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="8a466-149">Pilih **entitas hukum** untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="8a466-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="8a466-150">Pilih **proyek**.</span><span class="sxs-lookup"><span data-stu-id="8a466-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="8a466-151">Klik **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a466-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="8a466-152">Membuat proyek baru dari dalam Microsoft Project client</span><span class="sxs-lookup"><span data-stu-id="8a466-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="8a466-153">Buka Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8a466-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="8a466-154">Buat jadwal di Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="8a466-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="8a466-155">Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **Simpan ke Proyek baru**.</span><span class="sxs-lookup"><span data-stu-id="8a466-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="8a466-156">Pilih **entitas hukum** untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="8a466-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="8a466-157">Masukkan **id proyek**, jika perlu.</span><span class="sxs-lookup"><span data-stu-id="8a466-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="8a466-158">Masukkan **nama proyek**.</span><span class="sxs-lookup"><span data-stu-id="8a466-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="8a466-159">Pilih **jenis proyek**, **grup proyek**, dan **id kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="8a466-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="8a466-160">Atau, Anda dapat membuat kontrak proyek baru dengan mengeklik **baru**.</span><span class="sxs-lookup"><span data-stu-id="8a466-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="8a466-161">Pilih **kalender** yang akan digunakan untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="8a466-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="8a466-162">Klik **OK**.</span><span class="sxs-lookup"><span data-stu-id="8a466-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
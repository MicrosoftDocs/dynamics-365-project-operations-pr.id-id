---
title: Menyalin proyek
description: Topik ini menyediakan informasi tentang menyalin proyek di Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091258"
---
# <a name="copy-a-project"></a><span data-ttu-id="1c34c-103">Menyalin proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-103">Copy a project</span></span>

<span data-ttu-id="1c34c-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="1c34c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1c34c-105">Dengan Dynamics 365 Project Operations, Anda dapat dengan cepat membangun proyek baru dengan memilih **Salin Proyek** pada formulir **Proyek**.</span><span class="sxs-lookup"><span data-stu-id="1c34c-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="1c34c-106">Untuk menyalin proyek, buka proyek yang akan disalin, lalu pilih **Salin proyek**.</span><span class="sxs-lookup"><span data-stu-id="1c34c-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="1c34c-107">Tindakan akan menyalin yang berikut:</span><span class="sxs-lookup"><span data-stu-id="1c34c-107">The action will copy the following:</span></span>

- <span data-ttu-id="1c34c-108">Properti proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-108">Project properties</span></span> 
- <span data-ttu-id="1c34c-109">Struktur rincian kerja</span><span class="sxs-lookup"><span data-stu-id="1c34c-109">Work breakdown structure</span></span>
- <span data-ttu-id="1c34c-110">Anggota tim proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-110">Project team members</span></span>
- <span data-ttu-id="1c34c-111">Perkiraan proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-111">Project estimates</span></span>
- <span data-ttu-id="1c34c-112">Estimasi pengeluaran proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-112">Project expense estimates</span></span>
- <span data-ttu-id="1c34c-113">Estimasi bahan proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="1c34c-114">Properti proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-114">Project properties</span></span>

<span data-ttu-id="1c34c-115">Saat proyek disalin, nilai pada bidang berikut akan disalin:</span><span class="sxs-lookup"><span data-stu-id="1c34c-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="1c34c-116">Nama</span><span class="sxs-lookup"><span data-stu-id="1c34c-116">Name</span></span>
- <span data-ttu-id="1c34c-117">KETERANGAN</span><span class="sxs-lookup"><span data-stu-id="1c34c-117">Description</span></span>
- <span data-ttu-id="1c34c-118">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="1c34c-118">Customer</span></span>
- <span data-ttu-id="1c34c-119">Template kalender</span><span class="sxs-lookup"><span data-stu-id="1c34c-119">Calendar Template</span></span>
- <span data-ttu-id="1c34c-120">Mata uang</span><span class="sxs-lookup"><span data-stu-id="1c34c-120">Currency</span></span>
- <span data-ttu-id="1c34c-121">Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="1c34c-121">Contracting Unit</span></span>
- <span data-ttu-id="1c34c-122">Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-122">Project Manager</span></span>
- <span data-ttu-id="1c34c-123">Status</span><span class="sxs-lookup"><span data-stu-id="1c34c-123">Status</span></span>
- <span data-ttu-id="1c34c-124">Keseluruhan Status Proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-124">Overall Project Status</span></span>
- <span data-ttu-id="1c34c-125">Komentar</span><span class="sxs-lookup"><span data-stu-id="1c34c-125">Comments</span></span>
- <span data-ttu-id="1c34c-126">Estimasi</span><span class="sxs-lookup"><span data-stu-id="1c34c-126">Estimates</span></span>
- <span data-ttu-id="1c34c-127">Estimasi Tanggal Mulai: Tanggal proyek dibuat dari salinan.</span><span class="sxs-lookup"><span data-stu-id="1c34c-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="1c34c-128">Estimasi Tanggal Selesai: Tanggal ini disesuaikan berdasarkan tanggal mulai proyek baru yang dibuat dari salinan.</span><span class="sxs-lookup"><span data-stu-id="1c34c-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="1c34c-129">Upaya (Jam)</span><span class="sxs-lookup"><span data-stu-id="1c34c-129">Effort (Hours)</span></span>
- <span data-ttu-id="1c34c-130">Perkiraan Biaya Tenaga Kerja</span><span class="sxs-lookup"><span data-stu-id="1c34c-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="1c34c-131">Perkiraan Biaya Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="1c34c-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="1c34c-132">Perkiraan Biaya Materi</span><span class="sxs-lookup"><span data-stu-id="1c34c-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="1c34c-133">Salin proyek adalah operasi yang berjalan lama.</span><span class="sxs-lookup"><span data-stu-id="1c34c-133">Copy project is a long running operation.</span></span> <span data-ttu-id="1c34c-134">Rekaman proyek, atribut yang relevan, dan banyak entitas terkait juga disalin.</span><span class="sxs-lookup"><span data-stu-id="1c34c-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="1c34c-135">Karena sifat operasi yang berjalan lama, setelah salinan dimulai, halaman proyek target dikunci untuk pengeditan hingga operasi penyalinan selesai.</span><span class="sxs-lookup"><span data-stu-id="1c34c-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="1c34c-136">Struktur rincian kerja</span><span class="sxs-lookup"><span data-stu-id="1c34c-136">Work breakdown structure</span></span>

<span data-ttu-id="1c34c-137">Saat proyek disalin, seluruh struktur rincian kerja berisi sumber daya disalin.</span><span class="sxs-lookup"><span data-stu-id="1c34c-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="1c34c-138">Sumber daya bernama digantikan dengan sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="1c34c-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="1c34c-139">Jika sumber daya bernama tidak memiliki jam kerja yang sama seperti sumber daya generik, jadwal akan dihitung ulang dan durasi tugas dapat berubah.</span><span class="sxs-lookup"><span data-stu-id="1c34c-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="1c34c-140">Anggota tim proyek</span><span class="sxs-lookup"><span data-stu-id="1c34c-140">Project team members</span></span>

<span data-ttu-id="1c34c-141">Bila tim proyek disalin dari proyek sumber, sumber daya generik akan disalin.</span><span class="sxs-lookup"><span data-stu-id="1c34c-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="1c34c-142">Tugas sumber generik juga dikelola seperti proyek sumber.</span><span class="sxs-lookup"><span data-stu-id="1c34c-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="1c34c-143">Sumber daya bernama akan dikonversi ke anggota tim generik.</span><span class="sxs-lookup"><span data-stu-id="1c34c-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="1c34c-144">Estimasi</span><span class="sxs-lookup"><span data-stu-id="1c34c-144">Estimates</span></span>

<span data-ttu-id="1c34c-145">Bila proyek disalin, baris estimasi bahan, pengeluaran, dan sumber daya disalin dari proyek sumber.</span><span class="sxs-lookup"><span data-stu-id="1c34c-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="1c34c-146">Untuk informasi tentang cara mengakses salinan proyek secara programatik, lihat [mengembangkan template proyek dengan salinan proyek](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="1c34c-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Menyalin proyek
description: Topik ini menyediakan informasi tentang menyalin proyek di Dynamics 365 Project operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908253"
---
# <a name="copy-a-project"></a><span data-ttu-id="15834-103">Menyalin proyek</span><span class="sxs-lookup"><span data-stu-id="15834-103">Copy a project</span></span>

<span data-ttu-id="15834-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="15834-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="15834-105">Dengan Dynamics 365 Project Operations, Anda dapat dengan cepat membangun proyek baru dengan menggunakan tindakan **Salin proyek** pada **proyek**.</span><span class="sxs-lookup"><span data-stu-id="15834-105">With Dynamics 365 Project Operations, you can quickly build new projects by using the **Copy Project** action on the **Projects** from.</span></span> <span data-ttu-id="15834-106">Untuk menyalin proyek, pilih proyek, lalu pilih **Salin**.</span><span class="sxs-lookup"><span data-stu-id="15834-106">To copy a project, select a project, and then select **Copy**.</span></span> <span data-ttu-id="15834-107">Tindakan akan menyalin:</span><span class="sxs-lookup"><span data-stu-id="15834-107">The action will copy:</span></span>

- <span data-ttu-id="15834-108">Properti proyek</span><span class="sxs-lookup"><span data-stu-id="15834-108">Project properties</span></span>
- <span data-ttu-id="15834-109">Struktur rincian kerja</span><span class="sxs-lookup"><span data-stu-id="15834-109">The Work breakdown structure</span></span>
- <span data-ttu-id="15834-110">Anggota tim proyek</span><span class="sxs-lookup"><span data-stu-id="15834-110">Project team members</span></span>
- <span data-ttu-id="15834-111">Perkiraan proyek</span><span class="sxs-lookup"><span data-stu-id="15834-111">Project estimates</span></span>
- <span data-ttu-id="15834-112">Estimasi pengeluaran proyek</span><span class="sxs-lookup"><span data-stu-id="15834-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="15834-113">Properti proyek</span><span class="sxs-lookup"><span data-stu-id="15834-113">Project properties</span></span>

<span data-ttu-id="15834-114">Saat proyek disalin, nilai pada bidang berikut akan disalin:</span><span class="sxs-lookup"><span data-stu-id="15834-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="15834-115">Nama</span><span class="sxs-lookup"><span data-stu-id="15834-115">Name</span></span>
- <span data-ttu-id="15834-116">KETERANGAN</span><span class="sxs-lookup"><span data-stu-id="15834-116">Description</span></span>
- <span data-ttu-id="15834-117">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="15834-117">Customer</span></span>
- <span data-ttu-id="15834-118">Template kalender</span><span class="sxs-lookup"><span data-stu-id="15834-118">Calendar Template</span></span>
- <span data-ttu-id="15834-119">Mata uang</span><span class="sxs-lookup"><span data-stu-id="15834-119">Currency</span></span>
- <span data-ttu-id="15834-120">Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="15834-120">Contracting Unit</span></span>
- <span data-ttu-id="15834-121">Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="15834-121">Project Manager</span></span>
- <span data-ttu-id="15834-122">Status</span><span class="sxs-lookup"><span data-stu-id="15834-122">Status</span></span>
- <span data-ttu-id="15834-123">Keseluruhan Status Proyek</span><span class="sxs-lookup"><span data-stu-id="15834-123">Overall Project Status</span></span>
- <span data-ttu-id="15834-124">Komentar</span><span class="sxs-lookup"><span data-stu-id="15834-124">Comments</span></span>
- <span data-ttu-id="15834-125">Perkiraan</span><span class="sxs-lookup"><span data-stu-id="15834-125">Estimates</span></span>
- <span data-ttu-id="15834-126">Perkiraan Tanggal Mulai</span><span class="sxs-lookup"><span data-stu-id="15834-126">Estimated Start Date</span></span>
- <span data-ttu-id="15834-127">Tanggal Berakhir</span><span class="sxs-lookup"><span data-stu-id="15834-127">Finish Date</span></span>
- <span data-ttu-id="15834-128">Upaya (Jam)</span><span class="sxs-lookup"><span data-stu-id="15834-128">Effort (Hours)</span></span>
- <span data-ttu-id="15834-129">Perkiraan Biaya Tenaga Kerja</span><span class="sxs-lookup"><span data-stu-id="15834-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="15834-130">Perkiraan Biaya Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="15834-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="15834-131">Struktur rincian kerja</span><span class="sxs-lookup"><span data-stu-id="15834-131">Work breakdown structure</span></span>

<span data-ttu-id="15834-132">Saat proyek disalin, seluruh struktur rincian kerja berisi sumber daya disalin.</span><span class="sxs-lookup"><span data-stu-id="15834-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="15834-133">Sumber daya bernama digantikan dengan sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="15834-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="15834-134">Jika sumber daya bernama tidak memiliki jam kerja yang sama seperti sumber daya generik, jadwal akan dihitung ulang dan durasi tugas dapat berubah.</span><span class="sxs-lookup"><span data-stu-id="15834-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="15834-135">Anggota tim proyek</span><span class="sxs-lookup"><span data-stu-id="15834-135">Project team members</span></span>

<span data-ttu-id="15834-136">Bila tim proyek disalin dari proyek sumber, sumber daya generik akan disalin.</span><span class="sxs-lookup"><span data-stu-id="15834-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="15834-137">Tugas sumber generik juga dikelola seperti proyek sumber.</span><span class="sxs-lookup"><span data-stu-id="15834-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="15834-138">Sumber daya bernama akan dikonversi ke anggota tim generik.</span><span class="sxs-lookup"><span data-stu-id="15834-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="15834-139">Perkiraan</span><span class="sxs-lookup"><span data-stu-id="15834-139">Estimates</span></span>

<span data-ttu-id="15834-140">Saat proyek disalin, baris sumber daya maupun perkiraan pengeluaran disalin dari proyek sumber.</span><span class="sxs-lookup"><span data-stu-id="15834-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span>
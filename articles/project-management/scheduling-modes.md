---
title: Mode penjadwalan
description: Topik ini menyediakan informasi tentang mode penjadwalan.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981439"
---
# <a name="scheduling-modes"></a><span data-ttu-id="2183b-103">Mode penjadwalan</span><span class="sxs-lookup"><span data-stu-id="2183b-103">Scheduling modes</span></span>

<span data-ttu-id="2183b-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="2183b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2183b-105">Dynamics 365 Project Operations memberikan kemampuan bagi organisasi untuk menentukan cara mengelola perubahan pada variabel utama dalam tugas dalam struktur perincian kerja.</span><span class="sxs-lookup"><span data-stu-id="2183b-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="2183b-106">Berdasarkan kebutuhan organisasi yang spesifik, Manajer Proyek dapat membuat perubahan pada mode penjadwalan saat proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="2183b-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="2183b-107">Ada tiga mode penjadwalan yang tersedia di Project Operations:</span><span class="sxs-lookup"><span data-stu-id="2183b-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="2183b-108">Durasi tetap (ini adalah mode default)</span><span class="sxs-lookup"><span data-stu-id="2183b-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="2183b-109">Pekerjaan tetap</span><span class="sxs-lookup"><span data-stu-id="2183b-109">Fixed work</span></span>
  - <span data-ttu-id="2183b-110">Unit tetap</span><span class="sxs-lookup"><span data-stu-id="2183b-110">Fixed units</span></span>

<span data-ttu-id="2183b-111">Nilai yang dipengaruhi oleh definisi mode penjadwalan tertentu ditentukan oleh rumus berikut:</span><span class="sxs-lookup"><span data-stu-id="2183b-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="2183b-112">Upaya (*Pekerjaan*) = Durasi x Unit</span><span class="sxs-lookup"><span data-stu-id="2183b-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="2183b-113">Saat menentukan mode penjadwalan proyek, Anda menetapkan salah satu nilai ini, yang kemudian tidak dapat diubah.</span><span class="sxs-lookup"><span data-stu-id="2183b-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="2183b-114">Mempertahankan nilai ini sebagai konstanta menempatkan prioritas pada nilai tersebut, yang akan memberitahukan sistem untuk tidak mengubahnya ketika kedua nilai lainnya berubah.</span><span class="sxs-lookup"><span data-stu-id="2183b-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="2183b-115">Tabel berikut memberikan informasi tentang dampak memilih mode tertentu.</span><span class="sxs-lookup"><span data-stu-id="2183b-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="2183b-116">**Dalam tugas ini**</span><span class="sxs-lookup"><span data-stu-id="2183b-116">**In this task**</span></span>             | <span data-ttu-id="2183b-117">**Jika Anda merevisi unit**</span><span class="sxs-lookup"><span data-stu-id="2183b-117">**If you revise units**</span></span>   | <span data-ttu-id="2183b-118">**Jika Anda merevisi durasi**</span><span class="sxs-lookup"><span data-stu-id="2183b-118">**If you revise duration**</span></span> | <span data-ttu-id="2183b-119">**Jika Anda merevisi upaya**</span><span class="sxs-lookup"><span data-stu-id="2183b-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="2183b-120">Tugas Unit tetap</span><span class="sxs-lookup"><span data-stu-id="2183b-120">Fixed units task</span></span>     | <span data-ttu-id="2183b-121">Durasi akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-121">Duration is recalculated.</span></span> | <span data-ttu-id="2183b-122">Upaya akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-122">Effort is recalculated.</span></span>    | <span data-ttu-id="2183b-123">Durasi akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="2183b-124">Tugas Upaya tetap</span><span class="sxs-lookup"><span data-stu-id="2183b-124">Fixed effort task</span></span>    | <span data-ttu-id="2183b-125">Durasi akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-125">Duration is recalculated.</span></span> | <span data-ttu-id="2183b-126">Unit akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-126">Units are recalculated.</span></span>    | <span data-ttu-id="2183b-127">Durasi akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="2183b-128">Tugas Durasi tetap</span><span class="sxs-lookup"><span data-stu-id="2183b-128">Fixed duration task</span></span>  | <span data-ttu-id="2183b-129">Upaya akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-129">Effort is recalculated.</span></span>   | <span data-ttu-id="2183b-130">Upaya akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-130">Effort is recalculated.</span></span>    | <span data-ttu-id="2183b-131">Unit akan dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="2183b-131">Units are recalculated.</span></span>   |

<span data-ttu-id="2183b-132">Untuk informasi lebih lanjut tentang dampak mode tertentu, lihat [Mengubah jenis tugas untuk penjadwalan yang lebih akurat](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="2183b-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="2183b-133">Dalam topik, istilah **Pekerjaan** digunakan, bukan **Upaya**.</span><span class="sxs-lookup"><span data-stu-id="2183b-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="2183b-134">Mengubah mode penjadwalan organisasi</span><span class="sxs-lookup"><span data-stu-id="2183b-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="2183b-135">Selesaikan langkah-langkah berikut untuk menentukan mode penjadwalan organisasi.</span><span class="sxs-lookup"><span data-stu-id="2183b-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="2183b-136">Buka **Parameter** \> **Umum** \> **Pengaturan**, lalu pilih parameter proyek.</span><span class="sxs-lookup"><span data-stu-id="2183b-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="2183b-137">Pada halaman **Parameter Proyek**, pilih mode penjadwalan default untuk organisasi, lalu tentukan kemampuan manajer Proyek untuk menimpa pengaturan saat membuat proyek baru.</span><span class="sxs-lookup"><span data-stu-id="2183b-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="2183b-138">Mengubah pengaturan mode penjadwalan pada proyek</span><span class="sxs-lookup"><span data-stu-id="2183b-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="2183b-139">Jika organisasi mengizinkan Manajer proyek menimpa mode penjadwalan default, manajer proyek dapat membuat perubahan tersebut saat mereka membuat proyek baru.</span><span class="sxs-lookup"><span data-stu-id="2183b-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="2183b-140">Namun, setelah proyek disimpan, mode penjadwalan tidak dapat diubah.</span><span class="sxs-lookup"><span data-stu-id="2183b-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="2183b-141">Proyek yang disalin</span><span class="sxs-lookup"><span data-stu-id="2183b-141">Copied projects</span></span>

<span data-ttu-id="2183b-142">Karena proyek dibuat saat tindakan salin proyek dilakukan, manajer proyek tidak dapat mengatur mode penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="2183b-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="2183b-143">Proyek tujuan akan selalu diatur default ke mode yang ditentukan pada tingkat organisasional.</span><span class="sxs-lookup"><span data-stu-id="2183b-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="2183b-144">Tugas yang disalin</span><span class="sxs-lookup"><span data-stu-id="2183b-144">Copied tasks</span></span>

<span data-ttu-id="2183b-145">Ketika tugas disalin dari satu proyek ke proyek lain, tugas mewarisi mode penjadwalan proyek tujuan.</span><span class="sxs-lookup"><span data-stu-id="2183b-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>

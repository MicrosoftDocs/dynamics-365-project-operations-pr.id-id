---
title: Kemajuan proyek dan konsumsi biaya
description: Topik ini menyediakan informasi tentang cara melacak kemajuan proyek dan konsumsi biaya.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752494"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="5455e-103">Kemajuan proyek dan konsumsi biaya</span><span class="sxs-lookup"><span data-stu-id="5455e-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5455e-104">Kebutuhan untuk melacak kemajuan terhadap jadwal bervariasi menurut industri.</span><span class="sxs-lookup"><span data-stu-id="5455e-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="5455e-105">Beberapa industri melacak pada tingkat rinci, sedangkan industri lainnya melacak pada tingkat yang lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="5455e-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="5455e-106">Topik ini menunjukkan cara menjadwalkan untuk memenuhi kebutuhan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="5455e-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="5455e-107">Tampilan Pelacakan Upaya</span><span class="sxs-lookup"><span data-stu-id="5455e-107">Effort tracking view</span></span>

<span data-ttu-id="5455e-108">Tampilan **pelacakan upaya** melacak kemajuan tugas dalam jadwal.</span><span class="sxs-lookup"><span data-stu-id="5455e-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="5455e-109">Ini membandingkan waktu aktual upaya yang telah digunakan pada tugas terhadap jam upaya yang direncanakan untuk tugas itu.</span><span class="sxs-lookup"><span data-stu-id="5455e-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="5455e-110">PSA menggunakan rumus berikut untuk menghitung metrik pelacakan:</span><span class="sxs-lookup"><span data-stu-id="5455e-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="5455e-111">Persentase kemajuan = upaya yang dihabiskan hingga sekarang ÷ upaya yang direncanakan untuk tugas</span><span class="sxs-lookup"><span data-stu-id="5455e-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="5455e-112">Perkiraan untuk menyelesaikan (ETC) = rencana usaha – upaya yang sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="5455e-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="5455e-113">Perkiraan saat selesai (EAC) = usaha tersisa + upaya yang sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="5455e-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="5455e-114">Diproyeksikan variance usaha = usaha yang direncanakan – EAC</span><span class="sxs-lookup"><span data-stu-id="5455e-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="5455e-115">PSA menunjukkan proyeksi dari varians upaya terhadap tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="5455e-116">Jika EAC lebih dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih banyak waktu daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="5455e-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="5455e-117">Oleh karena itu, terlambat dari jadwal.</span><span class="sxs-lookup"><span data-stu-id="5455e-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="5455e-118">Jika EAC kurang dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih sedikit waktu daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="5455e-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="5455e-119">Oleh karena itu, lebih dini dari jadwal.</span><span class="sxs-lookup"><span data-stu-id="5455e-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="5455e-120">Upaya memproyeksikan ulang</span><span class="sxs-lookup"><span data-stu-id="5455e-120">Re-projecting effort</span></span>

<span data-ttu-id="5455e-121">biasanya manajer proyek merevisi perkiraan asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="5455e-122">Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini.</span><span class="sxs-lookup"><span data-stu-id="5455e-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="5455e-123">Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.</span><span class="sxs-lookup"><span data-stu-id="5455e-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="5455e-124">Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:</span><span class="sxs-lookup"><span data-stu-id="5455e-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="5455e-125">Menimpa ETC default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="5455e-126">Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="5455e-127">Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, EAC tugas, dan persentase progres, serta proyeksi varians upaya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="5455e-128">EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.</span><span class="sxs-lookup"><span data-stu-id="5455e-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="5455e-129">Proyeksi ulang upaya pada tugas ringkasan</span><span class="sxs-lookup"><span data-stu-id="5455e-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="5455e-130">Upaya pada ringkasan tugas atau tugas kontainer dapat diproyeksikan ulang.</span><span class="sxs-lookup"><span data-stu-id="5455e-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="5455e-131">Terlepas dari apakah pengguna memproyeksikan kembali menggunakan usaha yang tersisa atau persentase kemajuan pada tugas ringkasan, rangkaian perhitungan berikut dimulai:</span><span class="sxs-lookup"><span data-stu-id="5455e-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="5455e-132">EAC, ETC, dan persentase kemajuan tugas dihitung.</span><span class="sxs-lookup"><span data-stu-id="5455e-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="5455e-133">EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti EAC asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="5455e-134">EAC baru pada setiap tugas individual hingga tugas node leaf dihitung.</span><span class="sxs-lookup"><span data-stu-id="5455e-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="5455e-135">Tugas anak yang terpengaruh hingga node leaf memiliki persentase ETC dan kemajuan yang akan dihitung ulang berdasarkan nilai EAC.</span><span class="sxs-lookup"><span data-stu-id="5455e-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="5455e-136">Ini menghasilkan proyeksi baru untuk varians upaya dari tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="5455e-137">EAC dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="5455e-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="5455e-138">Tampilan Pelacakan Biaya</span><span class="sxs-lookup"><span data-stu-id="5455e-138">Cost tracking view</span></span> 

<span data-ttu-id="5455e-139">Tampilan **pelacakan biaya** membandingkan biaya aktual yang dihabiskan pada tugas dengan rencana biaya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="5455e-140">Tampilan ini hanya menampilkan biaya tenaga kerja dan tidak mencakup biaya dari perkiraan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="5455e-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="5455e-141">PSA menggunakan rumus berikut untuk menghitung metrik pelacakan:</span><span class="sxs-lookup"><span data-stu-id="5455e-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="5455e-142">Persentase dari biaya yang dihabiskan = biaya aktual yang dibelanjakan hingga sekarang ÷ rencana biaya untuk tugas</span><span class="sxs-lookup"><span data-stu-id="5455e-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="5455e-143">Biaya untuk menyelesaikan (CTC) = rencana biaya – biaya sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="5455e-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="5455e-144">EAC = CTC + biaya aktual yang dibelanjakan hingga saat ini</span><span class="sxs-lookup"><span data-stu-id="5455e-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="5455e-145">varians Biaya diproyeksikan = biaya direncanakan - EAC</span><span class="sxs-lookup"><span data-stu-id="5455e-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="5455e-146">Proyeksi varians biaya ditampilkan terhadap tugas.</span><span class="sxs-lookup"><span data-stu-id="5455e-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="5455e-147">Jika EAC lebih dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih banyak biaya daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="5455e-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="5455e-148">Oleh karena itu, tren lebih dari anggaran.</span><span class="sxs-lookup"><span data-stu-id="5455e-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="5455e-149">Jika EAC kurang dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih sedikit biaya daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="5455e-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="5455e-150">Oleh karena itu, tren di bawah anggaran.</span><span class="sxs-lookup"><span data-stu-id="5455e-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="5455e-151">Proyeksi ulang biaya manajer proyek</span><span class="sxs-lookup"><span data-stu-id="5455e-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="5455e-152">Bila upaya diproyeksikan ulang, CTC, EAC, persentase biaya yang dihabiskan, dan variasi biaya yang diproyeksikan akan dihitung ulang dalam tampilan **pelacakan biaya**.</span><span class="sxs-lookup"><span data-stu-id="5455e-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="5455e-153">Ringkasan Status Proyek</span><span class="sxs-lookup"><span data-stu-id="5455e-153">Project status summary</span></span>

<span data-ttu-id="5455e-154">Pelacakan data dalam tampilan **pelacakan upaya** dan **pelacakan biaya** menampilkan kemajuan dan konsumsi biaya pada node root proyek, tugas ringkasan, dan tingkat tugas node daun.</span><span class="sxs-lookup"><span data-stu-id="5455e-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="5455e-155">Bagian **status** pada halaman **entitas proyek** menunjukkan ringkasan status tingkat proyek.</span><span class="sxs-lookup"><span data-stu-id="5455e-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="5455e-156">Bidang ringkasan status</span><span class="sxs-lookup"><span data-stu-id="5455e-156">Status summary fields</span></span>

<span data-ttu-id="5455e-157">Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek.</span><span class="sxs-lookup"><span data-stu-id="5455e-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="5455e-158">Menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="5455e-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="5455e-159">Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status.</span><span class="sxs-lookup"><span data-stu-id="5455e-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="5455e-160">Bidang **Status diperbarui pada** tidak dapat diedit dan nilainya adalah stempel waktu yang menunjukkan Kapan status diperbarui terakhir.</span><span class="sxs-lookup"><span data-stu-id="5455e-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="5455e-161">Bidang **performa jadwal** dan **performa biaya** ditetapkan dari tanggal pelacakan.</span><span class="sxs-lookup"><span data-stu-id="5455e-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="5455e-162">Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat menetapkan bidang ini ke **depan**.</span><span class="sxs-lookup"><span data-stu-id="5455e-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="5455e-163">Bila jadwal dan varians biaya untuk node root negatif, Anda dapat mengaturnya ke **belakang**.</span><span class="sxs-lookup"><span data-stu-id="5455e-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>

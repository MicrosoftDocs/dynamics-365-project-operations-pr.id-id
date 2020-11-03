---
title: Kemajuan proyek dan konsumsi biaya
description: Topik ini menyediakan informasi tentang melacak kemajuan proyek dan konsumsi biaya.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3b60f72b371a76a59216b0b528d8e63513b06e0d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078645"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="93781-103">Kemajuan proyek dan konsumsi biaya</span><span class="sxs-lookup"><span data-stu-id="93781-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="93781-104">Kebutuhan untuk melacak kemajuan terhadap jadwal bervariasi menurut industri.</span><span class="sxs-lookup"><span data-stu-id="93781-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="93781-105">Beberapa industri melacak pada tingkat rinci, sedangkan industri lainnya melacak pada tingkat yang lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="93781-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="93781-106">Topik ini menunjukkan cara menjadwalkan untuk memenuhi kebutuhan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="93781-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="93781-107">Tampilan Pelacakan Upaya</span><span class="sxs-lookup"><span data-stu-id="93781-107">Effort tracking view</span></span>

<span data-ttu-id="93781-108">Tampilan **pelacakan upaya** melacak kemajuan tugas dalam jadwal.</span><span class="sxs-lookup"><span data-stu-id="93781-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="93781-109">Ini membandingkan waktu aktual upaya yang digunakan dalam tugas terhadap jam upaya yang direncanakan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="93781-110">Project Service Automation menggunakan rumus berikut untuk menghitung metrik pelacakan:</span><span class="sxs-lookup"><span data-stu-id="93781-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="93781-111">Awalnya pada pembuatan tugas: rencana biaya akan diatur ke perkiraan biaya saat selesai.</span><span class="sxs-lookup"><span data-stu-id="93781-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="93781-112">Setelah aktual direkam pada tugas, berikut ini akan menjadi perhitungan tentang tampilan pelacakan untuk upaya</span><span class="sxs-lookup"><span data-stu-id="93781-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="93781-113">Persentase Kemajuan = upaya yang sebenarnya yang dihabiskan sampai saat ini ÷Estimasi saat penyelesaian (EAC)</span><span class="sxs-lookup"><span data-stu-id="93781-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="93781-114">Estimasi untuk menyelesaikan (ETC) = Estimasi saat penyelesaian (EAC)-upaya yang sebenarnya dihabiskan hingga saat ini</span><span class="sxs-lookup"><span data-stu-id="93781-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="93781-115">EAC = usaha tersisa + upaya yang sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="93781-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="93781-116">Diproyeksikan variance usaha = usaha yang direncanakan – EAC</span><span class="sxs-lookup"><span data-stu-id="93781-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="93781-117">Project Service Automation menunjukkan proyeksi dari varians upaya terhadap tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="93781-118">Jika EAC lebih dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih banyak waktu daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="93781-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="93781-119">Oleh karena itu, terlambat dari jadwal.</span><span class="sxs-lookup"><span data-stu-id="93781-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="93781-120">Jika EAC kurang dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih sedikit waktu daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="93781-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="93781-121">Oleh karena itu, lebih dini dari jadwal.</span><span class="sxs-lookup"><span data-stu-id="93781-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="93781-122">Upaya memproyeksikan ulang</span><span class="sxs-lookup"><span data-stu-id="93781-122">Reprojecting effort</span></span>

<span data-ttu-id="93781-123">biasanya manajer proyek merevisi perkiraan asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="93781-124">Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini.</span><span class="sxs-lookup"><span data-stu-id="93781-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="93781-125">Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.</span><span class="sxs-lookup"><span data-stu-id="93781-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="93781-126">Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:</span><span class="sxs-lookup"><span data-stu-id="93781-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="93781-127">Menimpa ETC default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="93781-128">Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="93781-129">Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, EAC tugas, dan persentase progres, serta proyeksi varians upaya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="93781-130">EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.</span><span class="sxs-lookup"><span data-stu-id="93781-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="93781-131">Proyeksi ulang upaya pada tugas ringkasan</span><span class="sxs-lookup"><span data-stu-id="93781-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="93781-132">Upaya pada ringkasan tugas atau tugas kontainer dapat diproyeksikan ulang.</span><span class="sxs-lookup"><span data-stu-id="93781-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="93781-133">Terlepas dari apakah pengguna memproyeksikan kembali menggunakan usaha yang tersisa atau persentase kemajuan pada tugas ringkasan, rangkaian perhitungan berikut dimulai:</span><span class="sxs-lookup"><span data-stu-id="93781-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="93781-134">EAC, ETC, dan persentase kemajuan tugas dihitung.</span><span class="sxs-lookup"><span data-stu-id="93781-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="93781-135">EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti EAC asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="93781-136">EAC baru pada setiap tugas individual hingga tugas node leaf dihitung.</span><span class="sxs-lookup"><span data-stu-id="93781-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="93781-137">Tugas anak yang terpengaruh hingga node leaf memiliki persentase ETC dan kemajuan yang akan dihitung ulang berdasarkan nilai EAC.</span><span class="sxs-lookup"><span data-stu-id="93781-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="93781-138">Ini menghasilkan proyeksi baru untuk varians upaya dari tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="93781-139">EAC dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="93781-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="93781-140">Tampilan Pelacakan Biaya</span><span class="sxs-lookup"><span data-stu-id="93781-140">Cost tracking view</span></span> 

<span data-ttu-id="93781-141">Tampilan **pelacakan biaya** membandingkan biaya aktual yang dihabiskan pada tugas dengan rencana biaya.</span><span class="sxs-lookup"><span data-stu-id="93781-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="93781-142">Tampilan ini hanya menampilkan biaya tenaga kerja dan tidak mencakup biaya dari perkiraan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="93781-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="93781-143">Project Service Automation menggunakan rumus berikut untuk menghitung metrik pelacakan:</span><span class="sxs-lookup"><span data-stu-id="93781-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="93781-144">Bila tugas dibuat, biaya yang direncanakan sama dengan perkiraan biaya saat penyelesaian.</span><span class="sxs-lookup"><span data-stu-id="93781-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="93781-145">Setelah aktual direkam pada tugas, berikut ini akan dihitung pada tampilan **pelacakan** untuk biaya:</span><span class="sxs-lookup"><span data-stu-id="93781-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="93781-146">Persentase dari biaya yang dihabiskan = biaya aktual yang dibelanjakan hingga sekarang ÷ Estimasi biaya saat penyelesaian untuk tugas</span><span class="sxs-lookup"><span data-stu-id="93781-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="93781-147">Biaya untuk menyelesaikan (CTC) = Estimasi biaya saat penyelesaian – biaya sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="93781-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="93781-148">Biaya untuk menyelesaikan = CTC + biaya sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="93781-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="93781-149">varians Biaya terproyeksi = biaya yang direncanakan - Estimasi biaya saat penyelesaian</span><span class="sxs-lookup"><span data-stu-id="93781-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="93781-150">Proyeksi varians biaya ditampilkan terhadap tugas.</span><span class="sxs-lookup"><span data-stu-id="93781-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="93781-151">Jika estimasi biaya saat penyelesaian lebih dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih banyak biaya daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="93781-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="93781-152">Oleh karena itu, tren lebih dari anggaran.</span><span class="sxs-lookup"><span data-stu-id="93781-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="93781-153">Jika estimasi biaya saat penyelesaian kurang dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih sedikit biaya daripada yang direncanakan semula dan cenderung di bawah anggaran.</span><span class="sxs-lookup"><span data-stu-id="93781-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="93781-154">Proyeksi ulang biaya manajer proyek</span><span class="sxs-lookup"><span data-stu-id="93781-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="93781-155">Bila upaya diproyeksikan ulang, CTC, Estimasi biaya saat penyelesaian, persentase biaya yang dihabiskan, dan variasi biaya yang diproyeksikan akan dihitung ulang dalam tampilan **pelacakan biaya**.</span><span class="sxs-lookup"><span data-stu-id="93781-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="93781-156">Ringkasan Status Proyek</span><span class="sxs-lookup"><span data-stu-id="93781-156">Project status summary</span></span>

<span data-ttu-id="93781-157">Pelacakan data dalam tampilan **pelacakan upaya** dan **pelacakan biaya** menampilkan kemajuan dan konsumsi biaya pada node root proyek, tugas ringkasan, dan tingkat tugas node daun.</span><span class="sxs-lookup"><span data-stu-id="93781-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="93781-158">Bagian **status** pada halaman **entitas proyek** menunjukkan ringkasan status tingkat proyek.</span><span class="sxs-lookup"><span data-stu-id="93781-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="93781-159">Bidang ringkasan status</span><span class="sxs-lookup"><span data-stu-id="93781-159">Status summary fields</span></span>

<span data-ttu-id="93781-160">Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek.</span><span class="sxs-lookup"><span data-stu-id="93781-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="93781-161">Menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="93781-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="93781-162">Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status.</span><span class="sxs-lookup"><span data-stu-id="93781-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="93781-163">Bidang **Status diperbarui pada** tidak dapat diedit dan nilainya adalah stempel waktu yang menunjukkan Kapan status diperbarui terakhir.</span><span class="sxs-lookup"><span data-stu-id="93781-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="93781-164">Bidang **performa jadwal** dan **performa biaya** ditetapkan dari tanggal pelacakan.</span><span class="sxs-lookup"><span data-stu-id="93781-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="93781-165">Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat menetapkan bidang ini ke **depan**.</span><span class="sxs-lookup"><span data-stu-id="93781-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="93781-166">Bila jadwal dan varians biaya untuk node root negatif, Anda dapat mengaturnya ke **belakang**.</span><span class="sxs-lookup"><span data-stu-id="93781-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>

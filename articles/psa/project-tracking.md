---
title: Kemajuan proyek dan konsumsi biaya
description: Topik ini menyediakan informasi tentang melacak kemajuan proyek dan konsumsi biaya.
author: ruhercul
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
ms.openlocfilehash: 4fe6adf1a16c1eafc5e37dbd8878dda44cbca230
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009035"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="32d46-103">Kemajuan proyek dan konsumsi biaya</span><span class="sxs-lookup"><span data-stu-id="32d46-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="32d46-104">Kebutuhan untuk melacak kemajuan terhadap jadwal bervariasi menurut industri.</span><span class="sxs-lookup"><span data-stu-id="32d46-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="32d46-105">Beberapa industri melacak pada tingkat rinci, sedangkan industri lainnya melacak pada tingkat yang lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="32d46-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="32d46-106">Topik ini menunjukkan cara menjadwalkan untuk memenuhi kebutuhan organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="32d46-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="32d46-107">Tampilan Pelacakan Upaya</span><span class="sxs-lookup"><span data-stu-id="32d46-107">Effort tracking view</span></span>

<span data-ttu-id="32d46-108">Tampilan **pelacakan upaya** melacak kemajuan tugas dalam jadwal.</span><span class="sxs-lookup"><span data-stu-id="32d46-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="32d46-109">Ini membandingkan waktu aktual upaya yang digunakan dalam tugas terhadap jam upaya yang direncanakan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="32d46-110">Project Service Automation menggunakan rumus berikut untuk menghitung metrik pelacakan:</span><span class="sxs-lookup"><span data-stu-id="32d46-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="32d46-111">Awalnya pada pembuatan tugas: rencana biaya akan diatur ke perkiraan biaya saat selesai.</span><span class="sxs-lookup"><span data-stu-id="32d46-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="32d46-112">Setelah aktual direkam pada tugas, berikut ini akan menjadi perhitungan tentang tampilan pelacakan untuk upaya</span><span class="sxs-lookup"><span data-stu-id="32d46-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="32d46-113">Persentase Kemajuan = upaya yang sebenarnya yang dihabiskan sampai saat ini ÷Estimasi saat penyelesaian (EAC)</span><span class="sxs-lookup"><span data-stu-id="32d46-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="32d46-114">Estimasi untuk menyelesaikan (ETC) = Estimasi saat penyelesaian (EAC)-upaya yang sebenarnya dihabiskan hingga saat ini</span><span class="sxs-lookup"><span data-stu-id="32d46-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="32d46-115">EAC = usaha tersisa + upaya yang sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="32d46-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="32d46-116">Diproyeksikan variance usaha = usaha yang direncanakan – EAC</span><span class="sxs-lookup"><span data-stu-id="32d46-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="32d46-117">Project Service Automation menunjukkan proyeksi dari varians upaya terhadap tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="32d46-118">Jika EAC lebih dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih banyak waktu daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="32d46-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="32d46-119">Oleh karena itu, terlambat dari jadwal.</span><span class="sxs-lookup"><span data-stu-id="32d46-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="32d46-120">Jika EAC kurang dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih sedikit waktu daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="32d46-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="32d46-121">Oleh karena itu, lebih dini dari jadwal.</span><span class="sxs-lookup"><span data-stu-id="32d46-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="32d46-122">Upaya memproyeksikan ulang</span><span class="sxs-lookup"><span data-stu-id="32d46-122">Reprojecting effort</span></span>

<span data-ttu-id="32d46-123">biasanya manajer proyek merevisi perkiraan asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="32d46-124">Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini.</span><span class="sxs-lookup"><span data-stu-id="32d46-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="32d46-125">Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.</span><span class="sxs-lookup"><span data-stu-id="32d46-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="32d46-126">Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:</span><span class="sxs-lookup"><span data-stu-id="32d46-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="32d46-127">Menimpa ETC default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="32d46-128">Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="32d46-129">Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, EAC tugas, dan persentase progres, serta proyeksi varians upaya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="32d46-130">EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.</span><span class="sxs-lookup"><span data-stu-id="32d46-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="32d46-131">Proyeksi ulang upaya pada tugas ringkasan</span><span class="sxs-lookup"><span data-stu-id="32d46-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="32d46-132">Upaya pada ringkasan tugas atau tugas kontainer dapat diproyeksikan ulang.</span><span class="sxs-lookup"><span data-stu-id="32d46-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="32d46-133">Terlepas dari apakah pengguna memproyeksikan kembali menggunakan usaha yang tersisa atau persentase kemajuan pada tugas ringkasan, rangkaian perhitungan berikut dimulai:</span><span class="sxs-lookup"><span data-stu-id="32d46-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="32d46-134">EAC, ETC, dan persentase kemajuan tugas dihitung.</span><span class="sxs-lookup"><span data-stu-id="32d46-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="32d46-135">EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti EAC asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="32d46-136">EAC baru pada setiap tugas individual hingga tugas node leaf dihitung.</span><span class="sxs-lookup"><span data-stu-id="32d46-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="32d46-137">Tugas anak yang terpengaruh hingga node leaf memiliki persentase ETC dan kemajuan yang akan dihitung ulang berdasarkan nilai EAC.</span><span class="sxs-lookup"><span data-stu-id="32d46-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="32d46-138">Ini menghasilkan proyeksi baru untuk varians upaya dari tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="32d46-139">EAC dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="32d46-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="32d46-140">Tampilan Pelacakan Biaya</span><span class="sxs-lookup"><span data-stu-id="32d46-140">Cost tracking view</span></span> 

<span data-ttu-id="32d46-141">Tampilan **pelacakan biaya** membandingkan biaya aktual yang dihabiskan pada tugas dengan rencana biaya.</span><span class="sxs-lookup"><span data-stu-id="32d46-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="32d46-142">Tampilan ini hanya menampilkan biaya tenaga kerja dan tidak mencakup biaya dari perkiraan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="32d46-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="32d46-143">Project Service Automation menggunakan rumus berikut untuk menghitung metrik pelacakan:</span><span class="sxs-lookup"><span data-stu-id="32d46-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="32d46-144">Bila tugas dibuat, biaya yang direncanakan sama dengan perkiraan biaya saat penyelesaian.</span><span class="sxs-lookup"><span data-stu-id="32d46-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="32d46-145">Setelah aktual direkam pada tugas, berikut ini akan dihitung pada tampilan **pelacakan** untuk biaya:</span><span class="sxs-lookup"><span data-stu-id="32d46-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="32d46-146">Persentase dari biaya yang dihabiskan = biaya aktual yang dibelanjakan hingga sekarang ÷ Estimasi biaya saat penyelesaian untuk tugas</span><span class="sxs-lookup"><span data-stu-id="32d46-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="32d46-147">Biaya untuk menyelesaikan (CTC) = Estimasi biaya saat penyelesaian – biaya sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="32d46-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="32d46-148">Biaya untuk menyelesaikan = CTC + biaya sebenarnya yang dihabiskan sampai saat ini</span><span class="sxs-lookup"><span data-stu-id="32d46-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="32d46-149">varians Biaya terproyeksi = biaya yang direncanakan - Estimasi biaya saat penyelesaian</span><span class="sxs-lookup"><span data-stu-id="32d46-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="32d46-150">Proyeksi varians biaya ditampilkan terhadap tugas.</span><span class="sxs-lookup"><span data-stu-id="32d46-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="32d46-151">Jika estimasi biaya saat penyelesaian lebih dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih banyak biaya daripada yang direncanakan semula.</span><span class="sxs-lookup"><span data-stu-id="32d46-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="32d46-152">Oleh karena itu, tren lebih dari anggaran.</span><span class="sxs-lookup"><span data-stu-id="32d46-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="32d46-153">Jika estimasi biaya saat penyelesaian kurang dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih sedikit biaya daripada yang direncanakan semula dan cenderung di bawah anggaran.</span><span class="sxs-lookup"><span data-stu-id="32d46-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="32d46-154">Proyeksi ulang biaya manajer proyek</span><span class="sxs-lookup"><span data-stu-id="32d46-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="32d46-155">Bila upaya diproyeksikan ulang, CTC, Estimasi biaya saat penyelesaian, persentase biaya yang dihabiskan, dan variasi biaya yang diproyeksikan akan dihitung ulang dalam tampilan **pelacakan biaya**.</span><span class="sxs-lookup"><span data-stu-id="32d46-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="32d46-156">Ringkasan Status Proyek</span><span class="sxs-lookup"><span data-stu-id="32d46-156">Project status summary</span></span>

<span data-ttu-id="32d46-157">Pelacakan data dalam tampilan **pelacakan upaya** dan **pelacakan biaya** menampilkan kemajuan dan konsumsi biaya pada node root proyek, tugas ringkasan, dan tingkat tugas node daun.</span><span class="sxs-lookup"><span data-stu-id="32d46-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="32d46-158">Bagian **status** pada halaman **entitas proyek** menunjukkan ringkasan status tingkat proyek.</span><span class="sxs-lookup"><span data-stu-id="32d46-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="32d46-159">Bidang ringkasan status</span><span class="sxs-lookup"><span data-stu-id="32d46-159">Status summary fields</span></span>

<span data-ttu-id="32d46-160">Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek.</span><span class="sxs-lookup"><span data-stu-id="32d46-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="32d46-161">Menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko.</span><span class="sxs-lookup"><span data-stu-id="32d46-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="32d46-162">Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status.</span><span class="sxs-lookup"><span data-stu-id="32d46-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="32d46-163">Bidang **Status diperbarui pada** tidak dapat diedit dan nilainya adalah stempel waktu yang menunjukkan Kapan status diperbarui terakhir.</span><span class="sxs-lookup"><span data-stu-id="32d46-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="32d46-164">Bidang **performa jadwal** dan **performa biaya** ditetapkan dari tanggal pelacakan.</span><span class="sxs-lookup"><span data-stu-id="32d46-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="32d46-165">Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat menetapkan bidang ini ke **depan**.</span><span class="sxs-lookup"><span data-stu-id="32d46-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="32d46-166">Bila jadwal dan varians biaya untuk node root negatif, Anda dapat mengaturnya ke **belakang**.</span><span class="sxs-lookup"><span data-stu-id="32d46-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
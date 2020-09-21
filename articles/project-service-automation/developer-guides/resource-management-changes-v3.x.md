---
title: Perubahan manajemen Sumber Daya (Project Service Automation 3.x)
description: Topik ini menyediakan informasi tentang perubahan area manajemen sumber daya.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 25fafd22-fe94-4865-8d4d-3e6582c999d5
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: e00ce5a9604e25764567a3f9d38ec85aec4245d4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752453"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="93904-103">Perubahan manajemen Sumber Daya (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="93904-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="93904-104">Bagian dari topik ini memberikan informasi tentang perubahan yang telah dibuat ke area manajemen sumber daya dari Dynamics 365 Project Service Automation versi 3. x.</span><span class="sxs-lookup"><span data-stu-id="93904-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="93904-105">Perkiraan proyek</span><span class="sxs-lookup"><span data-stu-id="93904-105">Project estimates</span></span>

<span data-ttu-id="93904-106">Alih-alih berdasarkan entitas **msdyn\_projecttask** (**tugasproyek**), perkiraan proyek didasarkan pada entitas **msdyn\_resourceassignment** (**penetapan sumber daya**).</span><span class="sxs-lookup"><span data-stu-id="93904-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="93904-107">Tugas sumber daya telah menjadi "sumber kebenaran" untuk penjadwalan tugas dan harga.</span><span class="sxs-lookup"><span data-stu-id="93904-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="93904-108">Baris tugas</span><span class="sxs-lookup"><span data-stu-id="93904-108">Line tasks</span></span>

<span data-ttu-id="93904-109">Dalam PSA 3. x, Baris tugas sudah usang (ditolak).</span><span class="sxs-lookup"><span data-stu-id="93904-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="93904-110">Tugas sekarang diarahkan ke tugas keseluruhan dan bukan baris tugas.</span><span class="sxs-lookup"><span data-stu-id="93904-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="93904-111">Contoh berikut menunjukkan cara kerja yang bernama "tes tugas" ditetapkan untuk anggota tim A dan B di versi sebelumnya PSA dan PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="93904-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="93904-112">**Sebelum PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="93904-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="93904-113">tes tugas</span><span class="sxs-lookup"><span data-stu-id="93904-113">Test task</span></span>

        - <span data-ttu-id="93904-114">tes tugas – baris tugas 1</span><span class="sxs-lookup"><span data-stu-id="93904-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="93904-115">Penetapan ke A</span><span class="sxs-lookup"><span data-stu-id="93904-115">Assignment to A</span></span>

        - <span data-ttu-id="93904-116">tes tugas – baris tugas 2</span><span class="sxs-lookup"><span data-stu-id="93904-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="93904-117">Penetapan ke B</span><span class="sxs-lookup"><span data-stu-id="93904-117">Assignment to B</span></span>

- <span data-ttu-id="93904-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="93904-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="93904-119">tes tugas</span><span class="sxs-lookup"><span data-stu-id="93904-119">Test task</span></span>

        - <span data-ttu-id="93904-120">Penetapan ke A</span><span class="sxs-lookup"><span data-stu-id="93904-120">Assignment to A</span></span>
        - <span data-ttu-id="93904-121">Penetapan ke B</span><span class="sxs-lookup"><span data-stu-id="93904-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="93904-122">Penugasan yang belum ditetapkan</span><span class="sxs-lookup"><span data-stu-id="93904-122">Unassigned assignment</span></span>

<span data-ttu-id="93904-123">Dalam PSA 3. x, tugas yang belum ditetapkan adalah tugas yang ditetapkan ke anggota tim **null** dan sumber daya **null**.</span><span class="sxs-lookup"><span data-stu-id="93904-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="93904-124">Tugas yang tidak ditetapkan dapat terjadi dalam beberapa skenario:</span><span class="sxs-lookup"><span data-stu-id="93904-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="93904-125">Jika tugas dibuat, namun belum ditetapkan ke anggota tim, tugas yang belum ditetapkan akan selalu dibuat.</span><span class="sxs-lookup"><span data-stu-id="93904-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="93904-126">Jika semua penerima tugas dihapus, tugas yang belum ditetapkan akan dibuat ulang untuk tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="93904-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="93904-127">Bidang penjadwalan pada entitas tugas proyek</span><span class="sxs-lookup"><span data-stu-id="93904-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="93904-128">Bidang entitas **msdyn\_projecttask** telah ditolak atau dipindahkan ke entitas **msdyn\_resourceassignment**, atau mereka sekarang dirujuk dari entitas **msdyn\_projectteam** (**anggota tim proyek**).</span><span class="sxs-lookup"><span data-stu-id="93904-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="93904-129">Bidang ditolak pada msdyn\_projecttask (tugas proyek)</span><span class="sxs-lookup"><span data-stu-id="93904-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="93904-130">Bidang baru pada msdyn\_resourceassignment (penetapan sumber daya)</span><span class="sxs-lookup"><span data-stu-id="93904-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="93904-131">Komentar</span><span class="sxs-lookup"><span data-stu-id="93904-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="93904-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="93904-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="93904-133">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="93904-133">None</span></span> | |
| <span data-ttu-id="93904-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="93904-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="93904-135">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="93904-135">None</span></span> | |
| <span data-ttu-id="93904-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="93904-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="93904-137">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="93904-137">None</span></span> | |
| <span data-ttu-id="93904-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="93904-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="93904-139">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="93904-139">None</span></span> | |
| <span data-ttu-id="93904-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="93904-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="93904-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="93904-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="93904-142">Format struktur data notasi objek JavaScript (JSON) yang disimpan di bidang telah diubah.</span><span class="sxs-lookup"><span data-stu-id="93904-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="93904-143">Kontur jadwal</span><span class="sxs-lookup"><span data-stu-id="93904-143">Schedule contour</span></span>

<span data-ttu-id="93904-144">Kontur jadwal disimpan di bidang **kerja yang direncanakan** (**msdyn\_plannedwork**) dari setiap entitas **penetapan sumber daya** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="93904-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="93904-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="93904-145">Structure</span></span>

<span data-ttu-id="93904-146">Struktur baru kontur jadwal terdiri dari potongan waktu fleksibel yang ditentukan untuk setiap hari jadwal.</span><span class="sxs-lookup"><span data-stu-id="93904-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="93904-147">Setiap potongan waktu memiliki properti berikut:</span><span class="sxs-lookup"><span data-stu-id="93904-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="93904-148">**Mulai** – dimulainya jam kerja untuk hari tersebut, sesuai kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="93904-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="93904-149">**Akhir** – akhir jam kerja untuk hari tersebut, sesuai kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="93904-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="93904-150">**Jam** – jumlah jam yang ditetapkan pada hari.</span><span class="sxs-lookup"><span data-stu-id="93904-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="93904-151">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="93904-151">**Example**</span></span>

<span data-ttu-id="93904-152">Contoh ini menggunakan kalender proyek dengan hari kerja adalah dari jam 9 hingga 5 sore di zona waktu UTC-8.</span><span class="sxs-lookup"><span data-stu-id="93904-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="93904-153">Penjadwalan otomatis dan penjadwalan manual</span><span class="sxs-lookup"><span data-stu-id="93904-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="93904-154">Jika tugas dijadwalkan otomatis, jam dimasukkan di depan, dan durasi tugas mungkin dikurangi.</span><span class="sxs-lookup"><span data-stu-id="93904-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="93904-155">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="93904-155">**Example**</span></span>

<span data-ttu-id="93904-156">Tugas berikut dijadwalkan otomatis selama 18 jam selama tiga hari (3 Desember 2018, hingga 5 Desember 2018).</span><span class="sxs-lookup"><span data-stu-id="93904-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="93904-157">Jika tugas dijadwalkan secara manual, jam akan didistribusikan secara merata ke semua tanggal.</span><span class="sxs-lookup"><span data-stu-id="93904-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="93904-158">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="93904-158">**Example**</span></span>

<span data-ttu-id="93904-159">Tugas berikut dijadwalkan secara manual selama 18 jam selama tiga hari (3 Desember 2018, hingga 5 Desember 2018).</span><span class="sxs-lookup"><span data-stu-id="93904-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="93904-160">Unit Penetapan</span><span class="sxs-lookup"><span data-stu-id="93904-160">Assignment unit</span></span>

<span data-ttu-id="93904-161">Unit penetapan telah ditolak dalam PSA 3. x.</span><span class="sxs-lookup"><span data-stu-id="93904-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="93904-162">Jam kerja tugas sekarang terbagi rata, per hari, di antara semua sumber daya yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="93904-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="93904-163">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="93904-163">**Example**</span></span>

<span data-ttu-id="93904-164">Dalam contoh ini, tugas ditetapkan ke dua sumber daya dan dijadwalkan otomatis untuk 36 jam selama tiga hari (3 Desember 2018, 5 Desember 2018).</span><span class="sxs-lookup"><span data-stu-id="93904-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="93904-165">Penetapan 1:</span><span class="sxs-lookup"><span data-stu-id="93904-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="93904-166">Penetapan 2:</span><span class="sxs-lookup"><span data-stu-id="93904-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="93904-167">Dimensi Harga</span><span class="sxs-lookup"><span data-stu-id="93904-167">Pricing dimensions</span></span>

<span data-ttu-id="93904-168">Di PSA 3.x, bidang dimensi harga spesifik sumber daya (seperti **peran** dan **unit organisasi**) telah dihapus dari entitas **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="93904-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="93904-169">Bidang ini sekarang dapat diperoleh dari anggota tim proyek terkait (**msdyn\_projectteam**) dari tugas sumber daya (**msdyn\_resourceassignment**) saat perkiraan proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="93904-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="93904-170">Bidang baru , **msdyn\_organizationalunit**, telah ditambahkan ke entitas **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="93904-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="93904-171">Bidang ditolak pada msdyn\_projecttask (tugas proyek)</span><span class="sxs-lookup"><span data-stu-id="93904-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="93904-172">Bidang dari msdyn\_projectteam (anggota tim proyek) yang digunakan sebagai gantinya</span><span class="sxs-lookup"><span data-stu-id="93904-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="93904-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="93904-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="93904-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="93904-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="93904-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="93904-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="93904-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="93904-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="93904-177">Kontur</span><span class="sxs-lookup"><span data-stu-id="93904-177">Contours</span></span>

<span data-ttu-id="93904-178">Bidang kontur harga dan perkiraan telah ditolak pada entitas **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="93904-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="93904-179">Mereka telah dipindahkan ke entitas **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="93904-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="93904-180">Bidang ditolak pada msdyn\_projecttask (tugas proyek)</span><span class="sxs-lookup"><span data-stu-id="93904-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="93904-181">Bidang baru pada msdyn\_resourceassignment (penetapan sumber daya)</span><span class="sxs-lookup"><span data-stu-id="93904-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="93904-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="93904-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="93904-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="93904-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="93904-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="93904-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="93904-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="93904-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="93904-186">Bidang berikut ini telah ditambahkan ke entitas **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="93904-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="93904-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="93904-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="93904-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="93904-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="93904-189">Bidang berikut untuk biaya dan penjualan yang direncanakan, aktual, dan tersisa tidak berubah pada entitas **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="93904-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="93904-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="93904-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="93904-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="93904-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="93904-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="93904-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="93904-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="93904-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="93904-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="93904-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="93904-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="93904-195">msdyn\_remainingsales</span></span>

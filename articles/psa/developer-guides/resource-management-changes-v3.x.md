---
title: Perubahan manajemen Sumber Daya (Project Service Automation 3.x)
description: Topik ini menyediakan informasi tentang perubahan area manajemen sumber daya.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148647"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="7b6fd-103">Perubahan manajemen Sumber Daya (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="7b6fd-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="7b6fd-104">Bagian dari topik ini memberikan informasi tentang perubahan yang telah dibuat ke area manajemen sumber daya dari Dynamics 365 Project Service Automation versi 3. x.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="7b6fd-105">Perkiraan proyek</span><span class="sxs-lookup"><span data-stu-id="7b6fd-105">Project estimates</span></span>

<span data-ttu-id="7b6fd-106">Alih-alih berdasarkan entitas **msdyn\_projecttask** (**tugasproyek**), perkiraan proyek didasarkan pada entitas **msdyn\_resourceassignment** (**penetapan sumber daya**).</span><span class="sxs-lookup"><span data-stu-id="7b6fd-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="7b6fd-107">Tugas sumber daya telah menjadi "sumber kebenaran" untuk penjadwalan tugas dan harga.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="7b6fd-108">Baris tugas</span><span class="sxs-lookup"><span data-stu-id="7b6fd-108">Line tasks</span></span>

<span data-ttu-id="7b6fd-109">Dalam PSA 3. x, Baris tugas sudah usang (ditolak).</span><span class="sxs-lookup"><span data-stu-id="7b6fd-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="7b6fd-110">Tugas sekarang diarahkan ke tugas keseluruhan dan bukan baris tugas.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="7b6fd-111">Contoh berikut menunjukkan cara kerja yang bernama "tes tugas" ditetapkan untuk anggota tim A dan B di versi sebelumnya PSA dan PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="7b6fd-112">**Sebelum PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="7b6fd-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="7b6fd-113">tes tugas</span><span class="sxs-lookup"><span data-stu-id="7b6fd-113">Test task</span></span>

        - <span data-ttu-id="7b6fd-114">tes tugas – baris tugas 1</span><span class="sxs-lookup"><span data-stu-id="7b6fd-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="7b6fd-115">Penetapan ke A</span><span class="sxs-lookup"><span data-stu-id="7b6fd-115">Assignment to A</span></span>

        - <span data-ttu-id="7b6fd-116">tes tugas – baris tugas 2</span><span class="sxs-lookup"><span data-stu-id="7b6fd-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="7b6fd-117">Penetapan ke B</span><span class="sxs-lookup"><span data-stu-id="7b6fd-117">Assignment to B</span></span>

- <span data-ttu-id="7b6fd-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="7b6fd-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="7b6fd-119">tes tugas</span><span class="sxs-lookup"><span data-stu-id="7b6fd-119">Test task</span></span>

        - <span data-ttu-id="7b6fd-120">Penetapan ke A</span><span class="sxs-lookup"><span data-stu-id="7b6fd-120">Assignment to A</span></span>
        - <span data-ttu-id="7b6fd-121">Penetapan ke B</span><span class="sxs-lookup"><span data-stu-id="7b6fd-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="7b6fd-122">Penugasan yang belum ditetapkan</span><span class="sxs-lookup"><span data-stu-id="7b6fd-122">Unassigned assignment</span></span>

<span data-ttu-id="7b6fd-123">Dalam PSA 3. x, tugas yang belum ditetapkan adalah tugas yang ditetapkan ke anggota tim **null** dan sumber daya **null**.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="7b6fd-124">Tugas yang tidak ditetapkan dapat terjadi dalam beberapa skenario:</span><span class="sxs-lookup"><span data-stu-id="7b6fd-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="7b6fd-125">Jika tugas dibuat, namun belum ditetapkan ke anggota tim, tugas yang belum ditetapkan akan selalu dibuat.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="7b6fd-126">Jika semua penerima tugas dihapus, tugas yang belum ditetapkan akan dibuat ulang untuk tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="7b6fd-127">Bidang penjadwalan pada entitas tugas proyek</span><span class="sxs-lookup"><span data-stu-id="7b6fd-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="7b6fd-128">Bidang entitas **msdyn\_projecttask** telah ditolak atau dipindahkan ke entitas **msdyn\_resourceassignment**, atau mereka sekarang dirujuk dari entitas **msdyn\_projectteam** (**anggota tim proyek**).</span><span class="sxs-lookup"><span data-stu-id="7b6fd-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="7b6fd-129">Bidang ditolak pada msdyn\_projecttask (tugas proyek)</span><span class="sxs-lookup"><span data-stu-id="7b6fd-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="7b6fd-130">Bidang baru pada msdyn\_resourceassignment (penetapan sumber daya)</span><span class="sxs-lookup"><span data-stu-id="7b6fd-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="7b6fd-131">Komentar</span><span class="sxs-lookup"><span data-stu-id="7b6fd-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="7b6fd-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="7b6fd-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="7b6fd-133">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="7b6fd-133">None</span></span> | |
| <span data-ttu-id="7b6fd-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="7b6fd-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="7b6fd-135">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="7b6fd-135">None</span></span> | |
| <span data-ttu-id="7b6fd-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="7b6fd-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="7b6fd-137">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="7b6fd-137">None</span></span> | |
| <span data-ttu-id="7b6fd-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="7b6fd-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="7b6fd-139">Tidak ada</span><span class="sxs-lookup"><span data-stu-id="7b6fd-139">None</span></span> | |
| <span data-ttu-id="7b6fd-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="7b6fd-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="7b6fd-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="7b6fd-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="7b6fd-142">Format struktur data notasi objek JavaScript (JSON) yang disimpan di bidang telah diubah.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="7b6fd-143">Kontur jadwal</span><span class="sxs-lookup"><span data-stu-id="7b6fd-143">Schedule contour</span></span>

<span data-ttu-id="7b6fd-144">Kontur jadwal disimpan di bidang **kerja yang direncanakan** (**msdyn\_plannedwork**) dari setiap entitas **penetapan sumber daya** (**msdyn\_resourceassignment**).</span><span class="sxs-lookup"><span data-stu-id="7b6fd-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="7b6fd-145">Struktur</span><span class="sxs-lookup"><span data-stu-id="7b6fd-145">Structure</span></span>

<span data-ttu-id="7b6fd-146">Struktur baru kontur jadwal terdiri dari potongan waktu fleksibel yang ditentukan untuk setiap hari jadwal.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="7b6fd-147">Setiap potongan waktu memiliki properti berikut:</span><span class="sxs-lookup"><span data-stu-id="7b6fd-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="7b6fd-148">**Mulai** – dimulainya jam kerja untuk hari tersebut, sesuai kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="7b6fd-149">**Akhir** – akhir jam kerja untuk hari tersebut, sesuai kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="7b6fd-150">**Jam** – jumlah jam yang ditetapkan pada hari.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="7b6fd-151">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="7b6fd-151">**Example**</span></span>

<span data-ttu-id="7b6fd-152">Contoh ini menggunakan kalender proyek dengan hari kerja adalah dari jam 9 hingga 5 sore di zona waktu UTC-8.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="7b6fd-153">Penjadwalan otomatis dan penjadwalan manual</span><span class="sxs-lookup"><span data-stu-id="7b6fd-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="7b6fd-154">Jika tugas dijadwalkan otomatis, jam dimasukkan di depan, dan durasi tugas mungkin dikurangi.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="7b6fd-155">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="7b6fd-155">**Example**</span></span>

<span data-ttu-id="7b6fd-156">Tugas berikut dijadwalkan otomatis selama 18 jam selama tiga hari (3 Desember 2018, hingga 5 Desember 2018).</span><span class="sxs-lookup"><span data-stu-id="7b6fd-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="7b6fd-157">Jika tugas dijadwalkan secara manual, jam akan didistribusikan secara merata ke semua tanggal.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="7b6fd-158">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="7b6fd-158">**Example**</span></span>

<span data-ttu-id="7b6fd-159">Tugas berikut dijadwalkan secara manual selama 18 jam selama tiga hari (3 Desember 2018, hingga 5 Desember 2018).</span><span class="sxs-lookup"><span data-stu-id="7b6fd-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="7b6fd-160">Unit Penetapan</span><span class="sxs-lookup"><span data-stu-id="7b6fd-160">Assignment unit</span></span>

<span data-ttu-id="7b6fd-161">Unit penetapan telah ditolak dalam PSA 3. x.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="7b6fd-162">Jam kerja tugas sekarang terbagi rata, per hari, di antara semua sumber daya yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="7b6fd-163">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="7b6fd-163">**Example**</span></span>

<span data-ttu-id="7b6fd-164">Dalam contoh ini, tugas ditetapkan ke dua sumber daya dan dijadwalkan otomatis untuk 36 jam selama tiga hari (3 Desember 2018, 5 Desember 2018).</span><span class="sxs-lookup"><span data-stu-id="7b6fd-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="7b6fd-165">Penetapan 1:</span><span class="sxs-lookup"><span data-stu-id="7b6fd-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="7b6fd-166">Penetapan 2:</span><span class="sxs-lookup"><span data-stu-id="7b6fd-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="7b6fd-167">Dimensi Harga</span><span class="sxs-lookup"><span data-stu-id="7b6fd-167">Pricing dimensions</span></span>

<span data-ttu-id="7b6fd-168">Di PSA 3.x, bidang dimensi harga spesifik sumber daya (seperti **peran** dan **unit organisasi**) telah dihapus dari entitas **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="7b6fd-169">Bidang ini sekarang dapat diperoleh dari anggota tim proyek terkait (**msdyn\_projectteam**) dari tugas sumber daya (**msdyn\_resourceassignment**) saat perkiraan proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="7b6fd-170">Bidang baru , **msdyn\_organizationalunit**, telah ditambahkan ke entitas **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="7b6fd-171">Bidang ditolak pada msdyn\_projecttask (tugas proyek)</span><span class="sxs-lookup"><span data-stu-id="7b6fd-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="7b6fd-172">Bidang dari msdyn\_projectteam (anggota tim proyek) yang digunakan sebagai gantinya</span><span class="sxs-lookup"><span data-stu-id="7b6fd-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="7b6fd-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="7b6fd-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="7b6fd-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="7b6fd-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="7b6fd-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="7b6fd-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="7b6fd-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="7b6fd-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="7b6fd-177">Kontur</span><span class="sxs-lookup"><span data-stu-id="7b6fd-177">Contours</span></span>

<span data-ttu-id="7b6fd-178">Bidang kontur harga dan perkiraan telah ditolak pada entitas **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="7b6fd-179">Mereka telah dipindahkan ke entitas **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="7b6fd-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="7b6fd-180">Bidang ditolak pada msdyn\_projecttask (tugas proyek)</span><span class="sxs-lookup"><span data-stu-id="7b6fd-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="7b6fd-181">Bidang baru pada msdyn\_resourceassignment (penetapan sumber daya)</span><span class="sxs-lookup"><span data-stu-id="7b6fd-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="7b6fd-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="7b6fd-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="7b6fd-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="7b6fd-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="7b6fd-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="7b6fd-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="7b6fd-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="7b6fd-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="7b6fd-186">Bidang berikut ini telah ditambahkan ke entitas **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="7b6fd-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="7b6fd-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7b6fd-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="7b6fd-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7b6fd-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="7b6fd-189">Bidang berikut untuk biaya dan penjualan yang direncanakan, aktual, dan tersisa tidak berubah pada entitas **msdyn\_projecttask**:</span><span class="sxs-lookup"><span data-stu-id="7b6fd-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="7b6fd-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="7b6fd-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="7b6fd-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="7b6fd-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="7b6fd-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="7b6fd-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="7b6fd-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="7b6fd-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="7b6fd-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="7b6fd-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="7b6fd-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="7b6fd-195">msdyn\_remainingsales</span></span>

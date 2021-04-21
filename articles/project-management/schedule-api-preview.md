---
title: Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan
description: Pembaruan topik memberikan informasi dan sampel untuk menggunakan API Jadwal.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868133"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="181d0-103">Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="181d0-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="181d0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="181d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="181d0-105">Beberapa atau semua fungsi yang tercantum dalam topik ini tersedia sebagai bagian dari rilis pratinjau.</span><span class="sxs-lookup"><span data-stu-id="181d0-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="181d0-106">Konten dan fungsi ini dapat berubah.</span><span class="sxs-lookup"><span data-stu-id="181d0-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="181d0-107">Entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="181d0-107">Scheduling entities</span></span>

<span data-ttu-id="181d0-108">API jadwal memberikan kemampuan untuk melakukan operasi pembuatan, pembaruan, dan penghapusan dengan **entitas Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="181d0-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="181d0-109">Entitas ini dikelola melalui mesin Penjadwalan di Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="181d0-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="181d0-110">Membuat, memperbarui, dan menghapus operasi dengan **entitas Penjadwalan** dibatasi di rilis Dynamics 365 Project Operations sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="181d0-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="181d0-111">Tabel berikut menyediakan daftar lengkap **entitas Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="181d0-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="181d0-112">Nama entitas</span><span class="sxs-lookup"><span data-stu-id="181d0-112">Entity name</span></span>  | <span data-ttu-id="181d0-113">Nama logika entitas</span><span class="sxs-lookup"><span data-stu-id="181d0-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="181d0-114">Project</span><span class="sxs-lookup"><span data-stu-id="181d0-114">Project</span></span> | <span data-ttu-id="181d0-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="181d0-115">msdyn_project</span></span> |
| <span data-ttu-id="181d0-116">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-116">Project Task</span></span>  | <span data-ttu-id="181d0-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="181d0-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="181d0-118">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-118">Project Task Dependency</span></span>  | <span data-ttu-id="181d0-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="181d0-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="181d0-120">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="181d0-120">Resource Assignment</span></span> | <span data-ttu-id="181d0-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="181d0-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="181d0-122">Wadah Proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-122">Project Bucket</span></span>  | <span data-ttu-id="181d0-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="181d0-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="181d0-124">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-124">Project Team Member</span></span> | <span data-ttu-id="181d0-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="181d0-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="181d0-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="181d0-126">OperationSet</span></span>

<span data-ttu-id="181d0-127">OperationSet adalah pola unit kerja yang dapat digunakan ketika beberapa jadwal yang mempengaruhi permintaan harus diproses dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="181d0-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="181d0-128">API Jadwal</span><span class="sxs-lookup"><span data-stu-id="181d0-128">Schedule APIs</span></span>

<span data-ttu-id="181d0-129">Berikut adalah daftar API Jadwal saat ini.</span><span class="sxs-lookup"><span data-stu-id="181d0-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="181d0-130">**msdyn_CreateProjectV1**: API ini dapat digunakan untuk membuat proyek.</span><span class="sxs-lookup"><span data-stu-id="181d0-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="181d0-131">Proyek dan wadah proyek default dibuat dengan segera.</span><span class="sxs-lookup"><span data-stu-id="181d0-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="181d0-132">**msdyn_CreateTeamMemberV1**: API ini dapat digunakan untuk membuat anggota tim proyek.</span><span class="sxs-lookup"><span data-stu-id="181d0-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="181d0-133">Rekaman anggota tim akan segera dibuat.</span><span class="sxs-lookup"><span data-stu-id="181d0-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="181d0-134">**msdyn_CreateOperationSetV1**: API ini dapat digunakan untuk menjadwalkan beberapa permintaan yang harus dilakukan dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="181d0-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="181d0-135">**msdyn_PSSCreateV1**: API ini dapat digunakan untuk membuat entitas.</span><span class="sxs-lookup"><span data-stu-id="181d0-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="181d0-136">Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi pembuatan.</span><span class="sxs-lookup"><span data-stu-id="181d0-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="181d0-137">**msdyn_PSSUpdateV1**: API ini dapat digunakan untuk memperbarui entitas.</span><span class="sxs-lookup"><span data-stu-id="181d0-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="181d0-138">Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi pembaruan.</span><span class="sxs-lookup"><span data-stu-id="181d0-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="181d0-139">**msdyn_PSSDeleteV1**: API ini dapat digunakan untuk menghapus entitas.</span><span class="sxs-lookup"><span data-stu-id="181d0-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="181d0-140">Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi penghapusan.</span><span class="sxs-lookup"><span data-stu-id="181d0-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="181d0-141">**msdyn_ExecuteOperationSetV1**: API ini digunakan untuk mengeksekusi semua operasi dalam rangkaian operasi yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="181d0-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="181d0-142">Menggunakan API Jadwal dengan OperationSet</span><span class="sxs-lookup"><span data-stu-id="181d0-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="181d0-143">Karena rekaman dengan **CreateProjectV1** dan **CreateTeamMemberV1** dibuat dengan segera, API ini tidak dapat digunakan di **OperationSet** secara langsung.</span><span class="sxs-lookup"><span data-stu-id="181d0-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="181d0-144">Namun, Anda dapat menggunakan API untuk membuat rekaman yang diperlukan, membuat **OperationSet**, dan kemudian menggunakan rekaman yang dibuat sebelumnya di **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="181d0-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="181d0-145">Operasi yang Didukung</span><span class="sxs-lookup"><span data-stu-id="181d0-145">Supported operations</span></span>

| <span data-ttu-id="181d0-146">Entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="181d0-146">Scheduling entity</span></span> | <span data-ttu-id="181d0-147">Buat</span><span class="sxs-lookup"><span data-stu-id="181d0-147">Create</span></span> | <span data-ttu-id="181d0-148">Pembaruan</span><span class="sxs-lookup"><span data-stu-id="181d0-148">Update</span></span> | <span data-ttu-id="181d0-149">Delete</span><span class="sxs-lookup"><span data-stu-id="181d0-149">Delete</span></span> | <span data-ttu-id="181d0-150">Pertimbangan penting</span><span class="sxs-lookup"><span data-stu-id="181d0-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="181d0-151">Tugas proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-151">Project task</span></span> | <span data-ttu-id="181d0-152">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-152">Yes</span></span> | <span data-ttu-id="181d0-153">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-153">Yes</span></span> | <span data-ttu-id="181d0-154">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-154">Yes</span></span> | <span data-ttu-id="181d0-155">Tidak Ada</span><span class="sxs-lookup"><span data-stu-id="181d0-155">None</span></span> |
| <span data-ttu-id="181d0-156">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-156">Project task dependency</span></span> | <span data-ttu-id="181d0-157">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-157">Yes</span></span> | <span data-ttu-id="181d0-158">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-158">Yes</span></span> | | <span data-ttu-id="181d0-159">Rekaman dependensi tugas proyek tidak diperbarui.</span><span class="sxs-lookup"><span data-stu-id="181d0-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="181d0-160">Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat.</span><span class="sxs-lookup"><span data-stu-id="181d0-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="181d0-161">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="181d0-161">Resource assignment</span></span> | <span data-ttu-id="181d0-162">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-162">Yes</span></span> | <span data-ttu-id="181d0-163">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-163">Yes</span></span> | | <span data-ttu-id="181d0-164">Operasi dengan bidang berikut tidak didukung: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, dan **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="181d0-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="181d0-165">Rekaman penetapan sumber daya tidak diperbarui.</span><span class="sxs-lookup"><span data-stu-id="181d0-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="181d0-166">Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat.</span><span class="sxs-lookup"><span data-stu-id="181d0-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="181d0-167">Wadah Proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-167">Project bucket</span></span> | <span data-ttu-id="181d0-168">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="181d0-168">N/A</span></span> | <span data-ttu-id="181d0-169">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="181d0-169">N/A</span></span> | <span data-ttu-id="181d0-170">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="181d0-170">N/A</span></span> | <span data-ttu-id="181d0-171">Seeer default dibuat menggunakan API **CREATEKainyV1**.</span><span class="sxs-lookup"><span data-stu-id="181d0-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="181d0-172">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="181d0-172">Project team member</span></span> | <span data-ttu-id="181d0-173">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-173">Yes</span></span> | <span data-ttu-id="181d0-174">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-174">Yes</span></span> | <span data-ttu-id="181d0-175">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-175">Yes</span></span> | <span data-ttu-id="181d0-176">Untuk operasi pembuatan, gunakan API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="181d0-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="181d0-177">Project</span><span class="sxs-lookup"><span data-stu-id="181d0-177">Project</span></span> | <span data-ttu-id="181d0-178">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-178">Yes</span></span> | <span data-ttu-id="181d0-179">Ya</span><span class="sxs-lookup"><span data-stu-id="181d0-179">Yes</span></span> | <span data-ttu-id="181d0-180">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="181d0-180">N/A</span></span> | <span data-ttu-id="181d0-181">Operasi dengan bidang berikut tidak didukung: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, dan **Duration**.</span><span class="sxs-lookup"><span data-stu-id="181d0-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="181d0-182">API ini dapat dipanggil dengan objek entitas yang mencakup bidang kustom.</span><span class="sxs-lookup"><span data-stu-id="181d0-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="181d0-183">Properti ID bersifat opsional.</span><span class="sxs-lookup"><span data-stu-id="181d0-183">The ID property is optional.</span></span> <span data-ttu-id="181d0-184">Jika diberikan, sistem mencoba menggunakannya dan memberikan pengecualian jika tidak dapat digunakan.</span><span class="sxs-lookup"><span data-stu-id="181d0-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="181d0-185">Jika tidak disediakan, sistem akan membuatnya.</span><span class="sxs-lookup"><span data-stu-id="181d0-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="181d0-186">Masalah dan batasan yang diketahui</span><span class="sxs-lookup"><span data-stu-id="181d0-186">Limitations and known issues</span></span>
<span data-ttu-id="181d0-187">Berikut adalah daftar batasan dan masalah umum:</span><span class="sxs-lookup"><span data-stu-id="181d0-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="181d0-188">API jadwal hanya dapat digunakan oleh **Pengguna dengan Lisensi Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="181d0-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="181d0-189">Tidak dapat digunakan oleh:</span><span class="sxs-lookup"><span data-stu-id="181d0-189">They can't be used by:</span></span>
    - <span data-ttu-id="181d0-190">Pengguna Aplikasi</span><span class="sxs-lookup"><span data-stu-id="181d0-190">Application users</span></span>
    - <span data-ttu-id="181d0-191">Pengguna Sistem</span><span class="sxs-lookup"><span data-stu-id="181d0-191">System users</span></span>
    - <span data-ttu-id="181d0-192">Pengguna Integrasi</span><span class="sxs-lookup"><span data-stu-id="181d0-192">Integration users</span></span>
    - <span data-ttu-id="181d0-193">Pengguna lain yang tidak memiliki lisensi yang diperlukan</span><span class="sxs-lookup"><span data-stu-id="181d0-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="181d0-194">Setiap **OperationSet** hanya dapat memiliki maksimum 100 operasi.</span><span class="sxs-lookup"><span data-stu-id="181d0-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="181d0-195">Setiap pengguna hanya dapat membuka maksimum 10 **OperationSet** terbuka.</span><span class="sxs-lookup"><span data-stu-id="181d0-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="181d0-196">Project Operations saat ini mendukung maksimum 500 tugas total pada proyek.</span><span class="sxs-lookup"><span data-stu-id="181d0-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="181d0-197">Status kegagalan dan log kegagalan **OperationSet** saat ini tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="181d0-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="181d0-198">API Jadwal ada dalam pratinjau umum.</span><span class="sxs-lookup"><span data-stu-id="181d0-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="181d0-199">Menggunakan API ini di lingkungan Produksi tidak didukung oleh Microsoft.</span><span class="sxs-lookup"><span data-stu-id="181d0-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="181d0-200">Contoh Skenario</span><span class="sxs-lookup"><span data-stu-id="181d0-200">Sample scenario</span></span>

<span data-ttu-id="181d0-201">Dalam skenario ini, Anda akan membuat proyek, anggota tim, empat tugas, dan dua penugasan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="181d0-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="181d0-202">Selanjutnya, Anda akan memperbarui satu tugas, memperbarui proyek, menghapus satu tugas, menghapus satu penetapan sumber daya, dan membuat dependensi tugas.</span><span class="sxs-lookup"><span data-stu-id="181d0-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="181d0-203">Contoh tambahan</span><span class="sxs-lookup"><span data-stu-id="181d0-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };
    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
    return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";
    return project;
}

private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
        task["new_amount"] = 591.34m;
        task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }
    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;
    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);
    return taskDependency;
}

#endregion

#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```

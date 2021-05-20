---
title: Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan
description: Pembaruan topik memberikan informasi dan sampel untuk menggunakan API Jadwal.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950808"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="89ff8-103">Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="89ff8-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="89ff8-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="89ff8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="89ff8-105">Beberapa atau semua fungsi yang tercantum dalam topik ini tersedia sebagai bagian dari rilis pratinjau.</span><span class="sxs-lookup"><span data-stu-id="89ff8-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="89ff8-106">Konten dan fungsi ini dapat berubah.</span><span class="sxs-lookup"><span data-stu-id="89ff8-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="89ff8-107">Entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="89ff8-107">Scheduling entities</span></span>

<span data-ttu-id="89ff8-108">API jadwal memberikan kemampuan untuk melakukan operasi pembuatan, pembaruan, dan penghapusan dengan **entitas Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="89ff8-109">Entitas ini dikelola melalui mesin Penjadwalan di Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="89ff8-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="89ff8-110">Membuat, memperbarui, dan menghapus operasi dengan **entitas Penjadwalan** dibatasi di rilis Dynamics 365 Project Operations sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="89ff8-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="89ff8-111">Tabel berikut menyediakan daftar lengkap **entitas Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="89ff8-112">Nama entitas</span><span class="sxs-lookup"><span data-stu-id="89ff8-112">Entity name</span></span>  | <span data-ttu-id="89ff8-113">Nama logika entitas</span><span class="sxs-lookup"><span data-stu-id="89ff8-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="89ff8-114">Project</span><span class="sxs-lookup"><span data-stu-id="89ff8-114">Project</span></span> | <span data-ttu-id="89ff8-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="89ff8-115">msdyn_project</span></span> |
| <span data-ttu-id="89ff8-116">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-116">Project Task</span></span>  | <span data-ttu-id="89ff8-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="89ff8-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="89ff8-118">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-118">Project Task Dependency</span></span>  | <span data-ttu-id="89ff8-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="89ff8-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="89ff8-120">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="89ff8-120">Resource Assignment</span></span> | <span data-ttu-id="89ff8-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="89ff8-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="89ff8-122">Wadah Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-122">Project Bucket</span></span>  | <span data-ttu-id="89ff8-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="89ff8-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="89ff8-124">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-124">Project Team Member</span></span> | <span data-ttu-id="89ff8-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="89ff8-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="89ff8-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="89ff8-126">OperationSet</span></span>

<span data-ttu-id="89ff8-127">OperationSet adalah pola unit kerja yang dapat digunakan ketika beberapa jadwal yang mempengaruhi permintaan harus diproses dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="89ff8-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="89ff8-128">API Jadwal</span><span class="sxs-lookup"><span data-stu-id="89ff8-128">Schedule APIs</span></span>

<span data-ttu-id="89ff8-129">Berikut adalah daftar API Jadwal saat ini.</span><span class="sxs-lookup"><span data-stu-id="89ff8-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="89ff8-130">**msdyn_CreateProjectV1**: API ini dapat digunakan untuk membuat proyek.</span><span class="sxs-lookup"><span data-stu-id="89ff8-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="89ff8-131">Proyek dan wadah proyek default dibuat dengan segera.</span><span class="sxs-lookup"><span data-stu-id="89ff8-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="89ff8-132">**msdyn_CreateTeamMemberV1**: API ini dapat digunakan untuk membuat anggota tim proyek.</span><span class="sxs-lookup"><span data-stu-id="89ff8-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="89ff8-133">Rekaman anggota tim akan segera dibuat.</span><span class="sxs-lookup"><span data-stu-id="89ff8-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="89ff8-134">**msdyn_CreateOperationSetV1**: API ini dapat digunakan untuk menjadwalkan beberapa permintaan yang harus dilakukan dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="89ff8-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="89ff8-135">**msdyn_PSSCreateV1**: API ini dapat digunakan untuk membuat entitas.</span><span class="sxs-lookup"><span data-stu-id="89ff8-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="89ff8-136">Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi pembuatan.</span><span class="sxs-lookup"><span data-stu-id="89ff8-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="89ff8-137">**msdyn_PSSUpdateV1**: API ini dapat digunakan untuk memperbarui entitas.</span><span class="sxs-lookup"><span data-stu-id="89ff8-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="89ff8-138">Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi pembaruan.</span><span class="sxs-lookup"><span data-stu-id="89ff8-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="89ff8-139">**msdyn_PSSDeleteV1**: API ini dapat digunakan untuk menghapus entitas.</span><span class="sxs-lookup"><span data-stu-id="89ff8-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="89ff8-140">Entitas dapat menjadi salah satu entitas Penjadwalan yang mendukung operasi penghapusan.</span><span class="sxs-lookup"><span data-stu-id="89ff8-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="89ff8-141">**msdyn_ExecuteOperationSetV1**: API ini digunakan untuk mengeksekusi semua operasi dalam rangkaian operasi yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="89ff8-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="89ff8-142">Menggunakan API Jadwal dengan OperationSet</span><span class="sxs-lookup"><span data-stu-id="89ff8-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="89ff8-143">Karena rekaman dengan **CreateProjectV1** dan **CreateTeamMemberV1** dibuat dengan segera, API ini tidak dapat digunakan di **OperationSet** secara langsung.</span><span class="sxs-lookup"><span data-stu-id="89ff8-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="89ff8-144">Namun, Anda dapat menggunakan API untuk membuat rekaman yang diperlukan, membuat **OperationSet**, dan kemudian menggunakan rekaman yang dibuat sebelumnya di **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="89ff8-145">Operasi yang Didukung</span><span class="sxs-lookup"><span data-stu-id="89ff8-145">Supported operations</span></span>

| <span data-ttu-id="89ff8-146">Entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="89ff8-146">Scheduling entity</span></span> | <span data-ttu-id="89ff8-147">Buat</span><span class="sxs-lookup"><span data-stu-id="89ff8-147">Create</span></span> | <span data-ttu-id="89ff8-148">Pembaruan</span><span class="sxs-lookup"><span data-stu-id="89ff8-148">Update</span></span> | <span data-ttu-id="89ff8-149">Delete</span><span class="sxs-lookup"><span data-stu-id="89ff8-149">Delete</span></span> | <span data-ttu-id="89ff8-150">Pertimbangan penting</span><span class="sxs-lookup"><span data-stu-id="89ff8-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="89ff8-151">Tugas proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-151">Project task</span></span> | <span data-ttu-id="89ff8-152">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-152">Yes</span></span> | <span data-ttu-id="89ff8-153">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-153">Yes</span></span> | <span data-ttu-id="89ff8-154">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-154">Yes</span></span> | <span data-ttu-id="89ff8-155">Tidak Ada</span><span class="sxs-lookup"><span data-stu-id="89ff8-155">None</span></span> |
| <span data-ttu-id="89ff8-156">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-156">Project task dependency</span></span> | <span data-ttu-id="89ff8-157">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-157">Yes</span></span> | <span data-ttu-id="89ff8-158">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-158">Yes</span></span> | | <span data-ttu-id="89ff8-159">Rekaman dependensi tugas proyek tidak diperbarui.</span><span class="sxs-lookup"><span data-stu-id="89ff8-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="89ff8-160">Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat.</span><span class="sxs-lookup"><span data-stu-id="89ff8-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="89ff8-161">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="89ff8-161">Resource assignment</span></span> | <span data-ttu-id="89ff8-162">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-162">Yes</span></span> | <span data-ttu-id="89ff8-163">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-163">Yes</span></span> | | <span data-ttu-id="89ff8-164">Operasi dengan bidang berikut tidak didukung: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, dan **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="89ff8-165">Rekaman penetapan sumber daya tidak diperbarui.</span><span class="sxs-lookup"><span data-stu-id="89ff8-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="89ff8-166">Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat.</span><span class="sxs-lookup"><span data-stu-id="89ff8-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="89ff8-167">Wadah Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-167">Project bucket</span></span> | <span data-ttu-id="89ff8-168">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="89ff8-168">N/A</span></span> | <span data-ttu-id="89ff8-169">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="89ff8-169">N/A</span></span> | <span data-ttu-id="89ff8-170">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="89ff8-170">N/A</span></span> | <span data-ttu-id="89ff8-171">Seeer default dibuat menggunakan API **CREATEKainyV1**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="89ff8-172">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-172">Project team member</span></span> | <span data-ttu-id="89ff8-173">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-173">Yes</span></span> | <span data-ttu-id="89ff8-174">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-174">Yes</span></span> | <span data-ttu-id="89ff8-175">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-175">Yes</span></span> | <span data-ttu-id="89ff8-176">Untuk operasi pembuatan, gunakan API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="89ff8-177">Project</span><span class="sxs-lookup"><span data-stu-id="89ff8-177">Project</span></span> | <span data-ttu-id="89ff8-178">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-178">Yes</span></span> | <span data-ttu-id="89ff8-179">Ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-179">Yes</span></span> | <span data-ttu-id="89ff8-180">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="89ff8-180">N/A</span></span> | <span data-ttu-id="89ff8-181">Operasi dengan bidang berikut tidak didukung: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, dan **Duration**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="89ff8-182">API ini dapat dipanggil dengan objek entitas yang mencakup bidang kustom.</span><span class="sxs-lookup"><span data-stu-id="89ff8-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="89ff8-183">Properti ID bersifat opsional.</span><span class="sxs-lookup"><span data-stu-id="89ff8-183">The ID property is optional.</span></span> <span data-ttu-id="89ff8-184">Jika diberikan, sistem mencoba menggunakannya dan memberikan pengecualian jika tidak dapat digunakan.</span><span class="sxs-lookup"><span data-stu-id="89ff8-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="89ff8-185">Jika tidak disediakan, sistem akan membuatnya.</span><span class="sxs-lookup"><span data-stu-id="89ff8-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="89ff8-186">Bidang dibatasi</span><span class="sxs-lookup"><span data-stu-id="89ff8-186">Restricted fields</span></span>

<span data-ttu-id="89ff8-187">Tabel berikut menentukan bidang yang dibatasi dari **Buat** dan **Edit**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="89ff8-188">Tugas proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-188">Project task</span></span>

| <span data-ttu-id="89ff8-189">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="89ff8-189">**Logical name**</span></span>                       | <span data-ttu-id="89ff8-190">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="89ff8-190">**Can create**</span></span> | <span data-ttu-id="89ff8-191">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="89ff8-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="89ff8-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="89ff8-193">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-193">no</span></span>             | <span data-ttu-id="89ff8-194">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-194">no</span></span>               |
| <span data-ttu-id="89ff8-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="89ff8-196">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-196">no</span></span>             | <span data-ttu-id="89ff8-197">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-197">no</span></span>               |
| <span data-ttu-id="89ff8-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="89ff8-198">msdyn_actualend</span></span>                        | <span data-ttu-id="89ff8-199">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-199">no</span></span>             | <span data-ttu-id="89ff8-200">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-200">no</span></span>               |
| <span data-ttu-id="89ff8-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="89ff8-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="89ff8-202">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-202">no</span></span>             | <span data-ttu-id="89ff8-203">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-203">no</span></span>               |
| <span data-ttu-id="89ff8-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="89ff8-205">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-205">no</span></span>             | <span data-ttu-id="89ff8-206">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-206">no</span></span>               |
| <span data-ttu-id="89ff8-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="89ff8-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="89ff8-208">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-208">no</span></span>             | <span data-ttu-id="89ff8-209">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-209">no</span></span>               |
| <span data-ttu-id="89ff8-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="89ff8-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="89ff8-211">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-211">no</span></span>             | <span data-ttu-id="89ff8-212">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-212">no</span></span>               |
| <span data-ttu-id="89ff8-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="89ff8-214">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-214">no</span></span>             | <span data-ttu-id="89ff8-215">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-215">no</span></span>               |
| <span data-ttu-id="89ff8-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="89ff8-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="89ff8-217">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-217">no</span></span>             | <span data-ttu-id="89ff8-218">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-218">no</span></span>               |
| <span data-ttu-id="89ff8-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="89ff8-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="89ff8-220">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-220">no</span></span>             | <span data-ttu-id="89ff8-221">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-221">no</span></span>               |
| <span data-ttu-id="89ff8-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="89ff8-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="89ff8-223">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-223">no</span></span>             | <span data-ttu-id="89ff8-224">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-224">no</span></span>               |
| <span data-ttu-id="89ff8-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="89ff8-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="89ff8-226">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-226">no</span></span>             | <span data-ttu-id="89ff8-227">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-227">no</span></span>               |
| <span data-ttu-id="89ff8-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="89ff8-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="89ff8-229">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-229">no</span></span>             | <span data-ttu-id="89ff8-230">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-230">no</span></span>               |
| <span data-ttu-id="89ff8-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="89ff8-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="89ff8-232">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-232">no</span></span>             | <span data-ttu-id="89ff8-233">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-233">no</span></span>               |
| <span data-ttu-id="89ff8-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="89ff8-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="89ff8-235">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-235">no</span></span>             | <span data-ttu-id="89ff8-236">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-236">no</span></span>               |
| <span data-ttu-id="89ff8-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="89ff8-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="89ff8-238">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-238">no</span></span>             | <span data-ttu-id="89ff8-239">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-239">no</span></span>               |
| <span data-ttu-id="89ff8-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="89ff8-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="89ff8-241">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-241">no</span></span>             | <span data-ttu-id="89ff8-242">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-242">no</span></span>               |
| <span data-ttu-id="89ff8-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="89ff8-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="89ff8-244">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-244">no</span></span>             | <span data-ttu-id="89ff8-245">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-245">no</span></span>               |
| <span data-ttu-id="89ff8-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="89ff8-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="89ff8-247">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-247">no</span></span>             | <span data-ttu-id="89ff8-248">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-248">no</span></span>               |
| <span data-ttu-id="89ff8-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="89ff8-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="89ff8-250">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-250">no</span></span>             | <span data-ttu-id="89ff8-251">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-251">no</span></span>               |
| <span data-ttu-id="89ff8-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="89ff8-253">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-253">no</span></span>             | <span data-ttu-id="89ff8-254">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-254">no</span></span>               |
| <span data-ttu-id="89ff8-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="89ff8-256">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-256">no</span></span>             | <span data-ttu-id="89ff8-257">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-257">no</span></span>               |
| <span data-ttu-id="89ff8-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="89ff8-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="89ff8-259">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-259">no</span></span>             | <span data-ttu-id="89ff8-260">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-260">no</span></span>               |
| <span data-ttu-id="89ff8-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="89ff8-262">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-262">no</span></span>             | <span data-ttu-id="89ff8-263">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-263">no</span></span>               |
| <span data-ttu-id="89ff8-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="89ff8-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="89ff8-265">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-265">no</span></span>             | <span data-ttu-id="89ff8-266">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-266">no</span></span>               |
| <span data-ttu-id="89ff8-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="89ff8-267">msdyn_progress</span></span>                         | <span data-ttu-id="89ff8-268">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-268">no</span></span>             | <span data-ttu-id="89ff8-269">tidak (ya untuk P4W)</span><span class="sxs-lookup"><span data-stu-id="89ff8-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="89ff8-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="89ff8-271">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-271">no</span></span>             | <span data-ttu-id="89ff8-272">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-272">no</span></span>               |
| <span data-ttu-id="89ff8-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="89ff8-274">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-274">no</span></span>             | <span data-ttu-id="89ff8-275">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-275">no</span></span>               |
| <span data-ttu-id="89ff8-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="89ff8-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="89ff8-277">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-277">no</span></span>             | <span data-ttu-id="89ff8-278">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-278">no</span></span>               |
| <span data-ttu-id="89ff8-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="89ff8-280">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-280">no</span></span>             | <span data-ttu-id="89ff8-281">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-281">no</span></span>               |
| <span data-ttu-id="89ff8-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="89ff8-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="89ff8-283">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-283">no</span></span>             | <span data-ttu-id="89ff8-284">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-284">no</span></span>               |
| <span data-ttu-id="89ff8-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="89ff8-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="89ff8-286">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-286">no</span></span>             | <span data-ttu-id="89ff8-287">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-287">no</span></span>               |
| <span data-ttu-id="89ff8-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="89ff8-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="89ff8-289">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-289">no</span></span>             | <span data-ttu-id="89ff8-290">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-290">no</span></span>               |
| <span data-ttu-id="89ff8-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="89ff8-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="89ff8-292">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-292">no</span></span>             | <span data-ttu-id="89ff8-293">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-293">no</span></span>               |
| <span data-ttu-id="89ff8-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="89ff8-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="89ff8-295">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-295">no</span></span>             | <span data-ttu-id="89ff8-296">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-296">no</span></span>               |
| <span data-ttu-id="89ff8-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="89ff8-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="89ff8-298">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-298">no</span></span>             | <span data-ttu-id="89ff8-299">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-299">no</span></span>               |
| <span data-ttu-id="89ff8-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="89ff8-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="89ff8-301">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-301">no</span></span>             | <span data-ttu-id="89ff8-302">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-302">no</span></span>               |
| <span data-ttu-id="89ff8-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="89ff8-304">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-304">no</span></span>             | <span data-ttu-id="89ff8-305">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-305">no</span></span>               |
| <span data-ttu-id="89ff8-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="89ff8-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="89ff8-307">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-307">no</span></span>             | <span data-ttu-id="89ff8-308">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-308">no</span></span>               |
| <span data-ttu-id="89ff8-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="89ff8-310">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-310">no</span></span>             | <span data-ttu-id="89ff8-311">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-311">no</span></span>               |
| <span data-ttu-id="89ff8-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="89ff8-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="89ff8-313">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-313">no</span></span>             | <span data-ttu-id="89ff8-314">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-314">no</span></span>               |
| <span data-ttu-id="89ff8-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="89ff8-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="89ff8-316">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-316">no</span></span>             | <span data-ttu-id="89ff8-317">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-317">no</span></span>               |
| <span data-ttu-id="89ff8-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="89ff8-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="89ff8-319">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-319">no</span></span>             | <span data-ttu-id="89ff8-320">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-320">no</span></span>               |
| <span data-ttu-id="89ff8-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="89ff8-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="89ff8-322">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-322">no</span></span>             | <span data-ttu-id="89ff8-323">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-323">no</span></span>               |
| <span data-ttu-id="89ff8-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="89ff8-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="89ff8-325">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-325">no</span></span>             | <span data-ttu-id="89ff8-326">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-326">no</span></span>               |
| <span data-ttu-id="89ff8-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="89ff8-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="89ff8-328">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-328">no</span></span>             | <span data-ttu-id="89ff8-329">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-329">no</span></span>               |
| <span data-ttu-id="89ff8-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="89ff8-330">msdyn_summary</span></span>                          | <span data-ttu-id="89ff8-331">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-331">no</span></span>             | <span data-ttu-id="89ff8-332">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-332">no</span></span>               |
| <span data-ttu-id="89ff8-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="89ff8-334">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-334">no</span></span>             | <span data-ttu-id="89ff8-335">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-335">no</span></span>               |
| <span data-ttu-id="89ff8-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="89ff8-337">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-337">no</span></span>             | <span data-ttu-id="89ff8-338">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="89ff8-339">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-339">Project task dependency</span></span>

| <span data-ttu-id="89ff8-340">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="89ff8-340">**Logical name**</span></span>              | <span data-ttu-id="89ff8-341">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="89ff8-341">**Can create**</span></span> | <span data-ttu-id="89ff8-342">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="89ff8-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="89ff8-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="89ff8-343">msdyn_linktype</span></span>                | <span data-ttu-id="89ff8-344">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-344">no</span></span>             | <span data-ttu-id="89ff8-345">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-345">no</span></span>           |
| <span data-ttu-id="89ff8-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="89ff8-346">msdyn_linktypename</span></span>            | <span data-ttu-id="89ff8-347">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-347">no</span></span>             | <span data-ttu-id="89ff8-348">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-348">no</span></span>           |
| <span data-ttu-id="89ff8-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="89ff8-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="89ff8-350">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-350">yes</span></span>            | <span data-ttu-id="89ff8-351">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-351">no</span></span>           |
| <span data-ttu-id="89ff8-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="89ff8-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="89ff8-353">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-353">yes</span></span>            | <span data-ttu-id="89ff8-354">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-354">no</span></span>           |
| <span data-ttu-id="89ff8-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="89ff8-355">msdyn_project</span></span>                 | <span data-ttu-id="89ff8-356">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-356">yes</span></span>            | <span data-ttu-id="89ff8-357">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-357">no</span></span>           |
| <span data-ttu-id="89ff8-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="89ff8-358">msdyn_projectname</span></span>             | <span data-ttu-id="89ff8-359">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-359">yes</span></span>            | <span data-ttu-id="89ff8-360">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-360">no</span></span>           |
| <span data-ttu-id="89ff8-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="89ff8-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="89ff8-362">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-362">yes</span></span>            | <span data-ttu-id="89ff8-363">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-363">no</span></span>           |
| <span data-ttu-id="89ff8-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="89ff8-364">msdyn_successortask</span></span>           | <span data-ttu-id="89ff8-365">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-365">yes</span></span>            | <span data-ttu-id="89ff8-366">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-366">no</span></span>           |
| <span data-ttu-id="89ff8-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="89ff8-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="89ff8-368">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-368">yes</span></span>            | <span data-ttu-id="89ff8-369">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="89ff8-370">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="89ff8-370">Resource assignment</span></span>

| <span data-ttu-id="89ff8-371">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="89ff8-371">**Logical name**</span></span>             | <span data-ttu-id="89ff8-372">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="89ff8-372">**Can create**</span></span> | <span data-ttu-id="89ff8-373">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="89ff8-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="89ff8-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="89ff8-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="89ff8-375">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-375">yes</span></span>            | <span data-ttu-id="89ff8-376">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-376">no</span></span>           |
| <span data-ttu-id="89ff8-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="89ff8-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="89ff8-378">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-378">yes</span></span>            | <span data-ttu-id="89ff8-379">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-379">no</span></span>           |
| <span data-ttu-id="89ff8-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="89ff8-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="89ff8-381">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-381">no</span></span>             | <span data-ttu-id="89ff8-382">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-382">no</span></span>           |
| <span data-ttu-id="89ff8-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="89ff8-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="89ff8-384">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-384">no</span></span>             | <span data-ttu-id="89ff8-385">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-385">no</span></span>           |
| <span data-ttu-id="89ff8-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="89ff8-386">msdyn_committype</span></span>             | <span data-ttu-id="89ff8-387">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-387">no</span></span>             | <span data-ttu-id="89ff8-388">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-388">no</span></span>           |
| <span data-ttu-id="89ff8-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="89ff8-389">msdyn_committypename</span></span>         | <span data-ttu-id="89ff8-390">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-390">no</span></span>             | <span data-ttu-id="89ff8-391">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-391">no</span></span>           |
| <span data-ttu-id="89ff8-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="89ff8-392">msdyn_effort</span></span>                 | <span data-ttu-id="89ff8-393">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-393">no</span></span>             | <span data-ttu-id="89ff8-394">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-394">no</span></span>           |
| <span data-ttu-id="89ff8-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="89ff8-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="89ff8-396">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-396">no</span></span>             | <span data-ttu-id="89ff8-397">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-397">no</span></span>           |
| <span data-ttu-id="89ff8-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="89ff8-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="89ff8-399">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-399">no</span></span>             | <span data-ttu-id="89ff8-400">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-400">no</span></span>           |
| <span data-ttu-id="89ff8-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="89ff8-401">msdyn_finish</span></span>                 | <span data-ttu-id="89ff8-402">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-402">no</span></span>             | <span data-ttu-id="89ff8-403">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-403">no</span></span>           |
| <span data-ttu-id="89ff8-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="89ff8-405">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-405">no</span></span>             | <span data-ttu-id="89ff8-406">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-406">no</span></span>           |
| <span data-ttu-id="89ff8-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="89ff8-408">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-408">no</span></span>             | <span data-ttu-id="89ff8-409">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-409">no</span></span>           |
| <span data-ttu-id="89ff8-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="89ff8-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="89ff8-411">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-411">no</span></span>             | <span data-ttu-id="89ff8-412">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-412">no</span></span>           |
| <span data-ttu-id="89ff8-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="89ff8-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="89ff8-414">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-414">no</span></span>             | <span data-ttu-id="89ff8-415">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-415">no</span></span>           |
| <span data-ttu-id="89ff8-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="89ff8-417">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-417">no</span></span>             | <span data-ttu-id="89ff8-418">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-418">no</span></span>           |
| <span data-ttu-id="89ff8-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="89ff8-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="89ff8-420">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-420">no</span></span>             | <span data-ttu-id="89ff8-421">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-421">no</span></span>           |
| <span data-ttu-id="89ff8-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="89ff8-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="89ff8-423">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-423">no</span></span>             | <span data-ttu-id="89ff8-424">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-424">no</span></span>           |
| <span data-ttu-id="89ff8-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="89ff8-425">msdyn_projectid</span></span>              | <span data-ttu-id="89ff8-426">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-426">yes</span></span>            | <span data-ttu-id="89ff8-427">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-427">no</span></span>           |
| <span data-ttu-id="89ff8-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="89ff8-428">msdyn_projectidname</span></span>          | <span data-ttu-id="89ff8-429">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-429">no</span></span>             | <span data-ttu-id="89ff8-430">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-430">no</span></span>           |
| <span data-ttu-id="89ff8-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="89ff8-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="89ff8-432">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-432">no</span></span>             | <span data-ttu-id="89ff8-433">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-433">no</span></span>           |
| <span data-ttu-id="89ff8-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="89ff8-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="89ff8-435">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-435">no</span></span>             | <span data-ttu-id="89ff8-436">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-436">no</span></span>           |
| <span data-ttu-id="89ff8-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="89ff8-437">msdyn_start</span></span>                  | <span data-ttu-id="89ff8-438">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-438">no</span></span>             | <span data-ttu-id="89ff8-439">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-439">no</span></span>           |
| <span data-ttu-id="89ff8-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="89ff8-440">msdyn_taskid</span></span>                 | <span data-ttu-id="89ff8-441">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-441">no</span></span>             | <span data-ttu-id="89ff8-442">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-442">no</span></span>           |
| <span data-ttu-id="89ff8-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="89ff8-443">msdyn_taskidname</span></span>             | <span data-ttu-id="89ff8-444">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-444">no</span></span>             | <span data-ttu-id="89ff8-445">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-445">no</span></span>           |
| <span data-ttu-id="89ff8-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="89ff8-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="89ff8-447">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-447">no</span></span>             | <span data-ttu-id="89ff8-448">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="89ff8-449">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="89ff8-449">Project team member</span></span>

| <span data-ttu-id="89ff8-450">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="89ff8-450">**Logical name**</span></span>                                 | <span data-ttu-id="89ff8-451">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="89ff8-451">**Can create**</span></span> | <span data-ttu-id="89ff8-452">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="89ff8-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="89ff8-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="89ff8-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="89ff8-454">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-454">no</span></span>             | <span data-ttu-id="89ff8-455">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-455">no</span></span>           |
| <span data-ttu-id="89ff8-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="89ff8-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="89ff8-457">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-457">no</span></span>             | <span data-ttu-id="89ff8-458">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-458">no</span></span>           |
| <span data-ttu-id="89ff8-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="89ff8-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="89ff8-460">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-460">no</span></span>             | <span data-ttu-id="89ff8-461">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-461">no</span></span>           |
| <span data-ttu-id="89ff8-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="89ff8-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="89ff8-463">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-463">no</span></span>             | <span data-ttu-id="89ff8-464">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-464">no</span></span>           |
| <span data-ttu-id="89ff8-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="89ff8-465">msdyn_effort</span></span>                                     | <span data-ttu-id="89ff8-466">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-466">no</span></span>             | <span data-ttu-id="89ff8-467">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-467">no</span></span>           |
| <span data-ttu-id="89ff8-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="89ff8-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="89ff8-469">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-469">no</span></span>             | <span data-ttu-id="89ff8-470">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-470">no</span></span>           |
| <span data-ttu-id="89ff8-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="89ff8-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="89ff8-472">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-472">no</span></span>             | <span data-ttu-id="89ff8-473">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-473">no</span></span>           |
| <span data-ttu-id="89ff8-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="89ff8-474">msdyn_finish</span></span>                                     | <span data-ttu-id="89ff8-475">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-475">no</span></span>             | <span data-ttu-id="89ff8-476">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-476">no</span></span>           |
| <span data-ttu-id="89ff8-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="89ff8-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="89ff8-478">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-478">no</span></span>             | <span data-ttu-id="89ff8-479">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-479">no</span></span>           |
| <span data-ttu-id="89ff8-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="89ff8-480">msdyn_hours</span></span>                                      | <span data-ttu-id="89ff8-481">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-481">no</span></span>             | <span data-ttu-id="89ff8-482">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-482">no</span></span>           |
| <span data-ttu-id="89ff8-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="89ff8-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="89ff8-484">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-484">no</span></span>             | <span data-ttu-id="89ff8-485">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-485">no</span></span>           |
| <span data-ttu-id="89ff8-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="89ff8-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="89ff8-487">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-487">no</span></span>             | <span data-ttu-id="89ff8-488">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-488">no</span></span>           |
| <span data-ttu-id="89ff8-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="89ff8-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="89ff8-490">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-490">no</span></span>             | <span data-ttu-id="89ff8-491">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-491">no</span></span>           |
| <span data-ttu-id="89ff8-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="89ff8-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="89ff8-493">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-493">no</span></span>             | <span data-ttu-id="89ff8-494">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-494">no</span></span>           |
| <span data-ttu-id="89ff8-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="89ff8-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="89ff8-496">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-496">no</span></span>             | <span data-ttu-id="89ff8-497">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-497">no</span></span>           |
| <span data-ttu-id="89ff8-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="89ff8-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="89ff8-499">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-499">no</span></span>             | <span data-ttu-id="89ff8-500">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-500">no</span></span>           |
| <span data-ttu-id="89ff8-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="89ff8-501">msdyn_start</span></span>                                      | <span data-ttu-id="89ff8-502">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-502">no</span></span>             | <span data-ttu-id="89ff8-503">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="89ff8-504">Project</span><span class="sxs-lookup"><span data-stu-id="89ff8-504">Project</span></span>

| <span data-ttu-id="89ff8-505">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="89ff8-505">**Logical name**</span></span>                       | <span data-ttu-id="89ff8-506">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="89ff8-506">**Can create**</span></span> | <span data-ttu-id="89ff8-507">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="89ff8-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="89ff8-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="89ff8-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="89ff8-509">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-509">no</span></span>             | <span data-ttu-id="89ff8-510">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-510">no</span></span>           |
| <span data-ttu-id="89ff8-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="89ff8-512">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-512">no</span></span>             | <span data-ttu-id="89ff8-513">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-513">no</span></span>           |
| <span data-ttu-id="89ff8-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="89ff8-515">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-515">no</span></span>             | <span data-ttu-id="89ff8-516">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-516">no</span></span>           |
| <span data-ttu-id="89ff8-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="89ff8-518">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-518">no</span></span>             | <span data-ttu-id="89ff8-519">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-519">no</span></span>           |
| <span data-ttu-id="89ff8-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="89ff8-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="89ff8-521">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-521">no</span></span>             | <span data-ttu-id="89ff8-522">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-522">no</span></span>           |
| <span data-ttu-id="89ff8-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="89ff8-524">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-524">no</span></span>             | <span data-ttu-id="89ff8-525">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-525">no</span></span>           |
| <span data-ttu-id="89ff8-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="89ff8-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="89ff8-527">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-527">yes</span></span>            | <span data-ttu-id="89ff8-528">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-528">no</span></span>           |
| <span data-ttu-id="89ff8-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="89ff8-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="89ff8-530">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-530">yes</span></span>            | <span data-ttu-id="89ff8-531">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-531">no</span></span>           |
| <span data-ttu-id="89ff8-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="89ff8-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="89ff8-533">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-533">yes</span></span>            | <span data-ttu-id="89ff8-534">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-534">no</span></span>           |
| <span data-ttu-id="89ff8-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="89ff8-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="89ff8-536">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-536">no</span></span>             | <span data-ttu-id="89ff8-537">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-537">no</span></span>           |
| <span data-ttu-id="89ff8-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="89ff8-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="89ff8-539">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-539">no</span></span>             | <span data-ttu-id="89ff8-540">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-540">no</span></span>           |
| <span data-ttu-id="89ff8-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="89ff8-542">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-542">no</span></span>             | <span data-ttu-id="89ff8-543">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-543">no</span></span>           |
| <span data-ttu-id="89ff8-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="89ff8-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="89ff8-545">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-545">no</span></span>             | <span data-ttu-id="89ff8-546">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-546">no</span></span>           |
| <span data-ttu-id="89ff8-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="89ff8-548">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-548">no</span></span>             | <span data-ttu-id="89ff8-549">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-549">no</span></span>           |
| <span data-ttu-id="89ff8-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="89ff8-550">msdyn_duration</span></span>                         | <span data-ttu-id="89ff8-551">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-551">no</span></span>             | <span data-ttu-id="89ff8-552">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-552">no</span></span>           |
| <span data-ttu-id="89ff8-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="89ff8-553">msdyn_effort</span></span>                           | <span data-ttu-id="89ff8-554">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-554">no</span></span>             | <span data-ttu-id="89ff8-555">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-555">no</span></span>           |
| <span data-ttu-id="89ff8-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="89ff8-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="89ff8-557">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-557">no</span></span>             | <span data-ttu-id="89ff8-558">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-558">no</span></span>           |
| <span data-ttu-id="89ff8-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="89ff8-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="89ff8-560">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-560">no</span></span>             | <span data-ttu-id="89ff8-561">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-561">no</span></span>           |
| <span data-ttu-id="89ff8-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="89ff8-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="89ff8-563">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-563">no</span></span>             | <span data-ttu-id="89ff8-564">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-564">no</span></span>           |
| <span data-ttu-id="89ff8-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="89ff8-565">msdyn_finish</span></span>                           | <span data-ttu-id="89ff8-566">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-566">yes</span></span>            | <span data-ttu-id="89ff8-567">ya</span><span class="sxs-lookup"><span data-stu-id="89ff8-567">yes</span></span>          |
| <span data-ttu-id="89ff8-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="89ff8-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="89ff8-569">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-569">no</span></span>             | <span data-ttu-id="89ff8-570">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-570">no</span></span>           |
| <span data-ttu-id="89ff8-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="89ff8-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="89ff8-572">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-572">no</span></span>             | <span data-ttu-id="89ff8-573">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-573">no</span></span>           |
| <span data-ttu-id="89ff8-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="89ff8-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="89ff8-575">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-575">no</span></span>             | <span data-ttu-id="89ff8-576">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-576">no</span></span>           |
| <span data-ttu-id="89ff8-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="89ff8-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="89ff8-578">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-578">no</span></span>             | <span data-ttu-id="89ff8-579">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-579">no</span></span>           |
| <span data-ttu-id="89ff8-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="89ff8-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="89ff8-581">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-581">no</span></span>             | <span data-ttu-id="89ff8-582">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-582">no</span></span>           |
| <span data-ttu-id="89ff8-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="89ff8-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="89ff8-584">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-584">no</span></span>             | <span data-ttu-id="89ff8-585">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-585">no</span></span>           |
| <span data-ttu-id="89ff8-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="89ff8-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="89ff8-587">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-587">no</span></span>             | <span data-ttu-id="89ff8-588">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-588">no</span></span>           |
| <span data-ttu-id="89ff8-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="89ff8-590">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-590">no</span></span>             | <span data-ttu-id="89ff8-591">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-591">no</span></span>           |
| <span data-ttu-id="89ff8-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="89ff8-593">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-593">no</span></span>             | <span data-ttu-id="89ff8-594">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-594">no</span></span>           |
| <span data-ttu-id="89ff8-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="89ff8-596">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-596">no</span></span>             | <span data-ttu-id="89ff8-597">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-597">no</span></span>           |
| <span data-ttu-id="89ff8-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="89ff8-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="89ff8-599">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-599">no</span></span>             | <span data-ttu-id="89ff8-600">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-600">no</span></span>           |
| <span data-ttu-id="89ff8-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="89ff8-602">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-602">no</span></span>             | <span data-ttu-id="89ff8-603">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-603">no</span></span>           |
| <span data-ttu-id="89ff8-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="89ff8-604">msdyn_progress</span></span>                         | <span data-ttu-id="89ff8-605">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-605">no</span></span>             | <span data-ttu-id="89ff8-606">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-606">no</span></span>           |
| <span data-ttu-id="89ff8-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="89ff8-608">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-608">no</span></span>             | <span data-ttu-id="89ff8-609">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-609">no</span></span>           |
| <span data-ttu-id="89ff8-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="89ff8-611">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-611">no</span></span>             | <span data-ttu-id="89ff8-612">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-612">no</span></span>           |
| <span data-ttu-id="89ff8-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="89ff8-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="89ff8-614">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-614">no</span></span>             | <span data-ttu-id="89ff8-615">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-615">no</span></span>           |
| <span data-ttu-id="89ff8-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="89ff8-617">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-617">no</span></span>             | <span data-ttu-id="89ff8-618">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-618">no</span></span>           |
| <span data-ttu-id="89ff8-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="89ff8-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="89ff8-620">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-620">no</span></span>             | <span data-ttu-id="89ff8-621">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-621">no</span></span>           |
| <span data-ttu-id="89ff8-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="89ff8-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="89ff8-623">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-623">no</span></span>             | <span data-ttu-id="89ff8-624">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-624">no</span></span>           |
| <span data-ttu-id="89ff8-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="89ff8-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="89ff8-626">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-626">no</span></span>             | <span data-ttu-id="89ff8-627">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-627">no</span></span>           |
| <span data-ttu-id="89ff8-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="89ff8-629">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-629">no</span></span>             | <span data-ttu-id="89ff8-630">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-630">no</span></span>           |
| <span data-ttu-id="89ff8-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="89ff8-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="89ff8-632">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-632">no</span></span>             | <span data-ttu-id="89ff8-633">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-633">no</span></span>           |
| <span data-ttu-id="89ff8-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="89ff8-635">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-635">no</span></span>             | <span data-ttu-id="89ff8-636">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-636">no</span></span>           |
| <span data-ttu-id="89ff8-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="89ff8-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="89ff8-638">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-638">no</span></span>             | <span data-ttu-id="89ff8-639">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-639">no</span></span>           |
| <span data-ttu-id="89ff8-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="89ff8-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="89ff8-641">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-641">no</span></span>             | <span data-ttu-id="89ff8-642">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-642">no</span></span>           |
| <span data-ttu-id="89ff8-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="89ff8-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="89ff8-644">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-644">no</span></span>             | <span data-ttu-id="89ff8-645">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-645">no</span></span>           |
| <span data-ttu-id="89ff8-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="89ff8-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="89ff8-647">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-647">no</span></span>             | <span data-ttu-id="89ff8-648">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-648">no</span></span>           |
| <span data-ttu-id="89ff8-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="89ff8-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="89ff8-650">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-650">no</span></span>             | <span data-ttu-id="89ff8-651">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-651">no</span></span>           |
| <span data-ttu-id="89ff8-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="89ff8-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="89ff8-653">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-653">no</span></span>             | <span data-ttu-id="89ff8-654">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-654">no</span></span>           |
| <span data-ttu-id="89ff8-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="89ff8-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="89ff8-656">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-656">no</span></span>             | <span data-ttu-id="89ff8-657">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-657">no</span></span>           |
| <span data-ttu-id="89ff8-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="89ff8-659">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-659">no</span></span>             | <span data-ttu-id="89ff8-660">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-660">no</span></span>           |
| <span data-ttu-id="89ff8-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="89ff8-662">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-662">no</span></span>             | <span data-ttu-id="89ff8-663">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-663">no</span></span>           |
| <span data-ttu-id="89ff8-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="89ff8-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="89ff8-665">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-665">no</span></span>             | <span data-ttu-id="89ff8-666">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-666">no</span></span>           |
| <span data-ttu-id="89ff8-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="89ff8-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="89ff8-668">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-668">no</span></span>             | <span data-ttu-id="89ff8-669">tidak</span><span class="sxs-lookup"><span data-stu-id="89ff8-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="89ff8-670">Masalah dan batasan yang diketahui</span><span class="sxs-lookup"><span data-stu-id="89ff8-670">Limitations and known issues</span></span>
<span data-ttu-id="89ff8-671">Berikut adalah daftar batasan dan masalah umum:</span><span class="sxs-lookup"><span data-stu-id="89ff8-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="89ff8-672">API jadwal hanya dapat digunakan oleh **Pengguna dengan Lisensi Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="89ff8-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="89ff8-673">Tidak dapat digunakan oleh:</span><span class="sxs-lookup"><span data-stu-id="89ff8-673">They can't be used by:</span></span>
    - <span data-ttu-id="89ff8-674">Pengguna Aplikasi</span><span class="sxs-lookup"><span data-stu-id="89ff8-674">Application users</span></span>
    - <span data-ttu-id="89ff8-675">Pengguna Sistem</span><span class="sxs-lookup"><span data-stu-id="89ff8-675">System users</span></span>
    - <span data-ttu-id="89ff8-676">Pengguna Integrasi</span><span class="sxs-lookup"><span data-stu-id="89ff8-676">Integration users</span></span>
    - <span data-ttu-id="89ff8-677">Pengguna lain yang tidak memiliki lisensi yang diperlukan</span><span class="sxs-lookup"><span data-stu-id="89ff8-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="89ff8-678">Setiap **OperationSet** hanya dapat memiliki maksimum 100 operasi.</span><span class="sxs-lookup"><span data-stu-id="89ff8-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="89ff8-679">Setiap pengguna hanya dapat membuka maksimum 10 **OperationSet** terbuka.</span><span class="sxs-lookup"><span data-stu-id="89ff8-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="89ff8-680">Project Operations saat ini mendukung maksimum 500 tugas total pada proyek.</span><span class="sxs-lookup"><span data-stu-id="89ff8-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="89ff8-681">Status kegagalan dan log kegagalan **OperationSet** saat ini tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="89ff8-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="89ff8-682">API Jadwal ada dalam pratinjau umum.</span><span class="sxs-lookup"><span data-stu-id="89ff8-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="89ff8-683">Menggunakan API ini di lingkungan Produksi tidak didukung oleh Microsoft.</span><span class="sxs-lookup"><span data-stu-id="89ff8-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="89ff8-684">Batas dan batasan pada proyek dan tugas</span><span class="sxs-lookup"><span data-stu-id="89ff8-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="89ff8-685">Penanganan kesalahan</span><span class="sxs-lookup"><span data-stu-id="89ff8-685">Error handling</span></span>

   - <span data-ttu-id="89ff8-686">Untuk memeriksa kesalahan yang dihasilkan dari Rangkaian Operasi, buka **Pengaturan** \> **Integrasi Jadwal** \> **Rangkaian Operasi**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="89ff8-687">Untuk memeriksa kesalahan yang dihasilkan dari Layanan Penjadwalan Proyek, buka **Pengaturan** \> **Integrasi Jadwal** \> **Log Kesalahan PSS**.</span><span class="sxs-lookup"><span data-stu-id="89ff8-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="89ff8-688">Contoh Skenario</span><span class="sxs-lookup"><span data-stu-id="89ff8-688">Sample scenario</span></span>

<span data-ttu-id="89ff8-689">Dalam skenario ini, Anda akan membuat proyek, anggota tim, empat tugas, dan dua penugasan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="89ff8-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="89ff8-690">Selanjutnya, Anda akan memperbarui satu tugas, memperbarui proyek, menghapus satu tugas, menghapus satu penetapan sumber daya, dan membuat dependensi tugas.</span><span class="sxs-lookup"><span data-stu-id="89ff8-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
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
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="89ff8-691">Contoh tambahan</span><span class="sxs-lookup"><span data-stu-id="89ff8-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
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
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
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
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
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
/// </summary>
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="operationSetId">operationSet id</param>
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
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
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
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
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
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```

---
title: Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan
description: Topik ini memberikan informasi dan sampel untuk menggunakan API jadwal proyek.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293231"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="188ed-103">Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="188ed-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="188ed-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="188ed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="188ed-105">Beberapa atau semua fungsi yang tercantum dalam topik ini tersedia sebagai bagian dari rilis pratinjau.</span><span class="sxs-lookup"><span data-stu-id="188ed-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="188ed-106">Konten dan fungsi ini dapat berubah.</span><span class="sxs-lookup"><span data-stu-id="188ed-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="188ed-107">Entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="188ed-107">Scheduling entities</span></span>

<span data-ttu-id="188ed-108">API jadwal proyek memberikan kemampuan untuk melakukan operasi pembuatan, pembaruan, dan penghapusan dengan **entitas Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="188ed-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="188ed-109">Entitas ini dikelola melalui mesin Penjadwalan di Project for the Web.</span><span class="sxs-lookup"><span data-stu-id="188ed-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="188ed-110">Membuat, memperbarui, dan menghapus operasi dengan **entitas Penjadwalan** dibatasi di rilis Dynamics 365 Project Operations sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="188ed-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="188ed-111">Tabel berikut menyediakan daftar lengkap entitas jadwal Proyek.</span><span class="sxs-lookup"><span data-stu-id="188ed-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="188ed-112">Nama entitas</span><span class="sxs-lookup"><span data-stu-id="188ed-112">Entity name</span></span>  | <span data-ttu-id="188ed-113">Nama logika entitas</span><span class="sxs-lookup"><span data-stu-id="188ed-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="188ed-114">Project</span><span class="sxs-lookup"><span data-stu-id="188ed-114">Project</span></span> | <span data-ttu-id="188ed-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="188ed-115">msdyn_project</span></span> |
| <span data-ttu-id="188ed-116">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-116">Project Task</span></span>  | <span data-ttu-id="188ed-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="188ed-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="188ed-118">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-118">Project Task Dependency</span></span>  | <span data-ttu-id="188ed-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="188ed-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="188ed-120">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="188ed-120">Resource Assignment</span></span> | <span data-ttu-id="188ed-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="188ed-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="188ed-122">Wadah Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-122">Project Bucket</span></span>  | <span data-ttu-id="188ed-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="188ed-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="188ed-124">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-124">Project Team Member</span></span> | <span data-ttu-id="188ed-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="188ed-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="188ed-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="188ed-126">OperationSet</span></span>

<span data-ttu-id="188ed-127">OperationSet adalah pola unit kerja yang dapat digunakan ketika beberapa jadwal yang mempengaruhi permintaan harus diproses dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="188ed-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="188ed-128">API Jadwal proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-128">Project schedule APIs</span></span>

<span data-ttu-id="188ed-129">Berikut adalah daftar API jadwal Proyek saat ini.</span><span class="sxs-lookup"><span data-stu-id="188ed-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="188ed-130">**msdyn_CreateProjectV1**: API ini dapat digunakan untuk membuat proyek.</span><span class="sxs-lookup"><span data-stu-id="188ed-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="188ed-131">Proyek dan wadah proyek default dibuat dengan segera.</span><span class="sxs-lookup"><span data-stu-id="188ed-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="188ed-132">**msdyn_CreateTeamMemberV1**: API ini dapat digunakan untuk membuat anggota tim proyek.</span><span class="sxs-lookup"><span data-stu-id="188ed-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="188ed-133">Rekaman anggota tim akan segera dibuat.</span><span class="sxs-lookup"><span data-stu-id="188ed-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="188ed-134">**msdyn_CreateOperationSetV1**: API ini dapat digunakan untuk menjadwalkan beberapa permintaan yang harus dilakukan dalam transaksi.</span><span class="sxs-lookup"><span data-stu-id="188ed-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="188ed-135">**msdyn_PSSCreateV1**: API ini dapat digunakan untuk membuat entitas.</span><span class="sxs-lookup"><span data-stu-id="188ed-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="188ed-136">Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi pembuatan.</span><span class="sxs-lookup"><span data-stu-id="188ed-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="188ed-137">**msdyn_PSSUpdateV1**: API ini dapat digunakan untuk memperbarui entitas.</span><span class="sxs-lookup"><span data-stu-id="188ed-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="188ed-138">Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi pembaruan.</span><span class="sxs-lookup"><span data-stu-id="188ed-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="188ed-139">**msdyn_PSSDeleteV1**: API ini dapat digunakan untuk menghapus entitas.</span><span class="sxs-lookup"><span data-stu-id="188ed-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="188ed-140">Entitas dapat merupakan entitas penjadwalan Proyek yang mendukung operasi penghapusan.</span><span class="sxs-lookup"><span data-stu-id="188ed-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="188ed-141">**msdyn_ExecuteOperationSetV1**: API ini digunakan untuk mengeksekusi semua operasi dalam rangkaian operasi yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="188ed-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="188ed-142">Menggunakan API jadwal proyek dengan OperationSet</span><span class="sxs-lookup"><span data-stu-id="188ed-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="188ed-143">Karena rekaman dengan **CreateProjectV1** dan **CreateTeamMemberV1** dibuat dengan segera, API ini tidak dapat digunakan di **OperationSet** secara langsung.</span><span class="sxs-lookup"><span data-stu-id="188ed-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="188ed-144">Namun, Anda dapat menggunakan API untuk membuat rekaman yang diperlukan, membuat **OperationSet**, dan kemudian menggunakan rekaman yang dibuat sebelumnya di **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="188ed-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="188ed-145">Operasi yang Didukung</span><span class="sxs-lookup"><span data-stu-id="188ed-145">Supported operations</span></span>

| <span data-ttu-id="188ed-146">Entitas Penjadwalan</span><span class="sxs-lookup"><span data-stu-id="188ed-146">Scheduling entity</span></span> | <span data-ttu-id="188ed-147">Buat</span><span class="sxs-lookup"><span data-stu-id="188ed-147">Create</span></span> | <span data-ttu-id="188ed-148">Pembaruan</span><span class="sxs-lookup"><span data-stu-id="188ed-148">Update</span></span> | <span data-ttu-id="188ed-149">Delete</span><span class="sxs-lookup"><span data-stu-id="188ed-149">Delete</span></span> | <span data-ttu-id="188ed-150">Pertimbangan penting</span><span class="sxs-lookup"><span data-stu-id="188ed-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="188ed-151">Tugas proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-151">Project task</span></span> | <span data-ttu-id="188ed-152">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-152">Yes</span></span> | <span data-ttu-id="188ed-153">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-153">Yes</span></span> | <span data-ttu-id="188ed-154">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-154">Yes</span></span> | <span data-ttu-id="188ed-155">Tidak Ada</span><span class="sxs-lookup"><span data-stu-id="188ed-155">None</span></span> |
| <span data-ttu-id="188ed-156">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-156">Project task dependency</span></span> | <span data-ttu-id="188ed-157">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-157">Yes</span></span> | <span data-ttu-id="188ed-158">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-158">Yes</span></span> | | <span data-ttu-id="188ed-159">Rekaman dependensi tugas proyek tidak diperbarui.</span><span class="sxs-lookup"><span data-stu-id="188ed-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="188ed-160">Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat.</span><span class="sxs-lookup"><span data-stu-id="188ed-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="188ed-161">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="188ed-161">Resource assignment</span></span> | <span data-ttu-id="188ed-162">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-162">Yes</span></span> | <span data-ttu-id="188ed-163">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-163">Yes</span></span> | | <span data-ttu-id="188ed-164">Operasi dengan bidang berikut tidak didukung: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, dan **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="188ed-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="188ed-165">Rekaman penetapan sumber daya tidak diperbarui.</span><span class="sxs-lookup"><span data-stu-id="188ed-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="188ed-166">Sebagai gantinya, rekaman lama dapat dihapus dan rekaman baru dapat dibuat.</span><span class="sxs-lookup"><span data-stu-id="188ed-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="188ed-167">Wadah Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-167">Project bucket</span></span> | <span data-ttu-id="188ed-168">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="188ed-168">N/A</span></span> | <span data-ttu-id="188ed-169">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="188ed-169">N/A</span></span> | <span data-ttu-id="188ed-170">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="188ed-170">N/A</span></span> | <span data-ttu-id="188ed-171">Seeer default dibuat menggunakan API **CREATEKainyV1**.</span><span class="sxs-lookup"><span data-stu-id="188ed-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="188ed-172">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-172">Project team member</span></span> | <span data-ttu-id="188ed-173">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-173">Yes</span></span> | <span data-ttu-id="188ed-174">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-174">Yes</span></span> | <span data-ttu-id="188ed-175">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-175">Yes</span></span> | <span data-ttu-id="188ed-176">Untuk operasi pembuatan, gunakan API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="188ed-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="188ed-177">Project</span><span class="sxs-lookup"><span data-stu-id="188ed-177">Project</span></span> | <span data-ttu-id="188ed-178">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-178">Yes</span></span> | <span data-ttu-id="188ed-179">Ya</span><span class="sxs-lookup"><span data-stu-id="188ed-179">Yes</span></span> | <span data-ttu-id="188ed-180">Tidak Tersedia</span><span class="sxs-lookup"><span data-stu-id="188ed-180">N/A</span></span> | <span data-ttu-id="188ed-181">Operasi dengan bidang berikut tidak didukung: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, dan **Duration**.</span><span class="sxs-lookup"><span data-stu-id="188ed-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="188ed-182">API ini dapat dipanggil dengan objek entitas yang mencakup bidang kustom.</span><span class="sxs-lookup"><span data-stu-id="188ed-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="188ed-183">Properti ID bersifat opsional.</span><span class="sxs-lookup"><span data-stu-id="188ed-183">The ID property is optional.</span></span> <span data-ttu-id="188ed-184">Jika diberikan, sistem mencoba menggunakannya dan memberikan pengecualian jika tidak dapat digunakan.</span><span class="sxs-lookup"><span data-stu-id="188ed-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="188ed-185">Jika tidak disediakan, sistem akan membuatnya.</span><span class="sxs-lookup"><span data-stu-id="188ed-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="188ed-186">Bidang dibatasi</span><span class="sxs-lookup"><span data-stu-id="188ed-186">Restricted fields</span></span>

<span data-ttu-id="188ed-187">Tabel berikut menentukan bidang yang dibatasi dari **Buat** dan **Edit**.</span><span class="sxs-lookup"><span data-stu-id="188ed-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="188ed-188">Tugas proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-188">Project task</span></span>

| <span data-ttu-id="188ed-189">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="188ed-189">**Logical name**</span></span>                       | <span data-ttu-id="188ed-190">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="188ed-190">**Can create**</span></span> | <span data-ttu-id="188ed-191">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="188ed-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="188ed-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="188ed-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="188ed-193">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-193">no</span></span>             | <span data-ttu-id="188ed-194">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-194">no</span></span>               |
| <span data-ttu-id="188ed-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="188ed-196">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-196">no</span></span>             | <span data-ttu-id="188ed-197">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-197">no</span></span>               |
| <span data-ttu-id="188ed-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="188ed-198">msdyn_actualend</span></span>                        | <span data-ttu-id="188ed-199">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-199">no</span></span>             | <span data-ttu-id="188ed-200">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-200">no</span></span>               |
| <span data-ttu-id="188ed-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="188ed-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="188ed-202">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-202">no</span></span>             | <span data-ttu-id="188ed-203">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-203">no</span></span>               |
| <span data-ttu-id="188ed-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="188ed-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="188ed-205">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-205">no</span></span>             | <span data-ttu-id="188ed-206">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-206">no</span></span>               |
| <span data-ttu-id="188ed-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="188ed-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="188ed-208">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-208">no</span></span>             | <span data-ttu-id="188ed-209">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-209">no</span></span>               |
| <span data-ttu-id="188ed-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="188ed-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="188ed-211">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-211">no</span></span>             | <span data-ttu-id="188ed-212">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-212">no</span></span>               |
| <span data-ttu-id="188ed-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="188ed-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="188ed-214">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-214">no</span></span>             | <span data-ttu-id="188ed-215">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-215">no</span></span>               |
| <span data-ttu-id="188ed-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="188ed-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="188ed-217">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-217">no</span></span>             | <span data-ttu-id="188ed-218">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-218">no</span></span>               |
| <span data-ttu-id="188ed-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="188ed-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="188ed-220">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-220">no</span></span>             | <span data-ttu-id="188ed-221">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-221">no</span></span>               |
| <span data-ttu-id="188ed-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="188ed-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="188ed-223">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-223">no</span></span>             | <span data-ttu-id="188ed-224">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-224">no</span></span>               |
| <span data-ttu-id="188ed-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="188ed-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="188ed-226">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-226">no</span></span>             | <span data-ttu-id="188ed-227">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-227">no</span></span>               |
| <span data-ttu-id="188ed-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="188ed-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="188ed-229">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-229">no</span></span>             | <span data-ttu-id="188ed-230">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-230">no</span></span>               |
| <span data-ttu-id="188ed-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="188ed-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="188ed-232">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-232">no</span></span>             | <span data-ttu-id="188ed-233">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-233">no</span></span>               |
| <span data-ttu-id="188ed-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="188ed-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="188ed-235">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-235">no</span></span>             | <span data-ttu-id="188ed-236">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-236">no</span></span>               |
| <span data-ttu-id="188ed-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="188ed-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="188ed-238">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-238">no</span></span>             | <span data-ttu-id="188ed-239">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-239">no</span></span>               |
| <span data-ttu-id="188ed-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="188ed-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="188ed-241">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-241">no</span></span>             | <span data-ttu-id="188ed-242">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-242">no</span></span>               |
| <span data-ttu-id="188ed-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="188ed-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="188ed-244">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-244">no</span></span>             | <span data-ttu-id="188ed-245">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-245">no</span></span>               |
| <span data-ttu-id="188ed-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="188ed-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="188ed-247">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-247">no</span></span>             | <span data-ttu-id="188ed-248">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-248">no</span></span>               |
| <span data-ttu-id="188ed-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="188ed-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="188ed-250">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-250">no</span></span>             | <span data-ttu-id="188ed-251">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-251">no</span></span>               |
| <span data-ttu-id="188ed-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="188ed-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="188ed-253">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-253">no</span></span>             | <span data-ttu-id="188ed-254">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-254">no</span></span>               |
| <span data-ttu-id="188ed-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="188ed-256">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-256">no</span></span>             | <span data-ttu-id="188ed-257">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-257">no</span></span>               |
| <span data-ttu-id="188ed-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="188ed-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="188ed-259">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-259">no</span></span>             | <span data-ttu-id="188ed-260">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-260">no</span></span>               |
| <span data-ttu-id="188ed-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="188ed-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="188ed-262">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-262">no</span></span>             | <span data-ttu-id="188ed-263">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-263">no</span></span>               |
| <span data-ttu-id="188ed-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="188ed-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="188ed-265">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-265">no</span></span>             | <span data-ttu-id="188ed-266">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-266">no</span></span>               |
| <span data-ttu-id="188ed-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="188ed-267">msdyn_progress</span></span>                         | <span data-ttu-id="188ed-268">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-268">no</span></span>             | <span data-ttu-id="188ed-269">tidak (ya untuk P4W)</span><span class="sxs-lookup"><span data-stu-id="188ed-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="188ed-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="188ed-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="188ed-271">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-271">no</span></span>             | <span data-ttu-id="188ed-272">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-272">no</span></span>               |
| <span data-ttu-id="188ed-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="188ed-274">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-274">no</span></span>             | <span data-ttu-id="188ed-275">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-275">no</span></span>               |
| <span data-ttu-id="188ed-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="188ed-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="188ed-277">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-277">no</span></span>             | <span data-ttu-id="188ed-278">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-278">no</span></span>               |
| <span data-ttu-id="188ed-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="188ed-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="188ed-280">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-280">no</span></span>             | <span data-ttu-id="188ed-281">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-281">no</span></span>               |
| <span data-ttu-id="188ed-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="188ed-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="188ed-283">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-283">no</span></span>             | <span data-ttu-id="188ed-284">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-284">no</span></span>               |
| <span data-ttu-id="188ed-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="188ed-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="188ed-286">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-286">no</span></span>             | <span data-ttu-id="188ed-287">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-287">no</span></span>               |
| <span data-ttu-id="188ed-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="188ed-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="188ed-289">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-289">no</span></span>             | <span data-ttu-id="188ed-290">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-290">no</span></span>               |
| <span data-ttu-id="188ed-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="188ed-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="188ed-292">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-292">no</span></span>             | <span data-ttu-id="188ed-293">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-293">no</span></span>               |
| <span data-ttu-id="188ed-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="188ed-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="188ed-295">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-295">no</span></span>             | <span data-ttu-id="188ed-296">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-296">no</span></span>               |
| <span data-ttu-id="188ed-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="188ed-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="188ed-298">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-298">no</span></span>             | <span data-ttu-id="188ed-299">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-299">no</span></span>               |
| <span data-ttu-id="188ed-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="188ed-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="188ed-301">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-301">no</span></span>             | <span data-ttu-id="188ed-302">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-302">no</span></span>               |
| <span data-ttu-id="188ed-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="188ed-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="188ed-304">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-304">no</span></span>             | <span data-ttu-id="188ed-305">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-305">no</span></span>               |
| <span data-ttu-id="188ed-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="188ed-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="188ed-307">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-307">no</span></span>             | <span data-ttu-id="188ed-308">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-308">no</span></span>               |
| <span data-ttu-id="188ed-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="188ed-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="188ed-310">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-310">no</span></span>             | <span data-ttu-id="188ed-311">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-311">no</span></span>               |
| <span data-ttu-id="188ed-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="188ed-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="188ed-313">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-313">no</span></span>             | <span data-ttu-id="188ed-314">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-314">no</span></span>               |
| <span data-ttu-id="188ed-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="188ed-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="188ed-316">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-316">no</span></span>             | <span data-ttu-id="188ed-317">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-317">no</span></span>               |
| <span data-ttu-id="188ed-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="188ed-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="188ed-319">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-319">no</span></span>             | <span data-ttu-id="188ed-320">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-320">no</span></span>               |
| <span data-ttu-id="188ed-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="188ed-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="188ed-322">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-322">no</span></span>             | <span data-ttu-id="188ed-323">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-323">no</span></span>               |
| <span data-ttu-id="188ed-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="188ed-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="188ed-325">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-325">no</span></span>             | <span data-ttu-id="188ed-326">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-326">no</span></span>               |
| <span data-ttu-id="188ed-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="188ed-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="188ed-328">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-328">no</span></span>             | <span data-ttu-id="188ed-329">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-329">no</span></span>               |
| <span data-ttu-id="188ed-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="188ed-330">msdyn_summary</span></span>                          | <span data-ttu-id="188ed-331">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-331">no</span></span>             | <span data-ttu-id="188ed-332">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-332">no</span></span>               |
| <span data-ttu-id="188ed-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="188ed-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="188ed-334">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-334">no</span></span>             | <span data-ttu-id="188ed-335">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-335">no</span></span>               |
| <span data-ttu-id="188ed-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="188ed-337">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-337">no</span></span>             | <span data-ttu-id="188ed-338">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="188ed-339">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-339">Project task dependency</span></span>

| <span data-ttu-id="188ed-340">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="188ed-340">**Logical name**</span></span>              | <span data-ttu-id="188ed-341">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="188ed-341">**Can create**</span></span> | <span data-ttu-id="188ed-342">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="188ed-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="188ed-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="188ed-343">msdyn_linktype</span></span>                | <span data-ttu-id="188ed-344">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-344">no</span></span>             | <span data-ttu-id="188ed-345">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-345">no</span></span>           |
| <span data-ttu-id="188ed-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="188ed-346">msdyn_linktypename</span></span>            | <span data-ttu-id="188ed-347">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-347">no</span></span>             | <span data-ttu-id="188ed-348">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-348">no</span></span>           |
| <span data-ttu-id="188ed-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="188ed-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="188ed-350">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-350">yes</span></span>            | <span data-ttu-id="188ed-351">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-351">no</span></span>           |
| <span data-ttu-id="188ed-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="188ed-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="188ed-353">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-353">yes</span></span>            | <span data-ttu-id="188ed-354">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-354">no</span></span>           |
| <span data-ttu-id="188ed-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="188ed-355">msdyn_project</span></span>                 | <span data-ttu-id="188ed-356">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-356">yes</span></span>            | <span data-ttu-id="188ed-357">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-357">no</span></span>           |
| <span data-ttu-id="188ed-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="188ed-358">msdyn_projectname</span></span>             | <span data-ttu-id="188ed-359">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-359">yes</span></span>            | <span data-ttu-id="188ed-360">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-360">no</span></span>           |
| <span data-ttu-id="188ed-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="188ed-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="188ed-362">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-362">yes</span></span>            | <span data-ttu-id="188ed-363">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-363">no</span></span>           |
| <span data-ttu-id="188ed-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="188ed-364">msdyn_successortask</span></span>           | <span data-ttu-id="188ed-365">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-365">yes</span></span>            | <span data-ttu-id="188ed-366">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-366">no</span></span>           |
| <span data-ttu-id="188ed-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="188ed-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="188ed-368">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-368">yes</span></span>            | <span data-ttu-id="188ed-369">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="188ed-370">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="188ed-370">Resource assignment</span></span>

| <span data-ttu-id="188ed-371">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="188ed-371">**Logical name**</span></span>             | <span data-ttu-id="188ed-372">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="188ed-372">**Can create**</span></span> | <span data-ttu-id="188ed-373">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="188ed-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="188ed-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="188ed-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="188ed-375">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-375">yes</span></span>            | <span data-ttu-id="188ed-376">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-376">no</span></span>           |
| <span data-ttu-id="188ed-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="188ed-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="188ed-378">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-378">yes</span></span>            | <span data-ttu-id="188ed-379">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-379">no</span></span>           |
| <span data-ttu-id="188ed-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="188ed-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="188ed-381">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-381">no</span></span>             | <span data-ttu-id="188ed-382">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-382">no</span></span>           |
| <span data-ttu-id="188ed-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="188ed-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="188ed-384">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-384">no</span></span>             | <span data-ttu-id="188ed-385">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-385">no</span></span>           |
| <span data-ttu-id="188ed-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="188ed-386">msdyn_committype</span></span>             | <span data-ttu-id="188ed-387">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-387">no</span></span>             | <span data-ttu-id="188ed-388">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-388">no</span></span>           |
| <span data-ttu-id="188ed-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="188ed-389">msdyn_committypename</span></span>         | <span data-ttu-id="188ed-390">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-390">no</span></span>             | <span data-ttu-id="188ed-391">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-391">no</span></span>           |
| <span data-ttu-id="188ed-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="188ed-392">msdyn_effort</span></span>                 | <span data-ttu-id="188ed-393">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-393">no</span></span>             | <span data-ttu-id="188ed-394">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-394">no</span></span>           |
| <span data-ttu-id="188ed-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="188ed-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="188ed-396">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-396">no</span></span>             | <span data-ttu-id="188ed-397">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-397">no</span></span>           |
| <span data-ttu-id="188ed-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="188ed-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="188ed-399">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-399">no</span></span>             | <span data-ttu-id="188ed-400">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-400">no</span></span>           |
| <span data-ttu-id="188ed-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="188ed-401">msdyn_finish</span></span>                 | <span data-ttu-id="188ed-402">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-402">no</span></span>             | <span data-ttu-id="188ed-403">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-403">no</span></span>           |
| <span data-ttu-id="188ed-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="188ed-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="188ed-405">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-405">no</span></span>             | <span data-ttu-id="188ed-406">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-406">no</span></span>           |
| <span data-ttu-id="188ed-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="188ed-408">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-408">no</span></span>             | <span data-ttu-id="188ed-409">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-409">no</span></span>           |
| <span data-ttu-id="188ed-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="188ed-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="188ed-411">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-411">no</span></span>             | <span data-ttu-id="188ed-412">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-412">no</span></span>           |
| <span data-ttu-id="188ed-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="188ed-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="188ed-414">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-414">no</span></span>             | <span data-ttu-id="188ed-415">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-415">no</span></span>           |
| <span data-ttu-id="188ed-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="188ed-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="188ed-417">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-417">no</span></span>             | <span data-ttu-id="188ed-418">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-418">no</span></span>           |
| <span data-ttu-id="188ed-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="188ed-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="188ed-420">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-420">no</span></span>             | <span data-ttu-id="188ed-421">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-421">no</span></span>           |
| <span data-ttu-id="188ed-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="188ed-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="188ed-423">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-423">no</span></span>             | <span data-ttu-id="188ed-424">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-424">no</span></span>           |
| <span data-ttu-id="188ed-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="188ed-425">msdyn_projectid</span></span>              | <span data-ttu-id="188ed-426">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-426">yes</span></span>            | <span data-ttu-id="188ed-427">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-427">no</span></span>           |
| <span data-ttu-id="188ed-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="188ed-428">msdyn_projectidname</span></span>          | <span data-ttu-id="188ed-429">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-429">no</span></span>             | <span data-ttu-id="188ed-430">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-430">no</span></span>           |
| <span data-ttu-id="188ed-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="188ed-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="188ed-432">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-432">no</span></span>             | <span data-ttu-id="188ed-433">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-433">no</span></span>           |
| <span data-ttu-id="188ed-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="188ed-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="188ed-435">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-435">no</span></span>             | <span data-ttu-id="188ed-436">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-436">no</span></span>           |
| <span data-ttu-id="188ed-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="188ed-437">msdyn_start</span></span>                  | <span data-ttu-id="188ed-438">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-438">no</span></span>             | <span data-ttu-id="188ed-439">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-439">no</span></span>           |
| <span data-ttu-id="188ed-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="188ed-440">msdyn_taskid</span></span>                 | <span data-ttu-id="188ed-441">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-441">no</span></span>             | <span data-ttu-id="188ed-442">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-442">no</span></span>           |
| <span data-ttu-id="188ed-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="188ed-443">msdyn_taskidname</span></span>             | <span data-ttu-id="188ed-444">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-444">no</span></span>             | <span data-ttu-id="188ed-445">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-445">no</span></span>           |
| <span data-ttu-id="188ed-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="188ed-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="188ed-447">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-447">no</span></span>             | <span data-ttu-id="188ed-448">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="188ed-449">Anggota Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="188ed-449">Project team member</span></span>

| <span data-ttu-id="188ed-450">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="188ed-450">**Logical name**</span></span>                                 | <span data-ttu-id="188ed-451">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="188ed-451">**Can create**</span></span> | <span data-ttu-id="188ed-452">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="188ed-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="188ed-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="188ed-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="188ed-454">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-454">no</span></span>             | <span data-ttu-id="188ed-455">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-455">no</span></span>           |
| <span data-ttu-id="188ed-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="188ed-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="188ed-457">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-457">no</span></span>             | <span data-ttu-id="188ed-458">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-458">no</span></span>           |
| <span data-ttu-id="188ed-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="188ed-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="188ed-460">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-460">no</span></span>             | <span data-ttu-id="188ed-461">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-461">no</span></span>           |
| <span data-ttu-id="188ed-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="188ed-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="188ed-463">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-463">no</span></span>             | <span data-ttu-id="188ed-464">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-464">no</span></span>           |
| <span data-ttu-id="188ed-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="188ed-465">msdyn_effort</span></span>                                     | <span data-ttu-id="188ed-466">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-466">no</span></span>             | <span data-ttu-id="188ed-467">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-467">no</span></span>           |
| <span data-ttu-id="188ed-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="188ed-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="188ed-469">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-469">no</span></span>             | <span data-ttu-id="188ed-470">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-470">no</span></span>           |
| <span data-ttu-id="188ed-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="188ed-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="188ed-472">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-472">no</span></span>             | <span data-ttu-id="188ed-473">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-473">no</span></span>           |
| <span data-ttu-id="188ed-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="188ed-474">msdyn_finish</span></span>                                     | <span data-ttu-id="188ed-475">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-475">no</span></span>             | <span data-ttu-id="188ed-476">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-476">no</span></span>           |
| <span data-ttu-id="188ed-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="188ed-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="188ed-478">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-478">no</span></span>             | <span data-ttu-id="188ed-479">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-479">no</span></span>           |
| <span data-ttu-id="188ed-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="188ed-480">msdyn_hours</span></span>                                      | <span data-ttu-id="188ed-481">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-481">no</span></span>             | <span data-ttu-id="188ed-482">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-482">no</span></span>           |
| <span data-ttu-id="188ed-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="188ed-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="188ed-484">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-484">no</span></span>             | <span data-ttu-id="188ed-485">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-485">no</span></span>           |
| <span data-ttu-id="188ed-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="188ed-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="188ed-487">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-487">no</span></span>             | <span data-ttu-id="188ed-488">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-488">no</span></span>           |
| <span data-ttu-id="188ed-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="188ed-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="188ed-490">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-490">no</span></span>             | <span data-ttu-id="188ed-491">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-491">no</span></span>           |
| <span data-ttu-id="188ed-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="188ed-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="188ed-493">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-493">no</span></span>             | <span data-ttu-id="188ed-494">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-494">no</span></span>           |
| <span data-ttu-id="188ed-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="188ed-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="188ed-496">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-496">no</span></span>             | <span data-ttu-id="188ed-497">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-497">no</span></span>           |
| <span data-ttu-id="188ed-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="188ed-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="188ed-499">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-499">no</span></span>             | <span data-ttu-id="188ed-500">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-500">no</span></span>           |
| <span data-ttu-id="188ed-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="188ed-501">msdyn_start</span></span>                                      | <span data-ttu-id="188ed-502">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-502">no</span></span>             | <span data-ttu-id="188ed-503">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="188ed-504">Project</span><span class="sxs-lookup"><span data-stu-id="188ed-504">Project</span></span>

| <span data-ttu-id="188ed-505">**Nama logis**</span><span class="sxs-lookup"><span data-stu-id="188ed-505">**Logical name**</span></span>                       | <span data-ttu-id="188ed-506">**Dapat membuat**</span><span class="sxs-lookup"><span data-stu-id="188ed-506">**Can create**</span></span> | <span data-ttu-id="188ed-507">**Dapat mengedit**</span><span class="sxs-lookup"><span data-stu-id="188ed-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="188ed-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="188ed-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="188ed-509">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-509">no</span></span>             | <span data-ttu-id="188ed-510">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-510">no</span></span>           |
| <span data-ttu-id="188ed-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="188ed-512">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-512">no</span></span>             | <span data-ttu-id="188ed-513">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-513">no</span></span>           |
| <span data-ttu-id="188ed-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="188ed-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="188ed-515">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-515">no</span></span>             | <span data-ttu-id="188ed-516">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-516">no</span></span>           |
| <span data-ttu-id="188ed-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="188ed-518">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-518">no</span></span>             | <span data-ttu-id="188ed-519">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-519">no</span></span>           |
| <span data-ttu-id="188ed-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="188ed-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="188ed-521">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-521">no</span></span>             | <span data-ttu-id="188ed-522">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-522">no</span></span>           |
| <span data-ttu-id="188ed-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="188ed-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="188ed-524">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-524">no</span></span>             | <span data-ttu-id="188ed-525">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-525">no</span></span>           |
| <span data-ttu-id="188ed-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="188ed-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="188ed-527">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-527">yes</span></span>            | <span data-ttu-id="188ed-528">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-528">no</span></span>           |
| <span data-ttu-id="188ed-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="188ed-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="188ed-530">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-530">yes</span></span>            | <span data-ttu-id="188ed-531">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-531">no</span></span>           |
| <span data-ttu-id="188ed-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="188ed-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="188ed-533">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-533">yes</span></span>            | <span data-ttu-id="188ed-534">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-534">no</span></span>           |
| <span data-ttu-id="188ed-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="188ed-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="188ed-536">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-536">no</span></span>             | <span data-ttu-id="188ed-537">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-537">no</span></span>           |
| <span data-ttu-id="188ed-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="188ed-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="188ed-539">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-539">no</span></span>             | <span data-ttu-id="188ed-540">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-540">no</span></span>           |
| <span data-ttu-id="188ed-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="188ed-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="188ed-542">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-542">no</span></span>             | <span data-ttu-id="188ed-543">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-543">no</span></span>           |
| <span data-ttu-id="188ed-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="188ed-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="188ed-545">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-545">no</span></span>             | <span data-ttu-id="188ed-546">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-546">no</span></span>           |
| <span data-ttu-id="188ed-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="188ed-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="188ed-548">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-548">no</span></span>             | <span data-ttu-id="188ed-549">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-549">no</span></span>           |
| <span data-ttu-id="188ed-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="188ed-550">msdyn_duration</span></span>                         | <span data-ttu-id="188ed-551">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-551">no</span></span>             | <span data-ttu-id="188ed-552">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-552">no</span></span>           |
| <span data-ttu-id="188ed-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="188ed-553">msdyn_effort</span></span>                           | <span data-ttu-id="188ed-554">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-554">no</span></span>             | <span data-ttu-id="188ed-555">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-555">no</span></span>           |
| <span data-ttu-id="188ed-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="188ed-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="188ed-557">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-557">no</span></span>             | <span data-ttu-id="188ed-558">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-558">no</span></span>           |
| <span data-ttu-id="188ed-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="188ed-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="188ed-560">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-560">no</span></span>             | <span data-ttu-id="188ed-561">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-561">no</span></span>           |
| <span data-ttu-id="188ed-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="188ed-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="188ed-563">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-563">no</span></span>             | <span data-ttu-id="188ed-564">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-564">no</span></span>           |
| <span data-ttu-id="188ed-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="188ed-565">msdyn_finish</span></span>                           | <span data-ttu-id="188ed-566">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-566">yes</span></span>            | <span data-ttu-id="188ed-567">ya</span><span class="sxs-lookup"><span data-stu-id="188ed-567">yes</span></span>          |
| <span data-ttu-id="188ed-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="188ed-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="188ed-569">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-569">no</span></span>             | <span data-ttu-id="188ed-570">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-570">no</span></span>           |
| <span data-ttu-id="188ed-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="188ed-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="188ed-572">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-572">no</span></span>             | <span data-ttu-id="188ed-573">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-573">no</span></span>           |
| <span data-ttu-id="188ed-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="188ed-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="188ed-575">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-575">no</span></span>             | <span data-ttu-id="188ed-576">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-576">no</span></span>           |
| <span data-ttu-id="188ed-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="188ed-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="188ed-578">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-578">no</span></span>             | <span data-ttu-id="188ed-579">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-579">no</span></span>           |
| <span data-ttu-id="188ed-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="188ed-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="188ed-581">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-581">no</span></span>             | <span data-ttu-id="188ed-582">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-582">no</span></span>           |
| <span data-ttu-id="188ed-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="188ed-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="188ed-584">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-584">no</span></span>             | <span data-ttu-id="188ed-585">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-585">no</span></span>           |
| <span data-ttu-id="188ed-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="188ed-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="188ed-587">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-587">no</span></span>             | <span data-ttu-id="188ed-588">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-588">no</span></span>           |
| <span data-ttu-id="188ed-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="188ed-590">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-590">no</span></span>             | <span data-ttu-id="188ed-591">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-591">no</span></span>           |
| <span data-ttu-id="188ed-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="188ed-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="188ed-593">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-593">no</span></span>             | <span data-ttu-id="188ed-594">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-594">no</span></span>           |
| <span data-ttu-id="188ed-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="188ed-596">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-596">no</span></span>             | <span data-ttu-id="188ed-597">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-597">no</span></span>           |
| <span data-ttu-id="188ed-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="188ed-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="188ed-599">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-599">no</span></span>             | <span data-ttu-id="188ed-600">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-600">no</span></span>           |
| <span data-ttu-id="188ed-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="188ed-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="188ed-602">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-602">no</span></span>             | <span data-ttu-id="188ed-603">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-603">no</span></span>           |
| <span data-ttu-id="188ed-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="188ed-604">msdyn_progress</span></span>                         | <span data-ttu-id="188ed-605">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-605">no</span></span>             | <span data-ttu-id="188ed-606">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-606">no</span></span>           |
| <span data-ttu-id="188ed-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="188ed-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="188ed-608">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-608">no</span></span>             | <span data-ttu-id="188ed-609">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-609">no</span></span>           |
| <span data-ttu-id="188ed-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="188ed-611">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-611">no</span></span>             | <span data-ttu-id="188ed-612">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-612">no</span></span>           |
| <span data-ttu-id="188ed-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="188ed-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="188ed-614">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-614">no</span></span>             | <span data-ttu-id="188ed-615">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-615">no</span></span>           |
| <span data-ttu-id="188ed-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="188ed-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="188ed-617">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-617">no</span></span>             | <span data-ttu-id="188ed-618">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-618">no</span></span>           |
| <span data-ttu-id="188ed-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="188ed-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="188ed-620">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-620">no</span></span>             | <span data-ttu-id="188ed-621">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-621">no</span></span>           |
| <span data-ttu-id="188ed-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="188ed-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="188ed-623">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-623">no</span></span>             | <span data-ttu-id="188ed-624">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-624">no</span></span>           |
| <span data-ttu-id="188ed-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="188ed-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="188ed-626">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-626">no</span></span>             | <span data-ttu-id="188ed-627">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-627">no</span></span>           |
| <span data-ttu-id="188ed-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="188ed-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="188ed-629">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-629">no</span></span>             | <span data-ttu-id="188ed-630">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-630">no</span></span>           |
| <span data-ttu-id="188ed-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="188ed-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="188ed-632">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-632">no</span></span>             | <span data-ttu-id="188ed-633">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-633">no</span></span>           |
| <span data-ttu-id="188ed-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="188ed-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="188ed-635">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-635">no</span></span>             | <span data-ttu-id="188ed-636">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-636">no</span></span>           |
| <span data-ttu-id="188ed-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="188ed-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="188ed-638">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-638">no</span></span>             | <span data-ttu-id="188ed-639">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-639">no</span></span>           |
| <span data-ttu-id="188ed-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="188ed-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="188ed-641">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-641">no</span></span>             | <span data-ttu-id="188ed-642">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-642">no</span></span>           |
| <span data-ttu-id="188ed-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="188ed-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="188ed-644">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-644">no</span></span>             | <span data-ttu-id="188ed-645">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-645">no</span></span>           |
| <span data-ttu-id="188ed-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="188ed-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="188ed-647">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-647">no</span></span>             | <span data-ttu-id="188ed-648">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-648">no</span></span>           |
| <span data-ttu-id="188ed-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="188ed-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="188ed-650">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-650">no</span></span>             | <span data-ttu-id="188ed-651">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-651">no</span></span>           |
| <span data-ttu-id="188ed-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="188ed-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="188ed-653">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-653">no</span></span>             | <span data-ttu-id="188ed-654">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-654">no</span></span>           |
| <span data-ttu-id="188ed-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="188ed-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="188ed-656">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-656">no</span></span>             | <span data-ttu-id="188ed-657">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-657">no</span></span>           |
| <span data-ttu-id="188ed-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="188ed-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="188ed-659">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-659">no</span></span>             | <span data-ttu-id="188ed-660">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-660">no</span></span>           |
| <span data-ttu-id="188ed-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="188ed-662">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-662">no</span></span>             | <span data-ttu-id="188ed-663">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-663">no</span></span>           |
| <span data-ttu-id="188ed-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="188ed-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="188ed-665">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-665">no</span></span>             | <span data-ttu-id="188ed-666">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-666">no</span></span>           |
| <span data-ttu-id="188ed-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="188ed-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="188ed-668">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-668">no</span></span>             | <span data-ttu-id="188ed-669">tidak</span><span class="sxs-lookup"><span data-stu-id="188ed-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="188ed-670">Masalah dan batasan yang diketahui</span><span class="sxs-lookup"><span data-stu-id="188ed-670">Limitations and known issues</span></span>
<span data-ttu-id="188ed-671">Berikut adalah daftar batasan dan masalah umum:</span><span class="sxs-lookup"><span data-stu-id="188ed-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="188ed-672">API Jadwal Proyek hanya dapat digunakan oleh **Pengguna dengan Lisensi Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="188ed-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="188ed-673">Tidak dapat digunakan oleh:</span><span class="sxs-lookup"><span data-stu-id="188ed-673">They can't be used by:</span></span>
    - <span data-ttu-id="188ed-674">Pengguna Aplikasi</span><span class="sxs-lookup"><span data-stu-id="188ed-674">Application users</span></span>
    - <span data-ttu-id="188ed-675">Pengguna Sistem</span><span class="sxs-lookup"><span data-stu-id="188ed-675">System users</span></span>
    - <span data-ttu-id="188ed-676">Pengguna Integrasi</span><span class="sxs-lookup"><span data-stu-id="188ed-676">Integration users</span></span>
    - <span data-ttu-id="188ed-677">Pengguna lain yang tidak memiliki lisensi yang diperlukan</span><span class="sxs-lookup"><span data-stu-id="188ed-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="188ed-678">Setiap **OperationSet** hanya dapat memiliki maksimum 100 operasi.</span><span class="sxs-lookup"><span data-stu-id="188ed-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="188ed-679">Setiap pengguna hanya dapat membuka maksimum 10 **OperationSet** terbuka.</span><span class="sxs-lookup"><span data-stu-id="188ed-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="188ed-680">Project Operations saat ini mendukung maksimum 500 tugas total pada proyek.</span><span class="sxs-lookup"><span data-stu-id="188ed-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="188ed-681">Status kegagalan dan log kegagalan **OperationSet** saat ini tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="188ed-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="188ed-682">Batas dan batasan pada proyek dan tugas</span><span class="sxs-lookup"><span data-stu-id="188ed-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="188ed-683">Penanganan kesalahan</span><span class="sxs-lookup"><span data-stu-id="188ed-683">Error handling</span></span>

   - <span data-ttu-id="188ed-684">Untuk memeriksa kesalahan yang dihasilkan dari Rangkaian Operasi, buka **Pengaturan** \> **Integrasi Jadwal** \> **Rangkaian Operasi**.</span><span class="sxs-lookup"><span data-stu-id="188ed-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="188ed-685">Untuk memeriksa kesalahan yang dihasilkan dari Layanan Jadwal Proyek, buka **pengaturan** \> **integrasi Jadwal** \> **Log Kesalahan PSS**.</span><span class="sxs-lookup"><span data-stu-id="188ed-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="188ed-686">Contoh Skenario</span><span class="sxs-lookup"><span data-stu-id="188ed-686">Sample scenario</span></span>

<span data-ttu-id="188ed-687">Dalam skenario ini, Anda akan membuat proyek, anggota tim, empat tugas, dan dua penugasan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="188ed-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="188ed-688">Selanjutnya, Anda akan memperbarui satu tugas, memperbarui proyek, menghapus satu tugas, menghapus satu penetapan sumber daya, dan membuat dependensi tugas.</span><span class="sxs-lookup"><span data-stu-id="188ed-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="188ed-689">Contoh tambahan</span><span class="sxs-lookup"><span data-stu-id="188ed-689">Additional samples</span></span>

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

---
title: Pertimbangan peningkatan untuk struktur rincian kerja
description: Topik ini menyediakan informasi tentang cara meningkatkan struktur rincian kerja dari Project Service Automation 2.x hingga 3.x.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: 169dc24f0d1ae151ea5927123fb738221de88250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078566"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="b5ccd-103">Pertimbangan peningkatan untuk struktur rincian kerja</span><span class="sxs-lookup"><span data-stu-id="b5ccd-103">Upgrade considerations for the work breakdown structure</span></span>
<span data-ttu-id="b5ccd-104">Topik ini menyediakan informasi tentang cara meningkatkan struktur rincian kerja dari Project Service Automation 2.x hingga 3.x.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="b5ccd-105">Topik ini menentukan status sehat proyek di project Service Automation (PSA) yang diperlukan untuk peningkatan yang berhasil.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="b5ccd-106">Ada juga informasi tentang kondisi pemblokiran umum yang akan menyebabkan peningkatan gagal.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="b5ccd-107">Untuk informasi lebih lanjut tentang mendefinisikan tugas proyek dan fungsinya dalam jadwal proyek, lihat [jadwal proyek](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="b5ccd-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="b5ccd-108">Entitas utama</span><span class="sxs-lookup"><span data-stu-id="b5ccd-108">Key entities</span></span>
<span data-ttu-id="b5ccd-109">Untuk struktur rincian kerja yang akurat yang telah dimuat dengan sumber daya, entitas berikut diperlukan:</span><span class="sxs-lookup"><span data-stu-id="b5ccd-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="b5ccd-110">Proyek</span><span class="sxs-lookup"><span data-stu-id="b5ccd-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="b5ccd-111">Tim Proyek</span><span class="sxs-lookup"><span data-stu-id="b5ccd-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="b5ccd-112">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="b5ccd-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="b5ccd-113">Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="b5ccd-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="b5ccd-114">Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="b5ccd-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="b5ccd-115">Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="b5ccd-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="b5ccd-116">Untuk menentukan struktur rincian kerja yang dimuat sumber daya, Anda harus menyelesaikan langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="b5ccd-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="b5ccd-117">Buat proyek baru.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-117">Create a new project.</span></span> <span data-ttu-id="b5ccd-118">Untuk informasi lebih lanjut tentang cara membuat proyek baru, lihat [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="b5ccd-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="b5ccd-119">Buat satu atau beberapa tugas.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-119">Create one or more tasks.</span></span> <span data-ttu-id="b5ccd-120">Untuk informasi lebih lanjut tentang cara membuat tugas baru, lihat [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="b5ccd-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="b5ccd-121">Tentukan dependensi tugas.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-121">Define the task dependencies.</span></span> <span data-ttu-id="b5ccd-122">Untuk informasi lebih lanjut, Lihat [ketergantungan tugas proyek](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="b5ccd-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="b5ccd-123">Tetapkan anggota tim proyek ke proyek.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-123">Assign project team members to the project.</span></span> <span data-ttu-id="b5ccd-124">Untuk informasi selengkapnya, lihat [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="b5ccd-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="b5ccd-125">Tetapkan anggota tim proyek ke tugas.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="b5ccd-126">Untuk informasi selengkapnya, lihat [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="b5ccd-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="b5ccd-127">Relasi tim proyek</span><span class="sxs-lookup"><span data-stu-id="b5ccd-127">Project team relationships</span></span>

<span data-ttu-id="b5ccd-128">Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:</span><span class="sxs-lookup"><span data-stu-id="b5ccd-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="b5ccd-129">Semua anggota tim proyek harus dikaitkan dengan sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="b5ccd-130">Semua anggota tim proyek harus dikaitkan dengan proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="b5ccd-131">Relasi tugas proyek</span><span class="sxs-lookup"><span data-stu-id="b5ccd-131">Project task relationships</span></span>
<span data-ttu-id="b5ccd-132">Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:</span><span class="sxs-lookup"><span data-stu-id="b5ccd-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="b5ccd-133">Tugas terkait harus dikaitkan dengan proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="b5ccd-134">Setiap tugas baris harus memiliki tugas induk.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="b5ccd-135">Setiap tugas harus memiliki proyek induk.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="b5ccd-136">Tambah valid</span><span class="sxs-lookup"><span data-stu-id="b5ccd-136">Valid conditions</span></span>

- <span data-ttu-id="b5ccd-137">Semua durasi tugas harus lebih dari atau sama dengan (> =) satu jam dan kurang dari 1.800.000 menit (1.250 hari). \*</span><span class="sxs-lookup"><span data-stu-id="b5ccd-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="b5ccd-138">Semua tugas harus memiliki tanggal mulai tidak lebih dari 01/01/2000. \*</span><span class="sxs-lookup"><span data-stu-id="b5ccd-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="b5ccd-139">Semua tugas harus memiliki tanggal mulai selambat-lambatnya 17 tahun dari hari ini. \*</span><span class="sxs-lookup"><span data-stu-id="b5ccd-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="b5ccd-140">Semua tugas harus memiliki tanggal mulai sebelumnya atau sama dengan tanggal selesai.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="b5ccd-141">Semua jenis transaksi pada klasifikasi (pengeluaran, material, pajak, dan waktu) harus memiliki nilai untuk **unit default** dan **grup unit**.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="b5ccd-142">Format tanggal dengan huruf harus dihindari.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="b5ccd-143">Langkah-langkah mitigasi potensial</span><span class="sxs-lookup"><span data-stu-id="b5ccd-143">Potential mitigation steps</span></span>
- <span data-ttu-id="b5ccd-144">Gunakan pencarian tingkat lanjut untuk mengidentifikasi tugas proyek yang tidak berisi ID proyek.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="b5ccd-145">Gunakan pencarian tingkat lanjut untuk mengidentifikasi tugas proyek dengan durasi yang dijadwalkan lebih besar dari > 1.800.000.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="b5ccd-146">Sebelum membuat perubahan data apa pun, Anda harus menyelidiki penyesuaian apa pun yang terkait dengan entitas yang mungkin menyebabkan data menjadi status buruk.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="b5ccd-147">Penyesuaian ini harus ditangani sebelum melanjutkan dengan pembaruan terkait data.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="b5ccd-148">Untuk tugas yang teridentifikasi yang tidak memiliki keterkaitan, pertimbangkan untuk menghapus tugas ini jika tidak diperlukan atau jika mereka harus dikaitkan dengan proyek induk yang benar.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="b5ccd-149">Untuk tugas yang durasinya lebih dari 1.250 hari, pertimbangkan untuk menambahkan beberapa tugas untuk menunjukkan total durasi, jika memungkinkan.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="b5ccd-150">Item yang diperhatikan dengan tanda bintang (\*) memiliki batas yang disebabkan oleh fakta bahwa manajemen hubungan pelanggan (CRM) hanya mendukung perluasan pengulangan 7.320.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="b5ccd-151">Anda harus tetap berada di bawah batas ini.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="b5ccd-152">Relasi Penetapan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="b5ccd-152">Resource Assignment relationships</span></span>
<span data-ttu-id="b5ccd-153">Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:</span><span class="sxs-lookup"><span data-stu-id="b5ccd-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="b5ccd-154">Semua tugas sumber daya dalam struktur rincian kerja harus terkait dengan proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="b5ccd-155">Semua tugas sumber daya dalam struktur rincian kerja harus terkait dengan anggota tim proyek dalam proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="b5ccd-156">Langkah-langkah mitigasi potensial</span><span class="sxs-lookup"><span data-stu-id="b5ccd-156">Potential mitigation steps</span></span>
- <span data-ttu-id="b5ccd-157">Identifikasi semua tugas yang berada di luar kondisi yang dijelaskan di atas.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="b5ccd-158">Tugas sumber daya yang tidak lagi valid harus dihapus.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="b5ccd-159">Relasi Dependensi Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="b5ccd-159">Project task dependency relationships</span></span>
<span data-ttu-id="b5ccd-160">Untuk memastikan keberhasilan peningkatan, Relasi berikut harus dipelihara dengan benar:</span><span class="sxs-lookup"><span data-stu-id="b5ccd-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="b5ccd-161">Semua dependensi tugas proyek harus terkait dengan proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="b5ccd-162">Tugas tidak dapat memiliki dependensi yang sama yang dirujuk lebih dari satu kali.</span><span class="sxs-lookup"><span data-stu-id="b5ccd-162">A task can't have the same dependency referenced more than once.</span></span>

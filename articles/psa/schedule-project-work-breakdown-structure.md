---
title: Jadwalkan proyek dengan struktur rincian kerja
description: Cara menjadwalkan proyek dengan struktur rincian kerja di Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: cf12cc3bcf061e1daffafb248cfd76809c6444ec
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149817"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="b4406-103">Jadwalkan proyek dengan struktur rincian kerja (Project Service)</span><span class="sxs-lookup"><span data-stu-id="b4406-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="b4406-104">Jadwal proyek mengomunikasikan apa pekerjaan yang perlu dilakukan, sumber daya yang akan melakukan pekerjaan, dan jangka waktu di mana pekerjaan perlu diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="b4406-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="b4406-105">Jadwal proyek mencerminkan semua pekerjaan yang berkaitan dengan penyampaian proyek tepat waktu.</span><span class="sxs-lookup"><span data-stu-id="b4406-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="b4406-106">Salah satu langkah pertama dalam fase inisiasi proyek adalah untuk menghasilkan jadwal proyek.</span><span class="sxs-lookup"><span data-stu-id="b4406-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="b4406-107">Untuk menetapkan jadwal proyek, Anda perlu membuat struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="b4406-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="b4406-108">Buat struktur proyek dengan struktur rincian kerja, yang akan membantu Anda:</span><span class="sxs-lookup"><span data-stu-id="b4406-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="b4406-109">Memecah kerja ke dalam tugas-tugas yang bisa dikelola</span><span class="sxs-lookup"><span data-stu-id="b4406-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="b4406-110">Memperkirakan waktu yang dibutuhkan untuk menyelesaikan tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="b4406-111">Mengatur ketergantungan tugas dan durasi tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="b4406-112">Menentukan peran yang diperlukan untuk menyelesaikan setiap tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="b4406-113">Jadwal proyek dalam struktur rincian kerja memiliki tampilan dan nuansa akrab, lengkap dengan diagram Gantt interaktif.</span><span class="sxs-lookup"><span data-stu-id="b4406-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="b4406-114">Buat struktur rincian kerja untuk proyek</span><span class="sxs-lookup"><span data-stu-id="b4406-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="b4406-115">Buat struktur rincian kerja untuk mewakili urutan tugas dalam sebuah proyek.</span><span class="sxs-lookup"><span data-stu-id="b4406-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="b4406-116">Struktur rincian kerja termasuk tugas-tugas, persyaratan untuk setiap tugas, dan informasi pendapatan dan biaya.</span><span class="sxs-lookup"><span data-stu-id="b4406-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="b4406-117">Dalam struktur rincian kerja Anda, Anda dapat menambahkan:</span><span class="sxs-lookup"><span data-stu-id="b4406-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="b4406-118">Urutan tugas dalam hirarki</span><span class="sxs-lookup"><span data-stu-id="b4406-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="b4406-119">Tugas-tugas lain, jika ada, yang harus diselesaikan sebelum tugas dapat dimulai</span><span class="sxs-lookup"><span data-stu-id="b4406-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="b4406-120">Tanggal mulai, tanggal berakhir, dan durasi tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="b4406-121">Jumlah jam yang dibutuhkan untuk tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="b4406-122">Segala keterampilan dan pendidikan pekerja yang diperlukan</span><span class="sxs-lookup"><span data-stu-id="b4406-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="b4406-123">Para pekerja yang diberi tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="b4406-124">Perkiraan penerimaan dan biaya</span><span class="sxs-lookup"><span data-stu-id="b4406-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="b4406-125">Jenis Tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-125">Task types</span></span>  
<span data-ttu-id="b4406-126">Anda akan menggunakan jenis tugas berikut saat membuat struktur rincian kerja Anda:</span><span class="sxs-lookup"><span data-stu-id="b4406-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="b4406-127">**Node akar proyek**.</span><span class="sxs-lookup"><span data-stu-id="b4406-127">**Project root node**</span></span> | <span data-ttu-id="b4406-128">Ringkasan tugas tingkat atas untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="b4406-128">The top-level summary task for the project.</span></span> <span data-ttu-id="b4406-129">Semua tugas-tugas proyek lain yang dibuat di bawahnya.</span><span class="sxs-lookup"><span data-stu-id="b4406-129">All other project tasks are created under it.</span></span> <span data-ttu-id="b4406-130">Nama tugas akar adalah nama proyek.</span><span class="sxs-lookup"><span data-stu-id="b4406-130">The name of the root task is the project name.</span></span> <span data-ttu-id="b4406-131">Usaha, tanggal, dan durasi dari node akar didasarkan pada nilai-nilai pada hirarki di bawahnya.</span><span class="sxs-lookup"><span data-stu-id="b4406-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="b4406-132">Anda tidak dapat mengedit properti node akar atau menghapus node akar.</span><span class="sxs-lookup"><span data-stu-id="b4406-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="b4406-133">**Ringkasan atau tugas wadah**</span><span class="sxs-lookup"><span data-stu-id="b4406-133">**Summary or container tasks**</span></span> | <span data-ttu-id="b4406-134">Ringkasan tugas adalah tugas yang memiliki sub-tugas di bawahnya.</span><span class="sxs-lookup"><span data-stu-id="b4406-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="b4406-135">Ringkasan tugas tidak memiliki usaha kerja atau biaya sendiri.</span><span class="sxs-lookup"><span data-stu-id="b4406-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="b4406-136">Usaha kerja dan biayanya adalah rollup sub tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="b4406-137">Anda dapat mengubah nama tugas ringkasan, tetapi Anda tidak dapat mengubah usaha, tanggal, atau durasi, karena mereka secara otomatis dihitung.</span><span class="sxs-lookup"><span data-stu-id="b4406-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="b4406-138">Menghapus tugas ringkasan menghapus tugas dan semua sub-tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="b4406-139">**Tugas node leaf**</span><span class="sxs-lookup"><span data-stu-id="b4406-139">**Leaf node tasks**</span></span> | <span data-ttu-id="b4406-140">Tugas node leaf merupakan karya yang paling rinci pada proyek.</span><span class="sxs-lookup"><span data-stu-id="b4406-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="b4406-141">Ini memiliki upaya perkiraan, jumlah sumber daya yang direncanakan, durasi dan tanggal akhir dan awal yang direncanakan.</span><span class="sxs-lookup"><span data-stu-id="b4406-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="b4406-142">Hierarki tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-142">Task hierarchy</span></span>  
 <span data-ttu-id="b4406-143">Anda memiliki pilihan berikut saat membuat hierarki tugas:</span><span class="sxs-lookup"><span data-stu-id="b4406-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="b4406-144">**Menambahkan tugas**.</span><span class="sxs-lookup"><span data-stu-id="b4406-144">**Add task**.</span></span>   <span data-ttu-id="b4406-145">Anda dapat menambahkan tugas pada posisi yang Anda pilih dalam hirarki tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="b4406-146">Jika Anda tidak memilih posisi, tugas baru muncul pada akhir.</span><span class="sxs-lookup"><span data-stu-id="b4406-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="b4406-147">**Indentasi tugas**.</span><span class="sxs-lookup"><span data-stu-id="b4406-147">**Indent task**.</span></span>   <span data-ttu-id="b4406-148">Indentasi tugas untuk membuat anak tugas langsung di atasnya.</span><span class="sxs-lookup"><span data-stu-id="b4406-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="b4406-149">**Outdentasi tugas**.</span><span class="sxs-lookup"><span data-stu-id="b4406-149">**Outdent task**.</span></span>   <span data-ttu-id="b4406-150">Outdentasi tugas untuk membuatnya sedemikian rupa sehingga tidak lagi menjadi sub-tugas induk yang asli.</span><span class="sxs-lookup"><span data-stu-id="b4406-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="b4406-151">**Naik dan bergerak ke bawah**.</span><span class="sxs-lookup"><span data-stu-id="b4406-151">**Move up and Move down**.</span></span>   <span data-ttu-id="b4406-152">Pindahkan tugas naik dan turun dalam hirarki tugas induknya.</span><span class="sxs-lookup"><span data-stu-id="b4406-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="b4406-153">Memindahkan tugas naik atau turun tidak berpengaruh pada upaya, biaya, tanggal, atau durasi.</span><span class="sxs-lookup"><span data-stu-id="b4406-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="b4406-154">Atribut tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-154">Task attributes</span></span>  
 <span data-ttu-id="b4406-155">Nama tugas menjelaskan pekerjaan yang perlu diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="b4406-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="b4406-156">Anda menggunakan berbagai tugas atribut untuk menggambarkan persyaratan staf dan jadwal untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="b4406-157">Atribut jadwal</span><span class="sxs-lookup"><span data-stu-id="b4406-157">Schedule attributes</span></span>

 - <span data-ttu-id="b4406-158">Tetapkan nilai-nilai untuk **jam usaha**, **jumlah sumber daya**, **tanggal mulai**, **tanggal berakhir**, dan **durasi** untuk menentukan jadwal tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="b4406-159">**Upaya** merupakan perkiraan jam yang dibutuhkan untuk menyelesaikan tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="b4406-160">**Jumlah sumber daya** merupakan perkiraan yang manajer proyek tempatkan dalam tugas untuk membantu menghasilkan jadwal sebaik mungkin.</span><span class="sxs-lookup"><span data-stu-id="b4406-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="b4406-161">**Durasi** (dalam hari) menunjukkan jumlah hari kerja yang dibutuhkan untuk menyelesaikan tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="b4406-162">Atribut staf</span><span class="sxs-lookup"><span data-stu-id="b4406-162">Staffing attributes</span></span>

 - <span data-ttu-id="b4406-163">**Peran**, **unit organisasi sumber daya**, **jumlah sumber daya**, dan **sumber daya** menjelaskan persyaratan staf untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="b4406-164">**Peran** menjelaskan jenis sumber daya yang diperlukan untuk melakukan tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="b4406-165">**Unit organisasi sumber daya** menunjukkan unit organisasi dari mana sumber daya harus diisi stafnya untuk tugas itu; ini juga berdampak pada biaya dan perkiraan penjualan tugas, karena ini diperhitungkan ketika menentukan harga penjualan unit untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="b4406-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="b4406-166">**Sumber daya** memegang sumber daya generik atau sumber daya yang bernama ketika ditemukan.</span><span class="sxs-lookup"><span data-stu-id="b4406-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="b4406-167">Dependensi tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-167">Task dependencies</span></span>  
 <span data-ttu-id="b4406-168">Anda dapat membuat hubungan pendahulu antara satu atau lebih tugas dalam struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="b4406-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="b4406-169">Anda dapat mengatur nilai satu atau lebih bidang pendahulu pada tugas-tugas untuk menunjukkan tugas-tugas yang akan bergantung padanya.</span><span class="sxs-lookup"><span data-stu-id="b4406-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="b4406-170">Bila Anda menetapkan nilai pendahulu tugas, tugas hanya dapat mulai ketika menyelesaikan semua tugas-tugas pendahulunya.</span><span class="sxs-lookup"><span data-stu-id="b4406-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="b4406-171">Mengatur ketergantungan ini pada tugas akan mengakibatkan perhitungan kembali tanggal mulai tugas yang direncanakan sebagai akhir terbaru dari semua pendahulunya.</span><span class="sxs-lookup"><span data-stu-id="b4406-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="b4406-172">Dampak terkait dengan pendahulu pada jadwal tidak dibatasi oleh modus tugas yang didefinisikan pada tugas.</span><span class="sxs-lookup"><span data-stu-id="b4406-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="b4406-173">Modus tugas</span><span class="sxs-lookup"><span data-stu-id="b4406-173">Task mode</span></span>  
 <span data-ttu-id="b4406-174">Mode tugas adalah salah satu faktor penting yang menentukan penjadwalan tugas node leaf.</span><span class="sxs-lookup"><span data-stu-id="b4406-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="b4406-175">Ada dua mode tugas untuk setiap tugas: modus penjadwalan otomatis dan modus manual penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="b4406-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="b4406-176">**Penjadwalan Otomatis**.</span><span class="sxs-lookup"><span data-stu-id="b4406-176">**Auto scheduling**.</span></span>   <span data-ttu-id="b4406-177">Ketika Anda mengatur modus tugas untuk secara otomatis dijadwalkan, mesin penjadwalan tugas menggunakan aturan penjadwalan pada atribut tugas berikut untuk menentukan jadwal tugas:</span><span class="sxs-lookup"><span data-stu-id="b4406-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="b4406-178">Pendahulu</span><span class="sxs-lookup"><span data-stu-id="b4406-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="b4406-179">Upaya</span><span class="sxs-lookup"><span data-stu-id="b4406-179">Effort</span></span>  
  
    -   <span data-ttu-id="b4406-180">Jumlah sumber daya</span><span class="sxs-lookup"><span data-stu-id="b4406-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="b4406-181">Tanggal Mulai dan Berakhir</span><span class="sxs-lookup"><span data-stu-id="b4406-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="b4406-182">**Aturan Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="b4406-182">**Scheduling rules**.</span></span>   <span data-ttu-id="b4406-183">Tanggal mulai tugas node leaf yang tidak memiliki default pendahulu untuk tanggal mulai penjadwalan proyek.</span><span class="sxs-lookup"><span data-stu-id="b4406-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="b4406-184">Masa tugas node leaf selalu dihitung sebagai jumlah hari kerja antara tanggal yang awal dan akhir.</span><span class="sxs-lookup"><span data-stu-id="b4406-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="b4406-185">Ketika tugas dijadwalkan secara otomatis, Mesin penjadwalan mengikuti aturan di bawah ini:</span><span class="sxs-lookup"><span data-stu-id="b4406-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="b4406-186">Tanggal mulai dan akhir dari tugas yang harus selalu hari kerja menurut kalender penjadwalan proyek</span><span class="sxs-lookup"><span data-stu-id="b4406-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="b4406-187">Tanggal mulai tugas yang pendahulunya memiliki default tanggal akhir terbaru dari pendahulunya</span><span class="sxs-lookup"><span data-stu-id="b4406-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="b4406-188">Upaya = jumlah orang \* durasi \* jam dalam satu hari kerja standar kalendar proyek</span><span class="sxs-lookup"><span data-stu-id="b4406-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="b4406-189">**Penjadwalan manual**.</span><span class="sxs-lookup"><span data-stu-id="b4406-189">**Manual scheduling**.</span></span>   <span data-ttu-id="b4406-190">Dalam beberapa kasus, Anda mungkin ingin menyimpang dari aturan-aturan ini.</span><span class="sxs-lookup"><span data-stu-id="b4406-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="b4406-191">Dalam kasus ini, Anda dapat mengatur modus tugas untuk tugas untuk secara manual dijadwalkan.</span><span class="sxs-lookup"><span data-stu-id="b4406-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="b4406-192">Ini menghentikan mesin penjadwalan menghitung nilai untuk atribut penjadwalan lainnya.</span><span class="sxs-lookup"><span data-stu-id="b4406-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="b4406-193">Mengatur pendahulu pada tugas-tugas selalu berdampak pada tanggal mulai tugas yang tergantung.</span><span class="sxs-lookup"><span data-stu-id="b4406-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="b4406-194">Buat struktur rincian kerja</span><span class="sxs-lookup"><span data-stu-id="b4406-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="b4406-195">Pergi ke **Project Service > Proyek**.</span><span class="sxs-lookup"><span data-stu-id="b4406-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="b4406-196">Klik proyek yang ingin Anda kerjakan.</span><span class="sxs-lookup"><span data-stu-id="b4406-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="b4406-197">Di bar di bagian atas layar, pilih panah bawah di sebelah nama proyek, dan kemudian klik struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="b4406-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="b4406-198">Untuk menambahkan tugas, klik **Tambahkan tugas**.</span><span class="sxs-lookup"><span data-stu-id="b4406-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="b4406-199">Isi bidang untuk tugas, lalu klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="b4406-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="b4406-200">Terus menambahkan tugas sampai struktur rincian kerja Anda selesai.</span><span class="sxs-lookup"><span data-stu-id="b4406-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="b4406-201">Sementara membuat struktur rincian kerja Anda, Anda dapat melakukan hal berikut untuk mengatur tugas-tugas Anda:</span><span class="sxs-lookup"><span data-stu-id="b4406-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="b4406-202">Pilih tugas dan klik **Indent** untuk memindahkannya di bawah tugas lain atau klik Outdent untuk memindahkannya keluar tingkat.</span><span class="sxs-lookup"><span data-stu-id="b4406-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="b4406-203">Pilih tugas dan klik **Naik** atau **Turun** untuk bergerak naik atau turun dalam daftar.</span><span class="sxs-lookup"><span data-stu-id="b4406-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="b4406-204">Klik **Sembunyikan Gantt** untuk menyembunyikan Gantt chart, dan klik **Tunjukkan Gantt** untuk menampilkan lagi.</span><span class="sxs-lookup"><span data-stu-id="b4406-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="b4406-205">Pilih jangka waktu untuk Gantt chart di **skala waktu** berbeda.</span><span class="sxs-lookup"><span data-stu-id="b4406-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="b4406-206">Untuk menambahkan peran yang Anda tentukan dalam struktur rincian kerja Anda ke anggota tim proyek Anda, klik **Hasilkan tim proyek**.</span><span class="sxs-lookup"><span data-stu-id="b4406-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="b4406-207">Klik **Simpan** di sudut kanan bawah layar Setelah selesai melakukan perubahan.</span><span class="sxs-lookup"><span data-stu-id="b4406-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="b4406-208">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="b4406-208">See Also</span></span>  
 [<span data-ttu-id="b4406-209">Panduan Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="b4406-209">Project manager guide</span></span>](../psa/project-manager-guide.md)

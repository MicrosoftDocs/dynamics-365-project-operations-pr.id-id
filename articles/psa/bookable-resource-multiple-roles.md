---
title: Perkirakan penjualan proyek dan biaya saat sumber daya yang dapat dipesan memenuhi beberapa peran pada proyek
description: Topik ini menyediakan informasi tentang bagaimana dimensi harga dapat digunakan untuk mendukung harga dan biaya untuk sumber daya yang mengisi beberapa peran pada proyek.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078536"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="8aa20-103">Perkirakan penjualan proyek dan biaya saat sumber daya yang dapat dipesan memenuhi beberapa peran pada proyek</span><span class="sxs-lookup"><span data-stu-id="8aa20-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="8aa20-104">Perusahaan berbasis proyek sering memiliki kebutuhan atas satu sumber daya untuk melakukan beberapa peran pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="8aa20-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="8aa20-105">Masing-masing peran ini dapat dihargai dan ditentukan biayanya dengan cara yang berbeda yang berarti waktu sumber daya yang sama pada proyek dapat memperoleh perkiraan keuangan yang berbeda tergantung pada tagihan dan tarif biaya untuk masing-masing peran.</span><span class="sxs-lookup"><span data-stu-id="8aa20-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="8aa20-106">Project Service Automation memungkinkan konfigurasi nilai pada rekaman anggota tim untuk sumber daya bernama dan memungkinkan untuk penimpaan berbeda pada setiap tugas yang ditetapkan untuk anggota tim.</span><span class="sxs-lookup"><span data-stu-id="8aa20-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="8aa20-107">Contoh berikut menjelaskan bagaimana penimpaan sederhana nilai ini memungkinkan sumber daya untuk memiliki beberapa peran pada proyek dengan biaya dan tarif tagihan yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="8aa20-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="8aa20-108">Membuat tugas</span><span class="sxs-lookup"><span data-stu-id="8aa20-108">Create tasks</span></span>
<span data-ttu-id="8aa20-109">Buat dua tugas proyek untuk 40 jam masing-masing, tugas A dan tugas B. Pilih tugas A sebagai pendahulu tugas B.</span><span class="sxs-lookup"><span data-stu-id="8aa20-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="8aa20-110">Konfigurasi peran dan unit organisasi untuk anggota tim proyek generik</span><span class="sxs-lookup"><span data-stu-id="8aa20-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="8aa20-111">Pada halaman **jadwal** , pilih baris **tugas** untuk tugas A.</span><span class="sxs-lookup"><span data-stu-id="8aa20-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="8aa20-112">Di bidang **sumber daya** , pilih **buat** dalam daftar drop-down.</span><span class="sxs-lookup"><span data-stu-id="8aa20-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="8aa20-113">Pada halaman **Buat cepat anggota tim** , tentukan atribut anggota tim umum yang dapat melakukan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="8aa20-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="8aa20-114">Pilih peran dan unit organisasi yang sesuai, lalu pilih **Simpan dan tutup**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="8aa20-115">Anggota tim umum dibuat dan ditetapkan ke tugas ini.</span><span class="sxs-lookup"><span data-stu-id="8aa20-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="8aa20-116">Ulangi langkah ini untuk tugas B dan pastikan bahwa peran dan unit organisasi pada anggota tim umum yang dibuat untuk tugas B berbeda dari tugas A.</span><span class="sxs-lookup"><span data-stu-id="8aa20-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="8aa20-117">Konfigurasi peran dan unit organisasi untuk tugas proyek</span><span class="sxs-lookup"><span data-stu-id="8aa20-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="8aa20-118">Setelah Anda membuat tugas A, pilih tugas, lalu pilih **Edit tugas**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="8aa20-119">Pada halaman **rincian tugas** , temukan **peran** dan bidang **unit organisasi** , tambahkan nilai yang diperlukan dari sumber daya yang akan melakukan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="8aa20-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="8aa20-120">Jika Anda menyelesaikan skenario ini menggunakan data demo Project Service Automation, pilih **Pimpinan konsultasi** untuk peran, dan **fabrikam US** sebagai unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="8aa20-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="8aa20-121">Pilih Tugas B, dan kemudian pilih **Edit tugas**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="8aa20-122">Pada halaman **rincian tugas** , temukan **peran** dan bidang **unit organisasi** , tambahkan nilai yang diperlukan dari sumber daya yang akan melakukan tugas ini.</span><span class="sxs-lookup"><span data-stu-id="8aa20-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="8aa20-123">Pastikan bahwa nilai di bidang **peran** dan **unit organisasi** berbeda untuk tugas B dari tugas A.</span><span class="sxs-lookup"><span data-stu-id="8aa20-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="8aa20-124">Jika Anda menyelesaikan skenario ini menggunakan data demo Project Service Automation, pilih **Teknisi Jaringan** untuk peran, dan **fabrikam US** sebagai unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="8aa20-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="8aa20-125">Simpan dan tutup halaman **Detail Tugas**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="8aa20-126">Anggota tim dan perilaku perkiraan</span><span class="sxs-lookup"><span data-stu-id="8aa20-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="8aa20-127">Pada halaman **rincian tugas** , pada **anggota tim** , pilih dua anggota tim umum, lalu pilih **buat persyaratan**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="8aa20-128">Ini akan membuat persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="8aa20-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="8aa20-129">Pilih baris anggota tim untuk **Pimpinan konsultasi** lalu pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="8aa20-130">Papan jadwal membuka dan memesan sumber daya untuk persyaratan tersebut.</span><span class="sxs-lookup"><span data-stu-id="8aa20-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="8aa20-131">Pilih baris anggota tim untuk **Teknisi Jaringan** lalu pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="8aa20-132">Papan jadwal membuka dan memesan sumber daya yang sama untuk persyaratan tersebut.</span><span class="sxs-lookup"><span data-stu-id="8aa20-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="8aa20-133">Kisi anggota tim</span><span class="sxs-lookup"><span data-stu-id="8aa20-133">Team Member grid</span></span> 
<span data-ttu-id="8aa20-134">Pada kisi **anggota tim** , perhatikan bahwa dua rekaman anggota tim umum dihapus dan telah diganti menjadi satu sumber daya.</span><span class="sxs-lookup"><span data-stu-id="8aa20-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="8aa20-135">Ada satu rangkaian nilai untuk sumber daya yang menampilkan rangkaian nilai default untuk **peran** dan **unit organisasi**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="8aa20-136">Bila Anda memperluas baris rekaman anggota tim tersebut, Anda dapat melihat tugas yang berbeda pada rekaman anggota tim untuk kedua tugas tersebut.</span><span class="sxs-lookup"><span data-stu-id="8aa20-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="8aa20-137">Setiap baris tugas memiliki nilai spesifik tugas untuk **peran** dan **unit organisasi**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="8aa20-138">Kisi Perkiraan</span><span class="sxs-lookup"><span data-stu-id="8aa20-138">Estimates grid</span></span> 
<span data-ttu-id="8aa20-139">Saat menavigasi kisi **Estimasi** , Anda akan melihat bahwa kedua tugas untuk sumber daya yang sama harganya berbeda.</span><span class="sxs-lookup"><span data-stu-id="8aa20-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="8aa20-140">Tugas untuk sumber daya pada tugas A harganya menggunakan nilai atribut **peran** **Pimpinan konsultasi**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="8aa20-141">Tugas untuk sumber daya yang sama pada tugas B harganya menggunakan nilai atribut **peran** **Teknisi Jaringan**.</span><span class="sxs-lookup"><span data-stu-id="8aa20-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>






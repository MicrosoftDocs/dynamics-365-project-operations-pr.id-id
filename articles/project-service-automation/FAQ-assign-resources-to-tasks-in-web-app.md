---
title: Cara menetapkan sumber daya dapat dipesan untuk tugas di aplikasi web
description: Ikhtisar cara menetapkan sumber daya yang dapat dipesan.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752532"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="d5406-103">Cara menetapkan sumber daya yang dapat dipesan untuk tugas di aplikasi web (aplikasi Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="d5406-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d5406-104">Ada dua cara untuk menetapkan sumber daya tugas di Project Service.</span><span class="sxs-lookup"><span data-stu-id="d5406-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="d5406-105">Anda dapat memesan sumber daya sebagai anggota tim dan menetapkan sumber daya untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="d5406-106">Atau, Anda dapat membuat anggota tim generik melalui penetapan peran pada tugas, membuat tim, dan kemudian memenuhi persyaratan dukungan dengan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="d5406-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="d5406-107">Perlu diketahui bahwa jika Anda ingin menetapkan sumber daya yang dapat dipesan untuk tugas, anggota tim sumber daya dapat dipesan harus memiliki Pemesanan yang cukup tersedia.</span><span class="sxs-lookup"><span data-stu-id="d5406-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="d5406-108">Status pemesanan harus melakukan Pemesanan Nyata Jenis Komitmen dan Status berkomitmen.</span><span class="sxs-lookup"><span data-stu-id="d5406-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="d5406-109">Jika tidak ada cukup Pemesanan sumber daya, Project Service menghilangkan tugas dan menampilkan pesan kesalahan berikut:</span><span class="sxs-lookup"><span data-stu-id="d5406-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="d5406-110">*Tidak dapat menetapkan sumber daya untuk tugas - sumber daya berikut ini tidak memiliki cukup jam tercatat terhadap proyek*</span><span class="sxs-lookup"><span data-stu-id="d5406-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="d5406-111">Pesan sumber daya sebagai anggota tim lalu tetapkan sumber daya untuk tugas</span><span class="sxs-lookup"><span data-stu-id="d5406-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="d5406-112">Dengan metode ini Anda dapat menambahkan sumber daya untuk tim proyek dan kemudian menetapkan tugas ke sumber daya dalam jadwal proyek.</span><span class="sxs-lookup"><span data-stu-id="d5406-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="d5406-113">Berikut adalah cara Anda melakukan hal ini:</span><span class="sxs-lookup"><span data-stu-id="d5406-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="d5406-114">Pada tab Team Member, Anda dapat menambahkan anggota tim baru dengan memilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="d5406-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="d5406-115">Pada layar Team Member Quick Create, pilih nama sumber daya dapat dipesan dan tetapkan peran.</span><span class="sxs-lookup"><span data-stu-id="d5406-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="d5406-116">Pilih tanggal **dari** dan **hingga**.</span><span class="sxs-lookup"><span data-stu-id="d5406-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d5406-117">![Tangkapan layar menambahkan anggota tim](media/FAQ-Resources-to-Tasks2-1.png "Tangkapan layar menambahkan anggota tim")</span><span class="sxs-lookup"><span data-stu-id="d5406-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="d5406-118">Pilih salah satu metode alokasi berikut untuk pemesanan sumber daya:</span><span class="sxs-lookup"><span data-stu-id="d5406-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="d5406-119">**Kapasitas Penuh** Metode ini memesan kapasitas penuh sumber daya untuk tanggal dari dan hingga yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="d5406-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d5406-120">**Kapasitas Persentase** memesan sumber daya untuk persentase kapasitas sumber daya untuk tanggal dari dan hingga yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="d5406-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="d5406-121">**Distribusi merata Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, menyebarkannya secara merata setiap hari lebih dari yang ditentukan tanggal dari dan hingga.</span><span class="sxs-lookup"><span data-stu-id="d5406-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="d5406-122">**Muat Depan Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, memuat dulu jam per hari lebih dari yang ditentukan tanggal dari dan hingga.</span><span class="sxs-lookup"><span data-stu-id="d5406-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="d5406-123">Jangan pilih **Nihil** karena ini menambahkan sumber daya ke tim, namun tidak membuat pemesanan yang menyerap kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d5406-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="d5406-124">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="d5406-124">Select **Save**.</span></span>

    <span data-ttu-id="d5406-125">Perlu diketahui bahwa jam Pemesanan harus cukup untuk menutup jam upaya dan rentang tanggal tugas yang Anda tetapkan dengan sumber daya ini.</span><span class="sxs-lookup"><span data-stu-id="d5406-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="d5406-126">Jika mereka tidak sejajar, Anda tidak dapat menetapkan sumber daya untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="d5406-127">Pada struktur rincian kerja (WBS) untuk tugas, klik dropdown sel sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d5406-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="d5406-128">lalu:</span><span class="sxs-lookup"><span data-stu-id="d5406-128">Then:</span></span> 

    1. <span data-ttu-id="d5406-129">Pilih **Tambahkan**.</span><span class="sxs-lookup"><span data-stu-id="d5406-129">Select **Add**.</span></span>
    2. <span data-ttu-id="d5406-130">Pilih dropdown dalam **sumber daya** dan pilih anggota tim yang Anda tambahkan di atas.</span><span class="sxs-lookup"><span data-stu-id="d5406-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="d5406-131">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5406-131">Select **OK**.</span></span> <span data-ttu-id="d5406-132">Anggota tim sekarang ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d5406-133">![Screenshot menambahkan sumber daya dengan WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot menambahkan sumber daya dengan WBS")</span><span class="sxs-lookup"><span data-stu-id="d5406-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="d5406-134">Pada kisi anggota tim, Anda akan melihat agregat jam sumber daya yang ditetapkan dalam jam yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="d5406-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="d5406-135">Ini akan menjadi kurang dari atau sama dengan jam tercatat untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d5406-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5406-136">![Screenshot jam yang ditetapkan untuk sumber daya](media/FAQ-Resources-to-Tasks2-3.png "Screenshot jam yang ditetapkan untuk sumber daya")</span><span class="sxs-lookup"><span data-stu-id="d5406-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="d5406-137">Jika tugas yang Anda coba untuk tetapkan sumber dayanya dimulai setelah tanggal berakhir Pemesanan sumber daya, sumber daya tidak akan muncul di dropdown.</span><span class="sxs-lookup"><span data-stu-id="d5406-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="d5406-138">Perlu diketahui bahwa Anda dapat menetapkan sumber daya untuk lebih lama daripada jam mereka tercatat jika sumber daya memiliki kapasitas belum ditugaskan yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="d5406-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="d5406-139">Dalam kasus ini sumber daya hanya akan ditetapkan sebagian hingga Pemesanan mereka.</span><span class="sxs-lookup"><span data-stu-id="d5406-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="d5406-140">Anda dapat melihat jam tugas belum ditugaskan yang tersisa tersebut dengan menambahkan kolom jam kosong untuk struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="d5406-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="d5406-141">Jika sumber daya ditetapkan ke jam mereka dipesan (jam mereka dipesan sama dengan jam mereka ditetapkan), Anda akan melihat pesan kesalahan berikut bila Anda mencoba menetapkan mereka lebih lanjut dengan tugas:</span><span class="sxs-lookup"><span data-stu-id="d5406-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="d5406-142">*Tidak dapat menetapkan sumber daya untuk tugas - sumber daya berikut ini tidak memiliki cukup jam tercatat terhadap proyek.*</span><span class="sxs-lookup"><span data-stu-id="d5406-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="d5406-143">Selain itu, anggota tim manajer proyek default yang ditambahkan ke tim saat Anda membuat proyek ditambahkan tanpa Pemesanan apa pun dan tidak dapat ditetapkan ke tugas apa pun.</span><span class="sxs-lookup"><span data-stu-id="d5406-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="d5406-144">Mereka tidak akan ditampilkan di dropdown sumber daya untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="d5406-145">Jika Anda ingin menetapkan sumber daya ini, Anda harus menghapusnya dari tim dan kemudian kembali menambahkannya dengan alokasi metode Selain Nihil.</span><span class="sxs-lookup"><span data-stu-id="d5406-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="d5406-146">Alasan ditambahkan ke tim ketika proyek dibuat adalah sehingga proyek memiliki minimal satu pemberi izin proyek secara default.</span><span class="sxs-lookup"><span data-stu-id="d5406-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="d5406-147">Membuat anggota tim generik melalui penetapan peran di tugas</span><span class="sxs-lookup"><span data-stu-id="d5406-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="d5406-148">Metode ini menjamin bahwa sumber daya memiliki cukup Pemesanan untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="d5406-149">Pertama, dengan metode ini Anda membuat placeholder atau sumber daya generik yang menjelaskan karakteristik sumber daya bernama yang pada akhirnya akan bekerja pada tugas dengan membuat tim setelah menetapkan peran untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="d5406-150">Berikut adalah cara Anda melakukan hal ini:</span><span class="sxs-lookup"><span data-stu-id="d5406-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="d5406-151">Pada struktur rincian kerja, pilih tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="d5406-152">Pilih ikon dropdown **Peran yang ditetapkan** di sel sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d5406-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="d5406-153">Pilih **peran** dropdown dan memilih peran untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="d5406-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="d5406-154">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5406-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="d5406-155">![Screenshot menggunakan WBS untuk menambahkan sumber daya](media/FAQ-Resources-to-Tasks2-4.png "Screenshot menggunakan WBS untuk menambahkan sumber daya")</span><span class="sxs-lookup"><span data-stu-id="d5406-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="d5406-156">Setelah menyelesaikan penugasan peran untuk tugas dalam WBS, pilih **membuat tim proyek**.</span><span class="sxs-lookup"><span data-stu-id="d5406-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="d5406-157">Project Service membuat jumlah minimum anggota tim generik berdasarkan peran, unit organisasi sumber daya, dan kalender proyek dengan menggabungkan penugasan tugas.</span><span class="sxs-lookup"><span data-stu-id="d5406-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5406-158">![Tangkapan layar membuat tim proyek](media/FAQ-Resources-to-Tasks2-5.png "Tangkapan layar membuat tim proyek")</span><span class="sxs-lookup"><span data-stu-id="d5406-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="d5406-159">Pada kisi Team Member, Anda akan melihat sumber daya jenis sumber daya generik dengan nama peran dan posisi.</span><span class="sxs-lookup"><span data-stu-id="d5406-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="d5406-160">Jika dua sumber daya diperlukan untuk peran untuk menyelesaikan pekerjaan, fitur membuat tim membuat dua anggota tim dan menggunakan nama posisi untuk membedakan mereka.</span><span class="sxs-lookup"><span data-stu-id="d5406-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5406-161">![Screenshot menambahkan dua sumber daya umum](media/FAQ-Resources-to-Tasks2-6.png "Screenshot menambahkan dua sumber daya umum")</span><span class="sxs-lookup"><span data-stu-id="d5406-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="d5406-162">Anda dapat membuka persyaratan sumber daya dukungan untuk anggota generik tim dengan memilih link dalam persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d5406-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="d5406-163">![Gambar layar membuka persyaratan sumber daya pendukung](media/FAQ-Resources-to-Tasks2-7.png "Gambar layar membuka persyaratan sumber daya pendukung")</span><span class="sxs-lookup"><span data-stu-id="d5406-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="d5406-164">Pilih **Pesan** untuk sumber daya generik, dan kemudian Anda dapat menggunakan papan jadwal untuk mencari dan memesan sumber daya nyata.</span><span class="sxs-lookup"><span data-stu-id="d5406-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="d5406-165">Anda juga dapat mengajukan persyaratan untuk pemenuhannya dengan memilih **Ajukan Permintaan**.</span><span class="sxs-lookup"><span data-stu-id="d5406-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="d5406-166">Ketika sumber daya generik dipenuhi dengan sumber daya bernama, sumber daya generik dihilangkan dari tim dan penugasan tugas untuk sumber daya generik ditetapkan ke sumber daya bernama yang memenuhi persyaratan sumber daya generik itu.</span><span class="sxs-lookup"><span data-stu-id="d5406-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 


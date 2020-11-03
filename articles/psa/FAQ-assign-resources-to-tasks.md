---
title: Menetapkan sumber daya untuk tugas
description: Topik ini menyediakan informasi tentang cara menetapkan sumber daya untuk tugas.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078673"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="76a71-103">Menetapkan sumber daya untuk tugas</span><span class="sxs-lookup"><span data-stu-id="76a71-103">Assign a resource to a task</span></span>

<span data-ttu-id="76a71-104">Ada tiga cara untuk menetapkan sumber daya tugas di Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="76a71-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="76a71-105">Pesan sumber daya sebagai anggota tim lalu tetapkan sumber daya untuk tugas</span><span class="sxs-lookup"><span data-stu-id="76a71-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="76a71-106">Anda dapat menambahkan sumber daya untuk tim proyek dan kemudian menetapkan sumber daya untuk tugas dalam jadwal proyek.</span><span class="sxs-lookup"><span data-stu-id="76a71-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="76a71-107">Pada tab **Team Member** , Anda dapat menambahkan anggota tim baru dengan memilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="76a71-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="76a71-108">Panel **Team Member Quick Create** terbuka, di mana Anda dapat memilih nama sumber daya dapat dipesan dan menetapkan peran.</span><span class="sxs-lookup"><span data-stu-id="76a71-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="76a71-109">Pilih salah satu metode alokasi berikut untuk pemesanan sumber daya:</span><span class="sxs-lookup"><span data-stu-id="76a71-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="76a71-110">**Kapasitas Penuh** Metode ini memesan kapasitas penuh sumber daya untuk tanggal dari dan hingga yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="76a71-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="76a71-111">**Kapasitas Persentase** memesan sumber daya untuk persentase kapasitas sumber daya untuk tanggal dari dan hingga yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="76a71-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="76a71-112">**Distribusi merata Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, menyebarkannya secara merata setiap hari lebih dari yang ditentukan tanggal dari dan hingga.</span><span class="sxs-lookup"><span data-stu-id="76a71-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="76a71-113">**Muat Depan Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, memuat dulu jam per hari lebih dari yang ditentukan tanggal dari dan hingga.</span><span class="sxs-lookup"><span data-stu-id="76a71-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="76a71-114">**Tidak ada** menambahkan sumber daya ke tim, namun tidak membuat pemesanan yang menyerap kapasitas mereka.</span><span class="sxs-lookup"><span data-stu-id="76a71-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="76a71-115">Pada kisi **jadwal** untuk tugas, pilih ikon **sumber daya** di sel sumber daya, dan kemudian pilih anggota tim yang baru saja ditambahkan di **Team Members**.</span><span class="sxs-lookup"><span data-stu-id="76a71-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="76a71-116">Pada tab **Team Member** dan tab **rekonsiliasi** , sumber daya menunjukkan jam dipesan dan ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="76a71-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="76a71-117">Jam harus sama, tetapi tidak wajib karena Pemesanan dan tugas tidak berhubungan erat.</span><span class="sxs-lookup"><span data-stu-id="76a71-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="76a71-118">Tab **rekonsiliasi** menyediakan rincian saat mereka berbeda, seperti saat Anda menetapkan sumber daya lebih lama dibandingkan Anda memesan.</span><span class="sxs-lookup"><span data-stu-id="76a71-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="76a71-119">Jika dibutuhkan Anda dapat mengoreksi informasi dengan memperluas Pemesanan sumber daya atau mengubah tugas.</span><span class="sxs-lookup"><span data-stu-id="76a71-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="76a71-120">Membuat anggota tim generik melalui penetapan tugas</span><span class="sxs-lookup"><span data-stu-id="76a71-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="76a71-121">Saat membuat anggota tim generik melalui penetapan tugas, Anda membuat placeholder atau sumber daya generik yang menjelaskan karakteristik sumber daya bernama yang pada akhirnya akan bekerja pada tugas.</span><span class="sxs-lookup"><span data-stu-id="76a71-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="76a71-122">Anda kemudian menghasilkan persyaratan (atau mengirimkan permintaan menggunakan persyaratan) yang digunakan untuk mencari dan memesan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="76a71-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="76a71-123">Pada kisi **jadwal** untuk tugas, pilih ikon sumber daya di sel **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="76a71-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="76a71-124">Masukkan nama untuk berfungsi sebagai nama sumber daya.</span><span class="sxs-lookup"><span data-stu-id="76a71-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="76a71-125">Misalnya, manajer program.</span><span class="sxs-lookup"><span data-stu-id="76a71-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="76a71-126">Pada **Buat** , dan di bidang **Buat cepat anggota tim proyek** , atur peran sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="76a71-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="76a71-127">Anda dapat terus menetapkan tugas ke sumber daya placeholder ini dengan memilih sumber daya pada **pemilih sumber daya** untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="76a71-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="76a71-128">Mereka terdaftar di bawah **Team Members**.</span><span class="sxs-lookup"><span data-stu-id="76a71-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="76a71-129">Setelah selesai menetapkan sumber daya generik, pilih sumber daya generik di **tim** tab kemudian pilih **menghasilkan persyaratan** untuk membuat persyaratan sumber daya untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="76a71-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="76a71-130">Pilih **Pesan** untuk sumber daya generik.</span><span class="sxs-lookup"><span data-stu-id="76a71-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="76a71-131">Anda dapat menggunakan papan jadwal untuk mencari dan memesan sumber daya nyata.</span><span class="sxs-lookup"><span data-stu-id="76a71-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="76a71-132">Anda juga dapat mengirimkan persyaratan untuk pemenuhannya dengan manajer sumber daya.</span><span class="sxs-lookup"><span data-stu-id="76a71-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="76a71-133">Ketika sumber daya generik dipenuhi dengan sumber daya bernama, sumber daya generik dihilangkan dari tim dan penugasan tugas untuk sumber daya generik ditetapkan ke sumber daya bernama yang memenuhi persyaratan sumber daya generik itu.</span><span class="sxs-lookup"><span data-stu-id="76a71-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="76a71-134">Menetapkan sumber daya bernama dari daftar semua sumber daya yang dapat dipesan</span><span class="sxs-lookup"><span data-stu-id="76a71-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="76a71-135">Anda dapat menggunakan kotak pencarian di **pemilih sumber daya** untuk mencari semua sumber daya dapat dipesan dan menetapkan mereka untuk tugas.</span><span class="sxs-lookup"><span data-stu-id="76a71-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="76a71-136">Sumber daya yang ditetapkan dengan cara ini ditambahkan ke tim tanpa pemesanan.</span><span class="sxs-lookup"><span data-stu-id="76a71-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="76a71-137">Hal ini mirip dengan menambahkan anggota tim dan memilih tidak ada sebagai metode alokasi.</span><span class="sxs-lookup"><span data-stu-id="76a71-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="76a71-138">Sumber daya ditampilkan dalam tab **tim** dan tab **rekonsiliasi** sebagai sumber daya dengan hanya tugas dan defisit pemesanan.</span><span class="sxs-lookup"><span data-stu-id="76a71-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="76a71-139">Pesan mereka jika Anda ingin menggunakan ketersediaan mereka.</span><span class="sxs-lookup"><span data-stu-id="76a71-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="76a71-140">Pada kisi **jadwal** untuk tugas, pilih ikon sumber daya di sel **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="76a71-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="76a71-141">Mulai mengetik nama.</span><span class="sxs-lookup"><span data-stu-id="76a71-141">Start typing a name.</span></span> <span data-ttu-id="76a71-142">Hasil pencarian untuk nama akan ditampilkan di **pemilih sumber daya** dalam **sumber daya lainnya**.</span><span class="sxs-lookup"><span data-stu-id="76a71-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="76a71-143">Pilih sumber daya yang akan ditetapkan ke tugas.</span><span class="sxs-lookup"><span data-stu-id="76a71-143">Select the resource that you want to assign to the task.</span></span>


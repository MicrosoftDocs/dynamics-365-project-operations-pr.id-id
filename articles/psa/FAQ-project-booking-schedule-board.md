---
title: Buat pemesanan proyek dari papan jadwal
description: Topik ini menyediakan informasi tentang cara membuat pemesanan proyek dari papan jadwal.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 7032af78168c742ac64cb2a7174cabcbda579ff8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146532"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="a34ad-103">Buat pemesanan proyek dari papan jadwal</span><span class="sxs-lookup"><span data-stu-id="a34ad-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a34ad-104">Anda dapat memesan sumber daya ke proyek baik secara langsung dari tab **tim** proyek atau dengan membuat persyaratan sumber daya dari tugas anggota tim generik dan kemudian memenuhi persyaratan yang dihasilkan dengan anggota tim proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="a34ad-105">Anda juga dapat memesan sumber daya ke proyek secara langsung dari papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="a34ad-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="a34ad-106">Ada tiga cara untuk melakukannya:</span><span class="sxs-lookup"><span data-stu-id="a34ad-106">There are three ways to do this:</span></span>

- <span data-ttu-id="a34ad-107">**Pesan dari persyaratan sumber daya yang dihasilkan** : Anda dapat membuat persyaratan sumber daya setelah membuat sumber daya generik dan menetapkan tugas dalam suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="a34ad-108">**Pesan dari persyaratan utama:** persyaratan utama ditampilkan di papan jadwal pada tab **Project**.</span><span class="sxs-lookup"><span data-stu-id="a34ad-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="a34ad-109">**Pesan dari persyaratan sumber daya baru:** Anda dapat membuat persyaratan sumber daya dari awal dan mengaitkannya dengan proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="a34ad-110">Di papan jadwal, persyaratan sumber daya akan ditampilkan pada tab **persyaratan terbuka**.</span><span class="sxs-lookup"><span data-stu-id="a34ad-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="a34ad-111">Pesan dari persyaratan sumber daya yang dihasilkan.</span><span class="sxs-lookup"><span data-stu-id="a34ad-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="a34ad-112">Anda dapat membuat sumber daya generik dan menetapkan satu atau lebih tugas dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="a34ad-113">Kemudian Anda dapat membuat persyaratan sumber daya dari anggota tim generik.</span><span class="sxs-lookup"><span data-stu-id="a34ad-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="a34ad-114">Di papan jadwal, sumber daya ini akan muncul pada tab **persyaratan terbuka**. Anda mungkin harus menggunakan filter kolom pada kisi jika Anda memiliki banyak persyaratan terbuka.</span><span class="sxs-lookup"><span data-stu-id="a34ad-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="a34ad-115">![Buka tab Persyaratan di papan jadwal](media/FAQ-Project-Booking-Schedule-Board-1.png "Tangkapan layar tabel Pemesanan dan tugas")</span><span class="sxs-lookup"><span data-stu-id="a34ad-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="a34ad-116">Pilih Persyaratan.</span><span class="sxs-lookup"><span data-stu-id="a34ad-116">Select the requirement.</span></span> <span data-ttu-id="a34ad-117">Tab **cari ketersediaan** akan muncul di bagian atas baris yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="a34ad-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="a34ad-118">Ketika Anda memilih tab, mode asisten jadwal papan jadwal terbuka kemudian memfilter sumber daya yang tersedia yang memenuhi persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="a34ad-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="a34ad-119">Setelah itu, Anda dapat memesan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="a34ad-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="a34ad-120">Anda juga dapat tarik dan jatuhkan baris yang dipilih dari bawah papan jadwal ke sel sumber daya dalam kisi di atas.</span><span class="sxs-lookup"><span data-stu-id="a34ad-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="a34ad-121">Saat Anda melepas itu, buka **membuat pemesanan sumber daya** panel di sebelah kanan.</span><span class="sxs-lookup"><span data-stu-id="a34ad-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="a34ad-122">Memilih **Pesan** akan memesan sumber daya ke tim proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-122">Selecting **Book** books the resource onto the project team.</span></span>

![Buat panel Pemesanan Sumber Daya](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="a34ad-124">Pesan dari persyaratan utama</span><span class="sxs-lookup"><span data-stu-id="a34ad-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="a34ad-125">Membuat proyek dalam Project Service secara otomatis membuat persyaratan sumber daya yang disebut persyaratan utama.</span><span class="sxs-lookup"><span data-stu-id="a34ad-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="a34ad-126">Hal ini adalah persyaratan kosong yang digunakan untuk dengan cepat memesan sumber daya dengan papan jadwal tanpa membuat persyaratan atau membuatnya dari awal.</span><span class="sxs-lookup"><span data-stu-id="a34ad-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="a34ad-127">Karena persyaratan kosong, Anda harus menentukan tanggal serta metode alokasi dan jam jika berlaku.</span><span class="sxs-lookup"><span data-stu-id="a34ad-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="a34ad-128">Untuk memesan sumber daya dengan persyaratan Utam, di papan jadwal, pilih tab **proyek**. Anda mungkin perlu menggunakan filter kolom di kolom **Proyek** jika Anda punya banyak proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="a34ad-129">![Filter kolom di papan jadwal](media/FAQ-Project-Booking-Schedule-Board-2.png "Tangkapan layar tabel Pemesanan dan tugas")</span><span class="sxs-lookup"><span data-stu-id="a34ad-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="a34ad-130">Pilih persyaratan yang hanya memiliki nama proyek sebagai nama dan memiliki durasi nol (0).</span><span class="sxs-lookup"><span data-stu-id="a34ad-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="a34ad-131">Pilih Tab **cari ketersediaan** yang akan muncul di baris.</span><span class="sxs-lookup"><span data-stu-id="a34ad-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="a34ad-132">Hal ini menempatkan papan jadwal dalam mode asisten jadwal dan menampilkan sumber daya yang dapat dipesan ke proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="a34ad-133">Karena **persyaratan utama** adalah persyaratan kosong dengan durasi nol (0), Anda harus mengatur durasi pada panel **membuat pemesanan sumber daya** saat memilih dan Pemesanan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="a34ad-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="a34ad-134">Anda juga dapat memilih **persyaratan utama proyek** di bagian bawah papan jadwal dan tarik dan letakkan di sumber daya untuk memesannya.</span><span class="sxs-lookup"><span data-stu-id="a34ad-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="a34ad-135">Karena **persyaratan utama** adalah persyaratan kosong dengan durasi nol (0), Anda harus mengatur durasi pada panel **membuat pemesanan sumber daya** saat memilih dan Pemesanan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="a34ad-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="a34ad-136">Bila Anda memesan sumber daya melalui **persyaratan utama** di papan jadwal, Anda menambahkannya ke tim proyek tanpa tugas apa pun.</span><span class="sxs-lookup"><span data-stu-id="a34ad-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="a34ad-137">Pesan dari persyaratan sumber daya yang baru.</span><span class="sxs-lookup"><span data-stu-id="a34ad-137">Book from a new resource requirement</span></span>
<span data-ttu-id="a34ad-138">Selesaikan langkah-langkah berikut untuk memesan dari persyaratan sumber daya baru.</span><span class="sxs-lookup"><span data-stu-id="a34ad-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="a34ad-139">Buka **persyaratan sumber daya** kemudian pilih **baru** untuk membuat persyaratan sumber daya baru.</span><span class="sxs-lookup"><span data-stu-id="a34ad-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="a34ad-140">Pada tab **proyek**, pilih proyek untuk mengaitkan persyaratan ke proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="a34ad-141">Di papan jadwal, persyaratan yang baru dibuat ini ditampilkan sebagai **persyaratan terbuka** yang Anda dapat memenuhi.</span><span class="sxs-lookup"><span data-stu-id="a34ad-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="a34ad-142">Pesan sumber daya untuk menambahkannya ke tim proyek.</span><span class="sxs-lookup"><span data-stu-id="a34ad-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="a34ad-143">Karena sumber daya sudah dipesan, Anda harus menetapkan tugas secara manual.</span><span class="sxs-lookup"><span data-stu-id="a34ad-143">Now that the resource is booked, you must assign tasks manually.</span></span>


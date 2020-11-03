---
title: Pesan untuk proyek
description: Topik ini menyediakan informasi tentang cara memesan sumber daya untuk proyek.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078336"
---
# <a name="book-to-a-project"></a><span data-ttu-id="d244f-103">Pesan untuk proyek</span><span class="sxs-lookup"><span data-stu-id="d244f-103">Book to a project</span></span>

<span data-ttu-id="d244f-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="d244f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d244f-105">Ada saat di mana manajer proyek atau manajer sumber daya harus mengalokasikan sumber daya untuk proyek tanpa persyaratan tertentu yang ditentukan dari anggota tim umum.</span><span class="sxs-lookup"><span data-stu-id="d244f-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="d244f-106">Hal ini dapat dicapai dengan salah satu dari tiga cara.</span><span class="sxs-lookup"><span data-stu-id="d244f-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="d244f-107">Memesan dari kisi anggota tim</span><span class="sxs-lookup"><span data-stu-id="d244f-107">Book from the team member grid</span></span>
- <span data-ttu-id="d244f-108">Memesan dari papan jadwal</span><span class="sxs-lookup"><span data-stu-id="d244f-108">Book from the schedule board</span></span>
- <span data-ttu-id="d244f-109">Pesan dari formulir **proyek**</span><span class="sxs-lookup"><span data-stu-id="d244f-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="d244f-110">Memesan dari kisi anggota tim</span><span class="sxs-lookup"><span data-stu-id="d244f-110">Book from the team member grid</span></span>

<span data-ttu-id="d244f-111">Jika organisasi Anda beroperasi dalam mode alokasi sumber daya hibrid, manajer proyek dapat memesan sumber daya langsung ke proyek dengan menyelesaikan langkah-langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="d244f-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="d244f-112">Dari proyek, buka kisi anggota tim, lalu pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="d244f-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="d244f-113">Tentukan nama posisi dan peran sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d244f-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="d244f-114">Pilih sumber daya yang dapat dipesan dari pencarian yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="d244f-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="d244f-115">Setelah Anda memilih sumber daya, tentukan informasi bidang berikut untuk memesan sumber daya:</span><span class="sxs-lookup"><span data-stu-id="d244f-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="d244f-116">Tanggal mulai</span><span class="sxs-lookup"><span data-stu-id="d244f-116">Start date</span></span>
    - <span data-ttu-id="d244f-117">Tanggal Berakhir</span><span class="sxs-lookup"><span data-stu-id="d244f-117">Finish date</span></span>
    - <span data-ttu-id="d244f-118">Metode alokasi</span><span class="sxs-lookup"><span data-stu-id="d244f-118">Allocation method</span></span>
    - <span data-ttu-id="d244f-119">Jam, jika berlaku</span><span class="sxs-lookup"><span data-stu-id="d244f-119">Hours, if applicable</span></span>
    - <span data-ttu-id="d244f-120">Pemberi Persetujuan Proyek</span><span class="sxs-lookup"><span data-stu-id="d244f-120">Project approver</span></span>

6. <span data-ttu-id="d244f-121">Pilih **Simpan dan Tutup**</span><span class="sxs-lookup"><span data-stu-id="d244f-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="d244f-122">Memesan dari papan jadwal</span><span class="sxs-lookup"><span data-stu-id="d244f-122">Book from the schedule board</span></span>

<span data-ttu-id="d244f-123">Bila manajer sumber daya perlu memesan sumber daya secara langsung ke proyek, mereka dapat menggunakan papan jadwal dan persyaratan proyek.</span><span class="sxs-lookup"><span data-stu-id="d244f-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="d244f-124">Persyaratan proyek adalah persyaratan sumber daya yang selalu tersedia untuk dipesan.</span><span class="sxs-lookup"><span data-stu-id="d244f-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="d244f-125">Selesaikan langkah-langkah berikut untuk memesan langsung ke formulir proyek dari papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="d244f-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="d244f-126">Navigasi ke papan jadwal dan di halaman kiri, filter untuk sumber daya yang Anda pertimbangkan untuk kebutuhan.</span><span class="sxs-lookup"><span data-stu-id="d244f-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="d244f-127">Di panel bawah, pilih tab **proyek** untuk melihat daftar persyaratan proyek.</span><span class="sxs-lookup"><span data-stu-id="d244f-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="d244f-128">Tarik persyaratan ke sumber daya dan tentukan informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="d244f-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="d244f-129">Tanggal mulai</span><span class="sxs-lookup"><span data-stu-id="d244f-129">Start date</span></span>
    - <span data-ttu-id="d244f-130">Tanggal Berakhir</span><span class="sxs-lookup"><span data-stu-id="d244f-130">Finish date</span></span>
    - <span data-ttu-id="d244f-131">Status pemesanan</span><span class="sxs-lookup"><span data-stu-id="d244f-131">Booking status</span></span>
    - <span data-ttu-id="d244f-132">Metode Pemesanan</span><span class="sxs-lookup"><span data-stu-id="d244f-132">Booking method</span></span>
    - <span data-ttu-id="d244f-133">Durasi</span><span class="sxs-lookup"><span data-stu-id="d244f-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="d244f-134">Pesan dari formulir proyek</span><span class="sxs-lookup"><span data-stu-id="d244f-134">Book from the Project form</span></span>

<span data-ttu-id="d244f-135">Sebagai manajer proyek, Anda mungkin perlu memesan sumber daya untuk proyek, namun hanya mengetahui kriteria daripada nama sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d244f-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="d244f-136">Selesaikan langkah-langkah berikut untuk menggunakan Asisten jadwal untuk menemukan sumber daya berdasarkan atribut sumber daya yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="d244f-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="d244f-137">Navigasi ke proyek dan pilih **Pesan** untuk membuka asisten jadwal.</span><span class="sxs-lookup"><span data-stu-id="d244f-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="d244f-138">Menggunakan filter di sisi kiri asisten jadwal, Persempit kriteria, lalu pilih **Cari.**</span><span class="sxs-lookup"><span data-stu-id="d244f-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="d244f-139">Berdasarkan sumber daya yang dikembalikan dalam hasil, Anda dapat memesan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d244f-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="d244f-140">Metode ini tidak membuat pemesanan untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d244f-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="d244f-141">Justru, ia menambahkan sumber daya ke tim.</span><span class="sxs-lookup"><span data-stu-id="d244f-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="d244f-142">Setelah anggota tim ditambahkan ke proyek, manajer proyek dapat menggunakan memelihara Pemesanan atau memperpanjang Pemesanan untuk menambahkan Pemesanan yang diperlukan ke sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d244f-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>

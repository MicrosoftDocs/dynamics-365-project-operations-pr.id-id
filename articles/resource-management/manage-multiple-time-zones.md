---
title: Mengelola zona waktu
description: Saat proyek dibuat, zona waktunya didasarkan pada zona waktu yang ditentukan dalam template jam kerja yang diterapkan.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078422"
---
# <a name="manage-time-zones"></a><span data-ttu-id="22c71-103">Mengelola zona waktu</span><span class="sxs-lookup"><span data-stu-id="22c71-103">Manage time zones</span></span>

<span data-ttu-id="22c71-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="22c71-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="22c71-105">Proyek</span><span class="sxs-lookup"><span data-stu-id="22c71-105">Projects</span></span>

<span data-ttu-id="22c71-106">Saat proyek dibuat, zona waktunya didasarkan pada zona waktu yang ditentukan dalam template jam kerja yang diterapkan.</span><span class="sxs-lookup"><span data-stu-id="22c71-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="22c71-107">Pada **proyek** untuk, tanggalnya selalu relatif terhadap zona waktu pengguna yang masuk pada setiap tab, kecuali tab **tugas**. Bila Anda melihat struktur rincian kerja, tanggal akan selalu ditampilkan di zona waktu proyek.</span><span class="sxs-lookup"><span data-stu-id="22c71-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="22c71-108">Tugas</span><span class="sxs-lookup"><span data-stu-id="22c71-108">Tasks</span></span>

<span data-ttu-id="22c71-109">Bila tugas dibuat, waktu mulai, waktu berakhir, dan jam/hari dikontrol oleh jam kerja proyek.</span><span class="sxs-lookup"><span data-stu-id="22c71-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="22c71-110">Misalnya, jika tugas dibuat dengan proyek yang zona waktunya adalah -8 PST dan memiliki jam kerja berikut: 9:00 pagi hingga 5:00 sore Senin hingga Jumat, tugas apa pun yang dibuat tanpa penetapan akan menghormati waktu mulai dan waktu berakhir kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="22c71-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="22c71-111">Mengelola sumber daya dengan zona waktu</span><span class="sxs-lookup"><span data-stu-id="22c71-111">Manage resources with time zones</span></span>

<span data-ttu-id="22c71-112">Untuk hasil yang akurat dan dapat diprediksi saat menggunakan **memperpanjang Pemesanan** , ada dua prasyarat utama yang harus dipenuhi:</span><span class="sxs-lookup"><span data-stu-id="22c71-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="22c71-113">Pengguna harus mengkonfigurasi zona waktu perangkat mereka untuk mencocokkan zona waktu yang ditentukan di **Pengaturan personalisasi** sistem.</span><span class="sxs-lookup"><span data-stu-id="22c71-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Pengaturan zona waktu di Windows 10](media/reconcile-assignments-03.png)

  ![Pengaturan zona waktu di Pengaturan personalisasi](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="22c71-116">Sumber daya yang dapat dipesan harus memiliki minimal satu menit waktu kerja yang tumpang tindih dengan kontur yang digunakan untuk menentukan ekstensi yang diminta.</span><span class="sxs-lookup"><span data-stu-id="22c71-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="22c71-117">Misalnya, sumber daya berikut dengan jam kerja yang jatuh antara 9:00 pagi dan 7:00 sore.</span><span class="sxs-lookup"><span data-stu-id="22c71-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Perbandingan kontur sumber daya](media/reconcile-assignments-05.png)

<span data-ttu-id="22c71-119">Tabel berikut menampilkan:</span><span class="sxs-lookup"><span data-stu-id="22c71-119">The following table shows:</span></span>

- <span data-ttu-id="22c71-120">Template kalender Proyek</span><span class="sxs-lookup"><span data-stu-id="22c71-120">A project calendar template</span></span>
- <span data-ttu-id="22c71-121">Sumber daya A: sumber daya ini memiliki kalender yang sama dan berada di zona waktu yang sama dengan proyek.</span><span class="sxs-lookup"><span data-stu-id="22c71-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="22c71-122">Waktu mulai pemesanan adalah 9:00.</span><span class="sxs-lookup"><span data-stu-id="22c71-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="22c71-123">Sumber daya B: sumber daya ini terletak di zona waktu yang berbeda dari proyek dan dimulai pada 7:00 pagi di zona waktu mereka.</span><span class="sxs-lookup"><span data-stu-id="22c71-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="22c71-124">Namun, Pemesanan akan dimulai pada pukul 9:00 karena itu adalah waktu mulai terawal kontur tugas.</span><span class="sxs-lookup"><span data-stu-id="22c71-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="22c71-125">Sumber daya C dan D: sumber daya berada di zona waktu yang berbeda, keduanya berbeda dari satu sama lain dan proyek, dan Pemesanan mereka tidak dimulai lebih awal dari waktu mulai masing-masing yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="22c71-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="22c71-126">Entitas</span><span class="sxs-lookup"><span data-stu-id="22c71-126">Entity</span></span>  |<span data-ttu-id="22c71-127">Kalender</span><span class="sxs-lookup"><span data-stu-id="22c71-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="22c71-128">Template kalender Proyek</span><span class="sxs-lookup"><span data-stu-id="22c71-128">Project calendar template</span></span>   | ![Kalender Proyek](media/reconcile-assignments-06.png) |
|<span data-ttu-id="22c71-130">Sumber Daya A</span><span class="sxs-lookup"><span data-stu-id="22c71-130">Resource A</span></span>  | ![Kalender Sumber Daya A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="22c71-132">Sumber Daya B</span><span class="sxs-lookup"><span data-stu-id="22c71-132">Resource B</span></span>  |  ![Kalender Sumber Daya B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="22c71-134">Sumber Daya C</span><span class="sxs-lookup"><span data-stu-id="22c71-134">Resource C</span></span>  |  ![Kalender Sumber Daya C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="22c71-136">Sumber Daya D</span><span class="sxs-lookup"><span data-stu-id="22c71-136">Resource D</span></span>  | ![Kalender Sumber Daya D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="22c71-138">Bila Anda menavigasi ke tampilan **rekonsiliasi** , penetapan sumber daya dan kekurangan Pemesanan terkait ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="22c71-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Tampilan rekonsiliasi sebelum perpanjangan](media/reconcile-assignments-10.png)

<span data-ttu-id="22c71-140">Setelah fungsi perpanjangan Pemesanan telah digunakan untuk setiap sumber daya, Pemesanan akan berhasil diperpanjang untuk setiap sumber daya karena setiap jam kerja sumber daya saling tumpang tindih dengan kontur kekurangan.</span><span class="sxs-lookup"><span data-stu-id="22c71-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Tampilan rekonsiliasi setelah ekstensi pemesanan](media/reconcile-assignments-11.png) 

<span data-ttu-id="22c71-142">Perhatikan bahwa melihat lebih dekat rincian pemesanan menunjukkan perbedaan dalam waktu mulai pemesanan.</span><span class="sxs-lookup"><span data-stu-id="22c71-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="22c71-143">Pemesanan tidak dimulai lebih awal dari waktu mulai kontur penetapan dan tidak lebih awal dari waktu mulai yang tersedia untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="22c71-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Pemesanan baru sumber daya di papan jadwal](media/reconcile-assignments-12.png)

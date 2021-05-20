---
title: Jadwalkan sumber daya untuk sebuah proyek
description: Cara menjadwalkan sumber daya di Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 329923e6d47fd36881aea8db8eba41a868829220
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951438"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="f9d9a-103">Jadwalkan sumber daya untuk proyek (Project Service)</span><span class="sxs-lookup"><span data-stu-id="f9d9a-103">Schedule resources for a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f9d9a-104">Anda dapat memeriksa ketersediaan sumber untuk mendapatkan pandangan yang menyeluruh tentang sepadat apa tingkat pemesanan sumber daya Anda, atau Anda dapat menyaring tampilan menurut keterampilan, tim, lokasi, dan pilihan lainnya.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="f9d9a-105">Papan jadwal menunjukkan daftar sumber daya dan ketersediaan mereka.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="f9d9a-106">Pilih mode tampilan untuk menunjukkan ketersediaan menurut **jam**, **hari**, **minggu**, atau **bulan**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="f9d9a-107">Sebelum Anda menggunakan papan jadwal, sangat penting untuk mengatur itu.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="f9d9a-108">Untuk informasi lebih lanjut, lihat [Mengkonfigurasi papan jadwal (Field Service atau Project Service Automation)](/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="f9d9a-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="f9d9a-109">Jika Anda menggunakan versi yang lebih tua, untuk ketersediaan sumber daya, lihat [Lihat ketersediaan sumber daya](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="f9d9a-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="f9d9a-110">Untuk menggunakan fungsionalitas pemesanan papan jadwal, geocoding, dan Layanan lokasi, Anda perlu mengaktifkan peta.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="f9d9a-111">Di menu utama, pilih **Penjadwalan Sumber daya** > **Administrasi**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="f9d9a-112">Klik **Parameter Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="f9d9a-113">Buka rekaman dan gulir ke bawah ke bagian **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="f9d9a-114">Pada bidang **Sambung ke Maps**, pilih **ya**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="f9d9a-115">Tnerima persyaratan dan simpan rekaman.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="f9d9a-116">Di menu utama, pilih **Project Service** > **papan jadwal**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="f9d9a-117">Dari sini, ada beberapa cara untuk secara manual menjadwalkan persyaratan pemesanan.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="f9d9a-118">Pilih metode yang sesuai untuk Anda.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="f9d9a-119">Cari sumber daya tersedia</span><span class="sxs-lookup"><span data-stu-id="f9d9a-119">Find available resources</span></span>

1.  <span data-ttu-id="f9d9a-120">Dari daftar **persyaratan pemesanan**, klik kanan pada Pemesanan tak terjadwal dan pilih salah satu dari berikut:</span><span class="sxs-lookup"><span data-stu-id="f9d9a-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="f9d9a-121">Pilih **Temukan ketersediaan-sumber daya saat ini** untuk menemukan sumber daya yang tersedia dari daftar sumber daya di papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="f9d9a-122">Pilih **Temukan ketersediaan - semua sumber daya** untuk menemukan sumber daya yang tersedia dari sumber daya di sistem.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="f9d9a-123">Ketika Anda melakukan ini, filter akan menampilkan pilihan untuk persyaratan pemesanan yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="f9d9a-124">Ketika Anda melihat slot yang tersedia, klik kanan pada slot waktu pada papan jadwal dan pilih **Pesan di sini**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="f9d9a-125">Atau, tarik dan lepaskan persyaratan pemesanan ke slot waktu yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="f9d9a-126">Pesan sumber daya menggunakan tampilan harian dan temukan mana yang pesanannya di bawah target</span><span class="sxs-lookup"><span data-stu-id="f9d9a-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="f9d9a-127">Pada papan jadwal, pilih **Mode Tampilan** dan pilih **hari**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="f9d9a-128">Ini menunjukkan tampilan grid berapa jam sumber daya dipesan per hari dan hari-hari yang mereka bebas.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="f9d9a-129">Klik nama sumber daya yang ingin Anda pesan, dan kemudian pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="f9d9a-130">Pada kotak dialog **Pemesanan sumber daya (membuat)**, pilih proyek yang Anda ingin pesan sumber dayanya bersama dengan metode pemesanan serta waktu mulai dan selesai.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="f9d9a-131">Setelah selesai, pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="f9d9a-132">Lihat papan Jadwal</span><span class="sxs-lookup"><span data-stu-id="f9d9a-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="f9d9a-133">Pilih persyaratan pemesanan tak terjadwal dari daftar di bagian bawah.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="f9d9a-134">Tarik persyaratan pemesanan ke slot sumber daya/waktu yang tersedia di papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="f9d9a-135">Setelah selesai, pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="f9d9a-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="f9d9a-136">Sumber daya tambahan</span><span class="sxs-lookup"><span data-stu-id="f9d9a-136">Additional resources</span></span>  
 [<span data-ttu-id="f9d9a-137">Panduan Manajer Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="f9d9a-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Jadwalkan sumber daya untuk sebuah proyek
description: Cara menjadwalkan sumber daya di Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: db69348aac96cbfaaa865228c9230cbda4b1e784
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078690"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="1a859-103">Jadwalkan sumber daya untuk proyek (Project Service)</span><span class="sxs-lookup"><span data-stu-id="1a859-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="1a859-104">Anda dapat memeriksa ketersediaan sumber untuk mendapatkan pandangan yang menyeluruh tentang sepadat apa tingkat pemesanan sumber daya Anda, atau Anda dapat menyaring tampilan menurut keterampilan, tim, lokasi, dan pilihan lainnya.</span><span class="sxs-lookup"><span data-stu-id="1a859-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="1a859-105">Papan jadwal menunjukkan daftar sumber daya dan ketersediaan mereka.</span><span class="sxs-lookup"><span data-stu-id="1a859-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="1a859-106">Pilih mode tampilan untuk menunjukkan ketersediaan menurut **jam** , **hari** , **minggu** , atau **bulan**.</span><span class="sxs-lookup"><span data-stu-id="1a859-106">Select a view mode to show availability by **Hours** , **Day** , **Week** , or **Month**.</span></span>  
  
<span data-ttu-id="1a859-107">Sebelum Anda menggunakan papan jadwal, sangat penting untuk mengatur itu.</span><span class="sxs-lookup"><span data-stu-id="1a859-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="1a859-108">Untuk informasi lebih lanjut, lihat [Mengkonfigurasi papan jadwal (Field Service atau Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="1a859-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="1a859-109">Jika Anda menggunakan versi yang lebih tua, untuk ketersediaan sumber daya, lihat [Lihat ketersediaan sumber daya](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="1a859-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="1a859-110">Untuk menggunakan fungsionalitas pemesanan papan jadwal, geocoding, dan Layanan lokasi, Anda perlu mengaktifkan peta.</span><span class="sxs-lookup"><span data-stu-id="1a859-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="1a859-111">Di menu utama, pilih **Penjadwalan Sumber daya** > **Administrasi**.</span><span class="sxs-lookup"><span data-stu-id="1a859-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="1a859-112">Klik **Parameter Penjadwalan**.</span><span class="sxs-lookup"><span data-stu-id="1a859-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="1a859-113">Buka rekaman dan gulir ke bawah ke bagian **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="1a859-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="1a859-114">Pada bidang **Sambung ke Maps** , pilih **ya**.</span><span class="sxs-lookup"><span data-stu-id="1a859-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="1a859-115">Tnerima persyaratan dan simpan rekaman.</span><span class="sxs-lookup"><span data-stu-id="1a859-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="1a859-116">Di menu utama, pilih **Project Service** > **papan jadwal**.</span><span class="sxs-lookup"><span data-stu-id="1a859-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="1a859-117">Dari sini, ada beberapa cara untuk secara manual menjadwalkan persyaratan pemesanan.</span><span class="sxs-lookup"><span data-stu-id="1a859-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="1a859-118">Pilih metode yang sesuai untuk Anda.</span><span class="sxs-lookup"><span data-stu-id="1a859-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="1a859-119">Cari sumber daya tersedia</span><span class="sxs-lookup"><span data-stu-id="1a859-119">Find available resources</span></span>

1.  <span data-ttu-id="1a859-120">Dari daftar **persyaratan pemesanan** , klik kanan pada Pemesanan tak terjadwal dan pilih salah satu dari berikut:</span><span class="sxs-lookup"><span data-stu-id="1a859-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="1a859-121">Pilih **Temukan ketersediaan-sumber daya saat ini** untuk menemukan sumber daya yang tersedia dari daftar sumber daya di papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="1a859-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="1a859-122">Pilih **Temukan ketersediaan - semua sumber daya** untuk menemukan sumber daya yang tersedia dari sumber daya di sistem.</span><span class="sxs-lookup"><span data-stu-id="1a859-122">Choose **Find availability - All Resources** , to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="1a859-123">Ketika Anda melakukan ini, filter akan menampilkan pilihan untuk persyaratan pemesanan yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="1a859-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="1a859-124">Ketika Anda melihat slot yang tersedia, klik kanan pada slot waktu pada papan jadwal dan pilih **Pesan di sini**.</span><span class="sxs-lookup"><span data-stu-id="1a859-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="1a859-125">Atau, tarik dan lepaskan persyaratan pemesanan ke slot waktu yang tersedia.</span><span class="sxs-lookup"><span data-stu-id="1a859-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="1a859-126">Pesan sumber daya menggunakan tampilan harian dan temukan mana yang pesanannya di bawah target</span><span class="sxs-lookup"><span data-stu-id="1a859-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="1a859-127">Pada papan jadwal, pilih **Mode Tampilan** dan pilih **hari**.</span><span class="sxs-lookup"><span data-stu-id="1a859-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="1a859-128">Ini menunjukkan tampilan grid berapa jam sumber daya dipesan per hari dan hari-hari yang mereka bebas.</span><span class="sxs-lookup"><span data-stu-id="1a859-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="1a859-129">Klik nama sumber daya yang ingin Anda pesan, dan kemudian pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="1a859-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="1a859-130">Pada kotak dialog **Pemesanan sumber daya (membuat)** , pilih proyek yang Anda ingin pesan sumber dayanya bersama dengan metode pemesanan serta waktu mulai dan selesai.</span><span class="sxs-lookup"><span data-stu-id="1a859-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="1a859-131">Setelah selesai, pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="1a859-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="1a859-132">Lihat papan Jadwal</span><span class="sxs-lookup"><span data-stu-id="1a859-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="1a859-133">Pilih persyaratan pemesanan tak terjadwal dari daftar di bagian bawah.</span><span class="sxs-lookup"><span data-stu-id="1a859-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="1a859-134">Tarik persyaratan pemesanan ke slot sumber daya/waktu yang tersedia di papan jadwal.</span><span class="sxs-lookup"><span data-stu-id="1a859-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="1a859-135">Setelah selesai, pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="1a859-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="1a859-136">Sumber daya tambahan</span><span class="sxs-lookup"><span data-stu-id="1a859-136">Additional resources</span></span>  
 [<span data-ttu-id="1a859-137">Panduan Manajer Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="1a859-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)

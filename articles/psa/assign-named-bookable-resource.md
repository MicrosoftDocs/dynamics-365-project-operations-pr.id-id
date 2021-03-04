---
title: Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas
description: Topik ini menyediakan informasi tentang cara pemesanan sumber daya bernama untuk tim proyek dan menetapkan tugas.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: d8a49b6ae8423cb99c710e40704475b4a71d3724
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145362"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="52b48-103">Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas</span><span class="sxs-lookup"><span data-stu-id="52b48-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="52b48-104">Anda dapat menambahkan sumber daya bernama ke tim proyek Anda dengan memesan secara langsung ke tim.</span><span class="sxs-lookup"><span data-stu-id="52b48-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="52b48-105">Untuk melakukannya, selesaikan langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="52b48-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="52b48-106">Di Project Service Automation, buka **proyek**, lalu pilih proyek yang terbuka yang Anda lakukan saat pemesanan.</span><span class="sxs-lookup"><span data-stu-id="52b48-106">In  Project Service Automation, go to **Projects**, and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="52b48-107">Pada halaman **proyek**, pada tab **tim**, klik **baru**.</span><span class="sxs-lookup"><span data-stu-id="52b48-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Menambahkan anggota tim dari tab tim](media/RM-how-to-1.png)

3. <span data-ttu-id="52b48-109">Di kotak dialog **Buat Cepat anggota tim proyek**, pilih sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="52b48-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="52b48-110">Bidang **peran** akan terisi dengan peran default sumber daya jika telah ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="52b48-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="52b48-111">Anda dapat mengubah peran jika diperlukan.</span><span class="sxs-lookup"><span data-stu-id="52b48-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="52b48-112">Pilih tanggal dari dan hingga untuk kebutuhan sumber daya dan pilih metode alokasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="52b48-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="52b48-113">Jika Anda ingin agar anggota tim menjadi pemberi izin proyek, Pilih **ya** di bidang **pemberi izin proyek**.</span><span class="sxs-lookup"><span data-stu-id="52b48-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="52b48-114">Ini akan berarti bahwa anggota tim dapat menyetujui entri waktu dan biaya yang diajukan untuk proyek ini.</span><span class="sxs-lookup"><span data-stu-id="52b48-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="52b48-115">Klik **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="52b48-115">Click **Save**.</span></span>

![Menambahkan anggota tim pada formulir pembuatan cepat](media/RM-how-to-2.png)


<span data-ttu-id="52b48-117">Anda sekarang dapat menetapkan sumber daya yang dipesan untuk tugas pada proyek.</span><span class="sxs-lookup"><span data-stu-id="52b48-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="52b48-118">Pada halaman **proyek**, klik tab **jadwal** untuk menetapkan tugas ke sumber daya baru.</span><span class="sxs-lookup"><span data-stu-id="52b48-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="52b48-119">Pemilih sumber daya yang diluncurkan dari bidang **sumber daya** di kisi tugas akan menampilkan anggota tim yang dapat Anda pilih.</span><span class="sxs-lookup"><span data-stu-id="52b48-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Menetapkan anggota tim ke tugas pada tab jadwal](media/RM-how-to-3.png)

<span data-ttu-id="52b48-121">Dalam versi 3 untuk Project Service Automation (PSA), Pemesanan sumber daya dan penetapan tugas tidak digabungkan dengan ketat.</span><span class="sxs-lookup"><span data-stu-id="52b48-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="52b48-122">Ini berarti bahwa saat Anda menggunakan pemilih sumber daya dalam jadwal, Anda dapat menetapkan tugas untuk anggota tim lebih lama dibandingkan Pemesanan mereka tercakup dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="52b48-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="52b48-123">Anda dapat melihat perbedaan antara Pemesanan anggota tim dan tugas pada tab **tim** atau pada tab **rekonsiliasi sumber daya**. Anda juga dapat mendamaikan perbedaan antara Pemesanan dan tugas untuk sumber daya dengan tingkat yang lebih rinci.</span><span class="sxs-lookup"><span data-stu-id="52b48-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Tab rekonsiliasi Sumber Daya](media/RM-how-to-4.png)

<span data-ttu-id="52b48-125">Anda juga dapat menggunakan pemilih sumber daya pada tab **jadwal** untuk mencari dan memilih sumber daya yang dapat dipesan yang belum menjadi bagian dari tim proyek.</span><span class="sxs-lookup"><span data-stu-id="52b48-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="52b48-126">Ini ditampilkan dalam pemilih sumber daya sebagai **sumber daya lainnya**.</span><span class="sxs-lookup"><span data-stu-id="52b48-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Menetapkan sumber daya anggota non-tim ke tugas](media/RM-how-to-5.png)

<span data-ttu-id="52b48-128">Bila Anda melakukannya, sumber daya akan ditambahkan ke tim proyek dan ditetapkan ke tugas, namun tidak ada Pemesanan yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="52b48-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Anggota tim dengan tugas dan tanpa Pemesanan](media/RM-how-to-6.png)

<span data-ttu-id="52b48-130">Anda dapat menggunakan tab **rekonsiliasi** untuk memperluas kemampuan Pemesanan atau **papan jadwal** untuk memesan kapasitas sumber daya ke proyek.</span><span class="sxs-lookup"><span data-stu-id="52b48-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Memperluas Pemesanan untuk anggota tim pada tab rekonsiliasi sumber daya](media/RM-how-to-7.png)

<span data-ttu-id="52b48-132">Setelah anggota tim dipesan pada proyek Anda, Anda dapat menggunakan memelihara Pemesanan atau menggunakan papan jadwal secara langsung untuk mengelola Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="52b48-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>

---
title: Mengelola anggota tim
description: Topik ini menyediakan informasi tentang pemesanan sumber daya bernama untuk tim proyek dan tetapkan tugas.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: f5b36628e90896c9fe6570de71c95eab83a44ebd
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078350"
---
# <a name="maintain-team-members"></a><span data-ttu-id="c65bf-103">Mengelola anggota tim</span><span class="sxs-lookup"><span data-stu-id="c65bf-103">Maintain team members</span></span>

<span data-ttu-id="c65bf-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="c65bf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c65bf-105">Anda dapat menambahkan sumber daya bernama ke tim proyek Anda dengan memesan secara langsung ke tim.</span><span class="sxs-lookup"><span data-stu-id="c65bf-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="c65bf-106">Di Dynamics 365 Project Operations, buka **proyek** , lalu pilih proyek yang terbuka yang Anda lakukan pemesanannya.</span><span class="sxs-lookup"><span data-stu-id="c65bf-106">In Dynamics 365 Project Operations, go to **Projects** , and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="c65bf-107">Pada halaman **proyek** , pada tab **tim** , pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="c65bf-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="c65bf-108">Di kotak dialog **Buat Cepat anggota tim proyek** , pilih sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="c65bf-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="c65bf-109">Bidang **peran** akan terisi dengan peran default sumber daya jika telah ditugaskan.</span><span class="sxs-lookup"><span data-stu-id="c65bf-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="c65bf-110">Anda dapat mengubah peran.</span><span class="sxs-lookup"><span data-stu-id="c65bf-110">You can change the role.</span></span> 
4. <span data-ttu-id="c65bf-111">Pilih tanggal dari dan hingga untuk kebutuhan sumber daya dan pilih metode alokasi kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="c65bf-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="c65bf-112">Jika Anda ingin agar anggota tim menjadi pemberi persetujuan proyek, Pilih **ya** di bidang **pemberi persetujuan proyek**.</span><span class="sxs-lookup"><span data-stu-id="c65bf-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="c65bf-113">Anggota tim dapat menyetujui entri waktu dan biaya yang diajukan untuk proyek ini.</span><span class="sxs-lookup"><span data-stu-id="c65bf-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="c65bf-114">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="c65bf-114">Select **Save**.</span></span>

<span data-ttu-id="c65bf-115">Anda sekarang dapat menetapkan sumber daya yang dipesan untuk tugas pada proyek.</span><span class="sxs-lookup"><span data-stu-id="c65bf-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="c65bf-116">Pada halaman **proyek** , di tab **jadwal** , tetapkan tugas ke sumber daya baru.</span><span class="sxs-lookup"><span data-stu-id="c65bf-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="c65bf-117">Pemilih sumber daya yang diluncurkan dari bidang **sumber daya** di kisi tugas akan menampilkan anggota tim yang dapat Anda pilih.</span><span class="sxs-lookup"><span data-stu-id="c65bf-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="c65bf-118">Dalam Project Operations, Pemesanan sumber daya, dan penetapan tugas tidak digabungkan dengan ketat.</span><span class="sxs-lookup"><span data-stu-id="c65bf-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="c65bf-119">Saat Anda menggunakan pemilih sumber daya dalam jadwal, Anda dapat menetapkan tugas untuk anggota tim lebih lama dibandingkan Pemesanan mereka tercakup dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="c65bf-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="c65bf-120">Perbedaan antara Pemesanan anggota tim dan penetapan ditampilkan pada tab **tim** dan **rekonsiliasi sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="c65bf-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="c65bf-121">Anda juga dapat mendamaikan perbedaan antara Pemesanan dan tugas untuk sumber daya dengan tingkat yang lebih rinci.</span><span class="sxs-lookup"><span data-stu-id="c65bf-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="c65bf-122">Gunakan pemilih sumber daya pada tab **jadwal** untuk mencari dan memilih sumber daya yang dapat dipesan yang belum menjadi bagian dari tim proyek.</span><span class="sxs-lookup"><span data-stu-id="c65bf-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="c65bf-123">Sumber daya ini ditampilkan dalam pemilih sumber daya sebagai **sumber daya lainnya**.</span><span class="sxs-lookup"><span data-stu-id="c65bf-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="c65bf-124">Saat Anda menentukan pilihan, sumber daya akan ditambahkan ke tim proyek dan ditetapkan ke tugas, namun tidak ada Pemesanan yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="c65bf-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="c65bf-125">Anda dapat menggunakan tab **rekonsiliasi** untuk memperluas kemampuan Pemesanan atau **papan jadwal** untuk memesan kapasitas sumber daya ke proyek.</span><span class="sxs-lookup"><span data-stu-id="c65bf-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="c65bf-126">Setelah anggota tim dipesan pada proyek Anda, Anda dapat menggunakan **memelihara Pemesanan** atau **papan jadwal** secara langsung untuk mengelola Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="c65bf-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>

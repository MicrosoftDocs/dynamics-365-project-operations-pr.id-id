---
title: Tinjau sumber daya yang diusulkan
description: Topik ini menyediakan informasi tentang cara mengusulkan sumber daya proyek.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401177"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="0b581-103">Tinjau sumber daya yang diusulkan</span><span class="sxs-lookup"><span data-stu-id="0b581-103">Review proposed resources</span></span>

<span data-ttu-id="0b581-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="0b581-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0b581-105">Manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek menggunakan permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="0b581-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="0b581-106">Dari kisi permintaan atau permintaan itu sendiri, pilih **Cari sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="0b581-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="0b581-107">Di halaman **asisten jadwal**, pilih sumber daya, lalu di panel **buat Pemesanan sumber daya**, di bidang **status Pemesanan**, pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="0b581-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="0b581-108">Terjadi pembaruan status berikut:</span><span class="sxs-lookup"><span data-stu-id="0b581-108">The following status updates occur:</span></span>

- <span data-ttu-id="0b581-109">Di halaman **asisten jadwal**, indikator status diperbarui untuk menunjukkan bahwa Pemesanan diajukan, bukan pesanan definitif.</span><span class="sxs-lookup"><span data-stu-id="0b581-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="0b581-110">Pada permintaan sumber daya, status berubah menjadi **perlu ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="0b581-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="0b581-111">Pada tab **tim** proyek , nilai **status permintaan** anggota tim generik diubah ke **perlu ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="0b581-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="0b581-112">Manajer proyek dapat menerima atau menolak usulan tersebut.</span><span class="sxs-lookup"><span data-stu-id="0b581-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="0b581-113">Bila manajer sumber daya memproses permintaan sumber daya, mereka dapat menggunakan salah satu dari pendekatan berikut:</span><span class="sxs-lookup"><span data-stu-id="0b581-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="0b581-114">Mengusulkan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0b581-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="0b581-115">Jam yang diusulkan kemudian dipecah di antara beberapa sumber daya yang dapat memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0b581-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="0b581-116">Dalam skenario ini, jam tidak dapat tumpang tindih.</span><span class="sxs-lookup"><span data-stu-id="0b581-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="0b581-117">Mengusulkan sumber daya yang lebih sedikit daripada yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0b581-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="0b581-118">Dalam skenario ini, kapasitas sumber daya yang diusulkan kurang dari jam yang diperlukan yang ditentukan pemohon.</span><span class="sxs-lookup"><span data-stu-id="0b581-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="0b581-119">Oleh karena itu, bila pemohon menerima sumber daya yang diusulkan, persyaratan sumber daya yang tidak terpenuhi dibuat untuk merekam permintaan yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="0b581-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="0b581-120">Memesan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk menyelesaikan pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="0b581-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="0b581-121">Memesan sumber daya yang lebih sedikit daripada yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0b581-121">Book fewer resources than are required.</span></span> <span data-ttu-id="0b581-122">Dalam skenario ini, jam yang dipesan kurang dari jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="0b581-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="0b581-123">Sistem akan memandu Anda mengajukan sumber daya dan bukan Pemesanan, sehingga pemohon dapat memverifikasi dan melacak permintaan yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="0b581-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="0b581-124">Ketersediaan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="0b581-124">Resource availability</span></span>

<span data-ttu-id="0b581-125">Sangat penting bagi manajer sumber daya untuk dapat melihat ketersediaan sumber daya dan memperbarui Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="0b581-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="0b581-126">Dalam kasus tertentu, tidak ada permintaan formal (permintaan sumber daya), namun manajer sumber daya harus merespons permintaan yang tidak direncanakan yang berasal dari saluran seperti email, panggilan telepon, atau pesan instan.</span><span class="sxs-lookup"><span data-stu-id="0b581-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="0b581-127">Manajer sumber daya menggunakan papan jadwal untuk memperbarui sumber daya dan Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="0b581-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="0b581-128">Jam kerja sumber daya digunakan sebagai dasar untuk menghitung ketersediaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="0b581-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="0b581-129">Pemesanan sumber daya menghabiskan kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="0b581-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="0b581-130">Papan jadwal menggunakan warna dan arsiran untuk menampilkan Pemesanan, ketersediaan, dan pesanan berlebihan, dan juga status pemesanan.</span><span class="sxs-lookup"><span data-stu-id="0b581-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="0b581-131">Pengaturan di pengaturan papan jadwal memungkinkan Anda menampilkan legenda.</span><span class="sxs-lookup"><span data-stu-id="0b581-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="0b581-132">Jika tanda panah menunjuk ke kanan muncul di samping sumber daya yang dapat dipesan individual pada papan jadwal, sumber daya dapat diperluas untuk menampilkan rincian pekerjaan yang dipesan sumber dayanya.</span><span class="sxs-lookup"><span data-stu-id="0b581-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="0b581-133">Karena Dynamics 365 Project Operations menggunakan mesin Universal Resource Scheduling, jika Anda juga telah menginstal Dynamics 365 Field Service, Anda dapat melihat rincian pemesanan sumber daya untuk proyek, perintah kerja, dan entitas lain yang telah Anda gunakan untuk memperpanjang penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="0b581-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="0b581-134">Untuk melihat rincian lebih lanjut tentang sumber daya individual, klik kanan untuk membuka kartu sumber daya.</span><span class="sxs-lookup"><span data-stu-id="0b581-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>


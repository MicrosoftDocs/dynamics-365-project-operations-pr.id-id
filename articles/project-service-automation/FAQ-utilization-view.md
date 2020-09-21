---
title: Lihat pemanfaatan sumber daya yang dikenakan biaya
description: Topik ini menyediakan informasi tentang tampilan pemanfaatan sumber daya.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752384"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="16351-103">Lihat pemanfaatan sumber daya yang dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="16351-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="16351-104">**Tampilan pemanfaatan** pada halaman **pemanfaatan sumber daya Project Service** menampilkan pemanfaatan yang dikenai biaya untuk setiap sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="16351-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="16351-105">Karena tampilan didasarkan pada papan jadwal, Anda akan menemukan banyak fungsi yang sama.</span><span class="sxs-lookup"><span data-stu-id="16351-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Tangkapan layar tampilan pemanfaatan](media/FAQ-utilization-1.png)
 

<span data-ttu-id="16351-107">Perhitungan pemanfaatan dikenakan biaya berfungsi sebagai berikut:</span><span class="sxs-lookup"><span data-stu-id="16351-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="16351-108">Pemanfaatan dikenakan biaya = (Jam aktual kena biaya)/(kapasitas sumber daya )</span><span class="sxs-lookup"><span data-stu-id="16351-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="16351-109">Sel menyatakan pemanfaatan dikenakan biaya dihitung selama periode yang dipilih (hari, Minggu, atau bulan).</span><span class="sxs-lookup"><span data-stu-id="16351-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="16351-110">Warna dalam setiap sel menampilkan pemanfaatan sumber daya dikenakan biaya dibandingkan dengan pemanfaatan dikenakan biaya target mereka.</span><span class="sxs-lookup"><span data-stu-id="16351-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="16351-111">Pemanfaatan target dapat mengatur default peran sumber daya atau pada masing-masing sumber daya itu sendiri.</span><span class="sxs-lookup"><span data-stu-id="16351-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="16351-112">Perhitungan terlihat pada individual untuk target pertama, lalu default peran sumber daya.</span><span class="sxs-lookup"><span data-stu-id="16351-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="16351-113">Menetapkan target pada sumber daya</span><span class="sxs-lookup"><span data-stu-id="16351-113">Set target on a resource</span></span>

1. <span data-ttu-id="16351-114">Buka **Sumber Daya** \> **Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="16351-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="16351-115">Pilih sumber daya untuk membuka rekaman.</span><span class="sxs-lookup"><span data-stu-id="16351-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="16351-116">Di tab **Project Service**, Anda dapat mengatur pemanfaatan target sumber daya.</span><span class="sxs-lookup"><span data-stu-id="16351-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Tangkapan layar menggunakan tab Project Service untuk menetapkan target pemanfaatan](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="16351-118">Menetapkan target pemanfaatan peran</span><span class="sxs-lookup"><span data-stu-id="16351-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="16351-119">Buka **Sumber Daya** \> **Peran Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="16351-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="16351-120">Pilih peran dan buka rekaman.</span><span class="sxs-lookup"><span data-stu-id="16351-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="16351-121">Atur pemanfaatan target untuk peran.</span><span class="sxs-lookup"><span data-stu-id="16351-121">Set the target utilization for the role.</span></span>

> ![Tangkapan layar menggunakan peran sumber daya untuk menetapkan target pemanfaatan](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="16351-123">Hitung pemanfaatan yang dikenakan biaya untuk sumber daya</span><span class="sxs-lookup"><span data-stu-id="16351-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="16351-124">Menghitung pemanfaatan sumber daya yang bisa ditagih, Anda harus menyelesaikan beberapa prasyarat.</span><span class="sxs-lookup"><span data-stu-id="16351-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="16351-125">Mengatur peran default untuk sumber daya individual</span><span class="sxs-lookup"><span data-stu-id="16351-125">Set default role for individual resource</span></span>

<span data-ttu-id="16351-126">Pertama, Pemanfaatan target harus diatur di sumber daya individual atau pada peran sumber daya.</span><span class="sxs-lookup"><span data-stu-id="16351-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="16351-127">Jika Anda menggunakan peran sumber daya untuk target, setiap sumber daya individual harus memiliki peran default.</span><span class="sxs-lookup"><span data-stu-id="16351-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="16351-128">Untuk menetapkan ini, buka **sumber daya** \> **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="16351-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="16351-129">Pilih sumber daya, buka rekaman, lalu pilih tab **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="16351-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="16351-130">Di kisi **peran sumber daya**, pastikan ada satu peran untuk sumber daya dan **Is Default** diatur ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="16351-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="16351-131">Ubah jenis penagihan untuk peran sumber daya</span><span class="sxs-lookup"><span data-stu-id="16351-131">Change billing type for resource role</span></span>

<span data-ttu-id="16351-132">Peran sumber daya harus diatur untuk memiliki jenis penagihan **dikenakan biaya**.</span><span class="sxs-lookup"><span data-stu-id="16351-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="16351-133">Buka **Sumber Daya** \> **Peran Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="16351-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="16351-134">Buka rekaman yang ingin diperbarui, kemudian tetapkan jenis penagihan default ke **Dikenakan biaya**.</span><span class="sxs-lookup"><span data-stu-id="16351-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="16351-135">Mengatur jam kerja untuk peran sumber daya</span><span class="sxs-lookup"><span data-stu-id="16351-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="16351-136">Sumber daya harus memiliki jam kerja untuk perhitungan kapasitas.</span><span class="sxs-lookup"><span data-stu-id="16351-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="16351-137">Buka **Sumber Daya** \> **Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="16351-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="16351-138">Pilih sumber daya untuk membuka rekaman, lalu pilih **Tampilkan Jam Kerja**.</span><span class="sxs-lookup"><span data-stu-id="16351-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="16351-139">Anda dapat melakukan pembaruan massal daftar sumber daya dengan menerapkan **Template jam kerja** dari tampilan **daftar sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="16351-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="16351-140">Mengatasi masalah jam aktual kena biaya</span><span class="sxs-lookup"><span data-stu-id="16351-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="16351-141">Jam aktual dikenakan biaya bersumber dari entitas **aktual**.</span><span class="sxs-lookup"><span data-stu-id="16351-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="16351-142">Nilai aktual dengan jenis penagihan **dikenakan biaya** tercakup dalam perhitungan ini, dan untuk alasan ini, Anda harus memiliki proyek dengan nilai aktual dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="16351-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="16351-143">Jika Anda tidak melihat pemanfaatan dikenakan biaya, berikut adalah beberapa hal yang Anda dapat memeriksa:</span><span class="sxs-lookup"><span data-stu-id="16351-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="16351-144">Sumber daya memiliki jam kerja yang ditentukan untuk kapasitas.</span><span class="sxs-lookup"><span data-stu-id="16351-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="16351-145">Sumber daya memiliki target pemanfaatan yang ditentukan secara individual atau memiliki peran default yang ditetapkan ke dalamnya.</span><span class="sxs-lookup"><span data-stu-id="16351-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="16351-146">Peran memiliki target pemanfaatan yang ditentukan untuk itu.</span><span class="sxs-lookup"><span data-stu-id="16351-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="16351-147">Nilai aktual memiliki jenis penagihan **dikenakan biaya** selama periode yang Anda harapkan perhitungan pemanfaatannya.</span><span class="sxs-lookup"><span data-stu-id="16351-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="16351-148">Periksa yang berikut ini jika Anda melihat nilai aktual dengan tagihan jenis selain dikenakan biaya:</span><span class="sxs-lookup"><span data-stu-id="16351-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="16351-149">Peran yang digunakan di aktual memiliki jenis default penagihan sesuatu selain dari dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="16351-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="16351-150">Peran pada baris kontrak proyek yang mendukung proyek telah ditetapkan untuk tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="16351-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="16351-151">Proyek tidak memiliki baris kontrak terkait.</span><span class="sxs-lookup"><span data-stu-id="16351-151">The project does not have an associated contract line.</span></span>


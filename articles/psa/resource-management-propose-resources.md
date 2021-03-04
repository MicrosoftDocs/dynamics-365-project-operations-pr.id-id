---
title: Mengusulkan sumber daya proyek
description: Topik ini menyediakan informasi tentang mengusulkan sumber daya proyek.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 0a3eaa9929770c91523831d92744d5084aa28cb8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147522"
---
# <a name="propose-project-resources"></a><span data-ttu-id="bf4ac-103">Mengusulkan sumber daya proyek</span><span class="sxs-lookup"><span data-stu-id="bf4ac-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="bf4ac-104">Manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek menggunakan permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="bf4ac-105">Dari kisi permintaan atau permintaan itu sendiri, pilih **Cari sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="bf4ac-106">Di halaman **asisten jadwal**, pilih sumber daya, lalu di panel **buat Pemesanan sumber daya**, di bidang **status Pemesanan**, pilih **Pesan**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Sumber daya yang diusulkan dipilih](media/Resource-Management-image62.png)

<span data-ttu-id="bf4ac-108">Terjadi pembaruan status berikut:</span><span class="sxs-lookup"><span data-stu-id="bf4ac-108">The following status updates occur:</span></span>

- <span data-ttu-id="bf4ac-109">Di halaman **asisten jadwal**, indikator status diperbarui untuk menunjukkan bahwa Pemesanan diajukan, bukan pesanan definitif.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indikator status untuk usulan Pemesanan pada halaman asisten jadwal](media/Resource-Management-image63.png)

- <span data-ttu-id="bf4ac-111">Pada permintaan sumber daya, status berubah menjadi **perlu ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Status permintaan sumber daya berubah menjadi perlu ditinjau](media/Resource-Management-image64.png)

- <span data-ttu-id="bf4ac-113">Pada tab **tim** proyek , nilai **status permintaan** anggota tim generik diubah ke **perlu ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Status permintaan anggota tim generik diubah ke perlu ditinjau di tab Tim.](media/Resource-Management-image48.png)

<span data-ttu-id="bf4ac-115">Manajer proyek dapat menerima atau menolak usulan tersebut.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="bf4ac-116">Bila manajer sumber daya memproses permintaan sumber daya, mereka dapat menggunakan salah satu dari pendekatan berikut:</span><span class="sxs-lookup"><span data-stu-id="bf4ac-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="bf4ac-117">Mengusulkan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="bf4ac-118">Jam yang diusulkan kemudian dipecah di antara beberapa sumber daya yang dapat memenuhi jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="bf4ac-119">Dalam skenario ini, jam tidak dapat tumpang tindih.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="bf4ac-120">Mengusulkan sumber daya yang lebih sedikit daripada yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="bf4ac-121">Dalam skenario ini, kapasitas sumber daya yang diusulkan kurang dari jam yang diperlukan yang ditentukan pemohon.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="bf4ac-122">Oleh karena itu, bila pemohon menerima sumber daya yang diusulkan, persyaratan sumber daya yang tidak terpenuhi dibuat untuk merekam permintaan yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="bf4ac-123">Memesan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk menyelesaikan pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="bf4ac-124">Memesan sumber daya yang lebih sedikit daripada yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-124">Book fewer resources than are required.</span></span> <span data-ttu-id="bf4ac-125">Dalam skenario ini, jam yang dipesan kurang dari jam yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="bf4ac-126">Sistem akan memandu Anda mengajukan sumber daya dan bukan Pemesanan, sehingga pemohon dapat memverifikasi dan melacak permintaan yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="bf4ac-127">Pemanfaatan yang dapat ditagih</span><span class="sxs-lookup"><span data-stu-id="bf4ac-127">Billable utilization</span></span>

<span data-ttu-id="bf4ac-128">Sumber daya dapat memiliki pemanfaatan yang dapat ditagih.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="bf4ac-129">Pemanfaatan target ini didefinisikan sebagai atribut pada peran default sumber daya atau diatur pada rekaman sumber daya yang dapat dipesan individual.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="bf4ac-130">Penghitungan pemanfaatan didasarkan pada jam aktual yang dilaporkan sumber daya menggunakan entri waktu yang disetujui.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="bf4ac-131">Rumus berikut digunakan untuk menghitung pemanfaatan:</span><span class="sxs-lookup"><span data-stu-id="bf4ac-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="bf4ac-132">Pemanfaatan dapat ditagih = Jam aktual dapat ditagih ÷ kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="bf4ac-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="bf4ac-133">Pemanfaatan tidak dapat ditagih = waktu aktual dengan ID jenis penagihan = tidak dikenakan biaya, gratis, atau tidak tersedia ÷ kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="bf4ac-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="bf4ac-134">Internal = waktu aktual tanpa kontrak penjualan ÷ kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="bf4ac-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="bf4ac-135">Kapasitas sumber daya = jam kerja sumber daya – izin absen – hari tidak bekerja</span><span class="sxs-lookup"><span data-stu-id="bf4ac-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="bf4ac-136">Anda dapat menemukan tampilan **pemanfaatan sumber daya** di panel **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Tampilan pemanfaatan sumber daya](media/Resource-Management-image65.png)

<span data-ttu-id="bf4ac-138">Setiap sel di kisi mewakili persentase pemanfaatan yang dapat ditagih dari sumber daya dalam periode tertentu, seperti hari, pekan atau bulan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="bf4ac-139">Rumus berikut digunakan untuk mewarnai sel:</span><span class="sxs-lookup"><span data-stu-id="bf4ac-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="bf4ac-140">**Hijau:** Pemanfaatan yang ditagih \>= pemanfaatan sumber daya target</span><span class="sxs-lookup"><span data-stu-id="bf4ac-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="bf4ac-141">**Kuning:** target pemanfaatan – 20 \<= pemanfaatan ditagih \< target pemanfaatan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="bf4ac-142">**mérah:** Pemanfaatan yang ditagih \< pemanfaatan target – 20.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="bf4ac-143">Karena tampilan **pemanfaatan sumber daya** didasarkan pada papan jadwal, Anda dapat menggunakan kemampuan pemfilteran papan jadwal untuk memfilter hasil.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="bf4ac-144">Kisi-kisi mengharuskan Anda menetapkan Pemanfaatan peran atau sumber daya individual.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="bf4ac-145">Untuk melakukan konfigurasi ini, buka **sumber daya** \> **peran sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="bf4ac-146">Selain itu, peran default harus ditetapkan ke setiap sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="bf4ac-147">Buka **Sumber Daya** \> **Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="bf4ac-148">Pada tab **Project Service**, periksa apakah peran sumber daya ditentukan, dan bidang **merupakan default** untuk diatur ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="bf4ac-149">Anda dapat menambahkan peran tambahan di mana **merupakan default = Tidak**.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="bf4ac-150">Peran jika **merupakan default = Ya** digunakan untuk mengevaluasi pemanfaatan sumber daya terhadap target untuk peran tersebut.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Set Peran Default](media/Resource-Management-image67.png)

<span data-ttu-id="bf4ac-152">Di tab **Project Service**, Anda juga dapat menetapkan pemanfaatan target individual untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="bf4ac-153">Perhitungan pemanfaatan kemudian menggunakan pemanfaatan target untuk mengevaluasi target sumber daya bukan target dari peran default sumber daya.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="bf4ac-154">Pemanfaatan ditampilkan untuk sumber daya hanya jika sumber daya telah disetujui, waktu yang dapat ditagih selama periode yang ditampilkan di kisi.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="bf4ac-155">Ketersediaan Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="bf4ac-155">Resource availability</span></span>

<span data-ttu-id="bf4ac-156">Sangat penting bagi manajer sumber daya untuk dapat melihat ketersediaan sumber daya dan memperbarui Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="bf4ac-157">Dalam kasus tertentu, tidak ada permintaan formal (permintaan sumber daya), namun manajer sumber daya harus merespons permintaan yang tidak direncanakan yang berasal dari saluran seperti email, panggilan telepon, atau pesan instan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="bf4ac-158">Manajer sumber daya menggunakan papan jadwal untuk memperbarui sumber daya dan Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="bf4ac-159">Jam kerja sumber daya digunakan sebagai dasar untuk menghitung ketersediaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="bf4ac-160">Pemesanan sumber daya menghabiskan kapasitas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-160">Resource bookings consume the capacity of the resources.</span></span>

![Papan Jadwal](media/Resource-Management-image68.png)

<span data-ttu-id="bf4ac-162">Papan jadwal menggunakan warna dan arsiran untuk menampilkan Pemesanan, ketersediaan, dan pesanan berlebihan, dan juga status pemesanan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="bf4ac-163">Pengaturan di pengaturan papan jadwal memungkinkan Anda menampilkan legenda.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="bf4ac-164">Jika tanda panah menunjuk ke kanan muncul di samping sumber daya yang dapat dipesan individual pada papan jadwal, sumber daya dapat diperluas untuk menampilkan rincian pekerjaan yang dipesan sumber dayanya.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Sumber daya yang dapat dipesan diperluas di papan jadwal](media/Resource-Management-image69.png)

<span data-ttu-id="bf4ac-166">Karena Dynamics 365 Project Service Automation menggunakan mesin Universal Resource Scheduling, jika Anda juga telah menginstal Dynamics 365 Field Service, Anda dapat melihat rincian pemesanan sumber daya untuk proyek, perintah kerja, dan entitas lain yang telah Anda gunakan untuk memperpanjang penjadwalan.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Rincian pemesanan sumber daya untuk proyek dan perintah kerja](media/Resource-Management-image70.png)

<span data-ttu-id="bf4ac-168">Untuk melihat rincian lebih lanjut tentang sumber daya individual, klik kanan untuk membuka kartu sumber daya.</span><span class="sxs-lookup"><span data-stu-id="bf4ac-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Kartu Sumber Daya](media/Resource-Management-image71.png)

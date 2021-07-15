---
title: Ikhtisar pemanfaatan sumber daya
description: Topik ini menyediakan informasi tentang tampilan pemanfaatan sumber daya di Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367940"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="91d48-103">Ikhtisar pemanfaatan sumber daya</span><span class="sxs-lookup"><span data-stu-id="91d48-103">Resource utilization overview</span></span>

<span data-ttu-id="91d48-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="91d48-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="91d48-105">Sumber daya dapat memiliki pemanfaatan yang dapat ditagih.</span><span class="sxs-lookup"><span data-stu-id="91d48-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="91d48-106">Pemanfaatan target ini didefinisikan sebagai atribut pada peran default sumber daya atau diatur pada rekaman sumber daya yang dapat dipesan individual.</span><span class="sxs-lookup"><span data-stu-id="91d48-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="91d48-107">Penghitungan pemanfaatan didasarkan pada jam aktual yang dilaporkan sumber daya menggunakan entri waktu yang disetujui.</span><span class="sxs-lookup"><span data-stu-id="91d48-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="91d48-108">Rumus berikut digunakan untuk menghitung pemanfaatan:</span><span class="sxs-lookup"><span data-stu-id="91d48-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="91d48-109">Pemanfaatan dapat ditagih = Jam aktual dapat ditagih ÷ kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="91d48-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="91d48-110">Pemanfaatan tidak dapat ditagih = waktu aktual dengan ID jenis penagihan = tidak dikenakan biaya, gratis, atau tidak tersedia ÷ kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="91d48-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="91d48-111">Internal = waktu aktual tanpa kontrak penjualan ÷ kapasitas sumber daya</span><span class="sxs-lookup"><span data-stu-id="91d48-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="91d48-112">Kapasitas sumber daya = jam kerja sumber daya – izin absen – hari tidak bekerja</span><span class="sxs-lookup"><span data-stu-id="91d48-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="91d48-113">Anda dapat menemukan tampilan **pemanfaatan sumber daya** di panel **sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="91d48-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="91d48-114">Setiap sel di kisi mewakili persentase pemanfaatan yang dapat ditagih dari sumber daya dalam periode tertentu, seperti hari, pekan atau bulan.</span><span class="sxs-lookup"><span data-stu-id="91d48-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="91d48-115">Rumus berikut digunakan untuk mewarnai sel:</span><span class="sxs-lookup"><span data-stu-id="91d48-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="91d48-116">**Hijau**: Pemanfaatan yang ditagih > = pemanfaatan target sumber daya</span><span class="sxs-lookup"><span data-stu-id="91d48-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="91d48-117">**Kuning**: target pemanfaatan – 20 < = pemanfaatan yang bisa ditagih < target pemanfaatan.</span><span class="sxs-lookup"><span data-stu-id="91d48-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="91d48-118">**Merah**: Pemanfaatan yang bisa ditagih < pemanfaatan target – 20.</span><span class="sxs-lookup"><span data-stu-id="91d48-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="91d48-119">Karena tampilan **pemanfaatan sumber daya** didasarkan pada papan jadwal, Anda dapat menggunakan kemampuan pemfilteran papan jadwal untuk memfilter hasil.</span><span class="sxs-lookup"><span data-stu-id="91d48-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="91d48-120">Kisi-kisi mengharuskan Anda menetapkan Pemanfaatan peran atau sumber daya individual.</span><span class="sxs-lookup"><span data-stu-id="91d48-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="91d48-121">Untuk melakukan konfigurasi ini, buka **sumber daya** > **peran sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="91d48-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="91d48-122">Selain itu, peran default harus ditetapkan ke setiap sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="91d48-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="91d48-123">Buka **Sumber Daya** > **Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="91d48-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="91d48-124">Pada tab **Project Service**, periksa apakah peran sumber daya ditentukan, dan bidang **merupakan default** diatur ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="91d48-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="91d48-125">Anda dapat menambahkan peran tambahan di mana **merupakan default** = **Tidak**.</span><span class="sxs-lookup"><span data-stu-id="91d48-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="91d48-126">Peran jika **merupakan default** = **Ya** digunakan untuk mengevaluasi pemanfaatan sumber daya terhadap target untuk peran tersebut.</span><span class="sxs-lookup"><span data-stu-id="91d48-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="91d48-127">Di tab **Project Service**, Anda juga dapat menetapkan pemanfaatan target individual untuk sumber daya.</span><span class="sxs-lookup"><span data-stu-id="91d48-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="91d48-128">Perhitungan pemanfaatan kemudian menggunakan pemanfaatan target untuk mengevaluasi target sumber daya bukan target dari peran default sumber daya.</span><span class="sxs-lookup"><span data-stu-id="91d48-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="91d48-129">Pemanfaatan hanya ditampilkan untuk sumber daya hanya jika sumber daya telah disetujui, waktu yang dapat ditagih selama periode yang ditampilkan di kisi.</span><span class="sxs-lookup"><span data-stu-id="91d48-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
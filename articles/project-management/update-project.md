---
title: Perbarui proyek
description: Topik ini menyediakan informasi tentang memperbarui proyek di Project operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131437"
---
# <a name="update-a-project"></a><span data-ttu-id="ed2d5-103">Perbarui proyek</span><span class="sxs-lookup"><span data-stu-id="ed2d5-103">Update a project</span></span>

<span data-ttu-id="ed2d5-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="ed2d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ed2d5-105">Di bawah ini adalah ringkasan bidang yang dapat diperbarui pada proyek setelah dibuat dan implikasi pembaruan yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="ed2d5-106">Bidang rincian proyek</span><span class="sxs-lookup"><span data-stu-id="ed2d5-106">Project detail fields</span></span>

- <span data-ttu-id="ed2d5-107">**Nama**: Judul proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="ed2d5-108">**Deskripsi**: Ikhtisar proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="ed2d5-109">**Pelanggan**: perusahaan yang menerima hasil proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="ed2d5-110">**Template kalender**: jam kerja proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="ed2d5-111">Saat bidang diubah, seluruh jadwal dihitung ulang.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="ed2d5-112">**Mata uang**: mata uang proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="ed2d5-113">Default bidang ini adalah berdasarkan mata uang yang ditentukan di unit kontrak.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="ed2d5-114">Saat unit kontrak diperbarui, bidang juga diperbarui.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="ed2d5-115">**Unit kontrak**: unit organisasi yang mewakili grup perusahaan atau divisi yang terutama bertanggung jawab untuk memenangkan penjualan dan mengelola pengiriman pekerjaan dan layanan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="ed2d5-116">**Manajer Proyek**: anggota tim proyek yang memiliki wewenang untuk meninjau dan menyetujui entri waktu dan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="ed2d5-117">Bidang estimasi</span><span class="sxs-lookup"><span data-stu-id="ed2d5-117">Estimate fields</span></span>

- <span data-ttu-id="ed2d5-118">**Estimasi tanggal mulai**: tanggal saat proyek akan dimulai.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="ed2d5-119">Saat bidang ini diperbarui, tugas apa pun pada proyek akan bergerak secara proporsional dengan tanggal mulai baru mulai.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="ed2d5-120">**Tanggal selesai**: tanggal saat proyek dijadwalkan berakhir.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="ed2d5-121">**Upaya**: perkiraan upaya proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="ed2d5-122">Bila tugas ditambahkan ke proyek, bidang ini tidak lagi dapat diedit.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="ed2d5-123">**Estimasi biaya tenaga kerja**: perkiraan biaya tenaga kerja proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="ed2d5-124">Bila biaya tenaga kerja ditambahkan ke proyek, bidang ini tidak lagi dapat diedit.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="ed2d5-125">**Estimasi Pengeluaran**: perkiraan biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="ed2d5-126">Bila pengeluaran ditambahkan ke proyek, bidang ini tidak lagi dapat diedit.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="ed2d5-127">Bidang aktual proyek</span><span class="sxs-lookup"><span data-stu-id="ed2d5-127">Project actual fields</span></span>
- <span data-ttu-id="ed2d5-128">**Mulai aktual**: tanggal saat proyek dimulai.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="ed2d5-129">**Selesai aktual**: diperbarui setelah proyek selesai.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="ed2d5-130">Bidang Status Proyek</span><span class="sxs-lookup"><span data-stu-id="ed2d5-130">Project status fields</span></span>

- <span data-ttu-id="ed2d5-131">**status proyek keseluruhan**: kesehatan proyek keseluruhan yang dilakukan oleh manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="ed2d5-132">**Komentar** : narasi tentang kesehatan saat ini proyek yang dilakukan oleh manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="ed2d5-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>


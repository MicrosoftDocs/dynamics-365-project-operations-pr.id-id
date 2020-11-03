---
title: Tahapan proyek
description: Topik ini memberikan informasi tentang tahapan proyek yang tersedia dalam Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 554ad63bc44cbe5a1fe91eb47fedbb74bbedd4b6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078611"
---
# <a name="project-stages"></a><span data-ttu-id="27ca1-103">Tahapan proyek</span><span class="sxs-lookup"><span data-stu-id="27ca1-103">Project stages</span></span>

<span data-ttu-id="27ca1-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="27ca1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="27ca1-105">Tahapan proyek didesain untuk mencerminkan status proyek seiring kemajuannya.</span><span class="sxs-lookup"><span data-stu-id="27ca1-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="27ca1-106">Penyesuaian dapat digunakan untuk secara otomatis memperbarui tahapan dengan alur proses bisnis, Power Automate, atau ekstensi plug-in.</span><span class="sxs-lookup"><span data-stu-id="27ca1-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="27ca1-107">Tahapan berikut ditentukan dalam alur proses bisnis default:</span><span class="sxs-lookup"><span data-stu-id="27ca1-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="27ca1-108">Baru</span><span class="sxs-lookup"><span data-stu-id="27ca1-108">New</span></span>
- <span data-ttu-id="27ca1-109">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="27ca1-109">Quote</span></span>
- <span data-ttu-id="27ca1-110">Rencana</span><span class="sxs-lookup"><span data-stu-id="27ca1-110">Plan</span></span>
- <span data-ttu-id="27ca1-111">Kirim</span><span class="sxs-lookup"><span data-stu-id="27ca1-111">Deliver</span></span>
- <span data-ttu-id="27ca1-112">Selesaikan</span><span class="sxs-lookup"><span data-stu-id="27ca1-112">Complete</span></span>
- <span data-ttu-id="27ca1-113">Tutup</span><span class="sxs-lookup"><span data-stu-id="27ca1-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="27ca1-114">Baru</span><span class="sxs-lookup"><span data-stu-id="27ca1-114">New</span></span>

<span data-ttu-id="27ca1-115">Bila Anda membuat sebuah proyek, tahapan proyek diatur ke **Baru**.</span><span class="sxs-lookup"><span data-stu-id="27ca1-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="27ca1-116">Jika proyek dibuat dari template, mungkin memiliki jadwal, perkiraan, dan data tim.</span><span class="sxs-lookup"><span data-stu-id="27ca1-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="27ca1-117">Jika tidak, itu adalah garis besar proyek, dan komponen lainnya harus dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="27ca1-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="27ca1-118">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="27ca1-118">Quote</span></span>

<span data-ttu-id="27ca1-119">Ketika Anda menghubungkan sebuah proyek dengan kuotasi, atau ketika membuat proyek dari kuotasi, tahapan proyek diatur ke **kuotasi** , dan perkiraan awal dan akhir tanggal diperbarui.</span><span class="sxs-lookup"><span data-stu-id="27ca1-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote** , and the estimated start and end dates are updated.</span></span> <span data-ttu-id="27ca1-120">Ketika proyek pada tahapan **kuotasi** , tab **Penjualan** pada halaman **entitas proyek** menampilkan detail kuotasi.</span><span class="sxs-lookup"><span data-stu-id="27ca1-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="27ca1-121">Rencana</span><span class="sxs-lookup"><span data-stu-id="27ca1-121">Plan</span></span>

<span data-ttu-id="27ca1-122">Ketika Anda memenangkan kuotasi yang berkaitan dengan proyek, dan proyek itu dipindahkan ke fase **Kontrak** , tahapan proyek diperbarui ke **rencana**.</span><span class="sxs-lookup"><span data-stu-id="27ca1-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="27ca1-123">Ketika proyek pada tahapan **Rencana** , halaman **entitas proyek** menampilkan detail kontrak.</span><span class="sxs-lookup"><span data-stu-id="27ca1-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="27ca1-124">Kirim</span><span class="sxs-lookup"><span data-stu-id="27ca1-124">Deliver</span></span>

<span data-ttu-id="27ca1-125">Setelah rencana proyek selesai, dan Anda siap memulai proyek, manajer proyek harus memperbarui tahapan proyek ke **dilaksanakan** untuk menunjukkan bahwa proyek telah dimulai.</span><span class="sxs-lookup"><span data-stu-id="27ca1-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="27ca1-126">Selesai</span><span class="sxs-lookup"><span data-stu-id="27ca1-126">Complete</span></span> 

<span data-ttu-id="27ca1-127">Saat pekerjaan untuk proyek selesai, manajer proyek dapat memperbarui tahapan ke **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="27ca1-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="27ca1-128">Dengan memperbarui tahap proyek ke **Selesai** , manajer proyek menunjukkan bahwa pekerjaan 100 persen selesai, namun proyek tetap terbuka sehingga setiap entri waktu atau biaya yang tertunda dapat direkam.</span><span class="sxs-lookup"><span data-stu-id="27ca1-128">By updating the project stage to **Complete** , the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="27ca1-129">Tutup</span><span class="sxs-lookup"><span data-stu-id="27ca1-129">Close</span></span>

<span data-ttu-id="27ca1-130">Bila semua transaksi direkam untuk proyek, manajer proyek dapat memperbarui tahapan ke **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="27ca1-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="27ca1-131">Pada titik tersebut, tidak ada transaksi yang dapat direkam, dan proyek diatur ke hanya baca.</span><span class="sxs-lookup"><span data-stu-id="27ca1-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


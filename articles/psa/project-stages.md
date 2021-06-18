---
title: Jenis Tahapan proyek
description: Topik ini menyediakan informasi tentang tahapan proyek.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: ed725d8ea2f671c45a7a19bb017bbb08c41f42db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008990"
---
# <a name="project-stage-types"></a><span data-ttu-id="f079c-103">Jenis Tahapan proyek</span><span class="sxs-lookup"><span data-stu-id="f079c-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f079c-104">Tahapan proyek didesain untuk mencerminkan status proyek seiring kemajuannya.</span><span class="sxs-lookup"><span data-stu-id="f079c-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="f079c-105">Penyesuaian dapat digunakan untuk secara otomatis memperbarui tahapan dengan alur proses bisnis, Power Automate, atau ekstensi plug-in.</span><span class="sxs-lookup"><span data-stu-id="f079c-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="f079c-106">Tahapan berikut ditentukan dalam BPF default:</span><span class="sxs-lookup"><span data-stu-id="f079c-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="f079c-107">Baru</span><span class="sxs-lookup"><span data-stu-id="f079c-107">New</span></span>
- <span data-ttu-id="f079c-108">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="f079c-108">Quote</span></span>
- <span data-ttu-id="f079c-109">Rencana</span><span class="sxs-lookup"><span data-stu-id="f079c-109">Plan</span></span>
- <span data-ttu-id="f079c-110">Kirim</span><span class="sxs-lookup"><span data-stu-id="f079c-110">Deliver</span></span>
- <span data-ttu-id="f079c-111">Selesai</span><span class="sxs-lookup"><span data-stu-id="f079c-111">Complete</span></span>
- <span data-ttu-id="f079c-112">Tutup</span><span class="sxs-lookup"><span data-stu-id="f079c-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="f079c-113">Baru</span><span class="sxs-lookup"><span data-stu-id="f079c-113">New</span></span>

<span data-ttu-id="f079c-114">Bila Anda membuat sebuah proyek, tahapan proyek diatur ke **Baru**.</span><span class="sxs-lookup"><span data-stu-id="f079c-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="f079c-115">Jika proyek dibuat dari template, mungkin memiliki jadwal, perkiraan, dan data tim.</span><span class="sxs-lookup"><span data-stu-id="f079c-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="f079c-116">Jika tidak, itu hanya garis besar proyek, dan komponen lainnya harus dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="f079c-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="f079c-117">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="f079c-117">Quote</span></span>

<span data-ttu-id="f079c-118">Ketika Anda menghubungkan sebuah proyek dengan kuotasi, atau ketika membuat proyek dari kuotasi, tahapan proyek diatur ke **kuotasi**, dan perkiraan awal dan akhir tanggal diperbarui.</span><span class="sxs-lookup"><span data-stu-id="f079c-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="f079c-119">Ketika proyek pada tahapan **kuotasi**, tab **Penjualan** pada halaman **entitas proyek** menampilkan detail kuotasi.</span><span class="sxs-lookup"><span data-stu-id="f079c-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="f079c-120">Rencana</span><span class="sxs-lookup"><span data-stu-id="f079c-120">Plan</span></span>

<span data-ttu-id="f079c-121">Ketika Anda memenangkan kuotasi yang berkaitan dengan proyek, dan proyek itu dipindahkan ke fase **Kontrak**, tahapan proyek diperbarui ke **rencana**.</span><span class="sxs-lookup"><span data-stu-id="f079c-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="f079c-122">Ketika proyek pada tahapan **Rencana**, halaman **entitas proyek** menampilkan detail kontrak.</span><span class="sxs-lookup"><span data-stu-id="f079c-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="f079c-123">Kirim</span><span class="sxs-lookup"><span data-stu-id="f079c-123">Deliver</span></span>

<span data-ttu-id="f079c-124">Setelah rencana proyek selesai, dan Anda siap memulai proyek, manajer proyek harus memperbarui tahapan proyek ke **dilaksanakan** untuk menunjukkan bahwa proyek telah dimulai.</span><span class="sxs-lookup"><span data-stu-id="f079c-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="f079c-125">Selesai</span><span class="sxs-lookup"><span data-stu-id="f079c-125">Complete</span></span> 

<span data-ttu-id="f079c-126">Saat pekerjaan untuk proyek selesai, manajer proyek dapat memperbarui tahapan ke **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="f079c-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="f079c-127">Dengan memperbarui tahap proyek ke **Selesai**, manajer proyek menunjukkan bahwa pekerjaan 100 persen selesai, namun proyek tetap terbuka sehingga setiap entri waktu atau biaya yang tertunda dapat direkam.</span><span class="sxs-lookup"><span data-stu-id="f079c-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="f079c-128">Tutup</span><span class="sxs-lookup"><span data-stu-id="f079c-128">Close</span></span>

<span data-ttu-id="f079c-129">Bila semua transaksi direkam untuk proyek, manajer proyek dapat memperbarui tahapan ke **Tutup**.</span><span class="sxs-lookup"><span data-stu-id="f079c-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="f079c-130">Pada titik tersebut, tidak ada transaksi yang dapat direkam, dan proyek diatur ke hanya baca.</span><span class="sxs-lookup"><span data-stu-id="f079c-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
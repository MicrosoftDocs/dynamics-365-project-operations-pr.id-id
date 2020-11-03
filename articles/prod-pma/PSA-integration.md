---
title: Gambaran Umum Project Service Automation
description: Topik ini menyediakan informasi tentang solusi integrasi Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1e1a963bccefd1552aab6e42d3b2d1dc63a82e8f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078625"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="32457-103">Gambaran Umum Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="32457-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="32457-104">Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans Dynamics 365 Finance dan Dynamics 365 Project Service Automation melalui Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="32457-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="32457-105">Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran proyek, kontrak proyek, baris kontrak proyek, tonggak pencapaian baris kontrak proyek, tugas proyek, kategori transaksi pengeluaran, estimasi jam, dan estimasi pengeluaran dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="32457-106">Jika Anda menggunakan versi 7.3.0, Anda harus menginstal KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="32457-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="32457-107">Anda kemudian akan dapat mengintegrasikan proyek harga tetap.</span><span class="sxs-lookup"><span data-stu-id="32457-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="32457-108">Jika Anda menggunakan versi 7.3.0, dan Anda membawa transaksi biaya melalui dari Project Service Automation, Anda harus menginstal 4345320 KB agar dapat mencakup biaya tersebut dalam faktur proyek.</span><span class="sxs-lookup"><span data-stu-id="32457-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="32457-109">Jika Anda menggunakan versi 8.0, Anda akan dapat menggunakan Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi.</span><span class="sxs-lookup"><span data-stu-id="32457-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="32457-110">Jika Anda menggunakan versi 8.0.1 atau yang lebih baru, Anda akan dapat mensinkronisasi aktual.</span><span class="sxs-lookup"><span data-stu-id="32457-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="32457-111">Sebelum Anda dapat mengintegrasikan Project Service Automation Finance, Anda harus mengkonfigurasikan parameter integrasi Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="32457-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="32457-112">Untuk Informasi lebih lanjut, lihat [mengintegrasikan parameter integrasi Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="32457-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="32457-113">Solusi integrasi ini memungkinkan sinkronisasi langsung dalam skenario berikut:</span><span class="sxs-lookup"><span data-stu-id="32457-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="32457-114">Kelola kontrak proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="32457-115">Buat proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="32457-116">Kelola baris kontrak proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="32457-117">Kelola tonggak pencapaian baris kontrak proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="32457-118">Kelola tugas proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="32457-119">Kelola kategori transaksi pengeluaran di Finance, dan sinkronisasikan secara langsung dari Finance ke Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="32457-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="32457-120">Buat estimasi jam proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="32457-121">Buat estimasi pengeluaran proyek di Project Service Automation, dan sinkronisasikan secara langsung dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="32457-122">Buat waktu proyek, pengeluaran, dan aktual ongkos dalam Project Service Automation, dan buat transaksi proyek dalam jurnal integrasi Project Service Automation sehingga dapat diposting di Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="32457-123">Sinkronisasi data</span><span class="sxs-lookup"><span data-stu-id="32457-123">Data synchronization</span></span>

<span data-ttu-id="32457-124">Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan sebagai bagian integrasi antara Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="32457-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="32457-125">Tidak semua template tersedia saat ini.</span><span class="sxs-lookup"><span data-stu-id="32457-125">Not all templates are currently available.</span></span> <span data-ttu-id="32457-126">Template akan dirilis saat selesai.</span><span class="sxs-lookup"><span data-stu-id="32457-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="32457-127">[![Integrasi Project Service Automation dengan Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="32457-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="32457-128">Persyaratan sistem untuk Finance</span><span class="sxs-lookup"><span data-stu-id="32457-128">System requirements for Finance</span></span>

<span data-ttu-id="32457-129">Untuk menggunakan solusi integrasi Project Service Automation ke Finance, Anda harus menginstal Enterprise Edition 7.3 dengan pembaruan platform 12, atau yang lebih baru.</span><span class="sxs-lookup"><span data-stu-id="32457-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="32457-130">Persyaratan sistem untuk Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="32457-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="32457-131">Untuk menggunakan solusi integrasi Project Service Automation ke Finance, Anda harus menginstal komponen berikut:</span><span class="sxs-lookup"><span data-stu-id="32457-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="32457-132">Dynamics 365 Project Service Automation versi 9.0.0.0 atau lebih baru</span><span class="sxs-lookup"><span data-stu-id="32457-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="32457-133">Solusi Prospek ke kas untuk Dynamics 365 Sales, versi 1.14.0.0 (V14) atau versi lebih baru</span><span class="sxs-lookup"><span data-stu-id="32457-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="32457-134">Solusi Project Service Automation ke Finance untuk Dynamics 365 Project Service Automation versi 1.0.0.0 atau lebih baru</span><span class="sxs-lookup"><span data-stu-id="32457-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="32457-135">Instal solusi integrasi Project Service Automation ke Finance di instans Project Service Automation Anda</span><span class="sxs-lookup"><span data-stu-id="32457-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="32457-136">Unduh solusi integrasi Project Service Automation ke Finance dari [pusat Unduh Microsoft](https://www.microsoft.com/download/details.aspx?id=57016), dan ikuti petunjuk yang disertakan dengan solusi.</span><span class="sxs-lookup"><span data-stu-id="32457-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>

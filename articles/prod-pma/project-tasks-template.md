---
title: Sinkronisasikan tugas proyek secara langsung dari Project Service Automation ke Finance and Operations
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan tugas proyek secara langsung dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7cc9ee9de576549c132e14c333a1000c22a55236
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288923"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b268d-103">Sinkronisasikan tugas proyek secara langsung dari Project Service Automation ke Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b268d-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b268d-104">Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan tugas proyek secara langsung dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b268d-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="b268d-105">Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.</span><span class="sxs-lookup"><span data-stu-id="b268d-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="b268d-106">Jika Anda menggunakan Enterprise Edition 7.3.0 setelah menginstal 4132657 KB dan 4132660 KB, Anda dapat menggunakan template untuk mengintegrasikan tugas proyek, kategori transaksi pengeluaran, perkiraan jam, perkiraan biaya, dan aktual, serta untuk mengkonfigurasi penguncian fungsionalitas.</span><span class="sxs-lookup"><span data-stu-id="b268d-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b268d-107">Jika Anda harus me-reset distribusi akuntansi, kami sarankan Anda juga menginstal 4131710 KB.</span><span class="sxs-lookup"><span data-stu-id="b268d-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="b268d-108">Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.</span><span class="sxs-lookup"><span data-stu-id="b268d-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="b268d-109">Aliran data untuk Project Service Automation ke Finance</span><span class="sxs-lookup"><span data-stu-id="b268d-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="b268d-110">Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="b268d-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="b268d-111">Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang tugas proyek dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="b268d-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b268d-112">Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="b268d-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="b268d-113">[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b268d-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="b268d-114">Template dan tugas</span><span class="sxs-lookup"><span data-stu-id="b268d-114">Template and task</span></span>

<span data-ttu-id="b268d-115">Untuk mengakses template, di Pusat admin Microsoft Power Apps, pilih **proyek**, lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.</span><span class="sxs-lookup"><span data-stu-id="b268d-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b268d-116">Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan tugas proyek dari Project Service Automation ke Finance:</span><span class="sxs-lookup"><span data-stu-id="b268d-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="b268d-117">**Nama template di integrasi data:** tugas proyek (PSA ke Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="b268d-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b268d-118">**Nama tugas dalam proyek:** Tugas proyek</span><span class="sxs-lookup"><span data-stu-id="b268d-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="b268d-119">Sebelum sinkronisasi tugas proyek dapat terjadi, Anda harus mensinkronisasikan kontrak proyek dan proyek.</span><span class="sxs-lookup"><span data-stu-id="b268d-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="b268d-120">Rangkaian Entitas</span><span class="sxs-lookup"><span data-stu-id="b268d-120">Entity set</span></span>

| <span data-ttu-id="b268d-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b268d-121">Project Service Automation</span></span> | <span data-ttu-id="b268d-122">Keuangan</span><span class="sxs-lookup"><span data-stu-id="b268d-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="b268d-123">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="b268d-123">Project Tasks</span></span>              | <span data-ttu-id="b268d-124">Entitas integrasi untuk tugas proyek</span><span class="sxs-lookup"><span data-stu-id="b268d-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="b268d-125">Alur entitas</span><span class="sxs-lookup"><span data-stu-id="b268d-125">Entity flow</span></span>

<span data-ttu-id="b268d-126">Tugas proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai aktivitas proyek.</span><span class="sxs-lookup"><span data-stu-id="b268d-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="b268d-127">Prasyarat dan konfigurasi pemetaan</span><span class="sxs-lookup"><span data-stu-id="b268d-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="b268d-128">Sebelum sinkronisasi tugas proyek dapat terjadi, Anda harus mensinkronisasikan kontrak proyek dan proyek.</span><span class="sxs-lookup"><span data-stu-id="b268d-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="b268d-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="b268d-129">Power Query</span></span>

<span data-ttu-id="b268d-130">Anda harus menggunakan Microsoft Power Query untuk Excel untuk memfilter data jika ini terpenuhi:</span><span class="sxs-lookup"><span data-stu-id="b268d-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="b268d-131">Anda memiliki rekaman khusus sumber daya dalam tugas proyek.</span><span class="sxs-lookup"><span data-stu-id="b268d-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="b268d-132">Jika anda harus menggunakan Power Query, ikuti panduan ini:</span><span class="sxs-lookup"><span data-stu-id="b268d-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="b268d-133">Template tugas proyek (PSA untuk Fin dan Ops) memiliki filter default yang mengecualikan rekaman khusus sumber daya dari tugas proyek dengan mengatur filter pada **islinetask** ke **false**.</span><span class="sxs-lookup"><span data-stu-id="b268d-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="b268d-134">Jika Anda membuat template sendiri, Anda harus menambahkan filter ini.</span><span class="sxs-lookup"><span data-stu-id="b268d-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b268d-135">Pemetaan template di integrasi data</span><span class="sxs-lookup"><span data-stu-id="b268d-135">Template mapping in Data integration</span></span>

<span data-ttu-id="b268d-136">Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data.</span><span class="sxs-lookup"><span data-stu-id="b268d-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="b268d-137">Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="b268d-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="b268d-138">[![Pemetaan template](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="b268d-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
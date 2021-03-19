---
title: Sinkronisasikan estimasi proyek secara langsung dari Project Service Automation ke Finance and Operations
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan estimasi jam proyek dan estimasi pengeluaran proyek secara langsung dari Microsoft Dynamics 365 Project Service Automation ke Dynamics 365 Finance.
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
ms.openlocfilehash: 58e204b2c1238e00ffb16533cc82dad69fbf77a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289463"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3380b-103">Sinkronisasikan estimasi proyek secara langsung dari Project Service Automation ke Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3380b-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3380b-104">Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan estimasi jam proyek dan estimasi pengeluaran proyek secara langsung dari Dynamics 365 Project Service Automation ke Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="3380b-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="3380b-105">Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.</span><span class="sxs-lookup"><span data-stu-id="3380b-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="3380b-106">Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.</span><span class="sxs-lookup"><span data-stu-id="3380b-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="3380b-107">Aliran data untuk Project Service Automation ke Finance</span><span class="sxs-lookup"><span data-stu-id="3380b-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="3380b-108">Solusi integrasi Project Service Automation ke Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="3380b-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="3380b-109">Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang estimasi jam proyek dan estimasi pengeluaran proyek dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="3380b-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3380b-110">Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="3380b-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="3380b-111">[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="3380b-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="3380b-112">Estimasi jam proyek</span><span class="sxs-lookup"><span data-stu-id="3380b-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3380b-113">Template dan tugas</span><span class="sxs-lookup"><span data-stu-id="3380b-113">Template and tasks</span></span>

<span data-ttu-id="3380b-114">Untuk mengakses template yang tersedia, di Pusat admin Microsoft Power Apps, pilih **proyek**, lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.</span><span class="sxs-lookup"><span data-stu-id="3380b-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3380b-115">Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan estimasi jam proyek dari Project Service Automation ke Finance:</span><span class="sxs-lookup"><span data-stu-id="3380b-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3380b-116">**Nama template di integrasi data:** estimasi jam proyek (PSA ke Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3380b-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3380b-117">**Nama tugas dalam proyek**</span><span class="sxs-lookup"><span data-stu-id="3380b-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3380b-118">Relasi transaksi</span><span class="sxs-lookup"><span data-stu-id="3380b-118">Transaction relationships</span></span>
    - <span data-ttu-id="3380b-119">Perkiraan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="3380b-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3380b-120">Rangkaian Entitas</span><span class="sxs-lookup"><span data-stu-id="3380b-120">Entity set</span></span>

| <span data-ttu-id="3380b-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3380b-121">Project Service Automation</span></span> | <span data-ttu-id="3380b-122">Keuangan</span><span class="sxs-lookup"><span data-stu-id="3380b-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="3380b-123">Tugas Proyek</span><span class="sxs-lookup"><span data-stu-id="3380b-123">Project tasks</span></span>              | <span data-ttu-id="3380b-124">Entitas integrasi untuk estimasi jam proyek</span><span class="sxs-lookup"><span data-stu-id="3380b-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="3380b-125">Alur entitas</span><span class="sxs-lookup"><span data-stu-id="3380b-125">Entity flow</span></span>

<span data-ttu-id="3380b-126">Estimasi jam proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai perkiraan jam proyek.</span><span class="sxs-lookup"><span data-stu-id="3380b-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3380b-127">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="3380b-127">Prerequisites</span></span>

<span data-ttu-id="3380b-128">Sebelum sinkronisasi perkiraan jam proyek dapat terjadi, Anda harus mensinkronisasikan proyek, tugas proyek, dan kategori transaksi pengeluaran proyek.</span><span class="sxs-lookup"><span data-stu-id="3380b-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3380b-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="3380b-129">Power Query</span></span>

<span data-ttu-id="3380b-130">Di template estimasi jam proyek, anda harus menggunakan Microsoft Power Query untuk Excel untuk menyelesaikan tugas ini:</span><span class="sxs-lookup"><span data-stu-id="3380b-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="3380b-131">Atur ID model perkiraan default yang akan digunakan saat integrasi membuat perkiraan jam baru.</span><span class="sxs-lookup"><span data-stu-id="3380b-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3380b-132">Filter rekaman khusus sumber daya dalam tugas yang akan gagal dalam integrasi ke perkiraan jam.</span><span class="sxs-lookup"><span data-stu-id="3380b-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="3380b-133">Filter setiap baris kategori transaksi kosong.</span><span class="sxs-lookup"><span data-stu-id="3380b-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="3380b-134">Kegagalan untuk menyelesaikan tugas ini dapat mengakibatkan perkiraan jam salah.</span><span class="sxs-lookup"><span data-stu-id="3380b-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3380b-135">Mengatur ID model default perkiraan</span><span class="sxs-lookup"><span data-stu-id="3380b-135">Set the default forecast model ID</span></span>

<span data-ttu-id="3380b-136">Untuk memperbarui ID model perkiraan default dalam template, klik panah **peta** untuk membuka pemetaan.</span><span class="sxs-lookup"><span data-stu-id="3380b-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3380b-137">Lalu pilih tautan **kueri lanjutan dan filter**.</span><span class="sxs-lookup"><span data-stu-id="3380b-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3380b-138">Jika anda menggunakan estimasi jam proyek default (PSA ke Fin and Ops), pilih **kondisi dimasukkan** di daftar **langkah yang diterapkan**.</span><span class="sxs-lookup"><span data-stu-id="3380b-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="3380b-139">Di entri **fungsi**, ganti **O\_forecast** dengan nama ID model perkiraan yang harus digunakan dengan integrasi.</span><span class="sxs-lookup"><span data-stu-id="3380b-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3380b-140">Template default memiliki ID model perkiraan dari data demo.</span><span class="sxs-lookup"><span data-stu-id="3380b-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3380b-141">Jika Anda membuat template baru, Anda harus menambahkan kolom ini.</span><span class="sxs-lookup"><span data-stu-id="3380b-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3380b-142">Di Power Query, pilih **Tambah kolom kondisional**, dan masukkan nama untuk kolom baru, misalnya **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="3380b-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3380b-143">Masukkan kondisi untuk kolom, di mana, jika tugas proyek tidak null, maka \<enter the forecast model ID\>; jika tidak maka null.</span><span class="sxs-lookup"><span data-stu-id="3380b-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="3380b-144">Memfilter rekaman khusus sumber daya</span><span class="sxs-lookup"><span data-stu-id="3380b-144">Filter out resource-specific records</span></span>

<span data-ttu-id="3380b-145">Estimasi jam proyek (PSA ke Fin and Ops) memiliki filter default yang menghilangkan rekaman khusus sumber daya apa pun.</span><span class="sxs-lookup"><span data-stu-id="3380b-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="3380b-146">Jika Anda membuat template sendiri, Anda harus menambahkan filter ini.</span><span class="sxs-lookup"><span data-stu-id="3380b-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3380b-147">Pilih tautan **kueri lanjutan dan filter** untuk memfilter pada kolom **msdyn\_islinetask** agar hanya rekaman yang **salah** yang disertakan.</span><span class="sxs-lookup"><span data-stu-id="3380b-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="3380b-148">Filter baris kategori transaksi kosong</span><span class="sxs-lookup"><span data-stu-id="3380b-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="3380b-149">Anda harus menambahkan filter untuk menghapus setiap baris yang memiliki kategori transaksi kosong.</span><span class="sxs-lookup"><span data-stu-id="3380b-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="3380b-150">Tugas ini diperlukan, terlepas dari Apakah Anda menggunakan template default atau membuat template Anda sendiri.</span><span class="sxs-lookup"><span data-stu-id="3380b-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="3380b-151">Filter ini menghilangkan baris ringkasan apa pun dari Project Service Automation yang mungkin menyebabkan perkiraan jam di Finance menjadi tidak benar.</span><span class="sxs-lookup"><span data-stu-id="3380b-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="3380b-152">Pilih tautan **kueri lanjutan dan filter** untuk memfilter rekaman null di kolom **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="3380b-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3380b-153">Pemetaan template di integrasi data</span><span class="sxs-lookup"><span data-stu-id="3380b-153">Template mapping in Data integration</span></span>

<span data-ttu-id="3380b-154">Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data.</span><span class="sxs-lookup"><span data-stu-id="3380b-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="3380b-155">Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="3380b-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3380b-156">[![Pemetaan tugas template dalam integrasi data](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3380b-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="3380b-157">Estimasi pengeluaran proyek</span><span class="sxs-lookup"><span data-stu-id="3380b-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="3380b-158">Template dan tugas</span><span class="sxs-lookup"><span data-stu-id="3380b-158">Template and tasks</span></span>

<span data-ttu-id="3380b-159">Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan estimasi pengeluaran proyek dari Project Service Automation ke Finance:</span><span class="sxs-lookup"><span data-stu-id="3380b-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="3380b-160">**Nama template di integrasi data:** estimasi pengeluaran proyek (PSA ke Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3380b-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3380b-161">**Nama tugas dalam proyek**</span><span class="sxs-lookup"><span data-stu-id="3380b-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="3380b-162">Relasi transaksi</span><span class="sxs-lookup"><span data-stu-id="3380b-162">Transaction relationships</span></span> 
    - <span data-ttu-id="3380b-163">Perkiraan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="3380b-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="3380b-164">Rangkaian Entitas</span><span class="sxs-lookup"><span data-stu-id="3380b-164">Entity set</span></span>

| <span data-ttu-id="3380b-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3380b-165">Project Service Automation</span></span> | <span data-ttu-id="3380b-166">Keuangan</span><span class="sxs-lookup"><span data-stu-id="3380b-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="3380b-167">Koneksi Transaksi</span><span class="sxs-lookup"><span data-stu-id="3380b-167">Transaction Connections</span></span>    | <span data-ttu-id="3380b-168">Entitas integrasi untuk Relasi transaksi proyek</span><span class="sxs-lookup"><span data-stu-id="3380b-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="3380b-169">Baris Perkiraan</span><span class="sxs-lookup"><span data-stu-id="3380b-169">Estimate Lines</span></span>             | <span data-ttu-id="3380b-170">Entitas integrasi untuk estimasi proyek</span><span class="sxs-lookup"><span data-stu-id="3380b-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="3380b-171">Alur entitas</span><span class="sxs-lookup"><span data-stu-id="3380b-171">Entity flow</span></span>

<span data-ttu-id="3380b-172">Estimasi pengeluaran proyek dikelola dalam Project Service Automation, dan disinkronisasi ke Finance sebagai perkiraan pengeluaran proyek.</span><span class="sxs-lookup"><span data-stu-id="3380b-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="3380b-173">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="3380b-173">Prerequisites</span></span>

<span data-ttu-id="3380b-174">Sebelum sinkronisasi perkiraan pengeluaran proyek dapat terjadi, Anda harus mensinkronisasikan proyek, tugas proyek, dan kategori transaksi pengeluaran proyek.</span><span class="sxs-lookup"><span data-stu-id="3380b-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="3380b-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="3380b-175">Power Query</span></span>

<span data-ttu-id="3380b-176">Di template estimasi pengeluaran proyek, anda harus menggunakan Power Query untuk menyelesaikan tugas berikut ini:</span><span class="sxs-lookup"><span data-stu-id="3380b-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="3380b-177">Filter untuk menyertakan hanya rekaman baris estimasi pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="3380b-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="3380b-178">Atur ID model perkiraan default yang akan digunakan saat integrasi membuat perkiraan jam baru.</span><span class="sxs-lookup"><span data-stu-id="3380b-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="3380b-179">Ubah jenis penagihan.</span><span class="sxs-lookup"><span data-stu-id="3380b-179">Transform the billing types.</span></span>
- <span data-ttu-id="3380b-180">Ubah jenis transaksi.</span><span class="sxs-lookup"><span data-stu-id="3380b-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="3380b-181">Filter untuk menyertakan hanya baris estimasi pengeluaran</span><span class="sxs-lookup"><span data-stu-id="3380b-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="3380b-182">Template perkiraan pengeluaran proyek (PSA ke Fin and Ops) memiliki filter default yang mencakup hanya baris pengeluaran di integrasi.</span><span class="sxs-lookup"><span data-stu-id="3380b-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="3380b-183">Jika Anda membuat template sendiri, Anda harus menambahkan filter ini.</span><span class="sxs-lookup"><span data-stu-id="3380b-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="3380b-184">Pilih tugas **Relasi transaksi**, lalu klik panah **peta** untuk membuka pemetaan.</span><span class="sxs-lookup"><span data-stu-id="3380b-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3380b-185">Pilih tautan **kueri lanjutan dan filter**.</span><span class="sxs-lookup"><span data-stu-id="3380b-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="3380b-186">Filter kolom **msdyn\_transactiontype1** sehingga mencakup hanya **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="3380b-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="3380b-187">Mengatur ID model default perkiraan</span><span class="sxs-lookup"><span data-stu-id="3380b-187">Set the default forecast model ID</span></span>

<span data-ttu-id="3380b-188">Untuk memperbarui ID model perkiraan default dalam template, pilih tugas **Estimasi pengeluaran**, lalu klik panah **peta** untuk membuka pemetaan.</span><span class="sxs-lookup"><span data-stu-id="3380b-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="3380b-189">Pilih tautan **kueri lanjutan dan filter**.</span><span class="sxs-lookup"><span data-stu-id="3380b-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="3380b-190">Jika anda menggunakan template estimasi pengeluaran proyek default (PSA ke Fin and Ops), di Power Query, pilih **kondisi dimasukkan** pertama dari bagian **langkah yang diterapkan**.</span><span class="sxs-lookup"><span data-stu-id="3380b-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="3380b-191">Di entri **fungsi**, ganti **O\_forecast** dengan nama ID model perkiraan yang harus digunakan dengan integrasi.</span><span class="sxs-lookup"><span data-stu-id="3380b-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="3380b-192">Template default memiliki ID model perkiraan dari data demo.</span><span class="sxs-lookup"><span data-stu-id="3380b-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="3380b-193">Jika Anda membuat template baru, Anda harus menambahkan kolom ini.</span><span class="sxs-lookup"><span data-stu-id="3380b-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="3380b-194">Di Power Query, pilih **Tambah kolom kondisional**, dan masukkan nama untuk kolom baru, misalnya **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="3380b-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="3380b-195">Masukkan kondisi untuk kolom, di mana, jika ID baris estimasi tidak null, maka \<enter the forecast model ID\>; jika tidak maka null.</span><span class="sxs-lookup"><span data-stu-id="3380b-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="3380b-196">Ubah jenis penagihan</span><span class="sxs-lookup"><span data-stu-id="3380b-196">Transform the billing types</span></span>

<span data-ttu-id="3380b-197">Template perkiraan pengeluaran proyek (PSA ke Fin and Ops) mencakup bidang kondisional yang digunakan untuk mengubah jenis penagihan yang diterima dari Project Service Automation selama integrasi.</span><span class="sxs-lookup"><span data-stu-id="3380b-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3380b-198">Jika Anda membuat template sendiri, Anda harus menambahkan kolom bersyarat ini.</span><span class="sxs-lookup"><span data-stu-id="3380b-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3380b-199">Pilih tautan **kueri lanjutan dan pemfilteran**, lalu pilih **Tambah kolom kondisional**.</span><span class="sxs-lookup"><span data-stu-id="3380b-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3380b-200">Masukkan nama untuk kolom baru, seperti **billingtype**.</span><span class="sxs-lookup"><span data-stu-id="3380b-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="3380b-201">Lalu masukkan kondisi berikut:</span><span class="sxs-lookup"><span data-stu-id="3380b-201">Then enter the following condition:</span></span>

<span data-ttu-id="3380b-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="3380b-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="3380b-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="3380b-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="3380b-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="3380b-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="3380b-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="3380b-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="3380b-206">Ubah jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="3380b-206">Transform the transaction types</span></span>

<span data-ttu-id="3380b-207">Template perkiraan pengeluaran proyek (PSA ke Fin and Ops) mencakup bidang kondisional yang digunakan untuk mengubah jenis transaksi yang diterima dari Project Service Automation selama integrasi.</span><span class="sxs-lookup"><span data-stu-id="3380b-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="3380b-208">Jika Anda membuat template sendiri, Anda harus menambahkan kolom bersyarat ini.</span><span class="sxs-lookup"><span data-stu-id="3380b-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="3380b-209">Pilih tautan **kueri lanjutan dan pemfilteran**, lalu pilih **Tambah kolom kondisional**.</span><span class="sxs-lookup"><span data-stu-id="3380b-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="3380b-210">Masukkan nama untuk kolom baru, seperti **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="3380b-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="3380b-211">Lalu masukkan kondisi berikut:</span><span class="sxs-lookup"><span data-stu-id="3380b-211">Then enter the following condition:</span></span>

<span data-ttu-id="3380b-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="3380b-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="3380b-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="3380b-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="3380b-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="3380b-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3380b-215">Pemetaan template di integrasi data</span><span class="sxs-lookup"><span data-stu-id="3380b-215">Template mapping in Data integration</span></span>

<span data-ttu-id="3380b-216">Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data.</span><span class="sxs-lookup"><span data-stu-id="3380b-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="3380b-217">Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="3380b-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="3380b-218">[![Pemetaan template transaksi estimasi pengeluaran](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3380b-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="3380b-219">[![Pemetaan template estimasi pengeluaran](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="3380b-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
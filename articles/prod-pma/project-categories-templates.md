---
title: Mensinkronisasikan kategori pengeluaran proyek antara Finance and Operations dan Project Service Automation
description: Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan kategori pengeluaran proyek antara Microsoft Dynamics 365 Finance dan Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 2816d363dbfe6ef2d98a584b214f72d9b30c49bb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999855"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="a95f4-103">Mensinkronisasikan kategori pengeluaran proyek antara Finance and Operations dan Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a95f4-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a95f4-104">Topik ini menjelaskan template dan tugas yang mendasari yang digunakan untuk mensinkronisasikan kategori pengeluaran proyek antara Dynamics 365 Finance dan Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a95f4-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="a95f4-105">Integrasi tugas proyek, kategori transaksi pengeluaran, estimasi jam, estimasi pengeluaran, dan penguncian fungsi tersedia dalam versi 8.0.</span><span class="sxs-lookup"><span data-stu-id="a95f4-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="a95f4-106">Integrasi aktual proyek tersedia di versi 8.0.1 atau setelahnya.</span><span class="sxs-lookup"><span data-stu-id="a95f4-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="a95f4-107">Jika Anda menggunakan Enterprise Edition 7.3.0 setelah menginstal 4132657 KB dan 4132660 KB, Anda dapat menggunakan template untuk mengintegrasikan tugas proyek, kategori transaksi pengeluaran, perkiraan jam, perkiraan biaya, dan aktual, serta untuk mengkonfigurasi penguncian fungsionalitas.</span><span class="sxs-lookup"><span data-stu-id="a95f4-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="a95f4-108">Jika Anda harus me-reset distribusi akuntansi, kami sarankan Anda juga menginstal 4131710 KB.</span><span class="sxs-lookup"><span data-stu-id="a95f4-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="a95f4-109">Aliran data untuk Project Service Automation dan Finance</span><span class="sxs-lookup"><span data-stu-id="a95f4-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="a95f4-110">Solusi integrasi Project Service Automation dan Finance menggunakan fitur integrasi data untuk mensinkronisasi data di seluruh instans dari Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="a95f4-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="a95f4-111">Template integrasi yang tersedia dengan fitur integrasi data memungkinkan aliran data tentang kategori transaksi pengeluaran proyek antara Finance dan Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a95f4-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="a95f4-112">Jika kategori pengeluaran proyek memiliki induk dalam Finance, aliran integrasi adalah yang pertama dari Finance hingga Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a95f4-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="a95f4-113">Id integrasi dari kategori pengeluaran proyek kemudian diperbarui melalui sinkronisasi dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="a95f4-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a95f4-114">Jika kategori pengeluaran proyek memiliki induk dalam Project Service Automation, aliran integrasi adalah yang pertama dari Project Service ke Finance.</span><span class="sxs-lookup"><span data-stu-id="a95f4-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="a95f4-115">Kategori proyek harus sudah dikonfigurasi di Finance sebelum sinkronisasi dari Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a95f4-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="a95f4-116">Kemudian sinkronisasikan dari Finance kembali ke Project Service Automation, lalu dari Project Service Automation ke Finance lagi.</span><span class="sxs-lookup"><span data-stu-id="a95f4-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="a95f4-117">Dengan cara ini, Anda membantu menjamin bahwa kategori ditautkan, dan tidak ada duplikat yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="a95f4-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="a95f4-118">Biasanya, kategori biaya proyek memiliki induk di Finance.</span><span class="sxs-lookup"><span data-stu-id="a95f4-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="a95f4-119">Namun, jika tidak, atau jika kategori pengeluaran telah dibuat dalam Project Service Automation, Anda harus terlebih dulu mensinkronisasi menggunakan template kategori pengeluaran transaksi proyek (PSA ke Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="a95f4-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="a95f4-120">Kemudian sinkronisasikan dengan menggunakan template kategori pengeluaran transaksi proyek (Fin and Ops ke PSA).</span><span class="sxs-lookup"><span data-stu-id="a95f4-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="a95f4-121">Selanjutnya, Anda harus menjalankan sinkronisasi dari Project Service Automation ke Finance sekali lagi.</span><span class="sxs-lookup"><span data-stu-id="a95f4-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="a95f4-122">Jika Anda mensinkronisasi pertama kali dari Project Service Automation, persyaratan berikut harus dipenuhi di Finance sebelum sinkronisasi dijalankan:</span><span class="sxs-lookup"><span data-stu-id="a95f4-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="a95f4-123">Kategori bersama yang cocok dengan kategori proyek yang diatur dalam Project Service Automation harus ada, dan harus diaktifkan untuk **proyek** dan **Pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="a95f4-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="a95f4-124">Untuk setiap entitas hukum Finance yang harus diintegrasikan dengannya, kategori proyek berikut harus ada:</span><span class="sxs-lookup"><span data-stu-id="a95f4-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="a95f4-125">**Kategori proyek** ada.</span><span class="sxs-lookup"><span data-stu-id="a95f4-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="a95f4-126">**Penggunaan Pengeluaran** diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="a95f4-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="a95f4-127">**Aktif dalam jurnal** diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="a95f4-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="a95f4-128">**Jenis transaksi** diatur ke **pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="a95f4-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="a95f4-129">Ilustrasi berikut menunjukkan bagaimana data disinkronisasikan antara Project Service Automation dan Finance.</span><span class="sxs-lookup"><span data-stu-id="a95f4-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="a95f4-130">[![Aliran data untuk integrasi Project Service Automation dengan Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="a95f4-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="a95f4-131">Sinkronisasi kategori pengeluaran proyek dari Finance ke Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a95f4-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a95f4-132">Template dan tugas</span><span class="sxs-lookup"><span data-stu-id="a95f4-132">Template and task</span></span>

<span data-ttu-id="a95f4-133">Untuk mengakses template, di Pusat admin Microsoft Power Apps, pilih **proyek**, lalu di sudut kanan atas, pilih **proyek baru** untuk memilih template publik.</span><span class="sxs-lookup"><span data-stu-id="a95f4-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a95f4-134">Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan kategori pengeluaran proyek dari Finance ke Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="a95f4-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="a95f4-135">**Nama template di integrasi data:** kategori transaksi pengeluaran proyek (Fin and Ops ke PSA)</span><span class="sxs-lookup"><span data-stu-id="a95f4-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="a95f4-136">**Nama tugas dalam proyek:** sinkronisasi kategori ke PSA</span><span class="sxs-lookup"><span data-stu-id="a95f4-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="a95f4-137">Rangkaian Entitas</span><span class="sxs-lookup"><span data-stu-id="a95f4-137">Entity set</span></span>

| <span data-ttu-id="a95f4-138">Keuangan</span><span class="sxs-lookup"><span data-stu-id="a95f4-138">Finance</span></span>                           | <span data-ttu-id="a95f4-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a95f4-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="a95f4-140">Entitas integrasi untuk kategori</span><span class="sxs-lookup"><span data-stu-id="a95f4-140">Integration entity for categories</span></span> | <span data-ttu-id="a95f4-141">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="a95f4-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="a95f4-142">Alur entitas</span><span class="sxs-lookup"><span data-stu-id="a95f4-142">Entity flow</span></span>

<span data-ttu-id="a95f4-143">Kategori pengeluaran proyek dikelola dalam Finance, dan disinkronisasi ke Project Service Automation sebagai kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="a95f4-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="a95f4-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="a95f4-144">Power Query</span></span>

<span data-ttu-id="a95f4-145">Bila anda mensinkronisasi ke Project Service Automation, anda harus menggunakan Microsoft Power Query untuk Excel guna mengatur jenis penagihan pada kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="a95f4-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="a95f4-146">Template kategori transaksi pengeluaran proyek (Fin and Ops ke PSA) menyediakan kolom dan pemetaan default.</span><span class="sxs-lookup"><span data-stu-id="a95f4-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="a95f4-147">Jika Anda membuat template sendiri, Anda harus menambahkan kolom kondisional di Power Query.</span><span class="sxs-lookup"><span data-stu-id="a95f4-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="a95f4-148">ikuti langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="a95f4-148">Follow these steps.</span></span>

1. <span data-ttu-id="a95f4-149">Klik tanda panah untuk membuka pemetaan tugas kategori pengeluaran proyek dalam template kategori pengeluaran transaksi (Fin and Ops ke PSA).</span><span class="sxs-lookup"><span data-stu-id="a95f4-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="a95f4-150">Klik tautan **kueri lanjutan dan filter** untuk membuka Power query.</span><span class="sxs-lookup"><span data-stu-id="a95f4-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="a95f4-151">Pilih **Tambah kolom kondisional**.</span><span class="sxs-lookup"><span data-stu-id="a95f4-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="a95f4-152">Masukkan nama untuk kolom baru, seperti **billingtype**.</span><span class="sxs-lookup"><span data-stu-id="a95f4-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="a95f4-153">Masukkan kondisi berikut: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="a95f4-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="a95f4-154">Klik **OK** pada kolom.</span><span class="sxs-lookup"><span data-stu-id="a95f4-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="a95f4-155">Pastikan untuk memetakan kolom baru ini pada halaman pemetaan.</span><span class="sxs-lookup"><span data-stu-id="a95f4-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="a95f4-156">Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data.</span><span class="sxs-lookup"><span data-stu-id="a95f4-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="a95f4-157">Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Finance ke Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a95f4-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="a95f4-158">[![Pemetaan template kategori pengeluaran proyek ke Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a95f4-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="a95f4-159">Sinkronisasi kategori pengeluaran proyek dari Project Service Automation ke Finance</span><span class="sxs-lookup"><span data-stu-id="a95f4-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="a95f4-160">Template dan tugas</span><span class="sxs-lookup"><span data-stu-id="a95f4-160">Template and task</span></span>

<span data-ttu-id="a95f4-161">Template berikut dan tugas yang mendasari digunakan untuk mensinkronisasikan kategori pengeluaran proyek dari Project Service Automation ke Finance:</span><span class="sxs-lookup"><span data-stu-id="a95f4-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="a95f4-162">**Nama template di integrasi data:** kategori transaksi pengeluaran proyek (PSA ke Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a95f4-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="a95f4-163">**Nama tugas dalam proyek:** sinkronisasi kategori ke Fin Ops</span><span class="sxs-lookup"><span data-stu-id="a95f4-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="a95f4-164">Rangkaian Entitas</span><span class="sxs-lookup"><span data-stu-id="a95f4-164">Entity set</span></span>

| <span data-ttu-id="a95f4-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="a95f4-165">Project Service Automation</span></span> | <span data-ttu-id="a95f4-166">Keuangan</span><span class="sxs-lookup"><span data-stu-id="a95f4-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="a95f4-167">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="a95f4-167">Transaction categories</span></span>     | <span data-ttu-id="a95f4-168">Entitas integrasi untuk kategori</span><span class="sxs-lookup"><span data-stu-id="a95f4-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="a95f4-169">Alur entitas</span><span class="sxs-lookup"><span data-stu-id="a95f4-169">Entity flow</span></span>

<span data-ttu-id="a95f4-170">Kategori pengeluaran proyek dikelola dalam Finance, dan disinkronisasi ke Project Service Automation sebagai kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="a95f4-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="a95f4-171">Sinkronisasi kembali ke Finance memperbarui kategori proyek di Finance dengan ID integrasi dari Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a95f4-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a95f4-172">Pemetaan template di integrasi data</span><span class="sxs-lookup"><span data-stu-id="a95f4-172">Template mapping in Data integration</span></span>

<span data-ttu-id="a95f4-173">Ilustrasi berikut menunjukkan contoh pemetaan tugas template dalam integrasi data.</span><span class="sxs-lookup"><span data-stu-id="a95f4-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="a95f4-174">Pemetaan menampilkan informasi bidang yang akan disinkronisasikan dari Project Service Automation ke Finance.</span><span class="sxs-lookup"><span data-stu-id="a95f4-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="a95f4-175">[![Pemetaan template Project Service Automation ke Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="a95f4-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
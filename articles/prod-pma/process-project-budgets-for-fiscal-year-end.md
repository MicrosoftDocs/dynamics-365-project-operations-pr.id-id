---
title: Mentransfer anggaran proyek di akhir tahun fiskal
description: Artikel ini menyediakan informasi tentang cara mentransfer sisa jumlah anggaran ke masa depan dan membuat rincian register anggaran.
author: Yowelle
ms.date: 03/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008045"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="71f0a-103">Mentransfer anggaran proyek di akhir tahun fiskal</span><span class="sxs-lookup"><span data-stu-id="71f0a-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71f0a-104">Saat mengerjakan proyek selama beberapa tahun, anda mungkin memiliki anggaran yang tersisa di akhir tahun fiskal.</span><span class="sxs-lookup"><span data-stu-id="71f0a-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="71f0a-105">Anda dapat mentransfer sisa jumlah anggaran ke tahun mendatang, dan membuat rincian register anggaran untuk jumlah di akun buku besar terkait.</span><span class="sxs-lookup"><span data-stu-id="71f0a-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="71f0a-106">Sebelum Anda meneruskan jumlah yang tersisa, tinjau dan analisis jumlah anggaran yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="71f0a-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="71f0a-107">Meninjau dan menganalisis jumlah anggaran tersisa</span><span class="sxs-lookup"><span data-stu-id="71f0a-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="71f0a-108">Selesaikan langkah-langkah berikut untuk meninjau jumlah anggaran akhir tahun untuk proyek, namun tidak meneruskan jumlah ke depan.</span><span class="sxs-lookup"><span data-stu-id="71f0a-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="71f0a-109">Buka **manajemen proyek dan akuntansi** > **periodik** > **anggaran** > **Teruskan anggaran**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="71f0a-110">Pada halaman **proses meneruskan anggaran proyek**, pada tab **pilihan akhir tahun**, verifikasikan bahwa **Teruskan jumlah anggaran proyek yang tersisa** tidak diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="71f0a-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="71f0a-111">Pada tab **parameter**, di bidang **tahun anggaran proyek**, pilih tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="71f0a-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="71f0a-112">Pada bidang **Pembukaan tahun fiskal**, pilih tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="71f0a-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="71f0a-113">Di bidang **dari model perkiraan**, pilih **anggaran tersisa**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="71f0a-114">Untuk menyertakan proyek yang memenuhi kriteria yang Anda pilih dan tidak memiliki anggaran tersisa, pilih **Tampilkan nol tersisa**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="71f0a-115">Pada tab **pilih anggaran**, pilih **ambil semua anggaran** untuk memuat semua anggaran yang sesuai dengan kriteria yang dipilih, lalu pilih **proses**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="71f0a-116">Untuk merancang kueri database yang memuat kumpulan anggaran tertentu ke dalam panel, pilih **ambil anggaran yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="71f0a-117">Untuk informasi lebih lanjut tentang baris tertentu di panel, pilih baris, lalu pilih **Lihat rincian anggaran** atau **Lihat akun**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="71f0a-118">Teruskan jumlah anggaran yang tersisa</span><span class="sxs-lookup"><span data-stu-id="71f0a-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="71f0a-119">Bila Anda memproses jumlah anggaran yang tersisa, Anda dapat membuat transaksi di buku besar untuk jumlah yang Anda teruskan.</span><span class="sxs-lookup"><span data-stu-id="71f0a-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="71f0a-120">Untuk membuat transaksi buku besar, selesaikan langkah-langkah di bagian, [Teruskan jumlah anggaran dan buat transaksi buku besar](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="71f0a-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="71f0a-121">Jumlah anggaran yang diteruskan akan ditransfer ke model perkiraan yang dipilih di halaman **model perkiraan** sebagai model perkiraan teruskan.</span><span class="sxs-lookup"><span data-stu-id="71f0a-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="71f0a-122">Meneruskan jumlah anggaran dan membuat transaksi buku besar</span><span class="sxs-lookup"><span data-stu-id="71f0a-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="71f0a-123">Pilih **manajemen proyek dan akuntansi** > **periodik** > **anggaran** > **Teruskan anggaran**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="71f0a-124">Pada halaman **proses meneruskan anggaran proyek**, pilih **akhir tahun**, lalu Aktifkan Teruskan **jumlah anggaran proyek yang tersisa**, dan **buat entri daftar anggaran dalam buku besar**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="71f0a-125">Pada tab **parameter**, di grup bidang **parameter proyek**, pilih yang berikut:</span><span class="sxs-lookup"><span data-stu-id="71f0a-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="71f0a-126">**Tahun anggaran proyek**: pilih awal tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="71f0a-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="71f0a-127">**Laba-rugi**: buat transaksi laba-rugi di buku besar.</span><span class="sxs-lookup"><span data-stu-id="71f0a-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="71f0a-128">**WIP**: membuat transaksi pekerjaan dalam proses (WIP) di buku besar.</span><span class="sxs-lookup"><span data-stu-id="71f0a-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="71f0a-129">**Penggajian**: Buat transaksi alokasi gaji di buku besar.</span><span class="sxs-lookup"><span data-stu-id="71f0a-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="71f0a-130">Pada grup bidang **Buku besar**, berikan informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="71f0a-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="71f0a-131">Pada bidang **Pembukaan tahun fiskal**, pilih tahun fiskal yang ingin anda transfer jumlah sisa anggarannya untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="71f0a-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="71f0a-132">Nilai default-nya adalah satu tahun setelah nilai dalam bidang **tahun anggaran proyek**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="71f0a-133">Di **Periode penerusan**, pilih periode yang akan dibuat rincian register anggarannya di buku besar.</span><span class="sxs-lookup"><span data-stu-id="71f0a-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="71f0a-134">Biasanya ini adalah periode pertama di pembukaan tahun fiskal.</span><span class="sxs-lookup"><span data-stu-id="71f0a-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="71f0a-135">Pada grup bidang **Salin dari/ke**, berikan informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="71f0a-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="71f0a-136">Di bidang **dari model perkiraan**, pilih model anggaran perkiraan proyek yang terkait dengan jumlah anggaran tersisa yang akan ditransfer untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="71f0a-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="71f0a-137">Di bidang **Ke model anggaran buku besar**, pilih model anggaran buku besar yang terkait dengan jumlah anggaran tersisa yang akan ditransfer ke buku besar.</span><span class="sxs-lookup"><span data-stu-id="71f0a-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="71f0a-138">Pilih **Transfer mata uang penjualan** untuk menggunakan mata uang penjualan proyek untuk transaksi buku besar umum yang dibuat saat Anda mentransfer jumlah anggaran untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="71f0a-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="71f0a-139">Bila pilihan tidak dipilih, transaksi menggunakan mata uang akuntansi.</span><span class="sxs-lookup"><span data-stu-id="71f0a-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="71f0a-140">Pilih **Tampilkan nol yang tersisa** untuk menyertakan proyek yang tidak memiliki jumlah anggaran tersisa, namun memenuhi kriteria lain yang Anda pilih di proyek yang ditampilkan di panel bawah.</span><span class="sxs-lookup"><span data-stu-id="71f0a-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="71f0a-141">Pada tab **pilih anggaran**, pilih **ambil semua anggaran** untuk memuat semua anggaran yang sesuai dengan kriteria yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="71f0a-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="71f0a-142">Jika Anda memilih untuk merancang kueri database yang memuat kumpulan anggaran proyek tertentu ke dalam panel, pilih **ambil anggaran yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="71f0a-143">Untuk setiap proyek yang akan diproses, pilih pilihan di awal baris untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="71f0a-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="71f0a-144">Untuk memilih semua atau sebagian besar proyek, pilih tanda centang di sudut kiri atas.</span><span class="sxs-lookup"><span data-stu-id="71f0a-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="71f0a-145">Untuk mengecualikan pemrosesan setiap proyek, kosongkan tanda centang untuk proyek tersebut.</span><span class="sxs-lookup"><span data-stu-id="71f0a-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="71f0a-146">Untuk mentransfer jumlah anggaran yang tersisa untuk proyek yang dipilih ke tahun fiskal yang dipilih dan membuat rincian register anggaran di buku besar, pilih **proses**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="71f0a-147">Meneruskan jumlah anggaran tanpa membuat transaksi buku besar</span><span class="sxs-lookup"><span data-stu-id="71f0a-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="71f0a-148">Buka **manajemen proyek dan akuntansi** > **periodik** > **anggaran** > **Teruskan anggaran**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="71f0a-149">Pada halaman **proses meneruskan anggaran proyek**, pada bidang **pilihan akhir tahun**, pilih **Teruskan jumlah anggaran proyek yang tersisa**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="71f0a-150">Pada grup **parameter**, di bidang **tahun anggaran proyek**, pilih tahun fiskal yang ingin anda lihat jumlah anggarannya yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="71f0a-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="71f0a-151">Pada grup **Salin dari/ke**, berikan informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="71f0a-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="71f0a-152">Di bidang **dari model perkiraan**, pilih model anggaran perkiraan proyek yang terkait dengan jumlah anggaran tersisa yang akan ditransfer untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="71f0a-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="71f0a-153">Untuk menyertakan proyek yang tidak memiliki jumlah anggaran tersisa, namun memenuhi kriteria lain yang Anda pilih, pilih **Tampilkan nol tersisa**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="71f0a-154">Pada grup **pilih anggaran**, pilih **ambil semua anggaran** untuk memuat semua anggaran yang sesuai dengan kriteria yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="71f0a-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="71f0a-155">Untuk merancang kueri database yang memuat kumpulan anggaran proyek tertentu ke dalam panel, pilih **ambil anggaran yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="71f0a-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="71f0a-156">Untuk setiap proyek yang akan diproses, pilih pilihan di awal baris untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="71f0a-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="71f0a-157">Pilih **proses** untuk mentransfer jumlah anggaran yang tersisa untuk proyek yang dipilih ke tahun fiskal yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="71f0a-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
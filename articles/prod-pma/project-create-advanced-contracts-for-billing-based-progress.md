---
title: Membuat kontrak lanjutan untuk penagihan berdasarkan progres
description: Topik ini menjelaskan cara membuat kontrak proyek sehingga anda dapat membuat faktur untuk pelanggan, berdasarkan persentase pekerjaan yang diselesaikan.
author: RadhikaRS
ms.date: 03/26/2020
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
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999675"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="69d8d-103">Membuat kontrak lanjutan untuk penagihan berdasarkan progres</span><span class="sxs-lookup"><span data-stu-id="69d8d-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="69d8d-104">Topik ini menjelaskan cara membuat kontrak proyek sehingga anda dapat membuat faktur untuk pelanggan, berdasarkan persentase pekerjaan yang diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="69d8d-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="69d8d-105">Jumlah faktur akan secara otomatis dihitung untuk kategori anggaran pekerjaan yang Anda atur untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="69d8d-106">Waktu faktur diatur saat Anda menegosiasikan kontrak proyek dengan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="69d8d-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="69d8d-107">Gunakan prosedur dalam topik ini untuk mengkonfigurasi kontrak, proyek terkait, dan aturan penagihan yang menghitung jumlah faktur untuk kategori anggaran pekerjaan yang anda atur untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="69d8d-108">Setelah membuat kontrak dan proyek, Anda dapat mengkonfigurasi rincian proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="69d8d-109">Misalnya, Anda dapat menentukan aktivitas dan menetapkan pekerja ke proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="69d8d-110">Contoh</span><span class="sxs-lookup"><span data-stu-id="69d8d-110">Example</span></span>

<span data-ttu-id="69d8d-111">Organisasi Anda adalah perusahaan pengembang perangkat lunak.</span><span class="sxs-lookup"><span data-stu-id="69d8d-111">Your organization is a software development firm.</span></span> <span data-ttu-id="69d8d-112">Anda setuju untuk mengembangkan paket akuntansi untuk pelanggan yang memiliki total biaya 20.000 dolar AS (USD).</span><span class="sxs-lookup"><span data-stu-id="69d8d-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="69d8d-113">Organisasi Anda setuju untuk menagih pelanggan setelah Anda menyelesaikan persentase spesifik proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="69d8d-114">Anda mengkonfigurasi kategori proyek berikut untuk pekerjaan tersebut, sehingga Anda dapat menggunakannya dalam proses penagihan:</span><span class="sxs-lookup"><span data-stu-id="69d8d-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="69d8d-115">Konsultasi</span><span class="sxs-lookup"><span data-stu-id="69d8d-115">Consulting</span></span>
- <span data-ttu-id="69d8d-116">Desain</span><span class="sxs-lookup"><span data-stu-id="69d8d-116">Design</span></span>
- <span data-ttu-id="69d8d-117">Penginstalan</span><span class="sxs-lookup"><span data-stu-id="69d8d-117">Installation</span></span>

<span data-ttu-id="69d8d-118">Anda juga menyiapkan aturan penagihan yang menghitung jumlah faktur secara otomatis untuk persentase pekerjaan proyek yang diselesaikan di setiap kategori.</span><span class="sxs-lookup"><span data-stu-id="69d8d-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="69d8d-119">Manajer anggaran membuat anggaran untuk kategori proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="69d8d-120">Jumlah pekerjaan yang diselesaikan secara otomatis dihitung sebagai persentase kerja aktual dibandingkan dengan jumlah yang dianggarkan.</span><span class="sxs-lookup"><span data-stu-id="69d8d-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="69d8d-121">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="69d8d-121">Prerequisites</span></span>

<span data-ttu-id="69d8d-122">Sebelum membuat proyek yang menggunakan aturan penagihan, Anda harus mengkonfigurasi urutan nomor untuk aturan penagihan dan jurnal biaya yang digunakan untuk memposting tagihan progres.</span><span class="sxs-lookup"><span data-stu-id="69d8d-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="69d8d-123">Buka **manajemen proyek dan akuntansi** \> **konfigurasi** \> **parameter manajemen proyek dan akuntansi**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="69d8d-124">Pada halaman **parameter manajemen proyek dan akuntansi**, pada tab **urutan nomor**, atur urutan nomor yang akan digunakan saat aturan penagihan dibuat.</span><span class="sxs-lookup"><span data-stu-id="69d8d-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="69d8d-125">Buka **manajemen proyek dan akuntansi** \> **Jurnal** \> **Ongkos**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="69d8d-126">Pada halaman **jurnal Ongkos**, pilih **baru**, lalu masukkan nama jurnal.</span><span class="sxs-lookup"><span data-stu-id="69d8d-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="69d8d-127">Membuat kontrak untuk tagihan Progress</span><span class="sxs-lookup"><span data-stu-id="69d8d-127">Create a contract for progress billings</span></span>

<span data-ttu-id="69d8d-128">Gunakan prosedur ini untuk membuat kontrak proyek untuk proyek harga tetap.</span><span class="sxs-lookup"><span data-stu-id="69d8d-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="69d8d-129">Anda membuat faktur proyek saat pekerjaan yang diselesaikan pada proyek mencapai persentase tertentu.</span><span class="sxs-lookup"><span data-stu-id="69d8d-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="69d8d-130">Buka **manajemen proyek dan akuntansi** \> **Proyek** \> **Kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="69d8d-131">Pada halaman **Kontrak Proyek**, pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="69d8d-132">Di kotak dialog **kontrak proyek baru**, atur bidang berikut:</span><span class="sxs-lookup"><span data-stu-id="69d8d-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="69d8d-133">**Nama**</span><span class="sxs-lookup"><span data-stu-id="69d8d-133">**Name**</span></span>
    - <span data-ttu-id="69d8d-134">**Jenis pendanaan**</span><span class="sxs-lookup"><span data-stu-id="69d8d-134">**Funding type**</span></span>
    - <span data-ttu-id="69d8d-135">**Sumber pendanaan**</span><span class="sxs-lookup"><span data-stu-id="69d8d-135">**Funding source**</span></span>
    - <span data-ttu-id="69d8d-136">**Mata uang penjualan** – secara default, mata uang ini digunakan untuk faktur Pelanggan yang terkait dengan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="69d8d-137">Namun, Anda dapat mengubah mata uang penjualan pada faktur pelanggan tertentu.</span><span class="sxs-lookup"><span data-stu-id="69d8d-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="69d8d-138">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-138">Select **OK**.</span></span> <span data-ttu-id="69d8d-139">Informasi disalin ke header halaman **kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="69d8d-140">Di halaman **kontrak proyek**, isi sisa informasi yang diperlukan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="69d8d-141">Membuat proyek untuk tagihan Progress</span><span class="sxs-lookup"><span data-stu-id="69d8d-141">Create a project for progress billings</span></span>

<span data-ttu-id="69d8d-142">Ikuti langkah berikut untuk membuat proyek dan subproyek yang terkait dengan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="69d8d-143">Buka **manajemen proyek dan akuntansi** \> **proyek** \> **Semua proyek**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="69d8d-144">Pada halaman **Semua Proyek**, pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="69d8d-145">Di kotak dialog **proyek baru**, di bidang **jenis proyek**, pilih **waktu dan material**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="69d8d-146">Pilih grup proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-146">Select a project group.</span></span> <span data-ttu-id="69d8d-147">Grup proyek menentukan informasi posting untuk proyek yang ditetapkan ke grup.</span><span class="sxs-lookup"><span data-stu-id="69d8d-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="69d8d-148">Pilih **Buat proyek baru**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-148">Select **Create project**.</span></span>
6. <span data-ttu-id="69d8d-149">Setelah proyek dibuat, atur tahapan proyek **dalam proses**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="69d8d-150">Membuat anggaran untuk sebuah proyek</span><span class="sxs-lookup"><span data-stu-id="69d8d-150">Create a budget for a project</span></span>

<span data-ttu-id="69d8d-151">Kategori anggaran digunakan untuk secara otomatis menghitung jumlah faktur untuk persentase pekerjaan yang diselesaikan untuk setiap kategori.</span><span class="sxs-lookup"><span data-stu-id="69d8d-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="69d8d-152">Ikuti langkah berikut untuk membuat kategori anggaran untuk estimasi biaya.</span><span class="sxs-lookup"><span data-stu-id="69d8d-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="69d8d-153">Buka **manajemen proyek dan akuntansi** \> **proyek** \> **Semua proyek**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="69d8d-154">Pada halaman **semua proyek**, pilih dan buka proyek yang Anda inginkan.</span><span class="sxs-lookup"><span data-stu-id="69d8d-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="69d8d-155">Pada halaman **proyek**, di panel tindakan, pada tab **rencana**, di grup **anggaran**, pilih **anggaran proyek**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="69d8d-156">Di halaman **anggaran proyek**, masukkan perkiraan biaya untuk setiap kategori dalam proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="69d8d-157">Membuat aturan penagihan untuk Tagihan Progres</span><span class="sxs-lookup"><span data-stu-id="69d8d-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="69d8d-158">Buka **manajemen proyek dan akuntansi** \> **Proyek** \> **Kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="69d8d-159">Pada halaman **kontrak proyek**, pilih dan buka kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="69d8d-160">Pada halaman kontrak proyek, pada fasttab **aturan penagihan**, pilih **Tambah**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="69d8d-161">Pada halaman **aturan penagihan**, di bidang **jenis baris**, pilih **Progres**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="69d8d-162">Pada fasttab **detail baris aturan penagihan**, di bidang **nilai kontrak**, masukkan nilai total kontrak.</span><span class="sxs-lookup"><span data-stu-id="69d8d-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="69d8d-163">Di bidang **kategori**, pilih kategori untuk memposting transaksi ongkos.</span><span class="sxs-lookup"><span data-stu-id="69d8d-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="69d8d-164">Di bidang **proyek**, pilih proyek yang menggunakan aturan penagihan ini.</span><span class="sxs-lookup"><span data-stu-id="69d8d-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="69d8d-165">Opsional: Tetapkan aturan penagihan ke proyek tambahan.</span><span class="sxs-lookup"><span data-stu-id="69d8d-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="69d8d-166">Pada fasttab **proyek**, di Bagian **proyek yang tersedia**, pilih proyek, lalu pilih tombol panah kanan untuk menambahkan proyek ke Bagian **proyek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="69d8d-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="69d8d-167">Opsional: menghitung jumlah persentase yang dipotong pelanggan dari pembayaran pada faktur.</span><span class="sxs-lookup"><span data-stu-id="69d8d-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="69d8d-168">Pada fasttab **ketentuan retensi pembayaran**, pilih sumber pendanaan, lalu di bidang **persentase retensi**, masukkan persentase retensi.</span><span class="sxs-lookup"><span data-stu-id="69d8d-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="69d8d-169">Ulangi langkah ini untuk membuat aturan penagihan tambahan untuk kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="69d8d-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Aktual
description: Topik ini menyediakan informasi topik tentang cara bekerja dengan aktual dalam Microsoft Dynamics 365 Project operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078474"
---
# <a name="actuals"></a><span data-ttu-id="3d1e8-103">Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-103">Actuals</span></span> 

<span data-ttu-id="3d1e8-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="3d1e8-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3d1e8-105">Nilai aktual adalah jumlah pekerjaan yang telah diselesaikan pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="3d1e8-106">Mereka dibuat sebagai hasil dari entri waktu dan pengeluaran, serta entri jurnal dan faktur.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="3d1e8-107">Baris jurnal dan penyerahan waktu</span><span class="sxs-lookup"><span data-stu-id="3d1e8-107">Journal lines and time submission</span></span>

<span data-ttu-id="3d1e8-108">Untuk informasi lebih lanjut tentang entri waktu, lihat [Ikhtisar entri waktu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3d1e8-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3d1e8-109">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="3d1e8-109">Time and materials</span></span>

<span data-ttu-id="3d1e8-110">Bila entri waktu yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3d1e8-111">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="3d1e8-111">Fixed price</span></span>

<span data-ttu-id="3d1e8-112">Jika entri waktu yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3d1e8-113">Harga default</span><span class="sxs-lookup"><span data-stu-id="3d1e8-113">Default pricing</span></span>

<span data-ttu-id="3d1e8-114">Logika untuk membuat harga default berada pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="3d1e8-115">Nilai bidang dari entri waktu akan disalin ke baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="3d1e8-116">Nilai ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="3d1e8-117">Bidang yang mempengaruhi harga default, seperti **peran** dan **unit organisasi** , digunakan untuk menentukan harga yang sesuai pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="3d1e8-118">Anda dapat menambahkan bidang kustom pada entri waktu.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="3d1e8-119">Jika Anda ingin nilai bidang diterapkan ke aktual, buat bidang pada entitas aktual, dan gunakan pemetaan bidang untuk menyalin bidang dari entri waktu ke aktual.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="3d1e8-120">Baris jurnal dan pengajuan pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="3d1e8-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="3d1e8-121">Untuk informasi lebih lanjut tentang entri pengeluaran, lihat [Ikhtisar pengeluaran](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3d1e8-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3d1e8-122">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="3d1e8-122">Time and materials</span></span>

<span data-ttu-id="3d1e8-123">Bila entri pengeluaran dasar yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3d1e8-124">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="3d1e8-124">Fixed price</span></span>

<span data-ttu-id="3d1e8-125">Jika entri pengeluaran dasar yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3d1e8-126">Harga default</span><span class="sxs-lookup"><span data-stu-id="3d1e8-126">Default pricing</span></span>

<span data-ttu-id="3d1e8-127">Logika untuk memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="3d1e8-128">Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="3d1e8-129">Namun, per default, jumlah yang dimasukkan untuk harga itu sendiri diatur secara langsung pada baris jurnal pengeluaran terkait untuk biaya dan penjualan.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="3d1e8-130">Entri berdasarkan Kategori dari harga default per unit pada entri pengeluaran tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="3d1e8-131">Menggunakan jurnal entri untuk mencatat biaya</span><span class="sxs-lookup"><span data-stu-id="3d1e8-131">Use entry journals to record costs</span></span>

<span data-ttu-id="3d1e8-132">Anda dapat menggunakan jurnal entri untuk merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="3d1e8-133">Jurnal dapat digunakan untuk tujuan berikut:</span><span class="sxs-lookup"><span data-stu-id="3d1e8-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="3d1e8-134">Mencatat biaya aktual material dan penjualan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="3d1e8-135">Memindahkan aktual transaksi dari sistem lain ke Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="3d1e8-136">Mencatat biaya yang terjadi di sistem lain.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="3d1e8-137">Biaya ini dapat mencakup biaya pengadaan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d1e8-138">Aplikasi tidak memvalidasi jenis baris jurnal atau harga terkait yang dimasukkan pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="3d1e8-139">Oleh karena itu, hanya pengguna yang sepenuhnya menyadari dampak akuntansi yang dimiliki aktual pada proyeklah yang harus menggunakan jurnal entri untuk membuat aktual.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="3d1e8-140">Karena dampak jenis jurnal ini, Anda harus hati-hati memilih siapa yang memiliki akses untuk membuat jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="3d1e8-141">Mencatat aktual berdasarkan aktivitas proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-141">Record actuals based on project events</span></span>

<span data-ttu-id="3d1e8-142">Project Operations mencatat transaksi keuangan yang terjadi selama proyek berlangsung.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="3d1e8-143">Transaksi ini direkam sebagai aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="3d1e8-144">Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="3d1e8-145">Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3d1e8-146">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="3d1e8-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3d1e8-147">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3d1e8-148">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="3d1e8-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3d1e8-149">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="3d1e8-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3d1e8-150">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="3d1e8-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3d1e8-151">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="3d1e8-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3d1e8-152">Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-152">Actuals</span></span></th>
<th><span data-ttu-id="3d1e8-153">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="3d1e8-153">Transaction currency</span></span></th>
<th><span data-ttu-id="3d1e8-154">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="3d1e8-154">Fixed price</span></span></th>
<th><span data-ttu-id="3d1e8-155">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="3d1e8-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3d1e8-156">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3d1e8-157">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-158">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3d1e8-159">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3d1e8-160">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3d1e8-161">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-161">Cost actual</span></span></td>
<td><span data-ttu-id="3d1e8-162">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-163">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-164">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="3d1e8-165">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-166">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-167">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="3d1e8-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3d1e8-168">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3d1e8-169">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3d1e8-170">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-170">Cost actual</span></span></td>
<td><span data-ttu-id="3d1e8-171">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-172">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-173">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-174">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-175">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-176">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="3d1e8-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3d1e8-177">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-178">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3d1e8-179">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3d1e8-180">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3d1e8-181">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3d1e8-182">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-183">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="3d1e8-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-184">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-185">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-186">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-187">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-187">Billed sales</span></span></td>
<td><span data-ttu-id="3d1e8-188">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3d1e8-189">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3d1e8-190">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3d1e8-191">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-192">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-193">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-194">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-195">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-196">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="3d1e8-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3d1e8-197">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-198">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3d1e8-199">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3d1e8-200">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3d1e8-201">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="3d1e8-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3d1e8-202">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3d1e8-203">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="3d1e8-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3d1e8-204">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="3d1e8-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3d1e8-205">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-206">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-207">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-208">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-208">Billed sales</span></span></td>
<td><span data-ttu-id="3d1e8-209">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3d1e8-210">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3d1e8-211">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="3d1e8-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3d1e8-212">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-213">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="3d1e8-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3d1e8-214">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-215">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3d1e8-216">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="3d1e8-217">Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3d1e8-218">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="3d1e8-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3d1e8-219">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3d1e8-220">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="3d1e8-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3d1e8-221">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="3d1e8-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3d1e8-222">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="3d1e8-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3d1e8-223">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="3d1e8-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3d1e8-224">Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-224">Actuals</span></span></th>
<th><span data-ttu-id="3d1e8-225">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="3d1e8-225">Transaction currency</span></span></th>
<th><span data-ttu-id="3d1e8-226">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="3d1e8-226">Fixed price</span></span></th>
<th><span data-ttu-id="3d1e8-227">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="3d1e8-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3d1e8-228">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3d1e8-229">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-230">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3d1e8-231">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3d1e8-232">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3d1e8-233">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-233">Cost actual</span></span></td>
<td><span data-ttu-id="3d1e8-234">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3d1e8-235">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3d1e8-236">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3d1e8-237">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3d1e8-238">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-239">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="3d1e8-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3d1e8-240">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-241">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="3d1e8-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3d1e8-242">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="3d1e8-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-243">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="3d1e8-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3d1e8-244">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3d1e8-245">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3d1e8-246">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-246">Cost actual</span></span></td>
<td><span data-ttu-id="3d1e8-247">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-248">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-249">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-250">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-251">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="3d1e8-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-252">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="3d1e8-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3d1e8-253">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="3d1e8-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-254">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="3d1e8-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3d1e8-255">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="3d1e8-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-256">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="3d1e8-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3d1e8-257">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-258">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3d1e8-259">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3d1e8-260">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3d1e8-261">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3d1e8-262">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-263">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="3d1e8-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-264">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-265">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3d1e8-266">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-267">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-267">Billed sales</span></span></td>
<td><span data-ttu-id="3d1e8-268">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3d1e8-269">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3d1e8-270">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3d1e8-271">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-272">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-273">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-274">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3d1e8-275">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-276">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="3d1e8-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3d1e8-277">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-278">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3d1e8-279">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3d1e8-280">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3d1e8-281">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="3d1e8-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3d1e8-282">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3d1e8-283">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="3d1e8-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3d1e8-284">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="3d1e8-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3d1e8-285">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-286">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3d1e8-287">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="3d1e8-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-288">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-288">Billed sales</span></span></td>
<td><span data-ttu-id="3d1e8-289">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3d1e8-290">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="3d1e8-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3d1e8-291">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="3d1e8-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3d1e8-292">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-293">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="3d1e8-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3d1e8-294">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3d1e8-295">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="3d1e8-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3d1e8-296">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="3d1e8-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

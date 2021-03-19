---
title: Aktual
description: Pembaruan topik ini menyediakan informasi tentang cara bekerja dengan aktual di Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291803"
---
# <a name="actuals"></a><span data-ttu-id="782e7-103">Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-103">Actuals</span></span> 

<span data-ttu-id="782e7-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="782e7-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="782e7-105">Nilai aktual adalah jumlah pekerjaan yang telah diselesaikan pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="782e7-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="782e7-106">Mereka dibuat sebagai hasil dari entri waktu dan pengeluaran, serta entri jurnal dan faktur.</span><span class="sxs-lookup"><span data-stu-id="782e7-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="782e7-107">Baris jurnal dan penyerahan waktu</span><span class="sxs-lookup"><span data-stu-id="782e7-107">Journal lines and time submission</span></span>

<span data-ttu-id="782e7-108">Untuk informasi lebih lanjut tentang entri waktu, lihat [Ikhtisar entri waktu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="782e7-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="782e7-109">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="782e7-109">Time and materials</span></span>

<span data-ttu-id="782e7-110">Bila entri waktu yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="782e7-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="782e7-111">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="782e7-111">Fixed price</span></span>

<span data-ttu-id="782e7-112">Jika entri waktu yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="782e7-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="782e7-113">Harga default</span><span class="sxs-lookup"><span data-stu-id="782e7-113">Default pricing</span></span>

<span data-ttu-id="782e7-114">Logika untuk membuat harga default berada pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="782e7-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="782e7-115">Nilai bidang dari entri waktu akan disalin ke baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="782e7-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="782e7-116">Nilai ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="782e7-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="782e7-117">Bidang yang mempengaruhi harga default, seperti **peran** dan **unit organisasi**, digunakan untuk menentukan harga yang sesuai pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="782e7-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="782e7-118">Anda dapat menambahkan bidang kustom pada entri waktu.</span><span class="sxs-lookup"><span data-stu-id="782e7-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="782e7-119">Jika Anda ingin nilai bidang diterapkan ke aktual, buat bidang pada entitas aktual, dan gunakan pemetaan bidang untuk menyalin bidang dari entri waktu ke aktual.</span><span class="sxs-lookup"><span data-stu-id="782e7-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="782e7-120">Baris jurnal dan pengajuan pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="782e7-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="782e7-121">Untuk informasi lebih lanjut tentang entri pengeluaran, lihat [Ikhtisar pengeluaran](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="782e7-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="782e7-122">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="782e7-122">Time and materials</span></span>

<span data-ttu-id="782e7-123">Bila entri pengeluaran dasar yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="782e7-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="782e7-124">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="782e7-124">Fixed price</span></span>

<span data-ttu-id="782e7-125">Jika entri pengeluaran dasar yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="782e7-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="782e7-126">Harga default</span><span class="sxs-lookup"><span data-stu-id="782e7-126">Default pricing</span></span>

<span data-ttu-id="782e7-127">Logika untuk memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="782e7-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="782e7-128">Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="782e7-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="782e7-129">Namun, per default, jumlah yang dimasukkan untuk harga itu sendiri diatur secara langsung pada baris jurnal pengeluaran terkait untuk biaya dan penjualan.</span><span class="sxs-lookup"><span data-stu-id="782e7-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="782e7-130">Entri berdasarkan Kategori dari harga default per unit pada entri pengeluaran tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="782e7-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="782e7-131">Menggunakan jurnal entri untuk mencatat biaya</span><span class="sxs-lookup"><span data-stu-id="782e7-131">Use entry journals to record costs</span></span>

<span data-ttu-id="782e7-132">Anda dapat menggunakan jurnal entri untuk merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak.</span><span class="sxs-lookup"><span data-stu-id="782e7-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="782e7-133">Jurnal dapat digunakan untuk tujuan berikut:</span><span class="sxs-lookup"><span data-stu-id="782e7-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="782e7-134">Mencatat biaya aktual material dan penjualan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="782e7-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="782e7-135">Pindahkan aktual transaksi dari sistem lain ke Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="782e7-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="782e7-136">Mencatat biaya yang terjadi di sistem lain.</span><span class="sxs-lookup"><span data-stu-id="782e7-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="782e7-137">Biaya ini dapat mencakup biaya pengadaan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="782e7-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="782e7-138">Aplikasi tidak memvalidasi jenis baris jurnal atau harga terkait yang dimasukkan pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="782e7-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="782e7-139">Oleh karena itu, hanya pengguna yang sepenuhnya menyadari dampak akuntansi yang dimiliki aktual pada proyeklah yang harus menggunakan jurnal entri untuk membuat aktual.</span><span class="sxs-lookup"><span data-stu-id="782e7-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="782e7-140">Karena dampak jenis jurnal ini, Anda harus hati-hati memilih siapa yang memiliki akses untuk membuat jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="782e7-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="782e7-141">Mencatat aktual berdasarkan aktivitas proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-141">Record actuals based on project events</span></span>

<span data-ttu-id="782e7-142">Project Operations mencatat transaksi keuangan yang terjadi selama proyek berlangsung.</span><span class="sxs-lookup"><span data-stu-id="782e7-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="782e7-143">Transaksi ini direkam sebagai aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="782e7-144">Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.</span><span class="sxs-lookup"><span data-stu-id="782e7-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="782e7-145">Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="782e7-146">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="782e7-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="782e7-147">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="782e7-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="782e7-148">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="782e7-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="782e7-149">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="782e7-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="782e7-150">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="782e7-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="782e7-151">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="782e7-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="782e7-152">Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-152">Actuals</span></span></th>
<th><span data-ttu-id="782e7-153">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="782e7-153">Transaction currency</span></span></th>
<th><span data-ttu-id="782e7-154">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="782e7-154">Fixed price</span></span></th>
<th><span data-ttu-id="782e7-155">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="782e7-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="782e7-156">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="782e7-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="782e7-157">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-158">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="782e7-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="782e7-159">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="782e7-160">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="782e7-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="782e7-161">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-161">Cost actual</span></span></td>
<td><span data-ttu-id="782e7-162">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-163">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-164">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="782e7-165">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-166">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-167">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="782e7-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="782e7-168">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="782e7-169">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="782e7-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="782e7-170">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-170">Cost actual</span></span></td>
<td><span data-ttu-id="782e7-171">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-172">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-173">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-174">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-175">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-176">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="782e7-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="782e7-177">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-178">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="782e7-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="782e7-179">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="782e7-180">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="782e7-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="782e7-181">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="782e7-182">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-183">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="782e7-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-184">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-185">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-186">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-187">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-187">Billed sales</span></span></td>
<td><span data-ttu-id="782e7-188">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="782e7-189">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="782e7-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="782e7-190">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="782e7-191">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-192">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-193">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-194">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-195">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-196">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="782e7-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="782e7-197">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-198">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="782e7-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="782e7-199">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="782e7-200">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="782e7-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="782e7-201">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="782e7-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="782e7-202">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="782e7-203">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="782e7-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="782e7-204">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="782e7-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="782e7-205">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-206">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-207">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-208">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-208">Billed sales</span></span></td>
<td><span data-ttu-id="782e7-209">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="782e7-210">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="782e7-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="782e7-211">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="782e7-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="782e7-212">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-213">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="782e7-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="782e7-214">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-215">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="782e7-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="782e7-216">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="782e7-217">Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="782e7-218">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="782e7-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="782e7-219">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="782e7-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="782e7-220">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="782e7-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="782e7-221">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="782e7-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="782e7-222">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="782e7-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="782e7-223">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="782e7-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="782e7-224">Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-224">Actuals</span></span></th>
<th><span data-ttu-id="782e7-225">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="782e7-225">Transaction currency</span></span></th>
<th><span data-ttu-id="782e7-226">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="782e7-226">Fixed price</span></span></th>
<th><span data-ttu-id="782e7-227">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="782e7-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="782e7-228">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="782e7-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="782e7-229">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-230">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="782e7-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="782e7-231">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="782e7-232">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="782e7-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="782e7-233">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-233">Cost actual</span></span></td>
<td><span data-ttu-id="782e7-234">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="782e7-235">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="782e7-236">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="782e7-237">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="782e7-238">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-239">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="782e7-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="782e7-240">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-241">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="782e7-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="782e7-242">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="782e7-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-243">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="782e7-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="782e7-244">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="782e7-245">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="782e7-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="782e7-246">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-246">Cost actual</span></span></td>
<td><span data-ttu-id="782e7-247">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-248">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-249">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-250">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-251">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="782e7-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-252">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="782e7-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="782e7-253">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="782e7-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-254">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="782e7-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="782e7-255">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="782e7-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-256">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="782e7-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="782e7-257">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-258">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="782e7-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="782e7-259">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="782e7-260">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="782e7-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="782e7-261">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="782e7-262">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-263">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="782e7-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-264">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-265">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="782e7-266">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-267">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-267">Billed sales</span></span></td>
<td><span data-ttu-id="782e7-268">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="782e7-269">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="782e7-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="782e7-270">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="782e7-271">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-272">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-273">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-274">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="782e7-275">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-276">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="782e7-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="782e7-277">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-278">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="782e7-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="782e7-279">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="782e7-280">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="782e7-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="782e7-281">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="782e7-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="782e7-282">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="782e7-283">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="782e7-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="782e7-284">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="782e7-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="782e7-285">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-286">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="782e7-287">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="782e7-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-288">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="782e7-288">Billed sales</span></span></td>
<td><span data-ttu-id="782e7-289">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="782e7-290">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="782e7-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="782e7-291">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="782e7-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="782e7-292">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-293">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="782e7-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="782e7-294">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="782e7-295">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="782e7-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="782e7-296">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="782e7-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
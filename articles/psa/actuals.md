---
title: Sekilas aktual
description: Topik ini menyediakan informasi tentang nilai aktual proyek.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368165"
---
# <a name="actuals-overview"></a><span data-ttu-id="8e264-103">Sekilas aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8e264-104">Nilai aktual adalah jumlah pekerjaan yang telah diselesaikan pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="8e264-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="8e264-105">Aktual proyek dapat ditelusuri kembali ke dokumen sumbernya.</span><span class="sxs-lookup"><span data-stu-id="8e264-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="8e264-106">Dokumen sumber mencakup waktu, pengeluaran, dan entri jurnal, serta juga faktur.</span><span class="sxs-lookup"><span data-stu-id="8e264-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Bagaimana aktual proyek dilacak ke dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="8e264-108">Mengajukan entri waktu</span><span class="sxs-lookup"><span data-stu-id="8e264-108">Submitting a time entry</span></span>

<span data-ttu-id="8e264-109">Dalam PSA, bila entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat.</span><span class="sxs-lookup"><span data-stu-id="8e264-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="8e264-110">Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="8e264-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="8e264-111">Jika entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="8e264-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="8e264-112">Logika untuk memasukkan harga default berada pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="8e264-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="8e264-113">Semua nilai bidang dari entri waktu akan disalin ke baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="8e264-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="8e264-114">Bidang ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="8e264-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="8e264-115">Bidang yang mempengaruhi harga default, seperti **peran** dan **unit organisasi**, menyebabkan harga yang sesuai untuk dimasukkan secara default pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="8e264-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="8e264-116">Jika Anda menambahkan bidang kustom pada entri waktu, dan Anda ingin nilai bidang diterapkan ke aktual, buat bidang pada entitas aktual, dan gunakan pemetaan bidang untuk menyalin bidang dari entri waktu ke aktual.</span><span class="sxs-lookup"><span data-stu-id="8e264-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="8e264-117">Mengirimkan entri pengeluaran</span><span class="sxs-lookup"><span data-stu-id="8e264-117">Submitting an expense entry</span></span>

<span data-ttu-id="8e264-118">Dalam PSA, bila entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat.</span><span class="sxs-lookup"><span data-stu-id="8e264-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="8e264-119">Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="8e264-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="8e264-120">Jika entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="8e264-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="8e264-121">Logika memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran yang dipilih pada halaman **entri pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="8e264-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="8e264-122">Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="8e264-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="8e264-123">Namun, untuk harga itu sendiri, jumlah yang dimasukkan pengguna diatur secara langsung pada baris jurnal pengeluaran terkait untuk biaya dan penjualan secara default.</span><span class="sxs-lookup"><span data-stu-id="8e264-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="8e264-124">Di versi saat ini PSA, entri berdasarkan Kategori dari harga default per unit pada entri pengeluaran tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="8e264-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="8e264-125">Menggunakan jurnal entri untuk mencatat biaya</span><span class="sxs-lookup"><span data-stu-id="8e264-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="8e264-126">Dalam PSA, jurnal entri memungkinkan Anda merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak.</span><span class="sxs-lookup"><span data-stu-id="8e264-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="8e264-127">Jurnal memiliki header, baris, dan tindakan **konfirmasi**.</span><span class="sxs-lookup"><span data-stu-id="8e264-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="8e264-128">Berikut adalah beberapa skenario di mana Anda dapat menggunakan jurnal:</span><span class="sxs-lookup"><span data-stu-id="8e264-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="8e264-129">Anda harus mencatat biaya aktual material dan penjualan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="8e264-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="8e264-130">Anda harus memindahkan aktual transaksi dari sistem lain ke PSA.</span><span class="sxs-lookup"><span data-stu-id="8e264-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="8e264-131">Anda harus mencatat biaya yang terjadi di sistem lain, seperti biaya pengadaan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="8e264-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8e264-132">Menggunakan jurnal entri untuk membuat aktual harus dilakukan hanya oleh pengguna yang sepenuhnya menyadari dampak akuntansi yang dimiliki aktual pada proyek.</span><span class="sxs-lookup"><span data-stu-id="8e264-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="8e264-133">Hal ini karena aplikasi tidak memvalidasi jenis baris jurnal, atau harga terkait yang dimasukkan pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="8e264-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="8e264-134">Karena dampak jenis jurnal ini, berhati-hatilah tentang siapa yang diberi akses untuk membuat jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="8e264-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="8e264-135">Aktual rekaman berdasarkan aktivitas proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-135">Recording actuals based on project events</span></span>

<span data-ttu-id="8e264-136">PSA mencatat transaksi keuangan yang terjadi selama proyek berlangsung.</span><span class="sxs-lookup"><span data-stu-id="8e264-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="8e264-137">Transaksi ini direkam sebagai **aktual**</span><span class="sxs-lookup"><span data-stu-id="8e264-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="8e264-138">Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.</span><span class="sxs-lookup"><span data-stu-id="8e264-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="8e264-139">**Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek**</span><span class="sxs-lookup"><span data-stu-id="8e264-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8e264-140">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="8e264-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8e264-141">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="8e264-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8e264-142">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="8e264-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8e264-143">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="8e264-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8e264-144">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="8e264-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8e264-145">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="8e264-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e264-146">Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-146">Actuals</span></span></th>
<th><span data-ttu-id="8e264-147">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="8e264-147">Transaction currency</span></span></th>
<th><span data-ttu-id="8e264-148">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="8e264-148">Fixed price</span></span></th>
<th><span data-ttu-id="8e264-149">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="8e264-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e264-150">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="8e264-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8e264-151">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-152">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="8e264-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8e264-153">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8e264-154">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="8e264-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8e264-155">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-155">Cost actual</span></span></td>
<td><span data-ttu-id="8e264-156">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-157">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-158">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="8e264-159">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-160">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-161">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="8e264-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8e264-162">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8e264-163">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="8e264-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8e264-164">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-164">Cost actual</span></span></td>
<td><span data-ttu-id="8e264-165">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-166">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-167">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-168">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-169">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-170">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="8e264-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8e264-171">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-172">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="8e264-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8e264-173">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8e264-174">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="8e264-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8e264-175">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8e264-176">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-177">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="8e264-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-178">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-179">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-180">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-181">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-181">Billed sales</span></span></td>
<td><span data-ttu-id="8e264-182">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8e264-183">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="8e264-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8e264-184">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8e264-185">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-186">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-187">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-188">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-189">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-190">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="8e264-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8e264-191">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-192">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="8e264-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8e264-193">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8e264-194">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="8e264-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8e264-195">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="8e264-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8e264-196">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8e264-197">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="8e264-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8e264-198">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="8e264-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8e264-199">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-200">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-201">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-202">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-202">Billed sales</span></span></td>
<td><span data-ttu-id="8e264-203">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8e264-204">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="8e264-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8e264-205">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="8e264-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8e264-206">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-207">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="8e264-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8e264-208">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-209">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="8e264-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8e264-210">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="8e264-211">**Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek**</span><span class="sxs-lookup"><span data-stu-id="8e264-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="8e264-212">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="8e264-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="8e264-213">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="8e264-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="8e264-214">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="8e264-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="8e264-215">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="8e264-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="8e264-216">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="8e264-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="8e264-217">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="8e264-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="8e264-218">Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-218">Actuals</span></span></th>
<th><span data-ttu-id="8e264-219">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="8e264-219">Transaction currency</span></span></th>
<th><span data-ttu-id="8e264-220">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="8e264-220">Fixed price</span></span></th>
<th><span data-ttu-id="8e264-221">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="8e264-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="8e264-222">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="8e264-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="8e264-223">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-224">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="8e264-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="8e264-225">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="8e264-226">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="8e264-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8e264-227">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-227">Cost actual</span></span></td>
<td><span data-ttu-id="8e264-228">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8e264-229">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8e264-230">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="8e264-231">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="8e264-232">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-233">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="8e264-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="8e264-234">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-235">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="8e264-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8e264-236">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="8e264-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-237">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="8e264-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8e264-238">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="8e264-239">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="8e264-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="8e264-240">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-240">Cost actual</span></span></td>
<td><span data-ttu-id="8e264-241">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-242">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-243">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-244">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-245">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="8e264-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-246">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="8e264-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="8e264-247">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="8e264-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-248">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="8e264-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="8e264-249">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="8e264-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-250">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="8e264-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8e264-251">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-252">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="8e264-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8e264-253">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8e264-254">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="8e264-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8e264-255">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8e264-256">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-257">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="8e264-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-258">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-259">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="8e264-260">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-261">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-261">Billed sales</span></span></td>
<td><span data-ttu-id="8e264-262">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8e264-263">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="8e264-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="8e264-264">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="8e264-265">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-266">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-267">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-268">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="8e264-269">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-270">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="8e264-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="8e264-271">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-272">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="8e264-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="8e264-273">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="8e264-274">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="8e264-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8e264-275">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="8e264-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8e264-276">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="8e264-277">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="8e264-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="8e264-278">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="8e264-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="8e264-279">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-280">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="8e264-281">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="8e264-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-282">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="8e264-282">Billed sales</span></span></td>
<td><span data-ttu-id="8e264-283">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="8e264-284">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="8e264-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="8e264-285">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="8e264-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="8e264-286">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-287">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="8e264-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="8e264-288">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="8e264-289">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="8e264-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="8e264-290">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="8e264-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
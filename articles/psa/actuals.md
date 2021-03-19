---
title: Sekilas aktual
description: Topik ini menyediakan informasi tentang nilai aktual proyek.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
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
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285622"
---
# <a name="actuals-overview"></a><span data-ttu-id="47519-103">Sekilas aktual</span><span class="sxs-lookup"><span data-stu-id="47519-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="47519-104">Nilai aktual adalah jumlah pekerjaan yang telah diselesaikan pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="47519-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="47519-105">Aktual proyek dapat ditelusuri kembali ke dokumen sumbernya.</span><span class="sxs-lookup"><span data-stu-id="47519-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="47519-106">Dokumen sumber mencakup waktu, pengeluaran, dan entri jurnal, serta juga faktur.</span><span class="sxs-lookup"><span data-stu-id="47519-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Bagaimana aktual proyek dilacak ke dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="47519-108">Mengajukan entri waktu</span><span class="sxs-lookup"><span data-stu-id="47519-108">Submitting a time entry</span></span>

<span data-ttu-id="47519-109">Dalam PSA, bila entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat.</span><span class="sxs-lookup"><span data-stu-id="47519-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="47519-110">Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="47519-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="47519-111">Jika entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="47519-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="47519-112">Logika untuk memasukkan harga default berada pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="47519-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="47519-113">Semua nilai bidang dari entri waktu akan disalin ke baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="47519-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="47519-114">Bidang ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="47519-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="47519-115">Bidang yang mempengaruhi harga default, seperti **peran** dan **unit organisasi**, menyebabkan harga yang sesuai untuk dimasukkan secara default pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="47519-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="47519-116">Jika Anda menambahkan bidang kustom pada entri waktu, dan Anda ingin nilai bidang diterapkan ke aktual, buat bidang pada entitas aktual, dan gunakan pemetaan bidang untuk menyalin bidang dari entri waktu ke aktual.</span><span class="sxs-lookup"><span data-stu-id="47519-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="47519-117">Mengirimkan entri pengeluaran</span><span class="sxs-lookup"><span data-stu-id="47519-117">Submitting an expense entry</span></span>

<span data-ttu-id="47519-118">Dalam PSA, bila entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat.</span><span class="sxs-lookup"><span data-stu-id="47519-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="47519-119">Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="47519-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="47519-120">Jika entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="47519-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="47519-121">Logika memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran yang dipilih pada halaman **entri pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="47519-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="47519-122">Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="47519-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="47519-123">Namun, untuk harga itu sendiri, jumlah yang dimasukkan pengguna diatur secara langsung pada baris jurnal pengeluaran terkait untuk biaya dan penjualan secara default.</span><span class="sxs-lookup"><span data-stu-id="47519-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="47519-124">Di versi saat ini PSA, entri berdasarkan Kategori dari harga default per unit pada entri pengeluaran tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="47519-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="47519-125">Menggunakan jurnal entri untuk mencatat biaya</span><span class="sxs-lookup"><span data-stu-id="47519-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="47519-126">Dalam PSA, jurnal entri memungkinkan Anda merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak.</span><span class="sxs-lookup"><span data-stu-id="47519-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="47519-127">Jurnal memiliki header, baris, dan tindakan **konfirmasi**.</span><span class="sxs-lookup"><span data-stu-id="47519-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="47519-128">Berikut adalah beberapa skenario di mana Anda dapat menggunakan jurnal:</span><span class="sxs-lookup"><span data-stu-id="47519-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="47519-129">Anda harus mencatat biaya aktual material dan penjualan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="47519-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="47519-130">Anda harus memindahkan aktual transaksi dari sistem lain ke PSA.</span><span class="sxs-lookup"><span data-stu-id="47519-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="47519-131">Anda harus mencatat biaya yang terjadi di sistem lain, seperti biaya pengadaan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="47519-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="47519-132">Menggunakan jurnal entri untuk membuat aktual harus dilakukan hanya oleh pengguna yang sepenuhnya menyadari dampak akuntansi yang dimiliki aktual pada proyek.</span><span class="sxs-lookup"><span data-stu-id="47519-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="47519-133">Hal ini karena aplikasi tidak memvalidasi jenis baris jurnal, atau harga terkait yang dimasukkan pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="47519-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="47519-134">Karena dampak jenis jurnal ini, berhati-hatilah tentang siapa yang diberi akses untuk membuat jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="47519-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="47519-135">Aktual rekaman berdasarkan aktivitas proyek</span><span class="sxs-lookup"><span data-stu-id="47519-135">Recording actuals based on project events</span></span>

<span data-ttu-id="47519-136">PSA mencatat transaksi keuangan yang terjadi selama proyek berlangsung.</span><span class="sxs-lookup"><span data-stu-id="47519-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="47519-137">Transaksi ini direkam sebagai **aktual**</span><span class="sxs-lookup"><span data-stu-id="47519-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="47519-138">Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.</span><span class="sxs-lookup"><span data-stu-id="47519-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="47519-139">**Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek**</span><span class="sxs-lookup"><span data-stu-id="47519-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="47519-140">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="47519-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="47519-141">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="47519-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="47519-142">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="47519-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="47519-143">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="47519-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="47519-144">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="47519-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="47519-145">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="47519-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="47519-146">Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-146">Actuals</span></span></th>
<th><span data-ttu-id="47519-147">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="47519-147">Transaction currency</span></span></th>
<th><span data-ttu-id="47519-148">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="47519-148">Fixed price</span></span></th>
<th><span data-ttu-id="47519-149">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="47519-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="47519-150">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="47519-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="47519-151">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="47519-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-152">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="47519-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="47519-153">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="47519-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="47519-154">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="47519-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="47519-155">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-155">Cost actual</span></span></td>
<td><span data-ttu-id="47519-156">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-157">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-158">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="47519-159">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-160">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-161">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="47519-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="47519-162">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="47519-163">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="47519-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="47519-164">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-164">Cost actual</span></span></td>
<td><span data-ttu-id="47519-165">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-166">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-167">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-168">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-169">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-170">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="47519-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="47519-171">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-172">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="47519-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="47519-173">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="47519-174">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="47519-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="47519-175">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="47519-176">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-177">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="47519-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-178">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-179">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-180">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-181">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-181">Billed sales</span></span></td>
<td><span data-ttu-id="47519-182">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="47519-183">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="47519-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="47519-184">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="47519-185">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-186">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-187">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-188">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-189">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-190">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="47519-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="47519-191">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-192">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="47519-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="47519-193">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="47519-194">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="47519-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="47519-195">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="47519-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="47519-196">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="47519-197">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="47519-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="47519-198">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="47519-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="47519-199">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-200">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-201">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-202">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-202">Billed sales</span></span></td>
<td><span data-ttu-id="47519-203">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="47519-204">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="47519-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="47519-205">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="47519-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="47519-206">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-207">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="47519-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="47519-208">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-209">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="47519-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="47519-210">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="47519-211">**Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek**</span><span class="sxs-lookup"><span data-stu-id="47519-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="47519-212">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="47519-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="47519-213">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="47519-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="47519-214">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="47519-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="47519-215">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="47519-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="47519-216">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="47519-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="47519-217">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="47519-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="47519-218">Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-218">Actuals</span></span></th>
<th><span data-ttu-id="47519-219">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="47519-219">Transaction currency</span></span></th>
<th><span data-ttu-id="47519-220">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="47519-220">Fixed price</span></span></th>
<th><span data-ttu-id="47519-221">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="47519-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="47519-222">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="47519-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="47519-223">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="47519-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-224">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="47519-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="47519-225">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="47519-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="47519-226">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="47519-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="47519-227">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-227">Cost actual</span></span></td>
<td><span data-ttu-id="47519-228">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="47519-229">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="47519-230">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="47519-231">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="47519-232">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-233">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="47519-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="47519-234">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-235">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="47519-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="47519-236">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="47519-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-237">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="47519-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="47519-238">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="47519-239">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="47519-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="47519-240">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-240">Cost actual</span></span></td>
<td><span data-ttu-id="47519-241">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-242">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-243">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-244">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-245">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="47519-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-246">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="47519-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="47519-247">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="47519-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-248">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="47519-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="47519-249">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="47519-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-250">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="47519-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="47519-251">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-252">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="47519-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="47519-253">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="47519-254">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="47519-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="47519-255">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="47519-256">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-257">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="47519-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-258">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-259">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="47519-260">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-261">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-261">Billed sales</span></span></td>
<td><span data-ttu-id="47519-262">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="47519-263">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="47519-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="47519-264">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="47519-265">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-266">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-267">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-268">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="47519-269">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-270">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="47519-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="47519-271">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-272">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="47519-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="47519-273">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="47519-274">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="47519-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="47519-275">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="47519-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="47519-276">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="47519-277">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="47519-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="47519-278">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="47519-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="47519-279">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-280">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="47519-281">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="47519-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-282">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="47519-282">Billed sales</span></span></td>
<td><span data-ttu-id="47519-283">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="47519-284">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="47519-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="47519-285">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="47519-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="47519-286">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-287">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="47519-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="47519-288">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="47519-289">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="47519-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="47519-290">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="47519-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
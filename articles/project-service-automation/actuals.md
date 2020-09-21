---
title: Aktual
description: Topik ini menyediakan informasi tentang nilai aktual proyek.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752498"
---
# <a name="actuals"></a><span data-ttu-id="81900-103">Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="81900-104">Nilai aktual adalah jumlah pekerjaan yang telah diselesaikan pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="81900-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="81900-105">Aktual proyek dapat ditelusuri kembali ke dokumen sumbernya.</span><span class="sxs-lookup"><span data-stu-id="81900-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="81900-106">Dokumen sumber mencakup waktu, pengeluaran, dan entri jurnal, serta juga faktur.</span><span class="sxs-lookup"><span data-stu-id="81900-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Bagaimana aktual proyek dilacak ke dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="81900-108">Mengajukan entri waktu</span><span class="sxs-lookup"><span data-stu-id="81900-108">Submitting a time entry</span></span>

<span data-ttu-id="81900-109">Dalam PSA, bila entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat.</span><span class="sxs-lookup"><span data-stu-id="81900-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="81900-110">Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="81900-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="81900-111">Jika entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="81900-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="81900-112">Logika untuk memasukkan harga default berada pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="81900-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="81900-113">Semua nilai bidang dari entri waktu akan disalin ke baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="81900-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="81900-114">Bidang ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="81900-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="81900-115">Bidang yang mempengaruhi harga default, seperti **peran** dan **unit organisasi**, menyebabkan harga yang sesuai untuk dimasukkan secara default pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="81900-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="81900-116">Jika Anda menambahkan bidang kustom pada entri waktu, dan Anda ingin nilai bidang diterapkan ke aktual, buat bidang pada entitas aktual, dan gunakan pemetaan bidang untuk menyalin bidang dari entri waktu ke aktual.</span><span class="sxs-lookup"><span data-stu-id="81900-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="81900-117">Mengirimkan entri pengeluaran</span><span class="sxs-lookup"><span data-stu-id="81900-117">Submitting an expense entry</span></span>

<span data-ttu-id="81900-118">Dalam PSA, bila entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat.</span><span class="sxs-lookup"><span data-stu-id="81900-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="81900-119">Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="81900-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="81900-120">Jika entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="81900-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="81900-121">Logika memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran yang dipilih pada halaman **entri pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="81900-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="81900-122">Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="81900-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="81900-123">Namun, untuk harga itu sendiri, jumlah yang dimasukkan pengguna diatur secara langsung pada baris jurnal pengeluaran terkait untuk biaya dan penjualan secara default.</span><span class="sxs-lookup"><span data-stu-id="81900-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="81900-124">Di versi saat ini PSA, entri berdasarkan Kategori dari harga default per unit pada entri pengeluaran tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="81900-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="81900-125">Menggunakan jurnal untuk mencatat biaya</span><span class="sxs-lookup"><span data-stu-id="81900-125">Using journals to record costs</span></span>

<span data-ttu-id="81900-126">Dalam PSA, jurnal memungkinkan Anda merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak.</span><span class="sxs-lookup"><span data-stu-id="81900-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="81900-127">Jurnal memiliki header, baris, dan tindakan **konfirmasi**.</span><span class="sxs-lookup"><span data-stu-id="81900-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="81900-128">Berikut adalah beberapa skenario di mana Anda dapat menggunakan jurnal:</span><span class="sxs-lookup"><span data-stu-id="81900-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="81900-129">Anda harus mencatat biaya aktual material dan penjualan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="81900-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="81900-130">Anda harus memindahkan aktual transaksi dari sistem lain ke PSA.</span><span class="sxs-lookup"><span data-stu-id="81900-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="81900-131">Anda harus mencatat biaya yang terjadi di sistem lain, seperti biaya pengadaan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="81900-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="81900-132">Aktual rekaman berdasarkan aktivitas proyek</span><span class="sxs-lookup"><span data-stu-id="81900-132">Recording actuals based on project events</span></span>

<span data-ttu-id="81900-133">PSA mencatat transaksi keuangan yang terjadi selama proyek berlangsung.</span><span class="sxs-lookup"><span data-stu-id="81900-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="81900-134">Transaksi ini direkam sebagai **aktual**</span><span class="sxs-lookup"><span data-stu-id="81900-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="81900-135">Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.</span><span class="sxs-lookup"><span data-stu-id="81900-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="81900-136">**Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek**</span><span class="sxs-lookup"><span data-stu-id="81900-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="81900-137">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="81900-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="81900-138">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="81900-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="81900-139">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="81900-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="81900-140">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="81900-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="81900-141">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="81900-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="81900-142">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="81900-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="81900-143">Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-143">Actuals</span></span></th>
<th><span data-ttu-id="81900-144">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="81900-144">Transaction currency</span></span></th>
<th><span data-ttu-id="81900-145">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="81900-145">Fixed price</span></span></th>
<th><span data-ttu-id="81900-146">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="81900-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81900-147">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="81900-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="81900-148">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="81900-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-149">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="81900-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="81900-150">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="81900-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81900-151">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="81900-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81900-152">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-152">Cost actual</span></span></td>
<td><span data-ttu-id="81900-153">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-154">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-155">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="81900-156">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-157">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-158">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="81900-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="81900-159">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81900-160">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="81900-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81900-161">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-161">Cost actual</span></span></td>
<td><span data-ttu-id="81900-162">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-163">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-164">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-165">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-166">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-167">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="81900-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81900-168">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-169">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="81900-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81900-170">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81900-171">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="81900-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81900-172">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81900-173">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-174">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="81900-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-175">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-176">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-177">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-178">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-178">Billed sales</span></span></td>
<td><span data-ttu-id="81900-179">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81900-180">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="81900-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81900-181">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81900-182">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-183">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-184">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-185">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-186">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-187">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="81900-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81900-188">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-189">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="81900-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81900-190">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81900-191">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="81900-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81900-192">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="81900-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81900-193">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="81900-194">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="81900-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="81900-195">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="81900-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="81900-196">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-197">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-198">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-199">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-199">Billed sales</span></span></td>
<td><span data-ttu-id="81900-200">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81900-201">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="81900-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81900-202">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="81900-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81900-203">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-204">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="81900-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="81900-205">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-206">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="81900-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="81900-207">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="81900-208">**Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek**</span><span class="sxs-lookup"><span data-stu-id="81900-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="81900-209">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="81900-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="81900-210">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="81900-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="81900-211">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="81900-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="81900-212">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="81900-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="81900-213">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="81900-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="81900-214">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="81900-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="81900-215">Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-215">Actuals</span></span></th>
<th><span data-ttu-id="81900-216">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="81900-216">Transaction currency</span></span></th>
<th><span data-ttu-id="81900-217">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="81900-217">Fixed price</span></span></th>
<th><span data-ttu-id="81900-218">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="81900-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="81900-219">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="81900-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="81900-220">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="81900-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-221">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="81900-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="81900-222">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="81900-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="81900-223">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="81900-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81900-224">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-224">Cost actual</span></span></td>
<td><span data-ttu-id="81900-225">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="81900-226">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="81900-227">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="81900-228">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="81900-229">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-230">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="81900-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="81900-231">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-232">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="81900-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="81900-233">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="81900-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-234">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="81900-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="81900-235">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="81900-236">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="81900-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="81900-237">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-237">Cost actual</span></span></td>
<td><span data-ttu-id="81900-238">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-239">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-240">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-241">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-242">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="81900-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-243">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="81900-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="81900-244">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="81900-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-245">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="81900-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="81900-246">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="81900-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-247">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="81900-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81900-248">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-249">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="81900-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81900-250">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81900-251">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="81900-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81900-252">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81900-253">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-254">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="81900-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-255">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-256">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="81900-257">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-258">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-258">Billed sales</span></span></td>
<td><span data-ttu-id="81900-259">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81900-260">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="81900-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="81900-261">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="81900-262">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-263">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-264">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-265">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="81900-266">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-267">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="81900-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="81900-268">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-269">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="81900-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="81900-270">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="81900-271">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="81900-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81900-272">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="81900-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81900-273">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="81900-274">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="81900-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="81900-275">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="81900-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="81900-276">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-277">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="81900-278">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="81900-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-279">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="81900-279">Billed sales</span></span></td>
<td><span data-ttu-id="81900-280">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="81900-281">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="81900-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="81900-282">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="81900-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="81900-283">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-284">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="81900-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="81900-285">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="81900-286">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="81900-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="81900-287">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="81900-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

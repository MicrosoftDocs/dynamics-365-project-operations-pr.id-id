---
title: Aktual
description: Pembaruan topik ini menyediakan informasi tentang cara bekerja dengan aktual di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996615"
---
# <a name="actuals"></a><span data-ttu-id="faee0-103">Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-103">Actuals</span></span> 

<span data-ttu-id="faee0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="faee0-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="faee0-105">Aktual menunjukkan progres keuangan dan jadwal yang ditinjau dan disetujui pada proyek.</span><span class="sxs-lookup"><span data-stu-id="faee0-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="faee0-106">Entri dibuat sebagai hasil dari persetujuan waktu, pengeluaran, entri penggunaan bahan, serta entri jurnal dan faktur.</span><span class="sxs-lookup"><span data-stu-id="faee0-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="faee0-107">Baris jurnal dan penyerahan waktu</span><span class="sxs-lookup"><span data-stu-id="faee0-107">Journal lines and time submission</span></span>

<span data-ttu-id="faee0-108">Untuk informasi lebih lanjut tentang entri waktu, lihat [Ikhtisar entri waktu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="faee0-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="faee0-109">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="faee0-109">Time and materials</span></span>

<span data-ttu-id="faee0-110">Bila entri waktu yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="faee0-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="faee0-111">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="faee0-111">Fixed price</span></span>

<span data-ttu-id="faee0-112">Jika entri waktu yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="faee0-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="faee0-113">Harga default</span><span class="sxs-lookup"><span data-stu-id="faee0-113">Default pricing</span></span>

<span data-ttu-id="faee0-114">Logika untuk membuat harga default berada pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="faee0-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="faee0-115">Nilai bidang dari entri waktu akan disalin ke baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="faee0-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="faee0-116">Nilai ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="faee0-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="faee0-117">Bidang yang mempengaruhi harga default, seperti **peran** dan **unit sumber daya**, digunakan untuk menentukan harga yang sesuai untuk dimasukkan secara default pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="faee0-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="faee0-118">Anda dapat menambahkan bidang kustom pada entri waktu.</span><span class="sxs-lookup"><span data-stu-id="faee0-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="faee0-119">Jika Anda menginginkan nilai bidang disebarkan ke aktual, buat bidang dalam tabel **Aktual** dan **Baris Jurnal**.</span><span class="sxs-lookup"><span data-stu-id="faee0-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="faee0-120">Gunakan kode kustom untuk menyebarkan nilai bidang yang dipilih dari Entri Waktu ke Aktual melalui baris jurnal menggunakan asal transaksi.</span><span class="sxs-lookup"><span data-stu-id="faee0-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="faee0-121">Untuk informasi lebih lanjut tentang asal transaksi dan koneksi, lihat [Menautkan Aktual ke rekaman asli](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="faee0-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="faee0-122">Baris jurnal dan pengajuan pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="faee0-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="faee0-123">Untuk informasi lebih lanjut tentang entri pengeluaran, lihat [Ikhtisar pengeluaran](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="faee0-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="faee0-124">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="faee0-124">Time and materials</span></span>

<span data-ttu-id="faee0-125">Bila entri pengeluaran dasar yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.</span><span class="sxs-lookup"><span data-stu-id="faee0-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="faee0-126">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="faee0-126">Fixed price</span></span>

<span data-ttu-id="faee0-127">Jika entri pengeluaran dasar yang diajukan ditautkan ke suatu proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="faee0-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="faee0-128">Harga default</span><span class="sxs-lookup"><span data-stu-id="faee0-128">Default pricing</span></span>

<span data-ttu-id="faee0-129">Logika untuk memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="faee0-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="faee0-130">Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="faee0-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="faee0-131">Bidang yang mempengaruhi harga default, seperti **Kategori transaksi** dan **unit**, digunakan untuk menentukan harga yang sesuai untuk dimasukkan secara default pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="faee0-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="faee0-132">Namun, hal ini hanya berfungsi bila metode harga dalam daftar harga adalah **Harga per unit**.</span><span class="sxs-lookup"><span data-stu-id="faee0-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="faee0-133">Jika metode harga **Pada biaya** atau **Markup atas biaya**, harga yang dimasukkan saat entri pengeluaran dibuat akan digunakan untuk biaya dan harga pada baris jurnal penjualan dihitung berdasarkan metode penetapan harga.</span><span class="sxs-lookup"><span data-stu-id="faee0-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="faee0-134">Anda dapat menambahkan bidang kustom pada entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="faee0-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="faee0-135">Jika Anda menginginkan nilai bidang disebarkan ke aktual, buat bidang dalam tabel **Aktual** dan **Baris Jurnal**.</span><span class="sxs-lookup"><span data-stu-id="faee0-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="faee0-136">Gunakan kode kustom untuk menyebarkan nilai bidang yang dipilih dari Entri Waktu ke Aktual melalui baris jurnal menggunakan asal transaksi.</span><span class="sxs-lookup"><span data-stu-id="faee0-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="faee0-137">Untuk informasi lebih lanjut tentang asal transaksi dan koneksi, lihat [Menautkan Aktual ke rekaman asli](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="faee0-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="faee0-138">Pengajuan Baris jurnal dan log penggunaan bahan</span><span class="sxs-lookup"><span data-stu-id="faee0-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="faee0-139">Untuk informasi lebih lanjut tentang entri pengeluaran, lihat [Log Penggunaan Bahan](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="faee0-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="faee0-140">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="faee0-140">Time and materials</span></span>

<span data-ttu-id="faee0-141">Bila entri log penggunaan bahan yang diajukan ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan bahan, sistem membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum tertagih.</span><span class="sxs-lookup"><span data-stu-id="faee0-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="faee0-142">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="faee0-142">Fixed price</span></span>

<span data-ttu-id="faee0-143">Jika entri log penggunaan bahan yang diajukan ditautkan ke suatu proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="faee0-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="faee0-144">Harga default</span><span class="sxs-lookup"><span data-stu-id="faee0-144">Default pricing</span></span>

<span data-ttu-id="faee0-145">Logika untuk memasukkan harga default untuk bahan didasarkan pada kombinasi produk dan unit.</span><span class="sxs-lookup"><span data-stu-id="faee0-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="faee0-146">Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="faee0-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="faee0-147">Bidang yang mempengaruhi harga default, seperti **ID produk** dan **unit**, digunakan untuk menentukan harga yang sesuai untuk dimasukkan secara default pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="faee0-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="faee0-148">Namun, ini hanya berfungsi untuk produk katalog.</span><span class="sxs-lookup"><span data-stu-id="faee0-148">However, this only works for catalog products.</span></span> <span data-ttu-id="faee0-149">Untuk produk pilihan, harga yang dimasukkan saat entri log penggunaan bahan dibuat digunakan untuk biaya dan harga penjualan di baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="faee0-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="faee0-150">Anda dapat menambahkan bidang kustom pada entri **Log Penggunaan Bahan**.</span><span class="sxs-lookup"><span data-stu-id="faee0-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="faee0-151">Jika Anda menginginkan nilai bidang disebarkan ke aktual, buat bidang dalam tabel **Aktual** dan **Baris Jurnal**.</span><span class="sxs-lookup"><span data-stu-id="faee0-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="faee0-152">Gunakan kode kustom untuk menyebarkan nilai bidang yang dipilih dari Entri Waktu ke Aktual melalui baris jurnal menggunakan asal transaksi.</span><span class="sxs-lookup"><span data-stu-id="faee0-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="faee0-153">Untuk informasi lebih lanjut tentang asal transaksi dan koneksi, lihat [Menautkan Aktual ke rekaman asli](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="faee0-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="faee0-154">Menggunakan jurnal entri untuk mencatat biaya</span><span class="sxs-lookup"><span data-stu-id="faee0-154">Use entry journals to record costs</span></span>

<span data-ttu-id="faee0-155">Anda dapat menggunakan jurnal entri untuk merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak.</span><span class="sxs-lookup"><span data-stu-id="faee0-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="faee0-156">Jurnal dapat digunakan untuk tujuan berikut:</span><span class="sxs-lookup"><span data-stu-id="faee0-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="faee0-157">Pindahkan aktual transaksi dari sistem lain ke Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="faee0-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="faee0-158">Mencatat biaya yang terjadi di sistem lain.</span><span class="sxs-lookup"><span data-stu-id="faee0-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="faee0-159">Biaya ini dapat mencakup biaya pengadaan atau subkontrak.</span><span class="sxs-lookup"><span data-stu-id="faee0-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="faee0-160">Aplikasi tidak memvalidasi jenis baris jurnal atau harga terkait yang dimasukkan pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="faee0-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="faee0-161">Oleh karena itu, hanya pengguna yang sepenuhnya menyadari dampak akuntansi yang dimiliki aktual pada proyeklah yang harus menggunakan jurnal entri untuk membuat aktual.</span><span class="sxs-lookup"><span data-stu-id="faee0-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="faee0-162">Karena dampak jenis jurnal ini, Anda harus hati-hati memilih siapa yang memiliki akses untuk membuat jurnal entri.</span><span class="sxs-lookup"><span data-stu-id="faee0-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="faee0-163">Mencatat aktual berdasarkan aktivitas proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-163">Record actuals based on project events</span></span>

<span data-ttu-id="faee0-164">Project Operations mencatat transaksi keuangan yang terjadi selama proyek berlangsung.</span><span class="sxs-lookup"><span data-stu-id="faee0-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="faee0-165">Transaksi ini direkam sebagai aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="faee0-166">Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.</span><span class="sxs-lookup"><span data-stu-id="faee0-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="faee0-167">Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="faee0-168">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="faee0-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="faee0-169">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="faee0-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="faee0-170">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="faee0-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="faee0-171">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="faee0-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="faee0-172">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="faee0-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="faee0-173">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="faee0-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="faee0-174">Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-174">Actuals</span></span></th>
<th><span data-ttu-id="faee0-175">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="faee0-175">Transaction currency</span></span></th>
<th><span data-ttu-id="faee0-176">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="faee0-176">Fixed price</span></span></th>
<th><span data-ttu-id="faee0-177">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="faee0-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faee0-178">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="faee0-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="faee0-179">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-180">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="faee0-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="faee0-181">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="faee0-182">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="faee0-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="faee0-183">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-183">Cost actual</span></span></td>
<td><span data-ttu-id="faee0-184">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-185">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-186">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="faee0-187">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-188">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-189">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="faee0-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="faee0-190">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="faee0-191">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="faee0-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="faee0-192">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-192">Cost actual</span></span></td>
<td><span data-ttu-id="faee0-193">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-194">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-195">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-196">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-197">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-198">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="faee0-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="faee0-199">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-200">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="faee0-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="faee0-201">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="faee0-202">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="faee0-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="faee0-203">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="faee0-204">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-205">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="faee0-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-206">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-207">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-208">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-209">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-209">Billed sales</span></span></td>
<td><span data-ttu-id="faee0-210">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="faee0-211">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="faee0-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="faee0-212">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="faee0-213">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-214">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-215">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-216">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-217">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-218">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="faee0-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="faee0-219">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-220">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="faee0-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="faee0-221">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="faee0-222">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="faee0-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="faee0-223">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="faee0-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="faee0-224">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="faee0-225">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="faee0-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="faee0-226">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="faee0-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="faee0-227">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-228">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-229">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-230">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-230">Billed sales</span></span></td>
<td><span data-ttu-id="faee0-231">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="faee0-232">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="faee0-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="faee0-233">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="faee0-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="faee0-234">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-235">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="faee0-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="faee0-236">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-237">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="faee0-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="faee0-238">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="faee0-239">Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="faee0-240">Aktivitas</span><span class="sxs-lookup"><span data-stu-id="faee0-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="faee0-241">Proyek yang dapat ditagih atau dijual</span><span class="sxs-lookup"><span data-stu-id="faee0-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="faee0-242">Proyek dalam tahap pra-penjualan</span><span class="sxs-lookup"><span data-stu-id="faee0-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="faee0-243">Proyek internal</span><span class="sxs-lookup"><span data-stu-id="faee0-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="faee0-244">Waktu dan Material</span><span class="sxs-lookup"><span data-stu-id="faee0-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="faee0-245">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="faee0-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="faee0-246">Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-246">Actuals</span></span></th>
<th><span data-ttu-id="faee0-247">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="faee0-247">Transaction currency</span></span></th>
<th><span data-ttu-id="faee0-248">Harga Tetap</span><span class="sxs-lookup"><span data-stu-id="faee0-248">Fixed price</span></span></th>
<th><span data-ttu-id="faee0-249">mata uang transaksi</span><span class="sxs-lookup"><span data-stu-id="faee0-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="faee0-250">Entri Waktu dibuat.</span><span class="sxs-lookup"><span data-stu-id="faee0-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="faee0-251">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-252">Entri Waktu diajukan.</span><span class="sxs-lookup"><span data-stu-id="faee0-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="faee0-253">Tidak ada aktivitas di entitas aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="faee0-254">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="faee0-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="faee0-255">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-255">Cost actual</span></span></td>
<td><span data-ttu-id="faee0-256">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="faee0-257">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="faee0-258">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="faee0-259">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="faee0-260">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-261">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="faee0-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="faee0-262">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-263">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="faee0-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="faee0-264">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="faee0-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-265">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="faee0-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="faee0-266">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="faee0-267">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</span><span class="sxs-lookup"><span data-stu-id="faee0-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="faee0-268">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-268">Cost actual</span></span></td>
<td><span data-ttu-id="faee0-269">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-270">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-271">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-272">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-273">Biaya Aktual</span><span class="sxs-lookup"><span data-stu-id="faee0-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-274">Biaya Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="faee0-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="faee0-275">Mata uang Unit Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="faee0-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-276">Penjualan Interorganisasi</span><span class="sxs-lookup"><span data-stu-id="faee0-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="faee0-277">Mata uang Unit Kontrak</span><span class="sxs-lookup"><span data-stu-id="faee0-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-278">Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="faee0-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="faee0-279">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-280">Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="faee0-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="faee0-281">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="faee0-282">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="faee0-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="faee0-283">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="faee0-284">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-285">Penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="faee0-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-286">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-287">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="faee0-288">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-289">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-289">Billed sales</span></span></td>
<td><span data-ttu-id="faee0-290">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="faee0-291">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</span><span class="sxs-lookup"><span data-stu-id="faee0-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="faee0-292">Pembalikan penjualan yang tidak ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="faee0-293">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-294">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-295">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-296">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="faee0-297">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-298">Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="faee0-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="faee0-299">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-300">Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="faee0-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="faee0-301">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="faee0-302">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="faee0-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="faee0-303">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="faee0-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="faee0-304">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="faee0-305">Pembalikan penjualan yang ditagih untuk tonggak waktu</span><span class="sxs-lookup"><span data-stu-id="faee0-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="faee0-306">Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></span><span class="sxs-lookup"><span data-stu-id="faee0-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="faee0-307">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-308">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="faee0-309">Tidak berlaku</span><span class="sxs-lookup"><span data-stu-id="faee0-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-310">Penjualan yang Ditagih</span><span class="sxs-lookup"><span data-stu-id="faee0-310">Billed sales</span></span></td>
<td><span data-ttu-id="faee0-311">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="faee0-312">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</span><span class="sxs-lookup"><span data-stu-id="faee0-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="faee0-313">penjualan tertagih – Pembalikan</span><span class="sxs-lookup"><span data-stu-id="faee0-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="faee0-314">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-315">Penjualan Tertagih untuk kuantitas baru</span><span class="sxs-lookup"><span data-stu-id="faee0-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="faee0-316">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="faee0-317">Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</span><span class="sxs-lookup"><span data-stu-id="faee0-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="faee0-318">Mata uang Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="faee0-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

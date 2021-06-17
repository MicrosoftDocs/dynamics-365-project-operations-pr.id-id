---
title: Kontrak Proyek
description: Topik ini memberikan contoh tentang kontrak proyek yang dapat anda buat untuk berbagai jenis proyek dan sumber pendanaan, dan bagaimana anda dapat mengelola kontrak dan faktur pelanggan proyek.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999765"
---
# <a name="project-contracts"></a><span data-ttu-id="5b2e9-103">Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="5b2e9-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b2e9-104">Artikel ini memberikan contoh tentang kontrak proyek yang dapat anda buat untuk berbagai jenis proyek dan sumber pendanaan, dan bagaimana anda dapat mengelola kontrak dan faktur pelanggan proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="5b2e9-105">Jenis proyek yang Anda buat untuk kontrak proyek menentukan metode yang digunakan untuk menagih pelanggan proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="5b2e9-106">Anda dapat mengubah kontrak proyek dan proyek terkait, namun Anda tidak dapat mengubah jenis proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="5b2e9-107">Dengan menggunakan kontrak proyek, Anda dapat menagih satu atau beberapa proyek pada waktu yang sama.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="5b2e9-108">Kontrak proyek juga membantu menjamin prosedur faktur konsisten untuk setiap subproyek dalam struktur proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="5b2e9-109">Setiap proyek yang akan ditagih harus terkait dengan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="5b2e9-110">Pengaturan untuk kontrak proyek berlaku untuk semua proyek dan subproyek yang terkait dengan kontrak proyek tersebut.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="5b2e9-111">Kontrak proyek dapat menyebutkan satu atau beberapa sumber pendanaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="5b2e9-112">Oleh karena itu, Anda dapat membagi tagihan di antara beberapa penyandang dana, mengatur batas pendanaan sehingga sumber pendanaan tidak ditagih lebih dari jumlah tertentu, dan mengkonfigurasikan aturan pendanaan untuk menagih pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="5b2e9-113">Pendanaan untuk kontrak proyek</span><span class="sxs-lookup"><span data-stu-id="5b2e9-113">Funding for project contracts</span></span>
<span data-ttu-id="5b2e9-114">Beberapa kontrak proyek menentukan bahwa beberapa pihak berbagi tanggung jawab untuk mendanai biaya proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="5b2e9-115">Berikut adalah beberapa contoh:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-115">Here are some examples:</span></span>

-   <span data-ttu-id="5b2e9-116">Pelanggan besar yang memiliki beberapa divisi meminta pendanaan proyek dapat dibagi menurut Divisi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="5b2e9-117">Perusahaan Anda berbagi biaya proyek besar dengan organisasi eksternal.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="5b2e9-118">Sebuah proyek jalan didanai oleh dua pemerintah kota.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="5b2e9-119">Sebuah proyek jembatan didanai oleh hibah pemerintah dan perusahaan swasta.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="5b2e9-120">Di Dynamics 365 Finance, Anda dapat membagi penagihan untuk satu transaksi atau seluruh proyek di antara beberapa pelanggan, hibah, atau organisasi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="5b2e9-121">Dalam proyek yang memiliki beberapa penyandang dana, semua pihak yang berkontribusi pada pendanaan proyek pendanaan tingkat lanjut disebut sumber pendanaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="5b2e9-122">Setelah pelanggan, organisasi, atau hibah didefinisikan sebagai sumber pendanaan, ia dapat ditetapkan ke satu atau beberapa aturan pendanaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="5b2e9-123">Aturan pendanaan berisi kriteria yang menentukan cara biaya dialokasikan ke berbagai sumber pendanaan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="5b2e9-124">Karena item dalam stok, seperti yang muncul pada rekusisi pembelian dan pesanan pembelian, tidak dapat dibagi, jumlah biaya tidak dapat dibagi antara beberapa sumber pendanaan pada saat distribusi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="5b2e9-125">Oleh karena itu, nilai sumber dana tetap 0 (nol) hingga masalah inventaris diposting.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="5b2e9-126">Bila masalah inventaris diposting, jumlah biaya akan didistribusikan berdasarkan aturan distribusi akun untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="5b2e9-127">Berikut adalah beberapa langkah yang dapat Anda lakukan agar lebih mudah membagi tagihan di antara beberapa sumber pendanaan:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="5b2e9-128">Tentukan bahwa semua transaksi yang dimasukkan untuk proyek menggunakan mata uang penjualan yang sama dengan kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="5b2e9-129">Mengatur batas pendanaan, sehingga sumber pendanaan tidak ditagih lebih dari jumlah tertentu pada proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="5b2e9-130">Konfigurasikan aturan pendanaan dan batas pendanaan untuk setiap pekerja, item, kategori, grup kategori, dan jenis transaksi (atau untuk semua jenis transaksi).</span><span class="sxs-lookup"><span data-stu-id="5b2e9-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="5b2e9-131">Pilih tanggal mulai dan akhir opsional untuk menentukan periode saat setiap aturan pendanaan valid.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="5b2e9-132">Tentukan persentase tanggung jawab setiap sumber pendanaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="5b2e9-133">Tentukan sumber pendanaan yang bertanggung jawab atas pembulatan selisih yang disebabkan oleh penghitungan alokasi pendanaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="5b2e9-134">Konfigurasikan aturan yang menentukan cara biaya proyek ditagih ke pelanggan eksternal dan dibebankan ke organisasi internal.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="5b2e9-135">Catat transaksi di akun pendanaan yang ditahan hingga dana tambahan dapat diperoleh, atau hingga Anda memutuskan menanggung biaya secara internal.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="5b2e9-136">Untuk menentukan grup pajak yang akan dikaitkan dengan transaksi, proyek dicari tugas grup pajaknya.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="5b2e9-137">Jika tugas grup pajak tidak dibuat di tingkat proyek, kontrak proyek akan dicari.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="5b2e9-138">Contoh: beberapa sumber pendanaan (sederhana)</span><span class="sxs-lookup"><span data-stu-id="5b2e9-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="5b2e9-139">Tabel berikut menyediakan skenario untuk mengelola alokasi dana di antara beberapa sumber pendanaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="5b2e9-140">Skenario ini didasarkan pada asumsi berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="5b2e9-141">Pengaturan prioritas diperhitungkan dalam alokasi dana sebelum kriteria aturan pendanaan lainnya diterapkan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="5b2e9-142">Rentang tanggal tidak ditentukan untuk menentukan periode saat aturan pendanaan valid.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b2e9-143"><strong>Skenario</strong></span><span class="sxs-lookup"><span data-stu-id="5b2e9-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="5b2e9-144"><strong>Sumber pendanaan</strong></span><span class="sxs-lookup"><span data-stu-id="5b2e9-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="5b2e9-145"><strong>Persentase alokasi</strong></span><span class="sxs-lookup"><span data-stu-id="5b2e9-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="5b2e9-146"><strong>Prioritas alokasi</strong></span><span class="sxs-lookup"><span data-stu-id="5b2e9-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b2e9-147">Anda ingin mengalokasikan biaya ke satu sumber pendanaan hingga dananya habis, alokasikan biaya ke sumber dana kedua hingga dananya habis, dan akhirnya alokasikan sisa biaya ke sumber dana ketiga.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5b2e9-148">Sumber pendanaan 1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="5b2e9-149">Sumber pendanaan 2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="5b2e9-150">Sumber pendanaan 3</span><span class="sxs-lookup"><span data-stu-id="5b2e9-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-151">100%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-151">100%</span></span></li>
<li><span data-ttu-id="5b2e9-152">100%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-152">100%</span></span></li>
<li><span data-ttu-id="5b2e9-153">100%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-154">1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-154">1</span></span></li>
<li><span data-ttu-id="5b2e9-155">2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-155">2</span></span></li>
<li><span data-ttu-id="5b2e9-156">3</span><span class="sxs-lookup"><span data-stu-id="5b2e9-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b2e9-157">Anda ingin mengalokasikan 75 persen dari biaya ke salah satu sumber pendanaan dan 25 persen ke sumber dana kedua.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5b2e9-158">Bila salah satu dari sumber pendanaan tersebut habis, Anda ingin membayar sisa biaya dari sumber pendanaan ketiga.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5b2e9-159">Sumber pendanaan 1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="5b2e9-160">Sumber pendanaan 2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="5b2e9-161">Sumber pendanaan 3</span><span class="sxs-lookup"><span data-stu-id="5b2e9-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-162">75%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-162">75%</span></span></li>
<li><span data-ttu-id="5b2e9-163">25%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-163">25%</span></span></li>
<li><span data-ttu-id="5b2e9-164">100%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-165">1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-165">1</span></span></li>
<li><span data-ttu-id="5b2e9-166">1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-166">1</span></span></li>
<li><span data-ttu-id="5b2e9-167">2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b2e9-168">Anda ingin mengalokasikan 75 persen dari biaya ke salah satu sumber pendanaan dan 25 persen ke sumber dana kedua.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="5b2e9-169">Bila salah satu dari sumber pendanaan tersebut habis, Anda ingin memecah sisa biaya antara sumber pendanaan ketiga dan sumber dana keempat.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5b2e9-170">Sumber pendanaan 1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="5b2e9-171">Sumber pendanaan 2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="5b2e9-172">Sumber pendanaan 3</span><span class="sxs-lookup"><span data-stu-id="5b2e9-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="5b2e9-173">Sumber pendanaan 4</span><span class="sxs-lookup"><span data-stu-id="5b2e9-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-174">75%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-174">75%</span></span></li>
<li><span data-ttu-id="5b2e9-175">25%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-175">25%</span></span></li>
<li><span data-ttu-id="5b2e9-176">50%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-176">50%</span></span></li>
<li><span data-ttu-id="5b2e9-177">50%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-178">1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-178">1</span></span></li>
<li><span data-ttu-id="5b2e9-179">1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-179">1</span></span></li>
<li><span data-ttu-id="5b2e9-180">2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-180">2</span></span></li>
<li><span data-ttu-id="5b2e9-181">2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b2e9-182">Anda ingin mengalokasikan 25 persen dari biaya pertama ke salah satu sumber pendanaan dan sisanya ke sumber dana kedua.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="5b2e9-183">Sumber pendanaan 1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="5b2e9-184">Sumber pendanaan 2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-185">25%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-185">25%</span></span></li>
<li><span data-ttu-id="5b2e9-186">100%</span><span class="sxs-lookup"><span data-stu-id="5b2e9-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5b2e9-187">1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-187">1</span></span></li>
<li><span data-ttu-id="5b2e9-188">2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="5b2e9-189">Contoh: beberapa sumber pendanaan (kompleks)</span><span class="sxs-lookup"><span data-stu-id="5b2e9-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="5b2e9-190">Anda memiliki tiga sumber pendanaan yang ingin Anda gunakan dalam urutan berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="5b2e9-191">Gunakan pendanaan sumber 2 dan pendanaan sumber 3 sama hingga dana sumber 2 habis.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="5b2e9-192">Terus gunakan dana sumber 3 hingga habis.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="5b2e9-193">Gunakan dana sumber 1 setelah sumber dana 3 habis.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="5b2e9-194">Untuk mencapai sasaran ini, pertama-tama Anda harus melakukan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="5b2e9-195">Mengatur batas pendanaan untuk mendanai sumber 2 dan mendanai sumber 3, untuk jumlah masing-masing.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="5b2e9-196">Buat aturan pendanaan berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="5b2e9-197">Aturan 1 (Prioritas 1): mengalokasikan 50 persen dari transaksi ke sumber dana 2 dan 50 persen ke dana sumber 3.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="5b2e9-198">Aturan 2 (Prioritas 2): mengalokasikan 100 persen dari transaksi ke sumber dana 3.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="5b2e9-199">Aturan 3 (Prioritas 3): mengalokasikan 100 persen dari transaksi ke sumber dana 1.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="5b2e9-200">Konfigurasi ini berfungsi karena transaksi diperiksa terhadap aturan dan batas untuk menentukan apakah salah satu dari mereka berlaku untuk transaksi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="5b2e9-201">Jika tidak ada aturan atau batas tertentu berlaku untuk transaksi, semua aturan transaksi berlaku.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="5b2e9-202">Aturan semua transaksi cocok dengan semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="5b2e9-203">Jika aturan ditemukan sesuai dengan transaksi, maka persentase yang telah dialokasikan pada aturan tersebut akan diterapkan terlebih dulu, namun hanya setelah kecocokan diperiksa terhadap batas yang telah diatur.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="5b2e9-204">Jika batas telah terpenuhi, dan dana sumber pendanaan habis, aturan pendanaan yang terkait dengan batas pendanaan diabaikan, dan program akan memeriksa aturan berikutnya yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="5b2e9-205">Dalam kasus tertentu, hanya sebagian dari transaksi yang dapat dialokasikan berdasarkan aturan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="5b2e9-206">Hal ini mungkin terjadi karena batas tercapai bila transaksi dialokasikan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="5b2e9-207">Dalam kasus ini, hanya jumlah tertentu yang dialokasikan berdasarkan aturan tersebut, seperti 50 persen ke setiap sumber pendanaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="5b2e9-208">Ini adalah kasus di aturan 1, yang dijelaskan sebelumnya di bagian ini.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="5b2e9-209">Sisanya dialokasikan menurut aturan berikutnya dalam urutan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="5b2e9-210">Tabel berikut ini akan memeriksa skenario ini secara lebih rinci.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b2e9-211"><strong>Fokus</strong></span><span class="sxs-lookup"><span data-stu-id="5b2e9-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="5b2e9-212"><strong>Rincian</strong></span><span class="sxs-lookup"><span data-stu-id="5b2e9-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b2e9-213">Aturan pendanaan</span><span class="sxs-lookup"><span data-stu-id="5b2e9-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="5b2e9-214">Aturan 1 (Prioritas 1): semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="5b2e9-215">Mengalokasikan dana sumber 2 pada 50% dan mendanai sumber 3 di 50%.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="5b2e9-216">Aturan 2 (Prioritas 2): semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="5b2e9-217">Mengalokasikan dana sumber 3 di 100%.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="5b2e9-218">Aturan 3 (Prioritas 2): semua transaksi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="5b2e9-219">Mengalokasikan dana sumber 1 di 100%.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b2e9-220">Batas pendanaan</span><span class="sxs-lookup"><span data-stu-id="5b2e9-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="5b2e9-221">batas Sumber pendanaan 1 = 10.000,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="5b2e9-222">batas Sumber pendanaan 2 = 500,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="5b2e9-223">batas Sumber pendanaan 3 = 750,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b2e9-224">Transaksi 1</span><span class="sxs-lookup"><span data-stu-id="5b2e9-224">Transaction 1</span></span></td>
<td><span data-ttu-id="5b2e9-225"><strong>Jumlah transaksi:</strong> 100,00<strong>pendanaan:</strong> transaksi dibayar berdasarkan aturan 1 saja, karena transaksi dibayar penuh setelah aturan 1 diterapkan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="5b2e9-226">Transaksi ini didanai secara merata antara sumber pendanaan 2 dan sumber pendanaan 3.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="5b2e9-227">Sumber pendanaan 2: 50,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="5b2e9-228">Sumber pendanaan 3: 50,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b2e9-229">Transaksi 2</span><span class="sxs-lookup"><span data-stu-id="5b2e9-229">Transaction 2</span></span></td>
<td><span data-ttu-id="5b2e9-230"><strong>Jumlah transaksi:</strong> 5.000,00<strong>pendanaan:</strong> transaksi dibayar sesuai dengan ketiga aturan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="5b2e9-231"><strong>Aturan 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="5b2e9-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="5b2e9-232">Sumber pendanaan 2: 450,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="5b2e9-233">Sumber pendanaan 3: 450,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="5b2e9-234">
<strong>Aturan 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="5b2e9-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="5b2e9-235">Sumber pendanaan 3: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="5b2e9-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="5b2e9-236">
<strong>Aturan 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="5b2e9-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="5b2e9-237">Sumber pendanaan 1: 3.850,00 (= 5.000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="5b2e9-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b2e9-238">Total dana yang didistribusikan untuk setiap sumber pendanaan</span><span class="sxs-lookup"><span data-stu-id="5b2e9-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="5b2e9-239">Sumber pendanaan 1: 3.850,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="5b2e9-240">Sumber pendanaan 2: 500,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="5b2e9-241">Sumber pendanaan 3: 750,00</span><span class="sxs-lookup"><span data-stu-id="5b2e9-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="5b2e9-242">Aturan penagihan</span><span class="sxs-lookup"><span data-stu-id="5b2e9-242">Billing rules</span></span>
<span data-ttu-id="5b2e9-243">Ketika Anda menegosiasikan kontrak proyek dengan pelanggan, Anda menentukan bagaimana dan Kapan Anda dapat menagih pelanggan untuk bekerja pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="5b2e9-244">Setelah Anda mengkonfigurasi kontrak proyek dan proyek, Anda dapat mengkonfigurasi aturan penagihan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="5b2e9-245">Aturan penagihan didasarkan pada persyaratan proyek yang ditentukan dalam kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="5b2e9-246">Aturan penagihan yang dapat Anda buat tergantung pada persyaratan kontrak proyek dan jenis proyek, seperti waktu dan material atau harga tetap, yang Anda kaitkan dengan aturan penagihan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="5b2e9-247">Anda dapat membuat lebih dari satu aturan penagihan untuk kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="5b2e9-248">Anda juga dapat menetapkan aturan penagihan ke beberapa proyek yang terkait dengan kontrak proyek yang sama dan memiliki syarat penagihan yang serupa.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="5b2e9-249">Anda dapat mengkonfigurasi jenis aturan penagihan berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="5b2e9-250">**Unit pengiriman** – tagih pelanggan saat Anda menyelesaikan unit pengiriman.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="5b2e9-251">Anda menentukan unit pengiriman dalam kontrak.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="5b2e9-252">**Progres** – menagih pelanggan saat Anda menyelesaikan persentase tertentu dari proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="5b2e9-253">Anda dapat mengkonfigurasi aturan penagihan untuk menghitung secara otomatis persentase pekerjaan yang diselesaikan, atau Anda dapat secara manual menghitung persentase pekerjaan yang diselesaikan dan jumlah yang akan ditagih ke pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="5b2e9-254">**Tonggak pencapaian** –-tagih pelanggan untuk jumlah penuh tonggak pencapaian proyek saat tonggak tercapai.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="5b2e9-255">**Ongkos** – tagih pelanggan untuk layanan Anda ditambah biaya manajemen, yang biasanya merupakan persentase dari biaya layanan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="5b2e9-256">**Waktu dan material** – tagih pelanggan untuk nilai waktu dan bahan yang digunakan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="5b2e9-257">Untuk semua jenis aturan penagihan, Anda dapat menentukan persentase retensi yang dipotong dari faktur pelanggan hingga proyek mencapai tahapan yang disepakati.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="5b2e9-258">Persentase retensi pembayaran ditentukan dalam kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="5b2e9-259">Jumlah dihitung berdasarkan, dan dikurangi dari, nilai total baris di faktur pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="5b2e9-260">Untuk aturan penagihan **waktu dan material** dan **progres**, Anda dapat menetapkan kategori yang dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="5b2e9-261">Kategori yang dibebankan menunjukkan transaksi yang harus disertakan dalam faktur pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="5b2e9-262">Ketika Anda siap untuk faktur pelanggan, jumlah faktur untuk proyek dihitung berdasarkan aturan penagihan, dan proposal proyek faktur dibuat.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="5b2e9-263">Bagian berikut menyediakan contoh yang menunjukkan cara mengkonfigurasi dan mengelola aturan penagihan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="5b2e9-264">Contoh: Buat aturan penagihan yang didasarkan pada jumlah unit yang dikirim</span><span class="sxs-lookup"><span data-stu-id="5b2e9-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="5b2e9-265">Organisasi Anda menandatangani perjanjian untuk menyediakan total lima sesi pelatihan kepada karyawan pelanggan dengan biaya 10.000 per sesi pelatihan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="5b2e9-266">Anda menagih pelanggan setelah setiap sesi pelatihan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="5b2e9-267">Saat mengkonfigurasi aturan penagihan untuk kontrak, Anda menggunakan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="5b2e9-268">Unit pengiriman adalah satu sesi pelatihan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="5b2e9-269">Harga unit adalah 10.000 per sesi pelatihan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="5b2e9-270">Jumlah total unit adalah lima sesi pelatihan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="5b2e9-271">Setelah menyelesaikan satu sesi pelatihan, Anda dapat membuat faktur untuk 10.000, untuk unit pertama yang dikirim, dan mengirim faktur kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="5b2e9-272">Contoh: Buat aturan penagihan yang didasarkan pada persentase penyelesaian proyek yang ditentukan (penghitungan manual)</span><span class="sxs-lookup"><span data-stu-id="5b2e9-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="5b2e9-273">Organisasi Anda, sebuah firma konsultasi perangkat lunak, memasuki perjanjian dengan pelanggan untuk mengembangkan bagian dari produk yang sedang dikembangkan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="5b2e9-274">Organisasi Anda setuju untuk memberikan kode perangkat lunak selama periode enam bulan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="5b2e9-275">Pelanggan setuju untuk membayar organisasi Anda Total 100.000 untuk pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="5b2e9-276">Anda membuat aturan penagihan untuk menagih pelanggan berdasarkan persentase pekerjaan yang diselesaikan pada proyek, sebagaimana ditentukan dalam kontrak.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="5b2e9-277">Pada akhir bulan pertama, Anda bertemu dengan pelanggan untuk menentukan persentase pekerjaan yang diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="5b2e9-278">Setelah Anda dan pelanggan meninjau proyek, Anda memutuskan bahwa proyek 15 persen selesai.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="5b2e9-279">Anda membuat faktur 15.000 (15 persen dari 100.000) dan mengirimkannya ke pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="5b2e9-280">Contoh: Buat aturan penagihan yang didasarkan pada persentase penyelesaian proyek yang ditentukan (penghitungan otomatis)</span><span class="sxs-lookup"><span data-stu-id="5b2e9-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="5b2e9-281">Organisasi Anda, firma pengembangan perangkat lunak, setuju untuk mengembangkan paket akuntansi penggajian untuk pelanggan senilai 30.000.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="5b2e9-282">Pelanggan setuju untuk membayar organisasi Anda berdasarkan persentase pekerjaan yang selesai.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="5b2e9-283">Anda memperkirakan bahwa biaya proyek adalah 20.000.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="5b2e9-284">Kontrak proyek menentukan kategori pekerjaan yang Anda gunakan dalam proses penagihan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="5b2e9-285">Anda menyiapkan aturan penagihan yang menghitung jumlah faktur secara otomatis untuk persentase pekerjaan yang diselesaikan untuk setiap kategori.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="5b2e9-286">Anda mengkonfigurasi anggaran untuk setiap kategori:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="5b2e9-287">**Pengembangan** – biaya 15.000 dan pendapatan 20.000</span><span class="sxs-lookup"><span data-stu-id="5b2e9-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="5b2e9-288">**Instalasi** – biaya 5.000 dan pendapatan 10.000</span><span class="sxs-lookup"><span data-stu-id="5b2e9-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="5b2e9-289">Bila Anda membuat faktur pelanggan untuk pertama kalinya, jumlah faktur akan dihitung secara otomatis berdasarkan informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="5b2e9-290">Setelah sebulan, pekerja di proyek mengirimkan lembar waktu untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="5b2e9-291">Biaya pekerja jam adalah 5.000 untuk pengembangan dan 1.000 untuk penginstalan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="5b2e9-292">Pekerjaan pembangunan 33 persen selesai (5.000 biaya aktual/15000 biaya anggaran), dan pekerjaan penginstalan 20 persen selesai (1.000 biaya aktual/5000 biaya anggaran).</span><span class="sxs-lookup"><span data-stu-id="5b2e9-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="5b2e9-293">Jumlah faktur 8.667 secara otomatis dihitung (33 persen dari 20.000 + 20 persen dari 10.000).</span><span class="sxs-lookup"><span data-stu-id="5b2e9-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="5b2e9-294">Anda membuat faktur 8.667 dan mengirimkannya ke pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="5b2e9-295">Contoh: Buat aturan penagihan yang didasarkan pada tonggak prestasi yang disepakati</span><span class="sxs-lookup"><span data-stu-id="5b2e9-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="5b2e9-296">Organisasi Anda, perusahaan konsultan manajemen, setuju untuk melakukan riset pasar untuk produk konsumen yang akan dijual pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="5b2e9-297">Pelanggan setuju untuk menggunakan layanan selama periode tiga bulan, mulai Maret, dan setuju untuk membayar 50.000 organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="5b2e9-298">Proyek ini memiliki tiga tonggak:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-298">The project has three milestones:</span></span>

-   <span data-ttu-id="5b2e9-299">Tonggak 1: mengumpulkan data pelanggan – 31 Maret</span><span class="sxs-lookup"><span data-stu-id="5b2e9-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="5b2e9-300">Tonggak 2: analisis data konsumen – 30 April</span><span class="sxs-lookup"><span data-stu-id="5b2e9-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="5b2e9-301">Tonggak 3: proposal kelayakan produk – 31 Mei</span><span class="sxs-lookup"><span data-stu-id="5b2e9-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="5b2e9-302">Pelanggan setuju untuk membayar 10.000 organisasi Anda untuk tonggak pertama, 20.000 untuk tonggak kedua, dan 20.000 untuk tonggak ketiga.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="5b2e9-303">Saat Anda menyiapkan kontrak proyek, Anda setuju untuk menagih pelanggan berdasarkan tonggak yang telah diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="5b2e9-304">Penyiapan aturan penagihan mencakup langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="5b2e9-305">Tentukan tonggak proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-305">Define the project milestones.</span></span>
-   <span data-ttu-id="5b2e9-306">Tentukan jumlah faktur pelanggan saat setiap tonggak selesai.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="5b2e9-307">Ketika tonggak pertama selesai pada tanggal 31 Maret, Anda menandai tonggak prestasi sebagai selesai, dan kemudian membuat faktur untuk 10.000 dan mengirimkannya ke pelanggan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="5b2e9-308">Anda tidak dapat membuat faktur untuk tonggak hingga Anda telah menandai tonggak prestasi sebagai selesai.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="5b2e9-309">Contoh: Buat aturan penagihan yang didasarkan pada layanan ditambah biaya manajemen</span><span class="sxs-lookup"><span data-stu-id="5b2e9-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="5b2e9-310">Organisasi Anda, perusahaan konsultan manajemen, setuju untuk melakukan riset pasar untuk mengevaluasi kelangsungan hidup produk yang sedang dikembangkan oleh pelanggan, perusahaan ritel.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="5b2e9-311">Persyaratan perjanjian menentukan bahwa Anda akan memberikan layanan dari tiga konsultan manajemen teratas, yang akan melakukan penelitian berdasarkan waktu dan bahan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="5b2e9-312">Pelanggan setuju untuk membayar 100 per jam, ditambah biaya 10 persen manajemen untuk jam konsultasi yang dibebankan ke proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5b2e9-313">Saat Anda menyiapkan kontrak proyek, buat aturan penagihan untuk menambahkan biaya manajemen 10 persen ke jam konsultasi yang dibebankan ke proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="5b2e9-314">Bila Anda membuat faktur untuk pelanggan, pelanggan ditagih biaya manajemen 10 persen ditambah biaya jam konsultasi.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="5b2e9-315">Misalnya, jika tiga konsultan bekerja Total 200 jam pada proyek, faktur untuk 22.000 dibuat berdasarkan perhitungan berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="5b2e9-316">200 jam pada 100 per jam = 20.000</span><span class="sxs-lookup"><span data-stu-id="5b2e9-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="5b2e9-317">10 persen biaya manajemen = 2.000</span><span class="sxs-lookup"><span data-stu-id="5b2e9-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="5b2e9-318">Jumlah total faktur = 22.000</span><span class="sxs-lookup"><span data-stu-id="5b2e9-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="5b2e9-319">Jika biaya dapat dikenai pajak untuk pelanggan, dan Anda memilih grup pajak penjualan dalam kontrak proyek, grup pajak penjualan akan secara otomatis dimasukkan dalam aturan penagihan untuk biaya.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="5b2e9-320">Contoh: Buat aturan penagihan untuk nilai waktu dan material</span><span class="sxs-lookup"><span data-stu-id="5b2e9-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="5b2e9-321">Organisasi Anda, sebuah firma konsultasi perangkat lunak, setuju untuk menyediakan lima konsultan teknis untuk mengerjakan proyek pengembangan perangkat lunak untuk pelanggan selama enam bulan berikutnya.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="5b2e9-322">Pelanggan setuju untuk membayar 150 untuk setiap jam konsultasi, ditambah biaya perlengkapan kantor.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="5b2e9-323">Organisasi Anda mengirimkan faktur kepada pelanggan pada akhir setiap bulan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="5b2e9-324">Saat Anda menyiapkan kontrak proyek, Anda setuju untuk menagih pelanggan setiap bulan untuk waktu dan bahan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="5b2e9-325">Anda membuat aturan penagihan yang mencakup informasi berikut:</span><span class="sxs-lookup"><span data-stu-id="5b2e9-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="5b2e9-326">Periode kontrak adalah enam bulan.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-326">The contract period is six months.</span></span>
-   <span data-ttu-id="5b2e9-327">Waktu konsultasi dihitung pada tingkat 150 per jam.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="5b2e9-328">Persediaan kantor ditagih pada biaya, dan total biaya untuk proyek tidak boleh melebihi 10.000.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="5b2e9-329">Anda membuat faktur pelanggan di akhir setiap bulan kalender selama proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="5b2e9-330">Selama bulan pertama, Total 800 jam dicatat dicatat oleh konsultan pada proyek.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="5b2e9-331">Biaya perlengkapan kantor yang dibebankan pada proyek adalah 2.000.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="5b2e9-332">Oleh karena itu, pada akhir bulan, Anda membuat faktur untuk 122.000, yang dihitung sebagai 800 jam di 150 per jam, plus 2.000 untuk perlengkapan kantor.</span><span class="sxs-lookup"><span data-stu-id="5b2e9-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]
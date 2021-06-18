---
title: Grup unit dan unit
description: Topik ini menyediakan informasi tentang grup unit dan unit.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: e981f39bbb6ca4277778382a5816952df2a8a1fb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009575"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="b6f86-103">Grup unit dan unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b6f86-104">Grup unit dan unit adalah entitas dasar di Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b6f86-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="b6f86-105">Unit adalah satuan ukuran tunggal, dan beberapa unit dapat dikelompokkan ke dalam grup unit.</span><span class="sxs-lookup"><span data-stu-id="b6f86-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="b6f86-106">Grup unit terkadang disebut sebagai jadwal unit di antarmuka pengguna Dynamics 365 (UI).</span><span class="sxs-lookup"><span data-stu-id="b6f86-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="b6f86-107">Berikut adalah beberapa contoh unit dan grup unit:</span><span class="sxs-lookup"><span data-stu-id="b6f86-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="b6f86-108">**grup unit**: Jarak</span><span class="sxs-lookup"><span data-stu-id="b6f86-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="b6f86-109">**Unit**: mil, kilometer, dan sebagainya.</span><span class="sxs-lookup"><span data-stu-id="b6f86-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="b6f86-110">**grup unit**: waktu</span><span class="sxs-lookup"><span data-stu-id="b6f86-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="b6f86-111">**Unit**: jam, hari, Minggu, dan sebagainya.</span><span class="sxs-lookup"><span data-stu-id="b6f86-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="b6f86-112">Bila Anda mengkonfigurasi beberapa unit di grup unit, Anda juga harus menyiapkan faktor konversi di antara keduanya dengan menunjuk unit pertama yang Anda konfigurasikan sebagai unit default atau utama untuk grup unit.</span><span class="sxs-lookup"><span data-stu-id="b6f86-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="b6f86-113">Misalnya, di grup unit **waktu**, jika Anda mengatur **jam** sebagai unit pertama, sistem akan menunjukkan **jam** sebagai unit default.</span><span class="sxs-lookup"><span data-stu-id="b6f86-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="b6f86-114">Jika unit berikutnya yang Anda konfigurasikan adalah **hari**, Anda harus mengkonfigurasi faktor konversi untuk **hari** ke **jam**.</span><span class="sxs-lookup"><span data-stu-id="b6f86-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="b6f86-115">Jika **Anda menambahkan minggu** sebagai unit ketiga, Anda harus mengkonfigurasi faktor konversi untuk **minggu** dalam hal **hari** atau **jam**.</span><span class="sxs-lookup"><span data-stu-id="b6f86-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="b6f86-116">Gambar berikut menunjukkan contoh konfigurasi untuk unit **hari**, dengan bidang **kuantitas** menampilkan jumlah jam yang berada dalam satu hari, dan **minggu**, dengan bidang **kuantitas** menampilkan jumlah hari dalam seminggu.</span><span class="sxs-lookup"><span data-stu-id="b6f86-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Grup unit: Halaman informasi](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="b6f86-118">Menggunakan grup unit dan unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-118">Using units and unit groups</span></span>

<span data-ttu-id="b6f86-119">Dynamics 365 Project Service Automation menggunakan unit dan grup unit untuk memproses perkiraan dan entri untuk biaya dan waktu.</span><span class="sxs-lookup"><span data-stu-id="b6f86-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="b6f86-120">Untuk pengeluaran, setiap kategori pengeluaran memiliki unit dan grup unit default.</span><span class="sxs-lookup"><span data-stu-id="b6f86-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="b6f86-121">Nilai ini dimasukkan sebagai nilai default pada entri daftar harga untuk kategori pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="b6f86-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="b6f86-122">Misalnya, Anda memiliki kategori pengeluaran yang diberi nama **jarak tempuh**.</span><span class="sxs-lookup"><span data-stu-id="b6f86-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="b6f86-123">Ia memiliki grup unit yang diberi nama **jarak** dan unit default bernama **Mil**.</span><span class="sxs-lookup"><span data-stu-id="b6f86-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="b6f86-124">Jika Anda mengkonfigurasi grup unit **jarak** sehingga memiliki dua unit (**Mil** dan **kilometer**), Anda dapat menetapkan dua harga untuk kategori **jarak tempuh** pada satu daftar harga: harga per mil dan harga per kilometer.</span><span class="sxs-lookup"><span data-stu-id="b6f86-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="b6f86-125">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="b6f86-125">Expense category</span></span>  | <span data-ttu-id="b6f86-126">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-126">Unit group</span></span>  | <span data-ttu-id="b6f86-127">Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-127">Unit</span></span>      | <span data-ttu-id="b6f86-128">Metode Penetapan Harga</span><span class="sxs-lookup"><span data-stu-id="b6f86-128">Pricing method</span></span>  | <span data-ttu-id="b6f86-129">Harga per unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="b6f86-130">Jarak Tempuh</span><span class="sxs-lookup"><span data-stu-id="b6f86-130">Mileage</span></span>           | <span data-ttu-id="b6f86-131">Jarak</span><span class="sxs-lookup"><span data-stu-id="b6f86-131">Distance</span></span>      | <span data-ttu-id="b6f86-132">Mil</span><span class="sxs-lookup"><span data-stu-id="b6f86-132">Mile</span></span>      | <span data-ttu-id="b6f86-133">Harga per unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-133">Price per unit</span></span>    | <span data-ttu-id="b6f86-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="b6f86-134">10 USD</span></span>            |
| <span data-ttu-id="b6f86-135">Jarak Tempuh</span><span class="sxs-lookup"><span data-stu-id="b6f86-135">Mileage</span></span>           | <span data-ttu-id="b6f86-136">Jarak</span><span class="sxs-lookup"><span data-stu-id="b6f86-136">Distance</span></span>      | <span data-ttu-id="b6f86-137">Kilometer</span><span class="sxs-lookup"><span data-stu-id="b6f86-137">Kilometer</span></span> | <span data-ttu-id="b6f86-138">Harga per unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-138">Price per unit</span></span>    |  <span data-ttu-id="b6f86-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="b6f86-139">6 USD</span></span>            |

<span data-ttu-id="b6f86-140">Bila Anda memasukkan pengeluaran pada suatu proyek, sistem akan menentukan harga melalui kombinasi kategori dan unit pada biaya.</span><span class="sxs-lookup"><span data-stu-id="b6f86-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="b6f86-141">Deskripsi pengeluaran</span><span class="sxs-lookup"><span data-stu-id="b6f86-141">Expense description</span></span>        | <span data-ttu-id="b6f86-142">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="b6f86-142">Expense category</span></span>  | <span data-ttu-id="b6f86-143">Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-143">Unit</span></span>  | <span data-ttu-id="b6f86-144">Kuantitas</span><span class="sxs-lookup"><span data-stu-id="b6f86-144">Quantity</span></span>  | <span data-ttu-id="b6f86-145">Harga per Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="b6f86-146">Berkendara ke lokasi klien</span><span class="sxs-lookup"><span data-stu-id="b6f86-146">Drive to client location</span></span> | <span data-ttu-id="b6f86-147">Jarak Tempuh</span><span class="sxs-lookup"><span data-stu-id="b6f86-147">Mileage</span></span>             | <span data-ttu-id="b6f86-148">Mil</span><span class="sxs-lookup"><span data-stu-id="b6f86-148">Mile</span></span>  | <span data-ttu-id="b6f86-149">10</span><span class="sxs-lookup"><span data-stu-id="b6f86-149">10</span></span>        | <span data-ttu-id="b6f86-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="b6f86-150">10 USD</span></span>         |

<span data-ttu-id="b6f86-151">Untuk waktu, setiap header daftar harga memiliki bidang **unit waktu default**.</span><span class="sxs-lookup"><span data-stu-id="b6f86-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="b6f86-152">Nilai diatur saat Anda membuat header daftar harga.</span><span class="sxs-lookup"><span data-stu-id="b6f86-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="b6f86-153">Unit ini kemudian digunakan untuk mengatur semua harga berdasarkan peran pada daftar harga tersebut.</span><span class="sxs-lookup"><span data-stu-id="b6f86-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="b6f86-154">Baris perkiraan untuk bidang **waktu pada kuotasi** dapat dinyatakan dalam satuan waktu.</span><span class="sxs-lookup"><span data-stu-id="b6f86-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="b6f86-155">Namun, perkirakan baris pada entri proyek dan waktu untuk proyek hanya dapat menggunakan satuan waktu **jam**.</span><span class="sxs-lookup"><span data-stu-id="b6f86-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="b6f86-156">Jika unit pada baris entri waktu atau perkiraan tidak sesuai dengan unit pada baris daftar harga untuk peran tersebut, sistem akan mengkonversi harga ke unit yang ditentukan dalam perkiraan proyek atau transaksi aktual proyek.</span><span class="sxs-lookup"><span data-stu-id="b6f86-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="b6f86-157">Contoh berikut menunjukkan cara PSA menggunakan grup unit, unit, dan faktor konversi.</span><span class="sxs-lookup"><span data-stu-id="b6f86-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="b6f86-158">Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-158">Units</span></span>

   - <span data-ttu-id="b6f86-159">**grup unit**: waktu</span><span class="sxs-lookup"><span data-stu-id="b6f86-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="b6f86-160">**Unit**: jam</span><span class="sxs-lookup"><span data-stu-id="b6f86-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="b6f86-161">**hari** – Faktor konversi: 8 jam</span><span class="sxs-lookup"><span data-stu-id="b6f86-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="b6f86-162">**Minggu** – Faktor konversi: 40 jam</span><span class="sxs-lookup"><span data-stu-id="b6f86-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="b6f86-163">Konfigurasi daftar harga pada proyek A:</span><span class="sxs-lookup"><span data-stu-id="b6f86-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="b6f86-164">**Nama**: harga penjualan UK 2016</span><span class="sxs-lookup"><span data-stu-id="b6f86-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="b6f86-165">**Unit waktu default**: hari</span><span class="sxs-lookup"><span data-stu-id="b6f86-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="b6f86-166">**Mata Uang**: GBP</span><span class="sxs-lookup"><span data-stu-id="b6f86-166">**Currency**: GBP</span></span>

| <span data-ttu-id="b6f86-167">Peran</span><span class="sxs-lookup"><span data-stu-id="b6f86-167">Role</span></span>      | <span data-ttu-id="b6f86-168">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-168">Unit group</span></span> | <span data-ttu-id="b6f86-169">Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-169">Unit</span></span> | <span data-ttu-id="b6f86-170">Unit organisasi</span><span class="sxs-lookup"><span data-stu-id="b6f86-170">Organizational unit</span></span> | <span data-ttu-id="b6f86-171">Harga</span><span class="sxs-lookup"><span data-stu-id="b6f86-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="b6f86-172">Pengembang</span><span class="sxs-lookup"><span data-stu-id="b6f86-172">Developer</span></span> | <span data-ttu-id="b6f86-173">Waktu</span><span class="sxs-lookup"><span data-stu-id="b6f86-173">Time</span></span>       | <span data-ttu-id="b6f86-174">Hari</span><span class="sxs-lookup"><span data-stu-id="b6f86-174">Day</span></span>  | <span data-ttu-id="b6f86-175">Contoso Inggris</span><span class="sxs-lookup"><span data-stu-id="b6f86-175">Contoso UK</span></span>          | <span data-ttu-id="b6f86-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="b6f86-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="b6f86-177">Entri waktu</span><span class="sxs-lookup"><span data-stu-id="b6f86-177">Time entry</span></span>

<span data-ttu-id="b6f86-178">Tabel berikut Menampilkan hasil transaksi penjualan yang dibuat oleh PSA selama proyek tiga jam.</span><span class="sxs-lookup"><span data-stu-id="b6f86-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="b6f86-179">Proyek</span><span class="sxs-lookup"><span data-stu-id="b6f86-179">Project</span></span>   | <span data-ttu-id="b6f86-180">Tugas</span><span class="sxs-lookup"><span data-stu-id="b6f86-180">Task</span></span>    | <span data-ttu-id="b6f86-181">Peran</span><span class="sxs-lookup"><span data-stu-id="b6f86-181">Role</span></span>      | <span data-ttu-id="b6f86-182">Kuantitas</span><span class="sxs-lookup"><span data-stu-id="b6f86-182">Quantity</span></span> | <span data-ttu-id="b6f86-183">Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-183">Unit</span></span>  | <span data-ttu-id="b6f86-184">Harga per Unit</span><span class="sxs-lookup"><span data-stu-id="b6f86-184">Unit price</span></span> | <span data-ttu-id="b6f86-185">Jumlah Penjualan Tak Tertagih</span><span class="sxs-lookup"><span data-stu-id="b6f86-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="b6f86-186">Proyek A</span><span class="sxs-lookup"><span data-stu-id="b6f86-186">Project A</span></span> | <span data-ttu-id="b6f86-187">Rancang</span><span class="sxs-lookup"><span data-stu-id="b6f86-187">Design</span></span>  | <span data-ttu-id="b6f86-188">Pengembang</span><span class="sxs-lookup"><span data-stu-id="b6f86-188">Developer</span></span> | <span data-ttu-id="b6f86-189">3</span><span class="sxs-lookup"><span data-stu-id="b6f86-189">3</span></span>        | <span data-ttu-id="b6f86-190">Hour</span><span class="sxs-lookup"><span data-stu-id="b6f86-190">Hour</span></span>  | <span data-ttu-id="b6f86-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="b6f86-191">100 GBP</span></span>    | <span data-ttu-id="b6f86-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="b6f86-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="b6f86-193">Tanya-Jawab unit Waktu</span><span class="sxs-lookup"><span data-stu-id="b6f86-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="b6f86-194">Apakah PSA dikonversi ke unit yang berbeda dalam kasus pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="b6f86-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="b6f86-195">Tidak.</span><span class="sxs-lookup"><span data-stu-id="b6f86-195">No.</span></span> <span data-ttu-id="b6f86-196">Konversi unit berfungsi hanya untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="b6f86-196">Unit conversion works only for time.</span></span> <span data-ttu-id="b6f86-197">Untuk pengeluaran, jika sistem tidak dapat menemukan harga untuk kombinasi kategori pengeluaran dan unit, harga diatur ke 0,00 secara default.</span><span class="sxs-lookup"><span data-stu-id="b6f86-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="b6f86-198">Mengapa PSA mengkonversi unit waktu?</span><span class="sxs-lookup"><span data-stu-id="b6f86-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="b6f86-199">Di beberapa negara atau kawasan, ada persyaratan hukum yang mengatur tarif tagihan dalam hari.</span><span class="sxs-lookup"><span data-stu-id="b6f86-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="b6f86-200">Negosiasi harga dan diskon selama siklus kuotasi dilakukan dengan menggunakan tarif harian untuk setiap peran yang dapat ditagih.</span><span class="sxs-lookup"><span data-stu-id="b6f86-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="b6f86-201">Estimasi jadwal dan entri waktu dilakukan dalam jam.</span><span class="sxs-lookup"><span data-stu-id="b6f86-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="b6f86-202">Untuk mendukung perbedaan dalam unit waktu ini, PSA mengkonversi unit waktu.</span><span class="sxs-lookup"><span data-stu-id="b6f86-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="b6f86-203">Apakah unit waktu dapat diubah pada perkiraan proyek?</span><span class="sxs-lookup"><span data-stu-id="b6f86-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="b6f86-204">Tidak.</span><span class="sxs-lookup"><span data-stu-id="b6f86-204">No.</span></span> <span data-ttu-id="b6f86-205">Perkiraan jadwal saat saat ini dibatasi hingga jam dan tidak dapat diubah.</span><span class="sxs-lookup"><span data-stu-id="b6f86-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="b6f86-206">Apakah unit dan grup unit dapat diedit, dihapus, dan ditambahkan?</span><span class="sxs-lookup"><span data-stu-id="b6f86-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="b6f86-207">Ya.</span><span class="sxs-lookup"><span data-stu-id="b6f86-207">Yes.</span></span> <span data-ttu-id="b6f86-208">Dengan pengecualian grup unit **waktu** dan unit **jam**, Semua unit dapat dihapus atau diedit, dan unit baru dapat ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="b6f86-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="b6f86-209">Dalam PSA, grup unit **waktu** dan unit **jam** tidak dapat dihapus.</span><span class="sxs-lookup"><span data-stu-id="b6f86-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="b6f86-210">Namun, mereka dapat diperbarui dengan teks terjemahan untuk bidang **nama**.</span><span class="sxs-lookup"><span data-stu-id="b6f86-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Mengonfigurasikan komponen yang dikenakan biaya di baris kontrak berbasis proyek
description: Topik ini memberikan informasi tentang cara menambahkan komponen yang dikenakan biaya ke lini kontrak dalam Project Operations.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003725"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="7538b-103">Mengonfigurasikan komponen yang dikenakan biaya di baris kontrak berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="7538b-104">_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_</span><span class="sxs-lookup"><span data-stu-id="7538b-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7538b-105">Baris kontrak berbasis proyek telah *menyertakan* komponen dan komponen *yang dapat dikenakan biaya*.</span><span class="sxs-lookup"><span data-stu-id="7538b-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="7538b-106">Komponen yang disertakan adalah komponen yang tunduk pada:</span><span class="sxs-lookup"><span data-stu-id="7538b-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="7538b-107">Metode penagihan dan pemisahan pelanggan</span><span class="sxs-lookup"><span data-stu-id="7538b-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="7538b-108">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="7538b-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="7538b-109">Pengaturan frekuensi faktur yang didefinisikan pada baris kontrak berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="7538b-110">Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya menggunakan bidang **Tipe Penagihan**.</span><span class="sxs-lookup"><span data-stu-id="7538b-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="7538b-111">Bidang **Tipe Penagihan** adalah kumpulan opsi yang memungkinkan nilai berikut dalam konteks baris kontrak:</span><span class="sxs-lookup"><span data-stu-id="7538b-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="7538b-112">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-112">Chargeable</span></span>
  - <span data-ttu-id="7538b-113">Tidak Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-113">Non-chargeable</span></span>

<span data-ttu-id="7538b-114">Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori tugas, peran, dan transaksi.</span><span class="sxs-lookup"><span data-stu-id="7538b-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="7538b-115">Dapat dikenakan Biaya didefinisikan pada tugas untuk baris kontrak proyek dan berlaku untuk semua kelas transaksi yang disertakan di baris.</span><span class="sxs-lookup"><span data-stu-id="7538b-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="7538b-116">Jika bidang **Sertakan Tugas** pada baris kontrak kosong atau diatur ke **Seluruh proyek**, tab **Tugas yang dapat dikenakan biaya** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="7538b-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="7538b-117">Bisa dikenakan biaya yang didefinisikan pada peran untuk baris kontrak proyek hanya berlaku untuk kelas transaksi **waktu**.</span><span class="sxs-lookup"><span data-stu-id="7538b-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="7538b-118">Jika bidang **Sertakan waktu** pada baris kontrak diatur ke **Tidak**, tab **Peran yang dapat dikenakan biaya** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="7538b-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="7538b-119">Bisa dikenakan biaya yang didefinisikan pada kategori transaksi untuk baris kontrak proyek hanya berlaku untuk kelas transaksi **Pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="7538b-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="7538b-120">Jika bidang **Sertakan Pengeluaran** pada diatur ke **Tidak**, tab **Kategori yang dapat dikenakan biaya** tidak akan tersedia.</span><span class="sxs-lookup"><span data-stu-id="7538b-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7538b-121">Memperbarui tugas proyek sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="7538b-122">Tugas proyek dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu yang memungkinkan pengaturan berikut:</span><span class="sxs-lookup"><span data-stu-id="7538b-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="7538b-123">Jika baris kontrak berbasis proyek mencakup **Waktu** dan tugas tertentu, **T1** dikaitkan dengannya sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="7538b-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="7538b-124">Jika ada baris kontrak kedua yang mencakup **Pengeluaran**, Anda dapat mengaitkan tugas T1 di baris kontrak sebagai tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="7538b-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="7538b-125">Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="7538b-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="7538b-126">Jenis penagihan tugas dapat dikonfigurasi pada tab **tugas kena biaya** pada baris kontrak dengan memperbarui bidang **jenis penagihan** pada subkisi tugas baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="7538b-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="7538b-127">Atau, Anda dapat memperbarui bidang **jenis penagihan** pada subkisi dari konfigurasi penagihan tugas proyek yang menunjukkan baris kontrak yang terkait dengan tugas.</span><span class="sxs-lookup"><span data-stu-id="7538b-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7538b-128">Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="7538b-129">Peran dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu.</span><span class="sxs-lookup"><span data-stu-id="7538b-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="7538b-130">Jenis penagihan peran dapat dikonfigurasi pada tab **Peran Kena Biaya** dari baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="7538b-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="7538b-131">Untuk melakukannya, perbarui bidang **jenis penagihan** pada subkisi **peran kena biaya**.</span><span class="sxs-lookup"><span data-stu-id="7538b-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="7538b-132">Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="7538b-133">Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu.</span><span class="sxs-lookup"><span data-stu-id="7538b-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="7538b-134">Jenis penagihan transaksi dapat dikonfigurasi pada tab **Kategori Kena Biaya** dari baris kontrak berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="7538b-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="7538b-135">Untuk melakukannya, perbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**.</span><span class="sxs-lookup"><span data-stu-id="7538b-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="7538b-136">Menangani pengenaan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-136">Resolve chargeability</span></span>

<span data-ttu-id="7538b-137">Perkiraan atau aktual yang dibuat untuk waktu hanya dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="7538b-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="7538b-138">**Waktu** tercakup di baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="7538b-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="7538b-139">**Peran** dikonfigurasi sebagai dibebankan pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="7538b-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="7538b-140">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="7538b-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="7538b-141">Jika ketiga hal ini benar, maka tugas dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="7538b-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="7538b-142">Perkiraan atau aktual yang dibuat untuk pengeluaran hanya dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="7538b-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="7538b-143">**pengeluaran** tercakup di baris kontrak</span><span class="sxs-lookup"><span data-stu-id="7538b-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="7538b-144">**Kategori transaksi** dikonfigurasi sebagai dibebankan pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="7538b-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="7538b-145">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="7538b-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="7538b-146">Jika ketiga hal ini benar, maka **tugas** dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="7538b-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="7538b-147">Perkiraan atau aktual yang dibuat untuk bahan hanya dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="7538b-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="7538b-148">**Bahan** tercakup di baris kontrak</span><span class="sxs-lookup"><span data-stu-id="7538b-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="7538b-149">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kontrak</span><span class="sxs-lookup"><span data-stu-id="7538b-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="7538b-150">Jika kedua hal ini benar, maka **tugas** dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="7538b-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-151">
                    <strong>Mencakup Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7538b-152">
                    <strong>Mencakup Pengeluaran</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7538b-153">
                    <strong>Mencakup Bahan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="7538b-154">
                    <strong>Tugas Disertakan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-155">
                    <strong>Peran</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-156">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-157">
                    <strong>Tugas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="7538b-158">
                    <strong>Dampak pengenaan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-159">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-160">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-161">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-162">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-163">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-164">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-165">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-166">Penagihan pada aktual Waktu: <strong>Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-167">Jenis penagihan pada aktual Pengeluaran: <strong>Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-168">Jenis penagihan pada aktual bahan: <strong>Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-169">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-170">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-171">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-172">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="7538b-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-173">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-174">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-175">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-176">Penagihan pada aktual Waktu: <strong>Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-177">Jenis penagihan pada aktual Pengeluaran: <strong>Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-178">Jenis penagihan pada aktual bahan: <strong>Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-179">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-180">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-181">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-182">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="7538b-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-183">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-184">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-185">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-186">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-187">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7538b-188">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-189">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-190">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-191">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-192">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="7538b-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-193">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-194">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-195">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-196">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-197">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-198">Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-199">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-200">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-201">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-202">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="7538b-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-203">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-204">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-205">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-206">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-207">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-208">Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-209">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-210">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-211">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-212">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="7538b-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-213">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-214">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-215">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-216">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-217">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-218">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-220">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-221">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-222">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-223">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-224">
                    <strong>Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-225">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-226">Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-227">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7538b-228">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-230">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-231">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-232">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-233">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-234">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-235">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-236">Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-237">Jenis penagihan pada aktual Pengeluaran: <strong> Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-238">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-239">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7538b-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-241">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-242">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-243">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-244">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-245">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-246">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7538b-247">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-248">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-249">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="7538b-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="7538b-251">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-252">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-253">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-254">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-255">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-256">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-257">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-258">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-259">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-260">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7538b-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-262">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-263">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-264">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-265">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-266">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7538b-267">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="7538b-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="7538b-268">Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="7538b-269">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="7538b-270">Ya</span><span class="sxs-lookup"><span data-stu-id="7538b-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="7538b-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="7538b-272">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="7538b-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="7538b-273">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="7538b-274">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="7538b-275">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="7538b-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="7538b-276">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-277">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak Dikenakan biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="7538b-278">Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="7538b-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

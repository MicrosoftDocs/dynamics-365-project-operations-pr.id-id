---
title: Konfigurasikan komponen yang dikenakan biaya pada baris kuotasi
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi komponen dikenakan biaya dan yang tidak dikenakan biaya pada baris kuotasi berbasis proyek.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003770"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="32791-103">Mengonfigurasikan komponen yang dikenakan biaya pada baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="32791-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="32791-104">_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_</span><span class="sxs-lookup"><span data-stu-id="32791-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="32791-105">Baris kuotasi berbasis proyek memiliki konsep *menyertakan* komponen dan komponen *yang dapat dikenakan biaya*.</span><span class="sxs-lookup"><span data-stu-id="32791-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="32791-106">Komponen yang tergantung pada:</span><span class="sxs-lookup"><span data-stu-id="32791-106">Included components are subject to:</span></span>

  - <span data-ttu-id="32791-107">Metode penagihan dan pemisahan pelanggan</span><span class="sxs-lookup"><span data-stu-id="32791-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="32791-108">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="32791-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="32791-109">Pengaturan frekuensi faktur yang didefinisikan pada baris kuotasi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="32791-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="32791-110">Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya menggunakan bidang **Tipe Penagihan**.</span><span class="sxs-lookup"><span data-stu-id="32791-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="32791-111">Bidang **Tipe Penagihan** adalah kumpulan opsi yang memungkinkan nilai berikut dalam konteks baris kuotasi:</span><span class="sxs-lookup"><span data-stu-id="32791-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="32791-112">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-112">Chargeable</span></span>
  - <span data-ttu-id="32791-113">Tidak Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="32791-113">Non-chargeable</span></span>

<span data-ttu-id="32791-114">Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori tugas, peran, dan transaksi.</span><span class="sxs-lookup"><span data-stu-id="32791-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="32791-115">Dapat dikenakan Biaya didefinisikan pada tugas untuk baris kuotasi dan berlaku untuk semua kelas transaksi yang disertakan di baris itu.</span><span class="sxs-lookup"><span data-stu-id="32791-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="32791-116">Jika bidang **Sertakan Tugas** diatur ke **Seluruh proyek** atau dibiarkan kosong, tab **Tugas yang dapat dikenakan biaya** tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="32791-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="32791-117">Bisa dikenakan biaya didefinisikan pada peran untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **waktu**.</span><span class="sxs-lookup"><span data-stu-id="32791-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="32791-118">Jika bidang, **Sertakan waktu** diatur ke **Tidak** di baris kuotasi proyek, tab **Peran yang dapat dikenakan biaya** tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="32791-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="32791-119">Bisa dikenakan biaya didefinisikan pada kategori transaksi untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **Pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="32791-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="32791-120">Jika bidang, **Sertakan Pengeluaran** diatur ke **Tidak** di baris kuotasi proyek, tab **Kategori yang dapat dikenakan biaya** tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="32791-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="32791-121">Memperbarui tugas proyek yang akan dikenakan biaya atau tidak dapat dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="32791-122">Tugas proyek dapat dikenakan biaya atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu yang memungkinkan pengaturan berikut.</span><span class="sxs-lookup"><span data-stu-id="32791-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="32791-123">Jika baris kuotasi berbasis proyek mencakup **waktu** dan tugas **T1**, tugas dikaitkan ke baris kuotasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="32791-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="32791-124">Jika ada baris kuotasi kedua yang mencakup **Pengeluaran**, Anda dapat mengaitkan tugas **T1** di baris kuotasi sebagai tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="32791-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="32791-125">Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran yang dicatat di tugas adalah tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="32791-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="32791-126">Jenis penagihan tugas dapat dikonfigurasi pada tab **tugas kena biaya** pada baris kuotasi berbasis proyek dengan memperbarui bidang **jenis penagihan** pada subkisi **tugas tugas baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="32791-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="32791-127">Atau, Anda dapat memperbarui jenis penagihan untuk tugas proyek di bidang **jenis penagihan** pada subkisi dari konfigurasi penagihan tugas proyek yang menunjukkan baris kuotasi yang terkait dengan tugas.</span><span class="sxs-lookup"><span data-stu-id="32791-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="32791-128">Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="32791-129">Peran dapat dikenakan atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu.</span><span class="sxs-lookup"><span data-stu-id="32791-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="32791-130">Jenis penagihan peran dapat dikonfigurasi pada tab **Peran kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **peran kena biaya**.</span><span class="sxs-lookup"><span data-stu-id="32791-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="32791-131">Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="32791-132">Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kuotasi tertentu.</span><span class="sxs-lookup"><span data-stu-id="32791-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="32791-133">Jenis penagihan transaksi dapat dikonfigurasi pada tab **Kategori kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**.</span><span class="sxs-lookup"><span data-stu-id="32791-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="32791-134">Menangani pengenaan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-134">Resolve chargeability</span></span>
<span data-ttu-id="32791-135">Perkiraan atau aktual yang dibuat untuk waktu hanya akan dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="32791-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="32791-136">**Waktu** tercakup di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="32791-137">**Peran** dikonfigurasi sebagai dibebankan pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="32791-138">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="32791-139">Jika ketiga hal ini benar, maka **tugas** juga dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="32791-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="32791-140">Perkiraan atau aktual yang dibuat untuk pengeluaran hanya dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="32791-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="32791-141">**pengeluaran** tercakup di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="32791-142">**Kategori transaksi** dikonfigurasi sebagai dibebankan pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="32791-143">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="32791-144">Jika ketiga hal ini benar, maka **tugas** juga dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="32791-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="32791-145">Perkiraan atau aktual yang dibuat untuk bahan hanya akan dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="32791-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="32791-146">**Bahan** tercakup di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="32791-147">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="32791-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="32791-148">Jika kedua hal ini benar, maka **tugas** juga harus dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="32791-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-149">
                    <strong>Mencakup Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="32791-150">
                    <strong>Mencakup Pengeluaran</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="32791-151">
                    <strong>Mencakup Bahan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="32791-152">
                    <strong>Tugas Disertakan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-153">
                    <strong>Peran</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-155">
                    <strong>Tugas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="32791-156">
                    <strong>Dampak pengenaan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-157">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-158">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-159">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-160">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="32791-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-161">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-162">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-163">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-164">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="32791-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-165">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-166">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-167">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-168">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-169">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-170">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="32791-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-171">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-172">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-173">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-174">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="32791-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-175">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-176">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-177">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-178">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-179">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-180">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="32791-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-181">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-182">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-183">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-184">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-185">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-186">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-187">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-188">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-189">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-190">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="32791-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-191">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-192">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-193">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-194">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-195">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-196">Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-197">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-198">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-199">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-200">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="32791-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-201">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-202">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-203">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-204">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-205">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-206">Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-207">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-208">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-209">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-210">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="32791-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-211">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-212">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-213">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-214">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-215">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-216">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-218">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-219">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-220">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="32791-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-221">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-222">
                    <strong>Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-223">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-224">Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-225">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-226">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-228">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-229">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-230">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="32791-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-231">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-232">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-233">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-234">Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-235">Jenis penagihan pada aktual Pengeluaran: <strong> Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-236">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-237">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="32791-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-239">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-240">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="32791-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-241">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-242">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-243">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-244">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="32791-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-245">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-246">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-247">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="32791-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="32791-249">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-250">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="32791-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-251">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-252">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-253">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-254">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-255">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-256">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-257">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-258">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="32791-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-260">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="32791-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-261">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-262">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-263">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-264">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="32791-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-265">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="32791-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="32791-266">Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="32791-267">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="32791-268">Ya</span><span class="sxs-lookup"><span data-stu-id="32791-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="32791-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="32791-270">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="32791-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="32791-271">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="32791-272">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="32791-273">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="32791-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="32791-274">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-275">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak Dikenakan biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="32791-276">Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="32791-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

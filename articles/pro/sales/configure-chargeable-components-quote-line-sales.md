---
title: Konfigurasikan komponen yang dikenakan biaya pada baris kuotasi
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi komponen dikenakan biaya dan yang tidak dikenakan biaya pada baris kuotasi berbasis proyek.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858297"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="bc5a2-103">Mengonfigurasikan komponen yang dikenakan biaya pada baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="bc5a2-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="bc5a2-104">_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_</span><span class="sxs-lookup"><span data-stu-id="bc5a2-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="bc5a2-105">Baris kuotasi berbasis proyek memiliki konsep *menyertakan* komponen dan komponen *yang dapat dikenakan biaya*.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="bc5a2-106">Komponen yang tergantung pada:</span><span class="sxs-lookup"><span data-stu-id="bc5a2-106">Included components are subject to:</span></span>

  - <span data-ttu-id="bc5a2-107">Metode penagihan dan pemisahan pelanggan</span><span class="sxs-lookup"><span data-stu-id="bc5a2-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="bc5a2-108">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="bc5a2-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="bc5a2-109">Pengaturan frekuensi faktur yang didefinisikan pada baris kuotasi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="bc5a2-110">Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya menggunakan bidang **Tipe Penagihan**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="bc5a2-111">Bidang **Tipe Penagihan** adalah kumpulan opsi yang memungkinkan nilai berikut dalam konteks baris kuotasi:</span><span class="sxs-lookup"><span data-stu-id="bc5a2-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="bc5a2-112">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-112">Chargeable</span></span>
  - <span data-ttu-id="bc5a2-113">Tidak Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-113">Non-chargeable</span></span>

<span data-ttu-id="bc5a2-114">Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori tugas, peran, dan transaksi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="bc5a2-115">Dapat dikenakan Biaya didefinisikan pada tugas untuk baris kuotasi dan berlaku untuk semua kelas transaksi yang disertakan di baris itu.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="bc5a2-116">Jika bidang **Sertakan Tugas** diatur ke **Seluruh proyek** atau dibiarkan kosong, tab **Tugas yang dapat dikenakan biaya** tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="bc5a2-117">Bisa dikenakan biaya didefinisikan pada peran untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **waktu**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="bc5a2-118">Jika bidang, **Sertakan waktu** diatur ke **Tidak** di baris kuotasi proyek, tab **Peran yang dapat dikenakan biaya** tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="bc5a2-119">Bisa dikenakan biaya didefinisikan pada kategori transaksi untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **Pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="bc5a2-120">Jika bidang, **Sertakan Pengeluaran** diatur ke **Tidak** di baris kuotasi proyek, tab **Kategori yang dapat dikenakan biaya** tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="bc5a2-121">Memperbarui tugas proyek yang akan dikenakan biaya atau tidak dapat dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="bc5a2-122">Tugas proyek dapat dikenakan biaya atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu yang memungkinkan pengaturan berikut.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="bc5a2-123">Jika baris kuotasi berbasis proyek mencakup **waktu** dan tugas **T1**, tugas dikaitkan ke baris kuotasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="bc5a2-124">Jika ada baris kuotasi kedua yang mencakup **Pengeluaran**, Anda dapat mengaitkan tugas **T1** di baris kuotasi sebagai tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="bc5a2-125">Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran yang dicatat di tugas adalah tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="bc5a2-126">Jenis penagihan tugas dapat dikonfigurasi pada tab **tugas kena biaya** pada baris kuotasi berbasis proyek dengan memperbarui bidang **jenis penagihan** pada subkisi **tugas tugas baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="bc5a2-127">Atau, Anda dapat memperbarui jenis penagihan untuk tugas proyek di bidang **jenis penagihan** pada subkisi dari konfigurasi penagihan tugas proyek yang menunjukkan baris kuotasi yang terkait dengan tugas.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="bc5a2-128">Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="bc5a2-129">Peran dapat dikenakan atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="bc5a2-130">Jenis penagihan peran dapat dikonfigurasi pada tab **Peran kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **peran kena biaya**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="bc5a2-131">Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="bc5a2-132">Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kuotasi tertentu.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="bc5a2-133">Jenis penagihan transaksi dapat dikonfigurasi pada tab **Kategori kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="bc5a2-134">Menangani pengenaan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-134">Resolve chargeability</span></span>
<span data-ttu-id="bc5a2-135">Perkiraan atau aktual yang dibuat untuk waktu hanya akan dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="bc5a2-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="bc5a2-136">**Waktu** tercakup di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="bc5a2-137">**Peran** dikonfigurasi sebagai dibebankan pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="bc5a2-138">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="bc5a2-139">Jika ketiga hal ini benar, maka **tugas** juga dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="bc5a2-140">Perkiraan atau aktual yang dibuat untuk pengeluaran hanya dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="bc5a2-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="bc5a2-141">**pengeluaran** tercakup di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="bc5a2-142">**Kategori transaksi** dikonfigurasi sebagai dibebankan pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="bc5a2-143">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="bc5a2-144">Jika ketiga hal ini benar, maka **tugas** juga dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="bc5a2-145">Perkiraan atau aktual yang dibuat untuk bahan hanya akan dianggap dibebankan jika:</span><span class="sxs-lookup"><span data-stu-id="bc5a2-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="bc5a2-146">**Bahan** tercakup di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="bc5a2-147">**Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="bc5a2-148">Jika kedua hal ini benar, maka **tugas** juga harus dikonfigurasi sebagai dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="bc5a2-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-149">
                    <strong>Mencakup Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="bc5a2-150">
                    <strong>Mencakup Pengeluaran</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="bc5a2-151">
                    <strong>Mencakup Bahan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="bc5a2-152">
                    <strong>Tugas Disertakan</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-153">
                    <strong>Peran</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-154">
                    <strong>Kategori</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-155">
                    <strong>Tugas</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="bc5a2-156">
                    <strong>Dampak pengenaan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-157">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-158">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-159">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-160">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-161">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-162">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-163">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-164">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-165">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-166">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-167">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-168">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-169">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-170">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="bc5a2-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-171">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-172">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-173">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-174">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-175">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-176">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-177">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-178">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-179">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-180">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="bc5a2-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-181">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-182">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-183">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-184">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-185">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-186">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-187">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-188">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-189">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-190">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="bc5a2-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-191">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-192">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-193">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-194">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-195">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-196">Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-197">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-198">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-199">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-200">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="bc5a2-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-201">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-202">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-203">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-204">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-205">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-206">Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-207">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-208">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-209">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-210">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="bc5a2-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-211">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-212">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-213">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-214">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-215">Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-216">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-218">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-219">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-220">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-221">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-222">
                    <strong>Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-223">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-224">Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-225">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-226">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-228">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-229">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-230">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-231">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-232">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-233">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-234">Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-235">Jenis penagihan pada aktual Pengeluaran: <strong> Tidak Dikenakan biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-236">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-237">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="bc5a2-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-239">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-240">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-241">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-242">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-243">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-244">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-245">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-246">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-247">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="bc5a2-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="bc5a2-249">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-250">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-251">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-252">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-253">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-254">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-255">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-256">Jenis penagihan pada aktual bahan: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-257">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-258">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="bc5a2-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-260">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-261">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-262">Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-263">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-264">Penagihan pada aktual Waktu: Dikenakan Biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-265">Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="bc5a2-266">Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="bc5a2-267">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="bc5a2-268">Ya</span><span class="sxs-lookup"><span data-stu-id="bc5a2-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="bc5a2-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="bc5a2-270">Keseluruhan proyek</span><span class="sxs-lookup"><span data-stu-id="bc5a2-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="bc5a2-271">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="bc5a2-272">
                    <strong>Tidak Dikenakan Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="bc5a2-273">Tidak dapat diatur</span><span class="sxs-lookup"><span data-stu-id="bc5a2-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="bc5a2-274">Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-275">Jenis penagihan pada aktual Pengeluaran:<strong> Tidak Dikenakan biaya </strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="bc5a2-276">Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bc5a2-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]

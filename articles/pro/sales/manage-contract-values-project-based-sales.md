---
title: Sekilas baris kontrak berbasis proyek
description: Topik ini menyediakan informasi tentang bekerja dengan baris kontrak berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858162"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="afb19-103">Sekilas baris kontrak berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="afb19-103">Project-based contract lines overview</span></span>

<span data-ttu-id="afb19-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="afb19-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="afb19-105">Baris kontrak berbasis proyek di Dynamics 365 Project Operations dirancang untuk menyimpan estimasi dan pengaturan penagihan untuk komponen tertentu dari pekerjaan proyek pada suatu kesepakatan.</span><span class="sxs-lookup"><span data-stu-id="afb19-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="afb19-106">Struktur baris kontrak berbasis proyek diperluas untuk perkiraan proyek dan skenario penagihan dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="afb19-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="afb19-107">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="afb19-107">Billing method</span></span>
- <span data-ttu-id="afb19-108">Pemetaan Proyek dan Tugas</span><span class="sxs-lookup"><span data-stu-id="afb19-108">Project and task mapping</span></span>
- <span data-ttu-id="afb19-109">Termasuk kelas transaksi</span><span class="sxs-lookup"><span data-stu-id="afb19-109">Included transaction classes</span></span>
- <span data-ttu-id="afb19-110">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="afb19-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="afb19-111">Konfigurasi ketertagihan</span><span class="sxs-lookup"><span data-stu-id="afb19-111">Chargeability setup</span></span>
- <span data-ttu-id="afb19-112">Memperkirakan penggunaan rincian baris kontrak</span><span class="sxs-lookup"><span data-stu-id="afb19-112">Estimates using contract line details</span></span>
- <span data-ttu-id="afb19-113">Pelanggan Baris Kontrak</span><span class="sxs-lookup"><span data-stu-id="afb19-113">Contract line customers</span></span>

<span data-ttu-id="afb19-114">Tabel berikut mencakup bidang pada tab **Umum** baris kontrak berbasis proyek yang membantu mengkonfigurasikan dasar estimasi terperinci dan dari awal serta pengaturan penagihan untuk pekerjaan berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="afb19-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="afb19-115">Bidang</span><span class="sxs-lookup"><span data-stu-id="afb19-115">Field</span></span> | <span data-ttu-id="afb19-116">KETERANGAN</span><span class="sxs-lookup"><span data-stu-id="afb19-116">Description</span></span> | <span data-ttu-id="afb19-117">Dampak hilir</span><span class="sxs-lookup"><span data-stu-id="afb19-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="afb19-118">**Nama**</span><span class="sxs-lookup"><span data-stu-id="afb19-118">**Name**</span></span> | <span data-ttu-id="afb19-119">Nama rekaman baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="afb19-119">Name of the contract line.</span></span> <span data-ttu-id="afb19-120">Ini mengidentifikasi komponen diskrit dari kontrak yang sedang diperkirakan.</span><span class="sxs-lookup"><span data-stu-id="afb19-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="afb19-121">Untuk kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari nilai baris kuotasi berbasis proyek yang terkait.</span><span class="sxs-lookup"><span data-stu-id="afb19-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="afb19-122">Nilai yang disalin ke baris faktur proyek yang dibuat dari baris kontrak ini saat faktur dibuat.</span><span class="sxs-lookup"><span data-stu-id="afb19-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="afb19-123">**Metode Penagihan**</span><span class="sxs-lookup"><span data-stu-id="afb19-123">**Billing Method**</span></span> | <span data-ttu-id="afb19-124">Di kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari bidang terkait di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="afb19-125">Ini adalah rangkaian pilihan yang menunjukkan dua model kontrak utama yang didukung oleh Project Operations:</span><span class="sxs-lookup"><span data-stu-id="afb19-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="afb19-126">- **Harga Tetap**</span><span class="sxs-lookup"><span data-stu-id="afb19-126">- **Fixed Price**</span></span></br><span data-ttu-id="afb19-127">- **Waktu dan Materi**</span><span class="sxs-lookup"><span data-stu-id="afb19-127">- **Time and Material**</span></span> | <span data-ttu-id="afb19-128">Berdasarkan metode penagihan baris kontrak yang dirujuk, transaksi aktual akan diproses.</span><span class="sxs-lookup"><span data-stu-id="afb19-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="afb19-129">Jika baris kontrak yang dirujuk oleh aktual memiliki metode penagihan waktu dan material, maka biaya dan rekaman aktual penjualan yang belum ditagih dibuat.</span><span class="sxs-lookup"><span data-stu-id="afb19-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="afb19-130">Jika baris kontrak yang dirujuk oleh metode aktual memiliki metode penagihan harga tetap, hanya aktual biaya yang dibuat.</span><span class="sxs-lookup"><span data-stu-id="afb19-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="afb19-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="afb19-131">**Project**</span></span> | <span data-ttu-id="afb19-132">Gunakan bidang ini untuk mengidentifikasi proyek yang akan digunakan untuk melaksanakan pekerjaan pada kesepakatan ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="afb19-133">Nilai ini akan digunakan secara bersama-sama dengan **Kelas Transaksi Tercakup** dan **Tugas Tercakup** untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="afb19-134">**Tugas Disertakan**</span><span class="sxs-lookup"><span data-stu-id="afb19-134">**Included Tasks**</span></span> | <span data-ttu-id="afb19-135">Menunjukkan jika baris kontrak ini mencakup semua tugas proyek untuk proyek yang dipilih atau hanya subset dari tugas.</span><span class="sxs-lookup"><span data-stu-id="afb19-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="afb19-136">Ini adalah rangkaian pilihan yang memiliki nilai yang mungkin berikut:</span><span class="sxs-lookup"><span data-stu-id="afb19-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="afb19-137">- **Semua Tugas Proyek**</span><span class="sxs-lookup"><span data-stu-id="afb19-137">- **All Project Tasks**</span></span></br><span data-ttu-id="afb19-138">- **Hanya tugas proyek yang dipilih**.</span><span class="sxs-lookup"><span data-stu-id="afb19-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="afb19-139">Nilai kosong pada bidang ini sama dengan memilih **semua tugas proyek**.</span><span class="sxs-lookup"><span data-stu-id="afb19-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="afb19-140">Jika **tugas yang dipilih saja** dipilih, Anda dapat memilih tugas tertentu dan mengaitkannya ke baris kontrak ini di tab **penyiapan penagihan tugas** pada halaman **proyek**.</span><span class="sxs-lookup"><span data-stu-id="afb19-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="afb19-141">Nilai ini akan digunakan bersama dengan **Proyek** dan kelas **Transaksi yang tercakup** untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="afb19-142">**Sertakan Waktu**</span><span class="sxs-lookup"><span data-stu-id="afb19-142">**Include Time**</span></span> | <span data-ttu-id="afb19-143">Nilai **Ya**/**Tidak** menunjukkan apakah transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="afb19-144">Nilai **Tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="afb19-145">Nilai **ya** menunjukkan bahwa akan disertakan.</span><span class="sxs-lookup"><span data-stu-id="afb19-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="afb19-146">Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="afb19-147">**Sertakan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="afb19-147">**Include Expense**</span></span> | <span data-ttu-id="afb19-148">Nilai **Ya**/**Tidak** menunjukkan apakah biaya pengeluaran pada proyek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="afb19-149">Nilai **Tidak** menunjukkan bahwa biaya pengeluaran tidak akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="afb19-150">Nilai **ya** menunjukkan bahwa akan disertakan.</span><span class="sxs-lookup"><span data-stu-id="afb19-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="afb19-151">Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="afb19-152">**Termasuk Bahan**</span><span class="sxs-lookup"><span data-stu-id="afb19-152">**Include Materials**</span></span> | <span data-ttu-id="afb19-153">Nilai **Ya**/**Tidak** menunjukkan apakah biaya bahan pada proyek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="afb19-154">Nilai **Tidak** menunjukkan bahwa biaya bahan tidak akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="afb19-155">Nilai **ya** menunjukkan bahwa akan disertakan.</span><span class="sxs-lookup"><span data-stu-id="afb19-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="afb19-156">Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="afb19-157">**Sertakan Tarif**</span><span class="sxs-lookup"><span data-stu-id="afb19-157">**Include Fee**</span></span> | <span data-ttu-id="afb19-158">Nilai **Ya**/**Tidak** menunjukkan apakah ongkos pada proyek yang dipilih akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="afb19-159">Nilai **Tidak** menunjukkan bahwa ongkos tidak akan disertakan pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="afb19-160">Nilai **ya** menunjukkan bahwa akan disertakan.</span><span class="sxs-lookup"><span data-stu-id="afb19-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="afb19-161">Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="afb19-162">**Jumlah yang Dikontrak**</span><span class="sxs-lookup"><span data-stu-id="afb19-162">**Contracted Amount**</span></span> | <span data-ttu-id="afb19-163">Pada baris kontrak harga tetap, jumlah ini adalah nilai yang disepakati yang akan ditagih kepada pelanggan untuk semua komponen kerja yang terkait dengan baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="afb19-164">Pada baris kontrak waktu dan material, jumlah ini adalah nilai estimasi tentang apa yang akan ditagih kepada pelanggan untuk semua komponen kerja yang terkait pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="afb19-165">Di kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari bidang terkait di baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="afb19-166">Bila baris kontrak berbasis proyek memiliki rincian baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="afb19-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="afb19-167">Bila baris kontrak memiliki rincian baris, nilai ini dapat dimodifikasi dengan mengubah jumlah rincian baris.</span><span class="sxs-lookup"><span data-stu-id="afb19-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="afb19-168">Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan jumlah sebelum pajak pada tonggak pencapaian penagihan berkala.</span><span class="sxs-lookup"><span data-stu-id="afb19-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="afb19-169">**Perkiraan Pajak**</span><span class="sxs-lookup"><span data-stu-id="afb19-169">**Estimated Tax**</span></span> | <span data-ttu-id="afb19-170">Pengguna dapat mengedit bidang ini untuk memasukkan estimasi jumlah pajak pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="afb19-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="afb19-171">Bila baris kontrak berbasis proyek memiliki rincian baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="afb19-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="afb19-172">Bila baris kontrak memiliki rincian baris, nilai ini dapat dimodifikasi dengan mengubah jumlah pajak pada rincian baris.</span><span class="sxs-lookup"><span data-stu-id="afb19-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="afb19-173">Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan pajak pada tonggak pencapaian penagihan berkala.</span><span class="sxs-lookup"><span data-stu-id="afb19-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="afb19-174">**Jumlah Kontrak Setelah Pajak**</span><span class="sxs-lookup"><span data-stu-id="afb19-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="afb19-175">Jumlah baris kontrak setelah pajak.</span><span class="sxs-lookup"><span data-stu-id="afb19-175">The contract line amount after tax.</span></span> <span data-ttu-id="afb19-176">Bidang ini hanya baca dan dihitung sebagai **jumlah kontrak + pajak**.</span><span class="sxs-lookup"><span data-stu-id="afb19-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="afb19-177">Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan tonggak pencapaian penagihan berkala.</span><span class="sxs-lookup"><span data-stu-id="afb19-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="afb19-178">**Batas Jangan terlampaui**</span><span class="sxs-lookup"><span data-stu-id="afb19-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="afb19-179">Pengguna dapat mengedit bidang ini dan hanya tersedia pada baris kontrak berbasis proyek yang mengatur metode penagihan sebagai waktu dan material.</span><span class="sxs-lookup"><span data-stu-id="afb19-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="afb19-180">Pengguna dapat mengedit bidang ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-180">The user can edit this field.</span></span> <span data-ttu-id="afb19-181">Bila aktual untuk waktu atau dan material merujuk baris kontrak ini untuk waktu dan material, jumlah pada aktual dievaluasi terhadap batas yang tidak boleh dilebihi pada baris kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="afb19-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="afb19-182">Evaluasi ini diselesaikan setelah jumlah pembelanjaan dan komitmen diperhitungkan.</span><span class="sxs-lookup"><span data-stu-id="afb19-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="afb19-183">**Anggaran Pelanggan**</span><span class="sxs-lookup"><span data-stu-id="afb19-183">**Customer Budget**</span></span> | <span data-ttu-id="afb19-184">Bidang ini dapat diedit dan disalin dari bidang terkait di baris kuotasi, jika kontrak dibuat dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="afb19-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="afb19-185">Bidang ini hanya digunakan untuk informasi dan tidak memiliki signifikansi hilir.</span><span class="sxs-lookup"><span data-stu-id="afb19-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="afb19-186">Aturan validasi untuk pilihan pada tab Umum baris kontrak berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="afb19-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="afb19-187">Aturan 1: jika bidang **tugas yang disertakan** kosong atau diatur ke **semua tugas proyek**, semua tugas proyek disertakan pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="afb19-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="afb19-188">Aturan 2: bila bidang **tugas yang disertakan** kosong atau diatur secara eksplisit ke **semua tugas proyek**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada satu baris kontrak berbasis proyek dari kontrak.</span><span class="sxs-lookup"><span data-stu-id="afb19-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="afb19-189">Aturan 3: bila bidang **tugas yang disertakan** diatur ke **tugas proyek yang dipilih saja**, proyek dan kelas transaksi tertentu dapat disertakan pada beberapa baris kontrak berbasis proyek dari kontrak.</span><span class="sxs-lookup"><span data-stu-id="afb19-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="afb19-190">
                    <strong>Kontrak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="afb19-191">
                    <strong>Baris Kontrak</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="afb19-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="afb19-193">
                    <strong>Tugas yang Disertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="afb19-194">
                    <strong>Sertakan Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="afb19-195">
                    <strong>Sertakan Pengeluaran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="afb19-196">
                    <strong>Termasuk Bahan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="afb19-197">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="afb19-198">
                    <strong>Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="afb19-199">
                    <strong>Valid/tidak valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="afb19-200">
                    <strong>Alasan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="afb19-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-201">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-202">CL1</span><span class="sxs-lookup"><span data-stu-id="afb19-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-203">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-204">Kosong</span><span class="sxs-lookup"><span data-stu-id="afb19-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-205">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-206">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-207">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-208">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-209">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="afb19-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-210">Pelanggaran aturan #2.</span><span class="sxs-lookup"><span data-stu-id="afb19-210">Violation of Rule #2.</span></span> <span data-ttu-id="afb19-211">Waktu, Pengeluaran, Bahan, dan Ongkos pada proyek P1 tercakup di baris Kontrak CL1 dan CL2.</span><span class="sxs-lookup"><span data-stu-id="afb19-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-212">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-213">CL2</span><span class="sxs-lookup"><span data-stu-id="afb19-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-214">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-215">Kosong</span><span class="sxs-lookup"><span data-stu-id="afb19-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-216">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-217">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-218">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-219">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-220">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-221">CL1</span><span class="sxs-lookup"><span data-stu-id="afb19-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-222">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-223">Kosong</span><span class="sxs-lookup"><span data-stu-id="afb19-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-224">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-225">No</span><span class="sxs-lookup"><span data-stu-id="afb19-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-226">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-227">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-228">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="afb19-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-229">Pelanggaran aturan #2.</span><span class="sxs-lookup"><span data-stu-id="afb19-229">Violation of Rule #2.</span></span> <span data-ttu-id="afb19-230">Waktu, Bahan, dan Ongkos pada proyek P1 tercakup di baris Kontrak CL1 dan CL2.</span><span class="sxs-lookup"><span data-stu-id="afb19-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-231">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-232">CL2</span><span class="sxs-lookup"><span data-stu-id="afb19-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-233">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-234">Kosong</span><span class="sxs-lookup"><span data-stu-id="afb19-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-235">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-236">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-237">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-238">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-239">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-240">CL1</span><span class="sxs-lookup"><span data-stu-id="afb19-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-241">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-242">Kosong</span><span class="sxs-lookup"><span data-stu-id="afb19-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-243">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-244">No</span><span class="sxs-lookup"><span data-stu-id="afb19-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-245">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-246">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-247">Valid</span><span class="sxs-lookup"><span data-stu-id="afb19-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-248">Waktu, Bahan, dan Ongkos pada proyek P1 tercakup di CL1.</span><span class="sxs-lookup"><span data-stu-id="afb19-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="afb19-249">pengeluaran pada proyek P1 disertakan pada CL2.</span><span class="sxs-lookup"><span data-stu-id="afb19-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="afb19-250">Tidak ada tumpang tindih dalam hal yang tercakup di setiap baris Kontrak dan oleh karena itu valid.</span><span class="sxs-lookup"><span data-stu-id="afb19-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-251">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-252">CL2</span><span class="sxs-lookup"><span data-stu-id="afb19-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-253">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-254">Kosong</span><span class="sxs-lookup"><span data-stu-id="afb19-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-255">No</span><span class="sxs-lookup"><span data-stu-id="afb19-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-256">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-257">No</span><span class="sxs-lookup"><span data-stu-id="afb19-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-258">No</span><span class="sxs-lookup"><span data-stu-id="afb19-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-259">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-260">CL1</span><span class="sxs-lookup"><span data-stu-id="afb19-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-261">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-262">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="afb19-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-263">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-264">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-265">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-266">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-267">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="afb19-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-268">Pelanggaran aturan #2</span><span class="sxs-lookup"><span data-stu-id="afb19-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="afb19-269">C1 mencakup Waktu, Bahan, Pengeluaran dan Ongkos pada subset tugas di proyek P1.</span><span class="sxs-lookup"><span data-stu-id="afb19-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="afb19-270">CL2 mencakup Waktu, Bahan, Pengeluaran dan Ongkos untuk seluruh proyek P1, sehingga tumpang tindih dengan yang tercakup di C1.</span><span class="sxs-lookup"><span data-stu-id="afb19-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-271">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-272">CL2</span><span class="sxs-lookup"><span data-stu-id="afb19-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-273">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-274">Kosong</span><span class="sxs-lookup"><span data-stu-id="afb19-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-275">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-276">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-277">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-278">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-279">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-280">CL1</span><span class="sxs-lookup"><span data-stu-id="afb19-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-281">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-282">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="afb19-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-283">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-284">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-285">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-286">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-287">Valid</span><span class="sxs-lookup"><span data-stu-id="afb19-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="afb19-288">Per aturan #3</span><span class="sxs-lookup"><span data-stu-id="afb19-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="afb19-289">C1 mencakup Waktu, Pengeluaran, Bahan, dan Ongkos pada subset tugas di proyek P1.</span><span class="sxs-lookup"><span data-stu-id="afb19-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="afb19-290">CL2 mencakup Waktu, Pengeluaran, Bahan, dan Ongkos untuk subset tugas di proyek P1.</span><span class="sxs-lookup"><span data-stu-id="afb19-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="afb19-291">Satu-satunya validasi tambahan adalah seputar subset tugas di CL1, berbeda dengan subset tugas di CL2 untuk memastikan tidak ada tumpang tindih di sana.</span><span class="sxs-lookup"><span data-stu-id="afb19-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="afb19-292">Hal ini dilakukan oleh sistem saat tugas terkait.</span><span class="sxs-lookup"><span data-stu-id="afb19-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="afb19-293">C1</span><span class="sxs-lookup"><span data-stu-id="afb19-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="afb19-294">CL2</span><span class="sxs-lookup"><span data-stu-id="afb19-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-295">P1</span><span class="sxs-lookup"><span data-stu-id="afb19-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="afb19-296">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="afb19-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-297">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="afb19-298">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-299">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="afb19-300">Ya</span><span class="sxs-lookup"><span data-stu-id="afb19-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
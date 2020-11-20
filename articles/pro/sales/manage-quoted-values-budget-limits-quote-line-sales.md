---
title: Sekilas baris kuotasi berbasis proyek - lite
description: Topik ini memberikan informasi tentang menggunakan baris kuotasi berbasis proyek untuk pekerjaan proyek. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181096"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="d92df-104">Sekilas baris kuotasi berbasis proyek - lite</span><span class="sxs-lookup"><span data-stu-id="d92df-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="d92df-105">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="d92df-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d92df-106">Baris kuotasi berbasis proyek dirancang untuk membantu memperkirakan pekerjaan proyek pada keterlibatan.</span><span class="sxs-lookup"><span data-stu-id="d92df-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d92df-107">Struktur baris kuotasi berbasis proyek diperluas untuk perkiraan proyek dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="d92df-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d92df-108">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="d92df-108">Billing Method</span></span>
- <span data-ttu-id="d92df-109">Pemetaan Proyek dan Tugas</span><span class="sxs-lookup"><span data-stu-id="d92df-109">Project and Task Mapping</span></span>
- <span data-ttu-id="d92df-110">Termasuk kelas transaksi</span><span class="sxs-lookup"><span data-stu-id="d92df-110">Included Transaction classes</span></span>
- <span data-ttu-id="d92df-111">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="d92df-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d92df-112">Konfigurasi ketertagihan</span><span class="sxs-lookup"><span data-stu-id="d92df-112">Chargeability setup</span></span>
- <span data-ttu-id="d92df-113">Estimasi menggunakan rincian baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="d92df-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d92df-114">Pelanggan Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="d92df-114">Quote line Customers</span></span>

<span data-ttu-id="d92df-115">Tabel berikut menyediakan informasi tentang bidang pada tab **Umum** baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="d92df-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d92df-116">Bidang ini membantu membuat dasar untuk estimasi yang rinci dan komprehensif untuk pekerjaan proyek.</span><span class="sxs-lookup"><span data-stu-id="d92df-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d92df-117">**Bidang**</span><span class="sxs-lookup"><span data-stu-id="d92df-117">**Field**</span></span> | <span data-ttu-id="d92df-118">**Keterangan**</span><span class="sxs-lookup"><span data-stu-id="d92df-118">**Description**</span></span> | <span data-ttu-id="d92df-119">**Dampak hilir**</span><span class="sxs-lookup"><span data-stu-id="d92df-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d92df-120">Nama</span><span class="sxs-lookup"><span data-stu-id="d92df-120">Name</span></span> | <span data-ttu-id="d92df-121">Nama baris kuotasi yang seharusnya membantu Anda mengidentifikasi komponen diskrit dari kuotasi yang sedang diperkirakan.</span><span class="sxs-lookup"><span data-stu-id="d92df-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d92df-122">Disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-123">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="d92df-123">Billing Method</span></span> | <span data-ttu-id="d92df-124">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang yang sesuai pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="d92df-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d92df-125">Bidang ini mencakup dua model kontrak utama yang didukung oleh Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d92df-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d92df-126">- Harga tetap</span><span class="sxs-lookup"><span data-stu-id="d92df-126">- Fixed price</span></span></br><span data-ttu-id="d92df-127">- Waktu dan bahan.</span><span class="sxs-lookup"><span data-stu-id="d92df-127">- Time and material.</span></span>| <span data-ttu-id="d92df-128">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-129">Project</span><span class="sxs-lookup"><span data-stu-id="d92df-129">Project</span></span> | <span data-ttu-id="d92df-130">Gunakan bidang opsional ini untuk mengidentifikasi proyek yang akan digunakan untuk melakukan pekerjaan pada keterlibatan ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d92df-131">Saat dipetakan ke baris kuotasi, proyek akan membantu dengan pengaturan tugas yang dapat dibebankan dan juga dengan mendatangkan estimasi berbasis proyek ke baris kuotasi sebagai rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d92df-132">Ketika proyek tidak dipetakan ke baris kuotasi berbasis proyek, perkiraan harus dibuat secara manual dengan membuat detail setiap baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d92df-133">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d92df-134">Tugas Disertakan</span><span class="sxs-lookup"><span data-stu-id="d92df-134">Included Tasks</span></span> | <span data-ttu-id="d92df-135">Menunjukkan jika baris kuotasi ini digunakan untuk semua atau sebagian tugas proyek untuk proyek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="d92df-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d92df-136">Bidang ini memiliki kemungkinan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="d92df-136">This field has the following possible values:</span></span></br><span data-ttu-id="d92df-137">- Semua tugas proyek</span><span class="sxs-lookup"><span data-stu-id="d92df-137">- All project tasks</span></span></br><span data-ttu-id="d92df-138">- Hanya tugas proyek yang dipilih</span><span class="sxs-lookup"><span data-stu-id="d92df-138">- Selected project tasks only</span></span></br><span data-ttu-id="d92df-139">Nilai kosong di bidang ini setara dengan pilihan **semua tugas proyek**.</span><span class="sxs-lookup"><span data-stu-id="d92df-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d92df-140">Bila **Hanya tugas proyek yang dipilih** dipilih kemudian pada halaman proyek, tab **pengaturan penagihan tugas** memungkinkan Anda untuk memilih tugas tertentu untuk mengasosiasikan mereka ke baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d92df-141">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-142">Sertakan Waktu</span><span class="sxs-lookup"><span data-stu-id="d92df-142">Include Time</span></span> | <span data-ttu-id="d92df-143">Peringatan **ya**/**tidak** menunjukkan jika transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d92df-144">Nilai **tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d92df-145">Nilai **Ya** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d92df-146">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-147">Sertakan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="d92df-147">Include Expense</span></span> | <span data-ttu-id="d92df-148">Peringatan **ya**/**tidak** menunjukkan jika biaya pengeluaran pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d92df-149">Nilai **tidak** menunjukkan bahwa biaya pengeluaran tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d92df-150">Nilai **tidak** menunjukkan bahwa biaya pengeluaran akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d92df-151">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-152">Sertakan Tarif</span><span class="sxs-lookup"><span data-stu-id="d92df-152">Include Fee</span></span> | <span data-ttu-id="d92df-153">Peringatan **ya**/**tidak** menunjukkan jika ongkos pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d92df-154">Nilai **tidak** menunjukkan bahwa ongkos tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d92df-155">Nilai **tidak** menunjukkan bahwa ongkos akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d92df-156">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-157">Jumlah Kuotasi</span><span class="sxs-lookup"><span data-stu-id="d92df-157">Quoted Amount</span></span> | <span data-ttu-id="d92df-158">Ini adalah jumlah yang akan ditawarkan untuk pelanggan untuk semua pekerjaan yang diperkirakan pada baris kuotasi berbasis proyek ini.</span><span class="sxs-lookup"><span data-stu-id="d92df-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d92df-159">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang **Anggaran Pelanggan** pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="d92df-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d92df-160">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d92df-161">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-162">Perkiraan Pajak</span><span class="sxs-lookup"><span data-stu-id="d92df-162">Estimated Tax</span></span> | <span data-ttu-id="d92df-163">Ini adalah bidang yang dapat diedit bagi pengguna untuk menambahkan estimasi jumlah pajak pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d92df-164">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d92df-165">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-166">Jumlah Kuotasi Setelah Pajak</span><span class="sxs-lookup"><span data-stu-id="d92df-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="d92df-167">Bidang ini adalah jumlah baris kuotasi setelah pajak dan bersifat hanya baca.</span><span class="sxs-lookup"><span data-stu-id="d92df-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d92df-168">Jumlah dalam bidang ini dihitung sebagai *jumlah yang ditawarkan + pajak*.</span><span class="sxs-lookup"><span data-stu-id="d92df-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d92df-169">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-170">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="d92df-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="d92df-171">Bidang ini dapat diedit dan hanya tersedia pada baris kuotasi berbasis proyek yang memiliki metode penagihan **waktu dan bahan**.</span><span class="sxs-lookup"><span data-stu-id="d92df-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d92df-172">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d92df-173">Anggaran Pelanggan</span><span class="sxs-lookup"><span data-stu-id="d92df-173">Customer Budget</span></span> | <span data-ttu-id="d92df-174">Bidang ini dapat diedit dan disalin dari bidang yang sesuai pada baris peluang jika kuotasi dibuat dari peluang.</span><span class="sxs-lookup"><span data-stu-id="d92df-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d92df-175">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="d92df-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d92df-176">Aturan validasi untuk bidang pada tab Umum baris kuotasi berdasarkan proyek</span><span class="sxs-lookup"><span data-stu-id="d92df-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d92df-177">**Aturan 1**: jika bidang **tugas yang disertakan** kosong, atau jika diatur ke **semua tugas proyek**, proyek disertakan dalam baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="d92df-178">**Aturan 2**: jika bidang **tugas yang disertakan** kosong, atau jika diatur ke **semua tugas proyek**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada satu baris kuotasi berbasis proyek dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d92df-179">**Aturan 3**: jika bidang **tugas yang disertakan** diatur ke **Hanya tugas proyek yang dipilih**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada beberapa baris kuotasi berbasis proyek dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="d92df-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d92df-180">**Aturan 4**: jika peluang memiliki beberapa kuotasi, ada baris kuotasi dari kuotasi berbeda yang semua mereferensi proyek yang sama dan mencakup kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="d92df-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d92df-181">**Aturan 5**: jika kuotasi bukan milik peluang yang sama, mereka tidak dapat menyertakan kelas proyek dan transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="d92df-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d92df-182">
                    <strong>Peluang</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d92df-183">
                    <strong>Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d92df-184">
                    <strong>Baris Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d92df-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="d92df-186">
                    <strong>Tugas yang Disertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d92df-187">
                    <strong>Sertakan Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d92df-188">
                    <strong>Sertakan Pengeluaran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d92df-189">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d92df-190">
                    <strong>Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d92df-191">
                    <strong>Valid/tidak valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d92df-192">
                    <strong>Alasan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d92df-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-193">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-194">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-195">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-196">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-197">Kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-198">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-199">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-200">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-201">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="d92df-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-202">Pelanggaran aturan #2.</span><span class="sxs-lookup"><span data-stu-id="d92df-202">Violation of Rule #2.</span></span> <span data-ttu-id="d92df-203">Waktu, pengeluaran, dan biaya pada proyek P1 disertakan pada baris kuotasi QL1 dan QL2.</span><span class="sxs-lookup"><span data-stu-id="d92df-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-204">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-205">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-206">QL2</span><span class="sxs-lookup"><span data-stu-id="d92df-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-207">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-208">Kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-209">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-210">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-211">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-212">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-213">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-214">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-215">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-216">Kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-217">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-218">No</span><span class="sxs-lookup"><span data-stu-id="d92df-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-219">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-220">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="d92df-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-221">Pelanggaran aturan #2.</span><span class="sxs-lookup"><span data-stu-id="d92df-221">Violation of Rule #2.</span></span> <span data-ttu-id="d92df-222">Waktu dan ongkos pada proyek P1 disertakan pada baris kuotasi QL1 dan QL2.</span><span class="sxs-lookup"><span data-stu-id="d92df-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-223">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-224">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-225">QL2</span><span class="sxs-lookup"><span data-stu-id="d92df-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-226">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-227">Kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-228">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-229">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-230">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-231">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-232">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-233">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-234">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-235">Kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-236">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-237">No</span><span class="sxs-lookup"><span data-stu-id="d92df-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-238">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-239">Valid</span><span class="sxs-lookup"><span data-stu-id="d92df-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="d92df-240">Waktu dan ongkos pada proyek P1 disertakan pada QL1.</span><span class="sxs-lookup"><span data-stu-id="d92df-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d92df-241">pengeluaran pada proyek P1 disertakan pada QL2.</span><span class="sxs-lookup"><span data-stu-id="d92df-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d92df-242">Tidak ada tumpang tindih dalam apa yang sedang dimasukkan pada setiap baris kuotasi dan valid.</span><span class="sxs-lookup"><span data-stu-id="d92df-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-243">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-244">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-245">QL2</span><span class="sxs-lookup"><span data-stu-id="d92df-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-246">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-247">Kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-248">No</span><span class="sxs-lookup"><span data-stu-id="d92df-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-249">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-250">No</span><span class="sxs-lookup"><span data-stu-id="d92df-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-251">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-252">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-254">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-255">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="d92df-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-256">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-257">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-258">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-259">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="d92df-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-260">Pelanggaran aturan #2 di atas</span><span class="sxs-lookup"><span data-stu-id="d92df-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="d92df-261">Q1 mencakup waktu, pengeluaran, dan ongkos pada subset tugas pada proyek P1.</span><span class="sxs-lookup"><span data-stu-id="d92df-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d92df-262">QL2 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1 dan tumpang tindih dengan yang disertakan pada Q1.</span><span class="sxs-lookup"><span data-stu-id="d92df-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-263">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-264">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-265">QL2</span><span class="sxs-lookup"><span data-stu-id="d92df-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-266">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-267">Kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-268">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-269">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-270">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-271">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-272">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-273">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-274">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-275">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="d92df-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-276">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-277">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-278">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-279">Valid</span><span class="sxs-lookup"><span data-stu-id="d92df-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-280">Per aturan #3 di atas,</span><span class="sxs-lookup"><span data-stu-id="d92df-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="d92df-281">Q1 mencakup waktu, pengeluaran, dan ongkos pada subset tugas pada proyek P1.</span><span class="sxs-lookup"><span data-stu-id="d92df-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d92df-282">QL2 mencakup waktu, pengeluaran, dan ongkos untuk subset tugas pada proyek P1.</span><span class="sxs-lookup"><span data-stu-id="d92df-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d92df-283">Satu-satunya validasi tambahan adalah sekitar subset tugas pada QL1 yang berbeda dari subset tugas pada QL2.</span><span class="sxs-lookup"><span data-stu-id="d92df-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="d92df-284">Hal ini memastikan tidak ada tumpang tindih.</span><span class="sxs-lookup"><span data-stu-id="d92df-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="d92df-285">Hal ini dilakukan oleh sistem saat tugas terkait.</span><span class="sxs-lookup"><span data-stu-id="d92df-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-286">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-287">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-288">QL2</span><span class="sxs-lookup"><span data-stu-id="d92df-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-289">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-290">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="d92df-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-291">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-292">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-293">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-294">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-295">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-296">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-297">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-298">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-299">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-300">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-301">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d92df-302">Valid</span><span class="sxs-lookup"><span data-stu-id="d92df-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-303">Berdasarkan aturan #5, Q1 dan Q2 adalah dua kuotasi pada peluang yang sama, sehingga mereka dapat memperkirakan komponen yang sama dari suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="d92df-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-304">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-305">K2</span><span class="sxs-lookup"><span data-stu-id="d92df-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-306">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-307">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-308">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-309">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-310">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-311">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-312">O1</span><span class="sxs-lookup"><span data-stu-id="d92df-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-313">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-314">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-315">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-316">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-317">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-318">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-319">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d92df-320">Valid</span><span class="sxs-lookup"><span data-stu-id="d92df-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d92df-321">Berdasarkan aturan #4, Q1 dan Q2 adalah dua kuotasi pada peluang yang berbeda, sehingga mereka tidak dapat memperkirakan komponen yang sama dari suatu proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="d92df-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d92df-322">O2</span><span class="sxs-lookup"><span data-stu-id="d92df-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d92df-323">K1</span><span class="sxs-lookup"><span data-stu-id="d92df-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-324">QL1</span><span class="sxs-lookup"><span data-stu-id="d92df-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-325">P1</span><span class="sxs-lookup"><span data-stu-id="d92df-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d92df-326">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="d92df-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-327">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d92df-328">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d92df-329">Ya</span><span class="sxs-lookup"><span data-stu-id="d92df-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d92df-330">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="d92df-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


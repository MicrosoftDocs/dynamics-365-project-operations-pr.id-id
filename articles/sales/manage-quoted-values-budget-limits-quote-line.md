---
title: Sekilas baris kuotasi proyek
description: Halaman topik ini menyediakan informasi tentang menggunakan baris kuotasi proyek untuk pekerjaan proyek.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c585bbc55119e678a4f75f5dfe8966a436db1a34
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368075"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="c0262-103">Sekilas baris kuotasi proyek</span><span class="sxs-lookup"><span data-stu-id="c0262-103">Project quote lines overview</span></span>

<span data-ttu-id="c0262-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="c0262-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="c0262-105">Baris kuotasi berbasis proyek dirancang untuk membantu memperkirakan pekerjaan proyek pada keterlibatan.</span><span class="sxs-lookup"><span data-stu-id="c0262-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="c0262-106">Struktur baris kuotasi berbasis proyek diperluas untuk perkiraan proyek dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="c0262-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="c0262-107">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="c0262-107">Billing Method</span></span>
- <span data-ttu-id="c0262-108">Pemetaan proyek</span><span class="sxs-lookup"><span data-stu-id="c0262-108">Project Mapping</span></span>
- <span data-ttu-id="c0262-109">Termasuk kelas transaksi</span><span class="sxs-lookup"><span data-stu-id="c0262-109">Included Transaction classes</span></span>
- <span data-ttu-id="c0262-110">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="c0262-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="c0262-111">Konfigurasi ketertagihan</span><span class="sxs-lookup"><span data-stu-id="c0262-111">Chargeability setup</span></span>
- <span data-ttu-id="c0262-112">Estimasi menggunakan rincian baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="c0262-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="c0262-113">Pelanggan Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="c0262-113">Quote line Customers</span></span>

<span data-ttu-id="c0262-114">Tabel berikut menyediakan informasi tentang bidang pada tab **Umum** baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="c0262-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="c0262-115">Bidang ini membantu membuat dasar untuk estimasi yang rinci dan komprehensif untuk pekerjaan proyek.</span><span class="sxs-lookup"><span data-stu-id="c0262-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="c0262-116">**Bidang**</span><span class="sxs-lookup"><span data-stu-id="c0262-116">**Field**</span></span> | <span data-ttu-id="c0262-117">**Keterangan**</span><span class="sxs-lookup"><span data-stu-id="c0262-117">**Description**</span></span> | <span data-ttu-id="c0262-118">**Dampak hilir**</span><span class="sxs-lookup"><span data-stu-id="c0262-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c0262-119">Nama</span><span class="sxs-lookup"><span data-stu-id="c0262-119">Name</span></span> | <span data-ttu-id="c0262-120">Nama baris kuotasi yang seharusnya membantu Anda mengidentifikasi komponen diskrit dari kuotasi yang sedang diperkirakan.</span><span class="sxs-lookup"><span data-stu-id="c0262-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="c0262-121">Disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-122">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="c0262-122">Billing Method</span></span> | <span data-ttu-id="c0262-123">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang yang sesuai pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="c0262-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="c0262-124">Bidang ini mencakup dua model kontrak utama yang didukung oleh Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="c0262-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="c0262-125">- Harga tetap</span><span class="sxs-lookup"><span data-stu-id="c0262-125">- Fixed price</span></span></br><span data-ttu-id="c0262-126">- Waktu dan bahan.</span><span class="sxs-lookup"><span data-stu-id="c0262-126">- Time and material.</span></span>| <span data-ttu-id="c0262-127">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-128">Project</span><span class="sxs-lookup"><span data-stu-id="c0262-128">Project</span></span> | <span data-ttu-id="c0262-129">Gunakan bidang opsional ini untuk mengidentifikasi proyek yang akan digunakan untuk melakukan pekerjaan pada keterlibatan ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="c0262-130">Saat dipetakan ke baris kuotasi, proyek akan membantu dengan pengaturan tugas yang dapat dibebankan dan juga dengan mendatangkan estimasi berbasis proyek ke baris kuotasi sebagai rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="c0262-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="c0262-131">Ketika proyek tidak dipetakan ke baris kuotasi berbasis proyek, perkiraan harus dibuat secara manual dengan membuat detail setiap baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="c0262-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="c0262-132">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-133">Sertakan Waktu</span><span class="sxs-lookup"><span data-stu-id="c0262-133">Include Time</span></span> | <span data-ttu-id="c0262-134">Peringatan **ya**/**tidak** menunjukkan jika transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0262-135">Nilai **tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0262-136">Nilai **Ya** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c0262-137">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-138">Sertakan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="c0262-138">Include Expense</span></span> | <span data-ttu-id="c0262-139">Peringatan **ya**/**tidak** menunjukkan jika biaya pengeluaran pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0262-140">Nilai **tidak** menunjukkan bahwa biaya pengeluaran tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0262-141">Nilai **tidak** menunjukkan bahwa biaya pengeluaran akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c0262-142">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-143">Sertakan Tarif</span><span class="sxs-lookup"><span data-stu-id="c0262-143">Include Fee</span></span> | <span data-ttu-id="c0262-144">Peringatan **ya**/**tidak** menunjukkan jika ongkos pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0262-145">Nilai **tidak** menunjukkan bahwa ongkos tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="c0262-146">Nilai **tidak** menunjukkan bahwa ongkos akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="c0262-147">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-148">Jumlah Kuotasi</span><span class="sxs-lookup"><span data-stu-id="c0262-148">Quoted Amount</span></span> | <span data-ttu-id="c0262-149">Ini adalah jumlah yang akan ditawarkan untuk pelanggan untuk semua pekerjaan yang diperkirakan pada baris kuotasi berbasis proyek ini.</span><span class="sxs-lookup"><span data-stu-id="c0262-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="c0262-150">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang **Anggaran Pelanggan** pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="c0262-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="c0262-151">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="c0262-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="c0262-152">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-153">Perkiraan Pajak</span><span class="sxs-lookup"><span data-stu-id="c0262-153">Estimated Tax</span></span> | <span data-ttu-id="c0262-154">Ini adalah bidang yang dapat diedit bagi pengguna untuk menambahkan estimasi jumlah pajak pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="c0262-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="c0262-155">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="c0262-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="c0262-156">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-157">Jumlah Kuotasi Setelah Pajak</span><span class="sxs-lookup"><span data-stu-id="c0262-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="c0262-158">Bidang ini adalah jumlah baris kuotasi setelah pajak dan bersifat hanya baca.</span><span class="sxs-lookup"><span data-stu-id="c0262-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="c0262-159">Jumlah dalam bidang ini dihitung sebagai *jumlah yang ditawarkan + pajak*.</span><span class="sxs-lookup"><span data-stu-id="c0262-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="c0262-160">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-161">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="c0262-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="c0262-162">Bidang ini dapat diedit dan hanya tersedia pada baris kuotasi berbasis proyek yang memiliki metode penagihan **waktu dan bahan**.</span><span class="sxs-lookup"><span data-stu-id="c0262-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="c0262-163">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="c0262-164">Anggaran Pelanggan</span><span class="sxs-lookup"><span data-stu-id="c0262-164">Customer Budget</span></span> | <span data-ttu-id="c0262-165">Bidang ini dapat diedit dan disalin dari bidang yang sesuai pada baris peluang jika kuotasi dibuat dari peluang.</span><span class="sxs-lookup"><span data-stu-id="c0262-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="c0262-166">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="c0262-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="c0262-167">Aturan validasi untuk bidang pada tab Umum baris kuotasi berdasarkan proyek</span><span class="sxs-lookup"><span data-stu-id="c0262-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="c0262-168">**Aturan 1**: kelas transaksi tertentu pada proyek yang dipilih hanya dapat disertakan pada satu baris kuotasi berbasis proyek dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="c0262-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="c0262-169">**Aturan 2**: jika peluang memiliki beberapa kuotasi, ada baris kuotasi dari kuotasi berbeda yang semua mereferensi proyek yang sama dan mencakup kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="c0262-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="c0262-170">**Aturan 3**: jika kuotasi bukan milik peluang yang sama, mereka tidak dapat menyertakan kelas proyek dan transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="c0262-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="c0262-171">
                    <strong>Peluang</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="c0262-172">
                    <strong>Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c0262-173">
                    <strong>Baris Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c0262-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c0262-175">
                    <strong>Sertakan Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="c0262-176">
                    <strong>Sertakan Pengeluaran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="c0262-177">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="c0262-178">
                    <strong>Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="c0262-179">
                    <strong>Valid/tidak valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="c0262-180">
                    <strong>Alasan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="c0262-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0262-181">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-182">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-183">QL1</span><span class="sxs-lookup"><span data-stu-id="c0262-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-184">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-185">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-186">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-187">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-188">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="c0262-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-189">Pelanggaran aturan #1.</span><span class="sxs-lookup"><span data-stu-id="c0262-189">Violation of Rule #1.</span></span> <span data-ttu-id="c0262-190">Waktu, pengeluaran, dan biaya pada proyek P1 disertakan pada baris kuotasi, QL1, dan QL2.</span><span class="sxs-lookup"><span data-stu-id="c0262-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0262-191">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-192">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-193">QL2</span><span class="sxs-lookup"><span data-stu-id="c0262-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-194">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-195">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-196">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-197">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-197">Yes</span></span> </p>
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
<span data-ttu-id="c0262-198">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-199">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-200">QL1</span><span class="sxs-lookup"><span data-stu-id="c0262-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-201">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-202">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-203">No</span><span class="sxs-lookup"><span data-stu-id="c0262-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-204">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-205">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="c0262-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-206">Pelanggaran aturan #1.</span><span class="sxs-lookup"><span data-stu-id="c0262-206">Violation of Rule #1.</span></span> <span data-ttu-id="c0262-207">Waktu dan ongkos pada proyek P1 disertakan pada baris kuotasi, QL1, dan QL2.</span><span class="sxs-lookup"><span data-stu-id="c0262-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0262-208">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-209">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-210">QL2</span><span class="sxs-lookup"><span data-stu-id="c0262-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-211">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-212">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-213">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-214">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-214">Yes</span></span> </p>
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
<span data-ttu-id="c0262-215">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-216">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-217">QL1</span><span class="sxs-lookup"><span data-stu-id="c0262-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-218">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-219">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-220">No</span><span class="sxs-lookup"><span data-stu-id="c0262-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-221">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-222">Valid</span><span class="sxs-lookup"><span data-stu-id="c0262-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="c0262-223">Waktu dan ongkos pada proyek P1 disertakan pada QL1.</span><span class="sxs-lookup"><span data-stu-id="c0262-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="c0262-224">pengeluaran pada proyek P1 disertakan pada QL2.</span><span class="sxs-lookup"><span data-stu-id="c0262-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="c0262-225">Tidak ada tumpang tindih dalam apa yang sedang dimasukkan pada setiap baris kuotasi sehingga ini valid.</span><span class="sxs-lookup"><span data-stu-id="c0262-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0262-226">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-227">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-228">QL2</span><span class="sxs-lookup"><span data-stu-id="c0262-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-229">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-230">No</span><span class="sxs-lookup"><span data-stu-id="c0262-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-231">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-232">No</span><span class="sxs-lookup"><span data-stu-id="c0262-232">No</span></span> </p>
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
<span data-ttu-id="c0262-233">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-234">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-235">QL1</span><span class="sxs-lookup"><span data-stu-id="c0262-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-236">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-237">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-238">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-239">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-240">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="c0262-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-241">Pelanggaran aturan #1 di atas</span><span class="sxs-lookup"><span data-stu-id="c0262-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="c0262-242">Q1 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1.</span><span class="sxs-lookup"><span data-stu-id="c0262-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="c0262-243">QL2 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1 dan tumpang tindih dengan yang disertakan pada Q1.</span><span class="sxs-lookup"><span data-stu-id="c0262-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0262-244">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-245">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-246">QL2</span><span class="sxs-lookup"><span data-stu-id="c0262-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-247">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-248">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-249">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-250">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-250">Yes</span></span> </p>
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
<span data-ttu-id="c0262-251">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-252">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-253">QL1</span><span class="sxs-lookup"><span data-stu-id="c0262-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-254">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-255">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-256">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-257">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c0262-258">Valid</span><span class="sxs-lookup"><span data-stu-id="c0262-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-259">Berdasarkan aturan #2, Q1 dan Q2 adalah dua kuotasi pada peluang yang sama, sehingga mereka dapat memperkirakan komponen yang sama dari suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="c0262-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0262-260">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-261">K2</span><span class="sxs-lookup"><span data-stu-id="c0262-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-262">QL1 pada Q2</span><span class="sxs-lookup"><span data-stu-id="c0262-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-263">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-264">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-265">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-266">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-266">Yes</span></span> </p>
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
<span data-ttu-id="c0262-267">O1</span><span class="sxs-lookup"><span data-stu-id="c0262-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-268">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-269">QL1</span><span class="sxs-lookup"><span data-stu-id="c0262-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-270">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-271">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-272">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-273">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c0262-274">Valid</span><span class="sxs-lookup"><span data-stu-id="c0262-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="c0262-275">Berdasarkan aturan #3, Q1 dan Q2 adalah dua kuotasi pada peluang yang berbeda, sehingga mereka tidak dapat memperkirakan komponen yang sama dari suatu proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="c0262-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="c0262-276">O2</span><span class="sxs-lookup"><span data-stu-id="c0262-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="c0262-277">K1</span><span class="sxs-lookup"><span data-stu-id="c0262-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-278">QL1</span><span class="sxs-lookup"><span data-stu-id="c0262-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-279">P1</span><span class="sxs-lookup"><span data-stu-id="c0262-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-280">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="c0262-281">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="c0262-282">Ya</span><span class="sxs-lookup"><span data-stu-id="c0262-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="c0262-283">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="c0262-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]

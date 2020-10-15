---
title: Baris kuotasi berbasis proyek
description: Topik ini memberikan informasi tentang menggunakan baris kuotasi berbasis proyek untuk pekerjaan proyek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906211"
---
# <a name="project-based-quote-lines"></a><span data-ttu-id="57308-103">Baris kuotasi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="57308-103">Project-based quote lines</span></span>

<span data-ttu-id="57308-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="57308-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="57308-105">Baris kuotasi berbasis proyek dirancang untuk membantu memperkirakan pekerjaan proyek pada keterlibatan.</span><span class="sxs-lookup"><span data-stu-id="57308-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="57308-106">Struktur baris kuotasi berbasis proyek diperluas untuk perkiraan proyek dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="57308-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="57308-107">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="57308-107">Billing Method</span></span>
- <span data-ttu-id="57308-108">Pemetaan proyek</span><span class="sxs-lookup"><span data-stu-id="57308-108">Project Mapping</span></span>
- <span data-ttu-id="57308-109">Termasuk kelas transaksi</span><span class="sxs-lookup"><span data-stu-id="57308-109">Included Transaction classes</span></span>
- <span data-ttu-id="57308-110">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="57308-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="57308-111">Konfigurasi ketertagihan</span><span class="sxs-lookup"><span data-stu-id="57308-111">Chargeability setup</span></span>
- <span data-ttu-id="57308-112">Estimasi menggunakan rincian baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="57308-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="57308-113">Pelanggan Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="57308-113">Quote line Customers</span></span>

<span data-ttu-id="57308-114">Tabel berikut menyediakan informasi tentang bidang pada tab **Umum** baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="57308-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="57308-115">Bidang ini membantu membuat dasar untuk estimasi yang rinci dan komprehensif untuk pekerjaan proyek.</span><span class="sxs-lookup"><span data-stu-id="57308-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="57308-116">**Bidang**</span><span class="sxs-lookup"><span data-stu-id="57308-116">**Field**</span></span> | <span data-ttu-id="57308-117">**Relevansi, tujuan, dan panduan**</span><span class="sxs-lookup"><span data-stu-id="57308-117">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="57308-118">**Dampak hilir**</span><span class="sxs-lookup"><span data-stu-id="57308-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="57308-119">Nama</span><span class="sxs-lookup"><span data-stu-id="57308-119">Name</span></span> | <span data-ttu-id="57308-120">Nama baris kuotasi yang seharusnya membantu Anda mengidentifikasi komponen diskrit dari kuotasi yang sedang diperkirakan.</span><span class="sxs-lookup"><span data-stu-id="57308-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="57308-121">Disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-122">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="57308-122">Billing Method</span></span> | <span data-ttu-id="57308-123">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang yang sesuai pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="57308-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="57308-124">Bidang ini mencakup dua model kontrak utama yang didukung oleh Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="57308-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="57308-125">- Harga tetap</span><span class="sxs-lookup"><span data-stu-id="57308-125">- Fixed price</span></span></br><span data-ttu-id="57308-126">- Waktu dan bahan.</span><span class="sxs-lookup"><span data-stu-id="57308-126">- Time and material.</span></span>| <span data-ttu-id="57308-127">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-128">Project</span><span class="sxs-lookup"><span data-stu-id="57308-128">Project</span></span> | <span data-ttu-id="57308-129">Gunakan bidang opsional ini untuk mengidentifikasi proyek yang akan digunakan untuk melakukan pekerjaan pada keterlibatan ini.</span><span class="sxs-lookup"><span data-stu-id="57308-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="57308-130">Saat dipetakan ke baris kuotasi, proyek akan membantu dengan pengaturan tugas yang dapat dibebankan dan juga dengan mendatangkan estimasi berbasis proyek ke baris kuotasi sebagai rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="57308-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="57308-131">Ketika proyek tidak dipetakan ke baris kuotasi berbasis proyek, perkiraan harus dibuat secara manual dengan membuat detail setiap baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="57308-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="57308-132">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-133">Sertakan Waktu</span><span class="sxs-lookup"><span data-stu-id="57308-133">Include Time</span></span> | <span data-ttu-id="57308-134">Peringatan **ya**/**tidak** menunjukkan jika transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="57308-135">Nilai **tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="57308-136">Nilai **Ya** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="57308-137">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-138">Sertakan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="57308-138">Include Expense</span></span> | <span data-ttu-id="57308-139">Peringatan **ya**/**tidak** menunjukkan jika biaya pengeluaran pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="57308-140">Nilai **tidak** menunjukkan bahwa biaya pengeluaran tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="57308-141">Nilai **tidak** menunjukkan bahwa biaya pengeluaran akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="57308-142">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-143">Sertakan Tarif</span><span class="sxs-lookup"><span data-stu-id="57308-143">Include Fee</span></span> | <span data-ttu-id="57308-144">Peringatan **ya**/**tidak** menunjukkan jika ongkos pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="57308-145">Nilai **tidak** menunjukkan bahwa ongkos tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="57308-146">Nilai **tidak** menunjukkan bahwa ongkos akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="57308-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="57308-147">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-148">Jumlah Kuotasi</span><span class="sxs-lookup"><span data-stu-id="57308-148">Quoted Amount</span></span> | <span data-ttu-id="57308-149">Ini adalah jumlah yang akan ditawarkan untuk pelanggan untuk semua pekerjaan yang diperkirakan pada baris kuotasi berbasis proyek ini.</span><span class="sxs-lookup"><span data-stu-id="57308-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="57308-150">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang **Anggaran Pelanggan** pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="57308-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="57308-151">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="57308-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="57308-152">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-153">Perkiraan Pajak</span><span class="sxs-lookup"><span data-stu-id="57308-153">Estimated Tax</span></span> | <span data-ttu-id="57308-154">Ini adalah bidang yang dapat diedit bagi pengguna untuk menambahkan estimasi jumlah pajak pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="57308-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="57308-155">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="57308-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="57308-156">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-157">Jumlah Kuotasi Setelah Pajak</span><span class="sxs-lookup"><span data-stu-id="57308-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="57308-158">Bidang ini adalah jumlah baris kuotasi setelah pajak dan bersifat hanya baca.</span><span class="sxs-lookup"><span data-stu-id="57308-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="57308-159">Jumlah dalam bidang ini dihitung sebagai *jumlah yang ditawarkan + pajak*.</span><span class="sxs-lookup"><span data-stu-id="57308-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="57308-160">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-161">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="57308-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="57308-162">Bidang ini dapat diedit dan hanya tersedia pada baris kuotasi berbasis proyek yang memiliki metode penagihan **waktu dan bahan**.</span><span class="sxs-lookup"><span data-stu-id="57308-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="57308-163">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="57308-164">Anggaran Pelanggan</span><span class="sxs-lookup"><span data-stu-id="57308-164">Customer Budget</span></span> | <span data-ttu-id="57308-165">Bidang ini dapat diedit dan disalin dari bidang yang sesuai pada baris peluang jika kuotasi dibuat dari peluang.</span><span class="sxs-lookup"><span data-stu-id="57308-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="57308-166">Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="57308-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="57308-167">Aturan validasi untuk bidang pada tab Umum baris kuotasi berdasarkan proyek</span><span class="sxs-lookup"><span data-stu-id="57308-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="57308-168">**Aturan 1**: kelas transaksi tertentu pada proyek yang dipilih hanya dapat disertakan pada satu baris kuotasi berbasis proyek dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="57308-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="57308-169">**Aturan 2**: jika peluang memiliki beberapa kuotasi, ada baris kuotasi dari kuotasi berbeda yang semua mereferensi proyek yang sama dan mencakup kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="57308-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="57308-170">**Aturan 3**: jika kuotasi bukan milik peluang yang sama, mereka tidak dapat menyertakan kelas proyek dan transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="57308-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="57308-171">
                    <strong>Peluang</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="57308-172">
                    <strong>Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="57308-173">
                    <strong>Baris Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="57308-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="57308-175">
                    <strong>Sertakan Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="57308-176">
                    <strong>Sertakan Pengeluaran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="57308-177">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="57308-178">
                    <strong>Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="57308-179">
                    <strong>Valid/tidak valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="57308-180">
                    <strong>Alasan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="57308-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="57308-181">O1</span><span class="sxs-lookup"><span data-stu-id="57308-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-182">K1</span><span class="sxs-lookup"><span data-stu-id="57308-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-183">QL1</span><span class="sxs-lookup"><span data-stu-id="57308-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-184">P1</span><span class="sxs-lookup"><span data-stu-id="57308-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-185">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-186">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-187">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-188">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="57308-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-189">Pelanggaran aturan #1.</span><span class="sxs-lookup"><span data-stu-id="57308-189">Violation of Rule #1.</span></span> <span data-ttu-id="57308-190">Waktu, pengeluaran, dan biaya pada proyek P1 disertakan pada baris kuotasi, QL1, dan QL2.</span><span class="sxs-lookup"><span data-stu-id="57308-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="57308-191">O1</span><span class="sxs-lookup"><span data-stu-id="57308-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-192">K1</span><span class="sxs-lookup"><span data-stu-id="57308-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-193">QL2</span><span class="sxs-lookup"><span data-stu-id="57308-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-194">P1</span><span class="sxs-lookup"><span data-stu-id="57308-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-195">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-196">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-197">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-197">Yes</span></span> </p>
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
<span data-ttu-id="57308-198">O1</span><span class="sxs-lookup"><span data-stu-id="57308-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-199">K1</span><span class="sxs-lookup"><span data-stu-id="57308-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-200">QL1</span><span class="sxs-lookup"><span data-stu-id="57308-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-201">P1</span><span class="sxs-lookup"><span data-stu-id="57308-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-202">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-203">No</span><span class="sxs-lookup"><span data-stu-id="57308-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-204">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-205">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="57308-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-206">Pelanggaran aturan #1.</span><span class="sxs-lookup"><span data-stu-id="57308-206">Violation of Rule #1.</span></span> <span data-ttu-id="57308-207">Waktu dan ongkos pada proyek P1 disertakan pada baris kuotasi, QL1, dan QL2.</span><span class="sxs-lookup"><span data-stu-id="57308-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="57308-208">O1</span><span class="sxs-lookup"><span data-stu-id="57308-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-209">K1</span><span class="sxs-lookup"><span data-stu-id="57308-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-210">QL2</span><span class="sxs-lookup"><span data-stu-id="57308-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-211">P1</span><span class="sxs-lookup"><span data-stu-id="57308-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-212">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-213">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-214">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-214">Yes</span></span> </p>
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
<span data-ttu-id="57308-215">O1</span><span class="sxs-lookup"><span data-stu-id="57308-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-216">K1</span><span class="sxs-lookup"><span data-stu-id="57308-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-217">QL1</span><span class="sxs-lookup"><span data-stu-id="57308-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-218">P1</span><span class="sxs-lookup"><span data-stu-id="57308-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-219">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-220">No</span><span class="sxs-lookup"><span data-stu-id="57308-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-221">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-222">Valid</span><span class="sxs-lookup"><span data-stu-id="57308-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="57308-223">Waktu dan ongkos pada proyek P1 disertakan pada QL1.</span><span class="sxs-lookup"><span data-stu-id="57308-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="57308-224">pengeluaran pada proyek P1 disertakan pada QL2.</span><span class="sxs-lookup"><span data-stu-id="57308-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="57308-225">Tidak ada tumpang tindih dalam apa yang sedang dimasukkan pada setiap baris kuotasi sehingga ini valid.</span><span class="sxs-lookup"><span data-stu-id="57308-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="57308-226">O1</span><span class="sxs-lookup"><span data-stu-id="57308-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-227">K1</span><span class="sxs-lookup"><span data-stu-id="57308-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-228">QL2</span><span class="sxs-lookup"><span data-stu-id="57308-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-229">P1</span><span class="sxs-lookup"><span data-stu-id="57308-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-230">No</span><span class="sxs-lookup"><span data-stu-id="57308-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-231">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-232">No</span><span class="sxs-lookup"><span data-stu-id="57308-232">No</span></span> </p>
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
<span data-ttu-id="57308-233">O1</span><span class="sxs-lookup"><span data-stu-id="57308-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-234">K1</span><span class="sxs-lookup"><span data-stu-id="57308-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-235">QL1</span><span class="sxs-lookup"><span data-stu-id="57308-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-236">P1</span><span class="sxs-lookup"><span data-stu-id="57308-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-237">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-238">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-239">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-240">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="57308-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-241">Pelanggaran aturan #1 di atas</span><span class="sxs-lookup"><span data-stu-id="57308-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="57308-242">Q1 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1.</span><span class="sxs-lookup"><span data-stu-id="57308-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="57308-243">QL2 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1 dan tumpang tindih dengan yang disertakan pada Q1.</span><span class="sxs-lookup"><span data-stu-id="57308-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="57308-244">O1</span><span class="sxs-lookup"><span data-stu-id="57308-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-245">K1</span><span class="sxs-lookup"><span data-stu-id="57308-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-246">QL2</span><span class="sxs-lookup"><span data-stu-id="57308-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-247">P1</span><span class="sxs-lookup"><span data-stu-id="57308-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-248">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-249">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-250">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-250">Yes</span></span> </p>
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
<span data-ttu-id="57308-251">O1</span><span class="sxs-lookup"><span data-stu-id="57308-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-252">K1</span><span class="sxs-lookup"><span data-stu-id="57308-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-253">QL1</span><span class="sxs-lookup"><span data-stu-id="57308-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-254">P1</span><span class="sxs-lookup"><span data-stu-id="57308-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-255">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-256">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-257">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="57308-258">Valid</span><span class="sxs-lookup"><span data-stu-id="57308-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-259">Berdasarkan aturan #2, Q1 dan Q2 adalah dua kuotasi pada peluang yang sama, sehingga mereka dapat memperkirakan komponen yang sama dari suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="57308-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="57308-260">O1</span><span class="sxs-lookup"><span data-stu-id="57308-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-261">K2</span><span class="sxs-lookup"><span data-stu-id="57308-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-262">QL1 pada Q2</span><span class="sxs-lookup"><span data-stu-id="57308-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-263">P1</span><span class="sxs-lookup"><span data-stu-id="57308-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-264">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-265">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-266">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-266">Yes</span></span> </p>
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
<span data-ttu-id="57308-267">O1</span><span class="sxs-lookup"><span data-stu-id="57308-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-268">K1</span><span class="sxs-lookup"><span data-stu-id="57308-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-269">QL1</span><span class="sxs-lookup"><span data-stu-id="57308-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-270">P1</span><span class="sxs-lookup"><span data-stu-id="57308-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-271">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-272">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-273">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="57308-274">Valid</span><span class="sxs-lookup"><span data-stu-id="57308-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="57308-275">Berdasarkan aturan #3, Q1 dan Q2 adalah dua kuotasi pada peluang yang berbeda, sehingga mereka tidak dapat memperkirakan komponen yang sama dari suatu proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="57308-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="57308-276">O2</span><span class="sxs-lookup"><span data-stu-id="57308-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="57308-277">K1</span><span class="sxs-lookup"><span data-stu-id="57308-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-278">QL1</span><span class="sxs-lookup"><span data-stu-id="57308-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-279">P1</span><span class="sxs-lookup"><span data-stu-id="57308-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-280">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="57308-281">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="57308-282">Ya</span><span class="sxs-lookup"><span data-stu-id="57308-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="57308-283">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="57308-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


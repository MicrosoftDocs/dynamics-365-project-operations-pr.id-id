---
title: Sekilas baris kuotasi berbasis proyek
description: Topik ini memberikan informasi tentang menggunakan baris kuotasi berbasis proyek untuk pekerjaan proyek.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cfe98fc89130c93dd0a36af8583881fdcb4550c0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858702"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="6c4b6-103">Sekilas baris kuotasi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="6c4b6-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="6c4b6-104">_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_</span><span class="sxs-lookup"><span data-stu-id="6c4b6-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6c4b6-105">Baris kuotasi berbasis proyek dirancang untuk membantu memperkirakan pekerjaan proyek pada keterlibatan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="6c4b6-106">Struktur baris kuotasi berbasis proyek diperluas untuk perkiraan proyek dengan konsep berikut:</span><span class="sxs-lookup"><span data-stu-id="6c4b6-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="6c4b6-107">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="6c4b6-107">Billing Method</span></span>
- <span data-ttu-id="6c4b6-108">Pemetaan Proyek dan Tugas</span><span class="sxs-lookup"><span data-stu-id="6c4b6-108">Project and Task Mapping</span></span>
- <span data-ttu-id="6c4b6-109">Termasuk kelas transaksi</span><span class="sxs-lookup"><span data-stu-id="6c4b6-109">Included Transaction classes</span></span>
- <span data-ttu-id="6c4b6-110">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="6c4b6-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="6c4b6-111">Konfigurasi ketertagihan</span><span class="sxs-lookup"><span data-stu-id="6c4b6-111">Chargeability setup</span></span>
- <span data-ttu-id="6c4b6-112">Estimasi menggunakan rincian baris kuotasi</span><span class="sxs-lookup"><span data-stu-id="6c4b6-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="6c4b6-113">Pelanggan Baris Kuotasi</span><span class="sxs-lookup"><span data-stu-id="6c4b6-113">Quote line Customers</span></span>

<span data-ttu-id="6c4b6-114">Tabel berikut menyediakan informasi tentang bidang pada tab **Umum** baris kuotasi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="6c4b6-115">Bidang ini membantu membuat dasar untuk estimasi yang rinci dan komprehensif untuk pekerjaan proyek.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="6c4b6-116">**Bidang**</span><span class="sxs-lookup"><span data-stu-id="6c4b6-116">**Field**</span></span> | <span data-ttu-id="6c4b6-117">**Deskripsi**</span><span class="sxs-lookup"><span data-stu-id="6c4b6-117">**Description**</span></span> | <span data-ttu-id="6c4b6-118">**Dampak hilir**</span><span class="sxs-lookup"><span data-stu-id="6c4b6-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6c4b6-119">Nama</span><span class="sxs-lookup"><span data-stu-id="6c4b6-119">Name</span></span> | <span data-ttu-id="6c4b6-120">Nama baris kuotasi yang membantu Anda mengidentifikasi komponen terpisah dari kuotasi yang sedang diestimasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="6c4b6-121">Disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-122">Metode Penagihan</span><span class="sxs-lookup"><span data-stu-id="6c4b6-122">Billing Method</span></span> | <span data-ttu-id="6c4b6-123">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang yang sesuai pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="6c4b6-124">Bidang ini mencakup dua model kontrak utama yang didukung oleh Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="6c4b6-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="6c4b6-125">- Harga tetap</span><span class="sxs-lookup"><span data-stu-id="6c4b6-125">- Fixed price</span></span></br><span data-ttu-id="6c4b6-126">- Waktu dan bahan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-126">- Time and material.</span></span>| <span data-ttu-id="6c4b6-127">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-128">Project</span><span class="sxs-lookup"><span data-stu-id="6c4b6-128">Project</span></span> | <span data-ttu-id="6c4b6-129">Gunakan bidang opsional ini untuk mengidentifikasi proyek yang akan digunakan untuk melakukan pekerjaan pada keterlibatan ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="6c4b6-130">Saat dipetakan ke baris kuotasi, proyek akan membantu dengan pengaturan tugas yang dapat dibebankan dan juga dengan mendatangkan estimasi berbasis proyek ke baris kuotasi sebagai rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="6c4b6-131">Ketika proyek tidak dipetakan ke baris kuotasi berbasis proyek, perkiraan harus dibuat secara manual dengan membuat detail setiap baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="6c4b6-132">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="6c4b6-133">Tugas Disertakan</span><span class="sxs-lookup"><span data-stu-id="6c4b6-133">Included Tasks</span></span> | <span data-ttu-id="6c4b6-134">Menunjukkan jika baris kuotasi ini digunakan untuk semua atau sebagian tugas proyek untuk proyek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="6c4b6-135">Bidang ini memiliki kemungkinan nilai berikut:</span><span class="sxs-lookup"><span data-stu-id="6c4b6-135">This field has the following possible values:</span></span></br><span data-ttu-id="6c4b6-136">- Semua tugas proyek</span><span class="sxs-lookup"><span data-stu-id="6c4b6-136">- All project tasks</span></span></br><span data-ttu-id="6c4b6-137">- Hanya tugas proyek yang dipilih</span><span class="sxs-lookup"><span data-stu-id="6c4b6-137">- Selected project tasks only</span></span></br><span data-ttu-id="6c4b6-138">Nilai kosong di bidang ini setara dengan pilihan **semua tugas proyek**.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="6c4b6-139">Bila **Tugas proyek yang Dipilih saja** dipilih pada halaman proyek, tab **Konfigurasi penagihan Tugas** memungkinkan Anda memilih tugas tertentu untuk mengaitkannya ke baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="6c4b6-140">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-141">Sertakan Waktu</span><span class="sxs-lookup"><span data-stu-id="6c4b6-141">Include Time</span></span> | <span data-ttu-id="6c4b6-142">Nilai **Ya**/**Tidak** menunjukkan apakah transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-143">Nilai **tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-144">Nilai **Ya** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6c4b6-145">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-146">Sertakan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="6c4b6-146">Include Expense</span></span> | <span data-ttu-id="6c4b6-147">Nilai **Ya**/**Tidak** menunjukkan apakah biaya pengeluaran pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-148">Nilai **tidak** menunjukkan bahwa biaya pengeluaran tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-149">Nilai **tidak** menunjukkan bahwa biaya pengeluaran akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6c4b6-150">Nilai ini disalin pada baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-151">Termasuk Materi</span><span class="sxs-lookup"><span data-stu-id="6c4b6-151">Include Material</span></span> | <span data-ttu-id="6c4b6-152">Nilai **Ya**/**Tidak** menunjukkan apakah biaya bahan pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-153">Nilai **Tidak** menunjukkan bahwa biaya bahan tidak akan disertakan dalam estimasi di baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-154">Nilai **Ya** menunjukkan bahwa biaya bahan akan disertakan dalam estimasi di baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6c4b6-155">Nilai ini disalin pada baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-156">Sertakan Tarif</span><span class="sxs-lookup"><span data-stu-id="6c4b6-156">Include Fee</span></span> | <span data-ttu-id="6c4b6-157">Nilai **Ya**/**Tidak** menunjukkan apakah ongkos pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-158">Nilai **tidak** menunjukkan bahwa ongkos tidak akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="6c4b6-159">Nilai **tidak** menunjukkan bahwa ongkos akan dimasukkan dalam perkiraan baris kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="6c4b6-160">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-161">Jumlah Kuotasi</span><span class="sxs-lookup"><span data-stu-id="6c4b6-161">Quoted Amount</span></span> | <span data-ttu-id="6c4b6-162">Ini adalah jumlah yang akan diberikan kuotasinya kepada pelanggan untuk semua pekerjaan yang diramalkan pada baris kuotasi berbasis proyek ini.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="6c4b6-163">Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang **Anggaran Pelanggan** pada baris peluang.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="6c4b6-164">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="6c4b6-165">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-166">Perkiraan Pajak</span><span class="sxs-lookup"><span data-stu-id="6c4b6-166">Estimated Tax</span></span> | <span data-ttu-id="6c4b6-167">Ini adalah bidang yang dapat diedit bagi pengguna untuk menambahkan estimasi jumlah pajak pada baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="6c4b6-168">Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="6c4b6-169">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-170">Jumlah Kuotasi Setelah Pajak</span><span class="sxs-lookup"><span data-stu-id="6c4b6-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="6c4b6-171">Bidang ini adalah jumlah baris kuotasi setelah pajak dan bersifat hanya baca.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="6c4b6-172">Jumlah dalam bidang ini dihitung sebagai *jumlah yang ditawarkan + pajak*.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="6c4b6-173">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-174">Batas Jangan terlampaui</span><span class="sxs-lookup"><span data-stu-id="6c4b6-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="6c4b6-175">Bidang ini dapat diedit dan hanya tersedia pada baris kuotasi berbasis proyek yang memiliki metode penagihan **waktu dan bahan**.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="6c4b6-176">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="6c4b6-177">Anggaran Pelanggan</span><span class="sxs-lookup"><span data-stu-id="6c4b6-177">Customer Budget</span></span> | <span data-ttu-id="6c4b6-178">Bidang ini dapat diedit dan disalin dari bidang yang sesuai pada baris peluang jika kuotasi dibuat dari peluang.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="6c4b6-179">Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="6c4b6-180">Aturan validasi untuk bidang pada tab Umum baris kuotasi berdasarkan proyek</span><span class="sxs-lookup"><span data-stu-id="6c4b6-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="6c4b6-181">**Aturan 1**: jika bidang **tugas yang disertakan** kosong, atau jika diatur ke **semua tugas proyek**, proyek disertakan dalam baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="6c4b6-182">**Aturan 2**: jika bidang **tugas yang disertakan** kosong, atau jika diatur ke **semua tugas proyek**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada satu baris kuotasi berbasis proyek dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="6c4b6-183">**Aturan 3**: jika bidang **tugas yang disertakan** diatur ke **Hanya tugas proyek yang dipilih**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada beberapa baris kuotasi berbasis proyek dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="6c4b6-184">**Aturan 4**: jika peluang memiliki beberapa kuotasi, ada baris kuotasi dari kuotasi berbeda yang semua mereferensi proyek yang sama dan mencakup kelas transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="6c4b6-185">**Aturan 5**: jika kuotasi bukan milik peluang yang sama, mereka tidak dapat menyertakan kelas proyek dan transaksi yang sama.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="6c4b6-186">
                    <strong>Peluang</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="6c4b6-187">
                    <strong>Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="6c4b6-188">
                    <strong>Baris Kuotasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6c4b6-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="6c4b6-190">
                    <strong>Tugas yang Disertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="6c4b6-191">
                    <strong>Sertakan Waktu</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="6c4b6-192">
                    <strong>Sertakan Pengeluaran</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="6c4b6-193">
                    <strong>Termasuk Materi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="6c4b6-194">
                    <strong>Sertakan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="6c4b6-195">
                    <strong>Biaya</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="6c4b6-196">
                    <strong>Valid/tidak valid</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="6c4b6-197">
                    <strong>Alasan</strong>
                </span><span class="sxs-lookup"><span data-stu-id="6c4b6-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-198">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-199">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-200">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-201">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-202">Kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-203">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-204">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-205">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-206">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-207">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="6c4b6-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-208">Pelanggaran aturan #2.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-208">Violation of Rule #2.</span></span> <span data-ttu-id="6c4b6-209">Waktu, pengeluaran, dan Ongkos pada proyek P1 disertakan pada baris kuotasi QL1 dan QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-210">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-211">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-212">QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-213">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-214">Kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-215">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-216">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-217">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-218">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-219">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-220">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-221">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-222">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-223">Kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-224">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-225">No</span><span class="sxs-lookup"><span data-stu-id="6c4b6-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-226">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-227">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-228">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="6c4b6-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-229">Pelanggaran aturan #2.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-229">Violation of Rule #2.</span></span> <span data-ttu-id="6c4b6-230">Waktu, Bahan, dan Ongkos pada proyek P1 disertakan pada baris kuotasi QL1 dan QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-231">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-232">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-233">QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-234">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-235">Kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-236">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-237">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-238">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-239">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-240">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-241">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-242">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-243">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-244">Kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-245">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-246">No</span><span class="sxs-lookup"><span data-stu-id="6c4b6-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-247">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-248">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-249">Valid</span><span class="sxs-lookup"><span data-stu-id="6c4b6-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-250">Waktu, Bahan, dan Ongkos pada proyek P1 tercakup di QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="6c4b6-251">pengeluaran pada proyek P1 disertakan pada QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="6c4b6-252">Tidak ada tumpang tindih dalam hal yang tercakup di setiap baris kuotasi dan oleh karena itu valid.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-253">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-254">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-255">QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-256">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-257">Kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-258">No</span><span class="sxs-lookup"><span data-stu-id="6c4b6-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-259">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-260">No</span><span class="sxs-lookup"><span data-stu-id="6c4b6-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-261">No</span><span class="sxs-lookup"><span data-stu-id="6c4b6-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-262">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-263">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-264">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-265">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-266">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="6c4b6-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-267">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-268">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-269">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-270">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-271">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="6c4b6-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-272">Pelanggaran aturan #2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="6c4b6-273">Q1 mencakup Waktu, Bahan, Pengeluaran dan Ongkos pada subset tugas di proyek P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="6c4b6-274">QL2 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1 dan karena itu tumpang tindih dengan yang disertakan di Q1.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-275">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-276">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-277">QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-278">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-279">Kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-280">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-281">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-282">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-283">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-284">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-285">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-286">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-287">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-288">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="6c4b6-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-289">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-290">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-291">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-292">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-293">Valid</span><span class="sxs-lookup"><span data-stu-id="6c4b6-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-294">Per aturan #3,</span><span class="sxs-lookup"><span data-stu-id="6c4b6-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="6c4b6-295">Q1 mencakup Waktu, Bahan, Pengeluaran dan Ongkos pada subset tugas di proyek P1.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6c4b6-296">QL2 mencakup Waktu, Pengeluaran, Bahan, dan Ongkos untuk subset tugas di proyek P1.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="6c4b6-297">Satu-satunya validasi tambahan adalah seputar subset tugas di QL1, yang berbeda dengan subset tugas di QL2 untuk memastikan tidak ada tumpang tindih di sana.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="6c4b6-298">Hal ini dilakukan oleh sistem saat tugas terkait.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-299">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-300">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-301">QL2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-302">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-303">Hanya tugas yang dipilih</span><span class="sxs-lookup"><span data-stu-id="6c4b6-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-304">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-305">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-306">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-307">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-308">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-309">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-310">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-311">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-312">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-313">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-314">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-315">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-316">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-317">Valid</span><span class="sxs-lookup"><span data-stu-id="6c4b6-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-318">Per Aturan #5, Q1 dan Q2 adalah dua kuotasi pada peluang yang sama, sehingga mereka dapat memperkirakan untuk komponen proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-319">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-320">K2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-321">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-322">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-323">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-324">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-325">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-326">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-327">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-328">O1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-329">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-330">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-331">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-332">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-333">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-334">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-335">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-336">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-337">Tidak valid</span><span class="sxs-lookup"><span data-stu-id="6c4b6-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="6c4b6-338">Per Aturan #4, Q1 dan Q2 adalah dua kuotasi pada peluang yang berbeda, sehingga mereka tidak dapat memperkirakan untuk komponen proyek yang sama.</span><span class="sxs-lookup"><span data-stu-id="6c4b6-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="6c4b6-339">O2</span><span class="sxs-lookup"><span data-stu-id="6c4b6-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="6c4b6-340">K1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="6c4b6-341">QL1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-342">P1</span><span class="sxs-lookup"><span data-stu-id="6c4b6-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="6c4b6-343">Semua Tugas Proyek atau kosong</span><span class="sxs-lookup"><span data-stu-id="6c4b6-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="6c4b6-344">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="6c4b6-345">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="6c4b6-346">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="6c4b6-347">Ya</span><span class="sxs-lookup"><span data-stu-id="6c4b6-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

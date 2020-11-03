---
title: Konfigurasi Manajemen Pengeluaran
description: Artikel ini menjelaskan pertimbangan dan keputusan yang harus Anda buat selama proses perencanaan sebelum mengkonfigurasi manajemen pengeluaran di Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078632"
---
# <a name="configure-expense-management"></a><span data-ttu-id="ecc16-103">Konfigurasi Manajemen Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="ecc16-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ecc16-104">Topik ini menjelaskan pertimbangan dan keputusan yang harus Anda buat selama proses perencanaan sebelum mengkonfigurasi manajemen pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="ecc16-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="ecc16-105">Di manajemen pengeluaran, Anda dapat menyimpan informasi tentang metode pembayaran, permintaan perjalanan, laporan pengeluaran, kebijakan, dan sebagainya.</span><span class="sxs-lookup"><span data-stu-id="ecc16-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="ecc16-106">Karena banyak keputusan yang Anda buat saat merencanakan konfigurasi untuk manajemen pengeluaran berdasarkan hierarki dan struktur keuangan organisasi Anda, Anda harus merujuk ke dokumen perencanaan untuk area tersebut.</span><span class="sxs-lookup"><span data-stu-id="ecc16-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="ecc16-107">Pengeluaran antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="ecc16-107">Intercompany expenses</span></span>

<span data-ttu-id="ecc16-108">Bila Anda mengaktifkan biaya antarperusahaan, Anda mengizinkan entitas hukum dan karyawan untuk mengeluarkan biaya atas nama entitas hukum lain, dan menagih pembayaran dari badan hukum kerja dalam organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="ecc16-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="ecc16-109">Contohnya, seorang karyawan di entitas hukum A menyelesaikan proyek untuk badan hukum B, dan proyek ini menimbulkan pengeluaran terkait perjalanan.</span><span class="sxs-lookup"><span data-stu-id="ecc16-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="ecc16-110">Jika pengeluaran antarperusahaan diaktifkan, karyawan kemudian dapat mengajukan laporan pengeluaran yang akan memposting pengeluaran ke badan hukum B, dan pengeluaran kemudian harus dibayar oleh entitas hukum A. Jika organisasi Anda tidak memiliki beberapa entitas hukum, Anda tidak perlu mengaktifkan biaya antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="ecc16-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="ecc16-111">**Keputusan:** Apakah Anda ingin mengaktifkan biaya Antarperusahaan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="ecc16-112">Manajemen keuangan</span><span class="sxs-lookup"><span data-stu-id="ecc16-112">Financial management</span></span>

<span data-ttu-id="ecc16-113">Manajemen pengeluaran terintegrasi erat dengan manajemen keuangan organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="ecc16-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="ecc16-114">Banyak konfigurasi Anda untuk manajemen pengeluaran akan didasarkan pada keputusan yang telah Anda buat tentang keuangan organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="ecc16-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="ecc16-115">Bagian berikut menjelaskan berbagai area yang memerlukan perencanaan dan keputusan, berdasarkan keputusan keuangan organisasi Anda dan bimbingan dari tim kepemimpinan Anda.</span><span class="sxs-lookup"><span data-stu-id="ecc16-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="ecc16-116">Pembayaran harian</span><span class="sxs-lookup"><span data-stu-id="ecc16-116">Per diems</span></span>

<span data-ttu-id="ecc16-117">Anda harus menentukan uang saku karyawan yang disediakan organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="ecc16-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="ecc16-118">Karena setiap uang saku biasanya digunakan untuk mencakup pengeluaran seperti makanan, penginapan, dan biaya insidental lainnya, Anda dapat membuat aturan untuk tunjangan uang saku yang ditawarkan oleh organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="ecc16-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="ecc16-119">Tarif uang saku dapat didasarkan pada waktu, lokasi perjalanan, atau keduanya.</span><span class="sxs-lookup"><span data-stu-id="ecc16-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="ecc16-120">Saat menentukan aturan uang saku, Anda dapat menentukan bahwa persentase tingkat uang saku diabaikan jika pekerja menerima makanan, atau layanan gratis.</span><span class="sxs-lookup"><span data-stu-id="ecc16-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="ecc16-121">Anda juga dapat menetapkan tingkat tarif uang saku untuk mengatur jumlah jam minimum dan maksimum yang dapat diterapkan dalam tarif uang saku untuk perjalanan pekerja.</span><span class="sxs-lookup"><span data-stu-id="ecc16-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="ecc16-122">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="ecc16-122">**Decisions:**</span></span>

- <span data-ttu-id="ecc16-123">Aturan default uang saku untuk hari pertama dan terakhir:</span><span class="sxs-lookup"><span data-stu-id="ecc16-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="ecc16-124">Berapakah jumlah jam minimum yang dapat diklaim karyawan selama satu hari dan tetap menerima uang saku?</span><span class="sxs-lookup"><span data-stu-id="ecc16-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="ecc16-125">Apakah ada pengurangan dalam jumlah yang ditawarkan untuk makanan untuk hari pertama dan hari terakhir?</span><span class="sxs-lookup"><span data-stu-id="ecc16-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="ecc16-126">Jika ada pengurangan, berapa persentase pengurangan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="ecc16-127">Apakah ada pengurangan dalam jumlah yang ditawarkan untuk hotel untuk hari pertama dan hari terakhir?</span><span class="sxs-lookup"><span data-stu-id="ecc16-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="ecc16-128">Jika ada pengurangan, berapa persentase pengurangan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="ecc16-129">Apakah ada pengurangan dalam jumlah yang ditawarkan untuk pengeluaran lain yang ditanggung pada hari pertama dan hari terakhir?</span><span class="sxs-lookup"><span data-stu-id="ecc16-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="ecc16-130">Jika ada pengurangan, berapa persentase pengurangan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="ecc16-131">Default aturan uang saku:</span><span class="sxs-lookup"><span data-stu-id="ecc16-131">Default per diem rules:</span></span>

    - <span data-ttu-id="ecc16-132">Apakah ada pengurangan persentase pada penyisihan uang saku untuk setiap makanan jika, misalnya, makanan gratis?</span><span class="sxs-lookup"><span data-stu-id="ecc16-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="ecc16-133">Jika ada pengurangan, berapa persentase pengurangan untuk setiap makanan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="ecc16-134">Apakah pengurangan makanan dihitung per hari, per perjalanan, atau dengan jumlah makanan per hari?</span><span class="sxs-lookup"><span data-stu-id="ecc16-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="ecc16-135">Haruskah jumlah uang saku dibulatkan dalam cara biasa atau dibulatkan ke atas?</span><span class="sxs-lookup"><span data-stu-id="ecc16-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="ecc16-136">Apakah uang saku dihitung dalam periode 24 jam atau pada hari kalender?</span><span class="sxs-lookup"><span data-stu-id="ecc16-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="ecc16-137">Aturan uang saku yang didasarkan pada lokasi:</span><span class="sxs-lookup"><span data-stu-id="ecc16-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="ecc16-138">Apakah tarif uang saku bervariasi sesuai lokasi?</span><span class="sxs-lookup"><span data-stu-id="ecc16-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="ecc16-139">Lokasi apa yang disertakan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-139">What locations are included?</span></span>
    - <span data-ttu-id="ecc16-140">Jika tarif uang saku bervariasi menurut lokasi, untuk setiap lokasi, berapa jumlah persentase yang diberikan untuk jenis pengeluaran berikut:</span><span class="sxs-lookup"><span data-stu-id="ecc16-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="ecc16-141">Makan</span><span class="sxs-lookup"><span data-stu-id="ecc16-141">Meals</span></span>
        - <span data-ttu-id="ecc16-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="ecc16-142">Hotel</span></span>
        - <span data-ttu-id="ecc16-143">Pengeluaran lain</span><span class="sxs-lookup"><span data-stu-id="ecc16-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="ecc16-144">Jurnal dan akun manajemen pengeluaran</span><span class="sxs-lookup"><span data-stu-id="ecc16-144">Expense management journals and accounts</span></span>

<span data-ttu-id="ecc16-145">Manajemen pengeluaran mengharuskan Anda menggunakan beberapa jurnal dan akun.</span><span class="sxs-lookup"><span data-stu-id="ecc16-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="ecc16-146">Anda harus memutuskan, misalnya, Apakah akun yang sama digunakan untuk uang muka dan perselisihan kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="ecc16-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="ecc16-147">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="ecc16-147">**Decisions:**</span></span>

- <span data-ttu-id="ecc16-148">Jurnal pembukuan manakah yang merupakan laporan pengeluaran disetujui untuk diposting?</span><span class="sxs-lookup"><span data-stu-id="ecc16-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="ecc16-149">Akun yang digunakan untuk kasbon?</span><span class="sxs-lookup"><span data-stu-id="ecc16-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="ecc16-150">Apakah kasbon harus segera diposting?</span><span class="sxs-lookup"><span data-stu-id="ecc16-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="ecc16-151">Metode Pembayaran</span><span class="sxs-lookup"><span data-stu-id="ecc16-151">Payment methods</span></span>

<span data-ttu-id="ecc16-152">Bila Anda mengizinkan karyawan untuk mengeluarkan pengeluaran atas nama bisnis Anda, Anda harus menentukan metode pembayaran yang diizinkan untuk digunakan karyawan.</span><span class="sxs-lookup"><span data-stu-id="ecc16-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="ecc16-153">Misalnya, Anda dapat mengizinkan karyawan menggunakan uang tunai atau kartu kredit perusahaan.</span><span class="sxs-lookup"><span data-stu-id="ecc16-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="ecc16-154">Anda juga dapat mengizinkan karyawan menggunakan kartu kredit pribadi, dan kemudian meminta penggantian kepada karyawan.</span><span class="sxs-lookup"><span data-stu-id="ecc16-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="ecc16-155">Anda harus membuat keputusan berikut untuk setiap metode pembayaran yang Anda Izinkan.</span><span class="sxs-lookup"><span data-stu-id="ecc16-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="ecc16-156">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="ecc16-156">**Decisions:**</span></span>

- <span data-ttu-id="ecc16-157">Metode pembayaran apa saja yang diizinkan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="ecc16-158">Siapa yang bertanggung jawab atas pengeluaran metode pembayaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="ecc16-159">Apakah ada jenis akun offset?</span><span class="sxs-lookup"><span data-stu-id="ecc16-159">Is there an offset account type?</span></span> <span data-ttu-id="ecc16-160">Jika ada jenis akun offset, apakah itu?</span><span class="sxs-lookup"><span data-stu-id="ecc16-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="ecc16-161">Jika ada jenis akun offset, apakah akunnya?</span><span class="sxs-lookup"><span data-stu-id="ecc16-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="ecc16-162">Jika metode pembayaran adalah kartu kredit, Apakah metode pembayaran hanya digunakan dengan transaksi impor?</span><span class="sxs-lookup"><span data-stu-id="ecc16-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="ecc16-163">Kategori pengeluaran dan kategori bersama</span><span class="sxs-lookup"><span data-stu-id="ecc16-163">Expense categories and shared categories</span></span>

<span data-ttu-id="ecc16-164">Bila karyawan membuat laporan pengeluaran, setiap biaya yang direkam harus dikaitkan dengan kategori pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="ecc16-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="ecc16-165">Kategori pengeluaran berasal dari kategori bersama yang dapat dibagikan di seluruh entitas hukum di organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="ecc16-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="ecc16-166">Kategori ini juga dapat dibagikan dalam manajemen proyek dan akuntansi, tergantung pada cara yang organisasi Anda tentukan.</span><span class="sxs-lookup"><span data-stu-id="ecc16-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="ecc16-167">Berdasarkan definisi organisasi dan panduan dari tim penerapan, tentukan apakah kategori yang digunakan dalam manajemen pengeluaran hanya akan digunakan di manajemen pengeluaran, atau apakah harus dibagikan di antara manajemen proyek dan akuntansi serta manajemen pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="ecc16-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="ecc16-168">Ingat, kategori ini dapat dibagi antara proyek dan pengeluaran atau proyek dan produksi, bukan antara pengeluaran dan produksi.</span><span class="sxs-lookup"><span data-stu-id="ecc16-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="ecc16-169">Anda harus membuat keputusan berikut untuk setiap kategori pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="ecc16-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="ecc16-170">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="ecc16-170">**Decisions:**</span></span>

- <span data-ttu-id="ecc16-171">Apa itu kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-171">What is the expense category?</span></span> <span data-ttu-id="ecc16-172">Contohnya mencakup kategori untuk penerbangan, Hotel, atau jarak tempuh.</span><span class="sxs-lookup"><span data-stu-id="ecc16-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="ecc16-173">Dapatkah kategori pengeluaran juga dapat digunakan dalam manajemen proyek dan akuntansi?</span><span class="sxs-lookup"><span data-stu-id="ecc16-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="ecc16-174">Apa itu jenis pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-174">What is the expense type?</span></span>
- <span data-ttu-id="ecc16-175">Apa yang dimaksud dengan metode pembayaran default untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="ecc16-176">Apakah pengeluaran dalam kategori pengeluaran harus diitemkan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="ecc16-177">Apa yang dimaksud akun default utama untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="ecc16-178">Apa yang dimaksud dengan grup pajak penjualan item default untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="ecc16-179">Apakah metode pembayaran tambahan diizinkan untuk kategori pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="ecc16-180">Jika metode pembayaran tambahan diizinkan, apakah itu?</span><span class="sxs-lookup"><span data-stu-id="ecc16-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="ecc16-181">Apakah ada subkategori dalam kategori pengeluaran ini?</span><span class="sxs-lookup"><span data-stu-id="ecc16-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="ecc16-182">Jika ada subkategori, Anda juga harus membuat keputusan berikut:</span><span class="sxs-lookup"><span data-stu-id="ecc16-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="ecc16-183">Apakah ada subkategori yang dikecualikan dari pemulihan pajak?</span><span class="sxs-lookup"><span data-stu-id="ecc16-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="ecc16-184">Apa yang dimaksud dengan grup pajak penjualan item dari subkategori?</span><span class="sxs-lookup"><span data-stu-id="ecc16-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="ecc16-185">Jika kategori pengeluaran juga digunakan dalam manajemen proyek dan akuntansi, Jawablah pertanyaan yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="ecc16-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="ecc16-186">Atau, lanjutkan ke bagian berikutnya.</span><span class="sxs-lookup"><span data-stu-id="ecc16-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="ecc16-187">Biaya akun apa yang akan digunakan untuk biaya berikut?</span><span class="sxs-lookup"><span data-stu-id="ecc16-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="ecc16-188">Biaya</span><span class="sxs-lookup"><span data-stu-id="ecc16-188">Cost</span></span>
    - <span data-ttu-id="ecc16-189">Alokasi penggajian</span><span class="sxs-lookup"><span data-stu-id="ecc16-189">Payroll allocation</span></span>
    - <span data-ttu-id="ecc16-190">WIP-Nilai biaya</span><span class="sxs-lookup"><span data-stu-id="ecc16-190">WIP-cost value</span></span>
    - <span data-ttu-id="ecc16-191">Item biaya</span><span class="sxs-lookup"><span data-stu-id="ecc16-191">Cost-item</span></span>
    - <span data-ttu-id="ecc16-192">Item-Nilai biaya-WIP</span><span class="sxs-lookup"><span data-stu-id="ecc16-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="ecc16-193">Rugi akrual</span><span class="sxs-lookup"><span data-stu-id="ecc16-193">Accrued loss</span></span>
    - <span data-ttu-id="ecc16-194">Rugi akrual-WIP</span><span class="sxs-lookup"><span data-stu-id="ecc16-194">WIP-accrued loss</span></span>

- <span data-ttu-id="ecc16-195">Akun pendapatan mana yang akan digunakan untuk yang berikut?</span><span class="sxs-lookup"><span data-stu-id="ecc16-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="ecc16-196">Pendapatan yang ditagih</span><span class="sxs-lookup"><span data-stu-id="ecc16-196">Invoiced revenue</span></span>
    - <span data-ttu-id="ecc16-197">pendapatan akrual – nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="ecc16-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="ecc16-198">WIP-nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="ecc16-198">WIP-sales value</span></span>
    - <span data-ttu-id="ecc16-199">Pendapatan akrual-produksi</span><span class="sxs-lookup"><span data-stu-id="ecc16-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="ecc16-200">WIP-Produksi</span><span class="sxs-lookup"><span data-stu-id="ecc16-200">WIP-production</span></span>
    - <span data-ttu-id="ecc16-201">Pendapatan akrual-laba</span><span class="sxs-lookup"><span data-stu-id="ecc16-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="ecc16-202">WIP-Laba</span><span class="sxs-lookup"><span data-stu-id="ecc16-202">WIP-profit</span></span>
    - <span data-ttu-id="ecc16-203">Pendapatan akrual-langganan</span><span class="sxs-lookup"><span data-stu-id="ecc16-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="ecc16-204">WIP-Langganan</span><span class="sxs-lookup"><span data-stu-id="ecc16-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="ecc16-205">Pajak</span><span class="sxs-lookup"><span data-stu-id="ecc16-205">Taxes</span></span>

<span data-ttu-id="ecc16-206">Untuk pajak terkait pengeluaran, Anda harus menentukan apa yang disertakan atau diaktifkan pada laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="ecc16-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="ecc16-207">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="ecc16-207">**Decisions:**</span></span>

- <span data-ttu-id="ecc16-208">Apakah pajak penjualan termasuk dalam jumlah pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="ecc16-209">Haruskah pemulihan pajak diaktifkan pada pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="ecc16-210">Saat Anda merencanakan buku besar, jika Anda memutuskan untuk menerapkan pajak penjualan AS dan aturan pajak penggunaan, Anda tidak dapat mengaktifkan pemulihan pajak pada pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="ecc16-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="ecc16-211">(Untuk menerapkan pajak penjualan AS dan menggunakan aturan pajak, atur **Terapkan pilihan aturan perpajakan pajak penjualan** ke **ya**.)</span><span class="sxs-lookup"><span data-stu-id="ecc16-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="ecc16-212">Kebijakan</span><span class="sxs-lookup"><span data-stu-id="ecc16-212">Policies</span></span>

<span data-ttu-id="ecc16-213">Dengan membuat kebijakan laporan pengeluaran, Anda dapat membantu organisasi menghemat waktu dan uang saat karyawan memiliki pengeluaran atas namanya.</span><span class="sxs-lookup"><span data-stu-id="ecc16-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="ecc16-214">Kebijakan membantu menjamin bahwa karyawan tetap dalam anggaran, menyediakan semua informasi yang diperlukan, dan membelanjakan uang hanya saat mereka memerlukannya.</span><span class="sxs-lookup"><span data-stu-id="ecc16-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="ecc16-215">Anda harus membuat keputusan berikut untuk setiap kebijakan laporan pengeluaran dan setiap kebijakan persetujuan laporan pengeluaran yang Anda buat.</span><span class="sxs-lookup"><span data-stu-id="ecc16-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="ecc16-216">**Keputusan:**</span><span class="sxs-lookup"><span data-stu-id="ecc16-216">**Decisions:**</span></span>

- <span data-ttu-id="ecc16-217">Apa nama kebijakan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-217">What is the name of the policy?</span></span>
- <span data-ttu-id="ecc16-218">Apa yang dimaksud dengan kebijakan pengeluaran?</span><span class="sxs-lookup"><span data-stu-id="ecc16-218">What is the expense policy for?</span></span>
- <span data-ttu-id="ecc16-219">Jika Anda sebelumnya memutuskan untuk mengaktifkan pengeluaran antarperusahaan, perusahaan mana yang akan diterapkan kebijakan ini dalam organisasi Anda?</span><span class="sxs-lookup"><span data-stu-id="ecc16-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="ecc16-220">Kapan kebijakan menjadi efektif?</span><span class="sxs-lookup"><span data-stu-id="ecc16-220">When does the policy become effective?</span></span>
- <span data-ttu-id="ecc16-221">Kapan kebijakan berakhir?</span><span class="sxs-lookup"><span data-stu-id="ecc16-221">When does the policy expire?</span></span>
- <span data-ttu-id="ecc16-222">Apa aturan kebijakan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-222">What is the policy rule?</span></span>
- <span data-ttu-id="ecc16-223">Apa hasil dari aturan kebijakan?</span><span class="sxs-lookup"><span data-stu-id="ecc16-223">What is the outcome of the policy rule?</span></span>

---
title: Pemrosesan tanda terima pengeluaran
description: Topik ini menyediakan informasi tentang pemrosesan pengenalan karakter optik (OCR) untuk tanda terima. Fitur ini dirancang untuk meningkatkan pengalaman pengguna saat membuat laporan pengeluaran di Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271807"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="8364d-104">Pemrosesan tanda terima pengeluaran</span><span class="sxs-lookup"><span data-stu-id="8364d-104">Expense receipt processing</span></span>

<span data-ttu-id="8364d-105">Entri pengeluaran telah disempurnakan melalui pengenalan pemrosesan pengenalan karakter optik (OCR) untuk tanda terima.</span><span class="sxs-lookup"><span data-stu-id="8364d-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="8364d-106">Fitur ini dirancang untuk meningkatkan pengalaman pengguna saat membuat laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="8364d-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="8364d-107">Fitur utama</span><span class="sxs-lookup"><span data-stu-id="8364d-107">Key features</span></span>

- <span data-ttu-id="8364d-108">Nama pedagang, tanggal, dan jumlah total diekstrak dari kuitansi.</span><span class="sxs-lookup"><span data-stu-id="8364d-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="8364d-109">Fitur ini mencoba mencocokkan tanda terima yang tidak dilampirkan dengan transaksi pengeluaran yang tidak dilampirkan.</span><span class="sxs-lookup"><span data-stu-id="8364d-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="8364d-110">Pengguna dapat membuat transaksi pengeluaran yang dimasukkan secara manual dari tanda terima.</span><span class="sxs-lookup"><span data-stu-id="8364d-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="8364d-111">Contoh penggunaan</span><span class="sxs-lookup"><span data-stu-id="8364d-111">Usage examples</span></span>

<span data-ttu-id="8364d-112">Untuk secara otomatis melampirkan tanda terima yang mencakup transaksi kartu kredit saat laporan pengeluaran dibuat, lakukan yang berikut:</span><span class="sxs-lookup"><span data-stu-id="8364d-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="8364d-113">Buka ruang kerja **manajemen pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="8364d-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="8364d-114">Pada tab **tanda terima**, Verifikasikan bahwa ada tanda terima tanpa lampiran.</span><span class="sxs-lookup"><span data-stu-id="8364d-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="8364d-115">Anda juga dapat mengunggah tanda terima pada tab **tanda terima**.</span><span class="sxs-lookup"><span data-stu-id="8364d-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="8364d-116">Pada tab **Pengeluaran**, Verifikasikan bahwa ada Pengeluaran tanpa lampiran.</span><span class="sxs-lookup"><span data-stu-id="8364d-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="8364d-117">Biasanya, administrator pengeluaran mengimpor pengeluaran ini dari penyedia kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="8364d-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="8364d-118">Pilih **laporan pengeluaran baru**.</span><span class="sxs-lookup"><span data-stu-id="8364d-118">Select **New expense report**.</span></span> <span data-ttu-id="8364d-119">Perhatikan bahwa Anda dapat menyertakan pengeluaran, dan tanda terima, sekarang juga, saat membuat laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="8364d-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="8364d-120">Jika Anda menambahkan pengeluaran dan tanda terima, pencocokan otomatis tanda terima terhadap pengeluaran akan dipicu.</span><span class="sxs-lookup"><span data-stu-id="8364d-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="8364d-121">Untuk membuat pengeluaran, atau mencocokkan pengeluaran dari tanda terima, lakukan langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="8364d-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="8364d-122">Pada laporan pengeluaran, di tab **tanda terima**, lampirkan tanda terima dengan memilih **Tambah tanda terima**.</span><span class="sxs-lookup"><span data-stu-id="8364d-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="8364d-123">Di dalam gambar tanda terima yang telah diunggah, perhatikan pilihan **buat** dan **Cocokkan**.</span><span class="sxs-lookup"><span data-stu-id="8364d-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="8364d-124">Pilih **buat** untuk membuat transaksi pengeluaran yang dimasukkan secara manual dan masukkan nilai yang diekstrak dari tanda terima.</span><span class="sxs-lookup"><span data-stu-id="8364d-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="8364d-125">Jika Anda memilih **Cocokkan**, sistem akan mencoba mencocokkan pengeluaran yang ada dengan tanda terima.</span><span class="sxs-lookup"><span data-stu-id="8364d-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="8364d-126">Penginstalan</span><span class="sxs-lookup"><span data-stu-id="8364d-126">Installation</span></span>

<span data-ttu-id="8364d-127">Fitur ini bekerja sama dengan fitur **Konsep baru laporan pengeluaran** untuk membantu menyederhanakan pengalaman pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="8364d-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="8364d-128">Fitur ini hanya tersedia untuk lingkungan tingkat 2 +, yakni Sandbox dan produksi.</span><span class="sxs-lookup"><span data-stu-id="8364d-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="8364d-129">Untuk menggunakan kemampuan pengeluaran tingkat lanjut ini, instal Add-in Layanan Manajemen pengeluaran untuk Microsoft Dynamics 365 Finance, dan Aktifkan fitur tersebut dalam instans Anda.</span><span class="sxs-lookup"><span data-stu-id="8364d-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="8364d-130">Anda dapat mengakses Add-in dari proyek di Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="8364d-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="8364d-131">Masuk ke LCS, dan buka lingkungan yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="8364d-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="8364d-132">Buka **rincian lengkap**.</span><span class="sxs-lookup"><span data-stu-id="8364d-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="8364d-133">Pilih **Kelola**, atau gulir ke bawah ke fasttab **Add-in lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="8364d-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="8364d-134">Pilih **Instal Add-in baru**.</span><span class="sxs-lookup"><span data-stu-id="8364d-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="8364d-135">Pilih **Layanan Manajemen pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="8364d-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="8364d-136">Ikuti panduan penginstalan, dan Setujui persyaratan dan ketentuan.</span><span class="sxs-lookup"><span data-stu-id="8364d-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="8364d-137">Pilih **Instal**.</span><span class="sxs-lookup"><span data-stu-id="8364d-137">Select **Install**.</span></span>

<span data-ttu-id="8364d-138">Di ruang kerja **manajemen fitur**, Aktifkan fitur berikut:</span><span class="sxs-lookup"><span data-stu-id="8364d-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="8364d-139">Laporan pengeluaran model baru</span><span class="sxs-lookup"><span data-stu-id="8364d-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="8364d-140">Pencocokan otomatis dan membuat pengeluaran dari tanda terima</span><span class="sxs-lookup"><span data-stu-id="8364d-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="8364d-141">Bila Anda mengaktifkan fitur ini, maka tindakan berikut terjadi:</span><span class="sxs-lookup"><span data-stu-id="8364d-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="8364d-142">**Ruang kerja manajemen pengeluaran** yang ada digantikan dengan ruang kerja baru.</span><span class="sxs-lookup"><span data-stu-id="8364d-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="8364d-143">Item menu baru untuk visibilitas bidang pengeluaran ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="8364d-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="8364d-144">Anda tetap dapat membuka halaman **laporan pengeluaran** sebelumnya dengan membuka **manajemen pengeluaran > pengeluaran saya > laporan pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="8364d-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="8364d-145">Alur kerja dan persetujuan apa pun tetap akan membawa Anda ke halaman laporan pengeluaran yang ada.</span><span class="sxs-lookup"><span data-stu-id="8364d-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="8364d-146">Kuitansi akan diproses melalui Microsoft Azure Cognitive Services, dan metadata akan diekstrak dan ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="8364d-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="8364d-147">Pilihan ditambahkan yang memungkinkan Anda membuat laporan pengeluaran yang mencakup tanda terima tanpa lampiran yang dicocokkan.</span><span class="sxs-lookup"><span data-stu-id="8364d-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="8364d-148">Pilihan yang ditambahkan ke laporan pengeluaran memungkinkan Anda membuat baris pengeluaran dari tanda terima, atau mencoba mencocokkan tanda terima yang ada ke baris pengeluaran yang ada.</span><span class="sxs-lookup"><span data-stu-id="8364d-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="8364d-149">Untuk informasi lebih lanjut tentang fitur dengan konsep baru laporan pengeluaran, lihat [Konsep baru laporan pengeluaran](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="8364d-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="8364d-150">Tanya jawab</span><span class="sxs-lookup"><span data-stu-id="8364d-150">Frequently asked questions</span></span>

<span data-ttu-id="8364d-151">**Apakah Microsoft menggunakan data saya untuk modelnya?**</span><span class="sxs-lookup"><span data-stu-id="8364d-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="8364d-152">Tidak, Microsoft telah membangun model Pembelajaran Mesin umum untuk layanan pemrosesan tanda terima.</span><span class="sxs-lookup"><span data-stu-id="8364d-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="8364d-153">Model ini tidak didasarkan pada tanda terima yang Anda Unggah.</span><span class="sxs-lookup"><span data-stu-id="8364d-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="8364d-154">**Di manakah fitur ini tersedia dan diproses?**</span><span class="sxs-lookup"><span data-stu-id="8364d-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="8364d-155">Saat ini, Amerika Serikat didukung.</span><span class="sxs-lookup"><span data-stu-id="8364d-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="8364d-156">**Ke mana tanda terima saya pergi?**</span><span class="sxs-lookup"><span data-stu-id="8364d-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="8364d-157">Finance akan menghubungi Cognitive Services untuk mengekstrak data bidang.</span><span class="sxs-lookup"><span data-stu-id="8364d-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="8364d-158">Cognitive Services akan menyimpan salinan tAnda terima Anda hingga 24 jam saat pemrosesan terjadi.</span><span class="sxs-lookup"><span data-stu-id="8364d-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="8364d-159">Setelah pemrosesan selesai, Cognitive Services akan menghapus tanda terima.</span><span class="sxs-lookup"><span data-stu-id="8364d-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="8364d-160">Kuitansi tetap tersimpan di Finance.</span><span class="sxs-lookup"><span data-stu-id="8364d-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="8364d-161">Untuk informasi lebih lanjut, lihat [mengaktifkan pemahaman tanda terima dengan kemampuan baru Pengenal formulir](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="8364d-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
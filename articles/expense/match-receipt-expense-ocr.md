---
title: Merekam tanda terima dengan OCR
description: Topik ini menyediakan informasi tentang pemrosesan pengenalan karakter optik (OCR) untuk tanda terima.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499855"
---
# <a name="capture-a-receipt-using-ocr"></a><span data-ttu-id="b4d43-103">Merekam tanda terima dengan OCR</span><span class="sxs-lookup"><span data-stu-id="b4d43-103">Capture a receipt using OCR</span></span>

<span data-ttu-id="b4d43-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b4d43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b4d43-105">Entri pengeluaran telah disempurnakan melalui pengenalan pemrosesan pengenalan karakter optik (OCR) untuk tanda terima.</span><span class="sxs-lookup"><span data-stu-id="b4d43-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="b4d43-106">Fungsi ini dirancang untuk meningkatkan pengalaman pengguna saat membuat laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="b4d43-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="b4d43-107">Fitur utama</span><span class="sxs-lookup"><span data-stu-id="b4d43-107">Key features</span></span>

- <span data-ttu-id="b4d43-108">Sistem mengekstrak nama pedagang, tanggal, dan jumlah total dari kuitansi.</span><span class="sxs-lookup"><span data-stu-id="b4d43-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="b4d43-109">Sistem akan mencoba mencocokkan tanda terima yang tidak dilampirkan dengan transaksi pengeluaran yang tidak dilampirkan.</span><span class="sxs-lookup"><span data-stu-id="b4d43-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="b4d43-110">Anda dapat membuat transaksi pengeluaran yang dimasukkan secara manual dari tanda terima.</span><span class="sxs-lookup"><span data-stu-id="b4d43-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="b4d43-111">Melampirkan tanda terima ke laporan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="b4d43-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="b4d43-112">Untuk secara otomatis melampirkan tanda terima yang mencakup transaksi kartu kredit saat laporan pengeluaran dibuat, selesaikan langkah-langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="b4d43-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="b4d43-113">Buka ruang kerja **manajemen pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="b4d43-114">Pada tab **tanda terima**, Verifikasikan bahwa ada tanda terima tanpa lampiran.</span><span class="sxs-lookup"><span data-stu-id="b4d43-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="b4d43-115">Anda juga dapat mengunggah tanda terima pada tab **tanda terima**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="b4d43-116">Pada tab **Pengeluaran**, Verifikasikan bahwa ada Pengeluaran tanpa lampiran.</span><span class="sxs-lookup"><span data-stu-id="b4d43-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="b4d43-117">Biasanya, administrator pengeluaran mengimpor pengeluaran ini dari penyedia kartu kredit.</span><span class="sxs-lookup"><span data-stu-id="b4d43-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="b4d43-118">Pilih **laporan pengeluaran baru**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-118">Select **New expense report**.</span></span> <span data-ttu-id="b4d43-119">Perhatikan bahwa Anda dapat menyertakan pengeluaran, dan tanda terima, sekarang juga, saat membuat laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="b4d43-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="b4d43-120">Jika Anda menambahkan pengeluaran dan tanda terima, pencocokan otomatis tanda terima terhadap pengeluaran akan dipicu.</span><span class="sxs-lookup"><span data-stu-id="b4d43-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="b4d43-121">Membuat atau mencocokkan tanda terima ke laporan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="b4d43-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="b4d43-122">Untuk membuat pengeluaran, atau mencocokkan pengeluaran dari tanda terima, selesaikan langkah-langkah berikut.</span><span class="sxs-lookup"><span data-stu-id="b4d43-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="b4d43-123">Pada laporan pengeluaran, di tab **tanda terima**, lampirkan tanda terima dengan memilih **Tambah tanda terima**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="b4d43-124">Di dalam gambar tanda terima yang telah diunggah, perhatikan pilihan **buat** dan **Cocokkan**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="b4d43-125">Pilih **buat** untuk membuat transaksi pengeluaran yang dimasukkan secara manual dan masukkan nilai yang diekstrak dari tanda terima.</span><span class="sxs-lookup"><span data-stu-id="b4d43-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="b4d43-126">Jika Anda memilih **Cocokkan**, sistem akan mencoba mencocokkan pengeluaran yang ada dengan tanda terima.</span><span class="sxs-lookup"><span data-stu-id="b4d43-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="b4d43-127">Penginstalan</span><span class="sxs-lookup"><span data-stu-id="b4d43-127">Installation</span></span>

<span data-ttu-id="b4d43-128">Untuk menggunakan kemampuan pengeluaran tingkat lanjut ini, instal Add-in Layanan Manajemen pengeluaran untuk Microsoft Dynamics 365 Finance, dan Aktifkan fitur tersebut dalam instans Anda.</span><span class="sxs-lookup"><span data-stu-id="b4d43-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="b4d43-129">Anda dapat mengakses Add-in dari proyek di Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="b4d43-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="b4d43-130">Masuk ke LCS, dan buka lingkungan yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="b4d43-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="b4d43-131">Buka **rincian lengkap**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="b4d43-132">Pilih **Kelola**, atau gulir ke bawah ke fasttab **Add-in lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="b4d43-133">Pilih **Instal Add-in baru**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="b4d43-134">Pilih **Layanan Manajemen pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="b4d43-135">Ikuti panduan penginstalan, dan Setujui persyaratan dan ketentuan.</span><span class="sxs-lookup"><span data-stu-id="b4d43-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="b4d43-136">Pilih **Instal**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-136">Select **Install**.</span></span>

<span data-ttu-id="b4d43-137">Di ruang kerja **manajemen fitur**, Aktifkan fitur berikut:</span><span class="sxs-lookup"><span data-stu-id="b4d43-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="b4d43-138">Laporan pengeluaran model baru</span><span class="sxs-lookup"><span data-stu-id="b4d43-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="b4d43-139">Pencocokan otomatis dan membuat pengeluaran dari tanda terima</span><span class="sxs-lookup"><span data-stu-id="b4d43-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="b4d43-140">Bila Anda mengaktifkan fitur ini, maka tindakan berikut terjadi:</span><span class="sxs-lookup"><span data-stu-id="b4d43-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="b4d43-141">**Ruang kerja manajemen pengeluaran** yang ada digantikan dengan ruang kerja baru.</span><span class="sxs-lookup"><span data-stu-id="b4d43-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="b4d43-142">Item menu baru untuk visibilitas bidang pengeluaran ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="b4d43-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="b4d43-143">Anda tetap dapat membuka halaman **laporan pengeluaran** sebelumnya dengan membuka **manajemen pengeluaran > pengeluaran saya > laporan pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="b4d43-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="b4d43-144">Alur kerja dan persetujuan apa pun tetap akan membawa Anda ke halaman laporan pengeluaran yang ada.</span><span class="sxs-lookup"><span data-stu-id="b4d43-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="b4d43-145">Kuitansi akan diproses melalui Microsoft Azure Cognitive Services, dan metadata akan diekstrak dan ditambahkan.</span><span class="sxs-lookup"><span data-stu-id="b4d43-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="b4d43-146">Pilihan ditambahkan yang memungkinkan Anda membuat laporan pengeluaran yang mencakup tanda terima tanpa lampiran yang dicocokkan.</span><span class="sxs-lookup"><span data-stu-id="b4d43-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="b4d43-147">Pilihan yang ditambahkan ke laporan pengeluaran memungkinkan Anda membuat baris pengeluaran dari tanda terima, atau mencoba mencocokkan tanda terima yang ada ke baris pengeluaran yang ada.</span><span class="sxs-lookup"><span data-stu-id="b4d43-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="b4d43-148">Tanya jawab</span><span class="sxs-lookup"><span data-stu-id="b4d43-148">Frequently asked questions</span></span>

<span data-ttu-id="b4d43-149">**Apakah Microsoft menggunakan data saya untuk modelnya?**</span><span class="sxs-lookup"><span data-stu-id="b4d43-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="b4d43-150">Tidak, Microsoft telah membangun model Pembelajaran Mesin umum untuk layanan pemrosesan tanda terima.</span><span class="sxs-lookup"><span data-stu-id="b4d43-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="b4d43-151">Model ini tidak didasarkan pada tanda terima yang Anda Unggah.</span><span class="sxs-lookup"><span data-stu-id="b4d43-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="b4d43-152">**Di manakah fitur ini tersedia dan diproses?**</span><span class="sxs-lookup"><span data-stu-id="b4d43-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="b4d43-153">Saat ini, Amerika Serikat didukung.</span><span class="sxs-lookup"><span data-stu-id="b4d43-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="b4d43-154">**Ke mana tanda terima saya pergi?**</span><span class="sxs-lookup"><span data-stu-id="b4d43-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="b4d43-155">Finance akan menghubungi Cognitive Services untuk mengekstrak data bidang.</span><span class="sxs-lookup"><span data-stu-id="b4d43-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="b4d43-156">Cognitive Services akan menyimpan salinan tAnda terima Anda hingga 24 jam saat pemrosesan terjadi.</span><span class="sxs-lookup"><span data-stu-id="b4d43-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="b4d43-157">Setelah pemrosesan selesai, Cognitive Services akan menghapus tanda terima.</span><span class="sxs-lookup"><span data-stu-id="b4d43-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="b4d43-158">Kuitansi tetap tersimpan di Finance.</span><span class="sxs-lookup"><span data-stu-id="b4d43-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="b4d43-159">Untuk informasi lebih lanjut, lihat [mengaktifkan pemahaman tanda terima dengan kemampuan baru Pengenal formulir](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="b4d43-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

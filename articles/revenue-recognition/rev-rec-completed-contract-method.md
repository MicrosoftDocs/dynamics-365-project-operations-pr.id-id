---
title: Mengelola estimasi pendapatan
description: Topik ini berisi informasi tentang cara menggunakan estimasi pendapatan untuk berbagai proyek.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b63346f56db8b906e5aa45940465bdb18e3df480
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279007"
---
# <a name="manage-revenue-estimates"></a><span data-ttu-id="0c5f3-103">Mengelola estimasi pendapatan</span><span class="sxs-lookup"><span data-stu-id="0c5f3-103">Manage revenue estimates</span></span>

<span data-ttu-id="0c5f3-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="0c5f3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0c5f3-105">Anda dapat membuat, menghitung, memposting, membalik, atau menghilangkan estimasi pendapatan.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-105">You can create, calculate, post, reverse, or eliminate revenue estimates.</span></span> <span data-ttu-id="0c5f3-106">Anda dapat melakukannya, baik secara manual maupun menggunakan proses berkala.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-106">You can do this either manually or by using a periodic process.</span></span> <span data-ttu-id="0c5f3-107">Topik ini berisi informasi tentang cara menggunakan estimasi pendapatan untuk berbagai proyek.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-107">This topic provides information about how to work with revenue estimates for projects.</span></span>

### <a name="manage-revenue-estimates-manually"></a><span data-ttu-id="0c5f3-108">Mengelola estimasi pendapatan secara manual</span><span class="sxs-lookup"><span data-stu-id="0c5f3-108">Manage revenue estimates manually</span></span>

<span data-ttu-id="0c5f3-109">Pada proyek estimasi pendapatan harga tetap atau halaman **Estimasi permintaan** (**Manajemen dan akuntansi proyek** > **Laporan pertanyaan** > **Estimasi pertanyaan dan laporan**), pilih **Estimasi**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-109">On the fixed price revenue estimate project or the **Estimate inquiry** page (**Project management and accounting** > **Reports and inquiries** > **Estimates inquiries and reports**), select **Estimates**.</span></span>

### <a name="manage-revenue-estimates-using-a-periodic-process"></a><span data-ttu-id="0c5f3-110">Mengelola estimasi pendapatan menggunakan proses berkala</span><span class="sxs-lookup"><span data-stu-id="0c5f3-110">Manage revenue estimates using a periodic process</span></span>

<span data-ttu-id="0c5f3-111">Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Estimasi** dan pilih proses yang terkait.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-111">Go to **Project management and accounting** > **Periodic** > **Estimates** and select the corresponding process.</span></span>

## <a name="create-a-revenue-estimate"></a><span data-ttu-id="0c5f3-112">Membuat estimasi pendapatan</span><span class="sxs-lookup"><span data-stu-id="0c5f3-112">Create a revenue estimate</span></span>

<span data-ttu-id="0c5f3-113">Lakukan langkah-langkah berikut untuk membuat estimasi pendapatan.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-113">Complete the following steps to create a revenue estimate.</span></span> 

1. <span data-ttu-id="0c5f3-114">Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Estimasi**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-114">Go to **Project management and accounting** > **Periodic** > **Estimates**.</span></span>
2. <span data-ttu-id="0c5f3-115">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-115">Select **New**.</span></span> <span data-ttu-id="0c5f3-116">Pada halaman **Pembuatan estimasi**, pilih parameter berikut:</span><span class="sxs-lookup"><span data-stu-id="0c5f3-116">On the **Estimate creation** page, select the following parameters:</span></span>

   - <span data-ttu-id="0c5f3-117">**Kode periode** : Kode ini menentukan seberapa sering estimasi akan diposting.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-117">**Period code**: This code determines how frequently estimates are posted.</span></span>
   - <span data-ttu-id="0c5f3-118">**Tanggal estimasi**: Tanggal estimasi diproses.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-118">**Estimate date**: The date the estimate is processed.</span></span>
   - <span data-ttu-id="0c5f3-119">**Kontinu**: Pilih kotak centang ini untuk membuat estimasi hanya apabila estimasi diposting pada periode sebelumnya atau jika estimasi merupakan estimasi pertama yang telah dibuat.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-119">**Continuous**: Select this check box to create estimates only if estimates were posted in the previous period, or if the estimate is the first estimate that has been created.</span></span> <span data-ttu-id="0c5f3-120">Jika tidak dipilih, estimasi akan dibuat meskipun estimasi tidak diposting pada periode sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-120">If this is not selected, estimates are created even if estimates were not posted in the previous period.</span></span>
   - <span data-ttu-id="0c5f3-121">**Metode biaya penyelesaian**: Menentukan cara membuat estimasi pekerjaan proyek yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-121">**Cost to complete method**: Define how to estimate the remaining project work.</span></span> <span data-ttu-id="0c5f3-122">Untuk informasi lebih lanjut, lihat [metode biaya penyelesaian](cost-complete-methods.md).</span><span class="sxs-lookup"><span data-stu-id="0c5f3-122">For more information, see [Cost to complete methods](cost-complete-methods.md).</span></span>
   - <span data-ttu-id="0c5f3-123">**Metode penyelesaian**: Pilih metode penyelesaian dari pilihan berikut:</span><span class="sxs-lookup"><span data-stu-id="0c5f3-123">**Completion method**: Select a completion method from the following options:</span></span>
     - <span data-ttu-id="0c5f3-124">**Otomatis**: Persentase penyelesaian dihitung secara otomatis dan berdasarkan pada baris biaya yang tercakup dalam perhitungan.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-124">**Automatic**: The completion percentage is calculated automatically and based on the cost lines included in the calculation.</span></span> <span data-ttu-id="0c5f3-125">Template biaya menentukan baris biaya yang disertakan.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-125">The cost template defines the cost lines that are included.</span></span>
     - <span data-ttu-id="0c5f3-126">**Manual**: Persentase penyelesaian setara dengan persentase penyelesaian estimasi terakhir.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-126">**Manual**: The completion percentage equals the completion percentage of the last estimate.</span></span> <span data-ttu-id="0c5f3-127">Setelah estimasi dibuat, Anda dapat mengubah **Penghitungan manual** pada halaman **Estimasi**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-127">After the estimate is created, you can change the **Manual calculation** on the **Estimates** page.</span></span>
     - <span data-ttu-id="0c5f3-128">**Dari template biaya**: Kombinasi dari metode otomatis dan manual.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-128">**From cost template**: A combination of the automatic and manual methods.</span></span> <span data-ttu-id="0c5f3-129">Pilihan ini diatur secara otomatis atau manual, tergantung pada nilai default dalam template biaya.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-129">This option is set automatically or manually, depending on the default value in the cost template.</span></span>
   - <span data-ttu-id="0c5f3-130">**Model prakiraan**: Memilih model prakiraan untuk estimasi.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-130">**Forecast model**: Select a forecast model for the estimate.</span></span>
   - <span data-ttu-id="0c5f3-131">**Daftar estimasi cetak**: Membuat dan menampilkan daftar estimasi.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-131">**Print estimate list**: Create and show an estimate list.</span></span> <span data-ttu-id="0c5f3-132">Daftar berisi status fungsi saat ini.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-132">The list contains the status of the current function.</span></span> <span data-ttu-id="0c5f3-133">Anda dapat mencetak peringatan tentang estimasi pada laporan.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-133">You can print any warnings about the estimate on the report.</span></span> <span data-ttu-id="0c5f3-134">Kondisi berikut menyebabkan peringatan muncul di daftar estimasi:</span><span class="sxs-lookup"><span data-stu-id="0c5f3-134">The following conditions cause warnings to appear in the estimate list:</span></span>
     - <span data-ttu-id="0c5f3-135">Persentase penyelesaian lebih dari 100 persen.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-135">A completion percentage of more than 100 percent.</span></span>
     - <span data-ttu-id="0c5f3-136">Persentase penyelesaian kurang dari nol persen.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-136">A completion percentage less than zero percent.</span></span>
     - <span data-ttu-id="0c5f3-137">Jumlah negatif di kolom **Untuk diselesaikan**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-137">A negative amount in the **To complete** column.</span></span>
     - <span data-ttu-id="0c5f3-138">Estimasi tanpa jumlah kontrak yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-138">An estimate with no corresponding contract amount.</span></span>
     - <span data-ttu-id="0c5f3-139">Estimasi tanpa estimasi biaya terlampir.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-139">An estimate with no attached cost estimate.</span></span>
   - <span data-ttu-id="0c5f3-140">**Tampilkan Infolog**: Pilih pilihan ini untuk menerima pesan berisi informasi tentang estimasi proyek yang diproses saat pekerjaan berjalan.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-140">**Show Infolog**: Select this option to receive a message that contains information about the estimate projects that were processed when the job was run.</span></span>


## <a name="post-wip-or-accruals"></a><span data-ttu-id="0c5f3-141">Memposting WIP atau akrual</span><span class="sxs-lookup"><span data-stu-id="0c5f3-141">Post WIP or accruals</span></span>

<span data-ttu-id="0c5f3-142">Setelah estimasi dievaluasi, estimasi tersebut dikelola, dikurang atau ditingkatkan.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-142">After the estimates are evaluated, they are maintained, decreased, or increased.</span></span> <span data-ttu-id="0c5f3-143">Selanjutnya Anda dapat memposting WIP saat menggunakan prinsip penilaian **Kontrak yang telah selesai**, atau memposting akrual saat Anda menggunakan prinsip penilaian **Persentase yang telah selesai**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-143">You can then post the WIP when you work with the **Completed contract** assessment principle, or post the accruals when you work with the **Completed percentage** assessment principle.</span></span>
  
<span data-ttu-id="0c5f3-144">Status periode estimasi berubah dari **Dibuat** menjadi **Diposting**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-144">The estimate period status changes from **Created** to **Posted**.</span></span>

## <a name="reverse-wip-or-accruals"></a><span data-ttu-id="0c5f3-145">WIP Terbalik atau akrual</span><span class="sxs-lookup"><span data-stu-id="0c5f3-145">Reverse WIP or accruals</span></span>

<span data-ttu-id="0c5f3-146">Gunakan pilihan balik untuk kredit yang telah memposting WIP atau akrual, lalu buat estimasi untuk periode tersebut.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-146">Use the reverse option to credit already posted WIP or accruals, and then create estimates for the period.</span></span>

> [!NOTE]
> <span data-ttu-id="0c5f3-147">Untuk membalikkan periode yang berada di antara beberapa periode lain, balikkan periode estimasi yang diperlukan, lalu posting ulang.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-147">To reverse a period that is in between other periods, reverse the necessary estimate periods and then repost them.</span></span> <span data-ttu-id="0c5f3-148">Karena semua periode berikutnya tergantung pada estimasi dari periode sebelumnya, jangan lewati periode apa pun.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-148">Because all subsequent periods depend on the estimates from the previous period, don't skip any periods.</span></span>

## <a name="eliminate-the-estimate-project-and-finish-the-project"></a><span data-ttu-id="0c5f3-149">Hilangkan estimasi proyek dan selesaikan proyek</span><span class="sxs-lookup"><span data-stu-id="0c5f3-149">Eliminate the estimate project and finish the project</span></span>

<span data-ttu-id="0c5f3-150">Langkah terakhir dalam proses estimasi adalah menghilangkan estimasi proyek dan mengakhiri proyek harga tetap saat persentase penyelesaian mencapai 100 persen.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-150">The final step in the estimate process is to eliminate the estimate project and end the fixed price project when the percentage of completion reaches 100 percent.</span></span>

<span data-ttu-id="0c5f3-151">Berikut adalah yang akan terjadi saat Anda menjalankan penghapusan:</span><span class="sxs-lookup"><span data-stu-id="0c5f3-151">The following occurs when you run the elimination:</span></span>

- <span data-ttu-id="0c5f3-152">Untuk proyek harga tetap dengan kontrak yang telah diselesaikan, nilai WIP diperoleh dari akun saldo dan diposting ke akun laba dan rugi.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-152">For a fixed price project with a completed contract, the WIP values clear from the balance accounts and post to the profit and loss accounts.</span></span>
- <span data-ttu-id="0c5f3-153">Untuk proyek harga tetap dengan persentase yang telah selesai, akrual akan dihapus dari akun laba dan rugi.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-153">For a fixed-price project with a completed percentage, the accruals are removed from the profit and loss accounts.</span></span>

<span data-ttu-id="0c5f3-154">Estimasi akan berubah status menjadi **Dihilangkan**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-154">The estimate changes the status to **Eliminated**.</span></span>

> [!NOTE]
> <span data-ttu-id="0c5f3-155">Dalam kasus khusus, persentase dapat melampaui 100 persen.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-155">In special cases, the percentage can extend beyond 100 percent.</span></span> <span data-ttu-id="0c5f3-156">Bila ini terjadi, kurangi persentase penyelesaian dengan menggunakan **Atur biaya ke metode penyelesaian nol** untuk mencapai 100 persen.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-156">When this happens, reduce the percentage of completion by using the **Set cost to complete to zero method** to reach 100 percent.</span></span>

## <a name="reverse-elimination"></a><span data-ttu-id="0c5f3-157">Penghilangan terbalik</span><span class="sxs-lookup"><span data-stu-id="0c5f3-157">Reverse elimination</span></span>

1. <span data-ttu-id="0c5f3-158">Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Estimasi** > **Penghilangan terbalik**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-158">Go to **Project management and accounting** > **Periodic** > **Estimates** > **Reverse elimination**.</span></span> 
2. <span data-ttu-id="0c5f3-159">Pada Panel Tindakan, di tab **Proses**, dalam grup **Kelola**, pilih **Estimasi**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-159">On the Action Pane, on the **Process** tab, in the **Maintain** group, select **Estimate**.</span></span> 
3. <span data-ttu-id="0c5f3-160">Pilih **Penghilangan terbalik**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-160">Select **Reverse elimination**.</span></span>

<span data-ttu-id="0c5f3-161">Gunakan halaman ini untuk membalik semua penghilangan dengan tanggal estimasi yang ditentukan dan dengan status estimasi **Dihilangkan**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-161">Use this page to reverse all eliminations with a specified estimate date and with an estimate status of **Eliminated**.</span></span> <span data-ttu-id="0c5f3-162">Status transaksi berubah setelah Anda memilih bidang yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-162">The transaction status changes after you select the appropriate fields.</span></span>

<span data-ttu-id="0c5f3-163">Hal ini juga secara otomatis mengubah status proyek ke **Dalam proses** jika tahapan proyek diatur selesai.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-163">This also automatically changes the project status to **In process** if the project stage is set to finished.</span></span> <span data-ttu-id="0c5f3-164">Status estimasi periode proyek berubah kembali ke **Diposting**.</span><span class="sxs-lookup"><span data-stu-id="0c5f3-164">The estimate status of the project period changes back to **Posted**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
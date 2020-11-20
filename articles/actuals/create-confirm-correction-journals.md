---
title: Membuat dan mengonfirmasi jurnal koreksi
description: Topik ini menyediakan informasi tentang cara membuat dan mengonfirmasikan jurnal koreksi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6cc22168cdfefc4ae7b833bea75f68ba37c1ee67
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127759"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="42ad3-103">Membuat dan mengonfirmasi jurnal koreksi</span><span class="sxs-lookup"><span data-stu-id="42ad3-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="42ad3-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="42ad3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="42ad3-105">Terkadang entri waktu atau biaya dapat dimasukkan dengan benar.</span><span class="sxs-lookup"><span data-stu-id="42ad3-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="42ad3-106">Contohnya, konsultan mungkin memilih tanggal yang salah saat membuat entri waktu atau mereka mungkin mentransposisi angka saat memasukkan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="42ad3-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="42ad3-107">Jika konsultan tidak dapat melakukan pembaruan terhadap entri yang diajukan, administrator dapat secara langsung mengoreksi entri untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="42ad3-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="42ad3-108">Untuk menyelesaikan prosedur dalam topik ini, anda memerlukan izin Administrator.</span><span class="sxs-lookup"><span data-stu-id="42ad3-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="42ad3-109">Mengoreksi entri waktu yang disetujui</span><span class="sxs-lookup"><span data-stu-id="42ad3-109">Correct approved time entries</span></span>     

<span data-ttu-id="42ad3-110">Menyelesaikan langkah-langkah berikut untuk mengoreksi entri atau beberapa satu waktu untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="42ad3-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="42ad3-111">Di area **penjualan**, pilih **transaksi**, lalu pilih **waktu yang disetujui**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="42ad3-112">Di daftar **waktu disetujui**, Cari dan pilih satu atau beberapa entri waktu yang disetujui untuk dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="42ad3-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="42ad3-113">Anda dapat menggunakan filter untuk menemukan entri terkait.</span><span class="sxs-lookup"><span data-stu-id="42ad3-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="42ad3-114">Misalnya, Anda dapat memfilter ID proyek, dan memilih semua entri waktu yang disetujui dengan ID proyek tersebut.</span><span class="sxs-lookup"><span data-stu-id="42ad3-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="42ad3-115">Pilih **Koreksi Entri**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-115">Select **Correct entries**.</span></span> <span data-ttu-id="42ad3-116">Jurnal koreksi baru dibuat secara otomatis dengan **koreksi waktu** jenis yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="42ad3-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="42ad3-117">Entri yang Anda pilih ditambahkan ke jurnal.</span><span class="sxs-lookup"><span data-stu-id="42ad3-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="42ad3-118">Pada halaman **jurnal baru**, masukkan **Deskripsi** jurnal koreksi, lalu pilih tab **koreksi entri waktu**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="42ad3-119">Di bagian **nilai baru untuk entri waktu**, Perbarui bidang dengan informasi yang benar yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="42ad3-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="42ad3-120">Misalnya, Anda dapat mengubah proyek yang ditetapkan atau sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="42ad3-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="42ad3-121">pilih **Pratinjau**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-121">Select **Preview**.</span></span> <span data-ttu-id="42ad3-122">Pilih **Oke** di kotak dialog.</span><span class="sxs-lookup"><span data-stu-id="42ad3-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="42ad3-123">Pada tab **lini jurnal**, Anda dapat melihat daftar aktual asli yang terkait dengan entri waktu yang dipilih dan telah dibalik dan dikoreksi sesuai baris yang telah dibuat.</span><span class="sxs-lookup"><span data-stu-id="42ad3-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="42ad3-124">Jika koreksi tambahan perlu dilakukan, ulangi langkah 5 dan 6.</span><span class="sxs-lookup"><span data-stu-id="42ad3-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="42ad3-125">Semua aktual yang dikoreksi akan memiliki nilai yang sama dengan yang Anda pilih di bagian **nilai baru untuk entri waktu**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="42ad3-126">Jika koreksi ditampilkan seperti yang diharapkan, pilih **konfirmasikan**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="42ad3-127">Pilih **Oke** di kotak dialog.</span><span class="sxs-lookup"><span data-stu-id="42ad3-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="42ad3-128">Kembali ke area **penjualan**, pilih **proyek** , lalu buka proyek yang baru saja Anda gunakan untuk memasukkan entri waktu.</span><span class="sxs-lookup"><span data-stu-id="42ad3-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="42ad3-129">Pada halaman **proyek**, pada tab **aktual**, lihat perubahan yang Anda buat.</span><span class="sxs-lookup"><span data-stu-id="42ad3-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="42ad3-130">Jika tab **aktual** tidak terlihat, pilih **terkait** > **aktual**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="42ad3-131">Di daftar **tampilan terkait aktual**, Anda dapat melihat bahwa entri waktu asli yang telah dibalik masih terdaftar, seperti entri waktu dikoreksi yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="42ad3-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="42ad3-132">Misalnya, pada grafik berikut, ada dua item baris dengan kuantitas 8,00 yang memiliki debit yang tercantum di kolom jumlah.</span><span class="sxs-lookup"><span data-stu-id="42ad3-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="42ad3-133">Selain itu, ada dua item baris dengan kuantitas-8,00 yang menunjukkan jumlah dikreditkan di kolom jumlah.</span><span class="sxs-lookup"><span data-stu-id="42ad3-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="42ad3-134">Koreksi ini membawa kuantitas ke nol.</span><span class="sxs-lookup"><span data-stu-id="42ad3-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="42ad3-135">Mengoreksi entri pengeluaran yang disetujui</span><span class="sxs-lookup"><span data-stu-id="42ad3-135">Correct approved expense entries</span></span>

<span data-ttu-id="42ad3-136">Selesaikan langkah-langkah berikut untuk mengoreksi satu atau beberapa entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="42ad3-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="42ad3-137">Di area **penjualan**, di panel navigasi kiri, dalam **transaksi**, pilih **Pengeluaran yang disetujui**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="42ad3-138">Dalam daftar **pengeluaran yang disetujui**, pilih proyek yang ingin Anda Perbaiki, lalu pilih **Koreksi entri**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="42ad3-139">Jurnal koreksi baru akan dibuat secara otomatis dengan **koreksi pengeluaran** jenis yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="42ad3-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="42ad3-140">Pada halaman **jurnal baru**, masukkan **Deskripsi** untuk koreksi, dan di tab **koreksi pengeluaran**, di bagian **nilai baru untuk pengeluaran**, pilih bidang data yang ingin Anda Perbaiki untuk baris pengeluaran yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="42ad3-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="42ad3-141">Misalnya, Anda dapat menetapkan pengeluaran untuk **proyek** lain, atau memperbaiki **kategori pengeluaran**, **tanggal pengeluaran**, atau **sumber daya yang dapat dipesan**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="42ad3-142">pilih **Pratinjau**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-142">Select **Preview**.</span></span> <span data-ttu-id="42ad3-143">Pilih **Oke** di kotak dialog.</span><span class="sxs-lookup"><span data-stu-id="42ad3-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="42ad3-144">Verifikasi koreksi di tab **lini jurnal**. Anda dapat melihat daftar aktual asli yang terkait dengan entri pengeluaran yang dipilih dan telah dibalik dan dikoreksi sesuai baris yang telah dibuat.</span><span class="sxs-lookup"><span data-stu-id="42ad3-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="42ad3-145">Jika nilai yang dikoreksi adalah seperti yang diharapkan, pilih **konfirmasikan**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="42ad3-146">Di kotak dialog, Pilih **Oke.**</span><span class="sxs-lookup"><span data-stu-id="42ad3-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="42ad3-147">Jika nilai tidak ditampilkan sebagaimana mestinya, pilih **Batalkan** untuk kembali ke daftar **pengeluaran yang disetujui**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="42ad3-148">Ulangi langkah 2 hingga 5.</span><span class="sxs-lookup"><span data-stu-id="42ad3-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="42ad3-149">Aktual yang dikoreksi akan memiliki nilai yang sama dengan yang Anda pilih di bagian **nilai baru untuk pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="42ad3-150">Setelah Anda mengkonfirmasi jurnal koreksi, navigasikan kembali ke proyek atau proyek yang Anda diperbarui, untuk melihat perubahan Anda.</span><span class="sxs-lookup"><span data-stu-id="42ad3-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="42ad3-151">Di halaman proyek, pada tab **aktual**, Tinjau **tampilan terkait aktual**.</span><span class="sxs-lookup"><span data-stu-id="42ad3-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="42ad3-152">Entri asli dan entri yang dikoreksi didaftarkan.</span><span class="sxs-lookup"><span data-stu-id="42ad3-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="42ad3-153">Grafik berikut menunjukkan jumlah entri pengeluaran asli dan jumlah entri pengeluaran yang sesuai yang dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="42ad3-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 



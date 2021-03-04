---
title: Koreksi massal aktual yang dibuat berdasarkan entri waktu dan pengeluaran yang disetujui
description: Topik ini menjelaskan cara administrator melakukan koreksi tunggal atau massal terhadap entri waktu atau pengeluaran yang disetujui sebelumnya jika penagihan tidak selesai.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 063c4d017f5904f09c3c239bfa432a128872e4d7
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144957"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="10c9f-103">Koreksi massal aktual yang dibuat berdasarkan entri waktu dan pengeluaran yang disetujui</span><span class="sxs-lookup"><span data-stu-id="10c9f-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="10c9f-104">Terkadang entri waktu atau biaya dapat dimasukkan dengan benar.</span><span class="sxs-lookup"><span data-stu-id="10c9f-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="10c9f-105">Contohnya, konsultan mungkin memilih tanggal yang salah saat membuat entri waktu atau mereka mungkin mentransposisi angka saat memasukkan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="10c9f-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="10c9f-106">Jika konsultan tidak dapat melakukan pembaruan terhadap entri yang diajukan, administrator dapat secara langsung mengoreksi entri untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="10c9f-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="10c9f-107">Untuk menyelesaikan prosedur dalam topik ini, anda memerlukan izin Administrator.</span><span class="sxs-lookup"><span data-stu-id="10c9f-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="10c9f-108">Mengoreksi entri waktu yang disetujui</span><span class="sxs-lookup"><span data-stu-id="10c9f-108">Correct approved time entries</span></span>     

<span data-ttu-id="10c9f-109">Menyelesaikan langkah-langkah berikut untuk mengoreksi entri atau beberapa satu waktu untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="10c9f-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="10c9f-110">Di area **penjualan**, pilih **transaksi**, lalu pilih **waktu yang disetujui**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-110">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="10c9f-111">Di daftar **waktu disetujui**, Cari dan pilih satu atau beberapa entri waktu yang disetujui untuk dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="10c9f-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="10c9f-112">Anda dapat menggunakan filter untuk menemukan entri terkait.</span><span class="sxs-lookup"><span data-stu-id="10c9f-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="10c9f-113">Misalnya, Anda dapat memfilter ID proyek, dan memilih semua entri waktu yang disetujui dengan ID proyek tersebut.</span><span class="sxs-lookup"><span data-stu-id="10c9f-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="10c9f-114">Pilih **Koreksi Entri**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-114">Select **Correct entries**.</span></span> <span data-ttu-id="10c9f-115">Jurnal koreksi baru dibuat secara otomatis dengan **koreksi waktu** jenis yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="10c9f-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="10c9f-116">Entri yang Anda pilih ditambahkan ke jurnal.</span><span class="sxs-lookup"><span data-stu-id="10c9f-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="10c9f-117">Pada halaman **jurnal baru**, masukkan **Deskripsi** jurnal koreksi, lalu pilih tab **koreksi entri waktu**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="10c9f-118">Di bagian **nilai baru untuk entri waktu**, Perbarui bidang dengan informasi yang benar yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="10c9f-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="10c9f-119">Misalnya, Anda dapat mengubah proyek yang ditetapkan atau sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="10c9f-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="10c9f-120">pilih **Pratinjau**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-120">Select **Preview**.</span></span> <span data-ttu-id="10c9f-121">Pilih **Oke** di kotak dialog.</span><span class="sxs-lookup"><span data-stu-id="10c9f-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="10c9f-122">Pada tab **lini jurnal**, Anda dapat melihat daftar aktual asli yang terkait dengan entri waktu yang dipilih dan telah dibalik dan dikoreksi sesuai baris yang telah dibuat.</span><span class="sxs-lookup"><span data-stu-id="10c9f-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="10c9f-123">Jika koreksi tambahan perlu dilakukan, ulangi langkah 5 dan 6.</span><span class="sxs-lookup"><span data-stu-id="10c9f-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="10c9f-124">Semua aktual yang dikoreksi akan memiliki nilai yang sama dengan yang Anda pilih di bagian **nilai baru untuk entri waktu**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="10c9f-125">Jika koreksi ditampilkan seperti yang diharapkan, pilih **konfirmasikan**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="10c9f-126">Pilih **Oke** di kotak dialog.</span><span class="sxs-lookup"><span data-stu-id="10c9f-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="10c9f-127">Kembali ke area **penjualan**, pilih **proyek** , lalu buka proyek yang baru saja Anda gunakan untuk memasukkan entri waktu.</span><span class="sxs-lookup"><span data-stu-id="10c9f-127">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="10c9f-128">Pada halaman **proyek**, pada tab **aktual**, lihat perubahan yang Anda buat.</span><span class="sxs-lookup"><span data-stu-id="10c9f-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="10c9f-129">Jika tab **aktual** tidak terlihat, pilih **terkait** > **aktual**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="10c9f-130">Di daftar **tampilan terkait aktual**, Anda dapat melihat bahwa entri waktu asli yang telah dibalik masih terdaftar, seperti entri waktu dikoreksi yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="10c9f-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="10c9f-131">Misalnya, pada grafik berikut, ada dua item baris dengan kuantitas 8,00 yang memiliki debit yang tercantum di kolom jumlah.</span><span class="sxs-lookup"><span data-stu-id="10c9f-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="10c9f-132">Selain itu, ada dua item baris dengan kuantitas-8,00 yang menunjukkan jumlah dikreditkan di kolom jumlah.</span><span class="sxs-lookup"><span data-stu-id="10c9f-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="10c9f-133">Koreksi ini membawa kuantitas ke nol.</span><span class="sxs-lookup"><span data-stu-id="10c9f-133">These corrections bring the quantity to zero.</span></span>

![Daftar Tampilan Terkait Aktual](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="10c9f-135">Mengoreksi entri pengeluaran yang disetujui</span><span class="sxs-lookup"><span data-stu-id="10c9f-135">Correct approved expense entries</span></span>

<span data-ttu-id="10c9f-136">Selesaikan langkah-langkah berikut untuk mengoreksi satu atau beberapa entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="10c9f-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="10c9f-137">Di area **penjualan**, di panel navigasi kiri, dalam **transaksi**, pilih **Pengeluaran yang disetujui**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="10c9f-138">Dalam daftar **pengeluaran yang disetujui**, pilih proyek yang ingin Anda Perbaiki, lalu pilih **Koreksi entri**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="10c9f-139">Jurnal koreksi baru akan dibuat secara otomatis dengan **koreksi pengeluaran** jenis yang ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="10c9f-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="10c9f-140">Pada halaman **jurnal baru**, masukkan **Deskripsi** untuk koreksi, dan di tab **koreksi pengeluaran**, di bagian **nilai baru untuk pengeluaran**, pilih bidang data yang ingin Anda Perbaiki untuk baris pengeluaran yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="10c9f-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="10c9f-141">Misalnya, Anda dapat menetapkan pengeluaran untuk **proyek** lain, atau memperbaiki **kategori pengeluaran**, **tanggal pengeluaran**, atau **sumber daya yang dapat dipesan**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="10c9f-142">pilih **Pratinjau**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-142">Select **Preview**.</span></span> <span data-ttu-id="10c9f-143">Pilih **Oke** di kotak dialog.</span><span class="sxs-lookup"><span data-stu-id="10c9f-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="10c9f-144">Verifikasi koreksi di tab **lini jurnal**. Anda dapat melihat daftar aktual asli yang terkait dengan entri pengeluaran yang dipilih dan telah dibalik dan dikoreksi sesuai baris yang telah dibuat.</span><span class="sxs-lookup"><span data-stu-id="10c9f-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="10c9f-145">Jika nilai yang dikoreksi adalah seperti yang diharapkan, pilih **konfirmasikan**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="10c9f-146">Di kotak dialog, Pilih **Oke.**</span><span class="sxs-lookup"><span data-stu-id="10c9f-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="10c9f-147">Jika nilai tidak ditampilkan sebagaimana mestinya, pilih **Batalkan** untuk kembali ke daftar **pengeluaran yang disetujui**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="10c9f-148">Ulangi langkah 2 hingga 5.</span><span class="sxs-lookup"><span data-stu-id="10c9f-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="10c9f-149">Aktual yang dikoreksi akan memiliki nilai yang sama dengan yang Anda pilih di bagian **nilai baru untuk pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="10c9f-150">Setelah Anda mengkonfirmasi jurnal koreksi, navigasikan kembali ke proyek atau proyek yang Anda diperbarui, untuk melihat perubahan Anda.</span><span class="sxs-lookup"><span data-stu-id="10c9f-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="10c9f-151">Di halaman proyek, pada tab **aktual**, Tinjau **tampilan terkait aktual**.</span><span class="sxs-lookup"><span data-stu-id="10c9f-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="10c9f-152">Entri asli dan entri yang dikoreksi didaftarkan.</span><span class="sxs-lookup"><span data-stu-id="10c9f-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="10c9f-153">Grafik berikut menunjukkan jumlah entri pengeluaran asli dan jumlah entri pengeluaran yang sesuai yang dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="10c9f-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Aktual_pengeluaran](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)

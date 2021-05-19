---
title: Membuat faktur vendor dan pelanggan antarperusahaan
description: Topik ini memberikan informasi tentang cara membuat faktur pelanggan dan vendor antarperusahaan.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: dd9aa1a4d167d556206a487e79983090b3f4592a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287467"
---
# <a name="create-intercompany-customer-and-vendor-invoices"></a><span data-ttu-id="0865a-103">Membuat faktur vendor dan pelanggan antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="0865a-103">Create intercompany customer and vendor invoices</span></span>

<span data-ttu-id="0865a-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="0865a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0865a-105">Akuntan proyek dalam entitas hukum pemberi pinjaman membuat faktur pelanggan antarperusahaan untuk biaya proyek yang ditransfer ke entitas peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-105">A project accountant in a lending legal entity creates an intercompany customer invoice for the project costs that are being transferred to the borrowing entity.</span></span> <span data-ttu-id="0865a-106">Setelah faktur pelanggan antarperusahaan disetujui dan diposting, entitas hukum pemberi pinjaman mengirimkan faktur antarperusahaan ke entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-106">After the intercompany customer invoice is approved and posted, the lending legal entity sends the intercompany invoice to the borrowing legal entity.</span></span>

<span data-ttu-id="0865a-107">Akuntan proyek untuk entitas hukum pemberi pinjaman dapat mengonfigurasi proses batch untuk menghasilkan faktur antarperusahaan secara berulang.</span><span class="sxs-lookup"><span data-stu-id="0865a-107">The project accountant for the lending legal entity can set up a batch process to generate intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="0865a-108">Akuntan proyek menentukan kriteria, seperti proyek spesifik, untuk membuat faktur antarperusahaan dalam sebuah batch.</span><span class="sxs-lookup"><span data-stu-id="0865a-108">The project accountant specifies the criteria, such as specific projects, to create intercompany invoices in a batch.</span></span>

## <a name="manually-create-an-intercompany-customer-invoice-for-project-transactions"></a><span data-ttu-id="0865a-109">Membuat faktur pelanggan antarperusahaan secara manual untuk transaksi proyek</span><span class="sxs-lookup"><span data-stu-id="0865a-109">Manually create an intercompany customer invoice for project transactions</span></span> 

<span data-ttu-id="0865a-110">Gunakan prosedur ini untuk membuat faktur pelanggan antarperusahaan secara manual untuk transaksi proyek.</span><span class="sxs-lookup"><span data-stu-id="0865a-110">Use this procedure to manually create an intercompany customer invoice for project transactions.</span></span> <span data-ttu-id="0865a-111">Cari jumlah jam yang diposting oleh pekerja pada proyek di entitas hukum peminjam dan untuk biaya yang ditimbulkan oleh entitas hukum Anda atas nama entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-111">Search for hours that were posted by workers on projects in the borrowing legal entities and for expenses that were incurred by your legal entity on behalf of borrowing legal entities.</span></span> <span data-ttu-id="0865a-112">Anda dapat mencari berdasarkan nama entitas hukum, nomor kontrak proyek, nomor proyek, rentang tanggal, atau kombinasi beberapa pilihan ini.</span><span class="sxs-lookup"><span data-stu-id="0865a-112">You can search by legal entity name, project contract number, project number, date range, or any combination of these options.</span></span> <span data-ttu-id="0865a-113">Di hasil pencarian, pilih transaksi untuk ditambahkan ke faktur antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="0865a-113">In the search results, select the transactions to add to an intercompany invoice.</span></span>

1. <span data-ttu-id="0865a-114">Di Dynamics 365 Finance, buka **Manajemen dan akuntansi proyek** > **Faktur proyek** > **Faktur pelanggan antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="0865a-114">In Dynamics 365 Finance, go to **Project management and accounting** > **Project invoices** > **Intercompany customer invoices**.</span></span> <span data-ttu-id="0865a-115">Pada halaman daftar **Faktur pelanggan antarperusahaan**, di Panel Tindakan, pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="0865a-115">On the **Intercompany customer invoices**  list page, on the Action Pane, select **New.**</span></span>
2. <span data-ttu-id="0865a-116">Pada halaman **Buat faktur antarperusahaan**, di bidang **Entitas hukum**, pilih entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-116">On the **Create intercompany invoice** page, in the **Legal entity** field, select a borrowing legal entity.</span></span>
3. <span data-ttu-id="0865a-117">Opsional: Masukkan kontrak proyek dan nomor proyek tertentu.</span><span class="sxs-lookup"><span data-stu-id="0865a-117">Optional: Enter a specific project contract and project number.</span></span>
4. <span data-ttu-id="0865a-118">Persempit pencarian dengan memilih rentang tanggal.</span><span class="sxs-lookup"><span data-stu-id="0865a-118">Narrow the search by selecting a date range.</span></span> <span data-ttu-id="0865a-119">Masukkan tanggal tertentu di bidang **Tanggal mulai** dan **Tanggal akhir**.</span><span class="sxs-lookup"><span data-stu-id="0865a-119">Enter specific dates in the **Start date** and **End date** fields.</span></span> <span data-ttu-id="0865a-120">Hanya transaksi antarperusahaan yang diposting dalam rentang tanggal ini yang akan ditampilkan di hasil pencarian.</span><span class="sxs-lookup"><span data-stu-id="0865a-120">Only intercompany transactions that are posted within this date range are displayed in the search results.</span></span>
5. <span data-ttu-id="0865a-121">Atur **Parameter baris jurnal lanjutan proyek** ke **Ya** dan pilih **Cari**.</span><span class="sxs-lookup"><span data-stu-id="0865a-121">Set **Project advanced journal line parameter** to **Yes** and select **Search**.</span></span>
6. <span data-ttu-id="0865a-122">Di hasil pencarian, pilih transaksi yang akan disertakan dalam proposal faktur antarperusahaan, lalu pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="0865a-122">In the search results, select the transactions to include in the intercompany invoice proposal, and then select **OK**.</span></span>
7. <span data-ttu-id="0865a-123">Pada halaman **Faktur pelanggan antarperusahaan**, transaksi proyek antarperusahaan yang Anda pilih dari hasil pencarian akan ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="0865a-123">On the **Intercompany customer invoice** page, the intercompany project transactions that you selected from the search results are displayed.</span></span> <span data-ttu-id="0865a-124">Untuk mengubah transaksi sebelum Anda mengirim faktur ke entitas hukum peminjam, lakukan langkah-langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="0865a-124">To modify the transactions before you send the invoice to the borrowing legal entity, do the following:</span></span>
  
    1. <span data-ttu-id="0865a-125">Buka halaman **Buat proposal faktur**.</span><span class="sxs-lookup"><span data-stu-id="0865a-125">Open the **Create invoice proposal** page.</span></span> <span data-ttu-id="0865a-126">Pilih transaksi antarperusahaan tambahan untuk faktur saat ini, lalu pilih **Tambah baris**.</span><span class="sxs-lookup"><span data-stu-id="0865a-126">Select additional intercompany transactions for the current invoice, and then select **Add line**.</span></span>
    2. <span data-ttu-id="0865a-127">Untuk menghilangkan baris, pilih komponen, lalu pilih **Hilangkan**.</span><span class="sxs-lookup"><span data-stu-id="0865a-127">To remove a line, select it, and then select **Remove**.</span></span>
    3. <span data-ttu-id="0865a-128">Lihat komentar, alasan, dimensi keuangan, dan informasi lainnya tentang baris yang dipilih pada FastTab **Baris faktur**.</span><span class="sxs-lookup"><span data-stu-id="0865a-128">View comments, reasons, financial dimensions, and other information about a selected line on the  **Invoice lines**  FastTab.</span></span>
    
8. <span data-ttu-id="0865a-129">Untuk memposting faktur pelanggan antarperusahaan, pada Panel Tindakan, pilih **Posting**.</span><span class="sxs-lookup"><span data-stu-id="0865a-129">To post the intercompany customer invoice, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="0865a-130">Jika organisasi Anda mewajibkan faktur antarperusahaan ditinjau sebelum diposting, administrator sistem dapat mengonfigurasikan alur kerja untuk faktur antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="0865a-130">If your organization requires that intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="0865a-131">Jika alur kerja tidak dikonfigurasi untuk faktur antarperusahaan, Anda dapat mengirim faktur antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="0865a-131">If a workflow is not set up for intercompany invoices, you can post the intercompany invoice.</span></span>

## <a name="create-a-batch-job-for-intercompany-invoices"></a><span data-ttu-id="0865a-132">Membuat pekerjaan batch untuk faktur antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="0865a-132">Create a batch job for intercompany invoices</span></span>

<span data-ttu-id="0865a-133">Anda dapat membuat beberapa faktur antarperusahaan secara bersamaan untuk semua entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-133">You can create multiple intercompany invoices at the same time for all borrowing legal entities.</span></span> <span data-ttu-id="0865a-134">Dengan menggunakan fungsi pencarian, Anda dapat misalnya, mencari semua transaksi yang diposting oleh pekerja peminjam dan terkait dengan proyek yang dikelola oleh entitas hukum lainnya.</span><span class="sxs-lookup"><span data-stu-id="0865a-134">Using search functionality, you can for example, search for all transactions that are posted by borrowed workers and related to projects that are managed by other legal entities.</span></span> <span data-ttu-id="0865a-135">Kemudian, untuk setiap entitas hukum peminjam, Anda dapat membuat faktur antarperusahaan untuk transaksi yang tercantum di hasil pencarian.</span><span class="sxs-lookup"><span data-stu-id="0865a-135">Then, for each borrowing legal entity, you can create an intercompany invoice for the transactions provided in the search results.</span></span>

1. <span data-ttu-id="0865a-136">Buka **Manajemen dan akuntansi proyek** > **Berkala** > **Faktur proyek** > **Buat faktur pelanggan antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="0865a-136">Go to **Project management and accounting** > **Periodic** > **Project invoices** > **Create intercompany customer invoices**.</span></span>
2. <span data-ttu-id="0865a-137">Pada halaman **Buat faktur pelanggan antarperusahaan**, di bidang **Perusahaan**, pilih entitas hukum yang akan dibuatkan fakturnya.</span><span class="sxs-lookup"><span data-stu-id="0865a-137">On the **Create intercompany customer invoices** page, in the **Company**  field, select a legal entity to invoice.</span></span> <span data-ttu-id="0865a-138">Jika Anda tidak memilih perusahaan, semua transaksi yang memenuhi kriteria pencarian akan ditampilkan untuk semua entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-138">If you don't select a company, all transactions that meet the search criteria are displayed for all borrowing legal entities.</span></span>
3. <span data-ttu-id="0865a-139">Di **Buat satu faktur per**, pilih apakah akan membuat faktur untuk transaksi antarperusahaan berdasarkan proyek atau berdasarkan entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-139">In **Create one invoice per**, select whether to create an invoice for intercompany transactions based on a project or based on a borrowing legal entity.</span></span>
4. <span data-ttu-id="0865a-140">Opsional: Untuk memilih proyek dan kontrak proyek tertentu untuk membuat faktur antarperusahaan, klik **Pilih**.</span><span class="sxs-lookup"><span data-stu-id="0865a-140">Optional: To select a specific project and project contract to create intercompany invoices for, click **Select**.</span></span> <span data-ttu-id="0865a-141">Pada halaman **Pertanyaan**, di bidang **Kriteria**, pilih kontrak proyek, nomor proyek, atau keduanya, lalu pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="0865a-141">On the **Inquiry** page, in the **Criteria** field, select the project contract, project number, or both, and then select **OK**.</span></span>
5. <span data-ttu-id="0865a-142">Pada tab **Batch**, konfigurasikan proses batch untuk membuat faktur antarperusahaan secara berulang.</span><span class="sxs-lookup"><span data-stu-id="0865a-142">On the **Batch** tab, set up a batch process to create intercompany invoices on a recurring basis.</span></span> <span data-ttu-id="0865a-143">Untuk informasi lebih lanjut, lihat [Mengirimkan pekerjaan pemrosesan batch dari formulir](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span><span class="sxs-lookup"><span data-stu-id="0865a-143">For more information, see [Submit a batch processing job from a form](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/submit-a-batch-processing-job-from-a-form).</span></span>
6. <span data-ttu-id="0865a-144">Untuk memposting faktur antarperusahaan, pada Panel Tindakan, pilih **Posting**.</span><span class="sxs-lookup"><span data-stu-id="0865a-144">To post the intercompany invoices, on the Action Pane, select **Post**.</span></span>

> [!NOTE]
> <span data-ttu-id="0865a-145">Jika organisasi Anda mewajibkan faktur antarperusahaan ditinjau sebelum diposting, administrator sistem dapat mengonfigurasikan alur kerja untuk faktur antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="0865a-145">If your organization requires intercompany invoices be reviewed before they are posted, a system administrator might set up a workflow for intercompany invoices.</span></span> <span data-ttu-id="0865a-146">Jika alur kerja tidak dikonfigurasi untuk faktur antarperusahaan, Anda dapat mengirim faktur antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="0865a-146">If a workflow is not set up for intercompany invoices, you can post the intercompany invoices.</span></span>

## <a name="post-the-intercompany-vendor-invoice"></a><span data-ttu-id="0865a-147">Memposting faktur vendor antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="0865a-147">Post the intercompany vendor invoice</span></span>

<span data-ttu-id="0865a-148">Akuntan proyek di entitas hukum peminjam dapat meninjau faktur vendor antarperusahaan yang tertunda saat faktur pelanggan antarperusahaan terkait diposting.</span><span class="sxs-lookup"><span data-stu-id="0865a-148">A project accountant in the borrowing legal entity can review intercompany pending vendor invoices when the corresponding intercompany customer invoice is posted.</span></span> <span data-ttu-id="0865a-149">Di Keuangan, di entitas hukum peminjam, buka **Utang dagang** > **Faktur** > **Faktur tertunda vendor**.</span><span class="sxs-lookup"><span data-stu-id="0865a-149">In Finance, in the borrowing legal entity, go to **Accounts payable** > **Invoices** > **Pending vendor invoice**.</span></span> <span data-ttu-id="0865a-150">Nomor faktur tertunda faktur akan cocok dengan nomor faktur pelanggan antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="0865a-150">The pending invoice number will match the intercompany customer invoice number.</span></span> <span data-ttu-id="0865a-151">Verifikasikan bahwa faktur sudah benar, lalu posting faktur.</span><span class="sxs-lookup"><span data-stu-id="0865a-151">Verify that the invoice is correct and then post the invoice.</span></span> <span data-ttu-id="0865a-152">Memposting faktur vendor antarperusahaan akan menghasilkan subbuku besar proyek dan transaksi buku besar yang menunjukkan biaya transaksi di entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="0865a-152">Posting intercompany vendor invoice creates a project subledger and a general ledger transaction that reflects the transaction costs in the borrowing legal entity.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
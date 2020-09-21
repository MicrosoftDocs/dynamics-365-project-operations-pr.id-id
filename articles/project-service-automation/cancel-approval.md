---
title: Membatalkan entri waktu dan biaya yang disetujui sebelumnya
description: Topik ini menyediakan informasi tentang cara membatalkan transaksi waktu dan biaya proyek yang disetujui.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752350"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="c68fd-103">Membatalkan entri waktu dan biaya atau disetujui sebelumnya</span><span class="sxs-lookup"><span data-stu-id="c68fd-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c68fd-104">Di versi terbaru Dynamics 365 Project Service Automation, pemberi persetujuan dapat membatalkan entri waktu atau biaya yang telah disetujui sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="c68fd-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="c68fd-105">Membatalkan entri waktu dan biaya atau disetujui sebelumnya</span><span class="sxs-lookup"><span data-stu-id="c68fd-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="c68fd-106">Ikuti langkah berikut untuk membatalkan entri waktu atau biaya yang sebelumnya disetujui.</span><span class="sxs-lookup"><span data-stu-id="c68fd-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="c68fd-107">Buka **proyek** \> **Pekerjaan Saya** \> **Persetujuan**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="c68fd-108">Di halaman daftar **persetujuan**, Ubah tampilan menjadi **persetujuan saya sebelumnya**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="c68fd-109">Daftar entri waktu dan pengeluaran yang telah disetujui sebelumnya ditampilkan.</span><span class="sxs-lookup"><span data-stu-id="c68fd-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="c68fd-110">Pilih satu entri atau lebih, lalu pilih **Batalkan persetujuan**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="c68fd-111">Anda menerima pesan peringatan.</span><span class="sxs-lookup"><span data-stu-id="c68fd-111">You receive a warning message.</span></span>
4. <span data-ttu-id="c68fd-112">Untuk membatalkan persetujuan, pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="c68fd-113">Memahami dampak membatalkan waktu atau persetujuan entri biaya</span><span class="sxs-lookup"><span data-stu-id="c68fd-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="c68fd-114">Bila persetujuan dibatalkan, ada dampak operasional dan dampak keuangan.</span><span class="sxs-lookup"><span data-stu-id="c68fd-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="c68fd-115">Dampak operasional</span><span class="sxs-lookup"><span data-stu-id="c68fd-115">Operational impact</span></span>

<span data-ttu-id="c68fd-116">Di sisi operasi, saat persetujuan dibatalkan, status rekaman diatur ulang ke **draf**, dan persetujuan tidak lagi muncul di tampilan **persetujuan saya sebelumnya**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="c68fd-117">Namun, persetujuan yang dibatalkan ditampilkan di tampilan **entri waktu untuk persetujuan** maupun tampilan **entri pengeluaran untuk persetujuan**, tergantung pada apakah itu entri waktu atau entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="c68fd-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="c68fd-118">Selain itu, status entri waktu atau pengeluaran terkait diubah ke **Diajukan**, sehingga entri terkait sesuai dengan persetujuan yang memiliki status **draf**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="c68fd-119">Sebagai pemberi izin, Anda dapat mengedit beberapa bidang persetujuan yang memiliki status **draf**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="c68fd-120">Bidang ini mencakup **jenis penagihan** dan **jam yang dapat ditagih untuk entri waktu**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="c68fd-121">Setelah membuat perubahan, Anda dapat menyetujui kembali rekaman.</span><span class="sxs-lookup"><span data-stu-id="c68fd-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="c68fd-122">Atau, Anda dapat menolak entri.</span><span class="sxs-lookup"><span data-stu-id="c68fd-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="c68fd-123">Jika Anda menolak persetujuan untuk entri waktu, status entri akan diubah menjadi **dikembalikan**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="c68fd-124">Jika Anda menolak persetujuan untuk entri pengeluaran, status akan diubah menjadi **Ditolak**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="c68fd-125">Secara fungsional, entri yang dikembalikan dan ditolak akan berfungsi sama seperti entri yang memiliki status **draf**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="c68fd-126">Anggota tim proyek dapat membuat perubahan yang diperlukan pada entri dan kemudian mengirimkannya kembali untuk disetujui, atau menghapus seluruh entri.</span><span class="sxs-lookup"><span data-stu-id="c68fd-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="c68fd-127">Dampak keuangan</span><span class="sxs-lookup"><span data-stu-id="c68fd-127">Financial impact</span></span>

<span data-ttu-id="c68fd-128">Proyek juga terpengaruh secara finansial saat persetujuan dibatalkan.</span><span class="sxs-lookup"><span data-stu-id="c68fd-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="c68fd-129">Pertama, aktual yang sesuai untuk biaya dan penjualan diperbarui dengan cara berikut:</span><span class="sxs-lookup"><span data-stu-id="c68fd-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="c68fd-130">Status penyesuaian diatur ke **disesuaikan**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="c68fd-131">Status penagihan diatur ke **Dibatalkan**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="c68fd-132">Selanjutnya, entri pembalikan dibuat di dalam tabel aktual.</span><span class="sxs-lookup"><span data-stu-id="c68fd-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="c68fd-133">Untuk membuat entri pembalikan, sistem menyalin nilai bidang dari aktual asli.</span><span class="sxs-lookup"><span data-stu-id="c68fd-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="c68fd-134">Hanya nilai yang tidak disalin adalah nilai kuantitas.</span><span class="sxs-lookup"><span data-stu-id="c68fd-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="c68fd-135">Nilai ini dibalik sebagai gantinya.</span><span class="sxs-lookup"><span data-stu-id="c68fd-135">These values are reversed instead.</span></span> <span data-ttu-id="c68fd-136">Aktual terbalik dibuat untuk aktual **biaya** dan **penjualan tidak ditagih**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="c68fd-137">Bidang **status penyesuaian** pada aktual terbalik diatur ke **tidak dapat disesuaikan**, dan status penagihan diatur ke **dibatalkan**.</span><span class="sxs-lookup"><span data-stu-id="c68fd-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="c68fd-138">Setelah perubahan ini dibuat, jumlah yang tercatat sebagai dibelanjakan pada proyek dan akumulasi pendapatan pada proyek tidak mempertimbangkan lagi jumlah yang diwakili oleh aktual ini.</span><span class="sxs-lookup"><span data-stu-id="c68fd-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>

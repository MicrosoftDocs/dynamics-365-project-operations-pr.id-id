---
title: Entri pengeluaran (sederhana)
description: Topik ini menyediakan informasi tentang cara menangani entri pengeluaran di penyebaran sederhana.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078368"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="1e284-103">Entri pengeluaran (sederhana)</span><span class="sxs-lookup"><span data-stu-id="1e284-103">Expense entry (lite)</span></span>

<span data-ttu-id="1e284-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="1e284-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1e284-105">Basic, atau Lite, manajemen pengeluaran adalah kemampuan untuk merekam biaya sederhana.</span><span class="sxs-lookup"><span data-stu-id="1e284-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="1e284-106">Anda dapat merekam biaya terhadap proyek, dan kemudian pemberi izin proyek akan meninjau dan menyetujuinya.</span><span class="sxs-lookup"><span data-stu-id="1e284-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="1e284-107">Untuk informasi lebih lanjut tentang kemampuan pengeluaran di Dynamics 365 Project Operations, lihat [Ikhtisar pengeluaran](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="1e284-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="1e284-108">Mengambil biaya dasar</span><span class="sxs-lookup"><span data-stu-id="1e284-108">Capture a basic expense</span></span>

<span data-ttu-id="1e284-109">Anda dapat mengambil pengeluaran Anda sehingga Anda dapat mengirimkannya ke pemberi izin.</span><span class="sxs-lookup"><span data-stu-id="1e284-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="1e284-110">Buka **pengeluaran** , lalu pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="1e284-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="1e284-111">Pada halaman **pengeluaran baru** , masukkan informasi pengeluaran yang diperlukan, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="1e284-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="1e284-112">Ajukan pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="1e284-112">Submit a basic expense</span></span>

<span data-ttu-id="1e284-113">Setelah selesai menangkap semua pengeluaran, dan siap disetujui, Anda harus menyerahkannya.</span><span class="sxs-lookup"><span data-stu-id="1e284-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="1e284-114">Buka **pengeluaran** , lalu pilih pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="1e284-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="1e284-115">Atau, pilih semua pengeluaran menggunakan kotak centang di header.</span><span class="sxs-lookup"><span data-stu-id="1e284-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="1e284-116">Pilih **kirim**.</span><span class="sxs-lookup"><span data-stu-id="1e284-116">Select **Submit**.</span></span> <span data-ttu-id="1e284-117">Sistem memproses entri yang dipilih dan kemudian membuat permintaan persetujuan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="1e284-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="1e284-118">Tarik pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="1e284-118">Recall a basic expense</span></span>

<span data-ttu-id="1e284-119">Bila Anda mengirimkan pengeluaran secara tidak sengaja, Anda dapat menariknya.</span><span class="sxs-lookup"><span data-stu-id="1e284-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="1e284-120">Waktu yang diperlukan untuk menarik entri pengeluaran tergantung pada tingkat persetujuannya.</span><span class="sxs-lookup"><span data-stu-id="1e284-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="1e284-121">Jika pemberi izin belum menyetujui entri, penarikan dapat terjadi segera.</span><span class="sxs-lookup"><span data-stu-id="1e284-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="1e284-122">Namun, jika entri telah disetujui, pemberi izin diminta untuk menyetujui penarikan dan membalikkan transaksi.</span><span class="sxs-lookup"><span data-stu-id="1e284-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="1e284-123">Buka **pengeluaran** , lalu, dalam daftar pengeluaran, pilih biaya yang akan ditarik.</span><span class="sxs-lookup"><span data-stu-id="1e284-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="1e284-124">Pilih **Tarik**.</span><span class="sxs-lookup"><span data-stu-id="1e284-124">Select **Recall**.</span></span> <span data-ttu-id="1e284-125">Jika entri biaya belum disetujui, sistem segera akan menariknya.</span><span class="sxs-lookup"><span data-stu-id="1e284-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="1e284-126">Jika entri pengeluaran telah disetujui, permintaan penarikan dibuat untuk memberi tahu pemberi persetujuan bahwa Anda ingin membalikkan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="1e284-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="1e284-127">Pemberi persetujuan kemudian akan mengkonfirmasi bahwa pembalikan dapat dilakukan, dan entri akan dikembalikan.</span><span class="sxs-lookup"><span data-stu-id="1e284-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="1e284-128">Menghapus pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="1e284-128">Delete a basic expense</span></span>

<span data-ttu-id="1e284-129">Pengeluaran yang belum diajukan dapat dihapus.</span><span class="sxs-lookup"><span data-stu-id="1e284-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="1e284-130">Untuk menghapus pengeluaran yang telah dikirim, Anda harus menariknya terlebih dahulu.</span><span class="sxs-lookup"><span data-stu-id="1e284-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="1e284-131">Lihat juga</span><span class="sxs-lookup"><span data-stu-id="1e284-131">See also</span></span>

- [<span data-ttu-id="1e284-132">Sekilas persetujuan</span><span class="sxs-lookup"><span data-stu-id="1e284-132">Approvals overview</span></span>](../approvals/approvals-overview.md)

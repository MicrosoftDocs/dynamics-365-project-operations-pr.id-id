---
title: Mengonfigurasi kebijakan pengeluaran
description: Anda dapat membuat kebijakan pengeluaran yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan di Microsoft Dynamics 365 Finance.
author: suvaidya
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fa4f628a918e6e099a723ed05994f63d6ad847f5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005750"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="b9f13-103">Mengonfigurasi kebijakan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="b9f13-103">Set up expense policies</span></span>

<span data-ttu-id="b9f13-104">Anda dapat menentukan kebijakan yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan.</span><span class="sxs-lookup"><span data-stu-id="b9f13-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="b9f13-105">Mengimplementasikan kebijakan pengeluaran dapat membantu Anda mengelola pengeluaran secara efektif.</span><span class="sxs-lookup"><span data-stu-id="b9f13-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="b9f13-106">Misalnya, Anda dapat mengatur kebijakan untuk pengeluaran Hotel di New York City, yang menyatakan bahwa pengeluaran per malam tidak dapat melebihi USD 250.</span><span class="sxs-lookup"><span data-stu-id="b9f13-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="b9f13-107">Jika pekerja mengirimkan laporan pengeluaran atau permintaan perjalanan dengan tarif kamar melebihi jumlah ini, sistem akan memberi tahu</span><span class="sxs-lookup"><span data-stu-id="b9f13-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="b9f13-108">Pekerja bahwa jumlah kebijakan untuk pengeluaran telah terlampaui.</span><span class="sxs-lookup"><span data-stu-id="b9f13-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="b9f13-109">Anda dapat mengkonfigurasi pesan yang akan diterima oleh pekerja</span><span class="sxs-lookup"><span data-stu-id="b9f13-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="b9f13-110">menentukan kebijakan.</span><span class="sxs-lookup"><span data-stu-id="b9f13-110">define the policy.</span></span>      
        
<span data-ttu-id="b9f13-111">Anda dapat menentukan tiga jenis kebijakan:</span><span class="sxs-lookup"><span data-stu-id="b9f13-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="b9f13-112">Peringatan – memungkinkan pekerja untuk mengirimkan laporan pengeluaran atau permintaan perjalanan namun pengeluarannya akan ditandai untuk semua pemberi izin dan</span><span class="sxs-lookup"><span data-stu-id="b9f13-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="b9f13-113">Untuk pelaporan selanjutnya.</span><span class="sxs-lookup"><span data-stu-id="b9f13-113">for later reporting.</span></span>        

- <span data-ttu-id="b9f13-114">Kesalahan – mengharuskan pekerja untuk merevisi biaya untuk mematuhi kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="b9f13-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="b9f13-115">Pembenaran – memerlukan pekerja atau manajer untuk memasukkan pembenaran untuk melampaui jumlah kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="b9f13-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="b9f13-116">Tips kebijakan</span><span class="sxs-lookup"><span data-stu-id="b9f13-116">Policy tips</span></span>
<span data-ttu-id="b9f13-117">Berikut adalah beberapa saran yang dapat membantu Anda ketika membuat kebijakan baru untuk manajemen pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="b9f13-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="b9f13-118">Kebijakan adalah tanggal efektif dan tidak akan berlaku jika kebijakan dibuat dengan tanggal setelah tanggal pengeluaran terjadi.</span><span class="sxs-lookup"><span data-stu-id="b9f13-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="b9f13-119">Misalnya, jika Anda membuat kebijakan baru hari ini untuk memberlakukan biaya makan maksimum $50, maka setiap biaya yang ada yang dimasukkan kemarin tidak akan diperiksa terhadap kebijakan ini.</span><span class="sxs-lookup"><span data-stu-id="b9f13-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="b9f13-120">Saat membuat kebijakan untuk kategori pengeluaran yang dapat diperinci, pertimbangkan menambahkan kondisi untuk jenis baris pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="b9f13-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="b9f13-121">Beberapa kebijakan seperti memerlukan tanda terima mungkin tidak masuk akal untuk baris yang diperinci dan hanya dapat diterapkan ke baris header atau baris non-rinci.</span><span class="sxs-lookup"><span data-stu-id="b9f13-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="b9f13-122">Kebijakan manajemen pengeluaran dievaluasi terhadap entitas sumber secara default.</span><span class="sxs-lookup"><span data-stu-id="b9f13-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="b9f13-123">Untuk skenario antarperusahaan, Anda dapat mengatur kebijakan untuk dievaluasi terhadap entitas tujuan (entitas peminjam) sebagai gantinya.</span><span class="sxs-lookup"><span data-stu-id="b9f13-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="b9f13-124">Untuk menjalankan kebijakan terhadap entitas tujuan, Aktifkan fitur "Evaluasi kebijakan pengeluaran terhadap entitas hukum peminjaman" di ruang kerja **manajemen fitur**.</span><span class="sxs-lookup"><span data-stu-id="b9f13-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="b9f13-125">Kapan mengevaluasi kebijakan</span><span class="sxs-lookup"><span data-stu-id="b9f13-125">When to evaluate policies</span></span>

<span data-ttu-id="b9f13-126">Dalam parameter manajemen pengeluaran, ada opsi untuk mengevaluasi kebijakan manajemen pengeluaran bila baris disimpan atau saat laporan pengeluaran diajukan.</span><span class="sxs-lookup"><span data-stu-id="b9f13-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="b9f13-127">Jika Anda memilih untuk mengevaluasi bila baris disimpan, ini memastikan pengguna memiliki visibilitas sebelumnya ke apa yang perlu mereka lakukan untuk menyelesaikan laporan pengeluaran mereka sekaligus.</span><span class="sxs-lookup"><span data-stu-id="b9f13-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="b9f13-128">Jika tidak, Anda dapat menunda evaluasi kebijakan dan menghemat waktu jika Anda memiliki validasi yang terjadi di akhir, selama pengajuan ke alur kerja.</span><span class="sxs-lookup"><span data-stu-id="b9f13-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
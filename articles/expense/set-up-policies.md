---
title: Menentukan kebijakan pengeluaran
description: Anda dapat menentukan kebijakan pengeluaran yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan.
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
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128422"
---
# <a name="define-expense-policies"></a><span data-ttu-id="6569b-103">Menentukan kebijakan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="6569b-103">Define expense policies</span></span>

<span data-ttu-id="6569b-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="6569b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6569b-105">Anda dapat menentukan kebijakan yang harus diikuti pekerja Anda saat memasukkan dan mengirimkan laporan pengeluaran dan rekusisi perjalanan.</span><span class="sxs-lookup"><span data-stu-id="6569b-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="6569b-106">Mengimplementasikan kebijakan pengeluaran dapat membantu Anda mengelola pengeluaran secara efektif.</span><span class="sxs-lookup"><span data-stu-id="6569b-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="6569b-107">Misalnya, Anda dapat mengatur kebijakan untuk pengeluaran Hotel di New York City, yang menyatakan bahwa pengeluaran per malam tidak dapat melebihi USD 250.</span><span class="sxs-lookup"><span data-stu-id="6569b-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="6569b-108">Jika pekerja mengirimkan laporan pengeluaran atau permintaan perjalanan dengan tarif kamar melebihi jumlah ini, sistem akan memberi tahu</span><span class="sxs-lookup"><span data-stu-id="6569b-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="6569b-109">Pekerja bahwa jumlah kebijakan untuk pengeluaran telah terlampaui.</span><span class="sxs-lookup"><span data-stu-id="6569b-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="6569b-110">Anda dapat mengkonfigurasi pesan yang akan diterima oleh pekerja</span><span class="sxs-lookup"><span data-stu-id="6569b-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="6569b-111">menentukan kebijakan.</span><span class="sxs-lookup"><span data-stu-id="6569b-111">define the policy.</span></span>      
        
<span data-ttu-id="6569b-112">Anda dapat menentukan tiga jenis kebijakan:</span><span class="sxs-lookup"><span data-stu-id="6569b-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="6569b-113">**Peringatan**: memungkinkan pekerja untuk mengirimkan laporan pengeluaran atau permintaan perjalanan namun pengeluarannya akan ditandai untuk semua pemberi izin dan</span><span class="sxs-lookup"><span data-stu-id="6569b-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="6569b-114">Untuk pelaporan selanjutnya.</span><span class="sxs-lookup"><span data-stu-id="6569b-114">for later reporting.</span></span>        

- <span data-ttu-id="6569b-115">**Kesalahan**: mengharuskan pekerja untuk merevisi biaya untuk mematuhi kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="6569b-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="6569b-116">**Pembenaran**: memerlukan pekerja atau manajer untuk memasukkan pembenaran untuk melampaui jumlah kebijakan sebelum mengirimkan laporan pengeluaran atau permintaan perjalanan.</span><span class="sxs-lookup"><span data-stu-id="6569b-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="6569b-117">Tips kebijakan</span><span class="sxs-lookup"><span data-stu-id="6569b-117">Policy tips</span></span>
<span data-ttu-id="6569b-118">Berikut adalah beberapa saran yang dapat membantu Anda ketika membuat kebijakan baru untuk manajemen pengeluaran:</span><span class="sxs-lookup"><span data-stu-id="6569b-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="6569b-119">Kebijakan adalah tanggal efektif yang berarti kebijakan tidak akan berlaku jika dibuat dengan tanggal setelah tanggal pengeluaran terjadi.</span><span class="sxs-lookup"><span data-stu-id="6569b-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="6569b-120">Misalnya, Anda membuat kebijakan baru hari ini untuk memberlakukan pengeluaran makan maksimum $50.</span><span class="sxs-lookup"><span data-stu-id="6569b-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="6569b-121">Pengeluaran yang ada yang dimasukkan sebagai kemarin tidak akan diperiksa terhadap kebijakan ini.</span><span class="sxs-lookup"><span data-stu-id="6569b-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="6569b-122">Saat membuat kebijakan untuk kategori pengeluaran yang dapat diperinci, pertimbangkan menambahkan kondisi untuk jenis baris pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="6569b-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="6569b-123">Beberapa kebijakan, seperti memerlukan tanda terima, mungkin tidak masuk akal untuk baris terperinci.</span><span class="sxs-lookup"><span data-stu-id="6569b-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="6569b-124">Dalam situasi ini, kebijakan hanya diterapkan ke baris header atau baris non-itemisasi.</span><span class="sxs-lookup"><span data-stu-id="6569b-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="6569b-125">Kebijakan manajemen pengeluaran dievaluasi terhadap entitas sumber secara default.</span><span class="sxs-lookup"><span data-stu-id="6569b-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="6569b-126">Untuk skenario antarperusahaan, Anda dapat mengatur kebijakan untuk dievaluasi terhadap entitas tujuan (entitas peminjam) sebagai gantinya.</span><span class="sxs-lookup"><span data-stu-id="6569b-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="6569b-127">Untuk menjalankan kebijakan terhadap entitas tujuan, Aktifkan fitur **Evaluasi kebijakan pengeluaran terhadap entitas hukum peminjaman** di ruang kerja **manajemen fitur**.</span><span class="sxs-lookup"><span data-stu-id="6569b-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="6569b-128">Kapan mengevaluasi kebijakan</span><span class="sxs-lookup"><span data-stu-id="6569b-128">When to evaluate policies</span></span>

<span data-ttu-id="6569b-129">Dalam parameter manajemen pengeluaran, Anda dapat memilih untuk mengevaluasi kebijakan manajemen pengeluaran bila baris disimpan atau saat laporan pengeluaran diajukan.</span><span class="sxs-lookup"><span data-stu-id="6569b-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="6569b-130">Jika Anda memilih untuk mengevaluasi bila baris disimpan, pengguna akan memiliki visibilitas sebelumnya ke apa yang perlu mereka lakukan untuk menyelesaikan laporan pengeluaran mereka sekaligus.</span><span class="sxs-lookup"><span data-stu-id="6569b-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="6569b-131">Jika tidak, Anda dapat menunda evaluasi kebijakan dan menghemat waktu dengan memvalidasi di akhir, selama pengajuan ke alur kerja.</span><span class="sxs-lookup"><span data-stu-id="6569b-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>

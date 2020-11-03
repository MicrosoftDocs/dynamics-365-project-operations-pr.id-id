---
title: Mengkonfigurasi alur kerja untuk manajemen pengeluaran
description: Anda dapat mengkonfigurasi proses alur kerja yang digunakan untuk meninjau dan menyetujui dokumen perjalanan dan pengeluaran.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078511"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="83805-103">Mengkonfigurasi alur kerja untuk manajemen pengeluaran</span><span class="sxs-lookup"><span data-stu-id="83805-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="83805-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="83805-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="83805-105">Anda dapat mengkonfigurasi proses alur kerja untuk meninjau dan menyetujui dokumen perjalanan dan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="83805-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="83805-106">Anda dapat menentukan alur kerja untuk laporan pengeluaran, rekuisisi perjalanan, dan permintaan uang muka.</span><span class="sxs-lookup"><span data-stu-id="83805-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="83805-107">Alur kerja menunjukkan proses bisnis dan menentukan bagaimana suatu dokumen mengalir melalui sistem.</span><span class="sxs-lookup"><span data-stu-id="83805-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="83805-108">Alur kerja juga menunjukkan siapa yang harus menyelesaikan tugas atau menyetujui dokumen.</span><span class="sxs-lookup"><span data-stu-id="83805-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="83805-109">Ada beberapa manfaat menggunakan sistem alur kerja di organisasi Anda:</span><span class="sxs-lookup"><span data-stu-id="83805-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="83805-110">**Proses yang konsisten** : Anda dapat menentukan proses persetujuan untuk dokumen tertentu, seperti rekusisi pembelian dan laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="83805-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="83805-111">Menggunakan sistem alur kerja membantu memastikan bahwa dokumen diproses dan disetujui secara konsisten dan efisien.</span><span class="sxs-lookup"><span data-stu-id="83805-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="83805-112">**Visibilitas proses** : Anda dapat melacak metrik status, riwayat, dan performa instans alur kerja tertentu.</span><span class="sxs-lookup"><span data-stu-id="83805-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="83805-113">Ini akan membantu Anda menentukan apakah perubahan harus dibuat untuk alur kerja untuk meningkatkan efisiensi.</span><span class="sxs-lookup"><span data-stu-id="83805-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="83805-114">**Daftar kerja tersentralisasi** : pengguna dapat melihat daftar kerja tersentralisasi untuk melihat tugas dan persetujuan alur kerja yang ditetapkan ke mereka.</span><span class="sxs-lookup"><span data-stu-id="83805-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="83805-115">Jenis alur kerja</span><span class="sxs-lookup"><span data-stu-id="83805-115">Workflow types</span></span>

<span data-ttu-id="83805-116">Tabel berikut mencantumkan jenis alur kerja yang dapat Anda buat di **manajemen pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="83805-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="83805-117"><strong>Jenis</strong></span><span class="sxs-lookup"><span data-stu-id="83805-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="83805-118"><strong>Gunakan jenis ini untuk</strong></span><span class="sxs-lookup"><span data-stu-id="83805-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="83805-119"><strong>Persetujuan otomatis laporan pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="83805-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="83805-120">Membuat alur kerja persetujuan untuk laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="83805-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="83805-121"><strong>Memposting otomatis laporan pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="83805-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="83805-122">Membuat alur kerja posting otomatis untuk laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="83805-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="83805-123"><strong>Item baris pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="83805-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="83805-124">Membuat alur kerja persetujuan untuk item baris pada laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="83805-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="83805-125"><strong>posting otomatis item baris Pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="83805-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="83805-126">Membuat alur kerja posting otomatis untuk item baris pada laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="83805-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="83805-127"><strong>Permintaan perjalanan</strong></span><span class="sxs-lookup"><span data-stu-id="83805-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="83805-128">Buat alur kerja persetujuan untuk rekusisi perjalanan.</span><span class="sxs-lookup"><span data-stu-id="83805-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="83805-129"><strong>Permintaan Uang muka</strong></span><span class="sxs-lookup"><span data-stu-id="83805-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="83805-130">Buat alur kerja persetujuan untuk permintaan uang muka.</span><span class="sxs-lookup"><span data-stu-id="83805-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="83805-131"><strong>Pemulihan PPN</strong></span><span class="sxs-lookup"><span data-stu-id="83805-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="83805-132">Buat alur kerja persetujuan untuk pemulihan pajak pertambahan nilai (PPN).</span><span class="sxs-lookup"><span data-stu-id="83805-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

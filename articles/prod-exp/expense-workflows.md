---
title: Mengonfigurasi alur kerja manajemen pengeluaran
description: Anda dapat mengkonfigurasi proses alur kerja untuk meninjau dan menyetujui dokumen perjalanan dan pengeluaran.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005120"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="f31b6-103">Mengonfigurasi alur kerja manajemen pengeluaran</span><span class="sxs-lookup"><span data-stu-id="f31b6-103">Set up Expense management workflows</span></span>

<span data-ttu-id="f31b6-104">Anda dapat mengkonfigurasi proses alur kerja yang digunakan untuk meninjau dan menyetujui dokumen perjalanan dan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f31b6-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="f31b6-105">Dokumen untuk menentukan alur kerja mencakup laporan pengeluaran, rekuisisi perjalanan, dan permintaan uang muka.</span><span class="sxs-lookup"><span data-stu-id="f31b6-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="f31b6-106">Alur kerja merupakan proses bisnis.</span><span class="sxs-lookup"><span data-stu-id="f31b6-106">A workflow represents a business process.</span></span> <span data-ttu-id="f31b6-107">Ia menentukan bagaimana suatu dokumen mengalir melalui sistem dan menunjukkan siapa yang harus menyelesaikan tugas atau menyetujui suatu dokumen.</span><span class="sxs-lookup"><span data-stu-id="f31b6-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="f31b6-108">Ada beberapa manfaat menggunakan sistem alur kerja di organisasi Anda:</span><span class="sxs-lookup"><span data-stu-id="f31b6-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="f31b6-109">**Proses yang konsisten** — Anda dapat menentukan proses persetujuan untuk dokumen tertentu, seperti rekusisi pembelian dan laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f31b6-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="f31b6-110">Menggunakan sistem alur kerja untuk membantu memastikan bahwa dokumen diproses dan disetujui secara konsisten dan efisien.</span><span class="sxs-lookup"><span data-stu-id="f31b6-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="f31b6-111">Visibilitas proses — Anda dapat melacak metrik status, riwayat, dan performa instans alur kerja tertentu.</span><span class="sxs-lookup"><span data-stu-id="f31b6-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="f31b6-112">Ini akan membantu Anda menentukan apakah perubahan harus dibuat untuk alur kerja untuk meningkatkan efisiensi.</span><span class="sxs-lookup"><span data-stu-id="f31b6-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="f31b6-113">Daftar kerja tersentralisasi — pengguna dapat melihat daftar kerja tersentralisasi untuk melihat tugas dan persetujuan alur kerja yang ditetapkan ke mereka.</span><span class="sxs-lookup"><span data-stu-id="f31b6-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="f31b6-114">**Jenis alur kerja yang bisa Anda buat**</span><span class="sxs-lookup"><span data-stu-id="f31b6-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="f31b6-115">Tabel berikut mencantumkan jenis alur kerja yang dapat Anda buat di **pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="f31b6-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="f31b6-116"><strong>Jenis</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="f31b6-117"><strong>Gunakan jenis ini untuk</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="f31b6-118"><strong>Laporan pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="f31b6-119">Membuat alur kerja persetujuan untuk laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f31b6-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="f31b6-120"><strong>Memposting otomatis laporan pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="f31b6-121">Membuat alur kerja posting otomatis untuk laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f31b6-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="f31b6-122"><strong>Item baris pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="f31b6-123">Membuat alur kerja persetujuan untuk item baris pada laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f31b6-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="f31b6-124"><strong>posting otomatis item baris Pengeluaran</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="f31b6-125">Membuat alur kerja posting otomatis untuk item baris pada laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f31b6-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="f31b6-126"><strong>Permintaan perjalanan</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="f31b6-127">Buat alur kerja persetujuan untuk rekusisi perjalanan.</span><span class="sxs-lookup"><span data-stu-id="f31b6-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="f31b6-128"><strong>Permintaan Uang muka</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="f31b6-129">Buat alur kerja persetujuan untuk permintaan uang muka.</span><span class="sxs-lookup"><span data-stu-id="f31b6-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="f31b6-130"><strong>Pemulihan PPN</strong></span><span class="sxs-lookup"><span data-stu-id="f31b6-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="f31b6-131">Buat alur kerja persetujuan untuk pemulihan pajak pertambahan nilai (PPN).</span><span class="sxs-lookup"><span data-stu-id="f31b6-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
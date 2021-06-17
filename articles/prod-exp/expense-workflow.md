---
title: Alur kerja manajemen pengeluaran
description: Topik ini menjelaskan cara menggunakan sistem alur kerja di Microsoft Dynamics 365 Finance, untuk mengkonfigurasi proses peninjauan untuk laporan pengeluaran dalam manajemen pengeluaran.
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
ms.openlocfilehash: 51ac2712f62d5c5d85b21c0ea929517ccb893bca
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005210"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="4c56d-103">Alur kerja manajemen pengeluaran</span><span class="sxs-lookup"><span data-stu-id="4c56d-103">Expense management workflow</span></span>

<span data-ttu-id="4c56d-104">Anda dapat menggunakan sistem alur kerja untuk mengkonfigurasi proses peninjauan untuk laporan pengeluaran dalam manajemen pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4c56d-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="4c56d-105">Anda dapat mengkonfigurasi alur kerja yang menggunakan kriteria berikut untuk menentukan orang yang menyetujui laporan pengeluaran:</span><span class="sxs-lookup"><span data-stu-id="4c56d-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="4c56d-106">Hierarki pelaporan karyawan dan batas persetujuan yang telah ditetapkan sebelumnya</span><span class="sxs-lookup"><span data-stu-id="4c56d-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="4c56d-107">Persetujuan multi-level yang mendukung pemberi persetujuan dan pemberi persetujuan akhir</span><span class="sxs-lookup"><span data-stu-id="4c56d-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="4c56d-108">Dimensi keuangan dan tanggung jawab proyek</span><span class="sxs-lookup"><span data-stu-id="4c56d-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="4c56d-109">Penetapan ke pengguna atau grup pengguna tertentu</span><span class="sxs-lookup"><span data-stu-id="4c56d-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="4c56d-110">Persetujuan alur kerja dapat dibuat untuk laporan pengeluaran, permintaan perjalanan, uang tunai, dan pemulihan pajak pertambahan nilai (PPN).</span><span class="sxs-lookup"><span data-stu-id="4c56d-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="4c56d-111">**Contoh**</span><span class="sxs-lookup"><span data-stu-id="4c56d-111">**Example**</span></span>

<span data-ttu-id="4c56d-112">Proses berikut ini adalah contoh alur kerja manajemen pengeluaran untuk laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4c56d-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="4c56d-113">Karyawan membuat dan menyimpan laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4c56d-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="4c56d-114">Karyawan mengajukan laporan pengeluaran untuk persetujuan.</span><span class="sxs-lookup"><span data-stu-id="4c56d-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="4c56d-115">Pemberi persetujuan diidentifikasi berdasarkan aturan yang ditentukan saat alur kerja disiapkan.</span><span class="sxs-lookup"><span data-stu-id="4c56d-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="4c56d-116">Pemberi persetujuan menerima pemberitahuan bahwa laporan pengeluaran siap untuk disetujui.</span><span class="sxs-lookup"><span data-stu-id="4c56d-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="4c56d-117">Pemberi persetujuan akan memeriksa laporan pengeluaran dan memverifikasi bahwa kondisi berikut terpenuhi:</span><span class="sxs-lookup"><span data-stu-id="4c56d-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="4c56d-118">pengeluaran tidak melanggar kebijakan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4c56d-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="4c56d-119">Jika pengeluaran melanggar kebijakan, pemberi izin memverifikasi bahwa laporan pengeluaran mencakup pembenaran bisnis yang valid.</span><span class="sxs-lookup"><span data-stu-id="4c56d-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="4c56d-120">Tanda terima elektronik dilampirkan ke laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4c56d-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="4c56d-121">Pemberi persetujuan menyetujui laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4c56d-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="4c56d-122">Laporan pengeluaran ditetapkan ke Koordinator utang dagang untuk posting.</span><span class="sxs-lookup"><span data-stu-id="4c56d-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="4c56d-123">Salah satu langkah berikut terjadi, tergantung pada apakah posting otomatis dikonfigurasi:</span><span class="sxs-lookup"><span data-stu-id="4c56d-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="4c56d-124">Jika posting otomatis dikonfigurasi, laporan pengeluaran diproses untuk pembayaran, dan status laporan pengeluaran diperbarui.</span><span class="sxs-lookup"><span data-stu-id="4c56d-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="4c56d-125">Jika posting otomatis tidak dikonfigurasi, Koordinator utang dagang akan memverifikasi bahwa semua tanda terima asli telah dikirim dan bahwa tanda terima disesuaikan dengan pengeluaran di laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="4c56d-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="4c56d-126">Semua kode pajak yang dimasukkan pada laporan pengeluaran juga harus diverifikasi sebagai benar.</span><span class="sxs-lookup"><span data-stu-id="4c56d-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="4c56d-127">Setelah persyaratan ini diverifikasi, laporan pengeluaran akan dikirim.</span><span class="sxs-lookup"><span data-stu-id="4c56d-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="4c56d-128">Setelah laporan pengeluaran dikirim, pembayaran disahkan untuk laporan pengeluaran, dan uang karyawan akan diganti.</span><span class="sxs-lookup"><span data-stu-id="4c56d-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
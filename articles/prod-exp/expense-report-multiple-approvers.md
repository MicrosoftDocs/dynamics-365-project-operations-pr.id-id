---
title: Beberapa pemberi persetujuan pada laporan pengeluaran
description: Topik ini menyediakan informasi tentang laporan pengeluaran yang memerlukan persetujuan dari beberapa orang.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960611"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="d101f-103">Beberapa pemberi persetujuan pada laporan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="d101f-103">Multiple approvers on an expense report</span></span>

<span data-ttu-id="d101f-104">Tergantung pada kebijakan persetujuan pengeluaran organisasi Anda, lebih dari satu orang mungkin harus menyetujui laporan pengeluaran yang diajukan oleh seorang karyawan.</span><span class="sxs-lookup"><span data-stu-id="d101f-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="d101f-105">Bila Anda mengkonfigurasi proses alur kerja untuk persetujuan laporan pengeluaran, Anda dapat menambahkan elemen alur kerja yang mencakup tugas atau langkah-langkah untuk satu pemberi izin laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="d101f-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="d101f-106">Misalnya, Anda mungkin mengharuskan semua laporan biaya disetujui pertama oleh manajer karyawan yang mengajukan laporan dan kemudian oleh koordinator utang dagang.</span><span class="sxs-lookup"><span data-stu-id="d101f-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="d101f-107">Jika Anda memutuskan untuk meminta beberapa penyetuju laporan pengeluaran, Anda dapat menambahkan elemen alur kerja dengan salah satu cara berikut:</span><span class="sxs-lookup"><span data-stu-id="d101f-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="d101f-108">Tambahkan satu elemen persetujuan yang memiliki satu langkah.</span><span class="sxs-lookup"><span data-stu-id="d101f-108">Add one approval element that has one step.</span></span> <span data-ttu-id="d101f-109">Misalnya, langkah ini mungkin memerlukan laporan pengeluaran yang ditetapkan ke grup pengguna, dan bahwa laporan tersebut disetujui oleh 50 persen dari anggota grup pengguna.</span><span class="sxs-lookup"><span data-stu-id="d101f-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="d101f-110">Tambahkan satu elemen persetujuan yang memiliki beberapa langkah.</span><span class="sxs-lookup"><span data-stu-id="d101f-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="d101f-111">Misalnya, elemen persetujuan mungkin memiliki langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="d101f-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="d101f-112">Manajer karyawan yang mengajukan laporan pengeluaran menyetujuinya.</span><span class="sxs-lookup"><span data-stu-id="d101f-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="d101f-113">Petugas utang dagang memverifikasi tanda terima dan item laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="d101f-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="d101f-114">Pemilik anggaran menyetujui laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="d101f-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="d101f-115">Tambahkan beberapa elemen persetujuan, yang masing-masing memiliki satu langkah.</span><span class="sxs-lookup"><span data-stu-id="d101f-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="d101f-116">Misalnya, Anda dapat menambahkan elemen persetujuan terpisah untuk setiap langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="d101f-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="d101f-117">Manajer karyawan menyetujui laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="d101f-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="d101f-118">Pemilik anggaran menyetujui laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="d101f-118">The budget owner approves the expense report.</span></span>

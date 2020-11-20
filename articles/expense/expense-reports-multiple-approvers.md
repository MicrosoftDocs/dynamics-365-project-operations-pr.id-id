---
title: Laporan pengeluaran dan beberapa pemberi izin
description: Topik ini menyediakan informasi tentang laporan pengeluaran yang memerlukan persetujuan dari lebih dari satu orang.
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
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120997"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="f8abe-103">Laporan pengeluaran dan beberapa pemberi izin</span><span class="sxs-lookup"><span data-stu-id="f8abe-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="f8abe-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="f8abe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f8abe-105">Tergantung pada kebijakan persetujuan pengeluaran organisasi Anda, lebih dari satu orang mungkin harus menyetujui laporan pengeluaran yang diajukan.</span><span class="sxs-lookup"><span data-stu-id="f8abe-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="f8abe-106">Bila Anda mengkonfigurasi proses alur kerja untuk persetujuan laporan pengeluaran, Anda dapat menambahkan elemen alur kerja yang mencakup tugas atau langkah-langkah untuk satu pemberi izin laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f8abe-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="f8abe-107">Misalnya, Anda mungkin mengharuskan semua laporan biaya disetujui oleh dua orang terpisah, manajer karyawan yang mengajukan laporan dan koordinator utang dagang.</span><span class="sxs-lookup"><span data-stu-id="f8abe-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="f8abe-108">Jika Anda memutuskan untuk meminta beberapa penyetuju laporan pengeluaran, Anda dapat menambahkan elemen alur kerja dengan salah satu cara berikut:</span><span class="sxs-lookup"><span data-stu-id="f8abe-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="f8abe-109">Tambahkan satu elemen persetujuan yang memiliki satu langkah.</span><span class="sxs-lookup"><span data-stu-id="f8abe-109">Add one approval element that has one step.</span></span> <span data-ttu-id="f8abe-110">Misalnya, langkah ini mungkin memerlukan laporan pengeluaran yang ditetapkan ke grup pengguna, dan bahwa laporan tersebut disetujui oleh 50 persen dari anggota grup pengguna.</span><span class="sxs-lookup"><span data-stu-id="f8abe-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="f8abe-111">Tambahkan satu elemen persetujuan yang memiliki beberapa langkah.</span><span class="sxs-lookup"><span data-stu-id="f8abe-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="f8abe-112">Misalnya, elemen persetujuan mungkin memiliki langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="f8abe-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="f8abe-113">Manajer karyawan yang mengajukan laporan pengeluaran menyetujuinya.</span><span class="sxs-lookup"><span data-stu-id="f8abe-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="f8abe-114">Petugas utang dagang memverifikasi tanda terima dan item laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f8abe-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="f8abe-115">Pemilik anggaran menyetujui laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f8abe-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="f8abe-116">Tambahkan beberapa elemen persetujuan, yang masing-masing memiliki satu langkah.</span><span class="sxs-lookup"><span data-stu-id="f8abe-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="f8abe-117">Misalnya, Anda dapat menambahkan elemen persetujuan terpisah untuk setiap langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="f8abe-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="f8abe-118">Manajer karyawan menyetujui laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f8abe-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="f8abe-119">Pemilik anggaran menyetujui laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="f8abe-119">The budget owner approves the expense report.</span></span>

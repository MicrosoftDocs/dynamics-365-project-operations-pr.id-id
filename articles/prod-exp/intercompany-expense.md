---
title: Pengeluaran antarperusahaan
description: Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama. Dalam situasi ini, Anda dapat menggunakan fitur biaya antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum pekerjaan yang dilakukan.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078635"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="f413b-104">Pengeluaran antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="f413b-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f413b-105">Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama.</span><span class="sxs-lookup"><span data-stu-id="f413b-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="f413b-106">Dalam situasi ini, Anda dapat menggunakan fitur biaya antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum pekerjaan yang dilakukan.</span><span class="sxs-lookup"><span data-stu-id="f413b-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="f413b-107">Badan hukum yang mempekerjakan pekerja disebut entitas hukum pemberi pinjaman.</span><span class="sxs-lookup"><span data-stu-id="f413b-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="f413b-108">Badan hukum tempat pekerja mengalami pengeluaran disebut entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="f413b-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="f413b-109">Sebelum pekerja dapat membuat dan mengajukan pengeluaran untuk pekerjaan yang dilakukan untuk entitas hukum yang berbeda, di entitas hukum pemberi pinjaman, pada halaman **parameter manajemen pengeluaran** , pilih opsi **Izinkan baris pengeluaran antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="f413b-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="f413b-110">Posting pajak untuk pengeluaran antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="f413b-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f413b-111">Jika Anda ingin menggunakan grup pajak yang terkait dengan entitas hukum pemberi pinjaman (sumber) alih-alih entitas hukum peminjam (tujuan) dalam laporan pengeluaran Anda, Anda harus mengkonfigurasi ini di konfigurasi pajak penjualan buku besar umum.</span><span class="sxs-lookup"><span data-stu-id="f413b-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="f413b-112">Bila parameter buku besar, **entitas hukum untuk posting pajak antarperusahaan** diatur ke **sumber** dan **menerapkan aturan pajak pajak penjualan** diatur ke **tidak** , kombinasi pajak untuk entitas hukum pemberi pinjaman akan digunakan.</span><span class="sxs-lookup"><span data-stu-id="f413b-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="f413b-113">Bila parameter yang sama diatur ke **tujuan** , kombinasi pajak untuk entitas hukum peminjam akan digunakan.</span><span class="sxs-lookup"><span data-stu-id="f413b-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="f413b-114">Untuk entitas hukum di Amerika Serikat, bila parameter diatur ke **sumber** , bidang **piutang pajak penjualan** juga harus dikonfigurasi pada halaman **grup posting buku besar** baru.</span><span class="sxs-lookup"><span data-stu-id="f413b-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="f413b-115">Mesin akuntansi akan menggunakan informasi dari bidang ini untuk entri akuntansi terkait pajak.</span><span class="sxs-lookup"><span data-stu-id="f413b-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="f413b-116">Perilaku ini sesuai untuk baris pengeluaran yang diposting dengan atau tanpa proyek.</span><span class="sxs-lookup"><span data-stu-id="f413b-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  

---
title: Pengeluaran antarperusahaan
description: Topik ini memberikan informasi tentang cara menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan.
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
ms.openlocfilehash: 553ddbe622210169db8de4aa506dcf1ea1e9d5ef
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960836"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="93ed1-103">Pengeluaran antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="93ed1-103">Intercompany expenses</span></span>

<span data-ttu-id="93ed1-104">Pekerja yang dipekerjakan oleh satu badan hukum di suatu organisasi dapat melakukan pekerjaan untuk entitas hukum lain di organisasi yang sama.</span><span class="sxs-lookup"><span data-stu-id="93ed1-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="93ed1-105">Anda dapat menggunakan pengeluaran antarperusahaan untuk menetapkan pengeluaran pekerja ke entitas hukum tempat pekerjaan dilakukan.</span><span class="sxs-lookup"><span data-stu-id="93ed1-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="93ed1-106">Badan hukum yang mempekerjakan pekerja disebut entitas hukum pemberi pinjaman.</span><span class="sxs-lookup"><span data-stu-id="93ed1-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="93ed1-107">Badan hukum tempat pekerja mengalami pengeluaran disebut entitas hukum peminjam.</span><span class="sxs-lookup"><span data-stu-id="93ed1-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="93ed1-108">Sebelum pekerja dapat membuat dan mengirimkan pengeluaran antarperusahaan, Anda harus mengaktifkan baris pengeluaran antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="93ed1-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="93ed1-109">Di entitas hukum yang meminjamkan, pada halaman **Parameter manajemen pengeluaran**, pilih **izinkan baris pengeluaran antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="93ed1-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="93ed1-110">Posting pajak untuk pengeluaran antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="93ed1-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="93ed1-111">Sebelum Anda dapat menggunakan grup pajak yang terkait dengan entitas hukum yang meminjamkan (sumber), bukan entitas hukum peminjam (tujuan) dalam laporan pengeluaran, Anda harus mengaktifkan fungsi dalam konfigurasi pajak penjualan buku besar umum.</span><span class="sxs-lookup"><span data-stu-id="93ed1-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="93ed1-112">Bila **entitas hukum untuk parameter posting pajak antarperusahaan** diatur ke **Sumber** dan **Terapkan aturan perpajakan pajak penjualan** diatur ke **Tidak**, kombinasi pajak untuk entitas hukum yang meminjamkan digunakan.</span><span class="sxs-lookup"><span data-stu-id="93ed1-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="93ed1-113">Bila parameter yang sama diatur ke **tujuan**, kombinasi pajak untuk entitas hukum peminjam akan digunakan.</span><span class="sxs-lookup"><span data-stu-id="93ed1-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="93ed1-114">Untuk entitas hukum di Amerika Serikat, bila parameter diatur ke **sumber**, bidang **piutang pajak penjualan** juga harus dikonfigurasi pada halaman **grup posting buku besar** baru.</span><span class="sxs-lookup"><span data-stu-id="93ed1-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="93ed1-115">Mesin akuntansi akan menggunakan informasi dari bidang ini untuk entri akuntansi terkait pajak.</span><span class="sxs-lookup"><span data-stu-id="93ed1-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="93ed1-116">Perilaku ini sesuai untuk baris pengeluaran yang diposting dengan atau tanpa proyek.</span><span class="sxs-lookup"><span data-stu-id="93ed1-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  

---
title: Memposting laporan pengeluaran
description: Topik ini menjelaskan cara posting laporan pengeluaran untuk buku besar.
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078630"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="3c44b-103">Memposting laporan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="3c44b-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c44b-104">Setelah laporan pengeluaran disetujui dan ditransfer ke jurnal umum, dapat diposting ke buku besar.</span><span class="sxs-lookup"><span data-stu-id="3c44b-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="3c44b-105">Ketika Anda memposting laporan pengeluaran, pengeluaran yang memenuhi syarat untuk pemulihan pajak pertambahan nilai (PPN) diidentifikasi.</span><span class="sxs-lookup"><span data-stu-id="3c44b-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="3c44b-106">Tugas memverifikasi dan memulihkan pembayaran PPN ditetapkan ke karyawan yang bertanggung jawab untuk memverifikasi laporan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="3c44b-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="3c44b-107">Jika pengeluaran pada laporan pengeluaran dibebankan kepada perusahaan selain perusahaan yang mempekerjakan karyawan, Anda harus memverifikasi perusahaan tentang pengeluaran tersebut terutang pada perusahaan mana dan pengeluaran harus dibayar oleh perusahaan mana.</span><span class="sxs-lookup"><span data-stu-id="3c44b-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="3c44b-108">Misalnya, karyawan yang mengirimkan laporan pengeluaran bekerja untuk perusahaan DAT namun pengeluaran dibebankan ke perusahaan DIR.</span><span class="sxs-lookup"><span data-stu-id="3c44b-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="3c44b-109">Dalam kasus ini, DAT adalah perusahaan yang berpiutang, dan DIR adalah perusahaan yang berutang.</span><span class="sxs-lookup"><span data-stu-id="3c44b-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="3c44b-110">Setelah Anda memverifikasi baris jurnal ini, Anda dapat mengirim baris pengeluaran ke buku besar.</span><span class="sxs-lookup"><span data-stu-id="3c44b-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="3c44b-111">Untuk memposting laporan pengeluaran, pada halaman **laporan pengeluaran yang disetujui** , pilih laporan pengeluaran, lalu di panel tindakan, pilih **posting**.</span><span class="sxs-lookup"><span data-stu-id="3c44b-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="3c44b-112">Anda juga dapat memposting semua laporan pengeluaran dalam daftar secara bersamaan.</span><span class="sxs-lookup"><span data-stu-id="3c44b-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="3c44b-113">Pilih Semua laporan pengeluaran, lalu pilih **posting**.</span><span class="sxs-lookup"><span data-stu-id="3c44b-113">Select all the expense reports, and then select **Post**.</span></span>

---
title: Pengeluaran pribadi pada laporan pengeluaran
description: Topik ini menjelaskan dua metode untuk menangani pengeluaran pribadi pekerja di Microsoft Dynamics 365 Finance.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 825b6c131c8a65b99d5b7ebdadcd6389886f2d11
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078633"
---
# <a name="personal-expenses-on-an-expense-report"></a><span data-ttu-id="a16bc-103">Pengeluaran pribadi pada laporan pengeluaran</span><span class="sxs-lookup"><span data-stu-id="a16bc-103">Personal expenses on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a16bc-104">Selama perjalanan bisnis, pekerja terkadang dapat membebankan pengeluaran pribadi ke kartu kredit perusahaan mereka.</span><span class="sxs-lookup"><span data-stu-id="a16bc-104">During business travel, workers might sometimes charge personal expenses to their corporate credit cards.</span></span> <span data-ttu-id="a16bc-105">Jika Anda tidak menentukan proses untuk menangani pengeluaran pribadi, proses persetujuan untuk laporan pengeluaran mungkin akan terganggu saat pekerja mengirimkan laporan pengeluaran terperinci.</span><span class="sxs-lookup"><span data-stu-id="a16bc-105">If you don't define a process for handling personal expenses, the approval process for expense reports might be disrupted when workers submit their itemized expense reports.</span></span> 

<span data-ttu-id="a16bc-106">Ada dua metode untuk menangani pengeluaran pribadi pekerja:</span><span class="sxs-lookup"><span data-stu-id="a16bc-106">There are two methods for handling a worker's personal expenses:</span></span>

- <span data-ttu-id="a16bc-107">**Dibayar oleh karyawan** -organisasi Anda tidak membayar pengeluaran pribadi yang muncul pada tagihan untuk kartu kredit perusahaan.</span><span class="sxs-lookup"><span data-stu-id="a16bc-107">**Paid by employee** – Your organization doesn't pay personal expenses that appear on the bill for the corporate credit card.</span></span> <span data-ttu-id="a16bc-108">Namun, laporan ini akan membuat laporan yang menunjukkan pengeluaran pribadi bersama dengan pengeluaran perusahaan yang dibebankan ke kartu kredit perusahaan.</span><span class="sxs-lookup"><span data-stu-id="a16bc-108">Instead, it creates a report that shows personal expenses together with the corporate expenses that were charged to the corporate credit card.</span></span>
- <span data-ttu-id="a16bc-109">**Dibayar oleh perusahaan** -organisasi Anda membayar seluruh tagihan untuk kartu kredit perusahaan dan kemudian mendebet rekening pekerja untuk pengeluaran pribadi.</span><span class="sxs-lookup"><span data-stu-id="a16bc-109">**Paid by company** – Your organization pays the whole bill for the corporate credit card and then debits the worker's account for the personal expenses.</span></span>

<span data-ttu-id="a16bc-110">Anda dapat memilih metode yang digunakan organisasi pada halaman **parameter manajemen pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="a16bc-110">You can select the method that your organization uses on the **Expense management parameters** page.</span></span>

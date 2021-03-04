---
title: Mengapa harga diatur default ke nol pada pengeluaran biaya aktual?
description: Pemecahan masalah mengapa harga diatur default ke nol pada pengeluaran biaya aktual.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146352"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="3e5c4-103">Mengapa harga diatur secara default ke nol pada biaya pengeluaran aktual</span><span class="sxs-lookup"><span data-stu-id="3e5c4-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3e5c4-104">FAQ ini berlaku untuk pengeluaran aktual di mana kelas transaksi diatur ke pengeluaran dan jenis transaksi adalah biaya.</span><span class="sxs-lookup"><span data-stu-id="3e5c4-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="3e5c4-105">Pemecahan masalah tarif biaya pada pengeluaran biaya aktual</span><span class="sxs-lookup"><span data-stu-id="3e5c4-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="3e5c4-106">Buka entri pengeluaran terkait, lalu pastikan bahwa terdapat jumlah di bidang entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="3e5c4-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="3e5c4-107">Jika entri pengeluaran asal tidak memiliki bidang jumlah yang diisi, berarti Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="3e5c4-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="3e5c4-108">Untuk mengatasi masalah ini, buat ulang entri pengeluaran dengan jumlah yang valid dan setujui.</span><span class="sxs-lookup"><span data-stu-id="3e5c4-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>

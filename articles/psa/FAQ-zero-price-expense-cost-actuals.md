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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285848"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="a9a27-103">Mengapa harga diatur secara default ke nol pada biaya pengeluaran aktual</span><span class="sxs-lookup"><span data-stu-id="a9a27-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a9a27-104">FAQ ini berlaku untuk pengeluaran aktual di mana kelas transaksi diatur ke pengeluaran dan jenis transaksi adalah biaya.</span><span class="sxs-lookup"><span data-stu-id="a9a27-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="a9a27-105">Pemecahan masalah tarif biaya pada pengeluaran biaya aktual</span><span class="sxs-lookup"><span data-stu-id="a9a27-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="a9a27-106">Buka entri pengeluaran terkait, lalu pastikan bahwa terdapat jumlah di bidang entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="a9a27-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="a9a27-107">Jika entri pengeluaran asal tidak memiliki bidang jumlah yang diisi, berarti Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="a9a27-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="a9a27-108">Untuk mengatasi masalah ini, buat ulang entri pengeluaran dengan jumlah yang valid dan setujui.</span><span class="sxs-lookup"><span data-stu-id="a9a27-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
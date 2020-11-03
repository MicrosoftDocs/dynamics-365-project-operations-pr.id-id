---
title: Mengapa harga diatur default ke nol pada pengeluaran biaya aktual?
description: Pemecahan masalah mengapa harga diatur default ke nol pada pengeluaran biaya aktual.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078505"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="17a58-103">Mengapa harga diatur default ke nol pada pengeluaran biaya aktual?</span><span class="sxs-lookup"><span data-stu-id="17a58-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="17a58-104">FAQ ini berlaku untuk pengeluaran aktual di mana kelas transaksi diatur ke pengeluaran dan jenis transaksi adalah biaya.</span><span class="sxs-lookup"><span data-stu-id="17a58-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="17a58-105">Pemecahan masalah tarif biaya pada pengeluaran biaya aktual</span><span class="sxs-lookup"><span data-stu-id="17a58-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="17a58-106">Buka entri pengeluaran terkait, lalu pastikan bahwa terdapat jumlah di bidang entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="17a58-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="17a58-107">Jika entri pengeluaran asal tidak memiliki bidang jumlah yang diisi, berarti Anda telah mengisolasi masalah.</span><span class="sxs-lookup"><span data-stu-id="17a58-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="17a58-108">Untuk mengatasi masalah ini, buat ulang entri pengeluaran dengan jumlah yang valid dan setujui.</span><span class="sxs-lookup"><span data-stu-id="17a58-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>

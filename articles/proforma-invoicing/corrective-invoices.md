---
title: Faktur yang dikoreksi
description: Topik ini menyediakan informasi tentang faktur yang dikoreksi.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898085"
---
# <a name="corrected-invoices"></a><span data-ttu-id="b2e5f-103">Faktur yang dikoreksi</span><span class="sxs-lookup"><span data-stu-id="b2e5f-103">Corrected invoices</span></span>

<span data-ttu-id="b2e5f-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b2e5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2e5f-105">Faktur yang Dikonfirmasi dapat diedit.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="b2e5f-106">Setelah Anda mengedit faktur yang telah dikonfirmasi, draf faktur yang dikoreksi akan dibuat.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="b2e5f-107">Karena asumsi adalah bahwa Anda ingin membalikkan semua transaksi dan kuantitas dari faktur asli, faktur yang dikoreksi ini mencakup semua transaksi dari faktur asli, dan semua kuantitas di atasnya adalah 0 (nol).</span><span class="sxs-lookup"><span data-stu-id="b2e5f-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="b2e5f-108">Ketika transaksi tidak memerlukan koreksi, Anda dapat menghapusnya dari draf faktur perbaikan.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="b2e5f-109">Untuk membalikkan atau mengembalikan hanya kuantitas parsial, Anda dapat mengedit bidang kuantitas pada detail baris.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="b2e5f-110">Jika Anda membuka detail baris faktur, Anda dapat melihat jumlah faktur asli.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="b2e5f-111">Selanjutnya, Anda dapat mengedit kuantitas faktur saat ini sehingga lebih kecil atau lebih besar dari kuantitas faktur asli.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="b2e5f-112">Setelah Anda mengonfirmasikan faktur koreksi, aktual penjualan yang belum ditagih asli dibalik, dan aktual penjualan baru yang ditagih dibuat.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="b2e5f-113">Jika kuantitas dikurangi, perbedaannya akan menyebabkan penjualan baru yang belum ditagih juga dibuat.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="b2e5f-114">Misalnya, jika penjualan tagihan asli selama delapan jam, dan detail baris faktur perbaikan memiliki kuantitas kurang dari enam jam, baris penjualan asli yang ditagih dibalikkan dan dua aktual baru dibuat:</span><span class="sxs-lookup"><span data-stu-id="b2e5f-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="b2e5f-115">Penjualan yang ditagih untuk enam jam.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="b2e5f-116">Tagihan penjualan yang belum ditagih untuk dua jam yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="b2e5f-117">Transaksi ini dapat ditagih nanti atau ditandai sebagai tidak dikenakan biaya, tergantung pada negosiasi dengan pelanggan.</span><span class="sxs-lookup"><span data-stu-id="b2e5f-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>

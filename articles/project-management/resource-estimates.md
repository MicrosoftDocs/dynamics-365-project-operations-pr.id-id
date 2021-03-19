---
title: Estimasi sumber daya
description: Topik ini memberikan informasi tentang cara estimasi sumber daya dihitung dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286522"
---
# <a name="resource-estimates"></a><span data-ttu-id="46bfc-103">Estimasi sumber daya</span><span class="sxs-lookup"><span data-stu-id="46bfc-103">Resource estimates</span></span>

<span data-ttu-id="46bfc-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="46bfc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46bfc-105">Perkiraan sumber daya berasal dari upaya bertahap waktu yang ditentukan dalam struktur rincian kerja beserta dimensi harga yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="46bfc-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="46bfc-106">Biasanya, penghitungan adalah **tarif/jam untuk setiap peran x jam.**</span><span class="sxs-lookup"><span data-stu-id="46bfc-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="46bfc-107">Upaya bertahap waktu untuk setiap sumber daya disimpan dalam rekaman penetapan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="46bfc-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="46bfc-108">Harga disimpan dalam daftar harga yang telah ditentukan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="46bfc-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="46bfc-109">Konversi unit diterapkan berdasarkan daftar harga yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="46bfc-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimasi sumber daya](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="46bfc-111">Harga biaya dan mata uang biaya default</span><span class="sxs-lookup"><span data-stu-id="46bfc-111">Default cost price and cost currency</span></span>

<span data-ttu-id="46bfc-112">Harga biaya di-default dari unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="46bfc-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="46bfc-113">Default tarif tagihan dan mata uang penjualan</span><span class="sxs-lookup"><span data-stu-id="46bfc-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="46bfc-114">Harga penjualan diterapkan sekali per transaksi.</span><span class="sxs-lookup"><span data-stu-id="46bfc-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="46bfc-115">Hierarki untuk daftar harga penjualan yang di-default sebagai berikut:</span><span class="sxs-lookup"><span data-stu-id="46bfc-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="46bfc-116">Organisasi</span><span class="sxs-lookup"><span data-stu-id="46bfc-116">Organization</span></span>
2. <span data-ttu-id="46bfc-117">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="46bfc-117">Customer</span></span>
3. <span data-ttu-id="46bfc-118">Kuotasi/Kontrak</span><span class="sxs-lookup"><span data-stu-id="46bfc-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
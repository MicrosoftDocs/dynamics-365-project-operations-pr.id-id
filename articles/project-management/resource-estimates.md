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
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127368"
---
# <a name="resource-estimates"></a><span data-ttu-id="4d8ce-103">Estimasi sumber daya</span><span class="sxs-lookup"><span data-stu-id="4d8ce-103">Resource estimates</span></span>

<span data-ttu-id="4d8ce-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="4d8ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4d8ce-105">Perkiraan sumber daya berasal dari upaya bertahap waktu yang ditentukan dalam struktur rincian kerja beserta dimensi harga yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="4d8ce-106">Biasanya, penghitungan adalah **tarif/jam untuk setiap peran x jam.**</span><span class="sxs-lookup"><span data-stu-id="4d8ce-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="4d8ce-107">Upaya bertahap waktu untuk setiap sumber daya disimpan dalam rekaman penetapan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="4d8ce-108">Harga disimpan dalam daftar harga yang telah ditentukan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="4d8ce-109">Konversi unit diterapkan berdasarkan daftar harga yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimasi sumber daya](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="4d8ce-111">Harga biaya dan mata uang biaya default</span><span class="sxs-lookup"><span data-stu-id="4d8ce-111">Default cost price and cost currency</span></span>

<span data-ttu-id="4d8ce-112">Harga biaya di-default dari unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="4d8ce-113">Default tarif tagihan dan mata uang penjualan</span><span class="sxs-lookup"><span data-stu-id="4d8ce-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="4d8ce-114">Harga penjualan diterapkan sekali per transaksi.</span><span class="sxs-lookup"><span data-stu-id="4d8ce-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="4d8ce-115">Hierarki untuk daftar harga penjualan yang di-default sebagai berikut:</span><span class="sxs-lookup"><span data-stu-id="4d8ce-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="4d8ce-116">Organisasi</span><span class="sxs-lookup"><span data-stu-id="4d8ce-116">Organization</span></span>
2. <span data-ttu-id="4d8ce-117">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="4d8ce-117">Customer</span></span>
3. <span data-ttu-id="4d8ce-118">Kuotasi/Kontrak</span><span class="sxs-lookup"><span data-stu-id="4d8ce-118">Quote/contract</span></span>

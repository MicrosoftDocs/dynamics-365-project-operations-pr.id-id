---
title: Estimasi sumber daya
description: Topik ini memberikan informasi tentang cara estimasi sumber daya dihitung dalam Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078404"
---
# <a name="resource-estimates"></a><span data-ttu-id="0f0e0-103">Estimasi sumber daya</span><span class="sxs-lookup"><span data-stu-id="0f0e0-103">Resource estimates</span></span>

<span data-ttu-id="0f0e0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="0f0e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0f0e0-105">Perkiraan sumber daya berasal dari upaya bertahap waktu yang ditentukan dalam struktur rincian kerja beserta dimensi harga yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="0f0e0-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="0f0e0-106">Biasanya, penghitungan adalah **tarif/jam untuk setiap peran x jam.**</span><span class="sxs-lookup"><span data-stu-id="0f0e0-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="0f0e0-107">Upaya bertahap waktu untuk setiap sumber daya disimpan dalam rekaman penetapan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="0f0e0-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="0f0e0-108">Harga disimpan dalam daftar harga yang telah ditentukan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="0f0e0-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="0f0e0-109">Konversi unit diterapkan berdasarkan daftar harga yang berlaku.</span><span class="sxs-lookup"><span data-stu-id="0f0e0-109">Unit conversion is applied based on the applicable price list.</span></span>

![Estimasi sumber daya](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="0f0e0-111">Harga biaya dan mata uang biaya default</span><span class="sxs-lookup"><span data-stu-id="0f0e0-111">Default cost price and cost currency</span></span>

<span data-ttu-id="0f0e0-112">Harga biaya di-default dari unit organisasi.</span><span class="sxs-lookup"><span data-stu-id="0f0e0-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="0f0e0-113">Default tarif tagihan dan mata uang penjualan</span><span class="sxs-lookup"><span data-stu-id="0f0e0-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="0f0e0-114">Harga penjualan diterapkan sekali per transaksi.</span><span class="sxs-lookup"><span data-stu-id="0f0e0-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="0f0e0-115">Hierarki untuk daftar harga penjualan yang di-default sebagai berikut:</span><span class="sxs-lookup"><span data-stu-id="0f0e0-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="0f0e0-116">Organisasi</span><span class="sxs-lookup"><span data-stu-id="0f0e0-116">Organization</span></span>
2. <span data-ttu-id="0f0e0-117">Pelanggan</span><span class="sxs-lookup"><span data-stu-id="0f0e0-117">Customer</span></span>
3. <span data-ttu-id="0f0e0-118">Kuotasi/Kontrak</span><span class="sxs-lookup"><span data-stu-id="0f0e0-118">Quote/contract</span></span>

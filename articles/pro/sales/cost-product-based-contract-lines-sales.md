---
title: Menentukan biaya baris kontrak berbasis produk - lite
description: Topik ini menyediakan informasi tentang pembuatan
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003545"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="3e6d7-103">Menentukan biaya baris kontrak berbasis produk - lite</span><span class="sxs-lookup"><span data-stu-id="3e6d7-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="3e6d7-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="3e6d7-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3e6d7-105">Baris kontrak berbasis produk di Dynamics 365 Project Operations mencakup bidang **Harga Biaya**, yang menyimpan harga biaya produk untuk perhitungan profitabilitas hilir.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3e6d7-106">Bila baris kontrak berbasis produk dibuat untuk produk katalog, biaya baris di-default dari bidang **Biaya Standar** di katalog produk.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3e6d7-107">Bidang **biaya standar** di Katalog Produk diatur dalam mata uang dasar organisasi.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3e6d7-108">Bila unit biaya di-default pada baris kontrak, maka akan diubah menjadi mata uang penjualan pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3e6d7-109">Biaya per unit pada baris kontrak berbasis produk</span><span class="sxs-lookup"><span data-stu-id="3e6d7-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3e6d7-110">Memiliki biaya unit pada baris kontrak berbasis produk memungkinkan biaya produk yang berbeda untuk setiap penjualan unit.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3e6d7-111">Meskipun tidak selalu diperlukan, ada skenario tertentu dengan biaya produk yang dapat didiskon untuk pelanggan oleh pemasok.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3e6d7-112">Pertimbangkan skenario berikut:</span><span class="sxs-lookup"><span data-stu-id="3e6d7-112">Consider the following scenario:</span></span>

<span data-ttu-id="3e6d7-113">Fabrikam robotik memasang lengan robotik di lini perakitan Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3e6d7-114">Fabrikam menyediakan layanan penginstalan, namun lengan robot berasal dari Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="3e6d7-115">Jika pemasangan senjata robot di Adatum Corporation membuka industri vertikal baru untuk lengan robot Trey Research, mereka dapat menawarkan diskon khusus untuk penawaran ini ke fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3e6d7-116">Dalam kasus ini, Fabrikam membuat baris kontrak berbasis produk untuk Robotic Arms.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="3e6d7-117">Biaya per unit dimasukkan untuk kontrak ini.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="3e6d7-118">Biayanya berbeda dengan biaya lengan robot dari Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3e6d7-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Menentukan biaya baris kontrak berbasis produk
description: Topik ini menyediakan informasi tentang pembuatan
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/20/2020
ms.locfileid: "4078715"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="3f58e-103">Menentukan biaya baris kontrak berbasis produk</span><span class="sxs-lookup"><span data-stu-id="3f58e-103">Costing product-based contract lines</span></span>

<span data-ttu-id="3f58e-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="3f58e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="3f58e-105">Baris kontrak berbasis produk di Dynamics 365 Project Operations mencakup bidang **harga biaya** , yang menyimpan harga produk untuk penghitungan profitabilitas hilir.</span><span class="sxs-lookup"><span data-stu-id="3f58e-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="3f58e-106">Bila baris kontrak berbasis produk dibuat untuk produk Katalog, biaya baris kontrak berbasis produk akan diisi default dari bidang **biaya standar** dalam Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="3f58e-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="3f58e-107">Bidang **biaya standar** di Katalog Produk diatur dalam mata uang dasar organisasi.</span><span class="sxs-lookup"><span data-stu-id="3f58e-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="3f58e-108">Bila unit biaya di-default pada baris kontrak, maka akan diubah menjadi mata uang penjualan pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="3f58e-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="3f58e-109">Biaya per unit pada baris kontrak berbasis produk</span><span class="sxs-lookup"><span data-stu-id="3f58e-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="3f58e-110">Memiliki biaya unit pada baris kontrak berbasis produk memungkinkan biaya produk yang berbeda untuk setiap penjualan unit.</span><span class="sxs-lookup"><span data-stu-id="3f58e-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="3f58e-111">Meskipun tidak selalu diperlukan, ada skenario tertentu dengan biaya produk yang dapat didiskon untuk pelanggan oleh pemasok.</span><span class="sxs-lookup"><span data-stu-id="3f58e-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="3f58e-112">Pertimbangkan skenario berikut:</span><span class="sxs-lookup"><span data-stu-id="3f58e-112">Consider the following scenario:</span></span>

<span data-ttu-id="3f58e-113">Fabrikam robotik memasang lengan robotik di lini perakitan Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="3f58e-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="3f58e-114">Fabrikam menyediakan layanan penginstalan tetapi senjata robotik Diperoleh dari Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3f58e-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="3f58e-115">Jika pemasangan senjata robot di Adatum Corporation membuka industri vertikal baru untuk lengan robot Trey Research, mereka dapat menawarkan diskon khusus untuk penawaran ini ke fabrikam.</span><span class="sxs-lookup"><span data-stu-id="3f58e-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="3f58e-116">Dalam kasus ini, fabrikam membuat baris kontrak berbasis produk untuk lengan robot dan input per unit biaya untuk kontrak ini yang berbeda dari biaya standar lengan robot dari Trey Research.</span><span class="sxs-lookup"><span data-stu-id="3f58e-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>

---
title: Menentukan biaya baris kuotasi berbasis produk
description: Topik ini menyediakan informasi tentang menerapkan harga biaya ke baris kuotasi berbasis produk.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078387"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="a5b5f-103">Menentukan biaya baris kuotasi berbasis produk</span><span class="sxs-lookup"><span data-stu-id="a5b5f-103">Costing product-based quote lines</span></span>

<span data-ttu-id="a5b5f-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="a5b5f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a5b5f-105">Baris kuotasi berbasis produk di Dynamics 365 Project Operations juga memiliki bidang **harga biaya**.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="a5b5f-106">Bidang ini digunakan untuk melacak harga untuk produk pada penghitungan baris kuotasi dan untuk profitabilitas hilir.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="a5b5f-107">Bila baris kuotasi berbasis produk dibuat untuk produk Katalog, biaya baris kuotasi berbasis produk akan diisi default dari bidang **biaya standar** dalam Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="a5b5f-108">Bidang biaya standar di Katalog Produk diatur dalam mata uang dasar organisasi.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="a5b5f-109">Biaya unit default pada baris kuotasi berdasarkan produk dikonversi ke mata uang penjualan pada kuotasi.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="a5b5f-110">Biaya per unit pada baris kuotasi berbasis produk</span><span class="sxs-lookup"><span data-stu-id="a5b5f-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="a5b5f-111">Tujuan memiliki biaya unit pada baris kuotasi berbasis produk adalah untuk memungkinkan biaya yang berbeda untuk produk untuk setiap penjualan.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="a5b5f-112">Ini bukan skenario umum, namun terkadang biaya produk dapat didiskon oleh pemasok tergantung pada pelanggan penjualan akhir.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="a5b5f-113">Misalnya:</span><span class="sxs-lookup"><span data-stu-id="a5b5f-113">For example:</span></span>

<span data-ttu-id="a5b5f-114">Fabrikam robotik memasang lengan robotik di lini perakitan A Datum Corporation.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="a5b5f-115">Fabrikam menyediakan layanan penginstalan tetapi senjata robotik Diperoleh dari Trey Robotika.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="a5b5f-116">Jika pemasangan senjata robot di A Datum Corporation membuka industri vertikal baru untuk lengan robot Trey, Trey dapat memberikan diskon khusus untuk penawaran ini ke fabrikam.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="a5b5f-117">Dalam kasus ini, fabrikam akan membuat baris kuotasi berbasis produk untuk lengan robot dan memasukkan biaya khusus per unit untuk kuotasi ini.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="a5b5f-118">Biaya ini berbeda dari biaya standar lengan Trey Robotic.</span><span class="sxs-lookup"><span data-stu-id="a5b5f-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>

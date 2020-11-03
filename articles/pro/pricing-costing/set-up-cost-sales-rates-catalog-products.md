---
title: Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog
description: Topik ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078551"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="b70c5-103">Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog</span><span class="sxs-lookup"><span data-stu-id="b70c5-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="b70c5-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b70c5-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b70c5-105">Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="b70c5-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="b70c5-106">Karena produk tidak dapat diperkirakan atau digunakan pada proyek dalam Project Operations, tidak perlu menetapkan harga katalog produk pada daftar harga proyek untuk kuotasi dan kontrak.</span><span class="sxs-lookup"><span data-stu-id="b70c5-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="b70c5-107">Harga katalog produk harus disiapkan di bidang **Harga Produk** dari kuotasi, kontrak, atau akun.</span><span class="sxs-lookup"><span data-stu-id="b70c5-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="b70c5-108">Jangan menyiapkan harga katalog produk dalam daftar harga proyek untuk entitas ini.</span><span class="sxs-lookup"><span data-stu-id="b70c5-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="b70c5-109">Daftar harga proyek eksklusif untuk Project Operations.</span><span class="sxs-lookup"><span data-stu-id="b70c5-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="b70c5-110">Ada logika bisnis khusus aplikasi yang menyalin daftar harga dari kuotasi ke kontrak.</span><span class="sxs-lookup"><span data-stu-id="b70c5-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="b70c5-111">Hasilnya adalah Daftar Harga proyek Khusus Kontrak.</span><span class="sxs-lookup"><span data-stu-id="b70c5-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="b70c5-112">Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar.</span><span class="sxs-lookup"><span data-stu-id="b70c5-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="b70c5-113">Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="b70c5-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="b70c5-114">Ini berarti bahwa daftar harga produk tidak berdampak pada kinerja proses kemenangan kuotasi.</span><span class="sxs-lookup"><span data-stu-id="b70c5-114">This means that product price lists don't impact the performance of the quote win process.</span></span>

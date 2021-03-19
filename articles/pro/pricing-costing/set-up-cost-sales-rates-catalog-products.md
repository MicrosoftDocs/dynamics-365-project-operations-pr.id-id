---
title: Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite
description: Topik ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk item dalam katalog produk.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0941c549cc38f0938a5819e8cb6ca9912f14790
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274462"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="8e1d4-103">Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite</span><span class="sxs-lookup"><span data-stu-id="8e1d4-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="8e1d4-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="8e1d4-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="8e1d4-105">Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="8e1d4-106">Dalam Project Operations, produk tidak dapat diperkirakan atau digunakan pada proyek, sehingga harga katalog produk tidak perlu ditetapkan pada daftar harga proyek untuk penawaran dan kontrak.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="8e1d4-107">Gunakan bidang **Harga Produk** dari kuotasi, kontrak, atau akun untuk menyiapkan harga katalog produk.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="8e1d4-108">Jangan siapkan harga katalog produk dalam daftar harga proyek.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="8e1d4-109">Daftar harga proyek eksklusif untuk Project Operations.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="8e1d4-110">Logika bisnis khusus aplikasi menyalin daftar harga dari kuotasi ke kontrak.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="8e1d4-111">Hasilnya adalah Daftar Harga proyek Khusus Kontrak.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="8e1d4-112">Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="8e1d4-113">Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="8e1d4-114">Karena tidak ada penyalinan yang terlibat, kinerja proses kuotasi tidak terpengaruh.</span><span class="sxs-lookup"><span data-stu-id="8e1d4-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
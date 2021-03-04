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
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764556"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="ebebc-103">Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite</span><span class="sxs-lookup"><span data-stu-id="ebebc-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="ebebc-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="ebebc-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="ebebc-105">Menyiapkan harga untuk item katalog produk di Dynamics 365 Project Operations sama dengan di Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="ebebc-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="ebebc-106">Dalam Project Operations, produk tidak dapat diperkirakan atau digunakan pada proyek, sehingga harga katalog produk tidak perlu ditetapkan pada daftar harga proyek untuk penawaran dan kontrak.</span><span class="sxs-lookup"><span data-stu-id="ebebc-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="ebebc-107">Gunakan bidang **Harga Produk** dari kuotasi, kontrak, atau akun untuk menyiapkan harga katalog produk.</span><span class="sxs-lookup"><span data-stu-id="ebebc-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="ebebc-108">Jangan siapkan harga katalog produk dalam daftar harga proyek.</span><span class="sxs-lookup"><span data-stu-id="ebebc-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="ebebc-109">Daftar harga proyek eksklusif untuk Project Operations.</span><span class="sxs-lookup"><span data-stu-id="ebebc-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="ebebc-110">Logika bisnis khusus aplikasi menyalin daftar harga dari kuotasi ke kontrak.</span><span class="sxs-lookup"><span data-stu-id="ebebc-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="ebebc-111">Hasilnya adalah Daftar Harga proyek Khusus Kontrak.</span><span class="sxs-lookup"><span data-stu-id="ebebc-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="ebebc-112">Operasi salinan dapat menunda proses kemenangan kuotasi jika daftar harga proyek pada kuotasi menjadi terlalu besar.</span><span class="sxs-lookup"><span data-stu-id="ebebc-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="ebebc-113">Daftar harga produk tidak disalin untuk membuat daftar harga kustom pada kontrak.</span><span class="sxs-lookup"><span data-stu-id="ebebc-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="ebebc-114">Karena tidak ada penyalinan yang terlibat, kinerja proses kuotasi tidak terpengaruh.</span><span class="sxs-lookup"><span data-stu-id="ebebc-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>

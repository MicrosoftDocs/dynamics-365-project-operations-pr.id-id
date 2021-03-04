---
title: Baris peluang berbasis produk - lite
description: Topik ini menyediakan informasi tentang item baris peluang berbasis produk dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b826bf3a1320eee2758af7a094e9f1c2eac6a119
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764958"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="2802f-103">Baris peluang berbasis produk - lite</span><span class="sxs-lookup"><span data-stu-id="2802f-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="2802f-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="2802f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2802f-105">Lini peluang berbasis produk adalah item baris pada peluang.</span><span class="sxs-lookup"><span data-stu-id="2802f-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="2802f-106">Item baris yang berbeda ini berada di faktur akhir yang diberikan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="2802f-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="2802f-107">Faktur tidak mencakup layanan tambahan lainnya.</span><span class="sxs-lookup"><span data-stu-id="2802f-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="2802f-108">Pembelanjaan dan konsumsi terkait tidak dilacak pada tugas proyek terkait mana pun.</span><span class="sxs-lookup"><span data-stu-id="2802f-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="2802f-109">Baris berbasis produk dapat berupa item Katalog atau produk pilihan.</span><span class="sxs-lookup"><span data-stu-id="2802f-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="2802f-110">Sebagian besar fungsi pada baris berbasis produk peluang mengikuti fungsi yang disediakan oleh aplikasi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="2802f-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="2802f-111">Untuk informasi lebih lanjut tentang baris peluang berbasis produk, lihat [menambahkan produk ke peluang](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="2802f-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="2802f-112">**Anggaran pelanggan** adalah konsep yang khusus untuk baris peluang berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="2802f-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="2802f-113">Bidang **anggaran Pelanggan** melacak jumlah yang harus dibayar pelanggan untuk item tersebut.</span><span class="sxs-lookup"><span data-stu-id="2802f-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="2802f-114">Bila metode pendapatan ringkasan Peluang adalah **Terhitung Sistem**, nilai anggaran pelanggan di seluruh baris peluang diringkas untuk menghitung perkiraan pendapatan.</span><span class="sxs-lookup"><span data-stu-id="2802f-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 


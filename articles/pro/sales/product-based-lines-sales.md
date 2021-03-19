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
ms.openlocfilehash: 4f8da5258a1dd0aa4229654c0e1e222b8cf3a21a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272617"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="9c8ab-103">Baris peluang berbasis produk - lite</span><span class="sxs-lookup"><span data-stu-id="9c8ab-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="9c8ab-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="9c8ab-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9c8ab-105">Lini peluang berbasis produk adalah item baris pada peluang.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="9c8ab-106">Item baris yang berbeda ini berada di faktur akhir yang diberikan kepada pelanggan.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-106">These distinct line items are on the eventual invoice that is provided to the customer.</span></span> <span data-ttu-id="9c8ab-107">Faktur tidak mencakup layanan tambahan lainnya.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-107">The invoice doesn't include any other additional services.</span></span> <span data-ttu-id="9c8ab-108">Pembelanjaan dan konsumsi terkait tidak dilacak pada tugas proyek terkait mana pun.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-108">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="9c8ab-109">Baris berbasis produk dapat berupa item Katalog atau produk pilihan.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-109">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="9c8ab-110">Sebagian besar fungsi pada baris berbasis produk peluang mengikuti fungsi yang disediakan oleh aplikasi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-110">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="9c8ab-111">Untuk informasi lebih lanjut tentang baris peluang berbasis produk, lihat [menambahkan produk ke peluang](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="9c8ab-111">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="9c8ab-112">**Anggaran pelanggan** adalah konsep yang khusus untuk baris peluang berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-112">**Customer budget** is a concept that is specific to project-based opportunity lines.</span></span> <span data-ttu-id="9c8ab-113">Bidang **anggaran Pelanggan** melacak jumlah yang harus dibayar pelanggan untuk item tersebut.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-113">The **Customer budget** field tracks the amount the customer is willing to pay for the item.</span></span>

<span data-ttu-id="9c8ab-114">Bila metode pendapatan ringkasan Peluang adalah **Terhitung Sistem**, nilai anggaran pelanggan di seluruh baris peluang diringkas untuk menghitung perkiraan pendapatan.</span><span class="sxs-lookup"><span data-stu-id="9c8ab-114">When the revenue method of the Opportunity summary is **System Calculated**, the customer budget values across the opportunity lines are summarized to calculate the estimated revenue.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
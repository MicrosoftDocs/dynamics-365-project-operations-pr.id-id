---
title: Baris peluang berbasis produk - lite
description: Topik ini menyediakan informasi tentang item baris peluang berbasis produk dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176334"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="6c600-103">Baris peluang berbasis produk - lite</span><span class="sxs-lookup"><span data-stu-id="6c600-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="6c600-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="6c600-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6c600-105">Lini peluang berbasis produk adalah item baris pada peluang.</span><span class="sxs-lookup"><span data-stu-id="6c600-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="6c600-106">Baris ini dikirim ke pelanggan sebagai item baris yang berbeda pada faktur akhirnya tanpa layanan nilai tambah lainnya.</span><span class="sxs-lookup"><span data-stu-id="6c600-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="6c600-107">Pembelanjaan dan konsumsi terkait tidak dilacak pada tugas proyek terkait mana pun.</span><span class="sxs-lookup"><span data-stu-id="6c600-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="6c600-108">Baris berbasis produk dapat berupa item Katalog atau produk pilihan.</span><span class="sxs-lookup"><span data-stu-id="6c600-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="6c600-109">Sebagian besar fungsi pada baris berbasis produk peluang mengikuti fungsi yang disediakan oleh aplikasi Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="6c600-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="6c600-110">Untuk informasi lebih lanjut tentang baris peluang berbasis produk, lihat [menambahkan produk ke peluang](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="6c600-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="6c600-111">Satu konsep tentang baris peluang berbasis produk yang spesifik untuk peluang berbasis proyek adalah **anggaran pelanggan**.</span><span class="sxs-lookup"><span data-stu-id="6c600-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="6c600-112">Gunakan bidang ini untuk melacak jumlah yang bersedia dibayar pelanggan untuk item baris.</span><span class="sxs-lookup"><span data-stu-id="6c600-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="6c600-113">Jika metode pendapatan dari ringkasan peluang diatur ke **dihitung sistem**, nilai anggaran pelanggan di seluruh baris berbasis produk dan proyek diringkas untuk menghitung estimasi pendapatan.</span><span class="sxs-lookup"><span data-stu-id="6c600-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>

---
title: Bidang Project Operations sebagai dimensi harga
description: Topik ini memberikan informasi menggunakan bidang sebagai dimensi harga di Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004490"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="f6fe6-103">Bidang Project Operations sebagai dimensi harga</span><span class="sxs-lookup"><span data-stu-id="f6fe6-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="f6fe6-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="f6fe6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f6fe6-105">Entitas **aktual** memiliki banyak bidang yang dapat digunakan sebagai dimensi harga untuk harga berbasis sumber daya.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="f6fe6-106">Misalnya, satu bidang umum adalah **sumber daya dapat dipesan**.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="f6fe6-107">Perusahaan kecil yang memiliki sumber daya yang dapat ditagih kurang dari 20-30 mungkin menemukan bahwa memiliki tarif tagihan dan biaya yang spesifik untuk setiap sumber daya adalah pendekatan yang lebih sederhana.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="f6fe6-108">Namun demikian, seiring berkembangnya tenaga kerja yang dapat ditagih, tarif sumber daya spesifik dapat menjadi tidak realistis untuk dipertahankan.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="f6fe6-109">Biaya sumber daya dan tarif tagihan mulai bervariasi saat sumber daya dipromosikan, mendapatkan lebih banyak pengalaman, atau memperoleh seperangkat keterampilan yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="f6fe6-110">Contoh lainnya adalah kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-110">Another example is that of transaction category.</span></span> <span data-ttu-id="f6fe6-111">Pelanggan dan pelaksana telah menggunakan kategori transaksi untuk mengklasifikasikan pekerjaan dan menggunakan bidang untuk menetapkan harga dan biaya berdasarkan Kategori pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="f6fe6-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
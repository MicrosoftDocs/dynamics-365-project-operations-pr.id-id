---
title: Gunakan bidang yang ada dalam Project Service sebagai dimensi harga
description: Topik ini menyediakan informasi tentang penggunaan Project Service proyek yang ada sebagai dimensi harga.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: ad03f5f7c1c9e93ca12a8c8d48ffbd2f80b1511f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281572"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="fccb0-103">Gunakan bidang yang ada dalam Project Service sebagai dimensi harga</span><span class="sxs-lookup"><span data-stu-id="fccb0-103">Use an existing field in Project Service as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fccb0-104">Project Service Automation (PSA) memiliki banyak bidang pada entitas **aktual** yang dapat digunakan sebagai dimensi harga untuk harga berbasis sumber daya dalam organisasi proyek.</span><span class="sxs-lookup"><span data-stu-id="fccb0-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="fccb0-105">Misalnya, satu bidang umum adalah **sumber daya dapat dipesan**.</span><span class="sxs-lookup"><span data-stu-id="fccb0-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="fccb0-106">Perusahaan kecil yang memiliki sumber daya yang dapat ditagih kurang dari 20-30 mungkin menemukan bahwa memiliki tarif tagihan dan biaya yang spesifik untuk setiap sumber daya adalah pendekatan yang lebih sederhana.</span><span class="sxs-lookup"><span data-stu-id="fccb0-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="fccb0-107">Namun, karena tenaga kerja yang dapat ditagih tumbuh, tingkat spesifik dapat menjadi tidak realistis untuk dipertahankan karena biaya sumber daya dan tarif tagihan mulai bervariasi seiring sumber daya dipromosikan, mendapatkan lebih banyak pengalaman, atau memperoleh set keahlian yang berbeda.</span><span class="sxs-lookup"><span data-stu-id="fccb0-107">However, as the billable workforce grows, specific rates could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill set.</span></span> <span data-ttu-id="fccb0-108">Karena pendekatan ini masih berfungsi untuk perusahaan dengan ukuran tertentu, lihat [gunakan sumber daya yang dapat dipesan sebagai dimensi](bookable-resource-pricing-dimension.md) harga untuk memahami bagaimana bidang Project Service yang ada dapat digunakan sebagai dimensi harga.</span><span class="sxs-lookup"><span data-stu-id="fccb0-108">Because this approach still works for companies of a certain size, see [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="fccb0-109">Contoh lainnya adalah kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="fccb0-109">Another example is that of transaction category.</span></span> <span data-ttu-id="fccb0-110">Pelanggan dan pelaksana telah menggunakan kategori transaksi dalam PSA untuk mengklasifikasikan pekerjaan dan menggunakan bidang untuk menetapkan harga dan biaya berdasarkan Kategori pekerjaan.</span><span class="sxs-lookup"><span data-stu-id="fccb0-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="fccb0-111">Untuk informasi lebih lanjut, Lihat [menggunakan kategori transaksi sebagai dimensi harga](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="fccb0-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Analisis kuotasi proyek
description: Topik ini menyediakan informasi tentang analisis kuotasi proyek.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012455"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="a73c9-103">Analisis kuotasi proyek</span><span class="sxs-lookup"><span data-stu-id="a73c9-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a73c9-104">Dynamics 365 Project Service Automation menganalisis kuotasi proyek untuk memperkirakan profitabilitas.</span><span class="sxs-lookup"><span data-stu-id="a73c9-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="a73c9-105">Juga menganalisis seberapa baik kuotasi selaras dengan ekspektasi pelanggan tentang tanggal pengiriman atau tanggal selesai, dan tentang anggaran.</span><span class="sxs-lookup"><span data-stu-id="a73c9-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="a73c9-106">Analisis Profitabilitas</span><span class="sxs-lookup"><span data-stu-id="a73c9-106">Profitability analysis</span></span>

<span data-ttu-id="a73c9-107">Project Service Automation menganalisis profitabilitas menggunakan margin kotor dan margin kotor yang disesuaikan.</span><span class="sxs-lookup"><span data-stu-id="a73c9-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="a73c9-108">Margin kotor dihitung menggunakan rumus berikut:</span><span class="sxs-lookup"><span data-stu-id="a73c9-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="a73c9-109">Margin kotor yang disesuaikan dihitung menggunakan rumus berikut:</span><span class="sxs-lookup"><span data-stu-id="a73c9-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="a73c9-110">Jika nilai margin kotor dan margin kotor yang disesuaikan berbeda dengan margin yang lebar, sebagian besar pekerjaan dalam kuotasi diklasifikasikan sebagai tidak dikenakan biaya.</span><span class="sxs-lookup"><span data-stu-id="a73c9-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="a73c9-111">Analisis Harapan Pelanggan</span><span class="sxs-lookup"><span data-stu-id="a73c9-111">Analysis of customer expectations</span></span>

<span data-ttu-id="a73c9-112">Anda dapat menganalisis kuotasi dan membuat diagram untuk ekspektasi pelanggan tentang jadwal dan anggaran jika Anda memasukkan nilai untuk bidang berikut:</span><span class="sxs-lookup"><span data-stu-id="a73c9-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="a73c9-113">Bidang **tanggal pengiriman diminta** pada header kuotasi.</span><span class="sxs-lookup"><span data-stu-id="a73c9-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="a73c9-114">Bidang **anggaran pelanggan** untuk setiap baris kuotasi (untuk baris berbasis proyek dan baris berbasis produk).</span><span class="sxs-lookup"><span data-stu-id="a73c9-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="a73c9-115">Analisis ekspektasi pelanggan tentang jadwal dilakukan dengan membandingkan tanggal akhir terbaru detail baris kuotasi dengan tanggal pengiriman yang diminta di semua baris kuotasi dalam kuotasi.</span><span class="sxs-lookup"><span data-stu-id="a73c9-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="a73c9-116">Analisis ekspektasi pelanggan tentang anggaran dilakukan dengan membandingkan jumlah total anggaran pelanggan dengan jumlah yang dikutip di semua baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="a73c9-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
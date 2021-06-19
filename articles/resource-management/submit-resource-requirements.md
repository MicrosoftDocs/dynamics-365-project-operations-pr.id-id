---
title: Mengajukan permintaan sumber daya
description: Anda dapat mengajukan persyaratan sumber daya yang dihasilkan sebagai permintaan sumber daya. Permintaan tersebut kemudian dikirim ke manajer sumber daya untuk pemenuhan.
author: ruhercul
ms.date: 10/04/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6ac0044a27d1e506c9c62c477014017fd0ca06cb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014030"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="881a9-104">Mengajukan permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="881a9-104">Submit a resource request</span></span>

<span data-ttu-id="881a9-105">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="881a9-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="881a9-106">Anda dapat mengajukan persyaratan sumber daya yang dihasilkan sebagai permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="881a9-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="881a9-107">Permintaan tersebut kemudian dikirim ke manajer sumber daya untuk pemenuhan.</span><span class="sxs-lookup"><span data-stu-id="881a9-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="881a9-108">Di Dynamics 365 Project Operations, pada halaman **proyek**, pilih tab **tim** untuk melihat daftar sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="881a9-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="881a9-109">Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu klik **Ajukan Permintaan**.</span><span class="sxs-lookup"><span data-stu-id="881a9-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="881a9-110">Status permintaan anggota tim umum akan berubah menjadi **Diajukan**.</span><span class="sxs-lookup"><span data-stu-id="881a9-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="881a9-111">Setelah permintaan terpenuhi, sumber daya generik digantikan dengan sumber daya bernama jika Manajer sumber daya memenuhi permintaan dengan Pemesanan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="881a9-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="881a9-112">Atau, jika manajer sumber daya mengusulkan sumber daya bernama, sumber daya generik akan tetap berada di tim dan status permintaan akan berubah menjadi **Perlu Ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="881a9-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
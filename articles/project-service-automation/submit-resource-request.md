---
title: Ajukan permintaan sumber daya
description: Topik ini menyediakan informasi tentang pengajuan permintaan sumber daya proyek.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752481"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="90c91-103">Ajukan permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="90c91-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="90c91-104">Anda dapat mengajukan persyaratan sumber daya yang dihasilkan sebagai permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="90c91-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="90c91-105">Permintaan tersebut kemudian dikirim ke manajer sumber daya untuk pemenuhan.</span><span class="sxs-lookup"><span data-stu-id="90c91-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="90c91-106">Di Project Service Automation (PSA), pada halaman **proyek**, klik tab **tim** untuk melihat daftar sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="90c91-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="90c91-107">Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu klik **Ajukan Permintaan**.</span><span class="sxs-lookup"><span data-stu-id="90c91-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Mengajukan permintaan sumber daya](media/RM-how-to-18.png)

<span data-ttu-id="90c91-109">Status permintaan anggota tim umum akan berubah menjadi **Diajukan**.</span><span class="sxs-lookup"><span data-stu-id="90c91-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="90c91-110">Setelah permintaan terpenuhi oleh Manajer sumber daya, sumber daya generik akan digantikan dengan sumber daya bernama jika Manajer sumber daya memenuhi permintaan dengan Pemesanan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="90c91-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="90c91-111">Jika tidak, sumber daya generik akan tetap berada di tim dan status permintaan akan berubah menjadi **Perlu Ditinjau**, jika Manajer sumber daya telah mengusulkan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="90c91-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>

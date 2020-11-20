---
title: Mengajukan permintaan sumber daya
description: Anda dapat mengajukan persyaratan sumber daya yang dihasilkan sebagai permintaan sumber daya. Permintaan tersebut kemudian dikirim ke manajer sumber daya untuk pemenuhan.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 18f43acc64ed72b1543a2d7d91a2648e7e185fc4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128827"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="8244b-104">Mengajukan permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="8244b-104">Submit a resource request</span></span>

<span data-ttu-id="8244b-105">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="8244b-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8244b-106">Anda dapat mengajukan persyaratan sumber daya yang dihasilkan sebagai permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="8244b-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="8244b-107">Permintaan tersebut kemudian dikirim ke manajer sumber daya untuk pemenuhan.</span><span class="sxs-lookup"><span data-stu-id="8244b-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="8244b-108">Di Dynamics 365 Project Operations, di halaman **proyek**, pilih tab **tim** untuk melihat daftar sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="8244b-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="8244b-109">Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu klik **Ajukan Permintaan**.</span><span class="sxs-lookup"><span data-stu-id="8244b-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="8244b-110">Status permintaan anggota tim umum akan berubah menjadi **Diajukan**.</span><span class="sxs-lookup"><span data-stu-id="8244b-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="8244b-111">Setelah permintaan terpenuhi, sumber daya generik digantikan dengan sumber daya bernama jika Manajer sumber daya memenuhi permintaan dengan Pemesanan sumber daya bernama.</span><span class="sxs-lookup"><span data-stu-id="8244b-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="8244b-112">Atau, jika manajer sumber daya mengusulkan sumber daya bernama, sumber daya generik akan tetap berada di tim dan status permintaan akan berubah menjadi **Perlu Ditinjau**.</span><span class="sxs-lookup"><span data-stu-id="8244b-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>

---
title: Menentukan keterampilan dan kecakapan
description: Topik ini menyediakan informasi tentang cara mengonfigurasikan model kecakapan untuk menilai sumber daya.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897635"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="b2d09-103">Menentukan keterampilan dan kecakapan</span><span class="sxs-lookup"><span data-stu-id="b2d09-103">Define skills and proficiencies</span></span>

<span data-ttu-id="b2d09-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b2d09-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2d09-105">Keahlian adalah karakteristik sumber daya yang digunakan bersama antara Dynamics 365 Project Operations dan jika ada, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="b2d09-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="b2d09-106">Untuk mengelola repositori keahlian dalam Project Operations, buka **sumber daya** \> **Keahlian sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="b2d09-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="b2d09-107">Gunakan model kecakapan untuk menilai sumber daya</span><span class="sxs-lookup"><span data-stu-id="b2d09-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="b2d09-108">Keahlian untuk sumber daya dinilai berdasarkan model kecakapan.</span><span class="sxs-lookup"><span data-stu-id="b2d09-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="b2d09-109">Peringkat individual berada dalam model kemahiran.</span><span class="sxs-lookup"><span data-stu-id="b2d09-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="b2d09-110">Untuk membuat model kecakapan, buka **sumber daya** \> **model kecakapan**, lalu pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="b2d09-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="b2d09-111">Di model peringkat baru, tentukan nilai peringkat minimum, nilai peringkat maksimum, dan entitas yang dinilai.</span><span class="sxs-lookup"><span data-stu-id="b2d09-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="b2d09-112">Di subkisi **nilai peringkat**, Anda dapat menentukan nilai peringkat yang berbeda, dari minimum hingga maksimum.</span><span class="sxs-lookup"><span data-stu-id="b2d09-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="b2d09-113">Nilai peringkat ini ditampilkan pada **persyaratan sumber daya**, **papan jadwal**, dan filter **asisten jadwal**.</span><span class="sxs-lookup"><span data-stu-id="b2d09-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>

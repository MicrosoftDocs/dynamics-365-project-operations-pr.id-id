---
title: Menentukan keterampilan dan kecakapan
description: Topik ini menyediakan informasi tentang cara mengonfigurasikan model kecakapan untuk menilai sumber daya.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 8738a4743554704ef76807c81fdefcd74e668e1b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124777"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="ca511-103">Menentukan keterampilan dan kecakapan</span><span class="sxs-lookup"><span data-stu-id="ca511-103">Define skills and proficiencies</span></span>

<span data-ttu-id="ca511-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="ca511-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ca511-105">Keahlian adalah karakteristik sumber daya yang digunakan bersama antara Dynamics 365 Project Operations dan jika ada, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="ca511-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="ca511-106">Untuk mengelola repositori keahlian dalam Project Operations, buka **sumber daya** \> **Keahlian sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="ca511-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="ca511-107">Gunakan model kecakapan untuk menilai sumber daya</span><span class="sxs-lookup"><span data-stu-id="ca511-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="ca511-108">Keahlian untuk sumber daya dinilai berdasarkan model kecakapan.</span><span class="sxs-lookup"><span data-stu-id="ca511-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="ca511-109">Peringkat individual berada dalam model kemahiran.</span><span class="sxs-lookup"><span data-stu-id="ca511-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="ca511-110">Untuk membuat model kecakapan, buka **sumber daya** \> **model kecakapan**, lalu pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="ca511-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="ca511-111">Di model peringkat baru, tentukan nilai peringkat minimum, nilai peringkat maksimum, dan entitas yang dinilai.</span><span class="sxs-lookup"><span data-stu-id="ca511-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="ca511-112">Di subkisi **nilai peringkat**, Anda dapat menentukan nilai peringkat yang berbeda, dari minimum hingga maksimum.</span><span class="sxs-lookup"><span data-stu-id="ca511-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="ca511-113">Nilai peringkat ini ditampilkan pada **persyaratan sumber daya**, **papan jadwal**, dan filter **asisten jadwal**.</span><span class="sxs-lookup"><span data-stu-id="ca511-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>

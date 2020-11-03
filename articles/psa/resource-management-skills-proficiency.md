---
title: Model keahlian dan kecakapan
description: Topik ini menyediakan informasi tentang cara menggunakan keahlian dan model kecakapan.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cd243544df062e5801bbfa0a3bd75c4d9a116a6f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078704"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="1e0f0-103">Model keahlian dan kecakapan</span><span class="sxs-lookup"><span data-stu-id="1e0f0-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1e0f0-104">Keahlian adalah karakteristik sumber daya yang digunakan bersama antara Dynamics 365 Project Service Automation dan jika ada, Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="1e0f0-105">Untuk mengelola repositori keahlian dalam Project Service Automation, buka **sumber daya** \> **Keahlian sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Keterampilan Sumber Daya](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="1e0f0-107">Gunakan model kecakapan untuk menilai sumber daya</span><span class="sxs-lookup"><span data-stu-id="1e0f0-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="1e0f0-108">Keahlian untuk sumber daya dinilai berdasarkan model kecakapan.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="1e0f0-109">Peringkat individual berada dalam model kemahiran.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="1e0f0-110">Untuk membuat model kecakapan, buka **sumber daya** \> **model kecakapan** , lalu pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-110">To create a proficiency model, go to **Resources** \> **Proficiency Models** , and then select **New**.</span></span>
2. <span data-ttu-id="1e0f0-111">Di model peringkat baru, tentukan nilai peringkat minimum, nilai peringkat maksimum, dan entitas yang dinilai.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="1e0f0-112">Di subkisi **nilai peringkat** , Anda dapat menentukan nilai peringkat yang berbeda, dari minimum hingga maksimum.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Peringkat minimum dan maksimum ditentukan](media/Resource-Management-image85.png)

<span data-ttu-id="1e0f0-114">Nilai peringkat ini ditampilkan pada **persyaratan sumber daya** , **papan jadwal** , dan filter **asisten jadwal**.</span><span class="sxs-lookup"><span data-stu-id="1e0f0-114">These rating values are shown on the **Resource Requirements** , **Schedule Board** , and **Schedule Assistant** filters.</span></span>

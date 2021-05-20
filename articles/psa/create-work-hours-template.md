---
title: Membuat template jam kerja
description: Topik ini mendeskripsikan bagaimana membuat template jam kerja di Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981259"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="ebe3c-103">Buat template jam kerja (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ebe3c-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ebe3c-104">Untuk membuat dan mengelola proyek, Anda harus menerapkan template kalender ke proyek.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="ebe3c-105">Template kalender menentukan atribut proyek berikut:</span><span class="sxs-lookup"><span data-stu-id="ebe3c-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="ebe3c-106">Jam kerja, termasuk waktu mulai dan berakhir</span><span class="sxs-lookup"><span data-stu-id="ebe3c-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="ebe3c-107">Hari kerja</span><span class="sxs-lookup"><span data-stu-id="ebe3c-107">Working days</span></span>
- <span data-ttu-id="ebe3c-108">Pengecualian kalender seperti non-hari kerja</span><span class="sxs-lookup"><span data-stu-id="ebe3c-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="ebe3c-109">Template kalender yang diterapkan ke proyek adalah salinan template kalender yang ditentukan dalam pengaturan organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="ebe3c-110">Jika Anda mengubah template kalender, perubahan tersebut tidak akan diterapkan ke jam kerja proyek.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="ebe3c-111">Untuk mengubah jam kerja proyek, template baru harus diterapkan.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="ebe3c-112">Untuk membuat template kalender untuk organisasi Anda, ada dua persyaratan utama:</span><span class="sxs-lookup"><span data-stu-id="ebe3c-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="ebe3c-113">Tentukan jam kerja yang diinginkan dari template menggunakan sumber daya baru atau saat ini yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="ebe3c-114">Buat template kalender baru dan kaitkan template dengan sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="ebe3c-115">**Tentukan jam kerja template**</span><span class="sxs-lookup"><span data-stu-id="ebe3c-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="ebe3c-116">Buka **Sumber Daya** \> **Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="ebe3c-117">Buat sumber daya baru untuk referensi di template kalender, atau pilih sumber daya yang ada.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="ebe3c-118">Pilih tab **Jam Kerja** sumber daya, lalu lengkapi petunjuk dalam [Atur jam kerja untuk sumber daya](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) agar dapat mengkonfigurasi aturan kalender.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="ebe3c-119">**Membuat template kalender baru**</span><span class="sxs-lookup"><span data-stu-id="ebe3c-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="ebe3c-120">Buka **Pengaturan** \> **Template Kalender**.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="ebe3c-121">Pilih **Baru**, lalu masukkan nama, deskripsi, dan sumber daya template.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="ebe3c-122">Bila sumber daya direferensikan di template kalender, salinan kalender sumber daya dikaitkan dengan template kalender.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="ebe3c-123">Jika jam kerja template yang disalin berubah, perubahan tersebut tidak akan diperbanyak ke template kalender.</span><span class="sxs-lookup"><span data-stu-id="ebe3c-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="ebe3c-124">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="ebe3c-124">See Also</span></span>  
 [<span data-ttu-id="ebe3c-125">Konfigurasi sumber daya</span><span class="sxs-lookup"><span data-stu-id="ebe3c-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

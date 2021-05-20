---
title: Menentukan kalender proyek
description: Halaman topik ini menyediakan informasi tentang cara menerapkan template kalender ke proyek untuk melacak jadwal proyek.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981304"
---
# <a name="define-project-calendars"></a><span data-ttu-id="db2eb-103">Menentukan kalender proyek</span><span class="sxs-lookup"><span data-stu-id="db2eb-103">Define project calendars</span></span>

<span data-ttu-id="db2eb-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="db2eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="db2eb-105">Untuk membuat dan mengelola proyek, Anda harus menerapkan template kalender ke proyek.</span><span class="sxs-lookup"><span data-stu-id="db2eb-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="db2eb-106">Template kalender menentukan atribut proyek berikut:</span><span class="sxs-lookup"><span data-stu-id="db2eb-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="db2eb-107">Jam kerja, termasuk waktu mulai dan berakhir</span><span class="sxs-lookup"><span data-stu-id="db2eb-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="db2eb-108">Hari kerja</span><span class="sxs-lookup"><span data-stu-id="db2eb-108">Working days</span></span>
- <span data-ttu-id="db2eb-109">Pengecualian kalender seperti non-hari kerja</span><span class="sxs-lookup"><span data-stu-id="db2eb-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="db2eb-110">Template kalender yang diterapkan ke proyek adalah salinan template kalender yang ditentukan dalam pengaturan organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="db2eb-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="db2eb-111">Jika Anda mengubah template kalender, perubahan tersebut tidak akan diterapkan ke jam kerja proyek.</span><span class="sxs-lookup"><span data-stu-id="db2eb-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="db2eb-112">Untuk mengubah jam kerja proyek, template baru harus diterapkan.</span><span class="sxs-lookup"><span data-stu-id="db2eb-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="db2eb-113">Untuk membuat template kalender untuk organisasi Anda, ada dua persyaratan utama:</span><span class="sxs-lookup"><span data-stu-id="db2eb-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="db2eb-114">Tentukan jam kerja yang diinginkan dari template menggunakan sumber daya baru atau saat ini yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="db2eb-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="db2eb-115">Buat template kalender baru dan kaitkan template dengan sumber daya yang dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="db2eb-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="db2eb-116">**Tentukan jam kerja template**</span><span class="sxs-lookup"><span data-stu-id="db2eb-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="db2eb-117">Buka **Sumber Daya** \> **Sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="db2eb-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="db2eb-118">Buat sumber daya baru untuk referensi di template kalender, atau pilih sumber daya yang ada.</span><span class="sxs-lookup"><span data-stu-id="db2eb-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="db2eb-119">Pilih tab **Jam Kerja** sumber daya, lalu lengkapi petunjuk dalam [Atur jam kerja untuk sumber daya](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) agar dapat mengkonfigurasi aturan kalender.</span><span class="sxs-lookup"><span data-stu-id="db2eb-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="db2eb-120">**Membuat template kalender baru**</span><span class="sxs-lookup"><span data-stu-id="db2eb-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="db2eb-121">Buka **Pengaturan** \> **Template Kalender**.</span><span class="sxs-lookup"><span data-stu-id="db2eb-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="db2eb-122">Pilih **Baru**, lalu masukkan nama, deskripsi, dan sumber daya template.</span><span class="sxs-lookup"><span data-stu-id="db2eb-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="db2eb-123">Bila sumber daya direferensikan di template kalender, salinan kalender sumber daya dikaitkan dengan template kalender.</span><span class="sxs-lookup"><span data-stu-id="db2eb-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="db2eb-124">Jika jam kerja template yang disalin berubah, perubahan tersebut tidak akan diperbanyak ke template kalender.</span><span class="sxs-lookup"><span data-stu-id="db2eb-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="db2eb-125">Sekarang Anda dapat mengaitkan template kerja dengan template kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="db2eb-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]


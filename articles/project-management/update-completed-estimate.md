---
title: Memperbarui perkiraan saat penyelesaian
description: Topik ini menyediakan informasi tentang memperbarui proyeksi upaya pada proyek.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286432"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="7ded5-103">Memperbarui perkiraan saat penyelesaian</span><span class="sxs-lookup"><span data-stu-id="7ded5-103">Update estimate at completion</span></span>

<span data-ttu-id="7ded5-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="7ded5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7ded5-105">biasanya manajer proyek merevisi perkiraan asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="7ded5-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="7ded5-106">Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini.</span><span class="sxs-lookup"><span data-stu-id="7ded5-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="7ded5-107">Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.</span><span class="sxs-lookup"><span data-stu-id="7ded5-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="7ded5-108">Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:</span><span class="sxs-lookup"><span data-stu-id="7ded5-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="7ded5-109">Menimpa estimasi untuk menyelesaikan (ETC) default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="7ded5-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="7ded5-110">Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="7ded5-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="7ded5-111">Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, estimasi untuk menyelesaikan (EAC) tugas, dan persentase progres, serta proyeksi varians upaya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="7ded5-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="7ded5-112">EAC, ETC, dan persentase kemajuan pada ringkasan tugas dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.</span><span class="sxs-lookup"><span data-stu-id="7ded5-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Memperbarui perkiraan saat penyelesaian
description: Topik ini menyediakan informasi tentang memperbarui proyeksi upaya pada proyek.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897770"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="840d3-103">Memperbarui perkiraan saat penyelesaian</span><span class="sxs-lookup"><span data-stu-id="840d3-103">Update estimate at completion</span></span>

<span data-ttu-id="840d3-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="840d3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="840d3-105">biasanya manajer proyek merevisi perkiraan asli pada tugas.</span><span class="sxs-lookup"><span data-stu-id="840d3-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="840d3-106">Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini.</span><span class="sxs-lookup"><span data-stu-id="840d3-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="840d3-107">Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.</span><span class="sxs-lookup"><span data-stu-id="840d3-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="840d3-108">Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:</span><span class="sxs-lookup"><span data-stu-id="840d3-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="840d3-109">Menimpa estimasi untuk menyelesaikan (ETC) default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="840d3-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="840d3-110">Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="840d3-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="840d3-111">Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, estimasi untuk menyelesaikan (EAC) tugas, dan persentase progres, serta proyeksi varians upaya pada tugas.</span><span class="sxs-lookup"><span data-stu-id="840d3-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="840d3-112">EAC, ETC, dan persentase kemajuan pada ringkasan tugas dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.</span><span class="sxs-lookup"><span data-stu-id="840d3-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>

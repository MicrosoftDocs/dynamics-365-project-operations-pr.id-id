---
title: Sekilas mode manajemen sumber daya
description: Topik ini menyediakan informasi tentang fungsionalitas manajemen sumber daya di Dynamics 365 Project operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4a8e605109e48b50da68abeee989f8ac8d3d659c
ms.sourcegitcommit: cf79185c8c84c55fbae55f9cfc1b17840e072b49
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930095"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="444cc-103">Sekilas mode manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="444cc-103">Resource management modes overview</span></span>

<span data-ttu-id="444cc-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="444cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="444cc-105">Dynamics 365 Project Operations mendukung dua mode agar Anda dapat mengeksekusi alur Pemesanan secara keseluruhan.</span><span class="sxs-lookup"><span data-stu-id="444cc-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="444cc-106">Mode manajemen didefinisikan sebagai parameter proyek dan dapat dimodifikasi jika bisnis Anda memerlukan perubahan.</span><span class="sxs-lookup"><span data-stu-id="444cc-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="444cc-107">Mode Pusat</span><span class="sxs-lookup"><span data-stu-id="444cc-107">Central mode</span></span>
<span data-ttu-id="444cc-108">Untuk organisasi yang memusatkan alokasi sumber daya ke proyek, mode pusat menyediakan cara untuk memastikan manajer proyek dapat menentukan persyaratan sumber daya di tingkat proyek.</span><span class="sxs-lookup"><span data-stu-id="444cc-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="444cc-109">Pemenuhan persyaratan sumber daya didelegasikan ke manajer sumber daya.</span><span class="sxs-lookup"><span data-stu-id="444cc-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="444cc-110">Manajer proyek dapat menerima atau menolak sumber daya yang diusulkan oleh Manajer sumber daya.</span><span class="sxs-lookup"><span data-stu-id="444cc-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Mode Pusat](./media/resource-management-central.png)

<span data-ttu-id="444cc-112">Untuk mengelola sumber daya dengan mode pusat, lihat:</span><span class="sxs-lookup"><span data-stu-id="444cc-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="444cc-113">Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="444cc-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="444cc-114">Memesan sumber daya bernama dari persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="444cc-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="444cc-115">Mengajukan permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="444cc-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="444cc-116">Memenuhi permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="444cc-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="444cc-117">Menerima atau menolak sumber daya proyek yang diusulkan dari permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="444cc-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="444cc-118">Mode hibrida</span><span class="sxs-lookup"><span data-stu-id="444cc-118">Hybrid mode</span></span>
<span data-ttu-id="444cc-119">Untuk organisasi yang memerlukan fleksibilitas dalam alokasi sumber daya, mode hibrida memungkinkan untuk manajer proyek dan manajer sumber daya kemampuan untuk memesan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="444cc-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Mode hibrida](./media/resource-management-hybrid.png)

<span data-ttu-id="444cc-121">Selain proses mode pusat yang didukung, lihat topik berikut untuk mengelola semua alur Pemesanan yang didukung lainnya dalam mode hibrida:</span><span class="sxs-lookup"><span data-stu-id="444cc-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="444cc-122">Pesan sumber daya langsung untuk proyek:</span><span class="sxs-lookup"><span data-stu-id="444cc-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="444cc-123">Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas</span><span class="sxs-lookup"><span data-stu-id="444cc-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="444cc-124">Pesan sumber daya dari persyaratan sumber daya:</span><span class="sxs-lookup"><span data-stu-id="444cc-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="444cc-125">Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="444cc-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="444cc-126">Memesan sumber daya bernama dari persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="444cc-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)

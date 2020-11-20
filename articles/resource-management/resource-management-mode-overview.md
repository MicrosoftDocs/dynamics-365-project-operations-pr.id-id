---
title: Sekilas mode manajemen sumber daya
description: Topik ini menyediakan informasi tentang fungsionalitas manajemen sumber daya di Dynamics 365 Project operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118522"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="df2a7-103">Sekilas mode manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="df2a7-103">Resource management modes overview</span></span>

<span data-ttu-id="df2a7-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="df2a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="df2a7-105">Dynamics 365 Project Operations mendukung dua mode agar Anda dapat mengeksekusi alur Pemesanan secara keseluruhan.</span><span class="sxs-lookup"><span data-stu-id="df2a7-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="df2a7-106">Mode manajemen didefinisikan sebagai parameter proyek dan dapat dimodifikasi jika bisnis Anda memerlukan perubahan.</span><span class="sxs-lookup"><span data-stu-id="df2a7-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="df2a7-107">Mode Pusat</span><span class="sxs-lookup"><span data-stu-id="df2a7-107">Central mode</span></span>
<span data-ttu-id="df2a7-108">Untuk organisasi yang memusatkan alokasi sumber daya ke proyek, mode pusat menyediakan cara untuk memastikan manajer proyek dapat menentukan persyaratan sumber daya di tingkat proyek.</span><span class="sxs-lookup"><span data-stu-id="df2a7-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="df2a7-109">Pemenuhan persyaratan sumber daya didelegasikan ke manajer sumber daya.</span><span class="sxs-lookup"><span data-stu-id="df2a7-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="df2a7-110">Manajer proyek dapat menerima atau menolak sumber daya yang diusulkan oleh Manajer sumber daya.</span><span class="sxs-lookup"><span data-stu-id="df2a7-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Mode Pusat](./media/resource-management-central.png)

<span data-ttu-id="df2a7-112">Untuk mengelola sumber daya dengan mode pusat, lihat:</span><span class="sxs-lookup"><span data-stu-id="df2a7-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="df2a7-113">Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="df2a7-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="df2a7-114">Memesan sumber daya bernama dari persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="df2a7-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="df2a7-115">Mengajukan permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="df2a7-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="df2a7-116">Memenuhi permintaan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="df2a7-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="df2a7-117">Menerima atau menolak sumber daya proyek yang diusulkan dari permintaan sumber daya</span><span class="sxs-lookup"><span data-stu-id="df2a7-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="df2a7-118">Mode hibrida</span><span class="sxs-lookup"><span data-stu-id="df2a7-118">Hybrid mode</span></span>
<span data-ttu-id="df2a7-119">Untuk organisasi yang memerlukan fleksibilitas dalam alokasi sumber daya, mode hibrida memungkinkan untuk manajer proyek dan manajer sumber daya kemampuan untuk memesan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="df2a7-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Mode hibrida](./media/resource-management-hybrid.png)

<span data-ttu-id="df2a7-121">Selain proses mode pusat yang didukung, lihat topik berikut untuk mengelola semua alur Pemesanan yang didukung lainnya dalam mode hibrida:</span><span class="sxs-lookup"><span data-stu-id="df2a7-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="df2a7-122">Pesan sumber daya langsung untuk proyek:</span><span class="sxs-lookup"><span data-stu-id="df2a7-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="df2a7-123">Pesan sumber daya yang dapat dipesan bernama ke tim proyek dan tetapkan tugas</span><span class="sxs-lookup"><span data-stu-id="df2a7-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="df2a7-124">Pesan sumber daya dari persyaratan sumber daya:</span><span class="sxs-lookup"><span data-stu-id="df2a7-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="df2a7-125">Menetapkan sumber daya generik yang dapat dipesan ke tugas dan membuat persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="df2a7-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="df2a7-126">Memesan sumber daya bernama dari persyaratan sumber daya</span><span class="sxs-lookup"><span data-stu-id="df2a7-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)

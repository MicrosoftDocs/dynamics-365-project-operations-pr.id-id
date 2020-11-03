---
title: Pesanan penjualan proyek untuk proyek waktu dan material
description: Topik ini menjelaskan cara membuat pesanan penjualan berbasis proyek untuk proyek waktu dan material.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078469"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="9b5e2-103">Pesanan penjualan proyek untuk proyek waktu dan material</span><span class="sxs-lookup"><span data-stu-id="9b5e2-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9b5e2-104">Topik ini menjelaskan cara membuat pesanan penjualan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="9b5e2-105">Pesanan penjualan hanya dapat dibuat untuk proyek dengan jenis **waktu dan material**.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="9b5e2-106">Jika proyek waktu dan material memiliki beberapa sumber pendanaan pada kontrak proyek, Anda harus mengaktifkan parameter **Izinkan pesanan penjualan untuk proyek dengan beberapa sumber pendanaan** pada halaman **manajemen proyek dan parameter akuntansi**.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="9b5e2-107">Dukungan untuk pesanan penjualan proyek dengan beberapa sumber pendanaan tersedia mulai dari rilis aplikasi 10.0.2 dan lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="9b5e2-108">Parameter untuk mengaktifkan dukungan untuk pesanan penjualan proyek dengan beberapa sumber pendanaan akan dihapus di gelombang rilis 2020 April, setelah itu fungsi akan selalu diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="9b5e2-109">Anda dapat membuat pesanan penjualan berbasis proyek dengan dua cara:</span><span class="sxs-lookup"><span data-stu-id="9b5e2-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="9b5e2-110">Buka proyek itu sendiri.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-110">Go to the project itself.</span></span> <span data-ttu-id="9b5e2-111">Pada panel tindakan, pilih **kelola > tugas Item > pesanan penjualan**.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="9b5e2-112">Informasi proyek akan default ke pesanan penjualan dari proyek.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="9b5e2-113">Jika kontrak proyek memiliki lebih dari satu sumber pendanaan, Anda harus memilih sumber dana untuk menetapkan pelanggan untuk pesanan penjualan.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="9b5e2-114">Jika hanya ada satu sumber pendanaan untuk proyek, pelanggan akan secara otomatis diatur.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="9b5e2-115">Buka halaman daftar **semua pesanan penjualan** dan buat pesanan penjualan baru.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="9b5e2-116">Anda harus memilih proyek untuk pesanan penjualan.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="9b5e2-117">Setelah proyek dipilih, pelanggan akan diatur dari sumber pendanaan atau Anda perlu memilih sumber pendanaan jika kontrak proyek memiliki beberapa sumber pendanaan.</span><span class="sxs-lookup"><span data-stu-id="9b5e2-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>


---
title: Menyebarkan penyebaran Project Operations Lite - menangani faktur proforma
description: Topik ini menyediakan informasi tentang cara menginstal penawaran penyebaran Project operation lite ke faktur proforma.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e938876d459b3f6dfedd90e57e3042cda96bffb7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078348"
---
# <a name="deploy-project-operations-lite-deployment--deal-to-proforma-invoicing"></a><span data-ttu-id="3ad78-103">Menyebarkan penyebaran Project Operations Lite - menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="3ad78-103">Deploy Project Operations Lite deployment – deal to proforma invoicing</span></span>

<span data-ttu-id="3ad78-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="3ad78-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3ad78-105">Project Operations mendukung beberapa model penyebaran.</span><span class="sxs-lookup"><span data-stu-id="3ad78-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="3ad78-106">Untuk menentukan model penyebaran terbaik, lihat [jenis penyebaran](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="3ad78-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="3ad78-107">Penyebaran ini, penawaran penyebaran sederhana-untuk faktur proforma, menghasilkan **penyebaran Project Operations Common Data Service saja**.</span><span class="sxs-lookup"><span data-stu-id="3ad78-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="3ad78-108">Menginstal Project Operations ke lingkungan CDS baru</span><span class="sxs-lookup"><span data-stu-id="3ad78-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="3ad78-109">Instal ke lingkungan CDS yang ada</span><span class="sxs-lookup"><span data-stu-id="3ad78-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="3ad78-110">Menginstal Project Operations ke lingkungan CDS baru</span><span class="sxs-lookup"><span data-stu-id="3ad78-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="3ad78-111">Sebagai [administrator global atau Power Platform](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, buat lingkungan CDS baru di [Pusat admin powerplatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="3ad78-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="3ad78-112">Pastikan bahwa **database CDS** dan **aplikasi Dynamics 365** diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="3ad78-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="3ad78-113">Untuk informasi lebih lanjut, lihat [membuat dan mengelola lingkungan di pusat admin Power Platform](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="3ad78-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="3ad78-114">Pilih **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3ad78-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="3ad78-115">Menginstal Project Operations ke lingkungan CDS lama</span><span class="sxs-lookup"><span data-stu-id="3ad78-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="3ad78-116">Sebagai [administrator Power Platform atau global](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) dengan lisensi Project Operations, Cari lingkungan di [Pusat admin powerplatform](https://admin.powerplatform.com) tempat Anda ingin menginstal Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3ad78-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="3ad78-117">Instal **Microsoft Dynamics 365 Project Operations** dari daftar penyebaran aplikasi Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3ad78-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="3ad78-118">Untuk informasi lebih lanjut, lihat [Kelola aplikasi Dynamics 365](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="3ad78-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>



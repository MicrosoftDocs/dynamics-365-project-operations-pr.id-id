---
title: Menentukan jenis penyebaran Anda
description: Topik ini memberikan informasi untuk membantu Anda menentukan jenis penyebaran Project operations yang benar untuk perusahaan Anda.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078488"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="48c34-103">Menentukan jenis penyebaran Anda</span><span class="sxs-lookup"><span data-stu-id="48c34-103">Determine your deployment type</span></span>

<span data-ttu-id="48c34-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="48c34-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48c34-105">Setelah Anda membeli lisensi, mulai di sini untuk menentukan model penyebaran terbaik dari Dynamics 365 Project Operations menggunakan [alur penginstalan terpandu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="48c34-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="48c34-106">Setelah Anda menyelesaikan alur penginstalan terpandu, Anda akan diarahkan ke Portal manajemen yang benar untuk menyelesaikan penginstalan.</span><span class="sxs-lookup"><span data-stu-id="48c34-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="48c34-107">Lihat rincian penyebaran untuk menyelesaikan penginstalan.</span><span class="sxs-lookup"><span data-stu-id="48c34-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="48c34-108">Pelanggan Dynamics yang lama menggunakan Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="48c34-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="48c34-109">Project Operations mencakup kemampuan yang disertakan dengan Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="48c34-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="48c34-110">Jalur peningkatan akan dirilis untuk pelanggan ini di masa mendatang.</span><span class="sxs-lookup"><span data-stu-id="48c34-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="48c34-111">Pelanggan lama Dynamics 365 Finance menggunakan manajemen proyek dan akuntansi</span><span class="sxs-lookup"><span data-stu-id="48c34-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="48c34-112">Pelanggan Finance yang ada yang menggunakan fungsi manajemen proyek dan akuntansi dapat terus menggunakan ini sebagaimana adanya.</span><span class="sxs-lookup"><span data-stu-id="48c34-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="48c34-113">Lihat [Project Operations untuk skenario pesanan dengan stok/produksi](#pma).</span><span class="sxs-lookup"><span data-stu-id="48c34-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="48c34-114">Jenis Penyebaran</span><span class="sxs-lookup"><span data-stu-id="48c34-114">Deployment types</span></span>
<span data-ttu-id="48c34-115">Project Operations mendukung beberapa pilihan penyebaran agar sesuai dengan kebutuhan Anda.</span><span class="sxs-lookup"><span data-stu-id="48c34-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="48c34-116">Apakah Anda adalah pelanggan Dynamics 365 baru atau lama, Project Operations dapat mendukung kebutuhan Anda.</span><span class="sxs-lookup"><span data-stu-id="48c34-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="48c34-117">[Kuesioner penyebaran](https://aka.ms/provisionprojectoperations) kami akan membantu Anda menentukan penyebaran yang tepat.</span><span class="sxs-lookup"><span data-stu-id="48c34-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="48c34-118">Hasil akan memandu Anda menuju salah satu jenis penyebaran berikut:</span><span class="sxs-lookup"><span data-stu-id="48c34-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="48c34-119">Penyebaran sederhana – menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="48c34-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="48c34-120">Project Operations untuk skenario sumber daya/tanpa stok</span><span class="sxs-lookup"><span data-stu-id="48c34-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="48c34-121">Project Operations untuk skenario pesanan dengan stok/produksi</span><span class="sxs-lookup"><span data-stu-id="48c34-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="48c34-122">Project Operations mendukung skenario pesanan dengan stok/produksi dan skenario non-stok/berbasis sumber daya pada lingkungan yang sama melalui konfigurasi tingkat entitas hukum.</span><span class="sxs-lookup"><span data-stu-id="48c34-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="48c34-123">Misalnya, Aswono dapat menggunakan kemampuan pesanan produksi/penuh di fasilitas produksi AS (entitas hukum = Aswono Manufacturing Indonesia).</span><span class="sxs-lookup"><span data-stu-id="48c34-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="48c34-124">Aswono dapat menggunakan kemampuan berbasis sumber daya/non-stok di fasilitas layanan Aswono Lengan Robotika di Inggris (entitas hukum = Aswono Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="48c34-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="48c34-125">Penyebaran sederhana - menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="48c34-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="48c34-126">Penyebaran sederhana mencakup kemampuan berikut:</span><span class="sxs-lookup"><span data-stu-id="48c34-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="48c34-127">Perencanaan proyek menggunakan Microsoft Project untuk web</span><span class="sxs-lookup"><span data-stu-id="48c34-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="48c34-128">Harga multidimensi</span><span class="sxs-lookup"><span data-stu-id="48c34-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="48c34-129">Manajemen sumber daya terpadu</span><span class="sxs-lookup"><span data-stu-id="48c34-129">Unified Resource Management</span></span>
- <span data-ttu-id="48c34-130">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="48c34-130">Time Tracking</span></span>
- <span data-ttu-id="48c34-131">Pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="48c34-131">Basic Expense</span></span>
- <span data-ttu-id="48c34-132">Proposal faktur</span><span class="sxs-lookup"><span data-stu-id="48c34-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="48c34-133">Langkah-langkah penyebaran</span><span class="sxs-lookup"><span data-stu-id="48c34-133">Deployment steps</span></span>
<span data-ttu-id="48c34-134">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="48c34-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="48c34-135">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](lite-preview-subscription-sign-up.md) dan [penyediaan lingkungan baru](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="48c34-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="48c34-136">Project Operations untuk skenario sumber daya/tanpa stok</span><span class="sxs-lookup"><span data-stu-id="48c34-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="48c34-137">Project Operations untuk skenario sumber daya/non-stok mencakup kemampuan berikut:</span><span class="sxs-lookup"><span data-stu-id="48c34-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="48c34-138">Perencanaan proyek menggunakan Microsoft Project untuk web</span><span class="sxs-lookup"><span data-stu-id="48c34-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="48c34-139">Harga multidimensi</span><span class="sxs-lookup"><span data-stu-id="48c34-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="48c34-140">Manajemen sumber daya terpadu</span><span class="sxs-lookup"><span data-stu-id="48c34-140">Unified Resource Management</span></span>
- <span data-ttu-id="48c34-141">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="48c34-141">Time Tracking</span></span>
- <span data-ttu-id="48c34-142">Pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="48c34-142">Basic Expense</span></span>
- <span data-ttu-id="48c34-143">Pengeluaran Penuh</span><span class="sxs-lookup"><span data-stu-id="48c34-143">Full Expense</span></span>
- <span data-ttu-id="48c34-144">OCR Tanda Terima</span><span class="sxs-lookup"><span data-stu-id="48c34-144">Receipt OCR</span></span>
- <span data-ttu-id="48c34-145">Faktur Lengkap</span><span class="sxs-lookup"><span data-stu-id="48c34-145">Full Invoicing</span></span>
- <span data-ttu-id="48c34-146">Pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="48c34-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="48c34-147">Langkah-langkah penyebaran</span><span class="sxs-lookup"><span data-stu-id="48c34-147">Deployment steps</span></span>
<span data-ttu-id="48c34-148">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="48c34-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="48c34-149">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](resource-sign-up-preview-subscription.md) dan [penyediaan lingkungan baru](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="48c34-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="48c34-150">Project Operations untuk skenario pesanan dengan stok/produksi</span><span class="sxs-lookup"><span data-stu-id="48c34-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="48c34-151">Perencanaan proyek dengan WBS</span><span class="sxs-lookup"><span data-stu-id="48c34-151">Project planning using WBS</span></span>
- <span data-ttu-id="48c34-152">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="48c34-152">Resource Management</span></span>
- <span data-ttu-id="48c34-153">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="48c34-153">Time Tracking</span></span>
- <span data-ttu-id="48c34-154">Pengeluaran Penuh</span><span class="sxs-lookup"><span data-stu-id="48c34-154">Full Expense</span></span>
- <span data-ttu-id="48c34-155">OCR Tanda Terima</span><span class="sxs-lookup"><span data-stu-id="48c34-155">Receipt OCR</span></span>
- <span data-ttu-id="48c34-156">Faktur Lengkap</span><span class="sxs-lookup"><span data-stu-id="48c34-156">Full Invoicing</span></span>
- <span data-ttu-id="48c34-157">Pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="48c34-157">Revenue Recognition</span></span>
- <span data-ttu-id="48c34-158">Pesanan Produksi</span><span class="sxs-lookup"><span data-stu-id="48c34-158">Production Orders</span></span>
- <span data-ttu-id="48c34-159">Dukungan material</span><span class="sxs-lookup"><span data-stu-id="48c34-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="48c34-160">Langkah-langkah penyebaran</span><span class="sxs-lookup"><span data-stu-id="48c34-160">Deployment steps</span></span>
<span data-ttu-id="48c34-161">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="48c34-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="48c34-162">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) dan [penyediaan lingkungan baru](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="48c34-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 


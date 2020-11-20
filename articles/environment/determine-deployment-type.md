---
title: Menentukan jenis penyebaran Anda
description: Topik ini memberikan informasi untuk membantu Anda menentukan jenis penyebaran Project operations yang benar untuk perusahaan Anda.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401222"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="f6732-103">Menentukan jenis penyebaran Anda</span><span class="sxs-lookup"><span data-stu-id="f6732-103">Determine your deployment type</span></span>

<span data-ttu-id="f6732-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="f6732-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f6732-105">Setelah Anda membeli lisensi, mulai di sini untuk menentukan model penyebaran terbaik dari Dynamics 365 Project Operations menggunakan [alur penginstalan terpandu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f6732-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="f6732-106">Setelah Anda menyelesaikan alur penginstalan terpandu, Anda akan diarahkan ke Portal manajemen yang benar untuk menyelesaikan penginstalan.</span><span class="sxs-lookup"><span data-stu-id="f6732-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="f6732-107">Lihat rincian penyebaran untuk menyelesaikan penginstalan.</span><span class="sxs-lookup"><span data-stu-id="f6732-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="f6732-108">Pelanggan Dynamics yang lama menggunakan Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="f6732-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="f6732-109">Project Operations mencakup kemampuan yang disertakan dengan Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="f6732-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="f6732-110">Jalur peningkatan akan dirilis untuk pelanggan ini di rilis 2021 gelombang 1.</span><span class="sxs-lookup"><span data-stu-id="f6732-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="f6732-111">Pelanggan lama Dynamics 365 Finance menggunakan manajemen proyek dan akuntansi</span><span class="sxs-lookup"><span data-stu-id="f6732-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="f6732-112">Pelanggan Finance yang ada yang menggunakan fungsi manajemen proyek dan akuntansi dapat terus menggunakannya sebagaimana adanya.</span><span class="sxs-lookup"><span data-stu-id="f6732-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="f6732-113">Lihat [Project Operations untuk skenario pesanan dengan stok/produksi](#pma).</span><span class="sxs-lookup"><span data-stu-id="f6732-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="f6732-114">Jenis Penyebaran</span><span class="sxs-lookup"><span data-stu-id="f6732-114">Deployment types</span></span>
<span data-ttu-id="f6732-115">Project Operations mendukung beberapa pilihan penyebaran agar sesuai dengan kebutuhan Anda.</span><span class="sxs-lookup"><span data-stu-id="f6732-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="f6732-116">Apakah Anda adalah pelanggan Dynamics 365 baru atau lama, Project Operations dapat mendukung kebutuhan Anda.</span><span class="sxs-lookup"><span data-stu-id="f6732-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="f6732-117">[Kuesioner penyebaran](https://aka.ms/provisionprojectoperations) kami akan membantu Anda menentukan penyebaran yang tepat.</span><span class="sxs-lookup"><span data-stu-id="f6732-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="f6732-118">Hasil akan memandu Anda menuju salah satu jenis penyebaran berikut:</span><span class="sxs-lookup"><span data-stu-id="f6732-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="f6732-119">Penyebaran sederhana – menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="f6732-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="f6732-120">Project Operations untuk skenario sumber daya/tanpa stok</span><span class="sxs-lookup"><span data-stu-id="f6732-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="f6732-121">Project Operations untuk skenario pesanan dengan stok/produksi</span><span class="sxs-lookup"><span data-stu-id="f6732-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="f6732-122">Project Operations mendukung skenario pesanan dengan stok/produksi dan skenario non-stok/berbasis sumber daya pada lingkungan yang sama melalui konfigurasi tingkat entitas hukum.</span><span class="sxs-lookup"><span data-stu-id="f6732-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="f6732-123">Misalnya, Aswono dapat menggunakan kemampuan pesanan produksi/penuh di fasilitas produksi AS (entitas hukum = Aswono Manufacturing Indonesia).</span><span class="sxs-lookup"><span data-stu-id="f6732-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="f6732-124">Aswono dapat menggunakan kemampuan berbasis sumber daya/non-stok di fasilitas layanan Aswono Lengan Robotika di Inggris (entitas hukum = Aswono Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="f6732-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="f6732-125">Penyebaran sederhana - menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="f6732-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="f6732-126">Penyebaran sederhana mencakup kemampuan berikut:</span><span class="sxs-lookup"><span data-stu-id="f6732-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="f6732-127">Proses penjualan untuk proyek yang memperluas pengalaman aplikasi Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f6732-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="f6732-128">Perencanaan proyek menggunakan Microsoft Project untuk web</span><span class="sxs-lookup"><span data-stu-id="f6732-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f6732-129">Harga multidimensi</span><span class="sxs-lookup"><span data-stu-id="f6732-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f6732-130">Manajemen sumber daya terpadu</span><span class="sxs-lookup"><span data-stu-id="f6732-130">Unified resource management</span></span>
- <span data-ttu-id="f6732-131">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="f6732-131">Time tracking</span></span>
- <span data-ttu-id="f6732-132">Pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="f6732-132">Basic expense</span></span>
- <span data-ttu-id="f6732-133">faktur Proforma dan sisi pelanggan</span><span class="sxs-lookup"><span data-stu-id="f6732-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="f6732-134">Langkah-langkah penyebaran</span><span class="sxs-lookup"><span data-stu-id="f6732-134">Deployment steps</span></span>
<span data-ttu-id="f6732-135">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f6732-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f6732-136">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](lite-preview-subscription-sign-up.md) dan [penyediaan lingkungan baru](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="f6732-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="f6732-137">Project Operations untuk skenario sumber daya/tanpa stok</span><span class="sxs-lookup"><span data-stu-id="f6732-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="f6732-138">Project Operations untuk skenario sumber daya/non-stok mencakup kemampuan berikut:</span><span class="sxs-lookup"><span data-stu-id="f6732-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="f6732-139">Proses penjualan untuk proyek yang memperluas aplikasi Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="f6732-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="f6732-140">Perencanaan proyek menggunakan Microsoft Project untuk web</span><span class="sxs-lookup"><span data-stu-id="f6732-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="f6732-141">Harga multidimensi</span><span class="sxs-lookup"><span data-stu-id="f6732-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="f6732-142">Manajemen sumber daya terpadu</span><span class="sxs-lookup"><span data-stu-id="f6732-142">Unified resource management</span></span>
- <span data-ttu-id="f6732-143">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="f6732-143">Time tracking</span></span>
- <span data-ttu-id="f6732-144">Pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="f6732-144">Basic expense</span></span>
- <span data-ttu-id="f6732-145">Pengeluaran penuh</span><span class="sxs-lookup"><span data-stu-id="f6732-145">Full expense</span></span>
- <span data-ttu-id="f6732-146">OCR Tanda Terima</span><span class="sxs-lookup"><span data-stu-id="f6732-146">Receipt OCR</span></span>
- <span data-ttu-id="f6732-147">faktur Proforma dan sisi pelanggan</span><span class="sxs-lookup"><span data-stu-id="f6732-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="f6732-148">Pengakuan pendapatan untuk proyek</span><span class="sxs-lookup"><span data-stu-id="f6732-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f6732-149">Langkah-langkah penyebaran</span><span class="sxs-lookup"><span data-stu-id="f6732-149">Deployment steps</span></span>
<span data-ttu-id="f6732-150">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f6732-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f6732-151">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](resource-sign-up-preview-subscription.md) dan [penyediaan lingkungan baru](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="f6732-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="f6732-152">Project Operations untuk skenario pesanan dengan stok/produksi</span><span class="sxs-lookup"><span data-stu-id="f6732-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="f6732-153">Perencanaan proyek dengan WBS</span><span class="sxs-lookup"><span data-stu-id="f6732-153">Project planning using WBS</span></span>
- <span data-ttu-id="f6732-154">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="f6732-154">Resource Management</span></span>
- <span data-ttu-id="f6732-155">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="f6732-155">Time Tracking</span></span>
- <span data-ttu-id="f6732-156">Pengeluaran Penuh</span><span class="sxs-lookup"><span data-stu-id="f6732-156">Full Expense</span></span>
- <span data-ttu-id="f6732-157">OCR Tanda Terima</span><span class="sxs-lookup"><span data-stu-id="f6732-157">Receipt OCR</span></span>
- <span data-ttu-id="f6732-158">Faktur Lengkap</span><span class="sxs-lookup"><span data-stu-id="f6732-158">Full Invoicing</span></span>
- <span data-ttu-id="f6732-159">Pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="f6732-159">Revenue Recognition</span></span>
- <span data-ttu-id="f6732-160">Pesanan Produksi</span><span class="sxs-lookup"><span data-stu-id="f6732-160">Production Orders</span></span>
- <span data-ttu-id="f6732-161">Dukungan material</span><span class="sxs-lookup"><span data-stu-id="f6732-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="f6732-162">Langkah-langkah penyebaran</span><span class="sxs-lookup"><span data-stu-id="f6732-162">Deployment steps</span></span>
<span data-ttu-id="f6732-163">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="f6732-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="f6732-164">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) dan [penyediaan lingkungan baru](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="f6732-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 


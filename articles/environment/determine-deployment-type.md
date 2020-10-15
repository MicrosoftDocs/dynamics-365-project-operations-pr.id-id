---
title: Jenis Penyebaran
description: Topik ini memberikan informasi untuk membantu Anda menentukan jenis penyebaran Project operations yang benar untuk perusahaan Anda.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948918"
---
# <a name="deployment-types"></a><span data-ttu-id="62d00-103">Jenis Penyebaran</span><span class="sxs-lookup"><span data-stu-id="62d00-103">Deployment types</span></span>

<span data-ttu-id="62d00-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="62d00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="62d00-105">Setelah Anda membeli lisensi, mulai di sini untuk menentukan model penyebaran terbaik dari Dynamics 365 Project Operations menggunakan [alur penginstalan terpandu](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="62d00-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="62d00-106">Setelah Anda menyelesaikan alur penginstalan terpandu, Anda akan diarahkan ke Portal manajemen yang benar untuk menyelesaikan penginstalan.</span><span class="sxs-lookup"><span data-stu-id="62d00-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="62d00-107">Lihat rincian penyebaran di bawah untuk menyelesaikan penginstalan.</span><span class="sxs-lookup"><span data-stu-id="62d00-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="62d00-108">Pelanggan Dynamics yang lama menggunakan Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="62d00-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="62d00-109">Project Operations mencakup kemampuan yang disertakan dengan Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="62d00-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="62d00-110">Jalur peningkatan akan dirilis untuk pelanggan ini di masa mendatang.</span><span class="sxs-lookup"><span data-stu-id="62d00-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="62d00-111">Pelanggan lama Dynamics 365 Finance menggunakan manajemen proyek dan akuntansi</span><span class="sxs-lookup"><span data-stu-id="62d00-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="62d00-112">Pelanggan Finance yang ada yang menggunakan fungsi manajemen proyek dan akuntansi dapat terus menggunakan ini sebagaimana adanya.</span><span class="sxs-lookup"><span data-stu-id="62d00-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="62d00-113">Lihat [Project Operations untuk skenario pesanan dengan stok/produksi](#pma).</span><span class="sxs-lookup"><span data-stu-id="62d00-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="62d00-114">Project Operations mendukung beberapa pilihan penyebaran agar sesuai dengan kebutuhan Anda.</span><span class="sxs-lookup"><span data-stu-id="62d00-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="62d00-115">Apakah Anda adalah pelanggan Dynamics 365 baru atau lama, Project Operations dapat mendukung kebutuhan Anda.</span><span class="sxs-lookup"><span data-stu-id="62d00-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="62d00-116">[Kuesioner penyebaran](https://aka.ms/provisionprojectoperations) kami akan membantu Anda menentukan penyebaran yang tepat.</span><span class="sxs-lookup"><span data-stu-id="62d00-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="62d00-117">Hasil akan memandu Anda menuju salah satu jenis penyebaran berikut:</span><span class="sxs-lookup"><span data-stu-id="62d00-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="62d00-118">Penyebaran sederhana – menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="62d00-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="62d00-119">Project Operations untuk skenario sumber daya/tanpa stok</span><span class="sxs-lookup"><span data-stu-id="62d00-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="62d00-120">Project Operations untuk skenario pesanan dengan stok/produksi</span><span class="sxs-lookup"><span data-stu-id="62d00-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="62d00-121">Project Operations mendukung skenario pesanan dengan stok/produksi dan skenario non-stok/berbasis sumber daya pada lingkungan yang sama melalui konfigurasi tingkat entitas hukum.</span><span class="sxs-lookup"><span data-stu-id="62d00-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="62d00-122">Misalnya, Aswono dapat meningkatkan kemampuan pesanan produksi dan stok di fasilitas produksi AS (entitas hukum = Aswono Manufacturing United States) dan kemampuan berbasis sumber daya/non-stok di fasilitas layanan lengan Robotika Aswono mereka di Inggris (entitas hukum = Aswono Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="62d00-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="62d00-123"><a name="lite"><a/>Penyebaran sederhana - menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="62d00-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="62d00-124">Penyebaran sederhana mencakup kemampuan berikut:</span><span class="sxs-lookup"><span data-stu-id="62d00-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="62d00-125">Perencanaan proyek menggunakan Microsoft Project untuk web</span><span class="sxs-lookup"><span data-stu-id="62d00-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="62d00-126">Harga multidimensi</span><span class="sxs-lookup"><span data-stu-id="62d00-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="62d00-127">Manajemen sumber daya terpadu</span><span class="sxs-lookup"><span data-stu-id="62d00-127">Unified Resource Management</span></span>
- <span data-ttu-id="62d00-128">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="62d00-128">Time Tracking</span></span>
- <span data-ttu-id="62d00-129">Pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="62d00-129">Basic Expense</span></span>
- <span data-ttu-id="62d00-130">Proposal faktur</span><span class="sxs-lookup"><span data-stu-id="62d00-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="62d00-131">Langkah-langkah penyebaran:</span><span class="sxs-lookup"><span data-stu-id="62d00-131">Deployment steps:</span></span>
<span data-ttu-id="62d00-132">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="62d00-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="62d00-133">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](lite-preview-subscription-sign-up.md) dan [penyediaan lingkungan baru](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="62d00-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="62d00-134"><a name="integrated"><a/>Project Operations untuk skenario sumber daya/tanpa stok</span><span class="sxs-lookup"><span data-stu-id="62d00-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="62d00-135">Project Operations untuk skenario sumber daya/non-stok mencakup kemampuan berikut:</span><span class="sxs-lookup"><span data-stu-id="62d00-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="62d00-136">Perencanaan proyek menggunakan Microsoft Project untuk web</span><span class="sxs-lookup"><span data-stu-id="62d00-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="62d00-137">Harga multidimensi</span><span class="sxs-lookup"><span data-stu-id="62d00-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="62d00-138">Manajemen sumber daya terpadu</span><span class="sxs-lookup"><span data-stu-id="62d00-138">Unified Resource Management</span></span>
- <span data-ttu-id="62d00-139">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="62d00-139">Time Tracking</span></span>
- <span data-ttu-id="62d00-140">Pengeluaran dasar</span><span class="sxs-lookup"><span data-stu-id="62d00-140">Basic Expense</span></span>
- <span data-ttu-id="62d00-141">Pengeluaran Penuh</span><span class="sxs-lookup"><span data-stu-id="62d00-141">Full Expense</span></span>
- <span data-ttu-id="62d00-142">OCR Tanda Terima</span><span class="sxs-lookup"><span data-stu-id="62d00-142">Receipt OCR</span></span>
- <span data-ttu-id="62d00-143">Faktur Lengkap</span><span class="sxs-lookup"><span data-stu-id="62d00-143">Full Invoicing</span></span>
- <span data-ttu-id="62d00-144">Pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="62d00-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="62d00-145">Langkah-langkah penyebaran:</span><span class="sxs-lookup"><span data-stu-id="62d00-145">Deployment steps:</span></span>
<span data-ttu-id="62d00-146">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="62d00-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="62d00-147">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](resource-sign-up-preview-subscription.md) dan [penyediaan lingkungan baru](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="62d00-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="62d00-148">Project Operations untuk skenario pesanan dengan stok/produksi</span><span class="sxs-lookup"><span data-stu-id="62d00-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="62d00-149">Perencanaan proyek dengan WBS</span><span class="sxs-lookup"><span data-stu-id="62d00-149">Project planning using WBS</span></span>
- <span data-ttu-id="62d00-150">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="62d00-150">Resource Management</span></span>
- <span data-ttu-id="62d00-151">Pelacakan Waktu</span><span class="sxs-lookup"><span data-stu-id="62d00-151">Time Tracking</span></span>
- <span data-ttu-id="62d00-152">Pengeluaran Penuh</span><span class="sxs-lookup"><span data-stu-id="62d00-152">Full Expense</span></span>
- <span data-ttu-id="62d00-153">OCR Tanda Terima</span><span class="sxs-lookup"><span data-stu-id="62d00-153">Receipt OCR</span></span>
- <span data-ttu-id="62d00-154">Faktur Lengkap</span><span class="sxs-lookup"><span data-stu-id="62d00-154">Full Invoicing</span></span>
- <span data-ttu-id="62d00-155">Pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="62d00-155">Revenue Recognition</span></span>
- <span data-ttu-id="62d00-156">Pesanan Produksi</span><span class="sxs-lookup"><span data-stu-id="62d00-156">Production Orders</span></span>
- <span data-ttu-id="62d00-157">Dukungan material</span><span class="sxs-lookup"><span data-stu-id="62d00-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="62d00-158">Langkah-langkah penyebaran:</span><span class="sxs-lookup"><span data-stu-id="62d00-158">Deployment steps:</span></span>
<span data-ttu-id="62d00-159">Tentukan model penyebaran Project Operations terbaik menggunakan [kuesioner penyebaran](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="62d00-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="62d00-160">Untuk penyebaran ini, lihat [pendaftaran untuk langganan pratinjau](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) dan [penyediaan lingkungan baru](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="62d00-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 




---
title: Mengelola peluang berbasis proyek
description: Topik ini memberikan informasi tentang cara bekerja dengan peluang yang terkait dengan proyek.
author: rumant
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5ce9ad1458d338d63469c3d6fddb98b9cbbced31
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948395"
---
# <a name="manage-project-based-opportunities"></a><span data-ttu-id="55d2e-103">Mengelola peluang berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="55d2e-103">Manage project-based opportunities</span></span>

<span data-ttu-id="55d2e-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="55d2e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55d2e-105">Perusahaan berbasis proyek biasanya memiliki operasi untuk penyebaran penyebaran di beberapa negara dan geografi.</span><span class="sxs-lookup"><span data-stu-id="55d2e-105">Project-based companies typically have their operations for delivery spread across multiple countries and geographies.</span></span> <span data-ttu-id="55d2e-106">Biaya eksekusi dan pelaksanaan proyek dapat bervariasi berdasarkan geografi atau divisi yang mengelola pelaksanaan.</span><span class="sxs-lookup"><span data-stu-id="55d2e-106">The cost of the project execution and delivery can vary  based on which geography or division manages the delivery.</span></span> <span data-ttu-id="55d2e-107">Pada gilirannya, hal ini dapat berdampak pada margin transaksi.</span><span class="sxs-lookup"><span data-stu-id="55d2e-107">In turn, this can impact the margins of the deal.</span></span> <span data-ttu-id="55d2e-108">Pelaksanaan layanan berbasis proyek biasanya melibatkan sejumlah besar waktu sumber daya manusia, pengeluaran besar untuk perjalanan, biaya material, dan biaya lainnya.</span><span class="sxs-lookup"><span data-stu-id="55d2e-108">Delivery of project-based services typically involves large quantities of human resource time, considerable expenses for travel, material costs, and other expenses.</span></span>

<span data-ttu-id="55d2e-109">Peluang berbasis proyek Dynamics 365 Project Operations didesain dengan ekstensi untuk Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="55d2e-109">Project-based opportunities in Dynamics 365 Project Operations are designed with extensions to Dynamics 365 Sales.</span></span> <span data-ttu-id="55d2e-110">Topik ini memberikan rincian tentang bidang yang berbeda dan logika bisnis yang tercakup dalam fungsi tambahan yang diperlukan oleh perusahaan berbasis proyek untuk mengelola peluang berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="55d2e-110">The topic provides details about the different fields and business logic included in the additional functionality that is required by project-based companies to manage project-based opportunities.</span></span>

## <a name="view-all-project-based-opportunities"></a><span data-ttu-id="55d2e-111">Lihat semua peluang berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="55d2e-111">View all project-based opportunities</span></span>

<span data-ttu-id="55d2e-112">Daftar semua peluang berbasis proyek dapat dilihat dari halaman daftar **peluang**.</span><span class="sxs-lookup"><span data-stu-id="55d2e-112">A list of all the project-based opportunities can be seen from the **Opportunity** list page.</span></span> 

1. <span data-ttu-id="55d2e-113">Buka **Penjualan** > **Peluang**.</span><span class="sxs-lookup"><span data-stu-id="55d2e-113">Go to **Sales** > **Opportunities**.</span></span>
2. <span data-ttu-id="55d2e-114">Gunakan **penukar tampilan** untuk memilih tampilan terfilter lainnya dari peluang.</span><span class="sxs-lookup"><span data-stu-id="55d2e-114">Use the **View switcher** to select other filtered views of the opportunities.</span></span> <span data-ttu-id="55d2e-115">Anda dapat membuat tampilan sendiri dengan kriteria filter kustom untuk mengkonfigurasi tampilan dan pilihan navigasi.</span><span class="sxs-lookup"><span data-stu-id="55d2e-115">You can create your own views with custom filter criteria to configure these views and navigation options.</span></span>

<span data-ttu-id="55d2e-116">Peluang proyek dapat dibuat atau dihapus dari halaman daftar ini atau halaman detail.</span><span class="sxs-lookup"><span data-stu-id="55d2e-116">Project Opportunities can be created or deleted from this list page or the detail page.</span></span>

## <a name="business-process-flow-for-project-based-deals"></a><span data-ttu-id="55d2e-117">Alur proses bisnis untuk transaksi berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="55d2e-117">Business process flow for project-based deals</span></span>

<span data-ttu-id="55d2e-118">Alur proses bisnis berikut didukung untuk transaksi berbasis proyek dalam Project Operations:</span><span class="sxs-lookup"><span data-stu-id="55d2e-118">The following business process flows are supported for project-based deals in Project Operations:</span></span>

- <span data-ttu-id="55d2e-119">Proses bisnis Prospek ke Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-119">Lead to Opportunity business process</span></span>
- <span data-ttu-id="55d2e-120">Proses Penjualan Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-120">Opportunity sales process</span></span>

### <a name="lead-to-opportunity-business-process"></a><span data-ttu-id="55d2e-121">Proses bisnis Prospek ke Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-121">Lead to opportunity business process</span></span> 
<span data-ttu-id="55d2e-122">Proses bisnis prospek ke peluang mendukung tahapan berikut:</span><span class="sxs-lookup"><span data-stu-id="55d2e-122">The lead to opportunity business process supports the following stages:</span></span>

| <span data-ttu-id="55d2e-123">Tahap</span><span class="sxs-lookup"><span data-stu-id="55d2e-123">Stage</span></span> | <span data-ttu-id="55d2e-124">Entitas yang dipetakan</span><span class="sxs-lookup"><span data-stu-id="55d2e-124">Mapped entity</span></span> | <span data-ttu-id="55d2e-125">Fungsi</span><span class="sxs-lookup"><span data-stu-id="55d2e-125">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="55d2e-126">Kualifikasi</span><span class="sxs-lookup"><span data-stu-id="55d2e-126">Qualify</span></span> | <span data-ttu-id="55d2e-127">Prospek</span><span class="sxs-lookup"><span data-stu-id="55d2e-127">Lead</span></span> | <span data-ttu-id="55d2e-128">Kualifikasi prospek untuk membuat akun, kontrak, dan peluang.</span><span class="sxs-lookup"><span data-stu-id="55d2e-128">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="55d2e-129">Kembangkan</span><span class="sxs-lookup"><span data-stu-id="55d2e-129">Develop</span></span> | <span data-ttu-id="55d2e-130">Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-130">Opportunity</span></span> | <span data-ttu-id="55d2e-131">Kembangkan peluang untuk menambahkan informasi lebih lanjut tentang pekerjaan yang terlibat, pemangku kepentingan utama, dan pesaing.</span><span class="sxs-lookup"><span data-stu-id="55d2e-131">Develop the opportunity to add more information on the work involved, key stakeholders, and competition.</span></span> |
| <span data-ttu-id="55d2e-132">Usulkan</span><span class="sxs-lookup"><span data-stu-id="55d2e-132">Propose</span></span> | <span data-ttu-id="55d2e-133">Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-133">Opportunity</span></span> | <span data-ttu-id="55d2e-134">Kembangkan proposal dan Dapatkan persetujuan dari tim peninjauan internal.</span><span class="sxs-lookup"><span data-stu-id="55d2e-134">Develop the proposal and get approval from the internal review team.</span></span> |
| <span data-ttu-id="55d2e-135">Tutup</span><span class="sxs-lookup"><span data-stu-id="55d2e-135">Close</span></span> | <span data-ttu-id="55d2e-136">Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-136">Opportunity</span></span> | <span data-ttu-id="55d2e-137">Menangkan peluang untuk menutup penawaran.</span><span class="sxs-lookup"><span data-stu-id="55d2e-137">Win the opportunity to close the deal.</span></span> |

### <a name="opportunity-sales-process"></a><span data-ttu-id="55d2e-138">Proses Penjualan Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-138">Opportunity sales process</span></span>
<span data-ttu-id="55d2e-139">Proses penjualan peluang dalam Project Operations adalah perpanjangan ke alur bisnis proses penjualan peluang dalam aplikasi Sales.</span><span class="sxs-lookup"><span data-stu-id="55d2e-139">The Opportunity sales process in Project Operations is an extension to the Opportunity sales process business flow in the Sales application.</span></span> <span data-ttu-id="55d2e-140">Proses bisnis ini dirancang secara bawaan untuk mendukung tahapan berikut dalam peluang berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="55d2e-140">This business process is designed out-of-the-box to support the following stages in a project-based opportunity.</span></span>

| <span data-ttu-id="55d2e-141">Tahap</span><span class="sxs-lookup"><span data-stu-id="55d2e-141">Stage</span></span> | <span data-ttu-id="55d2e-142">Entitas yang dipetakan</span><span class="sxs-lookup"><span data-stu-id="55d2e-142">Mapped entity</span></span> | <span data-ttu-id="55d2e-143">Fungsi</span><span class="sxs-lookup"><span data-stu-id="55d2e-143">Functionality</span></span> |
| --- | --- | --- |
| <span data-ttu-id="55d2e-144">Kualifikasi</span><span class="sxs-lookup"><span data-stu-id="55d2e-144">Qualify</span></span> | <span data-ttu-id="55d2e-145">Peluang</span><span class="sxs-lookup"><span data-stu-id="55d2e-145">Opportunity</span></span> | <span data-ttu-id="55d2e-146">Kualifikasi prospek untuk membuat akun, kontrak, dan peluang.</span><span class="sxs-lookup"><span data-stu-id="55d2e-146">Qualify the lead to create an account, contact, and an opportunity.</span></span> |
| <span data-ttu-id="55d2e-147">Usulkan</span><span class="sxs-lookup"><span data-stu-id="55d2e-147">Propose</span></span> | <span data-ttu-id="55d2e-148">Kuotasi</span><span class="sxs-lookup"><span data-stu-id="55d2e-148">Quote</span></span> | <span data-ttu-id="55d2e-149">Kembangkan proposal dengan kuotasi proyek dan dapatkan persetujuan dari tim peninjauan internal.</span><span class="sxs-lookup"><span data-stu-id="55d2e-149">Develop the proposal using project quotes and get approval from the internal review team.</span></span> |
| <span data-ttu-id="55d2e-150">Kontrak</span><span class="sxs-lookup"><span data-stu-id="55d2e-150">Contract</span></span> | <span data-ttu-id="55d2e-151">Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="55d2e-151">Project Contract</span></span> | <span data-ttu-id="55d2e-152">Menangkan kuotasi untuk membuat kontrak dan memulai eksekusi dan pelaksanaan proyek.</span><span class="sxs-lookup"><span data-stu-id="55d2e-152">Win the quote to create the contract and begin execution and delivery on the project.</span></span> |
| <span data-ttu-id="55d2e-153">Tutup</span><span class="sxs-lookup"><span data-stu-id="55d2e-153">Close</span></span> | <span data-ttu-id="55d2e-154">Kontrak Proyek</span><span class="sxs-lookup"><span data-stu-id="55d2e-154">Project Contract</span></span> | <span data-ttu-id="55d2e-155">Selesaikan pekerjaan dengan sukses dan tutup kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="55d2e-155">Finish the work successfully and close the project contract.</span></span> |

> [!NOTE]
> <span data-ttu-id="55d2e-156">Jika perjanjian berbasis proyek Anda dimulai dengan Prospek, proses bisnis prospek ke peluang lebih diutamakan.</span><span class="sxs-lookup"><span data-stu-id="55d2e-156">If your project-based deal started with a Lead, the Lead to Opportunity business process takes precedence.</span></span>
>
> <span data-ttu-id="55d2e-157">Jika perjanjian berbasis proyek Anda dimulai dengan peluang, proses penjualan peluang lebih diutamakan.</span><span class="sxs-lookup"><span data-stu-id="55d2e-157">If your project-based deal started with an Opportunity, the Opportunity sales process takes precedence.</span></span>

<span data-ttu-id="55d2e-158">Anda dapat mengedit alur proses bisnis produk atau membuat alur proses bisnis Anda sendiri untuk melacak proses penjualan Anda sesuai kebutuhan.</span><span class="sxs-lookup"><span data-stu-id="55d2e-158">You can edit the product business process flow or create your own business process flows to track your sales process as needed.</span></span> <span data-ttu-id="55d2e-159">Untuk informasi lebih lanjut tentang alur proses bisnis, lihat [Ikhtisar alur proses bisnis](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span><span class="sxs-lookup"><span data-stu-id="55d2e-159">For more information about the business process flow, see [Business process flows overview](/dynamics365/customerengagement/on-premises/customize/business-process-flows-overview).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Sekilas penyebaran Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Topik ini menyediakan informasi tentang jenis penyebaran, Project Operations untuk skenario berbasis sumber daya/non-stok.
author: rumant
ms.date: 11/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ca8c0894dff1a74b532f8262278fb20400f097c5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001250"
---
# <a name="project-operations-for-resourcenon-stocked-based-scenarios-deployment-overview"></a><span data-ttu-id="70945-103">Sekilas penyebaran Project Operations untuk skenario berbasis sumber daya/tanpa stok</span><span class="sxs-lookup"><span data-stu-id="70945-103">Project Operations for resource/non-stocked based scenarios deployment overview</span></span>

<span data-ttu-id="70945-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="70945-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="70945-105">Jenis penyebaran, Dynamics 365 Project Operations untuk skenario berbasis sumber daya/non-stok memiliki kemampuan berikut untuk perusahaan berbasis proyek:</span><span class="sxs-lookup"><span data-stu-id="70945-105">The deployment type, Dynamics 365 Project Operations for resource/non-stocked based scenarios has the following capabilities for project-based companies:</span></span>

- <span data-ttu-id="70945-106">Perencanaan proyek menggunakan Microsoft Project untuk web</span><span class="sxs-lookup"><span data-stu-id="70945-106">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="70945-107">Harga multi-dimensi dan biaya untuk sumber daya tenaga kerja</span><span class="sxs-lookup"><span data-stu-id="70945-107">Multi-dimensional pricing and costing for labor resources</span></span>
- <span data-ttu-id="70945-108">Kategori berdasarkan harga untuk kategori pengeluaran</span><span class="sxs-lookup"><span data-stu-id="70945-108">Category-based pricing for expense categories</span></span>
- <span data-ttu-id="70945-109">Manajemen penjualan berbasis proyek menggunakan kemampuan Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="70945-109">Project-based sales management using Dynamics 365 Sales capabilities</span></span>
- <span data-ttu-id="70945-110">Universal Resource Scheduling yang berintegrasi dengan aplikasi lain seperti Dynamics 365 Field Service dan Dynamics 365 Customer Service</span><span class="sxs-lookup"><span data-stu-id="70945-110">Universal resource scheduling that integrates with other applications such as Dynamics 365 Field Service and Dynamics 365 Customer Service</span></span>
- <span data-ttu-id="70945-111">Kemajuan proyek dan pelacakan waktu</span><span class="sxs-lookup"><span data-stu-id="70945-111">Project progress and Time Tracking</span></span>
- <span data-ttu-id="70945-112">Pengalaman manajemen pengeluaran dasar dan penuh untuk pengeluaran proyek dan non-proyek termasuk pengambilan tanda terima menggunakan kemampuan OCR</span><span class="sxs-lookup"><span data-stu-id="70945-112">Basic and full Expense management experiences for project and non-project expenses including receipt capture using OCR capabilities</span></span>
- <span data-ttu-id="70945-113">Faktur yang membentang dari proforma ke sisi pelanggan dan didukung oleh sistem nilai tukar efektif tanggal dan pajak penjualan kelas perusahaan.</span><span class="sxs-lookup"><span data-stu-id="70945-113">Invoicing that extends from proforma to customer-facing and is backed by an enterprise-class sales tax and date-effective exchange rate system.</span></span>
- <span data-ttu-id="70945-114">Biaya proyek yang bisa dikonfigurasi, profil pendapatan, dan aturan untuk akuntansi pekerjaan dalam proses (WIP) dan akrual</span><span class="sxs-lookup"><span data-stu-id="70945-114">Configurable project cost, revenue profiles, and rules for work in progress (WIP) accounting and accruals</span></span>
- <span data-ttu-id="70945-115">Pengakuan pendapatan proyek</span><span class="sxs-lookup"><span data-stu-id="70945-115">Project revenue recognition</span></span>
- <span data-ttu-id="70945-116">Ekstensibilitas melalui Power Platform</span><span class="sxs-lookup"><span data-stu-id="70945-116">Extensibility through the Power Platform</span></span>

<span data-ttu-id="70945-117">Jenis penyebaran ini menyediakan ekstensi untuk fungsionalitas yang disediakan oleh aplikasi Dynamics 365 Finance dan Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="70945-117">This deployment type provides an extension to the functionality provided by Dynamics 365 Finance and Dynamics 365 Supply Chain Management applications.</span></span>

<span data-ttu-id="70945-118">Penyebaran ini harus dipilih untuk memastikan ekspektasi Project Operations adalah menggunakan siklus hidup proyek lengkap yang mencakup persyaratan berikut:</span><span class="sxs-lookup"><span data-stu-id="70945-118">This deployment should be chosen the expectation of Project Operations is to use the full project lifecycle that includes the following requirements:</span></span>

- <span data-ttu-id="70945-119">Kemampuan untuk mengelola penjualan berbasis proyek dengan jenis penjualan lain menggunakan kemampuan dalam aplikasi Sales.</span><span class="sxs-lookup"><span data-stu-id="70945-119">Ability to manage project-based sales with other types of sales using the capabilities in the Sales application.</span></span>
- <span data-ttu-id="70945-120">Sistem manajemen proyek terintegrasi yang mengelola proyek internal dan dapat ditagih untuk jadwal dan keuangan dari penjualan proyek ke akuntansi.</span><span class="sxs-lookup"><span data-stu-id="70945-120">An integrated project management system that manages internal and billable projects for schedules and financials from project sales to accounting.</span></span>
- <span data-ttu-id="70945-121">Sistem manajemen pengeluaran yang mencakup penegakan kebijakan dan penggantian uang untuk melacak pengeluaran proyek dan non-proyek.</span><span class="sxs-lookup"><span data-stu-id="70945-121">An expense management system that includes policy enforcements and reimbursements for tracking project and non-project expenses.</span></span>
- <span data-ttu-id="70945-122">Memerlukan mesin, pajak penjualan dan nilai tukar kelas perusahaan yang kaya untuk menghasilkan faktur sisi pelanggan untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="70945-122">Require a rich, enterprise-class sales tax and exchange rate engine to generate customer-facing invoices for projects.</span></span>
- <span data-ttu-id="70945-123">Sistem akuntansi proyek dan pengakuan pendapatan yang sesuai dengan International Financial Reporting Standards(IFRS).</span><span class="sxs-lookup"><span data-stu-id="70945-123">An International Financial Reporting Standards(IFRS)-compliant project accounting and revenue recognition system.</span></span>
- <span data-ttu-id="70945-124">Aplikasi Finance dan Supply Chain Management dan integrasi transaksi berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="70945-124">Finance or Supply Chain Management applications and integration of project-based transactions.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
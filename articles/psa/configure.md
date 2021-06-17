---
title: Konfigurasi Project Service Automation
description: Langkah-langkah untuk mengkonfigurasi Project Service
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ef1724bb92e62ae21472e133fff0978c4faeeffa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002843"
---
# <a name="configure-project-service"></a><span data-ttu-id="4c22e-103">Konfigurasi Project Service</span><span class="sxs-lookup"><span data-stu-id="4c22e-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4c22e-104">Sebelum Anda dapat menggunakan kemampuan otomatisasi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] untuk mengelola akun, proyek, dan sumber daya Anda, Anda perlu menyelesaikan beberapa langkah konfigurasi untuk memastikan solusi [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sesuai dengan kebutuhan organisasi Anda.</span><span class="sxs-lookup"><span data-stu-id="4c22e-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="4c22e-105">Langkah ini mencakup:</span><span class="sxs-lookup"><span data-stu-id="4c22e-105">These steps include:</span></span>  
  
-   <span data-ttu-id="4c22e-106">[Mengatur unit waktu](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="4c22e-107">Mengkonfigurasi unit waktu dalam Katalog Produk yang akan Anda gunakan sebagai dasar untuk penjadwalan dan penagihan proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="4c22e-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="4c22e-108">[Mengatur mata uang dan nilai tukar](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="4c22e-109">Mengatur mata uang untuk digunakan untuk proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="4c22e-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="4c22e-110">[Buat Unit Organisasi](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="4c22e-111">Mengatur kelompok-kelompok yang perusahaan Anda gunakan untuk membagi bisnisnya, Apakah menurut geografi, fungsi bisnis, atau divisi Logis lainnya.</span><span class="sxs-lookup"><span data-stu-id="4c22e-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="4c22e-112">[Konfigurasi Frekuensi Faktur](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="4c22e-113">Mengatur waktu yang Anda ingin gunakan untuk penagihan klien Anda.</span><span class="sxs-lookup"><span data-stu-id="4c22e-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="4c22e-114">[Konfigurasi Kategori Transaksi](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="4c22e-115">Mengatur kategori transaksi yang dapat ditagih konsultan Anda untuk biaya yang bisa ditagih dan tidak ditagih.</span><span class="sxs-lookup"><span data-stu-id="4c22e-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="4c22e-116">[Konfigurasi Kategori Pengeluaran](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="4c22e-117">Mengatur kategori yang dapat ditagih konsultan Anda untuk biaya yang bisa ditagih dan tidak ditagih.</span><span class="sxs-lookup"><span data-stu-id="4c22e-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="4c22e-118">[Membuat item katalog produk](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="4c22e-119">Tambahkan produk yang Anda Jual, seperti lisensi perangkat lunak untuk Katalog Produk.</span><span class="sxs-lookup"><span data-stu-id="4c22e-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="4c22e-120">[Membuat daftar harga](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="4c22e-121">Mengkonfigurasi daftar harga yang berbeda, tergantung berapa banyak yang ingin Anda tagih pada klien Anda untuk setiap peran yang dibutuhkan proyek mereka.</span><span class="sxs-lookup"><span data-stu-id="4c22e-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="4c22e-122">[Konfigurasi Sumber Daya](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="4c22e-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="4c22e-123">Tambahkan keterampilan, kecakapan, peran sumber daya dan informasi sumber daya lain yang Anda perlukan untuk proyek Anda.</span><span class="sxs-lookup"><span data-stu-id="4c22e-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4c22e-124">Lihat Juga</span><span class="sxs-lookup"><span data-stu-id="4c22e-124">See Also</span></span>  
 <span data-ttu-id="4c22e-125">[Gambaran Umum Project Service Automation](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="4c22e-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="4c22e-126">[Konfigurasi Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="4c22e-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="4c22e-127">[Panduan Manajer Akun](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="4c22e-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="4c22e-128">[Panduan Manajer Proyek](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="4c22e-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="4c22e-129">[Panduan Manajer Sumber Daya](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="4c22e-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="4c22e-130">Panduan Waktu, biaya dan kolaborasi</span><span class="sxs-lookup"><span data-stu-id="4c22e-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
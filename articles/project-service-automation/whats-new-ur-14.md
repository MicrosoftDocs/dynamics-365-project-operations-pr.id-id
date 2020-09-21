---
title: Yang baru di Project Service Automation Rilis Pembaruan 14, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 14 V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752434"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="72c69-103">Project Service Automation V3, Pembaruan Rilis 14</span><span class="sxs-lookup"><span data-stu-id="72c69-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="72c69-104">Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="72c69-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="72c69-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="72c69-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="72c69-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="72c69-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="72c69-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="72c69-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="72c69-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="72c69-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="72c69-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 14.</span><span class="sxs-lookup"><span data-stu-id="72c69-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="72c69-110">Versi ini memiliki nomor pembuatan V3.10.4.21 dan tersedia pada jadwal berikut ini:</span><span class="sxs-lookup"><span data-stu-id="72c69-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="72c69-111">**Ketersediaan umum (pembaruan mandiri):** Januari 2020</span><span class="sxs-lookup"><span data-stu-id="72c69-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="72c69-112">**Pembaruan otomatis:** Februari 2020</span><span class="sxs-lookup"><span data-stu-id="72c69-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="72c69-113">Pembaruan rilis 14</span><span class="sxs-lookup"><span data-stu-id="72c69-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="72c69-114">Peningkatan</span><span class="sxs-lookup"><span data-stu-id="72c69-114">Enhancements</span></span>

- <span data-ttu-id="72c69-115">Sales</span><span class="sxs-lookup"><span data-stu-id="72c69-115">Sales</span></span>

     - <span data-ttu-id="72c69-116">Nilai bidang kustom dari **detail baris kuotasi** disalin ke **detail baris kontrak proyek** saat kuotasi diperbarui ke **ditutup sebagai menang**.</span><span class="sxs-lookup"><span data-stu-id="72c69-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="72c69-117">Proyek yang dikonfirmasi dapat **ditutup sebagai kalah**.</span><span class="sxs-lookup"><span data-stu-id="72c69-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="72c69-118">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="72c69-118">Resource Management</span></span>

     - <span data-ttu-id="72c69-119">Saat memperpanjang Pemesanan, pengguna akan diminta dengan kotak dialog konfirmasi untuk merangkum hasil Pemesanan dan menyediakan tautan untuk mempertahankan Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="72c69-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="72c69-120">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="72c69-120">Bug fixes</span></span>

- <span data-ttu-id="72c69-121">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="72c69-121">Time and Expense</span></span>

     - <span data-ttu-id="72c69-122">Tetap: meningkatkan pengalaman pengguna saat pengguna belum memilih entri yang akan dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="72c69-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="72c69-123">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="72c69-123">Resource Management</span></span>

     - <span data-ttu-id="72c69-124">Tetap: Pemesanan sumber daya beberapa kali meluapkan nama sumber daya dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="72c69-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="72c69-125">Sales</span><span class="sxs-lookup"><span data-stu-id="72c69-125">Sales</span></span>

     - <span data-ttu-id="72c69-126">Tetap: Total harga penjualan tidak dihitung hingga pengguna juga memasukkan harga biaya untuk perkiraan pengeluaran pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="72c69-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="72c69-127">Tetap: menutup kuotasi sebagai **menang** gagal jika kontrak proyek terkait tidak dalam status **draf**.</span><span class="sxs-lookup"><span data-stu-id="72c69-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>


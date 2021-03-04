---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 14, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 14 V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: f9347741d8dae2c9a810bb5b3a32d4d6c0a628ed
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147162"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="f6ba5-103">Project Service Automation Pembaruan Rilis 14, V3</span><span class="sxs-lookup"><span data-stu-id="f6ba5-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f6ba5-104">Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="f6ba5-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="f6ba5-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f6ba5-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f6ba5-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="f6ba5-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f6ba5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f6ba5-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 14.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="f6ba5-110">Versi ini memiliki nomor pembuatan V3.10.4.21 dan tersedia pada jadwal berikut ini:</span><span class="sxs-lookup"><span data-stu-id="f6ba5-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="f6ba5-111">**Ketersediaan umum (pembaruan mandiri):** Januari 2020</span><span class="sxs-lookup"><span data-stu-id="f6ba5-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="f6ba5-112">**Pembaruan otomatis:** Februari 2020</span><span class="sxs-lookup"><span data-stu-id="f6ba5-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="f6ba5-113">Pembaruan rilis 14</span><span class="sxs-lookup"><span data-stu-id="f6ba5-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="f6ba5-114">Peningkatan</span><span class="sxs-lookup"><span data-stu-id="f6ba5-114">Enhancements</span></span>

- <span data-ttu-id="f6ba5-115">Sales</span><span class="sxs-lookup"><span data-stu-id="f6ba5-115">Sales</span></span>

     - <span data-ttu-id="f6ba5-116">Nilai bidang kustom dari **detail baris kuotasi** disalin ke **detail baris kontrak proyek** saat kuotasi diperbarui ke **ditutup sebagai menang**.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="f6ba5-117">Proyek yang dikonfirmasi dapat **ditutup sebagai kalah**.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="f6ba5-118">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="f6ba5-118">Resource Management</span></span>

     - <span data-ttu-id="f6ba5-119">Saat memperpanjang Pemesanan, pengguna akan diminta dengan kotak dialog konfirmasi untuk merangkum hasil Pemesanan dan menyediakan tautan untuk mempertahankan Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="f6ba5-120">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="f6ba5-120">Bug fixes</span></span>

- <span data-ttu-id="f6ba5-121">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="f6ba5-121">Time and Expense</span></span>

     - <span data-ttu-id="f6ba5-122">Tetap: meningkatkan pengalaman pengguna saat pengguna belum memilih entri yang akan dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="f6ba5-123">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="f6ba5-123">Resource Management</span></span>

     - <span data-ttu-id="f6ba5-124">Tetap: Pemesanan sumber daya beberapa kali meluapkan nama sumber daya dapat dipesan.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="f6ba5-125">Sales</span><span class="sxs-lookup"><span data-stu-id="f6ba5-125">Sales</span></span>

     - <span data-ttu-id="f6ba5-126">Tetap: Total harga penjualan tidak dihitung hingga pengguna juga memasukkan harga biaya untuk perkiraan pengeluaran pada suatu proyek.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="f6ba5-127">Tetap: menutup kuotasi sebagai **menang** gagal jika kontrak proyek terkait tidak dalam status **draf**.</span><span class="sxs-lookup"><span data-stu-id="f6ba5-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>


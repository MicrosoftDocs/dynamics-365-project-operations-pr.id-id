---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 16, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 16, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078443"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="aee47-103">Project Service Automation Pembaruan Rilis 16, V3</span><span class="sxs-lookup"><span data-stu-id="aee47-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="aee47-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="aee47-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="aee47-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="aee47-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="aee47-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="aee47-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="aee47-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="aee47-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="aee47-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui solusi pilihan](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="aee47-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="aee47-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 16.</span><span class="sxs-lookup"><span data-stu-id="aee47-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="aee47-110">Versi ini memiliki nomor pembuatan V3.10.6.34 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2020.</span><span class="sxs-lookup"><span data-stu-id="aee47-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="aee47-111">Pembaruan rilis 16</span><span class="sxs-lookup"><span data-stu-id="aee47-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="aee47-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="aee47-112">Bug fixes</span></span>

-   <span data-ttu-id="aee47-113">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="aee47-113">Time and Expense</span></span>

    -   <span data-ttu-id="aee47-114">Diperbaiki pengguna yang mencoba mengirimkan entri waktu dan pengeluaran yang dihapus untuk persetujuan sekarang akan menerima pesan kesalahan yang relevan.</span><span class="sxs-lookup"><span data-stu-id="aee47-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="aee47-115">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="aee47-115">Project Management</span></span>

    -   <span data-ttu-id="aee47-116">Diperbaiki: unit sumber daya yang ditentukan untuk anggota tim di template dihormati dengan template yang diterapkan ke proyek baru.</span><span class="sxs-lookup"><span data-stu-id="aee47-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="aee47-117">Diperbaiki: peningkatan penanganan penugasan ulang kepemilikan rekaman.</span><span class="sxs-lookup"><span data-stu-id="aee47-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="aee47-118">Diperbaiki: proyek yang ada dalam proses yang sedang disalin tidak akan diizinkan untuk disalin hingga semua operasi penyalinan selesai.</span><span class="sxs-lookup"><span data-stu-id="aee47-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="aee47-119">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="aee47-119">Resource Management</span></span>

    -   <span data-ttu-id="aee47-120">Diperbaiki" memperpanjang Pemesanan sekarang menangani durasi singkat dengan benar dan tidak lagi membuat nol jam untuk pemesanan diperpanjang.</span><span class="sxs-lookup"><span data-stu-id="aee47-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="aee47-121">Diperbaiki: tampilan rekonsiliasi sekarang dirender saat zona waktu proyek adalah + 5:30 GMT dan zona waktu pengguna berbeda.</span><span class="sxs-lookup"><span data-stu-id="aee47-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="aee47-122">Sales</span><span class="sxs-lookup"><span data-stu-id="aee47-122">Sales</span></span>

    -   <span data-ttu-id="aee47-123">Diperbaiki: saat proyek yang dipetakan ke baris kontrak dihapus dan proyek baru dipetakan, rekaman aktual pada proyek baru tidak dievaluasi ulang berdasarkan aturan penagihan dan harga yang ditentukan pada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="aee47-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="aee47-124">Ini telah diperbaiki dalam rilis ini.</span><span class="sxs-lookup"><span data-stu-id="aee47-124">This has been fixed in this release.</span></span> <span data-ttu-id="aee47-125">Harga dan rekaman aktual pada proyek yang baru dipetakan akan dibalik dan dibuat ulang dengan benar berdasarkan aturan harga dan penagihan baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="aee47-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="aee47-126">Rekaman aktual proyek yang tidak dipetakan juga akan dievaluasi ulang dan dibuat ulang sebagai konsekuensinya.</span><span class="sxs-lookup"><span data-stu-id="aee47-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="aee47-127">Diperbaiki: validasi tambahan telah ditambahkan ke bidang **jumlah** baris perkiraan untuk memastikan bahwa nilai null tidak dipertahankan.</span><span class="sxs-lookup"><span data-stu-id="aee47-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="aee47-128">Diperbaiki: saat aktual telah diperbarui pada proyek, tombol refresh telah ditambahkan ke formulir utama proyek untuk memungkinkan pengguna mensinkronisasi ulang aktual.</span><span class="sxs-lookup"><span data-stu-id="aee47-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="aee47-129">Diperbaiki: saat pengguna beralih dari 2. X ke 3. X, proyek dengan nilai NULL untuk nama proyek akan diizinkan.</span><span class="sxs-lookup"><span data-stu-id="aee47-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>


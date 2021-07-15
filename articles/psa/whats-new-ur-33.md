---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 33, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 33, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334554"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="d3383-103">Yang baru atau diubah di Project Service Automation Rilis Pembaruan 33, V3</span><span class="sxs-lookup"><span data-stu-id="d3383-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d3383-104">Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d3383-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="d3383-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="d3383-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d3383-106">Aplikasi ini kompatibel dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d3383-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d3383-107">Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="d3383-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="d3383-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d3383-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d3383-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 33.</span><span class="sxs-lookup"><span data-stu-id="d3383-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="d3383-110">Versi ini memiliki nomor build V3.10.54.98 dan secara umum tersedia melalui pembaruan mandiri pada Bulan Juli 2021.</span><span class="sxs-lookup"><span data-stu-id="d3383-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="d3383-111">Pembaruan rilis 33</span><span class="sxs-lookup"><span data-stu-id="d3383-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d3383-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="d3383-112">Bug fixes</span></span>

<span data-ttu-id="d3383-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="d3383-113">**Time and Expense**</span></span>

<span data-ttu-id="d3383-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="d3383-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="d3383-115">Dua bidang yang terkunci, **msdyn_description** dan **msdyn_externaldescription** dapat diedit setelah pengiriman.</span><span class="sxs-lookup"><span data-stu-id="d3383-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="d3383-116">Pesan kesalahan terjadi jika pengeluaran dibuat yang tidak terkait dengan proyek.</span><span class="sxs-lookup"><span data-stu-id="d3383-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="d3383-117">Bila entri waktu dibuat, peran sumber daya akan default ke peran tidak aktif.</span><span class="sxs-lookup"><span data-stu-id="d3383-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="d3383-118">Baris jurnal yang terkait dengan pengeluaran yang ditarik dan dihapus tidak akan dihapus.</span><span class="sxs-lookup"><span data-stu-id="d3383-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="d3383-119">Pada **Formulir Buat Cepat entri Waktu**, perbarui tampilan **Daftar Tugas Proyek** untuk mengubah tanggal yang ditampilkan secara default ke tanggal mulai tugas.</span><span class="sxs-lookup"><span data-stu-id="d3383-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="d3383-120">Ketika Anda membuat entri waktu dari tab **Terkait** sumber daya yang dapat dipesan, entri waktu salah dibuat untuk pengguna yang masuk, bukan sumber daya yang dapat dipesan induk.</span><span class="sxs-lookup"><span data-stu-id="d3383-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="d3383-121">Bidang baru ditambahkan ke kotak dialog **MDD persetujuan massal**.</span><span class="sxs-lookup"><span data-stu-id="d3383-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="d3383-122">**Perencanaan proyek**</span><span class="sxs-lookup"><span data-stu-id="d3383-122">**Project planning**</span></span>

<span data-ttu-id="d3383-123">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="d3383-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="d3383-124">Kinerja pembuatan proyek yang lambat saat template jam kerja proyek diterapkan dengan kalender kompleks.</span><span class="sxs-lookup"><span data-stu-id="d3383-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="d3383-125">Bila tanggal mulai lebih besar dari tanggal berakhir, kesalahan ditampilkan di template salin proyek karena perbedaan pada komponen waktu tiap bidang.</span><span class="sxs-lookup"><span data-stu-id="d3383-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="d3383-126">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="d3383-126">**Resource management**</span></span>

<span data-ttu-id="d3383-127">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="d3383-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="d3383-128">Parameter yang salah digunakan dalam kueri pemanfaatan sumber daya dan XML mengakibatkan hasil filter yang salah pada kisi **Pemanfaatan Sumber Daya**.</span><span class="sxs-lookup"><span data-stu-id="d3383-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="d3383-129">Konfirmasi **Perluas Pemesanan** menampilkan tanggal berakhir yang salah untuk pemesanan.</span><span class="sxs-lookup"><span data-stu-id="d3383-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="d3383-130">**Penjualan**</span><span class="sxs-lookup"><span data-stu-id="d3383-130">**Sales**</span></span>

<span data-ttu-id="d3383-131">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="d3383-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="d3383-132">Pesan kesalahan terjadi jika harga kategori dibuat dengan nilai yang tidak ada.</span><span class="sxs-lookup"><span data-stu-id="d3383-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="d3383-133">Pesan kesalahan terjadi jika tahapan baris kontrak dibuat tanpa baris pesanan.</span><span class="sxs-lookup"><span data-stu-id="d3383-133">An error message occurs if a contract line milestone is created without an order line.</span></span>

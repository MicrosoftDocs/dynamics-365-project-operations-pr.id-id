---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 32, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 32, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129670"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="d3036-103">Yang baru atau diubah di Project Service Automation Rilis Pembaruan 32, V3</span><span class="sxs-lookup"><span data-stu-id="d3036-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d3036-104">Kami senang mengumumkan pembaruan terbaru untuk aplikasi Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="d3036-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="d3036-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="d3036-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d3036-106">Aplikasi ini kompatibel dengan Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d3036-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d3036-107">Untuk memperbarui rilis ini, kunjungi halaman solusi online Pusat Admin untuk Dynamics 365, dan instal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="d3036-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="d3036-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d3036-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d3036-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 32.</span><span class="sxs-lookup"><span data-stu-id="d3036-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="d3036-110">Versi ini memiliki nomor build V3.10.53.108 dan secara umum tersedia melalui pembaruan mandiri pada Bulan Juni 2021.</span><span class="sxs-lookup"><span data-stu-id="d3036-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="d3036-111">Pembaruan rilis 32</span><span class="sxs-lookup"><span data-stu-id="d3036-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d3036-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="d3036-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="d3036-113">Umum</span><span class="sxs-lookup"><span data-stu-id="d3036-113">General</span></span>

- <span data-ttu-id="d3036-114">Bila peningkatan utama gagal, hanya titik masuk aplikasi utama yang harus diblokir, untuk memastikan entitas bersama tetap dapat diakses.</span><span class="sxs-lookup"><span data-stu-id="d3036-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="d3036-115">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="d3036-115">Time and Expense</span></span>

<span data-ttu-id="d3036-116">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="d3036-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d3036-117">**TimeEntriesImportSourceResourceAssignment** tidak mempertahankan waktu mulai dan berakhir potongan kontur penetapan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d3036-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="d3036-118">Bila Anda memilih **Buka Entri** pada kisi **Entri Waktu**, Anda mungkin dicegah memilih formulir lain.</span><span class="sxs-lookup"><span data-stu-id="d3036-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="d3036-119">Saat Anda mengimpor penetapan ke entri waktu, kueri kode klien dapat menghasilkan URL panjang yang menggagalkan kueri.</span><span class="sxs-lookup"><span data-stu-id="d3036-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="d3036-120">Di kisi **Entri Waktu**, setelah nilai dihapus dari sel, fokus tidak tetap berada di kisi.</span><span class="sxs-lookup"><span data-stu-id="d3036-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="d3036-121">Tombol **Tolak** telah dihilangkan dari tampilan **Pemrosesan persetujuan** untuk persetujuan modern.</span><span class="sxs-lookup"><span data-stu-id="d3036-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="d3036-122">Stabilitas dan performa persetujuan massal entri waktu terpengaruh kebuntuan dan kegagalan untuk menangani dengan benar penyesuaian yang terkait dengan entitas **Entri Waktu**.</span><span class="sxs-lookup"><span data-stu-id="d3036-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="d3036-123">Perencanaan proyek</span><span class="sxs-lookup"><span data-stu-id="d3036-123">Project Planning</span></span>

- <span data-ttu-id="d3036-124">Pengecualian referensi nihil dibuat saat Anda memperbarui proyek yang memiliki nilai nihil di bidang **Unit Kontrak**.</span><span class="sxs-lookup"><span data-stu-id="d3036-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="d3036-125">**Segarkan Total Proyek** dengan keliru menghitung biaya tersisa dan penjualan yang tersisa di proyek.</span><span class="sxs-lookup"><span data-stu-id="d3036-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="d3036-126">Penghitungan harga berulang mempengaruhi performa yang terkait dengan pembaruan pada kontur penugasan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d3036-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="d3036-127">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="d3036-127">Resource Management</span></span>

<span data-ttu-id="d3036-128">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="d3036-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="d3036-129">Ketika kapasitas kalender sumber daya yang dapat dipesan lebih dari 1, Project Service Automation dengan keliru mengenali kapasitas sebagai 0 (nol).</span><span class="sxs-lookup"><span data-stu-id="d3036-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="d3036-130">Oleh karena itu, lingkaran tak terbatas terjadi di tampilan jadwal.</span><span class="sxs-lookup"><span data-stu-id="d3036-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="d3036-131">Penjualan</span><span class="sxs-lookup"><span data-stu-id="d3036-131">Sales</span></span>

<span data-ttu-id="d3036-132">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="d3036-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="d3036-133">Ketika baris jurnal dibuat yang memiliki jenis transaksi kustom, pengecualian referensi nihil berikut terjadi: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="d3036-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="d3036-134">Peran dan kategori yang dinonaktifkan sebelum kuotasi disalin seharusnya tidak ditambahkan ke peran dan kategori yang dikenakan biaya dari kuotasi yang baru disalin.</span><span class="sxs-lookup"><span data-stu-id="d3036-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="d3036-135">Tanggal dokumen dan tanggal akuntansi tidak selaras dengan tanggal mulai yang diberikan pada detail baris faktur yang dibuat secara langsung pada draf faktur.</span><span class="sxs-lookup"><span data-stu-id="d3036-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="d3036-136">Pengecualian referensi nihil dibuat dalam skenario yang terkait dengan penonaktifan peran dan kategori sebelum kuotasi disalin.</span><span class="sxs-lookup"><span data-stu-id="d3036-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="d3036-137">Tindakan **Harga Pembaruan** di halaman **Proyek** tidak memperbarui estimasi pengeluaran dan estimasi bahan.</span><span class="sxs-lookup"><span data-stu-id="d3036-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>

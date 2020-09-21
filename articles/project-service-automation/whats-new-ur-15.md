---
title: Yang baru di Project Service Automation Rilis Pembaruan 15, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 15, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752433"
---
# <a name="project-service-automation-v3-update-release-15"></a><span data-ttu-id="5a30b-103">Project Service Automation V3, Pembaruan Rilis 15</span><span class="sxs-lookup"><span data-stu-id="5a30b-103">Project Service Automation V3, Update Release 15</span></span>

<span data-ttu-id="5a30b-104">Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="5a30b-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="5a30b-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="5a30b-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5a30b-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="5a30b-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5a30b-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="5a30b-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="5a30b-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5a30b-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5a30b-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 15.</span><span class="sxs-lookup"><span data-stu-id="5a30b-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="5a30b-110">Versi ini memiliki nomor pembuatan V3.10.5.28 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2020.</span><span class="sxs-lookup"><span data-stu-id="5a30b-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="5a30b-111">Pembaruan rilis 15</span><span class="sxs-lookup"><span data-stu-id="5a30b-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="5a30b-112">Peningkatan</span><span class="sxs-lookup"><span data-stu-id="5a30b-112">Enhancements</span></span>

- <span data-ttu-id="5a30b-113">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="5a30b-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="5a30b-114">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="5a30b-114">Bug fixes</span></span>

- <span data-ttu-id="5a30b-115">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="5a30b-115">Time and Expense</span></span>

  - <span data-ttu-id="5a30b-116">Tetap: menambahkan penanganan kesalahan dalam beban di tampilan rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="5a30b-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="5a30b-117">Tetap: Pusat sumber daya proyek: Ubah nama **jumlah** untuk mengurangi ambiguitas.</span><span class="sxs-lookup"><span data-stu-id="5a30b-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="5a30b-118">Tetap: Sesuaikan tampilan **kolom Salin entri waktu** untuk mencakup jenis.</span><span class="sxs-lookup"><span data-stu-id="5a30b-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="5a30b-119">Tetap: mengedit durasi entri waktu dalam tampilan kisi menggunakan hasil angka desimal dalam kesalahan yang tidak diketahui untuk sejumlah nomor.</span><span class="sxs-lookup"><span data-stu-id="5a30b-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="5a30b-120">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="5a30b-120">Project Management</span></span>

  - <span data-ttu-id="5a30b-121">Tetap: menu drop-down untuk **gunakan dalam tampilan pelacakan** sekarang diperluas berdasarkan lebar pilihan.</span><span class="sxs-lookup"><span data-stu-id="5a30b-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="5a30b-122">Tetap: saat mengelola proyek di zona waktu + 13, penghitungan tugas dapat menampilkan hasil yang tidak akurat.</span><span class="sxs-lookup"><span data-stu-id="5a30b-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="5a30b-123">Tetap: **waktu berakhir anggota tim** telah dikoreksi saat menggunakan kalender 24 jam.</span><span class="sxs-lookup"><span data-stu-id="5a30b-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="5a30b-124">Tetap: Mengaktifkan kembali **BPF** di formulir utama **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="5a30b-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="5a30b-125">Tetap: penghitungan tugas tidak lagi mengabaikan satu hari.</span><span class="sxs-lookup"><span data-stu-id="5a30b-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="5a30b-126">Tetap: banner pemberitahuan baru telah ditambahkan ke formulir proyek saat zona waktu berbeda antara pengguna dan proyek.</span><span class="sxs-lookup"><span data-stu-id="5a30b-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="5a30b-127">Sales</span><span class="sxs-lookup"><span data-stu-id="5a30b-127">Sales</span></span>

  - <span data-ttu-id="5a30b-128">Tetap: pencarian kategori perkiraan biaya dapat digunakan untuk memfilter duplikat.</span><span class="sxs-lookup"><span data-stu-id="5a30b-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="5a30b-129">Tetap: kode di **PluginDomain.ExecuteInTryCatchBlock(..)** tidak lagi menyembunyikan asal pengecualian.</span><span class="sxs-lookup"><span data-stu-id="5a30b-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="5a30b-130">Tetap: tidak lagi mendapatkan pesan kesalahan dalam **pencarian proyek** dalam formulir **baris kuotasi** saat terdapat lebih dari 1000 proyek.</span><span class="sxs-lookup"><span data-stu-id="5a30b-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="5a30b-131">Tetap: kisi **perkiraan** untuk perkiraan tenaga kerja dan perkiraan biaya sekarang menampilkan simbol mata uang yang benar.</span><span class="sxs-lookup"><span data-stu-id="5a30b-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="5a30b-132">Tetap: setelah organisasi pembaruan PSA dari rilis pembaruan 14 ke rilis pembaruan 15, tab **jadwal** tidak lagi ditampilkan sebagai kosong pada formulir **proyek**.</span><span class="sxs-lookup"><span data-stu-id="5a30b-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>

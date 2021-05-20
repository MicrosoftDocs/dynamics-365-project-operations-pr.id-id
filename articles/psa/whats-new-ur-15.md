---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 15, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 15, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: fe1e2b2046faeee4e4c71484a976d70e8722e090
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949323"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="b2360-103">Project Service Automation Pembaruan Rilis 15, V3</span><span class="sxs-lookup"><span data-stu-id="b2360-103">Project Service Automation Update Release 15, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b2360-104">Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="b2360-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b2360-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="b2360-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b2360-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="b2360-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b2360-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="b2360-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b2360-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b2360-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b2360-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 15.</span><span class="sxs-lookup"><span data-stu-id="b2360-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="b2360-110">Versi ini memiliki nomor pembuatan V3.10.5.28 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2020.</span><span class="sxs-lookup"><span data-stu-id="b2360-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="b2360-111">Pembaruan rilis 15</span><span class="sxs-lookup"><span data-stu-id="b2360-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="b2360-112">Peningkatan</span><span class="sxs-lookup"><span data-stu-id="b2360-112">Enhancements</span></span>

- <span data-ttu-id="b2360-113">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="b2360-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b2360-114">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="b2360-114">Bug fixes</span></span>

- <span data-ttu-id="b2360-115">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="b2360-115">Time and Expense</span></span>

  - <span data-ttu-id="b2360-116">Tetap: menambahkan penanganan kesalahan dalam beban di tampilan rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="b2360-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="b2360-117">Tetap: Pusat sumber daya proyek: Ubah nama **jumlah** untuk mengurangi ambiguitas.</span><span class="sxs-lookup"><span data-stu-id="b2360-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="b2360-118">Tetap: Sesuaikan tampilan **kolom Salin entri waktu** untuk mencakup jenis.</span><span class="sxs-lookup"><span data-stu-id="b2360-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="b2360-119">Tetap: mengedit durasi entri waktu dalam tampilan kisi menggunakan hasil angka desimal dalam kesalahan yang tidak diketahui untuk sejumlah nomor.</span><span class="sxs-lookup"><span data-stu-id="b2360-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="b2360-120">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="b2360-120">Project Management</span></span>

  - <span data-ttu-id="b2360-121">Tetap: menu drop-down untuk **gunakan dalam tampilan pelacakan** sekarang diperluas berdasarkan lebar pilihan.</span><span class="sxs-lookup"><span data-stu-id="b2360-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="b2360-122">Tetap: saat mengelola proyek di zona waktu + 13, penghitungan tugas dapat menampilkan hasil yang tidak akurat.</span><span class="sxs-lookup"><span data-stu-id="b2360-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="b2360-123">Tetap: **waktu berakhir anggota tim** telah dikoreksi saat menggunakan kalender 24 jam.</span><span class="sxs-lookup"><span data-stu-id="b2360-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="b2360-124">Tetap: Mengaktifkan kembali **BPF** di formulir utama **msdyn_project**.</span><span class="sxs-lookup"><span data-stu-id="b2360-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="b2360-125">Tetap: penghitungan tugas tidak lagi mengabaikan satu hari.</span><span class="sxs-lookup"><span data-stu-id="b2360-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="b2360-126">Tetap: banner pemberitahuan baru telah ditambahkan ke formulir proyek saat zona waktu berbeda antara pengguna dan proyek.</span><span class="sxs-lookup"><span data-stu-id="b2360-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="b2360-127">Sales</span><span class="sxs-lookup"><span data-stu-id="b2360-127">Sales</span></span>

  - <span data-ttu-id="b2360-128">Tetap: pencarian kategori perkiraan biaya dapat digunakan untuk memfilter duplikat.</span><span class="sxs-lookup"><span data-stu-id="b2360-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="b2360-129">Tetap: kode di **PluginDomain.ExecuteInTryCatchBlock(..)** tidak lagi menyembunyikan asal pengecualian.</span><span class="sxs-lookup"><span data-stu-id="b2360-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="b2360-130">Tetap: tidak lagi mendapatkan pesan kesalahan dalam **pencarian proyek** dalam formulir **baris kuotasi** saat terdapat lebih dari 1000 proyek.</span><span class="sxs-lookup"><span data-stu-id="b2360-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="b2360-131">Tetap: kisi **perkiraan** untuk perkiraan tenaga kerja dan perkiraan biaya sekarang menampilkan simbol mata uang yang benar.</span><span class="sxs-lookup"><span data-stu-id="b2360-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="b2360-132">Tetap: setelah organisasi pembaruan PSA dari rilis pembaruan 14 ke rilis pembaruan 15, tab **jadwal** tidak lagi ditampilkan sebagai kosong pada formulir **proyek**.</span><span class="sxs-lookup"><span data-stu-id="b2360-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
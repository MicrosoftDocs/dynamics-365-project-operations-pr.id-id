---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 22, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 22, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006560"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="ed6ca-103">Project Service Automation Pembaruan Rilis 22, V3</span><span class="sxs-lookup"><span data-stu-id="ed6ca-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ed6ca-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ed6ca-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ed6ca-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ed6ca-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ed6ca-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ed6ca-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ed6ca-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 22.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="ed6ca-110">Versi ini memiliki nomor pembuatan V 3.10.33.48 dan umumnya tersedia melalui pembaruan mandiri pada Juni 2020.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="ed6ca-111">Pembaruan rilis 22</span><span class="sxs-lookup"><span data-stu-id="ed6ca-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ed6ca-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="ed6ca-112">Bug fixes</span></span>



<span data-ttu-id="ed6ca-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-113">**Time and Expense**</span></span>

<span data-ttu-id="ed6ca-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ed6ca-115">**Entri waktu** tidak secara otomatis ditambahkan dalam jadwal entri waktu setelah impor.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="ed6ca-116">pemilih tanggal kisi **Entri waktu** tidak mengenali pengaturan wilayah pengguna.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="ed6ca-117">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-117">**Resource Management**</span></span>

<span data-ttu-id="ed6ca-118">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="ed6ca-119">Dalam mode manual, perubahan kontur **tugas sumber daya** tidak dikenali saat menghasilkan **kebutuhan sumber daya**.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="ed6ca-120">**Permintaan sumber daya** tidak mendukung status permintaan kustom.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="ed6ca-121">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-121">**Project Management**</span></span>

<span data-ttu-id="ed6ca-122">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="ed6ca-123">Menggunakan klik dua kali pada EstimateGridControl tidak akan dengan benar mengurai nomor format Belanda.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="ed6ca-124">Jam yang ditetapkan tidak diperbarui dengan benar saat penetapan diubah menggunakan Add-in klien desktop Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="ed6ca-125">Pelacakan proyek dan perkiraan kisi menampilkan kode mata uang penjualan yang salah ketika mata uang kontrak berbeda dari mata uang pelanggan dan organisasi dikonfigurasi untuk menampilkan kode mata uang dan bukan simbol mata uang.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="ed6ca-126">Tanggal selesai anggota tim akan ditambahkan satu hari jika jadwal jam kerja adalah 24 jam per hari.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="ed6ca-127">Pada jadwal proyek, menambahkan kategori transaksi ke tugas tidak memicu Simpan otomatis.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="ed6ca-128">Kesalahan berikut ditampilkan saat menambahkan anggota tim ke template proyek: "Persyaratan sumber daya tidak dapat dikaitkan dengan template proyek".</span><span class="sxs-lookup"><span data-stu-id="ed6ca-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="ed6ca-129">Skrip aturan pita "msdyn.Approval.CanApproveOrReject"menampilkan kesalahan batas waktu.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="ed6ca-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="ed6ca-130">**Sales**</span></span>

<span data-ttu-id="ed6ca-131">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="ed6ca-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="ed6ca-132">Pesan kesalahan validasi tidak ditampilkan bila daftar harga biaya dipilih dalam pencarian daftar harga pada formulir/entitas 'daftar harga proyek kuotasi baru'.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="ed6ca-133">Penutupan kuotasi sebagai menang tidak menavigasi ke kontrak yang dibuat jika BPF yang melekat pada kuotasi berada dalam tahapan akhir.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="ed6ca-134">Membalikkan **penjualan yang belum ditagih** ditautkan ke biaya awal bila entri waktu dipanggil.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="ed6ca-135">Setelah memilih tombol **konfirmasikan**, status faktur tidak akan diubah ke **dikonfirmasi** kecuali faktur diperbarui.</span><span class="sxs-lookup"><span data-stu-id="ed6ca-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
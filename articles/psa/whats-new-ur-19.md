---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 19, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 19, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: e116bcbb8e9d184b7b894709c893aaf1dadefc2f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126846"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="1eede-103">Project Service Automation Pembaruan Rilis 19, V3</span><span class="sxs-lookup"><span data-stu-id="1eede-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="1eede-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="1eede-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="1eede-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="1eede-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="1eede-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="1eede-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="1eede-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="1eede-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="1eede-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="1eede-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="1eede-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 19.</span><span class="sxs-lookup"><span data-stu-id="1eede-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="1eede-110">Versi ini memiliki nomor pembuatan V3.10.30.41 dan umumnya tersedia melalui pembaruan mandiri pada Mei 2020.</span><span class="sxs-lookup"><span data-stu-id="1eede-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="1eede-111">Pembaruan rilis 19</span><span class="sxs-lookup"><span data-stu-id="1eede-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="1eede-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="1eede-112">Bug fixes</span></span>

<span data-ttu-id="1eede-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="1eede-113">**Time and Expense**</span></span>

<span data-ttu-id="1eede-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="1eede-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="1eede-115">Kesalahan yang berasal dari impor entri waktu tidak muncul dengan benar.</span><span class="sxs-lookup"><span data-stu-id="1eede-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="1eede-116">Kisi waktu entri tidak mendukung perilaku bidang **hanya tanggal**.</span><span class="sxs-lookup"><span data-stu-id="1eede-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="1eede-117">Sumber daya proyek tidak dapat membuat pengeluaran dengan proyek.</span><span class="sxs-lookup"><span data-stu-id="1eede-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="1eede-118">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="1eede-118">**Project Management**</span></span>

<span data-ttu-id="1eede-119">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="1eede-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="1eede-120">Tugas cucu menyebabkan perkiraan upaya yang salah selama penghitungan penyelesaian (EAC).</span><span class="sxs-lookup"><span data-stu-id="1eede-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="1eede-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="1eede-121">**Sales**</span></span>

<span data-ttu-id="1eede-122">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="1eede-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="1eede-123">Tindakan **menghitung ulang** tidak bekerja dengan rincian baris kontrak pengeluaran atau rincian baris kuotasi.</span><span class="sxs-lookup"><span data-stu-id="1eede-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="1eede-124">**Harga pembaruan** hilang untuk perkiraan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="1eede-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="1eede-125">Pelanggan tidak dapat memilih alasan status kustom kontrak dari halaman **kontrak proyek**.</span><span class="sxs-lookup"><span data-stu-id="1eede-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="1eede-126">Pelanggan mengalami kinerja yang rusak saat membuat daftar harga kustom dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="1eede-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="1eede-127">Pelanggan mengalami inkonsistensi dengan default **unit** pada **detail baris kuotasi** dan halaman **rincian baris kontrak**.</span><span class="sxs-lookup"><span data-stu-id="1eede-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="1eede-128">Menambahkan item kategori transaksi yang tidak dikenakan biaya ke baris kontrak yang dikenakan biaya tidak akan menghormati jenis penagihan **Tidak dikenai biaya** dari kategori transaksi.</span><span class="sxs-lookup"><span data-stu-id="1eede-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="1eede-129">Pelanggan tidak dapat menggunakan peran dan kategori yang baru ditambahkan pada kontrak yang dibuat sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="1eede-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="1eede-130">Pelanggan mengalami kinerja terdegradasi pengambilan tidak perlu di PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="1eede-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="1eede-131">Peran yang diatur sebagai tidak dikenakan biaya dalam Daftar **kategori sumber daya** harus ditambahkan ke **peran dikenai biaya** sebagai **Tidak dikenai biaya** pada baris kontrak untuk proyek.</span><span class="sxs-lookup"><span data-stu-id="1eede-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="1eede-132">Pelanggan mungkin mengalami kinerja yang rusak saat membuat proyek karena **GetBookableResourceIdFromUser** mengambil semua kolom sumber daya yang dapat dipesan dan bukan hanya id utama.</span><span class="sxs-lookup"><span data-stu-id="1eede-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="1eede-133">Entitas **TransactionType** kehilangan plug-in pembaruan pra-validasi untuk mencegah pengguna memasukkan **unit** dan **UnitGroups** yang tidak berlaku untuk jenis transaksi.</span><span class="sxs-lookup"><span data-stu-id="1eede-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="1eede-134">Langkah **Hapus** tidak berfungsi untuk impor entri waktu.</span><span class="sxs-lookup"><span data-stu-id="1eede-134">The **Remove** step does not work for time entry import.</span></span>

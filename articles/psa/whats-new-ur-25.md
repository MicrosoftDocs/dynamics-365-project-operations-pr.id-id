---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 25, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 25, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183547"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="802b5-103">Yang baru atau diubah di Project Service Automation Rilis Pembaruan 25, V3</span><span class="sxs-lookup"><span data-stu-id="802b5-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

<span data-ttu-id="802b5-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="802b5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="802b5-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="802b5-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="802b5-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="802b5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="802b5-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="802b5-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="802b5-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="802b5-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="802b5-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, rilis pembaruan 25 Versi ini memiliki nomor pembuatan V 3.10.43.76 dan umumnya tersedia melalui pembaruan mandiri pada oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="802b5-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="802b5-110">Pembaruan rilis 25</span><span class="sxs-lookup"><span data-stu-id="802b5-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="802b5-111">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="802b5-111">Bug fixes</span></span>

<span data-ttu-id="802b5-112">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="802b5-112">**Time and Expense**</span></span>

<span data-ttu-id="802b5-113">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="802b5-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="802b5-114">Diagram entri waktu yang menampilkan data tambahan berdasarkan interval terlalu besar yang diambil.</span><span class="sxs-lookup"><span data-stu-id="802b5-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="802b5-115">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="802b5-115">**Resource Management**</span></span>

<span data-ttu-id="802b5-116">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="802b5-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="802b5-117">Menambahkan kode Package Deployer untuk melewati impor patch Universal Resource Scheduling jika patch versi lebih tinggi sudah ada.</span><span class="sxs-lookup"><span data-stu-id="802b5-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="802b5-118">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="802b5-118">**Project Management**</span></span>

<span data-ttu-id="802b5-119">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="802b5-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="802b5-120">Mengoreksi pembulatan dan selisih kurs yang mengakibatkan kesalahan biaya yang direncanakan dalam kisi pelacakan proyek.</span><span class="sxs-lookup"><span data-stu-id="802b5-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="802b5-121">Mendukung kemampuan untuk menampilkan dua atau lebih kisi reaksi pada formulir **proyek**.</span><span class="sxs-lookup"><span data-stu-id="802b5-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="802b5-122">Menyediakan validasi untuk menangani kemampuan untuk menetapkan tugas yang melewati tanggal berakhir Kalender, yang menghasilkan penetapan sumber daya yang gagal.</span><span class="sxs-lookup"><span data-stu-id="802b5-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="802b5-123">Memperbaiki penanganan kesalahan untuk mengatasi eksepsi referensi null yang dihasilkan dari yang berikut ini:</span><span class="sxs-lookup"><span data-stu-id="802b5-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="802b5-124">Plug-in **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="802b5-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="802b5-125">**PreValidateProjectTaskCreate** saat tugas proyek dibuat tanpa proyek terkait</span><span class="sxs-lookup"><span data-stu-id="802b5-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="802b5-126">Plug-in **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="802b5-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="802b5-127">Plug-in **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="802b5-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="802b5-128">Plug-in **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="802b5-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="802b5-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="802b5-129">**Sales**</span></span>

<span data-ttu-id="802b5-130">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="802b5-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="802b5-131">Memperbaiki penanganan kesalahan untuk mengatasi pengecualian referensi null yang dihasilkan dari **salinan proyek: perkiraan manajemen HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="802b5-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="802b5-132">**Tidak siap untuk faktur** pada **Akumulasi tagihan waktu dan material** tidak menghapus status penagihan.</span><span class="sxs-lookup"><span data-stu-id="802b5-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="802b5-133">Mengoreksi tombol **harga** yang salah label pada tab **Harga Peran** dan **item Katalog**.</span><span class="sxs-lookup"><span data-stu-id="802b5-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>

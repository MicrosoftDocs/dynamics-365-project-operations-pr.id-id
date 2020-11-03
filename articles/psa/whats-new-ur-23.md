---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 23, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 23, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: eaae9cc62c449695cb2e999be48c57075aadbb21
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078431"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="596d7-103">Project Service Automation Pembaruan Rilis 23, V3</span><span class="sxs-lookup"><span data-stu-id="596d7-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="596d7-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="596d7-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="596d7-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="596d7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="596d7-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="596d7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="596d7-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="596d7-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="596d7-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="596d7-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="596d7-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 23.</span><span class="sxs-lookup"><span data-stu-id="596d7-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="596d7-110">Versi ini memiliki nomor pembuatan V 3.10.34.30 dan umumnya tersedia melalui pembaruan mandiri pada Agustus 2020.</span><span class="sxs-lookup"><span data-stu-id="596d7-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="596d7-111">Pembaruan rilis 23</span><span class="sxs-lookup"><span data-stu-id="596d7-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="596d7-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="596d7-112">Bug fixes</span></span>

<span data-ttu-id="596d7-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="596d7-113">**Time and Expense**</span></span>

<span data-ttu-id="596d7-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="596d7-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="596d7-115">Tangani kasus tepi dalam **Penghapusan anggota tim proyek** untuk memberikan pengecualian bermakna.</span><span class="sxs-lookup"><span data-stu-id="596d7-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="596d7-116">Hasil impor tugas di layar Hapus kosong.</span><span class="sxs-lookup"><span data-stu-id="596d7-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="596d7-117">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="596d7-117">**Resource Management**</span></span>

<span data-ttu-id="596d7-118">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="596d7-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="596d7-119">**Kartu sumber daya pemanfaatan kisi sumber daya** menampilkan data yang salah saat skala waktu lebih dari lima hari.</span><span class="sxs-lookup"><span data-stu-id="596d7-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="596d7-120">Bila pelanggan membuat sumber daya yang dapat dipesan, plug-in terkadang gagal menambahkan sumber daya secara otomatis ke grup Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="596d7-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="596d7-121">Tampilan **rekonsiliasi** menampilkan kontur manual secara tidak benar dalam tampilan **Pekan** atau **bulan**.</span><span class="sxs-lookup"><span data-stu-id="596d7-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="596d7-122">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="596d7-122">**Project Management**</span></span>

<span data-ttu-id="596d7-123">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="596d7-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="596d7-124">Jumlah berlebihan entitas **retrievemultiple untuk usersettings** menyebabkan kinerja terdegradasi untuk persetujuan proyek dan operasi lainnya.</span><span class="sxs-lookup"><span data-stu-id="596d7-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="596d7-125">Pencarian sumber daya kisi **perencanaan tugas** terbatas hanya menampilkan hingga lima anggota tim dari tim proyek.</span><span class="sxs-lookup"><span data-stu-id="596d7-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="596d7-126">Pencarian sumber daya kisi **perencanaan tugas** tidak memfilter sumber daya yang tidak aktif.</span><span class="sxs-lookup"><span data-stu-id="596d7-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="596d7-127">Mode manual tidak berfungsi sebagaimana yang diharapkan dalam struktur rincian kerja Perencanaan proyek.</span><span class="sxs-lookup"><span data-stu-id="596d7-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="596d7-128">Kisi **perencanaan tugas** menunjukkan **kategori transaksi tidak aktif**.</span><span class="sxs-lookup"><span data-stu-id="596d7-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="596d7-129">Putaran kisi **Penetapan sumber daya** salah ketika tugas memiliki beberapa penetapan.</span><span class="sxs-lookup"><span data-stu-id="596d7-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="596d7-130">Nilai pembulatan berbeda antara biaya yang direncanakan dan biaya aktual untuk satu tugas.</span><span class="sxs-lookup"><span data-stu-id="596d7-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="596d7-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="596d7-131">**Sales**</span></span>

<span data-ttu-id="596d7-132">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="596d7-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="596d7-133">**Ambil Semua Kategori Transaksi** Klik dua kali membuat beberapa baris.</span><span class="sxs-lookup"><span data-stu-id="596d7-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>

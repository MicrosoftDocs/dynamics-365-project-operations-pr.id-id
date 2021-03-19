---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 12, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f1b2fdc37fa2c2e31537b89b7027d2833e905578
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281077"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="fde4e-103">Project Service Automation Pembaruan Rilis 12, V3</span><span class="sxs-lookup"><span data-stu-id="fde4e-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fde4e-104">Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="fde4e-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="fde4e-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="fde4e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fde4e-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="fde4e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fde4e-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="fde4e-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="fde4e-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fde4e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fde4e-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 12.</span><span class="sxs-lookup"><span data-stu-id="fde4e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="fde4e-110">Versi ini memiliki nomor pembuatan V 3.10.2.34 dan umumnya tersedia melalui pembaruan mandiri pada Oktober 2019.</span><span class="sxs-lookup"><span data-stu-id="fde4e-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="fde4e-111">Pembaruan rilis 12</span><span class="sxs-lookup"><span data-stu-id="fde4e-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fde4e-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="fde4e-112">Bug fixes</span></span>

- <span data-ttu-id="fde4e-113">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="fde4e-113">Time and Expense</span></span>

    - <span data-ttu-id="fde4e-114">Tetap: pesan kesalahan entri waktu telah diperbarui dengan konteks yang lebih relevan.</span><span class="sxs-lookup"><span data-stu-id="fde4e-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="fde4e-115">Tetap: waktu entri kisi dan jadwal dengan benar menampilkan bilah penggulir vertikal bila diperlukan.</span><span class="sxs-lookup"><span data-stu-id="fde4e-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="fde4e-116">Tetap: Entri waktu yang biaya yang diajukan dapat disetujui.</span><span class="sxs-lookup"><span data-stu-id="fde4e-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="fde4e-117">Tetap: pesan dialog konfirmasi pembatalan persetujuan telah diperbaiki untuk mencerminkan status persetujuan bila diubah **dari disetujui** untuk **dikirim**.</span><span class="sxs-lookup"><span data-stu-id="fde4e-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="fde4e-118">Tetap: Bidang **harga**, **unit**, dan **kuantitas** sekarang terkunci pada rekaman pengeluaran setelah disetujui.</span><span class="sxs-lookup"><span data-stu-id="fde4e-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="fde4e-119">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="fde4e-119">Project Management</span></span>

    - <span data-ttu-id="fde4e-120">Tetap: tindakan **baru** pada formulir utama **anggota tim** telah dihapus.</span><span class="sxs-lookup"><span data-stu-id="fde4e-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="fde4e-121">Tetap: tugas sumber daya telah diperbarui ke akun untuk kesalahan pembulatan yang tidak akurat, yang menyebabkan pergeseran pada tanggal berakhir tugas.</span><span class="sxs-lookup"><span data-stu-id="fde4e-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="fde4e-122">Tetap: di kisi tugas, kesalahan sisi server yang relevan akan muncul ke pengguna.</span><span class="sxs-lookup"><span data-stu-id="fde4e-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="fde4e-123">Tetap: nama anggota tim sekarang dirender dalam pemilih tugas, bukan nama posisi.</span><span class="sxs-lookup"><span data-stu-id="fde4e-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="fde4e-124">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="fde4e-124">Resource Management</span></span>

    - <span data-ttu-id="fde4e-125">Tetap: rincian kebutuhan sumber daya untuk proyek yang dibuat dari template sekarang menggunakan kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="fde4e-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="fde4e-126">Tetap: keterampilan dan kompetensi sekarang default dari data Master peran ke persyaratan sumber daya yang dibuat untuk peran tersebut.</span><span class="sxs-lookup"><span data-stu-id="fde4e-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="fde4e-127">Sales</span><span class="sxs-lookup"><span data-stu-id="fde4e-127">Sales</span></span>

    - <span data-ttu-id="fde4e-128">Tetap: id objek duplikat yang ditemukan pada formulir **utama kontrak**.</span><span class="sxs-lookup"><span data-stu-id="fde4e-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="fde4e-129">Tetap: logika telah diperbarui untuk membuat tab **analisis kuotasi** terlihat sehingga menampilkan konfigurasi metadata tab.</span><span class="sxs-lookup"><span data-stu-id="fde4e-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="fde4e-130">Tetap: tanggal akuntansi pada rekaman aktual sekarang berasal dari tanggal waktu/tanggal entri pengeluaran dan bukan tanggal persetujuan.</span><span class="sxs-lookup"><span data-stu-id="fde4e-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
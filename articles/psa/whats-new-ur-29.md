---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 29, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 29, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 320f4f74cb5997e42e2dc9e1d8c8a5ab95ae6647
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010475"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="b8b59-103">Yang baru atau diubah di Project Service Automation Rilis Pembaruan 29, V3</span><span class="sxs-lookup"><span data-stu-id="b8b59-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b8b59-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="b8b59-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="b8b59-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="b8b59-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b8b59-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="b8b59-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b8b59-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="b8b59-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="b8b59-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b8b59-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b8b59-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 29.</span><span class="sxs-lookup"><span data-stu-id="b8b59-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="b8b59-110">Versi ini memiliki nomor pembuatan V3.10.47.7 dan umumnya tersedia melalui pembaruan mandiri pada Februari 2021.</span><span class="sxs-lookup"><span data-stu-id="b8b59-110">This version has a build number of V3.10.47.7 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="b8b59-111">Pembaruan rilis 29</span><span class="sxs-lookup"><span data-stu-id="b8b59-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b8b59-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="b8b59-112">Bug fixes</span></span>

<span data-ttu-id="b8b59-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="b8b59-113">**Time and Expense**</span></span>

<span data-ttu-id="b8b59-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="b8b59-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="b8b59-115">Pengguna tidak dapat melihat jam kerja yang dicatat pada hari non-kerja dalam kisi entri waktu.</span><span class="sxs-lookup"><span data-stu-id="b8b59-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="b8b59-116">Entri pengeluaran yang disetujui dapat diedit pada kisi.</span><span class="sxs-lookup"><span data-stu-id="b8b59-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="b8b59-117">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="b8b59-117">**Project Management**</span></span>

<span data-ttu-id="b8b59-118">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="b8b59-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="b8b59-119">Logika validasi tidak ditemukan untuk memastikan jam kerja penetapan sumber daya tidak dapat negatif.</span><span class="sxs-lookup"><span data-stu-id="b8b59-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="b8b59-120">Tindakan kustom, **AssignResourcesForTask** akan memperbarui semua bidang dan bukan hanya bidang yang diubah.</span><span class="sxs-lookup"><span data-stu-id="b8b59-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="b8b59-121">Saat menyalin proyek di lingkungan dengan plug-in atau alur kerja yang terdaftar di aktivitas **CreateProject**, atribut **msdyn_bulkgenerationstatus** tidak diperbarui jika **CopyWBSToAddress** gagal.</span><span class="sxs-lookup"><span data-stu-id="b8b59-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="b8b59-122">Saat Anda memperluas kalender proyek, hari kerja tidak disusun dalam urutan menaik yang menyebabkan beberapa pembaruan tugas proyek gagal.</span><span class="sxs-lookup"><span data-stu-id="b8b59-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="b8b59-123">Mengubah Manajer Proyek pada proyek yang ada akan memicu logika default unit organisasional.</span><span class="sxs-lookup"><span data-stu-id="b8b59-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="b8b59-124">**Penjualan**</span><span class="sxs-lookup"><span data-stu-id="b8b59-124">**Sales**</span></span>

<span data-ttu-id="b8b59-125">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="b8b59-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="b8b59-126">Tab **Performa Kontrak** di halaman **Kontrak** gagal secara hening selama inisialisasi saat tidak ada baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="b8b59-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 31, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 31, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945539"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="fc4ca-103">Yang baru atau diubah di Project Service Automation Rilis Pembaruan 31, V3</span><span class="sxs-lookup"><span data-stu-id="fc4ca-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fc4ca-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fc4ca-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fc4ca-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fc4ca-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fc4ca-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fc4ca-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fc4ca-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 31.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="fc4ca-110">Versi ini memiliki nomor pembuatan V3.10.52.77 dan umumnya tersedia melalui pembaruan mandiri pada Mei 2021.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="fc4ca-111">Pembaruan rilis 31</span><span class="sxs-lookup"><span data-stu-id="fc4ca-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fc4ca-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="fc4ca-112">Bug fixes</span></span>

<span data-ttu-id="fc4ca-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="fc4ca-113">**Time and Expense**</span></span>

<span data-ttu-id="fc4ca-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="fc4ca-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="fc4ca-115">Tombol perintah kontrol entri waktu di halaman **Sumber Daya yang Dapat Dipesan** membingungkan.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="fc4ca-116">Pengecualian referensi nihil dibuat di **Project.SetTrackingFields** saat menyetujui entri waktu.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="fc4ca-117">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="fc4ca-117">**Resource Management**</span></span>

<span data-ttu-id="fc4ca-118">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="fc4ca-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="fc4ca-119">**Membuat Anggota Tim** tidak menampilkan pengaturan metadata konfigurasi pemesanan dengan benar untuk **Status komitmen Pemesanan Default**.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="fc4ca-120">Ketika beralih dari PSA 1.X ke 3.X, proses peningkatan gagal di **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="fc4ca-121">**Penjualan**</span><span class="sxs-lookup"><span data-stu-id="fc4ca-121">**Sales**</span></span>

<span data-ttu-id="fc4ca-122">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="fc4ca-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="fc4ca-123">Pendapatan aktual mengkonversi jumlah ke mata uang proyek di kisi pelacakan.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="fc4ca-124">Default mata uang tidak jelas saat membuat baris jurnal, baris kuotasi, dan baris kontrak dalam skenario dengan mata uang dasar organisasi berbeda dari mata uang proyek.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="fc4ca-125">**Kueri validasi koreksi yang tertunda** tidak difilter berdasarkan proyek.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="fc4ca-126">Penjualan tersisa dihitung dengan salah di proyek.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="fc4ca-127">Kuotasi berdasarkan kontak gagal bila dibuat tanpa daftar harga.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="fc4ca-128">Spinner pemrosesan tidak ditampilkan saat Anda memilih **Konfirmasikan Faktur**.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="fc4ca-129">Spinner pemrosesan tidak ditampilkan saat Anda memilih **Buat Faktur**.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="fc4ca-130">Menutup kuotasi sebagai kalah tidak akan membatalkan pemesanan.</span><span class="sxs-lookup"><span data-stu-id="fc4ca-130">Closing a quote as lost doesn't cancel the bookings.</span></span>








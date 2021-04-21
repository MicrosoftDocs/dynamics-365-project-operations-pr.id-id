---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 30, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 30, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852863"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="e4fee-103">Yang baru atau diubah di Project Service Automation Rilis Pembaruan 30, V3</span><span class="sxs-lookup"><span data-stu-id="e4fee-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e4fee-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e4fee-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e4fee-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="e4fee-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e4fee-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="e4fee-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e4fee-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="e4fee-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e4fee-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e4fee-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e4fee-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 30.</span><span class="sxs-lookup"><span data-stu-id="e4fee-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="e4fee-110">Versi ini memiliki nomor pembuatan V3.10.51.61 dan umumnya tersedia melalui pembaruan mandiri pada April 2021.</span><span class="sxs-lookup"><span data-stu-id="e4fee-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="e4fee-111">Pembaruan rilis 30</span><span class="sxs-lookup"><span data-stu-id="e4fee-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e4fee-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="e4fee-112">Bug fixes</span></span>

<span data-ttu-id="e4fee-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="e4fee-113">**Time and Expense**</span></span>

<span data-ttu-id="e4fee-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="e4fee-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4fee-115">Kesalahan terjadi saat Anda membuat dan menyimpan entri waktu pada halaman **Buat Cepat** jika bidang **Peran** dihilangkan.</span><span class="sxs-lookup"><span data-stu-id="e4fee-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="e4fee-116">Filter Entri Waktu menerapkan operator filter yang salah.</span><span class="sxs-lookup"><span data-stu-id="e4fee-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="e4fee-117">Lembar waktu yang disalin tidak akan secara otomatis ditampilkan bila Anda memilih **Salin Pekan** pada kontrol entri waktu.</span><span class="sxs-lookup"><span data-stu-id="e4fee-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="e4fee-118">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="e4fee-118">**Resource Management**</span></span>

<span data-ttu-id="e4fee-119">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="e4fee-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4fee-120">Saat Anda memperpanjang masa pemesanan, status pemesanan yang ditetapkan ke pemesanan definitif salah.</span><span class="sxs-lookup"><span data-stu-id="e4fee-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="e4fee-121">Memperluas pemesanan sesuai status pemesanan yang didefinisikan sebagai **Berkomitmen** dalam metadata konfigurasi pemesanan.</span><span class="sxs-lookup"><span data-stu-id="e4fee-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="e4fee-122">Bila status pemesanan yang valid tidak ditentukan, pesan kesalahan tidak dilokalkan dengan benar.</span><span class="sxs-lookup"><span data-stu-id="e4fee-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="e4fee-123">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="e4fee-123">**Project Management**</span></span>

<span data-ttu-id="e4fee-124">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="e4fee-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4fee-125">Proyek tidak dapat dibuat dalam satu mata uang dan mencakup tugas terkait dalam mata uang lain.</span><span class="sxs-lookup"><span data-stu-id="e4fee-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="e4fee-126">**Penjualan**</span><span class="sxs-lookup"><span data-stu-id="e4fee-126">**Sales**</span></span>

<span data-ttu-id="e4fee-127">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="e4fee-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="e4fee-128">Bila daftar harga disalin, harga tidak diperbarui.</span><span class="sxs-lookup"><span data-stu-id="e4fee-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="e4fee-129">Menutup kuotasi sebagai menang gagal bila detail biaya memiliki nilai untuk asal.</span><span class="sxs-lookup"><span data-stu-id="e4fee-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="e4fee-130">Pada entitas **Tugas Proyek**, **Perkiraan Biaya** telah diubah namanya menjadi **Biaya Terencana (Dasar)**.</span><span class="sxs-lookup"><span data-stu-id="e4fee-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="e4fee-131">Pengecualian referensi nihil dibuat saat faktur dibuat atau dihapus.</span><span class="sxs-lookup"><span data-stu-id="e4fee-131">A null reference exception is generated when invoices are created or deleted.</span></span>

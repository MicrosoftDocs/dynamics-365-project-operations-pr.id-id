---
title: Yang baru di Project Service Automation Rilis Pembaruan 13, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 13, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752435"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="0c1a4-103">Project Service Automation V3, Pembaruan Rilis 13</span><span class="sxs-lookup"><span data-stu-id="0c1a4-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="0c1a4-104">Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="0c1a4-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="0c1a4-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="0c1a4-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="0c1a4-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="0c1a4-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="0c1a4-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="0c1a4-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 13.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="0c1a4-110">Versi ini memiliki nomor pembuatan V3.10.3.18 Versi ini memiliki nomor pembuatan V 4 dan tersedia pada jadwal berikut ini:</span><span class="sxs-lookup"><span data-stu-id="0c1a4-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="0c1a4-111">**Ketersediaan umum (pembaruan mandiri):** November 2019</span><span class="sxs-lookup"><span data-stu-id="0c1a4-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="0c1a4-112">**Pembaruan otomatis:** Desember 2019</span><span class="sxs-lookup"><span data-stu-id="0c1a4-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="0c1a4-113">Pembaruan rilis 13</span><span class="sxs-lookup"><span data-stu-id="0c1a4-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="0c1a4-114">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="0c1a4-114">Bug fixes</span></span>

- <span data-ttu-id="0c1a4-115">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="0c1a4-115">Time and Expense</span></span>

     - <span data-ttu-id="0c1a4-116">Tetap: fungsi pencarian pada halaman **persetujuan pengeluaran** tidak berfungsi saat mencari berdasarkan tujuan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="0c1a4-117">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="0c1a4-117">Resource Management</span></span>

     - <span data-ttu-id="0c1a4-118">Fixed: nomor dalam rekonsiliasi telah diperbarui menjadi rata kanan.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="0c1a4-119">Tetap: sumber daya yang diberi nama tidak dapat ditetapkan ke tugas melalui tab **jadwal**.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="0c1a4-120">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="0c1a4-120">Project Management</span></span>

     - <span data-ttu-id="0c1a4-121">Tetap: pengecualian referensi null saat menetapkan anggota tim saat **transactiontype** tidak memiliki informasi konfigurasi untuk **unit** dan **defaultgroup**.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="0c1a4-122">Sales</span><span class="sxs-lookup"><span data-stu-id="0c1a4-122">Sales</span></span>

     - <span data-ttu-id="0c1a4-123">Tetap: rekaman jenis transaksi duplikat menghasilkan kesalahan saat rekaman harga peran dibuat.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="0c1a4-124">Tetap: tombol tambahan untuk **peluang baru**, **kuotasi**, **baris pesanan**, dan **Tambahkan produk** dapat dilihat di perintah untuk peluang, kuotasi, pesanan produk, dan subkisi baris berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="0c1a4-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>



---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 13, V3
description: Topik ini menyediakan informasi tentang apa yang baru dalam Project Service Automation Rilis Pembaruan 13, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 435b70255dd0053a496362c9ced9e742cfcca843
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078444"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="7b432-103">Project Service Automation Pembaruan Rilis 13, V3</span><span class="sxs-lookup"><span data-stu-id="7b432-103">Project Service Automation Update Release 13, V3</span></span>
<span data-ttu-id="7b432-104">Kami dengan gembira mengumumkan pembaruan terbaru untuk aplikasi Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="7b432-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="7b432-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="7b432-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7b432-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="7b432-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7b432-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, dan buka halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="7b432-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="7b432-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7b432-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7b432-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 13.</span><span class="sxs-lookup"><span data-stu-id="7b432-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="7b432-110">Versi ini memiliki nomor pembuatan V3.10.3.18 Versi ini memiliki nomor pembuatan V 4 dan tersedia pada jadwal berikut ini:</span><span class="sxs-lookup"><span data-stu-id="7b432-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="7b432-111">**Ketersediaan umum (pembaruan mandiri):** November 2019</span><span class="sxs-lookup"><span data-stu-id="7b432-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="7b432-112">**Pembaruan otomatis:** Desember 2019</span><span class="sxs-lookup"><span data-stu-id="7b432-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="7b432-113">Pembaruan rilis 13</span><span class="sxs-lookup"><span data-stu-id="7b432-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="7b432-114">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="7b432-114">Bug fixes</span></span>

- <span data-ttu-id="7b432-115">Waktu dan Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="7b432-115">Time and Expense</span></span>

     - <span data-ttu-id="7b432-116">Tetap: fungsi pencarian pada halaman **persetujuan pengeluaran** tidak berfungsi saat mencari berdasarkan tujuan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="7b432-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="7b432-117">Manajemen sumber daya</span><span class="sxs-lookup"><span data-stu-id="7b432-117">Resource Management</span></span>

     - <span data-ttu-id="7b432-118">Fixed: nomor dalam rekonsiliasi telah diperbarui menjadi rata kanan.</span><span class="sxs-lookup"><span data-stu-id="7b432-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="7b432-119">Tetap: sumber daya yang diberi nama tidak dapat ditetapkan ke tugas melalui tab **jadwal**.</span><span class="sxs-lookup"><span data-stu-id="7b432-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="7b432-120">Manajemen proyek</span><span class="sxs-lookup"><span data-stu-id="7b432-120">Project Management</span></span>

     - <span data-ttu-id="7b432-121">Tetap: pengecualian referensi null saat menetapkan anggota tim saat **transactiontype** tidak memiliki informasi konfigurasi untuk **unit** dan **defaultgroup**.</span><span class="sxs-lookup"><span data-stu-id="7b432-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="7b432-122">Sales</span><span class="sxs-lookup"><span data-stu-id="7b432-122">Sales</span></span>

     - <span data-ttu-id="7b432-123">Tetap: rekaman jenis transaksi duplikat menghasilkan kesalahan saat rekaman harga peran dibuat.</span><span class="sxs-lookup"><span data-stu-id="7b432-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="7b432-124">Tetap: tombol tambahan untuk **peluang baru** , **kuotasi** , **baris pesanan** , dan **Tambahkan produk** dapat dilihat di perintah untuk peluang, kuotasi, pesanan produk, dan subkisi baris berbasis proyek.</span><span class="sxs-lookup"><span data-stu-id="7b432-124">Fixed: Extra buttons for **New Opportunity** , **Quote** , **Order Line** , and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>



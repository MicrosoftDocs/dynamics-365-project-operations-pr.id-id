---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 17, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 17, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949233"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="e2ca2-103">Project Service Automation Pembaruan Rilis 17, V3</span><span class="sxs-lookup"><span data-stu-id="e2ca2-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e2ca2-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e2ca2-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="e2ca2-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e2ca2-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="e2ca2-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e2ca2-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e2ca2-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk PSA V3, pembaruan rilis 17.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="e2ca2-110">Versi ini memiliki nomor pembuatan V3.10.6.34 dan umumnya tersedia melalui pembaruan mandiri pada Maret 2020.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="e2ca2-111">Pembaruan rilis 17</span><span class="sxs-lookup"><span data-stu-id="e2ca2-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e2ca2-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="e2ca2-112">Bug fixes</span></span>

<span data-ttu-id="e2ca2-113">**Umum**</span><span class="sxs-lookup"><span data-stu-id="e2ca2-113">**General**</span></span>

- <span data-ttu-id="e2ca2-114">Diperbaiki: Memperbarui Project Service Automation untuk menegakkan lisensi Team Member (Pusat sumber daya proyek akan mencakup metadata paket Team Member 3.x)</span><span class="sxs-lookup"><span data-stu-id="e2ca2-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="e2ca2-115">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="e2ca2-115">**Time and Expense**</span></span>

- <span data-ttu-id="e2ca2-116">Diperbaiki tidak dapat mengubah perkiraan pengeluaran dari harga non-nol menjadi nol (0).</span><span class="sxs-lookup"><span data-stu-id="e2ca2-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="e2ca2-117">Perubahan diabaikan.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-117">The change is ignored.</span></span>

<span data-ttu-id="e2ca2-118">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="e2ca2-118">**Project Management**</span></span>

- <span data-ttu-id="e2ca2-119">Diperbaiki: Pemeriksaan nilai null telah ditambahkan pada nama posisi anggota tim.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="e2ca2-120">Diperbaiki bidang **msdyn_userresourceid** pada entitas **msdyn_resourceassignment** telah ditolak.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="e2ca2-121">Diperbaiki Peningkatan dari 2. x ke 3. x sekarang menangani kontur usaha kosong pada penugasan tugas.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="e2ca2-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="e2ca2-122">**Sales**</span></span>

- <span data-ttu-id="e2ca2-123">Diperbaiki: **faktur. PreValidateInvoiceUpdate** sekarang menangani skenario menetapkan kembali pemilik rekaman dengan benar.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="e2ca2-124">Diperbaiki: saat kelas transaksi adalah **waktu**, **unitgroup** tidak dapat diedit untuk semua entitas termasuk **quotelinedetails**, **JournalLine**, **InvoiceLineDetail**, dan **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="e2ca2-125">Namun, **unit** hanya tidak bisa diedit untuk **journalline** dan **invoicelinedetails**.</span><span class="sxs-lookup"><span data-stu-id="e2ca2-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
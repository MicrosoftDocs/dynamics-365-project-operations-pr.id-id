---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 28, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 28, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150627"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="fbb30-103">Yang baru atau diubah di Project Service Automation Rilis Pembaruan 28, V3</span><span class="sxs-lookup"><span data-stu-id="fbb30-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="fbb30-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="fbb30-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="fbb30-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="fbb30-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="fbb30-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="fbb30-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="fbb30-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="fbb30-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="fbb30-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="fbb30-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="fbb30-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, rilis pembaruan 28 Versi ini memiliki nomor pembuatan V3.10.46.32 dan umumnya tersedia melalui pembaruan mandiri pada Januari 2021.</span><span class="sxs-lookup"><span data-stu-id="fbb30-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="fbb30-110">Pembaruan rilis 28</span><span class="sxs-lookup"><span data-stu-id="fbb30-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="fbb30-111">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="fbb30-111">Bug fixes</span></span>

<span data-ttu-id="fbb30-112">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="fbb30-112">**Time and Expense**</span></span>

<span data-ttu-id="fbb30-113">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="fbb30-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbb30-114">Pengguna dapat menggunakan **Pengeditan Massal** untuk memperbarui entri waktu yang telah disetujui dan dikirimkan.</span><span class="sxs-lookup"><span data-stu-id="fbb30-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="fbb30-115">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="fbb30-115">**Project Management**</span></span>

<span data-ttu-id="fbb30-116">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="fbb30-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbb30-117">Dalam kasus di mana tugas GUID diinterpretasikan sebagai angka, tugas tidak bisa dibuka untuk diedit menggunakan **Edit Tugas** di pita pada halaman **struktur rincian kerja**.</span><span class="sxs-lookup"><span data-stu-id="fbb30-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="fbb30-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="fbb30-118">**Sales**</span></span>

<span data-ttu-id="fbb30-119">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="fbb30-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="fbb30-120">Pengecualian referensi null dihasilkan ketika plug-in **GetEstimatesForProject** dipanggil.</span><span class="sxs-lookup"><span data-stu-id="fbb30-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="fbb30-121">**Tandai siap untuk faktur** pada kisi tonggak pencapaian hanya sebagian memperbarui atribut, kecuali untuk atribut **InvoiceStatus**, yang diperbarui.</span><span class="sxs-lookup"><span data-stu-id="fbb30-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>


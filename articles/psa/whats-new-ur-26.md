---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 26, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 26, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 135f017533705e165230ac994d217ad7c58bab10
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280402"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="f6d38-103">Project Service Automation Pembaruan Rilis 26, V3</span><span class="sxs-lookup"><span data-stu-id="f6d38-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f6d38-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="f6d38-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="f6d38-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="f6d38-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f6d38-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="f6d38-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f6d38-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="f6d38-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="f6d38-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f6d38-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f6d38-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 26, V3.</span><span class="sxs-lookup"><span data-stu-id="f6d38-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="f6d38-110">Versi ini memiliki nomor pembuatan V3.10.44.59 dan umumnya tersedia melalui pembaruan mandiri pada Desember 2020.</span><span class="sxs-lookup"><span data-stu-id="f6d38-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="f6d38-111">Pembaruan rilis 26</span><span class="sxs-lookup"><span data-stu-id="f6d38-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f6d38-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="f6d38-112">Bug fixes</span></span>

<span data-ttu-id="f6d38-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="f6d38-113">**Time and Expense**</span></span>

<span data-ttu-id="f6d38-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="f6d38-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f6d38-115">Pengguna dapat mengubah tugas di entri waktu yang telah disetujui/dikirim.</span><span class="sxs-lookup"><span data-stu-id="f6d38-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="f6d38-116">Terjadi kesalahan "Referensi Objek Tidak Diatur" saat menyimpan entri waktu.</span><span class="sxs-lookup"><span data-stu-id="f6d38-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="f6d38-117">Impor entri waktu dari tugas sumber daya menyebabkan entri waktu dengan nilai DateTime salah.</span><span class="sxs-lookup"><span data-stu-id="f6d38-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="f6d38-118">Apabila aplikasi Project Service Automation dan Field Service diinstal, tombol **Baru** akan ditampilkan dua kali di bilah perintah untuk entri waktu di aplikasi Field Service.</span><span class="sxs-lookup"><span data-stu-id="f6d38-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="f6d38-119">Pembaruan sel **Bolehkan Unit** dan **Grup unit** sekarang berfungsi pada kisi **Estimasi Pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="f6d38-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="f6d38-120">Formulir **Perbarui Edit Entri Waktu** mencakup **Garis waktu**.</span><span class="sxs-lookup"><span data-stu-id="f6d38-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="f6d38-121">Persetujuan waktu untuk entri waktu nonproyek memblokir sistem saat mencari peran pemberi izin proyek.</span><span class="sxs-lookup"><span data-stu-id="f6d38-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="f6d38-122">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="f6d38-122">**Resource Management**</span></span>

<span data-ttu-id="f6d38-123">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="f6d38-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="f6d38-124">Penambahan validasi di plug-in **PostProjectCreate** untuk memeriksa persyaratan utama sebelum membuatnya.</span><span class="sxs-lookup"><span data-stu-id="f6d38-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="f6d38-125">**Anggota Tim Proyek** dengan cepat membuat formulir menghilangkan pengecualian referensi null jika bidang dihapus dari formulir.</span><span class="sxs-lookup"><span data-stu-id="f6d38-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="f6d38-126">Membuat persyaratan untuk 12 jam lebih dari 1 tahun akan gagal.</span><span class="sxs-lookup"><span data-stu-id="f6d38-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="f6d38-127">Peningkatan pesan kesalahan pengecualian referensi null selama pembuatan persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="f6d38-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="f6d38-128">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="f6d38-128">**Project Management**</span></span>

<span data-ttu-id="f6d38-129">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="f6d38-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="f6d38-130">Peningkatan validasi ke alamat pengecualian referensi null yang dibuat di plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="f6d38-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="f6d38-131">Proyek yang dipublikasikan melalui add-in desktop Microsoft Project akan menghapus tugas yang belum ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="f6d38-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="f6d38-132">Penambahan validasi baru apabila referensi proyek tugas tidak valid karena pengecualian referensi null di plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="f6d38-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="f6d38-133">Kisi Anggota Tim tidak menampilkan tugas yang berbeda pada record anggota tim.</span><span class="sxs-lookup"><span data-stu-id="f6d38-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="f6d38-134">Penambahan validasi baru dan pesan kesalahan karena pengecualian referensi null di plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="f6d38-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="f6d38-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="f6d38-135">**Sales**</span></span>

<span data-ttu-id="f6d38-136">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="f6d38-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="f6d38-137">Saat memilih baris berbasis proyek dalam kuotasi atau kontrak, tombol **Saran** hanya akan terlihat saat memilih baris berbasis produk yang terkait dengan produk yang ada.</span><span class="sxs-lookup"><span data-stu-id="f6d38-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="f6d38-138">Pisahkan hak istimewa **Buat_Produk** dari hak istimewa **Buat_Kontrak Proyek**.</span><span class="sxs-lookup"><span data-stu-id="f6d38-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="f6d38-139">Menghapus baris faktur dapat menyebabkan kegagalan referensi pada **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="f6d38-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
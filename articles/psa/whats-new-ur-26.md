---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 26, V3
ms.openlocfilehash: 849e7288ee91d3e9360c0b03f6b8b37ff29338e7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643267"
---
<a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="da182-102">Project Service Automation Pembaruan Rilis 26, V3</span><span class="sxs-lookup"><span data-stu-id="da182-102">Project Service Automation Update Release 26, V3</span></span>
================================================

<span data-ttu-id="da182-103">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="da182-103">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="da182-104">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="da182-104">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="da182-105">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="da182-105">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="da182-106">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="da182-106">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="da182-107">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="da182-107">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="da182-108">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 26, V3.</span><span class="sxs-lookup"><span data-stu-id="da182-108">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="da182-109">Versi ini memiliki nomor pembuatan V3.10.44.59 dan umumnya tersedia melalui pembaruan mandiri pada Desember 2020.</span><span class="sxs-lookup"><span data-stu-id="da182-109">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

<a name="update-release-26"></a><span data-ttu-id="da182-110">Pembaruan rilis 26</span><span class="sxs-lookup"><span data-stu-id="da182-110">Update Release 26</span></span>
-----------------

### <a name="bug-fixes"></a><span data-ttu-id="da182-111">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="da182-111">Bug fixes</span></span>

<span data-ttu-id="da182-112">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="da182-112">**Time and Expense**</span></span>

<span data-ttu-id="da182-113">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="da182-113">The following issues have been fixed:</span></span>

-   <span data-ttu-id="da182-114">Pengguna dapat mengubah tugas di entri waktu yang telah disetujui/dikirim.</span><span class="sxs-lookup"><span data-stu-id="da182-114">Users are able to change the task on a time entry that has been approved/submitted.</span></span>

-   <span data-ttu-id="da182-115">Terjadi kesalahan "Referensi Objek Tidak Diatur" saat menyimpan entri waktu.</span><span class="sxs-lookup"><span data-stu-id="da182-115">"Object Reference Not Set" error when saving time entry.</span></span>

-   <span data-ttu-id="da182-116">Impor entri waktu dari tugas sumber daya menyebabkan entri waktu dengan nilai DateTime salah.</span><span class="sxs-lookup"><span data-stu-id="da182-116">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>

-   <span data-ttu-id="da182-117">Apabila aplikasi Project Service Automation dan Field Service diinstal, tombol **Baru** akan ditampilkan dua kali di bilah perintah untuk entri waktu di aplikasi Field Service.</span><span class="sxs-lookup"><span data-stu-id="da182-117">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>

-   <span data-ttu-id="da182-118">Pembaruan sel **Bolehkan Unit** dan **Grup unit** sekarang berfungsi pada kisi **Estimasi Pengeluaran**.</span><span class="sxs-lookup"><span data-stu-id="da182-118">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>

-   <span data-ttu-id="da182-119">Formulir **Perbarui Edit Entri Waktu** mencakup **Garis waktu**.</span><span class="sxs-lookup"><span data-stu-id="da182-119">**Update Time Entry Edit** form includes **Timeline**.</span></span>

-   <span data-ttu-id="da182-120">Persetujuan waktu untuk entri waktu nonproyek memblokir sistem saat mencari peran pemberi izin proyek.</span><span class="sxs-lookup"><span data-stu-id="da182-120">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="da182-121">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="da182-121">**Resource Management**</span></span>

<span data-ttu-id="da182-122">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="da182-122">The following issues have been fixed:</span></span>

-   <span data-ttu-id="da182-123">Penambahan validasi di plug-in **PostProjectCreate** untuk memeriksa persyaratan utama sebelum membuatnya.</span><span class="sxs-lookup"><span data-stu-id="da182-123">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>

-   <span data-ttu-id="da182-124">**Anggota Tim Proyek** dengan cepat membuat formulir menghilangkan pengecualian referensi null jika bidang dihapus dari formulir.</span><span class="sxs-lookup"><span data-stu-id="da182-124">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>

-   <span data-ttu-id="da182-125">Membuat persyaratan untuk 12 jam lebih dari 1 tahun akan gagal.</span><span class="sxs-lookup"><span data-stu-id="da182-125">Generate requirements for 12 hours over 1 year will fail.</span></span>

-   <span data-ttu-id="da182-126">Peningkatan pesan kesalahan pengecualian referensi null selama pembuatan persyaratan sumber daya.</span><span class="sxs-lookup"><span data-stu-id="da182-126">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="da182-127">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="da182-127">**Project Management**</span></span>

<span data-ttu-id="da182-128">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="da182-128">The following issues have been fixed:</span></span>

-   <span data-ttu-id="da182-129">Peningkatan validasi ke alamat pengecualian referensi null yang dibuat di plug-in **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="da182-129">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>

-   <span data-ttu-id="da182-130">Proyek yang dipublikasikan melalui add-in desktop Microsoft Project akan menghapus tugas yang belum ditetapkan.</span><span class="sxs-lookup"><span data-stu-id="da182-130">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>

-   <span data-ttu-id="da182-131">Penambahan validasi baru apabila referensi proyek tugas tidak valid karena pengecualian referensi null di plug-in **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="da182-131">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>

-   <span data-ttu-id="da182-132">Kisi Anggota Tim tidak menampilkan tugas yang berbeda pada record anggota tim.</span><span class="sxs-lookup"><span data-stu-id="da182-132">Team Member grid does not show distinct assignments on the team member record.</span></span>

-   <span data-ttu-id="da182-133">Penambahan validasi baru dan pesan kesalahan karena pengecualian referensi null di plug-in **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="da182-133">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="da182-134">**Sales**</span><span class="sxs-lookup"><span data-stu-id="da182-134">**Sales**</span></span>

<span data-ttu-id="da182-135">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="da182-135">The following issues have been fixed:</span></span>

-   <span data-ttu-id="da182-136">Saat memilih baris berbasis proyek dalam kuotasi atau kontrak, tombol **Saran** hanya akan terlihat saat memilih baris berbasis produk yang terkait dengan produk yang ada.</span><span class="sxs-lookup"><span data-stu-id="da182-136">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>

-   <span data-ttu-id="da182-137">Pisahkan hak istimewa **Buat_Produk** dari hak istimewa **Buat_Kontrak Proyek**.</span><span class="sxs-lookup"><span data-stu-id="da182-137">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>

-   <span data-ttu-id="da182-138">Menghapus baris faktur dapat menyebabkan kegagalan referensi pada **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="da182-138">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>

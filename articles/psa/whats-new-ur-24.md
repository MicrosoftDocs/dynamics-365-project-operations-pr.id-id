---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 24, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 24, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15fe1c3482de66331dd543ee73391638919b2595
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146712"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="efda8-103">Project Service Automation Pembaruan Rilis 24, V3</span><span class="sxs-lookup"><span data-stu-id="efda8-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="efda8-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="efda8-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="efda8-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="efda8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="efda8-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="efda8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="efda8-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="efda8-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="efda8-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="efda8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="efda8-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 24.</span><span class="sxs-lookup"><span data-stu-id="efda8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="efda8-110">Versi ini memiliki nomor pembuatan V 3.10.42.43 dan umumnya tersedia melalui pembaruan mandiri pada Oktober 2020.</span><span class="sxs-lookup"><span data-stu-id="efda8-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="efda8-111">Pembaruan rilis 24</span><span class="sxs-lookup"><span data-stu-id="efda8-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="efda8-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="efda8-112">Bug fixes</span></span>

<span data-ttu-id="efda8-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="efda8-113">**Sales**</span></span>

<span data-ttu-id="efda8-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="efda8-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="efda8-115">Masalah saat menentukan daftar harga produk default.</span><span class="sxs-lookup"><span data-stu-id="efda8-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="efda8-116">Kinerja kuotasi menang lambat karena daftar harga tersemat dan salinan rekaman harga peran.</span><span class="sxs-lookup"><span data-stu-id="efda8-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="efda8-117">**kontrak proyek/pusat penjualan** > **Item baris produk/kuantitas baris pesanan** secara otomatis dibulatkan ke bilangan cacah terdekat.</span><span class="sxs-lookup"><span data-stu-id="efda8-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="efda8-118">Tingkatkan hak istimewa sistem saat membaca daftar harga.</span><span class="sxs-lookup"><span data-stu-id="efda8-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="efda8-119">Salin bidang alamat pelanggan **address1_freighttermscode** dan **address1_shippingmethodcode** ke kuotasi/pesanan.</span><span class="sxs-lookup"><span data-stu-id="efda8-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="efda8-120">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="efda8-120">**Time and Expense**</span></span>

<span data-ttu-id="efda8-121">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="efda8-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="efda8-122">**Kisi entri waktu** tidak mendukung perilaku waktu **tanggal saja**.</span><span class="sxs-lookup"><span data-stu-id="efda8-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="efda8-123">**Entri waktu** tidak disegarkan secara otomatis.</span><span class="sxs-lookup"><span data-stu-id="efda8-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="efda8-124">Refresh manual diperlukan.</span><span class="sxs-lookup"><span data-stu-id="efda8-124">A manual refresh is required.</span></span>
- <span data-ttu-id="efda8-125">Tidak dapat mengimpor entri waktu dari tugas bila ada waktu istirahat (0 jam) dalam tugas sumber daya.</span><span class="sxs-lookup"><span data-stu-id="efda8-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="efda8-126">Saat membuat entri waktu, atur awal ke sama dengan **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="efda8-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="efda8-127">Aktifkan ulang Edit massal untuk entri waktu.</span><span class="sxs-lookup"><span data-stu-id="efda8-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="efda8-128">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="efda8-128">**Resource Management**</span></span>

<span data-ttu-id="efda8-129">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="efda8-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="efda8-130">Mencoba memperbarui status pemesanan harian tanpa persyaratan akan menghasilkan pengecualian null-ref.</span><span class="sxs-lookup"><span data-stu-id="efda8-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="efda8-131">Kesalahan saat memuat **tampilan rekonsiliasi**.</span><span class="sxs-lookup"><span data-stu-id="efda8-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="efda8-132">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="efda8-132">**Project Management**</span></span>

<span data-ttu-id="efda8-133">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="efda8-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="efda8-134">Dalam **jadwal proyek**, saat mengubah dari **manual** menjadi **Otomatis**, Simpan Otomatis tidak selesai.</span><span class="sxs-lookup"><span data-stu-id="efda8-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="efda8-135">Biaya pengeluaran tidak boleh dihitung ke arah varians pada **kisi pelacakan proyek**.</span><span class="sxs-lookup"><span data-stu-id="efda8-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="efda8-136">Perilaku yang tidak konsisten untuk kolom **tag estimasi** selama memuat versus mengubah jenis **fase waktu**.</span><span class="sxs-lookup"><span data-stu-id="efda8-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="efda8-137">Biaya aktual pada proyek mungkin tidak mencerminkan total dari **aktual**.</span><span class="sxs-lookup"><span data-stu-id="efda8-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="efda8-138">**Estimasi tanggal selesai** pada tab **ringkasan** tidak sesuai dengan **jadwal WBS**.</span><span class="sxs-lookup"><span data-stu-id="efda8-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="efda8-139">**Pembaruan jam aktual** pada outdentasi tidak berfungsi dengan benar.</span><span class="sxs-lookup"><span data-stu-id="efda8-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="efda8-140">Manajer proyek di luar **BU** akar tidak dapat membuat proyek.</span><span class="sxs-lookup"><span data-stu-id="efda8-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="efda8-141">Perubahan pada tugas atau kategori pada **Estimasi pengeluaran** tidak ada.</span><span class="sxs-lookup"><span data-stu-id="efda8-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="efda8-142">**Salinan kontrak** menyalin jadwal faktur dan status Jalankan.</span><span class="sxs-lookup"><span data-stu-id="efda8-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="efda8-143">Tombol **refresh aktual** salah menghitung tugas ringkasan.</span><span class="sxs-lookup"><span data-stu-id="efda8-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="efda8-144">Add-In Microsoft Project: Memperbaiki kesalahan referensi null jika salah satu anggota tim memiliki unit sumber daya kosong.</span><span class="sxs-lookup"><span data-stu-id="efda8-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>


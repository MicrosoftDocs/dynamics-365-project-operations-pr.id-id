---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 21, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 21, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002331"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="71008-103">Project Service Automation Pembaruan Rilis 21, V3</span><span class="sxs-lookup"><span data-stu-id="71008-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="71008-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="71008-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="71008-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="71008-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="71008-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="71008-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="71008-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="71008-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="71008-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="71008-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="71008-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 21.</span><span class="sxs-lookup"><span data-stu-id="71008-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="71008-110">Versi ini memiliki nomor pembuatan V 3.10.32.50 dan umumnya tersedia melalui pembaruan mandiri pada Juni 2020.</span><span class="sxs-lookup"><span data-stu-id="71008-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="71008-111">Pembaruan rilis 21</span><span class="sxs-lookup"><span data-stu-id="71008-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="71008-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="71008-112">Bug fixes</span></span>

<span data-ttu-id="71008-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="71008-113">**Time and Expense**</span></span>

<span data-ttu-id="71008-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="71008-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="71008-115">Ketika menghosting **kontrol kisi entri waktu** di dasbor, kisi tidak menggunakan lebar penuh kontainer kisi dasbor.</span><span class="sxs-lookup"><span data-stu-id="71008-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="71008-116">Untuk zona waktu tertentu, kontrol kisi **entri waktu** tidak menampilkan rekaman.</span><span class="sxs-lookup"><span data-stu-id="71008-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="71008-117">Entri waktu setelah 9:00 PM muncul pada hari yang salah.</span><span class="sxs-lookup"><span data-stu-id="71008-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="71008-118">Pengguna tidak dapat mengajukan pengeluaran jika kategori pengeluaran, **tanda terima pengeluaran yang diperlukan** tidak memiliki nilai.</span><span class="sxs-lookup"><span data-stu-id="71008-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="71008-119">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="71008-119">**Resource Management**</span></span>

<span data-ttu-id="71008-120">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="71008-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="71008-121">Pemesanan tidak aktif ditampilkan dalam tampilan **rekonsiliasi**.</span><span class="sxs-lookup"><span data-stu-id="71008-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="71008-122">Pemenuhan sumber daya umum kehilangan validasi untuk memastikan bahwa status pemesanan yang valid itu ada.</span><span class="sxs-lookup"><span data-stu-id="71008-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="71008-123">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="71008-123">**Project Management**</span></span>

<span data-ttu-id="71008-124">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="71008-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="71008-125">Kisi formulir **proyek** (**penetapan sumber daya**, **tugas**, tampilan **rekonsiliasi**, **perkiraan pengeluaran**) tetap dapat diedit bahkan saat proyek tidak aktif.</span><span class="sxs-lookup"><span data-stu-id="71008-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="71008-126">Pelanggan duplikat tidak dapat digabungkan dengan pelanggan yang ditautkan ke kontrak proyek yang telah dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="71008-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="71008-127">Bila sumber daya yang belum memiliki kalender yang valid ditambahkan, sistem tidak memberikan pesan kesalahan yang mudah digunakan pengguna.</span><span class="sxs-lookup"><span data-stu-id="71008-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="71008-128">Tombol **Tambah tugas** pada kisi tugas diaktifkan saat proyek ditautkan ke **Add-In Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="71008-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="71008-129">Upaya bertumbuh tak terkendali bila tugas dengan kategori ditetapkan ke sumber daya dengan peran yang telah ditentukan harga biayanya.</span><span class="sxs-lookup"><span data-stu-id="71008-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="71008-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="71008-130">**Sales**</span></span>

<span data-ttu-id="71008-131">Penyempurnaan berikut telah dilakukan:</span><span class="sxs-lookup"><span data-stu-id="71008-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="71008-132">**Frekuensi faktur** dan **awal penagihan** telah dipindahkan ke tab **jadwal faktur**.</span><span class="sxs-lookup"><span data-stu-id="71008-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="71008-133">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="71008-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="71008-134">**Total harga penjualan** adalah nol (0) untuk **kategori** meskipun **peran** memiliki total harga penjualan yang bukan nol.</span><span class="sxs-lookup"><span data-stu-id="71008-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="71008-135">Pelanggan tidak dapat mengubah nilai bidang **status faktur** menjadi **siap untuk faktur** saat proses kustom lain memperbarui bidang tambahan.</span><span class="sxs-lookup"><span data-stu-id="71008-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="71008-136">Tombol **Segarkan baris faktur** dapat membuat beberapa baris duplikat jika berulang kali dipilih.</span><span class="sxs-lookup"><span data-stu-id="71008-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="71008-137">Tombol **Perbarui Harga** tidak berfungsi pada subgrid **Harga Peran** dalam formulir **Tampilan Cepat**.</span><span class="sxs-lookup"><span data-stu-id="71008-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="71008-138">Logika **resolusi daftar harga penjualan** menangani zona waktu dengan tidak baik, sehingga pilihan daftar harganya salah.</span><span class="sxs-lookup"><span data-stu-id="71008-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="71008-139">Biaya **total aktual proyek** dapat dinonaktifkan dengan jumlah pecahan setelah entri satu kali disetujui.</span><span class="sxs-lookup"><span data-stu-id="71008-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="71008-140">Logika **resolusi harga** tidak menyediakan pesan kesalahan yang mudah digunakan jika **Harga Peran yang Diperoleh** tidak memiliki nilai pada bidang **'unit utama'** dan **'harga di unit utama'**.</span><span class="sxs-lookup"><span data-stu-id="71008-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 20, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 20, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: 5562b1de1d655328cfbb22e46c7fed53525507b3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006515"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="a699e-103">Project Service Automation Pembaruan Rilis 20, V3</span><span class="sxs-lookup"><span data-stu-id="a699e-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a699e-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a699e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a699e-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="a699e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a699e-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="a699e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a699e-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="a699e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a699e-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a699e-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a699e-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 20.</span><span class="sxs-lookup"><span data-stu-id="a699e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="a699e-110">Versi ini memiliki nomor pembuatan V 3.10.31.37 dan umumnya tersedia melalui pembaruan mandiri pada Juni 2020.</span><span class="sxs-lookup"><span data-stu-id="a699e-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="a699e-111">Pembaruan rilis 20</span><span class="sxs-lookup"><span data-stu-id="a699e-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a699e-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="a699e-112">Bug fixes</span></span>

<span data-ttu-id="a699e-113">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="a699e-113">**Project Management**</span></span>

<span data-ttu-id="a699e-114">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="a699e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a699e-115">Mengimpor anggota tim proyek dengan metode alokasi yang memerlukan jam menghasilkan pesan kesalahan yang tidak jelas saat jam yang ditentukan adalah nol.</span><span class="sxs-lookup"><span data-stu-id="a699e-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="a699e-116">Pengguna menerima kesalahan yang salah ketika jumlah maksimum karakter telah dimasukkan ke dalam bidang **Deskripsi** untuk tugas proyek.</span><span class="sxs-lookup"><span data-stu-id="a699e-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="a699e-117">Halaman **unduh add-in Microsoft Dynamics 365 Project Service Automation** akan mengalihkan ke halaman unduh bahasa Inggris bila pengaturan bahasa pengguna diatur ke bahasa Jepang.</span><span class="sxs-lookup"><span data-stu-id="a699e-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="a699e-118">Bila terjadi kesalahan server, label sinkronisasi pada tab **jadwal** formulir **proyek** terkadang tetap ada.</span><span class="sxs-lookup"><span data-stu-id="a699e-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="a699e-119">Pembaruan tugas berlebihan dikirim ke server saat tugas dimodifikasi.</span><span class="sxs-lookup"><span data-stu-id="a699e-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="a699e-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a699e-120">**Sales**</span></span>

<span data-ttu-id="a699e-121">Masalah berikut telah diperbaiki:</span><span class="sxs-lookup"><span data-stu-id="a699e-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="a699e-122">Pada formulir **kontrak**, klik dua kali **buat faktur** akan membuat dua faktur untuk rekaman aktual tunggal.</span><span class="sxs-lookup"><span data-stu-id="a699e-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="a699e-123">Di Internet Explorer 11, pengguna tidak dapat membuat entri pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="a699e-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="a699e-124">Pembalikan biaya dan pembalikan aktual penjualan yang tidak ditagihkan tidak terkait.</span><span class="sxs-lookup"><span data-stu-id="a699e-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="a699e-125">Tombol **refresh aktual** pada formulir **proyek** tidak me- refresh **jam aktual tugas**.</span><span class="sxs-lookup"><span data-stu-id="a699e-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="a699e-126">Plugin **PreValidateProjectTeamMemberCreate** dapat membuat sumber daya duplikat generik yang dapat dipesan saat atribut **msdyn_isgenericresourceprojectscoped** diatur ke **Salah**.</span><span class="sxs-lookup"><span data-stu-id="a699e-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="a699e-127">**Hitung ulang** menghapus biaya yang dibebankan pada detail baris kuotasi berdasarkan produk dan rincian baris kontrak.</span><span class="sxs-lookup"><span data-stu-id="a699e-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="a699e-128">Dalam skenario tertentu, plug-in **PostEstimateLineUpdate** menampilkan kesalahan pengecualian referensi kosong.</span><span class="sxs-lookup"><span data-stu-id="a699e-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="a699e-129">Durasi fase waktu pada **diagram analisis profitabilitas** tidak sesuai dengan durasi biaya dalam detail baris kuotasi harga tetap dari kuotasi.</span><span class="sxs-lookup"><span data-stu-id="a699e-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="a699e-130">Nilai grup unit dan unit tidak ter-default dengan benar untuk kategori pengeluaran pada **rincian baris kontrak** dan formulir **rincian baris kuotasi**.</span><span class="sxs-lookup"><span data-stu-id="a699e-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="a699e-131">Izin daftar **harga unit organisasi** tumpang tindih di efektivitas tanggal.</span><span class="sxs-lookup"><span data-stu-id="a699e-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="a699e-132">Pengguna tidak diizinkan untuk mengubah **orgunit** saat jenis pesanan tidak berbasis pekerjaan karena akan menyebabkan kesalahan pengecualian referensi kosong.</span><span class="sxs-lookup"><span data-stu-id="a699e-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="a699e-133">Saat mencoba menavigasi dari formulir **rincian baris kuotasi**, kembali ke tab **kuotasi**, formulir akan menyegarkan dan menampilkan tab **ringkasan**.</span><span class="sxs-lookup"><span data-stu-id="a699e-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
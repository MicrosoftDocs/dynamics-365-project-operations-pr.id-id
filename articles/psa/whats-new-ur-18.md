---
title: Yang baru atau diubah di Project Service Automation Rilis Pembaruan 18, V3
description: Topik ini berisi daftar fitur dan perbaikan yang tersedia di Project Service Automation V3, pembaruan rilis 18, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078438"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="47dcb-103">Project Service Automation Pembaruan Rilis 18, V3</span><span class="sxs-lookup"><span data-stu-id="47dcb-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="47dcb-104">Kami dengan senang hati mengumumkan pembaruan terbaru untuk aplikasi Project Service Automation untuk Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="47dcb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="47dcb-105">Rilis ini mencakup beberapa peningkatan penting untuk kualitas, kinerja, dan kegunaan.</span><span class="sxs-lookup"><span data-stu-id="47dcb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="47dcb-106">Rilis ini kompatibel dengan Dynamics 365 9. x.</span><span class="sxs-lookup"><span data-stu-id="47dcb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="47dcb-107">Untuk memperbarui ke rilis ini, kunjungi Pusat admin untuk Dynamics 365 online, halaman solusi untuk menginstal pembaruan.</span><span class="sxs-lookup"><span data-stu-id="47dcb-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="47dcb-108">Untuk informasi lebih lanjut: [Menginstal, memperbarui, atau menghapus solusi pilihan](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="47dcb-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="47dcb-109">Topik ini berisi daftar fitur dan perbaikan yang baru atau diubah untuk Project Service Automation V3, pembaruan rilis 18.</span><span class="sxs-lookup"><span data-stu-id="47dcb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="47dcb-110">Versi ini memiliki nomor pembuatan V3.10.8.12 dan umumnya tersedia melalui pembaruan mandiri pada April 2020.</span><span class="sxs-lookup"><span data-stu-id="47dcb-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="47dcb-111">Pembaruan rilis 18</span><span class="sxs-lookup"><span data-stu-id="47dcb-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="47dcb-112">Perbaikan bug</span><span class="sxs-lookup"><span data-stu-id="47dcb-112">Bug fixes</span></span>

<span data-ttu-id="47dcb-113">**Waktu dan Pengeluaran**</span><span class="sxs-lookup"><span data-stu-id="47dcb-113">**Time and Expense**</span></span>

- <span data-ttu-id="47dcb-114">Diperbaiki: aliran **penarikan** , **permintaan** , dan **membatalkan persetujuan** menghasilkan pengecualian dengan pesan kesalahan tidak jelas.</span><span class="sxs-lookup"><span data-stu-id="47dcb-114">Fixed: **Recall** , **Request** , and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="47dcb-115">Diperbaiki: saat **membatalkan persetujuan** gagal untuk pengeluaran, kesalahan pengecualian yang relevan tidak dihasilkan.</span><span class="sxs-lookup"><span data-stu-id="47dcb-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="47dcb-116">Diperbaiki: kisi waktu entri salah menangani hari non-kerja di Australia setelah beralih ke Daylight Savings Time (DST) di Oktober.</span><span class="sxs-lookup"><span data-stu-id="47dcb-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="47dcb-117">Diperbaiki: logika default yang salah mencegah pengajuan pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="47dcb-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="47dcb-118">Diperbaiki: bila persetujuan entri waktu gagal, persetujuan tetap dalam status **tertunda**.</span><span class="sxs-lookup"><span data-stu-id="47dcb-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="47dcb-119">Diperbaiki: kesalahan SQL pada persetujuan massal (kemacetan/batas waktu).</span><span class="sxs-lookup"><span data-stu-id="47dcb-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="47dcb-120">Diperbaiki: masalah kinerja yang signifikan dalam pengalaman pengguna yang disebabkan oleh memperbarui anggota tim saat menyetujui entri waktu.</span><span class="sxs-lookup"><span data-stu-id="47dcb-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="47dcb-121">**Manajemen proyek**</span><span class="sxs-lookup"><span data-stu-id="47dcb-121">**Project Management**</span></span>

- <span data-ttu-id="47dcb-122">Diperbaiki: pemberitahuan zona waktu dipindahkan dari tampilan **rekonsiliasi** ke formulir utama **proyek**.</span><span class="sxs-lookup"><span data-stu-id="47dcb-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="47dcb-123">Diperbaiki: template kalender tidak dengan benar disetel ke format otomatis saat formulir proyek baru terbuka.</span><span class="sxs-lookup"><span data-stu-id="47dcb-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="47dcb-124">Diperbaiki: untuk browser berbasis Chromium, pengguna tidak dapat dengan mudah memilih tugas pendahulu untuk dihapus.</span><span class="sxs-lookup"><span data-stu-id="47dcb-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="47dcb-125">Diperbaiki: membuat atau menyalin **proyek dari template kosong** mengambil tugas yang tidak terkait.</span><span class="sxs-lookup"><span data-stu-id="47dcb-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="47dcb-126">Diperbaiki: di kasus tepi tertentu, membuat tugas baru dari kisi tugas menyebabkan rekaman duplikat dibuat.</span><span class="sxs-lookup"><span data-stu-id="47dcb-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="47dcb-127">Diperbaiki: dalam mode manual, pengguna tidak dapat memperbarui tanggal mulai tugas agar lebih belakangan dari tanggal saat ini yang disimpan.</span><span class="sxs-lookup"><span data-stu-id="47dcb-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="47dcb-128">**Manajemen sumber daya**</span><span class="sxs-lookup"><span data-stu-id="47dcb-128">**Resource Management**</span></span>

- <span data-ttu-id="47dcb-129">Diperbaiki: baris subtotal tampilan **rekonsiliasi** salah menghitung Pemesanan setelah memperpanjang Pemesanan.</span><span class="sxs-lookup"><span data-stu-id="47dcb-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="47dcb-130">Diperbaiki: tampilan **rekonsiliasi** salah menampilkan tugas sumber daya saat sumber daya dapat dipesan memiliki kalender yang tidak cocok dengan kalender proyek.</span><span class="sxs-lookup"><span data-stu-id="47dcb-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="47dcb-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="47dcb-131">**Sales**</span></span>

- <span data-ttu-id="47dcb-132">Diperbaiki: bila entri waktu disetujui ulang ( **setujui > Batalkan >** setujui lagi), nilai aktual tidak dikenai biaya duplikat dibuat.</span><span class="sxs-lookup"><span data-stu-id="47dcb-132">Fixed: When time entries are re-approved ( **Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>

---
title: Model keamanan
description: Topik ini memberikan informasi tentang model keamanan di Dynamics 365 Project Operations.
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 8acaa86dec8ebca8f9850877d345e30be3e3a919
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951213"
---
# <a name="security-model"></a><span data-ttu-id="d1261-103">Model keamanan</span><span class="sxs-lookup"><span data-stu-id="d1261-103">Security Model</span></span>

<span data-ttu-id="d1261-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="d1261-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="d1261-105">Microsoft Dynamics 365 Project Operations berisi model keamanan unik yang memungkinkan model keamanan bisnis berbasis peran yang berkolaborasi dengan Grup Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="d1261-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="d1261-106">Peran keamanan</span><span class="sxs-lookup"><span data-stu-id="d1261-106">Security roles</span></span>
<span data-ttu-id="d1261-107">Kemampuan Front-end Project Operations mencakup peran berikut:</span><span class="sxs-lookup"><span data-stu-id="d1261-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="d1261-108">Peran</span><span class="sxs-lookup"><span data-stu-id="d1261-108">Role</span></span>                          | <span data-ttu-id="d1261-109">KETERANGAN</span><span class="sxs-lookup"><span data-stu-id="d1261-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="d1261-110">Scope</span><span class="sxs-lookup"><span data-stu-id="d1261-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="d1261-111">Manajer praktik</span><span class="sxs-lookup"><span data-stu-id="d1261-111">Practice manager</span></span>              | <span data-ttu-id="d1261-112">Mendukung pelaporan lintas-proyek.</span><span class="sxs-lookup"><span data-stu-id="d1261-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="d1261-113">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="d1261-113">Business unit</span></span>              |
| <span data-ttu-id="d1261-114">Pemberi Persetujuan Proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-114">Project approver</span></span>              | <span data-ttu-id="d1261-115">Menyetujui waktu dan pengeluaran proyek.</span><span class="sxs-lookup"><span data-stu-id="d1261-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="d1261-116">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="d1261-116">Business unit</span></span> |
| <span data-ttu-id="d1261-117">Administrator penagihan proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-117">Project billing administrator</span></span> | <span data-ttu-id="d1261-118">Membuat proposal faktur.</span><span class="sxs-lookup"><span data-stu-id="d1261-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="d1261-119">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="d1261-119">Business unit</span></span> |
| <span data-ttu-id="d1261-120">Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-120">Project manager</span></span>               | <span data-ttu-id="d1261-121">Membuat rencana proyek dan meminta sumber daya.</span><span class="sxs-lookup"><span data-stu-id="d1261-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="d1261-122">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="d1261-122">Business unit</span></span> |
| <span data-ttu-id="d1261-123">Sumber Daya Proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-123">Project resource</span></span>              | <span data-ttu-id="d1261-124">Anggota tim yang dapat dipesan dan waktu laporan.</span><span class="sxs-lookup"><span data-stu-id="d1261-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="d1261-125">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="d1261-125">Business unit</span></span>|
| <span data-ttu-id="d1261-126">Manajer Sumber Daya</span><span class="sxs-lookup"><span data-stu-id="d1261-126">Resource manager</span></span>              | <span data-ttu-id="d1261-127">Semua fungsi manajemen sumber daya, seperti memenuhi permintaan sumber daya dan Pemesanan, dipisahkan untuk mendukung konfigurasi manajer proyek hibrida + manajer sumber daya dan peran Manajer sumber daya tunggal dan terpusat.</span><span class="sxs-lookup"><span data-stu-id="d1261-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="d1261-128">Unit bisnis</span><span class="sxs-lookup"><span data-stu-id="d1261-128">Business unit</span></span> |


<span data-ttu-id="d1261-129">Microsoft Project untuk web mencakup peran berikut:</span><span class="sxs-lookup"><span data-stu-id="d1261-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="d1261-130">Peran</span><span class="sxs-lookup"><span data-stu-id="d1261-130">Role</span></span>           | <span data-ttu-id="d1261-131">KETERANGAN</span><span class="sxs-lookup"><span data-stu-id="d1261-131">Description</span></span>                                                                                                        | <span data-ttu-id="d1261-132">Scope</span><span class="sxs-lookup"><span data-stu-id="d1261-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="d1261-133">Pengguna proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-133">Project user</span></span>   | <span data-ttu-id="d1261-134">Pengguna kolaboratif proyek yang mampu membuat proyek mereka sendiri dan melihat proyek yang dibagikan dengan mereka.</span><span class="sxs-lookup"><span data-stu-id="d1261-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="d1261-135">Pengguna</span><span class="sxs-lookup"><span data-stu-id="d1261-135">User</span></span>   |
| <span data-ttu-id="d1261-136">Sistem proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-136">Project system</span></span> | <span data-ttu-id="d1261-137">Peran yang digunakan untuk konteks aplikasi.</span><span class="sxs-lookup"><span data-stu-id="d1261-137">Role used for application   context.</span></span> <span data-ttu-id="d1261-138">Pelanggan tidak boleh menggunakan peran sistem ini.</span><span class="sxs-lookup"><span data-stu-id="d1261-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="d1261-139">Global</span><span class="sxs-lookup"><span data-stu-id="d1261-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="d1261-140">Penegakan keamanan</span><span class="sxs-lookup"><span data-stu-id="d1261-140">Security enforcement</span></span>
<span data-ttu-id="d1261-141">Tindakan yang dilakukan di tingkat proyek dilakukan dalam konteks pengguna yang masuk.</span><span class="sxs-lookup"><span data-stu-id="d1261-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="d1261-142">Ini berarti bahwa untuk membuat, membuka, atau menghapus suatu proyek, pengguna diharuskan memiliki akses yang tersedia dalam CDS.</span><span class="sxs-lookup"><span data-stu-id="d1261-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="d1261-143">Akses dalam CDS dapat diberikan melalui salah satu mekanisme yang mungkin tercakup dalam platform.</span><span class="sxs-lookup"><span data-stu-id="d1261-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="d1261-144">Misalnya, pengguna dengan cakupan yang lebih besar dapat mengakses proyek atau jika tindakan berbagi proyek eksplisit telah dilakukan yang memberikan akses kepada pengguna.</span><span class="sxs-lookup"><span data-stu-id="d1261-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="d1261-145">Penting untuk mempertimbangkan hal ini saat membuat proyek di Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d1261-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="d1261-146">Kolaborasi grup modern dengan Project Operations</span><span class="sxs-lookup"><span data-stu-id="d1261-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="d1261-147">Proyek untuk web dan Project Operations mendukung grup modern untuk kolaborasi.</span><span class="sxs-lookup"><span data-stu-id="d1261-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="d1261-148">Pengguna yang ditambahkan ke proyek melalui Grup dapat mengedit rencana proyek.</span><span class="sxs-lookup"><span data-stu-id="d1261-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="d1261-149">Proyek untuk web menambahkan pengguna ke grup secara otomatis setelah penetapan.</span><span class="sxs-lookup"><span data-stu-id="d1261-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="d1261-150">Grup memungkinkan izin proyek dan mendukung artefak kolaborasi agar dapat dikerjakan secara kolaboratif.</span><span class="sxs-lookup"><span data-stu-id="d1261-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="d1261-151">Diagram berikut menggambarkan peristiwa dan perubahan status yang terjadi selama proses penetapan grup.</span><span class="sxs-lookup"><span data-stu-id="d1261-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="d1261-152">Project Operations tidak membuat grup melalui tindakan implisit dan hanya melakukannya melalui tindakan eksplisit grup penekan.</span><span class="sxs-lookup"><span data-stu-id="d1261-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="d1261-153">Pencarian anggota grup di dialog **manajemen grup**, terbatas untuk mereka yang ditetapkan sebagai bagian dari grup keamanan lingkungan.</span><span class="sxs-lookup"><span data-stu-id="d1261-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="d1261-154">Untuk informasi lebih lanjut, lihat [Mengontrol akses pengguna ke lingkungan: grup keamanan dan lisensi](/power-platform/admin/control-user-access).</span><span class="sxs-lookup"><span data-stu-id="d1261-154">For more information, see [Control user access to environments: security groups and licenses](/power-platform/admin/control-user-access).</span></span>

![Mode grup](./media/groupsmode.png)

1. <span data-ttu-id="d1261-156">Proyek dibuat dan dimiliki oleh pengguna yang membuat.</span><span class="sxs-lookup"><span data-stu-id="d1261-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="d1261-157">Pemilik proyek diperbarui ke tim.</span><span class="sxs-lookup"><span data-stu-id="d1261-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="d1261-158">Tim pemilik dipetakan ke grup Office yang ditentukan atau dibuat.</span><span class="sxs-lookup"><span data-stu-id="d1261-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="d1261-159">Pemilik asli proyek ditambahkan ke Office Group.</span><span class="sxs-lookup"><span data-stu-id="d1261-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="d1261-160">Rekomendasi penyebaran</span><span class="sxs-lookup"><span data-stu-id="d1261-160">Deployment recommendation</span></span>
<span data-ttu-id="d1261-161">Seiring model kolaborasi Office Group berkembang, fungsi akan ditambahkan untuk memberikan kontrol yang lebih rinci dari waktu ke waktu.</span><span class="sxs-lookup"><span data-stu-id="d1261-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="d1261-162">Pelanggan yang menyebarkan Project Operations saat ini didorong untuk fokus pada model keamanan Microsoft Dynamics 365 tradisional.</span><span class="sxs-lookup"><span data-stu-id="d1261-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="d1261-163">Untuk informasi lebih lanjut, lihat [keamanan di Common Data Service](/power-platform/admin/wp-security).</span><span class="sxs-lookup"><span data-stu-id="d1261-163">For more information, see [Security in Common Data Service](/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="d1261-164">Keamanan Microsoft Dynamics 365 Finance dan Project Operations</span><span class="sxs-lookup"><span data-stu-id="d1261-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="d1261-165">Operasi proyek mencakup peran berikut:</span><span class="sxs-lookup"><span data-stu-id="d1261-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="d1261-166">Manajer Proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-166">Project manager</span></span>
- <span data-ttu-id="d1261-167">Akuntan proyek</span><span class="sxs-lookup"><span data-stu-id="d1261-167">Project accountant</span></span>

<span data-ttu-id="d1261-168">Untuk informasi lebih lanjut tentang peran keamanan di Finance, lihat [keamanan berbasis peran](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span><span class="sxs-lookup"><span data-stu-id="d1261-168">For more information about security in Finance, see [Role-based security](/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Memecahkan masalah penanganan kisi Tugas
description: Pembaruan topik memberikan informasi pemecahan masalah yang diperlukan saat menangani kisi Tugas.
author: ruhercul
ms.date: 01/19/2021
ms.topic: article
ms.product: ''
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a15a4752de7537b3f60d5ee3269c846257a1fe4a
ms.sourcegitcommit: 72fa1f09fe406805f7009fc68e2f3eeeb9b7d5fc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 06/09/2021
ms.locfileid: "6213404"
---
# <a name="troubleshoot-working-in-the-task-grid"></a><span data-ttu-id="322fc-103">Memecahkan masalah penanganan kisi Tugas</span><span class="sxs-lookup"><span data-stu-id="322fc-103">Troubleshoot working in the Task grid</span></span> 

<span data-ttu-id="322fc-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="322fc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="322fc-105">Deskripsi topik menjelaskan cara memperbaiki masalah yang mungkin Anda temui saat menangani manajemen biaya.</span><span class="sxs-lookup"><span data-stu-id="322fc-105">This topic describes how to fix issues that you might encounter while working with cost management.</span></span>

## <a name="enable-cookies"></a><span data-ttu-id="322fc-106">Aktifkan Cookie</span><span class="sxs-lookup"><span data-stu-id="322fc-106">Enable cookies</span></span>

<span data-ttu-id="322fc-107">Project Operations mengharuskan cookie pihak ketiga diaktifkan untuk membuat struktur perincian kerja.</span><span class="sxs-lookup"><span data-stu-id="322fc-107">Project Operations requires that third-party cookies be enabled in order to render the work breakdown structure.</span></span> <span data-ttu-id="322fc-108">Bila cookie pihak ketiga tidak diaktifkan, bukan melihat tugas, Anda akan melihat halaman kosong saat memilih tab **Tugas** di halaman **Proyek**.</span><span class="sxs-lookup"><span data-stu-id="322fc-108">When third-party cookies aren't enabled, instead of seeing tasks, you will see a blank page when you select the **Tasks** tab on the **Project** page.</span></span>

![Tab kosong bila cookie pihak ketiga tidak diaktifkan](media/blankschedule.png)


### <a name="workaround"></a><span data-ttu-id="322fc-110">Solusi</span><span class="sxs-lookup"><span data-stu-id="322fc-110">Workaround</span></span>
<span data-ttu-id="322fc-111">Untuk Microsoft Edge atau browser Google Chrome, prosedur berikut menjelaskan cara memperbarui pengaturan browser Anda untuk mengaktifkan cookie pihak ketiga.</span><span class="sxs-lookup"><span data-stu-id="322fc-111">For Microsoft Edge or Google Chrome browsers, the following procedures outline how to update your browser setting to enable third-party cookies.</span></span>

#### <a name="microsoft-edge"></a><span data-ttu-id="322fc-112">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="322fc-112">Microsoft Edge</span></span>

1. <span data-ttu-id="322fc-113">Buka browser Edgé Anda.</span><span class="sxs-lookup"><span data-stu-id="322fc-113">Open your Edge browser.</span></span>
2. <span data-ttu-id="322fc-114">Di sudut kanan atas, pilih **elipsis (...)**, lalu pilih **pengaturan**.</span><span class="sxs-lookup"><span data-stu-id="322fc-114">In the upper-right corner, select the **ellipsis** (...), and then select **Settings**.</span></span>
3. <span data-ttu-id="322fc-115">Dalam **Cookie dan izin situs**, pilih **Cookie dan data situs**.</span><span class="sxs-lookup"><span data-stu-id="322fc-115">Under **Cookies and site permissions**, select **Cookies and site data**.</span></span>
4. <span data-ttu-id="322fc-116">Nonaktifkan **Blokir cookie pihak ketiga**.</span><span class="sxs-lookup"><span data-stu-id="322fc-116">Turn off **Block third-party cookies**.</span></span>

#### <a name="google-chrome"></a><span data-ttu-id="322fc-117">Google Chrome</span><span class="sxs-lookup"><span data-stu-id="322fc-117">Google Chrome</span></span>

1. <span data-ttu-id="322fc-118">Buka browser Chrome Anda.</span><span class="sxs-lookup"><span data-stu-id="322fc-118">Open your Chrome browser.</span></span>
2. <span data-ttu-id="322fc-119">Di sudut kanan atas, pilih tiga titik vertikal, lalu pilih **pengaturan**.</span><span class="sxs-lookup"><span data-stu-id="322fc-119">In the upper-right corner, select the three vertical dots, and then select **Settings**.</span></span>
3. <span data-ttu-id="322fc-120">Dalam **Privasi dan keamanan**, pilih **Cookie dan data situs lainnya**.</span><span class="sxs-lookup"><span data-stu-id="322fc-120">Under **Privacy and security**, select **Cookies and other site data**.</span></span>
4. <span data-ttu-id="322fc-121">Pilih **Izinkan semua cookie**.</span><span class="sxs-lookup"><span data-stu-id="322fc-121">Select **Allow all cookies**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="322fc-122">Jika Anda memblokir cookie pihak ketiga, semua cookie dan data situs dari situs lain akan diblokir, meskipun situs diizinkan pada daftar pengecualian Anda.</span><span class="sxs-lookup"><span data-stu-id="322fc-122">If you block third-party cookies, all cookies and site data from other sites will be blocked, even if the site is allowed on your exceptions list.</span></span>

## <a name="pex-endpoint"></a><span data-ttu-id="322fc-123">Titik Akhir PEX</span><span class="sxs-lookup"><span data-stu-id="322fc-123">PEX Endpoint</span></span>

<span data-ttu-id="322fc-124">Project Operations mengharuskan parameter proyek mereferensi titik akhir PEX.</span><span class="sxs-lookup"><span data-stu-id="322fc-124">Project Operations requires that a project parameter reference the PEX Endpoint.</span></span> <span data-ttu-id="322fc-125">Titik akhir ini diperlukan untuk berkomunikasi dengan layanan yang digunakan untuk membuat struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="322fc-125">This endpoint is required to communicate with the service used to render the work breakdown structure.</span></span> <span data-ttu-id="322fc-126">Jika parameter tidak diaktifkan, Anda akan menerima kesalahan, "Parameter proyek tidak valid".</span><span class="sxs-lookup"><span data-stu-id="322fc-126">If the parameter isn't enabled, you will receive the error, "The project parameter is not valid".</span></span> 

### <a name="workaround"></a><span data-ttu-id="322fc-127">Solusi</span><span class="sxs-lookup"><span data-stu-id="322fc-127">Workaround</span></span>
 ![Bidang titik akhir PEX pada parameter proyek](media/projectparameter.png)

1. <span data-ttu-id="322fc-129">Tambahkan bidang **titik akhir** PEX ke halaman **Parameter Proyek**.</span><span class="sxs-lookup"><span data-stu-id="322fc-129">Add the **PEX Endpoint** field to the **Project Parameters** page.</span></span>
2. <span data-ttu-id="322fc-130">Perbarui bidang dengan nilai berikut ini: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span><span class="sxs-lookup"><span data-stu-id="322fc-130">Update the field with the following value: `https://project.microsoft.com/<lang>/?org=<cdsServer>#/taskgrid?projectId=/<id>&type=2`</span></span>
3. <span data-ttu-id="322fc-131">Hilangkan bidang dari halaman **Parameter Proyek**.</span><span class="sxs-lookup"><span data-stu-id="322fc-131">Remove the field from the **Project Parameters** page.</span></span>

## <a name="privileges-for-project-for-the-web"></a><span data-ttu-id="322fc-132">Hak istimewa untuk Proyek untuk Web</span><span class="sxs-lookup"><span data-stu-id="322fc-132">Privileges for Project for the Web</span></span>

<span data-ttu-id="322fc-133">Project Operations mengandalkan layanan penjadwalan eksternal.</span><span class="sxs-lookup"><span data-stu-id="322fc-133">Project Operations relies on an external scheduling service.</span></span> <span data-ttu-id="322fc-134">Layanan mengharuskan pengguna memiliki beberapa peran yang ditetapkan untuk membaca dan menulis ke entitas yang terkait dengan struktur rincian kerja.</span><span class="sxs-lookup"><span data-stu-id="322fc-134">The service requires that a user have several roles assigned to read and write to entities related to the work breakdown structure.</span></span> <span data-ttu-id="322fc-135">Entitas ini mencakup tugas proyek, penugasan sumber daya, dan dependensi tugas.</span><span class="sxs-lookup"><span data-stu-id="322fc-135">These entities include project tasks, resource assignments, and task dependencies.</span></span> <span data-ttu-id="322fc-136">Jika pengguna tidak dapat menampilkan struktur rincian kerja saat membuka tab **Tugas**, kemungkinan karena Proyek untuk Project Operations belum diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="322fc-136">If a user can't render the work breakdown structure when they go to the **Tasks** tab, it's probably because Project for Project Operations hasn't been enabled.</span></span> <span data-ttu-id="322fc-137">Pengguna mungkin menerima pesan kesalahan peran keamanan, atau kesalahan yang terkait dengan ditolaknya akses.</span><span class="sxs-lookup"><span data-stu-id="322fc-137">A user might receive either a security role error, or an error related to a denial of access.</span></span>


## <a name="workaround"></a><span data-ttu-id="322fc-138">Solusi</span><span class="sxs-lookup"><span data-stu-id="322fc-138">Workaround</span></span>

1. <span data-ttu-id="322fc-139">Buka **Pengaturan > Keamanan > Pengguna > Pengguna Aplikasi**.</span><span class="sxs-lookup"><span data-stu-id="322fc-139">Go to **Setting > Security > Users > Application Users**.</span></span>  

   ![Pembaca aplikasi](media/applicationuser.jpg)
   
2. <span data-ttu-id="322fc-141">Klik dua kali rekaman pengguna aplikasi untuk memverifikasi berikut ini:</span><span class="sxs-lookup"><span data-stu-id="322fc-141">Double-click the application user record to verify the following:</span></span>

 - <span data-ttu-id="322fc-142">Pengguna memiliki akses ke proyek.</span><span class="sxs-lookup"><span data-stu-id="322fc-142">The user has access to the project.</span></span> <span data-ttu-id="322fc-143">Verifikasi ini biasanya dilakukan dengan memastikan bahwa pengguna memiliki peran keamanan **Manajer Proyek**.</span><span class="sxs-lookup"><span data-stu-id="322fc-143">This verification is typically done by ensuring that the user has **Project Manager** security role.</span></span>
 - <span data-ttu-id="322fc-144">Pengguna aplikasi Microsoft Project ada dan dikonfigurasi dengan benar.</span><span class="sxs-lookup"><span data-stu-id="322fc-144">The Microsoft Project application user exists and is configured correctly.</span></span>
 
3. <span data-ttu-id="322fc-145">Jika pengguna ini tidak ada, Anda dapat membuat rekaman pengguna yang baru.</span><span class="sxs-lookup"><span data-stu-id="322fc-145">If this user doesn't exist, you can create a new user record.</span></span> <span data-ttu-id="322fc-146">Pilih **pengguna baru**.</span><span class="sxs-lookup"><span data-stu-id="322fc-146">Select **New Users**.</span></span> <span data-ttu-id="322fc-147">Ubah formulir entri ke **Pengguna Aplikasi**, lalu tambahkan **ID Aplikasi**.</span><span class="sxs-lookup"><span data-stu-id="322fc-147">Change the entry form to **Application User**, and then add the **Application ID**.</span></span>

   ![Rincian pengguna aplikasi](media/applicationuserdetails.jpg)

4. <span data-ttu-id="322fc-149">Verifikasikan bahwa pengguna telah menerima lisensi yang benar dan layanan diaktifkan dalam rincian paket layanan lisensi.</span><span class="sxs-lookup"><span data-stu-id="322fc-149">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
5. <span data-ttu-id="322fc-150">Pastikan pengguna dapat membuka project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="322fc-150">Verify that the user can open project.microsoft.com.</span></span>
6. <span data-ttu-id="322fc-151">Verifikasikan melalui parameter proyek bahwa sistem mengarah ke titik akhir proyek yang benar.</span><span class="sxs-lookup"><span data-stu-id="322fc-151">Verify through the project parameters that the system is pointing to the correct project endpoint.</span></span>
7. <span data-ttu-id="322fc-152">Verifikasikan bahwa pengguna aplikasi proyek dibuat.</span><span class="sxs-lookup"><span data-stu-id="322fc-152">Verify that the project application user is created.</span></span>
8. <span data-ttu-id="322fc-153">Terapkan peran keamanan berikut ke pengguna:</span><span class="sxs-lookup"><span data-stu-id="322fc-153">Apply the following security roles to the user:</span></span>

  - <span data-ttu-id="322fc-154">Pengguna Dataverse</span><span class="sxs-lookup"><span data-stu-id="322fc-154">Dataverse User</span></span>
  - <span data-ttu-id="322fc-155">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="322fc-155">Project Operations System</span></span>
  - <span data-ttu-id="322fc-156">Sistem proyek</span><span class="sxs-lookup"><span data-stu-id="322fc-156">Project System</span></span>

## <a name="error-when-updating-the-work-breakdown-structure"></a><span data-ttu-id="322fc-157">Kesalahan saat memperbarui struktur rincian kerja</span><span class="sxs-lookup"><span data-stu-id="322fc-157">Error when updating the work breakdown structure</span></span>

<span data-ttu-id="322fc-158">Ketika satu atau beberapa pembaruan dibuat pada struktur rincian kerja, perubahan pada akhirnya gagal dan tidak disimpan.</span><span class="sxs-lookup"><span data-stu-id="322fc-158">When one or more updates are made to the work breakdown structure, the changes eventually fail and aren't saved.</span></span> <span data-ttu-id="322fc-159">Kesalahan terjadi di kisi jadwal yang menyatakan bahwa "Perubahan terbaru yang anda buat tidak dapat disimpan".</span><span class="sxs-lookup"><span data-stu-id="322fc-159">An error occurs in the schedule grid noting that “Recent change you’ve made couldn’t be saved.”</span></span>

### <a name="workaround"></a><span data-ttu-id="322fc-160">Solusi</span><span class="sxs-lookup"><span data-stu-id="322fc-160">Workaround</span></span>

1. <span data-ttu-id="322fc-161">Verifikasikan bahwa pengguna telah menerima lisensi yang benar dan layanan diaktifkan dalam rincian paket layanan lisensi.</span><span class="sxs-lookup"><span data-stu-id="322fc-161">Verify that the user has been assigned the correct license and that the service is enabled in the service plans details of the license.</span></span>
2. <span data-ttu-id="322fc-162">Pastikan pengguna dapat membuka project.microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="322fc-162">Verify that the user can open project.microsoft.com.</span></span>
3. <span data-ttu-id="322fc-163">Verifikasikan bahwa sistem mengarah ke titik akhir proyek yang benar.</span><span class="sxs-lookup"><span data-stu-id="322fc-163">Verify that the system is pointing to the correct project endpoint,.</span></span>
4. <span data-ttu-id="322fc-164">Verifikasikan bahwa pengguna aplikasi proyek telah dibuat.</span><span class="sxs-lookup"><span data-stu-id="322fc-164">Verify that the Project Application user has been created.</span></span>
5. <span data-ttu-id="322fc-165">Terapkan peran keamanan berikut ke pengguna:</span><span class="sxs-lookup"><span data-stu-id="322fc-165">Apply the following security roles to the user:</span></span>
  
  - <span data-ttu-id="322fc-166">Pengguna dasar atau Pengguna Dataverse</span><span class="sxs-lookup"><span data-stu-id="322fc-166">Dataverse user or Base user</span></span>
  - <span data-ttu-id="322fc-167">Sistem Project Operations</span><span class="sxs-lookup"><span data-stu-id="322fc-167">Project Operations System</span></span>
  - <span data-ttu-id="322fc-168">Sistem proyek</span><span class="sxs-lookup"><span data-stu-id="322fc-168">Project System</span></span>
  - <span data-ttu-id="322fc-169">Sistem Tulis Ganda Project Operations (Peran ini diperlukan jika Anda menyebarkan skenario berbasis sumber daya/non-stok Project Operations.)</span><span class="sxs-lookup"><span data-stu-id="322fc-169">Project Operations Dual Write System (This role is required if you are deploying the resource/non-stocked based scenario of Project Operations.)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

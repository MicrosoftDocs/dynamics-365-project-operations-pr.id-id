---
title: Perbarui Project Operations di lingkungan Finance Anda
description: Topik ini menyediakan informasi tentang cara memperbarui Project Operations di lingkungan Dynamics 365 Finance Anda.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d68296ec59f0bd58f848154c90e02c58f275ab12
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291983"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="e344b-103">Perbarui Project Operations di lingkungan Finance Anda</span><span class="sxs-lookup"><span data-stu-id="e344b-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="e344b-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="e344b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="e344b-105">Topik ini menyediakan informasi tentang cara memperbarui Dynamics 365 Project Operations di lingkungan Dynamics 365 Finance Anda.</span><span class="sxs-lookup"><span data-stu-id="e344b-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="e344b-106">Ada tiga prosedur yang diperlukan untuk memperbarui Project Operations untuk Pembaruan 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="e344b-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="e344b-107">Impor paket ke proyek pratinjau</span><span class="sxs-lookup"><span data-stu-id="e344b-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="e344b-108">Terapkan pembaruan</span><span class="sxs-lookup"><span data-stu-id="e344b-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="e344b-109">Perbarui lingkungan Dataverse Anda</span><span class="sxs-lookup"><span data-stu-id="e344b-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="e344b-110">Impor paket ke proyek LCS Anda</span><span class="sxs-lookup"><span data-stu-id="e344b-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="e344b-111">Masuk ke [Lifecycle Services (LCS)](https://lcs.dynamics.com/) sebagai Pemilik Proyek atau manajer Lingkungan.</span><span class="sxs-lookup"><span data-stu-id="e344b-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="e344b-112">Dari daftar proyek, pilih proyek LCS Anda.</span><span class="sxs-lookup"><span data-stu-id="e344b-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="e344b-113">Pada halaman **Proyek**, dalam grup **Lingkungan**, buka lingkungan yang akan diperbarui.</span><span class="sxs-lookup"><span data-stu-id="e344b-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="e344b-114">Pastikan lingkungan berjalan.</span><span class="sxs-lookup"><span data-stu-id="e344b-114">Verify that the environment is running.</span></span> <span data-ttu-id="e344b-115">Jika belum dimulai, mulai lingkungan.</span><span class="sxs-lookup"><span data-stu-id="e344b-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="e344b-116">Di bagian **Rilis baru** dalam **Pembaruan yang tersedia**, pilih **Lihat pembaruan** untuk 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="e344b-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Lihat tombol Perbarui](media/view-update.png)

6. <span data-ttu-id="e344b-118">Pada halaman **pembaruan biner**, pilih **Simpan paket**.</span><span class="sxs-lookup"><span data-stu-id="e344b-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="e344b-119">Pada halaman **Tinjau dan simpan pembaruan**, pilih **Simpan paket**.</span><span class="sxs-lookup"><span data-stu-id="e344b-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="e344b-120">Pada panel **Simpan paket ke pustaka aset** yang terbuka, masukkan nama paket, lalu pilih **Simpan paket**.</span><span class="sxs-lookup"><span data-stu-id="e344b-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="e344b-121">Setelah LCS selesai menyimpan paket, tombol **Selesai** diaktifkan.</span><span class="sxs-lookup"><span data-stu-id="e344b-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="e344b-122">Pilih **Selesai**.</span><span class="sxs-lookup"><span data-stu-id="e344b-122">Select **Done**.</span></span> <span data-ttu-id="e344b-123">LCS akan memverifikasi paket.</span><span class="sxs-lookup"><span data-stu-id="e344b-123">LCS will verify the package.</span></span> <span data-ttu-id="e344b-124">Verifikasi dapat berlangsung selama beberapa menit atau hingga satu jam.</span><span class="sxs-lookup"><span data-stu-id="e344b-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="e344b-125">Terapkan pembaruan paket</span><span class="sxs-lookup"><span data-stu-id="e344b-125">Apply the package update</span></span>

1. <span data-ttu-id="e344b-126">Di LCS, pada halaman **rincian Lingkungan**, pilih **Pertahankan** > **Terapkan Pembaruan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="e344b-127">Dari daftar, pilih paket yang Anda simpan sebelumnya, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="e344b-128">Pilih **Ya** untuk mengkonfirmasikan bahwa Anda ingin menyebarkan paket.</span><span class="sxs-lookup"><span data-stu-id="e344b-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Kotak dialog Konfirmasikan penyebaran paket](media/confirm-package-deployment.png)

4. <span data-ttu-id="e344b-130">Pilih **Ya** untuk mengkonfirmasikan bahwa Anda ingin memperbarui aplikasi.</span><span class="sxs-lookup"><span data-stu-id="e344b-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Kotak dialog Konfirmasikan pembaruan aplikasi](media/confirm-application-update.png)

<span data-ttu-id="e344b-132">Penyebaran dan pembaruan aplikasi akan dimulai.</span><span class="sxs-lookup"><span data-stu-id="e344b-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="e344b-133">Pada halaman **rincian Lingkungan**, di sudut kanan atas, status lingkungan akan diperbarui ke **Pelayanan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="e344b-134">Dalam waktu sekitar dua jam, pembaruan akan selesai.</span><span class="sxs-lookup"><span data-stu-id="e344b-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="e344b-135">Informasi rilis aplikasi akan diperbarui ke **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** dan status lingkungan akan diperbarui ke **Disebarkan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="e344b-136">Perbarui lingkungan Dataverse Anda</span><span class="sxs-lookup"><span data-stu-id="e344b-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="e344b-137">Masuk ke [pusat admin Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="e344b-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="e344b-138">Dalam daftar, cari dan buka lingkungan yang digunakan untuk menginstal Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e344b-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="e344b-139">Pada halaman **Lingkungan**, pilih **Sumber Daya** > **aplikasi Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="e344b-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="e344b-140">Dalam daftar, cari **Microsoft Dynamics 365 Project Operations**, dan di kolom **Status**, pilih **Tersedia Pembaruan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="e344b-141">Pilih kotak centang **Saya menyetujui ketentuan layanan**, lalu pilih **Perbarui**.</span><span class="sxs-lookup"><span data-stu-id="e344b-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="e344b-142">Versi terbaru solusi akan diinstal.</span><span class="sxs-lookup"><span data-stu-id="e344b-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="e344b-143">Setelah penginstalan selesai, Anda akan memiliki versi yang 4.5.0.134 diinstal.</span><span class="sxs-lookup"><span data-stu-id="e344b-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="e344b-144">Mengonfigurasi fitur baru</span><span class="sxs-lookup"><span data-stu-id="e344b-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="e344b-145">Aktifkan pemetaan Tulis Ganda</span><span class="sxs-lookup"><span data-stu-id="e344b-145">Enable dual-write mapping</span></span>

<span data-ttu-id="e344b-146">Setelah menyelesaikan pembaruan Finance dan lingkungan Dataverse, Anda dapat mengaktifkan pemetaan penulisan gandasar yang diperlukan.</span><span class="sxs-lookup"><span data-stu-id="e344b-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="e344b-147">Selesaikan prosedur berikut ini untuk mengaktifkan pemetaan tulis ganda.</span><span class="sxs-lookup"><span data-stu-id="e344b-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="e344b-148">Memperbarui pengaturan keamanan di lingkungan Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="e344b-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="e344b-149">Segarkan entitas data</span><span class="sxs-lookup"><span data-stu-id="e344b-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="e344b-150">Memperbarui dan menjalankan pemetaan penulisan ganda</span><span class="sxs-lookup"><span data-stu-id="e344b-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="e344b-151">Memperbarui pengaturan keamanan di lingkungan Dataverse</span><span class="sxs-lookup"><span data-stu-id="e344b-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="e344b-152">Pembaruan berikut pada hak istimewa keamanan entitas diperlukan sebagai bagian dari pembaruan UR5.</span><span class="sxs-lookup"><span data-stu-id="e344b-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="e344b-153">Di lingkungan Dataverse Anda, buka **Pengaturan**, dan di grup **Sistem**, pilih **Keamanan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Pengaturan lingkungan Dataverse](media/Picture21.png)

2. <span data-ttu-id="e344b-155">Pilih **Peran Keamanan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="e344b-156">Dari daftar peran, pilih **pengguna aplikasi penulisan ganda** dan pilih tab **Entitas Kustom**.</span><span class="sxs-lookup"><span data-stu-id="e344b-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="e344b-157">Pastikan peran memiliki izin **Baca** dan **Lampirkan ke** untuk:</span><span class="sxs-lookup"><span data-stu-id="e344b-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="e344b-158">**Jenis Nilai Tukar Mata Uang**</span><span class="sxs-lookup"><span data-stu-id="e344b-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="e344b-159">**Bagan Akun**</span><span class="sxs-lookup"><span data-stu-id="e344b-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="e344b-160">**Kalender Fiskal**</span><span class="sxs-lookup"><span data-stu-id="e344b-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="e344b-161">**Buku besar**</span><span class="sxs-lookup"><span data-stu-id="e344b-161">**Ledger**</span></span>

5. <span data-ttu-id="e344b-162">Setelah peran keamanan diperbarui, buka **Pengaturan** > **Keamanan** > **Tim**.</span><span class="sxs-lookup"><span data-stu-id="e344b-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="e344b-163">Pastikan peran **pengguna aplikasi penulisan ganda** telah diterapkan ke tim.</span><span class="sxs-lookup"><span data-stu-id="e344b-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="e344b-164">segarkan entitas data dari pembaruan</span><span class="sxs-lookup"><span data-stu-id="e344b-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="e344b-165">Di lingkungan Finance, buka ruang kerja **manajemen Data**, lalu buka halaman **parameter Kerangka Kerja**.</span><span class="sxs-lookup"><span data-stu-id="e344b-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="e344b-166">Pada tab **Pengaturan entitas**, pilih **Segarkan daftar entitas**.</span><span class="sxs-lookup"><span data-stu-id="e344b-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="e344b-167">Pilih **Tutup** untuk mengkonfirmasi penyegaran entitas.</span><span class="sxs-lookup"><span data-stu-id="e344b-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="e344b-168">Proses ini akan berlangsung kira-kira 20 menit untuk diselesaikan.</span><span class="sxs-lookup"><span data-stu-id="e344b-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="e344b-169">Anda akan diberi tahu setelah pembaruan selesai.</span><span class="sxs-lookup"><span data-stu-id="e344b-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="e344b-170">Perbarui pemetaan Tulis Ganda</span><span class="sxs-lookup"><span data-stu-id="e344b-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="e344b-171">Di ruang kerja **manajemen Data**, pilih **Tulis ganda**.</span><span class="sxs-lookup"><span data-stu-id="e344b-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="e344b-172">Pilih **Terapkan solusi**, pilih kedua solusi dalam daftar, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="e344b-173">Pada halaman **Tulis ganda**, pilih peta tabel berikut, lalu pilih **Berhenti**.</span><span class="sxs-lookup"><span data-stu-id="e344b-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="e344b-174">**Aktual Integrasi Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="e344b-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="e344b-175">**Kategori pengeluaran proyek integrasi Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="e344b-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="e344b-176">**entitas ekspor pengeluaran proyek aktual integrasi Project Operations (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="e344b-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="e344b-177">Pada halaman **versi peta tabel**, terapkan versi baru peta untuk masing-masing dari ketiga entitas.</span><span class="sxs-lookup"><span data-stu-id="e344b-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="e344b-178">Pada halaman **Penulisan ganda**, pilih jalankan untuk memulai ulang peta.</span><span class="sxs-lookup"><span data-stu-id="e344b-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="e344b-179">Dari daftar peta, pilih peta **buku besar (msdyn_ledgers)** dengan semua prasyarat dan pilih kotak centang **Sinkronisasi awal**.</span><span class="sxs-lookup"><span data-stu-id="e344b-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="e344b-180">Di bidang **Induk untuk sinkronisasi awal**, pilih **aplikasi Finance and Operations**, lalu pilih **Jalankan**.</span><span class="sxs-lookup"><span data-stu-id="e344b-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Sinkronisasi peta buku besar](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Penyediaan lingkungan baru
description: Topik ini menyediakan informasi tentang bagaimana menyediakan lingkungan Project Operations baru.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ee9e4c31d1972e3a75ad214071b31527f0ca826
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950538"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="554d0-103">Penyediaan lingkungan baru</span><span class="sxs-lookup"><span data-stu-id="554d0-103">Provision a new environment</span></span>

<span data-ttu-id="554d0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="554d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="554d0-105">Topik ini menyediakan informasi tentang cara menyediakan lingkungan Dynamics 365 Project Operations untuk skenario berbasis sumber daya/non-stok.</span><span class="sxs-lookup"><span data-stu-id="554d0-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="554d0-106">Aktifkan penetapan otomatis Project Operations dalam proyek LCS</span><span class="sxs-lookup"><span data-stu-id="554d0-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="554d0-107">Gunakan langkah-langkah berikut untuk mengaktifkan alur penyediaan otomatis Project Operations untuk proyek LCS Anda.</span><span class="sxs-lookup"><span data-stu-id="554d0-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="554d0-108">Buka [LCS](https://lcs.dynamics.com/v2), lalu pilih ubin **manajemen fitur pratinjau**.</span><span class="sxs-lookup"><span data-stu-id="554d0-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="554d0-109">Dalam Daftar **fitur pratinjau**, pilih **Fitur Project Operations**, kemudian pilih **fitur pratinjau yang diaktifkan** untuk mengaktifkan Project Operations.</span><span class="sxs-lookup"><span data-stu-id="554d0-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="554d0-110">Langkah ini dilakukan hanya satu kali per proyek LCS.</span><span class="sxs-lookup"><span data-stu-id="554d0-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="554d0-111">Penyediaan lingkungan Project Operations</span><span class="sxs-lookup"><span data-stu-id="554d0-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="554d0-112">Buka Dynamics 365 Finance [lingkungan demo](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) baru atau penyebaran [lingkungan produksi/Sandbox](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="554d0-112">Open a new Dynamics 365 Finance [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="554d0-113">Lalui Wizard **penyediaan lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="554d0-114">Pastikan versi aplikasi yang dipilih adalah 10.0.13 atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="554d0-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="554d0-115">Untuk menyediakan Project Operations, di dalam **pengaturan lanjutan**, pilih **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="554d0-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="554d0-116">Aktifkan **pengaturan Common Data Service** dengan memilih **ya**, lalu masukkan informasi di bidang wajib:</span><span class="sxs-lookup"><span data-stu-id="554d0-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="554d0-117">Nama</span><span class="sxs-lookup"><span data-stu-id="554d0-117">Name</span></span>
  - <span data-ttu-id="554d0-118">Wilayah</span><span class="sxs-lookup"><span data-stu-id="554d0-118">Region</span></span>
  - <span data-ttu-id="554d0-119">Bahasa</span><span class="sxs-lookup"><span data-stu-id="554d0-119">Language</span></span>
  - <span data-ttu-id="554d0-120">Mata uang</span><span class="sxs-lookup"><span data-stu-id="554d0-120">Currency</span></span>
 
5. <span data-ttu-id="554d0-121">Di bidang **template Common Data Service**, pilih **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="554d0-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="554d0-122">Pilih jenis lingkungan untuk penyebaran Anda.</span><span class="sxs-lookup"><span data-stu-id="554d0-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="554d0-123">Uji coba berbasis langganan akan memungkinkan Anda menyebarkan lingkungan CDS selama 30 hari.</span><span class="sxs-lookup"><span data-stu-id="554d0-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Pengaturan penyebaran](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="554d0-125">Pilih **setuju** untuk menyetujui persyaratan layanan, lalu pilih **selesai** untuk kembali ke pengaturan penyebaran.</span><span class="sxs-lookup"><span data-stu-id="554d0-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Persetujuan Penyebaran](./media/2DeploymentConsent.png)

7. <span data-ttu-id="554d0-127">Opsional - Terapkan data demo ke lingkungan.</span><span class="sxs-lookup"><span data-stu-id="554d0-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="554d0-128">Buka **Pengaturan tingkat lanjut**, pilih **Sesuaikan Konfigurasi Database SQL**, dan atur **Tentukan kumpulan data untuk Aplikasi database** ke **Demo**.</span><span class="sxs-lookup"><span data-stu-id="554d0-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="554d0-129">Lengkapi bidang yang diperlukan yang tersisa di Wizard dan konfirmasikan penyebaran.</span><span class="sxs-lookup"><span data-stu-id="554d0-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="554d0-130">Waktu untuk menyediakan lingkungan bervariasi berdasarkan jenis lingkungan.</span><span class="sxs-lookup"><span data-stu-id="554d0-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="554d0-131">Penyediaan mungkin memerlukan waktu hingga enam jam.</span><span class="sxs-lookup"><span data-stu-id="554d0-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="554d0-132">Setelah penyebaran berhasil diselesaikan, lingkungan akan ditampilkan sebagai **disebarkan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="554d0-133">Untuk mengkonfirmasikan bahwa lingkungan telah berhasil disebarkan, pilih **Masuk** dan masuk ke lingkungan untuk mengkonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="554d0-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Rincian lingkungan ](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="554d0-135">Terapkan pembaruan ke lingkungan Finance</span><span class="sxs-lookup"><span data-stu-id="554d0-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="554d0-136">Project Operations memerlukan lingkungan Finance dengan versi aplikasi **10.0.13 (10.0.569.20009)** atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="554d0-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="554d0-137">Anda mungkin perlu menerapkan pembaruan kualitas ke lingkungan Finance Anda untuk menerima versi ini.</span><span class="sxs-lookup"><span data-stu-id="554d0-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="554d0-138">Di LCS, di halaman **rincian lingkungan**, di Bagian **pembaruan yang tersedia**, pilih **Lihat pembaruan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Lihat pembaruan](./media/5ViewUpdates.png)

2. <span data-ttu-id="554d0-140">Pada halaman **pembaruan biner**, pilih **Simpan paket.**</span><span class="sxs-lookup"><span data-stu-id="554d0-140">On the **Binary updates** page, select **Save package.**</span></span>

![Simpan paket](./media/6SavePackage.png)

3. <span data-ttu-id="554d0-142">Klik **pilih semua**, lalu pilih **Simpan paket**.</span><span class="sxs-lookup"><span data-stu-id="554d0-142">Click **Select all** and then select **Save package**.</span></span>

![Tinjau dan simpan pembaruan](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="554d0-144">Masukkan nama dan Deskripsi paket, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="554d0-145">Tergantung pada koneksi internet, proses ini mungkin akan memakan waktu.</span><span class="sxs-lookup"><span data-stu-id="554d0-145">Depending on the internet connection, this process might take some time.</span></span>

![Mengunggah paket ke pustaka aset](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="554d0-147">Setelah paket disimpan, pilih **selesai** dan Simpan paket ini ke pustaka aset dalam proyek LCS Anda.</span><span class="sxs-lookup"><span data-stu-id="554d0-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="554d0-148">Menyimpan dan memvalidasi paket mungkin memerlukan waktu ~ 15 menit.</span><span class="sxs-lookup"><span data-stu-id="554d0-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="554d0-149">Untuk menerapkan pembaruan, navigasi ke halaman **rincian lingkungan** di lcs dan pilih **memelihara** > **menerapkan pembaruan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Memelihara lingkungan](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="554d0-151">Dalam daftar pembaruan, pilih paket yang Anda buat, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Menerapkan pembaruan](./media/10ApplyUpdates.png)

<span data-ttu-id="554d0-153">Layanan lingkungan akan memakan waktu.</span><span class="sxs-lookup"><span data-stu-id="554d0-153">Environment servicing will take some time.</span></span> <span data-ttu-id="554d0-154">Setelah selesai, lingkungan akan kembali ke keadaan disebarkan.</span><span class="sxs-lookup"><span data-stu-id="554d0-154">After it is complete, the environment will return to a deployed state.</span></span>

![Lingkungan Disebarkan](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="554d0-156">Membuat sambungan tulis ganda</span><span class="sxs-lookup"><span data-stu-id="554d0-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="554d0-157">Di proyek LCS, buka halaman **rincian lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="554d0-158">Di dalam **informasi lingkungan Common Data Service**, pilih **tautkan ke CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="554d0-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="554d0-159">Setelah tautan selesai, pilih **tautkan ke CDS for Apps** lagi.</span><span class="sxs-lookup"><span data-stu-id="554d0-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="554d0-160">Anda akan diarahkan ke Tulis Ganda di Finance.</span><span class="sxs-lookup"><span data-stu-id="554d0-160">You will be redirected to Dual Write in Finance.</span></span>

![Tautan ke CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="554d0-162">Pilih **Terapkan solusi** untuk mengakses entitas yang akan dipetakan dalam integrasi.</span><span class="sxs-lookup"><span data-stu-id="554d0-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Terapkan solusi](./media/13ApplySolutions.png)

5. <span data-ttu-id="554d0-164">Pilih kedua solusi, Peta Entitas Penulisan Ganda **Dynamics 365 Finance and Operations** dan Peta Entitas Penulisan Ganda **Dynamics 365 Project Operations**, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Konfirmasi Solusi](./media/14ConfirmSolutions.png)

<span data-ttu-id="554d0-166">Setelah solusi diterapkan, entitas tulis ganda diterapkan ke lingkungan.</span><span class="sxs-lookup"><span data-stu-id="554d0-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Menerapkan solusi](./media/15ApplyingSolutions.png)

<span data-ttu-id="554d0-168">Setelah entitas diterapkan, Semua pemetaan yang tersedia didaftarkan di lingkungan.</span><span class="sxs-lookup"><span data-stu-id="554d0-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Peta Tulis Ganda](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="554d0-170">Segarkan entitas data setelah pembaruan</span><span class="sxs-lookup"><span data-stu-id="554d0-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="554d0-171">Di Finance, buka ruang kerja **manajemen data**.</span><span class="sxs-lookup"><span data-stu-id="554d0-171">In Finance, go to the **Data management** workspace.</span></span>

![Ruang kerja manajemen data](./media/16DataManagement.png)

2. <span data-ttu-id="554d0-173">Pilih ubin **parameter kerangka**.</span><span class="sxs-lookup"><span data-stu-id="554d0-173">Select the **Framework parameters** tile.</span></span>

![Parameter kerangka](./media/17FrameworkParameters.png)

3. <span data-ttu-id="554d0-175">Pada halaman **pengaturan entitas**, pilih **segarkan daftar entitas**.</span><span class="sxs-lookup"><span data-stu-id="554d0-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Segarkan daftar entitas](./media/18RefreshEntityList.png)

<span data-ttu-id="554d0-177">Penyegaran akan berlangsung sekitar 20 menit.</span><span class="sxs-lookup"><span data-stu-id="554d0-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="554d0-178">Anda akan menerima pemberitahuan setelah selesai.</span><span class="sxs-lookup"><span data-stu-id="554d0-178">You will receive an alert when it is complete.</span></span>

![Segarkan Konfirmasi](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="554d0-180">Memperbarui pengaturan keamanan di Project Operations di Dataverse</span><span class="sxs-lookup"><span data-stu-id="554d0-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="554d0-181">Buka Project Operations di lingkungan Dataverse.</span><span class="sxs-lookup"><span data-stu-id="554d0-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="554d0-182">Buka **Pengaturan** > **Keamanan** > **Peran Keamanan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="554d0-183">Pada halaman **Peran keamanan**, dalam daftar peran, pilih **pengguna aplikasi penulisan ganda** dan pilih tab **Entitas Kustom**.</span><span class="sxs-lookup"><span data-stu-id="554d0-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="554d0-184">Pastikan peran memiliki izin **Baca** dan **Lampirkan ke** untuk:</span><span class="sxs-lookup"><span data-stu-id="554d0-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="554d0-185">**Jenis Nilai Tukar Mata Uang**</span><span class="sxs-lookup"><span data-stu-id="554d0-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="554d0-186">**Bagan Akun**</span><span class="sxs-lookup"><span data-stu-id="554d0-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="554d0-187">**Kalender Fiskal**</span><span class="sxs-lookup"><span data-stu-id="554d0-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="554d0-188">**Buku besar**</span><span class="sxs-lookup"><span data-stu-id="554d0-188">**Ledger**</span></span>

5. <span data-ttu-id="554d0-189">Setelah peran keamanan diperbarui, buka **Pengaturan** > **Keamanan** > **Tim**, dan pilih tim default dalam tampilan tim **Pemilik Bisnis Lokal**.</span><span class="sxs-lookup"><span data-stu-id="554d0-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="554d0-190">Pilih **Kelola Peran** dan verifikasikan bahwa hak istimewa keamanan **pengguna aplikasi penulisan ganda** diterapkan ke tim ini.</span><span class="sxs-lookup"><span data-stu-id="554d0-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="554d0-191">Jalankan peta Tulis Ganda Project Operations</span><span class="sxs-lookup"><span data-stu-id="554d0-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="554d0-192">Di proyek LCS, buka halaman **rincian lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="554d0-193">Di dalam **informasi lingkungan Common Data Service**, pilih **tautkan ke CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="554d0-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="554d0-194">Setelah memilih tautan, Anda akan diarahkan ke daftar entitas di pemetaan.</span><span class="sxs-lookup"><span data-stu-id="554d0-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="554d0-195">Mulai peta seperti yang dijelaskan dalam tabel berikut.</span><span class="sxs-lookup"><span data-stu-id="554d0-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="554d0-196">Pastikan untuk mengikuti urutan yang tercantum.</span><span class="sxs-lookup"><span data-stu-id="554d0-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="554d0-197">**Peta Entitas**</span><span class="sxs-lookup"><span data-stu-id="554d0-197">**Entity Map**</span></span> | <span data-ttu-id="554d0-198">**Refresh Entitas**</span><span class="sxs-lookup"><span data-stu-id="554d0-198">**Refresh entity**</span></span> | <span data-ttu-id="554d0-199">**Sinkronisasi awal**</span><span class="sxs-lookup"><span data-stu-id="554d0-199">**Initial sync**</span></span> | <span data-ttu-id="554d0-200">**Master untuk sinkronisasi awal**</span><span class="sxs-lookup"><span data-stu-id="554d0-200">**Master for initial sync**</span></span> | <span data-ttu-id="554d0-201">**Prasyarat menjalankan**</span><span class="sxs-lookup"><span data-stu-id="554d0-201">**Run prerequisites**</span></span> | <span data-ttu-id="554d0-202">**Sinkronisasi awal prasyarat**</span><span class="sxs-lookup"><span data-stu-id="554d0-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="554d0-203">**Peran sumber daya proyek untuk semua perusahaan (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="554d0-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="554d0-204">No</span><span class="sxs-lookup"><span data-stu-id="554d0-204">No</span></span> | <span data-ttu-id="554d0-205">Ya</span><span class="sxs-lookup"><span data-stu-id="554d0-205">Yes</span></span> | <span data-ttu-id="554d0-206">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="554d0-206">Common Data Service</span></span> | <span data-ttu-id="554d0-207">No</span><span class="sxs-lookup"><span data-stu-id="554d0-207">No</span></span> | <span data-ttu-id="554d0-208">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-208">N\A</span></span> |
| <span data-ttu-id="554d0-209">**Entitas hukum (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="554d0-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="554d0-210">No</span><span class="sxs-lookup"><span data-stu-id="554d0-210">No</span></span> | <span data-ttu-id="554d0-211">Ya</span><span class="sxs-lookup"><span data-stu-id="554d0-211">Yes</span></span> | <span data-ttu-id="554d0-212">Aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="554d0-212">Finance and Operations apps</span></span> | <span data-ttu-id="554d0-213">No</span><span class="sxs-lookup"><span data-stu-id="554d0-213">No</span></span> | <span data-ttu-id="554d0-214">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-214">N\A</span></span> |
| <span data-ttu-id="554d0-215">**Buku Besar (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="554d0-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="554d0-216">No</span><span class="sxs-lookup"><span data-stu-id="554d0-216">No</span></span> | <span data-ttu-id="554d0-217">Ya</span><span class="sxs-lookup"><span data-stu-id="554d0-217">Yes</span></span> | <span data-ttu-id="554d0-218">Aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="554d0-218">Finance and Operations apps</span></span> | <span data-ttu-id="554d0-219">Ya</span><span class="sxs-lookup"><span data-stu-id="554d0-219">Yes</span></span> | <span data-ttu-id="554d0-220">Ya, aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="554d0-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="554d0-221">**Aktual Integrasi Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="554d0-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="554d0-222">No</span><span class="sxs-lookup"><span data-stu-id="554d0-222">No</span></span> | <span data-ttu-id="554d0-223">No</span><span class="sxs-lookup"><span data-stu-id="554d0-223">No</span></span> | <span data-ttu-id="554d0-224">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-224">N\A</span></span> | <span data-ttu-id="554d0-225">Ya</span><span class="sxs-lookup"><span data-stu-id="554d0-225">Yes</span></span> | <span data-ttu-id="554d0-226">No</span><span class="sxs-lookup"><span data-stu-id="554d0-226">No</span></span> |
| <span data-ttu-id="554d0-227">**Baris kontrak proyek (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="554d0-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="554d0-228">No</span><span class="sxs-lookup"><span data-stu-id="554d0-228">No</span></span> | <span data-ttu-id="554d0-229">No</span><span class="sxs-lookup"><span data-stu-id="554d0-229">No</span></span> | <span data-ttu-id="554d0-230">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-230">N\A</span></span> | <span data-ttu-id="554d0-231">No</span><span class="sxs-lookup"><span data-stu-id="554d0-231">No</span></span> | <span data-ttu-id="554d0-232">No</span><span class="sxs-lookup"><span data-stu-id="554d0-232">No</span></span> |
| <span data-ttu-id="554d0-233">**Entitas integrasi untuk Relasi transaksi proyek (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="554d0-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="554d0-234">No</span><span class="sxs-lookup"><span data-stu-id="554d0-234">No</span></span> | <span data-ttu-id="554d0-235">No</span><span class="sxs-lookup"><span data-stu-id="554d0-235">No</span></span> | <span data-ttu-id="554d0-236">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-236">N\A</span></span> | <span data-ttu-id="554d0-237">No</span><span class="sxs-lookup"><span data-stu-id="554d0-237">No</span></span> | <span data-ttu-id="554d0-238">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-238">N\A</span></span> |
| <span data-ttu-id="554d0-239">**Baris kontrak integrasi Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="554d0-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="554d0-240">No</span><span class="sxs-lookup"><span data-stu-id="554d0-240">No</span></span> | <span data-ttu-id="554d0-241">No</span><span class="sxs-lookup"><span data-stu-id="554d0-241">No</span></span> | <span data-ttu-id="554d0-242">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-242">N\A</span></span> | <span data-ttu-id="554d0-243">No</span><span class="sxs-lookup"><span data-stu-id="554d0-243">No</span></span> | <span data-ttu-id="554d0-244">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-244">N\A</span></span> |
| <span data-ttu-id="554d0-245">**Entitas integrasi Project Operations untuk estimasi pengeluaran (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="554d0-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="554d0-246">No</span><span class="sxs-lookup"><span data-stu-id="554d0-246">No</span></span> | <span data-ttu-id="554d0-247">No</span><span class="sxs-lookup"><span data-stu-id="554d0-247">No</span></span> | <span data-ttu-id="554d0-248">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-248">N\A</span></span> | <span data-ttu-id="554d0-249">No</span><span class="sxs-lookup"><span data-stu-id="554d0-249">No</span></span> | <span data-ttu-id="554d0-250">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-250">N\A</span></span> |
| <span data-ttu-id="554d0-251">**Entitas ekspor kategori pengeluaran proyek integrasi Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="554d0-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="554d0-252">No</span><span class="sxs-lookup"><span data-stu-id="554d0-252">No</span></span> | <span data-ttu-id="554d0-253">No</span><span class="sxs-lookup"><span data-stu-id="554d0-253">No</span></span> | <span data-ttu-id="554d0-254">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-254">N\A</span></span> | <span data-ttu-id="554d0-255">No</span><span class="sxs-lookup"><span data-stu-id="554d0-255">No</span></span> | <span data-ttu-id="554d0-256">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-256">N\A</span></span> |
| <span data-ttu-id="554d0-257">**Entitas ekspor pengeluaran proyek integrasi Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="554d0-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="554d0-258">Ya</span><span class="sxs-lookup"><span data-stu-id="554d0-258">Yes</span></span> | <span data-ttu-id="554d0-259">No</span><span class="sxs-lookup"><span data-stu-id="554d0-259">No</span></span> | <span data-ttu-id="554d0-260">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-260">N\A</span></span> | <span data-ttu-id="554d0-261">No</span><span class="sxs-lookup"><span data-stu-id="554d0-261">No</span></span> | <span data-ttu-id="554d0-262">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-262">N\A</span></span> |
| <span data-ttu-id="554d0-263">**Entitas integrasi Project Operations untuk estimasi jam (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="554d0-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="554d0-264">Ya</span><span class="sxs-lookup"><span data-stu-id="554d0-264">Yes</span></span> | <span data-ttu-id="554d0-265">No</span><span class="sxs-lookup"><span data-stu-id="554d0-265">No</span></span> | <span data-ttu-id="554d0-266">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-266">N\A</span></span> | <span data-ttu-id="554d0-267">No</span><span class="sxs-lookup"><span data-stu-id="554d0-267">No</span></span> | <span data-ttu-id="554d0-268">N\A</span><span class="sxs-lookup"><span data-stu-id="554d0-268">N\A</span></span> |


4. <span data-ttu-id="554d0-269">Untuk me-refresh entitas, pilih nama peta, lalu pilih **refresh entitas**.</span><span class="sxs-lookup"><span data-stu-id="554d0-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Segarkan Peta](./media/20RefreshMapping.png)

5. <span data-ttu-id="554d0-271">Jalankan peta setelah penyegaran selesai.</span><span class="sxs-lookup"><span data-stu-id="554d0-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="554d0-272">Sebelum Anda mengaktifkan peta berikutnya, Verifikasikan bahwa peta dalam tabel dalam status **berjalan**.</span><span class="sxs-lookup"><span data-stu-id="554d0-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="554d0-273">Menjalankan peta dengan sejumlah besar prasyarat mungkin akan memakan waktu.</span><span class="sxs-lookup"><span data-stu-id="554d0-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="554d0-274">Untuk menjalankan peta dengan prasyarat, Aktifkan pengalih **Tampilkan peta entitas yang terkait**.</span><span class="sxs-lookup"><span data-stu-id="554d0-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="554d0-275">Jika tabel menunjukkan **sinkronisasi awal prasyarat** adalah **Tidak**, Verifikasikan bahwa tanda **sinkronisasi awal** **dinonaktifkan** di semua peta prasyarat sebelum Anda menjalankannya.</span><span class="sxs-lookup"><span data-stu-id="554d0-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Jalankan Peta](./media/21RunMap.png)

6. <span data-ttu-id="554d0-277">Validasi semua peta terkait proyek berada dalam status berjalan.</span><span class="sxs-lookup"><span data-stu-id="554d0-277">Validate all project related maps are in the running state.</span></span>

![Semua peta berjalan](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="554d0-279">Menerapkan data konfigurasi di Project Operations untuk Project Operations (opsional)</span><span class="sxs-lookup"><span data-stu-id="554d0-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="554d0-280">Jika Anda telah menerapkan data demo ke lingkungan Finance, lihat [Menyiapkan dan menerapkan data konfigurasi di Common Data Service untuk Project Operations](resource-apply-pro-setup-config-data.md) untuk menerapkan data demo ke lingkungan CDS.</span><span class="sxs-lookup"><span data-stu-id="554d0-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="554d0-281">Lingkungan Project Operations Anda sekarang telah disediakan dan dikonfigurasi.</span><span class="sxs-lookup"><span data-stu-id="554d0-281">Your Project Operations environment is now provisioned and configured.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
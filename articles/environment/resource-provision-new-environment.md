---
title: Penyediaan lingkungan baru
description: Topik ini menyediakan informasi tentang bagaimana menyediakan lingkungan Project Operations baru.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9ed502a1312b702e029d8910d62f72b8e0e4df06
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642979"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="11097-103">Penyediaan lingkungan baru</span><span class="sxs-lookup"><span data-stu-id="11097-103">Provision a new environment</span></span>

<span data-ttu-id="11097-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="11097-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="11097-105">Topik ini menyediakan informasi tentang cara menyediakan lingkungan Dynamics 365 Project Operations untuk skenario berbasis sumber daya/non-stok.</span><span class="sxs-lookup"><span data-stu-id="11097-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="11097-106">Aktifkan penetapan otomatis Project Operations dalam proyek LCS</span><span class="sxs-lookup"><span data-stu-id="11097-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="11097-107">Gunakan langkah-langkah berikut untuk mengaktifkan alur penyediaan otomatis Project Operations untuk proyek LCS Anda.</span><span class="sxs-lookup"><span data-stu-id="11097-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="11097-108">Buka [LCS](https://lcs.dynamics.com/v2), lalu pilih ubin **manajemen fitur pratinjau**.</span><span class="sxs-lookup"><span data-stu-id="11097-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="11097-109">Dalam Daftar **fitur pratinjau**, pilih **Fitur Project Operations**, kemudian pilih **fitur pratinjau yang diaktifkan** untuk mengaktifkan Project Operations.</span><span class="sxs-lookup"><span data-stu-id="11097-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="11097-110">Langkah ini dilakukan hanya satu kali per proyek LCS.</span><span class="sxs-lookup"><span data-stu-id="11097-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="11097-111">Penyediaan lingkungan Project Operations</span><span class="sxs-lookup"><span data-stu-id="11097-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="11097-112">Buka Dynamics 365 Finance [lingkungan demo](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) baru atau penyebaran [lingkungan produksi/Sandbox](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="11097-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="11097-113">Lalui Wizard **penyediaan lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="11097-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="11097-114">Pastikan versi aplikasi yang dipilih adalah 10.0.13 atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="11097-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="11097-115">Untuk menyediakan Project Operations, di dalam **pengaturan lanjutan**, pilih **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="11097-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="11097-116">Aktifkan **pengaturan Common Data Service** dengan memilih **ya**, lalu masukkan informasi di bidang wajib:</span><span class="sxs-lookup"><span data-stu-id="11097-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="11097-117">Nama</span><span class="sxs-lookup"><span data-stu-id="11097-117">Name</span></span>
  - <span data-ttu-id="11097-118">Wilayah</span><span class="sxs-lookup"><span data-stu-id="11097-118">Region</span></span>
  - <span data-ttu-id="11097-119">Bahasa</span><span class="sxs-lookup"><span data-stu-id="11097-119">Language</span></span>
  - <span data-ttu-id="11097-120">Mata uang</span><span class="sxs-lookup"><span data-stu-id="11097-120">Currency</span></span>
 
5. <span data-ttu-id="11097-121">Di bidang **template Common Data Service**, pilih **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="11097-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="11097-122">Pilih jenis lingkungan untuk penyebaran Anda.</span><span class="sxs-lookup"><span data-stu-id="11097-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="11097-123">Uji coba berbasis langganan akan memungkinkan Anda menyebarkan lingkungan CDS selama 30 hari.</span><span class="sxs-lookup"><span data-stu-id="11097-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Pengaturan penyebaran](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="11097-125">Pilih **setuju** untuk menyetujui persyaratan layanan, lalu pilih **selesai** untuk kembali ke pengaturan penyebaran.</span><span class="sxs-lookup"><span data-stu-id="11097-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Persetujuan Penyebaran](./media/2DeploymentConsent.png)

7. <span data-ttu-id="11097-127">Lengkapi bidang yang diperlukan yang tersisa di Wizard dan konfirmasikan penyebaran.</span><span class="sxs-lookup"><span data-stu-id="11097-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="11097-128">Waktu penyediaan lingkungan bervariasi berdasarkan jenis lingkungan.</span><span class="sxs-lookup"><span data-stu-id="11097-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="11097-129">Penyediaan mungkin memerlukan waktu hingga enam jam.</span><span class="sxs-lookup"><span data-stu-id="11097-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="11097-130">Setelah penyebaran berhasil diselesaikan, lingkungan akan ditampilkan sebagai **disebarkan**.</span><span class="sxs-lookup"><span data-stu-id="11097-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="11097-131">Untuk mengonfirmasi bahwa lingkungan telah berhasil disebarkan, pilih **masuk** dan masuk ke lingkungan untuk mengonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="11097-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Rincian lingkungan ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="11097-133">Terapkan data demo Project Operations Finance (langkah opsional)</span><span class="sxs-lookup"><span data-stu-id="11097-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="11097-134">Terapkan data demo Project Operations Finance ke lingkungan host cloud rilis Layanan 10.0.13 seperti dijelaskan dalam [artikel ini](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="11097-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="11097-135">Terapkan pembaruan ke lingkungan Finance</span><span class="sxs-lookup"><span data-stu-id="11097-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="11097-136">Project Operations memerlukan lingkungan Finance dengan versi aplikasi **10.0.13 (10.0.569.20009)** atau lebih tinggi.</span><span class="sxs-lookup"><span data-stu-id="11097-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="11097-137">Anda mungkin perlu menerapkan pembaruan kualitas ke lingkungan Finance Anda untuk menerima versi ini.</span><span class="sxs-lookup"><span data-stu-id="11097-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="11097-138">Di LCS, di halaman **rincian lingkungan**, di Bagian **pembaruan yang tersedia**, pilih **Lihat pembaruan**.</span><span class="sxs-lookup"><span data-stu-id="11097-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Lihat pembaruan](./media/5ViewUpdates.png)

2. <span data-ttu-id="11097-140">Pada halaman **pembaruan biner**, pilih **Simpan paket.**</span><span class="sxs-lookup"><span data-stu-id="11097-140">On the **Binary updates** page, select **Save package.**</span></span>

![Simpan paket](./media/6SavePackage.png)

3. <span data-ttu-id="11097-142">Klik **pilih semua**, lalu pilih **Simpan paket**.</span><span class="sxs-lookup"><span data-stu-id="11097-142">Click **Select all** and then select **Save package**.</span></span>

![Tinjau dan simpan pembaruan](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="11097-144">Masukkan nama dan Deskripsi paket, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="11097-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="11097-145">Tergantung pada koneksi internet, proses ini mungkin akan memakan waktu.</span><span class="sxs-lookup"><span data-stu-id="11097-145">Depending on the internet connection, this process might take some time.</span></span>

![Mengunggah paket ke pustaka aset](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="11097-147">Setelah paket disimpan, pilih **selesai** dan Simpan paket ini ke pustaka aset dalam proyek LCS Anda.</span><span class="sxs-lookup"><span data-stu-id="11097-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="11097-148">Menyimpan dan memvalidasi paket mungkin memerlukan waktu ~ 15 menit.</span><span class="sxs-lookup"><span data-stu-id="11097-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="11097-149">Untuk menerapkan pembaruan, navigasi ke halaman **rincian lingkungan** di lcs dan pilih **memelihara** > **menerapkan pembaruan**.</span><span class="sxs-lookup"><span data-stu-id="11097-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Memelihara lingkungan](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="11097-151">Dalam daftar pembaruan, pilih paket yang Anda buat, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="11097-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Menerapkan pembaruan](./media/10ApplyUpdates.png)

<span data-ttu-id="11097-153">Layanan lingkungan akan memakan waktu.</span><span class="sxs-lookup"><span data-stu-id="11097-153">Environment servicing will take some time.</span></span> <span data-ttu-id="11097-154">Setelah selesai, lingkungan akan kembali ke keadaan disebarkan.</span><span class="sxs-lookup"><span data-stu-id="11097-154">After it is complete, the environment will return to a deployed state.</span></span>

![Lingkungan Disebarkan](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="11097-156">Membuat sambungan tulis ganda</span><span class="sxs-lookup"><span data-stu-id="11097-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="11097-157">Di proyek LCS, buka halaman **rincian lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="11097-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="11097-158">Di dalam **informasi lingkungan Common Data Service**, pilih **tautkan ke CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="11097-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="11097-159">Setelah tautan selesai, pilih **tautkan ke CDS for Apps** lagi.</span><span class="sxs-lookup"><span data-stu-id="11097-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="11097-160">Anda akan diarahkan ke Tulis Ganda di Finance.</span><span class="sxs-lookup"><span data-stu-id="11097-160">You will be redirected to Dual Write in Finance.</span></span>

![Tautan ke CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="11097-162">Pilih **Terapkan solusi** untuk mengakses entitas yang akan dipetakan dalam integrasi.</span><span class="sxs-lookup"><span data-stu-id="11097-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Terapkan solusi](./media/13ApplySolutions.png)

5. <span data-ttu-id="11097-164">Pilih kedua solusi, Peta Entitas Penulisan Ganda **Dynamics 365 Finance and Operations** dan Peta Entitas Penulisan Ganda **Dynamics 365 Project Operations**, lalu pilih **Terapkan**.</span><span class="sxs-lookup"><span data-stu-id="11097-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Konfirmasi Solusi](./media/14ConfirmSolutions.png)

<span data-ttu-id="11097-166">Setelah solusi diterapkan, entitas tulis ganda diterapkan ke lingkungan.</span><span class="sxs-lookup"><span data-stu-id="11097-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Menerapkan solusi](./media/15ApplyingSolutions.png)

<span data-ttu-id="11097-168">Setelah entitas diterapkan, Semua pemetaan yang tersedia didaftarkan di lingkungan.</span><span class="sxs-lookup"><span data-stu-id="11097-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Peta Tulis Ganda](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="11097-170">Segarkan entitas data setelah pembaruan</span><span class="sxs-lookup"><span data-stu-id="11097-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="11097-171">Di Finance, buka ruang kerja **manajemen data**.</span><span class="sxs-lookup"><span data-stu-id="11097-171">In Finance, go to the **Data management** workspace.</span></span>

![Ruang kerja manajemen data](./media/16DataManagement.png)

2. <span data-ttu-id="11097-173">Pilih ubin **parameter kerangka**.</span><span class="sxs-lookup"><span data-stu-id="11097-173">Select the **Framework parameters** tile.</span></span>

![Parameter kerangka](./media/17FrameworkParameters.png)

3. <span data-ttu-id="11097-175">Pada halaman **pengaturan entitas**, pilih **segarkan daftar entitas**.</span><span class="sxs-lookup"><span data-stu-id="11097-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Segarkan daftar entitas](./media/18RefreshEntityList.png)

<span data-ttu-id="11097-177">Penyegaran akan berlangsung sekitar 20 menit.</span><span class="sxs-lookup"><span data-stu-id="11097-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="11097-178">Anda akan menerima pemberitahuan setelah selesai.</span><span class="sxs-lookup"><span data-stu-id="11097-178">You will receive an alert when it is complete.</span></span>

![Segarkan Konfirmasi](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="11097-180">Jalankan peta Tulis Ganda Project Operations</span><span class="sxs-lookup"><span data-stu-id="11097-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="11097-181">Di proyek LCS, buka halaman **rincian lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="11097-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="11097-182">Di dalam **informasi lingkungan Common Data Service**, pilih **tautkan ke CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="11097-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="11097-183">Setelah memilih tautan, Anda akan diarahkan ke daftar entitas di pemetaan.</span><span class="sxs-lookup"><span data-stu-id="11097-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="11097-184">Mulai peta seperti yang dijelaskan dalam tabel berikut.</span><span class="sxs-lookup"><span data-stu-id="11097-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="11097-185">Pastikan untuk mengikuti urutan yang tercantum.</span><span class="sxs-lookup"><span data-stu-id="11097-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="11097-186">**Peta Entitas**</span><span class="sxs-lookup"><span data-stu-id="11097-186">**Entity Map**</span></span> | <span data-ttu-id="11097-187">**Refresh Entitas**</span><span class="sxs-lookup"><span data-stu-id="11097-187">**Refresh entity**</span></span> | <span data-ttu-id="11097-188">**Sinkronisasi awal**</span><span class="sxs-lookup"><span data-stu-id="11097-188">**Initial sync**</span></span> | <span data-ttu-id="11097-189">**Master untuk sinkronisasi awal**</span><span class="sxs-lookup"><span data-stu-id="11097-189">**Master for initial sync**</span></span> | <span data-ttu-id="11097-190">**Prasyarat menjalankan**</span><span class="sxs-lookup"><span data-stu-id="11097-190">**Run prerequisites**</span></span> | <span data-ttu-id="11097-191">**Sinkronisasi awal prasyarat**</span><span class="sxs-lookup"><span data-stu-id="11097-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="11097-192">**Peran sumber daya proyek untuk semua perusahaan (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="11097-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="11097-193">No</span><span class="sxs-lookup"><span data-stu-id="11097-193">No</span></span> | <span data-ttu-id="11097-194">Ya</span><span class="sxs-lookup"><span data-stu-id="11097-194">Yes</span></span> | <span data-ttu-id="11097-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="11097-195">Common Data Service</span></span> | <span data-ttu-id="11097-196">No</span><span class="sxs-lookup"><span data-stu-id="11097-196">No</span></span> | <span data-ttu-id="11097-197">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-197">N\A</span></span> |
| <span data-ttu-id="11097-198">**Entitas hukum (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="11097-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="11097-199">No</span><span class="sxs-lookup"><span data-stu-id="11097-199">No</span></span> | <span data-ttu-id="11097-200">Ya</span><span class="sxs-lookup"><span data-stu-id="11097-200">Yes</span></span> | <span data-ttu-id="11097-201">Aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11097-201">Finance and Operations apps</span></span> | <span data-ttu-id="11097-202">No</span><span class="sxs-lookup"><span data-stu-id="11097-202">No</span></span> | <span data-ttu-id="11097-203">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-203">N\A</span></span> |
| <span data-ttu-id="11097-204">**Buku Besar (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="11097-204">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="11097-205">No</span><span class="sxs-lookup"><span data-stu-id="11097-205">No</span></span> | <span data-ttu-id="11097-206">Ya</span><span class="sxs-lookup"><span data-stu-id="11097-206">Yes</span></span> | <span data-ttu-id="11097-207">Aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11097-207">Finance and Operations apps</span></span> | <span data-ttu-id="11097-208">Ya</span><span class="sxs-lookup"><span data-stu-id="11097-208">Yes</span></span> | <span data-ttu-id="11097-209">Ya, aplikasi Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="11097-209">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="11097-210">**Aktual Integrasi Project Operations (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="11097-210">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="11097-211">No</span><span class="sxs-lookup"><span data-stu-id="11097-211">No</span></span> | <span data-ttu-id="11097-212">No</span><span class="sxs-lookup"><span data-stu-id="11097-212">No</span></span> | <span data-ttu-id="11097-213">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-213">N\A</span></span> | <span data-ttu-id="11097-214">Ya</span><span class="sxs-lookup"><span data-stu-id="11097-214">Yes</span></span> | <span data-ttu-id="11097-215">No</span><span class="sxs-lookup"><span data-stu-id="11097-215">No</span></span> |
| <span data-ttu-id="11097-216">**Baris kontrak proyek (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="11097-216">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="11097-217">No</span><span class="sxs-lookup"><span data-stu-id="11097-217">No</span></span> | <span data-ttu-id="11097-218">No</span><span class="sxs-lookup"><span data-stu-id="11097-218">No</span></span> | <span data-ttu-id="11097-219">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-219">N\A</span></span> | <span data-ttu-id="11097-220">No</span><span class="sxs-lookup"><span data-stu-id="11097-220">No</span></span> | <span data-ttu-id="11097-221">No</span><span class="sxs-lookup"><span data-stu-id="11097-221">No</span></span> |
| <span data-ttu-id="11097-222">**Entitas integrasi untuk Relasi transaksi proyek (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="11097-222">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="11097-223">No</span><span class="sxs-lookup"><span data-stu-id="11097-223">No</span></span> | <span data-ttu-id="11097-224">No</span><span class="sxs-lookup"><span data-stu-id="11097-224">No</span></span> | <span data-ttu-id="11097-225">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-225">N\A</span></span> | <span data-ttu-id="11097-226">No</span><span class="sxs-lookup"><span data-stu-id="11097-226">No</span></span> | <span data-ttu-id="11097-227">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-227">N\A</span></span> |
| <span data-ttu-id="11097-228">**Baris kontrak integrasi Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="11097-228">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="11097-229">No</span><span class="sxs-lookup"><span data-stu-id="11097-229">No</span></span> | <span data-ttu-id="11097-230">No</span><span class="sxs-lookup"><span data-stu-id="11097-230">No</span></span> | <span data-ttu-id="11097-231">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-231">N\A</span></span> | <span data-ttu-id="11097-232">No</span><span class="sxs-lookup"><span data-stu-id="11097-232">No</span></span> | <span data-ttu-id="11097-233">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-233">N\A</span></span> |
| <span data-ttu-id="11097-234">**Entitas integrasi Project Operations untuk estimasi pengeluaran (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="11097-234">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="11097-235">No</span><span class="sxs-lookup"><span data-stu-id="11097-235">No</span></span> | <span data-ttu-id="11097-236">No</span><span class="sxs-lookup"><span data-stu-id="11097-236">No</span></span> | <span data-ttu-id="11097-237">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-237">N\A</span></span> | <span data-ttu-id="11097-238">No</span><span class="sxs-lookup"><span data-stu-id="11097-238">No</span></span> | <span data-ttu-id="11097-239">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-239">N\A</span></span> |
| <span data-ttu-id="11097-240">**Entitas ekspor kategori pengeluaran proyek integrasi Project Operations (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="11097-240">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="11097-241">No</span><span class="sxs-lookup"><span data-stu-id="11097-241">No</span></span> | <span data-ttu-id="11097-242">No</span><span class="sxs-lookup"><span data-stu-id="11097-242">No</span></span> | <span data-ttu-id="11097-243">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-243">N\A</span></span> | <span data-ttu-id="11097-244">No</span><span class="sxs-lookup"><span data-stu-id="11097-244">No</span></span> | <span data-ttu-id="11097-245">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-245">N\A</span></span> |
| <span data-ttu-id="11097-246">**Entitas ekspor pengeluaran proyek integrasi Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="11097-246">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="11097-247">Ya</span><span class="sxs-lookup"><span data-stu-id="11097-247">Yes</span></span> | <span data-ttu-id="11097-248">No</span><span class="sxs-lookup"><span data-stu-id="11097-248">No</span></span> | <span data-ttu-id="11097-249">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-249">N\A</span></span> | <span data-ttu-id="11097-250">No</span><span class="sxs-lookup"><span data-stu-id="11097-250">No</span></span> | <span data-ttu-id="11097-251">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-251">N\A</span></span> |
| <span data-ttu-id="11097-252">**Entitas integrasi Project Operations untuk estimasi jam (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="11097-252">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="11097-253">Ya</span><span class="sxs-lookup"><span data-stu-id="11097-253">Yes</span></span> | <span data-ttu-id="11097-254">No</span><span class="sxs-lookup"><span data-stu-id="11097-254">No</span></span> | <span data-ttu-id="11097-255">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-255">N\A</span></span> | <span data-ttu-id="11097-256">No</span><span class="sxs-lookup"><span data-stu-id="11097-256">No</span></span> | <span data-ttu-id="11097-257">N\A</span><span class="sxs-lookup"><span data-stu-id="11097-257">N\A</span></span> |


4. <span data-ttu-id="11097-258">Untuk me-refresh entitas, pilih nama peta, lalu pilih **refresh entitas**.</span><span class="sxs-lookup"><span data-stu-id="11097-258">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Segarkan Peta](./media/20RefreshMapping.png)

5. <span data-ttu-id="11097-260">Jalankan peta setelah penyegaran selesai.</span><span class="sxs-lookup"><span data-stu-id="11097-260">After the refresh is complete, run the map.</span></span> <span data-ttu-id="11097-261">Sebelum Anda mengaktifkan peta berikutnya, Verifikasikan bahwa peta dalam tabel dalam status **berjalan**.</span><span class="sxs-lookup"><span data-stu-id="11097-261">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="11097-262">Menjalankan peta dengan sejumlah besar prasyarat mungkin akan memakan waktu.</span><span class="sxs-lookup"><span data-stu-id="11097-262">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="11097-263">Untuk menjalankan peta dengan prasyarat, Aktifkan pengalih **Tampilkan peta entitas yang terkait**.</span><span class="sxs-lookup"><span data-stu-id="11097-263">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="11097-264">Jika tabel menunjukkan **sinkronisasi awal prasyarat** adalah **Tidak**, Verifikasikan bahwa tanda **sinkronisasi awal** **dinonaktifkan** di semua peta prasyarat sebelum Anda menjalankannya.</span><span class="sxs-lookup"><span data-stu-id="11097-264">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Jalankan Peta](./media/21RunMap.png)

6. <span data-ttu-id="11097-266">Validasi semua peta terkait proyek berada dalam status berjalan.</span><span class="sxs-lookup"><span data-stu-id="11097-266">Validate all project related maps are in the running state.</span></span>

![Semua peta berjalan](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="11097-268">Menerapkan data konfigurasi di Project Operations untuk Project Operations (opsional)</span><span class="sxs-lookup"><span data-stu-id="11097-268">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="11097-269">Jika Anda telah menerapkan data demo ke lingkungan Finance, lihat [Menyiapkan dan menerapkan data konfigurasi di Common Data Service untuk Project Operations](resource-apply-pro-setup-config-data.md) untuk menerapkan data demo ke lingkungan CDS.</span><span class="sxs-lookup"><span data-stu-id="11097-269">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="11097-270">Lingkungan Project Operations Anda sekarang telah disediakan dan dikonfigurasi.</span><span class="sxs-lookup"><span data-stu-id="11097-270">Your Project Operations environment is now provisioned and configured.</span></span> 

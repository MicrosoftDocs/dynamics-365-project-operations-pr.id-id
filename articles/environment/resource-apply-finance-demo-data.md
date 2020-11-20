---
title: Menerapkan data demo ke lingkungan di-host Finance cloud
description: Topik ini menjelaskan cara menerapkan data demo dari Project Operations ke lingkungan dihost Cloud Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a7cdbd2847ce45972aadd0d1a2d4f26270727ad9
ms.sourcegitcommit: d33ef0ae39f90fe3b0f6b4524f483e8052057361
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/03/2020
ms.locfileid: "4365242"
---
# <a name="apply-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="249d0-103">Menerapkan data demo ke lingkungan di-host Finance cloud</span><span class="sxs-lookup"><span data-stu-id="249d0-103">Apply demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="249d0-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="249d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="249d0-105">Topik ini hanya berlaku hanya Microsoft Dynamics 365 Finance versi 10.0.13 dan hanya dapat dilakukan di lingkungan yang di-host dengan Cloud.</span><span class="sxs-lookup"><span data-stu-id="249d0-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="249d0-106">Selesaikan langkah-langkah di topik ini **sebelum** anda menerapkan pembaruan kualitas ke lingkungan.</span><span class="sxs-lookup"><span data-stu-id="249d0-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="249d0-107">Di proyek LCS, buka halaman **rincian lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="249d0-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="249d0-108">Perhatikan bahwa ini mencakup rincian yang diperlukan untuk menyambung ke lingkungan dengan menggunakan Remote Desktop Protocol (RDP).</span><span class="sxs-lookup"><span data-stu-id="249d0-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Rincian lingkungan ](./media/1EnvironmentDetails.png)

<span data-ttu-id="249d0-110">Set pertama kredensial yang disorot adalah kredensial akun lokal dan berisi hyperlink ke sambungan desktop jarak jauh.</span><span class="sxs-lookup"><span data-stu-id="249d0-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="249d0-111">Kredensial mencakup nama pengguna dan sandi admin lingkungan.</span><span class="sxs-lookup"><span data-stu-id="249d0-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="249d0-112">Rangkaian kredensial kedua digunakan untuk masuk ke SQL Server di lingkungan ini.</span><span class="sxs-lookup"><span data-stu-id="249d0-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="249d0-113">Sambungkan ke lingkungan dengan hyperlink di **akun lokal**, dan gunakan **kredensial akun lokal** untuk mengautentikasi.</span><span class="sxs-lookup"><span data-stu-id="249d0-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="249d0-114">Buka **layanan informasi Internet** > **kumpulan aplikasi** > **AOSService** dan Hentikan layanan.</span><span class="sxs-lookup"><span data-stu-id="249d0-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="249d0-115">Anda menghentikan layanan pada titik ini sehingga Anda dapat melanjutkan untuk mengganti database SQL.</span><span class="sxs-lookup"><span data-stu-id="249d0-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Hentikan AOS](./media/2StopAOS.png)

4. <span data-ttu-id="249d0-117">Buka **Layanan** dan Hentikan dua item berikut:</span><span class="sxs-lookup"><span data-stu-id="249d0-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="249d0-118">Microsoft Dynamics 365 Unified Operations: Layanan Manajemen batch</span><span class="sxs-lookup"><span data-stu-id="249d0-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="249d0-119">Microsoft Dynamics 365 Unified Operations: kerangka impor ekspor data</span><span class="sxs-lookup"><span data-stu-id="249d0-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Hentikan Layanan](./media/3StopServices.png)

5. <span data-ttu-id="249d0-121">Buka Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="249d0-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="249d0-122">Masuk dengan kredensial SQL Server dan gunakan pengguna dan sandi axdbadmin dari halaman **rincian lingkungan** LCS.</span><span class="sxs-lookup"><span data-stu-id="249d0-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="249d0-124">Di object Explorer, **database** dan Cari **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="249d0-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="249d0-125">Anda akan mengganti database dengan database baru yang terletak di [pusat Unduh](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="249d0-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="249d0-126">Salin file zip ke VM yang mana Anda terhubung dari jarak jauh dan ekstrak konten zip.</span><span class="sxs-lookup"><span data-stu-id="249d0-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="249d0-127">Di SQL Server Management Studio, klik kanan **axdb**, dan kemudian pilih **tugas** > **Pulihkan** > **database**.</span><span class="sxs-lookup"><span data-stu-id="249d0-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Mengembalikan database](./media/5RestoreDatabase.png)

9. <span data-ttu-id="249d0-129">Pilih **perangkat sumber** dan navigasikan ke file yang diekstrak dari zip yang disalin.</span><span class="sxs-lookup"><span data-stu-id="249d0-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Perangkat sumber](./media/6SourceDevice.png)

10. <span data-ttu-id="249d0-131">Pilih **pilihan**, lalu pilih **Timpa database yang ada** dan **tutup koneksi yang ada ke database tujuan**.</span><span class="sxs-lookup"><span data-stu-id="249d0-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="249d0-132">Pilih **OK**.</span><span class="sxs-lookup"><span data-stu-id="249d0-132">Select **OK**.</span></span>

![Pulihkan Pengaturan](./media/7RestoreSetting.png)

<span data-ttu-id="249d0-134">Anda akan menerima konfirmasi bahwa pemulihan AXDB berhasil.</span><span class="sxs-lookup"><span data-stu-id="249d0-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="249d0-135">Setelah menerima konfirmasi ini, Anda dapat menutup SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="249d0-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="249d0-136">Kembali ke **layanan informasi Internet** > **kumpulan aplikasi** > **AOSService** dan mulai AOSService.</span><span class="sxs-lookup"><span data-stu-id="249d0-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="249d0-137">Buka **Layanan** dan mulai dua layanan yang Anda Hentikan sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="249d0-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="249d0-138">Cari alat AdminUserProvisioning pada VM ini.</span><span class="sxs-lookup"><span data-stu-id="249d0-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="249d0-139">Lihat ke bawah, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="249d0-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="249d0-140">Jalankan file .ext menggunakan alamat pengguna di bidang **alamat email**.</span><span class="sxs-lookup"><span data-stu-id="249d0-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="249d0-141">Pilih **kirim**.</span><span class="sxs-lookup"><span data-stu-id="249d0-141">Select **Submit**.</span></span>

![Penyediaan Sandi Admin](./media/8AdminUserProvisioning.png)

<span data-ttu-id="249d0-143">Hal ini berlangsung selama beberapa menit.</span><span class="sxs-lookup"><span data-stu-id="249d0-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="249d0-144">Anda akan menerima pesan konfirmasi bahwa pengguna admin berhasil diperbarui.</span><span class="sxs-lookup"><span data-stu-id="249d0-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="249d0-145">Terakhir, Jalankan Command Prompt sebagai administrator dan lakukan iisreset</span><span class="sxs-lookup"><span data-stu-id="249d0-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Reset IIS](./media/9IISReset.png)

18. <span data-ttu-id="249d0-147">Tutup sesi desktop jarak jauh dan gunakan halaman **rincian lingkungan** LCS untuk masuk ke lingkungan untuk mengkonfirmasi sudah berfungsi seperti yang diharapkan.</span><span class="sxs-lookup"><span data-stu-id="249d0-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)

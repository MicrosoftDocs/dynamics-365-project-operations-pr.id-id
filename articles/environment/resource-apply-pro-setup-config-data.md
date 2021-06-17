---
title: Pengaturan dan penerapan data konfigurasi di Common Data Service
description: Topik ini menyediakan informasi tentang mengonfigurasikan dan menerapkan data konfigurasi di Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001295"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="e78e4-103">Pengaturan dan penerapan data konfigurasi di Common Data Service</span><span class="sxs-lookup"><span data-stu-id="e78e4-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="e78e4-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="e78e4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="e78e4-105">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="e78e4-105">Prerequisites</span></span>

<span data-ttu-id="e78e4-106">Sebelum Anda mulai mengkonfigurasi data dalam Common Data Service (CDS), prasyarat berikut harus dipenuhi:</span><span class="sxs-lookup"><span data-stu-id="e78e4-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="e78e4-107">Penyediaan lingkungan CDS dan lingkungan Dynamics 365 Finance untuk Project Operations.</span><span class="sxs-lookup"><span data-stu-id="e78e4-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="e78e4-108">Informasi entitas hukum dari Dynamics 365 Finance dibagi ke lingkungan CDS.</span><span class="sxs-lookup"><span data-stu-id="e78e4-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="e78e4-109">Ini berarti bahwa entitas **perusahaan** dalam CDS memiliki rekaman perusahaan berikut:</span><span class="sxs-lookup"><span data-stu-id="e78e4-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="e78e4-110">THPM</span><span class="sxs-lookup"><span data-stu-id="e78e4-110">THPM</span></span>
  - <span data-ttu-id="e78e4-111">USPM</span><span class="sxs-lookup"><span data-stu-id="e78e4-111">USPM</span></span>
  - <span data-ttu-id="e78e4-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="e78e4-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e78e4-113">Menginstal data pengaturan dan konfigurasi</span><span class="sxs-lookup"><span data-stu-id="e78e4-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="e78e4-114">Unduh, buka blokir, dan buka [Paket paket data pengaturan dan konfigurasi](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="e78e4-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="e78e4-115">Arahkan ke folder zip terbuka dan Jalankan file eksekusi, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e78e4-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e78e4-116">Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e78e4-118">Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e78e4-119">Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e78e4-120">Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Masuk untuk konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e78e4-122">Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e78e4-123">Pada halaman 4, pilih file zip, *SampleSetupAndConfigData* dari folder yang telah dibongkar.</span><span class="sxs-lookup"><span data-stu-id="e78e4-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Pilihan file zip](./media/3ZipFile.png)

![Pilih file](./media/4SelectAFile.png)

9. <span data-ttu-id="e78e4-126">Setelah file zip dipilih, pilih **impor data**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-126">After the zip file is selected, select **Import Data**.</span></span>

![Impor Data](./media/5ImportData.png)

10. <span data-ttu-id="e78e4-128">Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda.</span><span class="sxs-lookup"><span data-stu-id="e78e4-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e78e4-129">Setelah impor selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="e78e4-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e78e4-130">Periksa organisasi Anda untuk data dalam 26 entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="e78e4-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="e78e4-131">Mata uang</span><span class="sxs-lookup"><span data-stu-id="e78e4-131">Currency</span></span>
  - <span data-ttu-id="e78e4-132">Bagan Akun</span><span class="sxs-lookup"><span data-stu-id="e78e4-132">Chart of Accounts</span></span>
  - <span data-ttu-id="e78e4-133">Kalender Fiskal</span><span class="sxs-lookup"><span data-stu-id="e78e4-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="e78e4-134">Jenis Nilai Tukar Mata Uang</span><span class="sxs-lookup"><span data-stu-id="e78e4-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="e78e4-135">Hari Pembayaran</span><span class="sxs-lookup"><span data-stu-id="e78e4-135">Payment Day</span></span>
  - <span data-ttu-id="e78e4-136">Jadwal Pembayaran</span><span class="sxs-lookup"><span data-stu-id="e78e4-136">Payment Schedule</span></span>
  - <span data-ttu-id="e78e4-137">Persyaratan Pembayaran</span><span class="sxs-lookup"><span data-stu-id="e78e4-137">Payment Term</span></span>
  - <span data-ttu-id="e78e4-138">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="e78e4-138">Organizational Unit</span></span>
  - <span data-ttu-id="e78e4-139">Kontak</span><span class="sxs-lookup"><span data-stu-id="e78e4-139">Contact</span></span>
  - <span data-ttu-id="e78e4-140">Grup pajak</span><span class="sxs-lookup"><span data-stu-id="e78e4-140">Tax Group</span></span>
  - <span data-ttu-id="e78e4-141">Grup Pelanggan</span><span class="sxs-lookup"><span data-stu-id="e78e4-141">Customer Group</span></span>
  - <span data-ttu-id="e78e4-142">Grup Vendor</span><span class="sxs-lookup"><span data-stu-id="e78e4-142">Vendor Group</span></span>
  - <span data-ttu-id="e78e4-143">Unit</span><span class="sxs-lookup"><span data-stu-id="e78e4-143">Unit</span></span>
  - <span data-ttu-id="e78e4-144">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="e78e4-144">Unit Group</span></span>
  - <span data-ttu-id="e78e4-145">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="e78e4-145">Price List</span></span>
  - <span data-ttu-id="e78e4-146">Daftar Harga Parameter Proyek</span><span class="sxs-lookup"><span data-stu-id="e78e4-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="e78e4-147">Frekuensi Faktur</span><span class="sxs-lookup"><span data-stu-id="e78e4-147">Invoice Frequency</span></span>
  - <span data-ttu-id="e78e4-148">Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="e78e4-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="e78e4-149">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="e78e4-149">Transaction Category</span></span>
  - <span data-ttu-id="e78e4-150">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="e78e4-150">Expense Category</span></span>
  - <span data-ttu-id="e78e4-151">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="e78e4-151">Role Price</span></span>
  - <span data-ttu-id="e78e4-152">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="e78e4-152">Transaction Category Price</span></span>
  - <span data-ttu-id="e78e4-153">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="e78e4-153">Characteristic</span></span>
  - <span data-ttu-id="e78e4-154">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="e78e4-154">Bookable Resource</span></span>
  - <span data-ttu-id="e78e4-155">Keterkaitan Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="e78e4-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e78e4-156">Karakteristik Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="e78e4-156">Bookable Resource Characteristic</span></span>

![Impor Selesai](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e78e4-158">Memperbarui konfigurasi Project Operations</span><span class="sxs-lookup"><span data-stu-id="e78e4-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e78e4-159">Telusuri ke lingkungan CE.</span><span class="sxs-lookup"><span data-stu-id="e78e4-159">Navigate to the CE environment.</span></span> <span data-ttu-id="e78e4-160">Anda dapat menemukannya dengan membuka [Pusat admin Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih lingkungan, lalu memilih **buka lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Buka Lingkungan](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e78e4-162">Buka **proyek** > **sumber daya**, lalu pilih **baru** untuk membuat sumber daya yang dapat dipesan untuk pengguna Anda.</span><span class="sxs-lookup"><span data-stu-id="e78e4-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Sumber Daya yang Dapat Dipesan](./media/8BookableResources.png)

3. <span data-ttu-id="e78e4-164">Pada tab **Umum**, pilih pengguna admin.</span><span class="sxs-lookup"><span data-stu-id="e78e4-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e78e4-165">Verifikasikan bahwa zona waktu sesuai dengan yang Anda miliki.</span><span class="sxs-lookup"><span data-stu-id="e78e4-165">Verify that the time zone matches the one you are in.</span></span> 

![Sumber Daya Dapat Dipesan Baru](./media/9NewBookableResource.png)

4. <span data-ttu-id="e78e4-167">Pada tab **penjadwalan**, di bidang **perusahaan**, pilih perusahaan **USPM**, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tab Penjadwalan](./media/10SchedulingTab.png)

5. <span data-ttu-id="e78e4-169">Pilih tab **Jam kerja**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-169">Select the **Work hours** tab.</span></span>  

![Waktu Kerja](./media/11WorkHours.png)

6. <span data-ttu-id="e78e4-171">Klik dua kali pada nilai yang ada di kalender dan pilih **Edit** > **semua aktivitas dalam rangkaian**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalender Kerja](./media/12WorkCalendar.png)

7. <span data-ttu-id="e78e4-173">Ubah jam kerja menjadi hari kerja selama delapan (8) jam, tandai akhir pekan sebagai hari non-kerja, dan pastikan zona waktu cocok dengan Anda.</span><span class="sxs-lookup"><span data-stu-id="e78e4-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e78e4-174">Pilih **Simpan dan Tutup**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-174">Select **Save and close**.</span></span>

![Perbarui Kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e78e4-176">Buka **pengaturan** > **template kalender** dan pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Template Kalender](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e78e4-178">Masukkan nama, pilih sumber daya template yang Anda buat, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Simpan Template kalender](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e78e4-180">Buka **parameter** dan klik dua kali rekaman.</span><span class="sxs-lookup"><span data-stu-id="e78e4-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parameter Proyek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e78e4-182">Perbarui bidang berikut:</span><span class="sxs-lookup"><span data-stu-id="e78e4-182">Update the following fields:</span></span>

 - <span data-ttu-id="e78e4-183">**Perusahaan Default**: USPM</span><span class="sxs-lookup"><span data-stu-id="e78e4-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="e78e4-184">**Unit Organisasi Default**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="e78e4-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="e78e4-185">**Frekuensi faktur**: hari ketujuh dan terakhir</span><span class="sxs-lookup"><span data-stu-id="e78e4-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="e78e4-186">**Template jam kerja**: Ubah ke template yang Anda buat.</span><span class="sxs-lookup"><span data-stu-id="e78e4-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="e78e4-187">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="e78e4-187">Select **Save**.</span></span> 

![Pembaruan Parameter Proyek](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

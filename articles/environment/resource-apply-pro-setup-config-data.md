---
title: Pengaturan dan penerapan data konfigurasi di Common Data Service
description: Topik ini menyediakan informasi tentang mengonfigurasikan dan menerapkan data konfigurasi di Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401132"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="d7a92-103">Pengaturan dan penerapan data konfigurasi di Common Data Service</span><span class="sxs-lookup"><span data-stu-id="d7a92-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="d7a92-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="d7a92-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d7a92-105">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="d7a92-105">Prerequisites</span></span>

<span data-ttu-id="d7a92-106">Sebelum Anda mulai mengkonfigurasi data dalam Common Data Service (CDS), prasyarat berikut harus dipenuhi:</span><span class="sxs-lookup"><span data-stu-id="d7a92-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="d7a92-107">Penyediaan lingkungan CDS dan lingkungan Dynamics 365 Finance untuk Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d7a92-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="d7a92-108">Informasi entitas hukum dari Dynamics 365 Finance dibagi ke lingkungan CDS.</span><span class="sxs-lookup"><span data-stu-id="d7a92-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="d7a92-109">Ini berarti bahwa entitas **perusahaan** dalam CDS memiliki rekaman perusahaan berikut:</span><span class="sxs-lookup"><span data-stu-id="d7a92-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="d7a92-110">THPM</span><span class="sxs-lookup"><span data-stu-id="d7a92-110">THPM</span></span>
  - <span data-ttu-id="d7a92-111">USPM</span><span class="sxs-lookup"><span data-stu-id="d7a92-111">USPM</span></span>
  - <span data-ttu-id="d7a92-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="d7a92-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="d7a92-113">Menginstal data pengaturan dan konfigurasi</span><span class="sxs-lookup"><span data-stu-id="d7a92-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="d7a92-114">Unduh, buka blokir, dan buka [Paket paket data pengaturan dan konfigurasi](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="d7a92-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="d7a92-115">Arahkan ke folder zip terbuka dan Jalankan file eksekusi, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d7a92-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d7a92-116">Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d7a92-118">Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d7a92-119">Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d7a92-120">Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Masuk untuk konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d7a92-122">Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="d7a92-123">Pada halaman 4, pilih file zip, *SampleSetupAndConfigData* dari folder yang telah dibongkar.</span><span class="sxs-lookup"><span data-stu-id="d7a92-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Pilihan file zip](./media/3ZipFile.png)

![Pilih file](./media/4SelectAFile.png)

9. <span data-ttu-id="d7a92-126">Setelah file zip dipilih, pilih **impor data**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-126">After the zip file is selected, select **Import Data**.</span></span>

![Impor Data](./media/5ImportData.png)

10. <span data-ttu-id="d7a92-128">Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda.</span><span class="sxs-lookup"><span data-stu-id="d7a92-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d7a92-129">Setelah impor selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="d7a92-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d7a92-130">Periksa organisasi Anda untuk data dalam 19 entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="d7a92-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="d7a92-131">Mata uang</span><span class="sxs-lookup"><span data-stu-id="d7a92-131">Currency</span></span>
  - <span data-ttu-id="d7a92-132">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="d7a92-132">Organizational Unit</span></span>
  - <span data-ttu-id="d7a92-133">Kontak</span><span class="sxs-lookup"><span data-stu-id="d7a92-133">Contact</span></span>
  - <span data-ttu-id="d7a92-134">Grup pajak</span><span class="sxs-lookup"><span data-stu-id="d7a92-134">Tax Group</span></span>
  - <span data-ttu-id="d7a92-135">Grup Pelanggan</span><span class="sxs-lookup"><span data-stu-id="d7a92-135">Customer Group</span></span>
  - <span data-ttu-id="d7a92-136">Unit</span><span class="sxs-lookup"><span data-stu-id="d7a92-136">Unit</span></span>
  - <span data-ttu-id="d7a92-137">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="d7a92-137">Unit Group</span></span>
  - <span data-ttu-id="d7a92-138">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="d7a92-138">Price List</span></span>
  - <span data-ttu-id="d7a92-139">Daftar Harga Parameter Proyek</span><span class="sxs-lookup"><span data-stu-id="d7a92-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="d7a92-140">Frekuensi Faktur</span><span class="sxs-lookup"><span data-stu-id="d7a92-140">Invoice Frequency</span></span>
  - <span data-ttu-id="d7a92-141">Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d7a92-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="d7a92-142">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="d7a92-142">Transaction Category</span></span>
  - <span data-ttu-id="d7a92-143">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="d7a92-143">Expense Category</span></span>
  - <span data-ttu-id="d7a92-144">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="d7a92-144">Role Price</span></span>
  - <span data-ttu-id="d7a92-145">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="d7a92-145">Transaction Category Price</span></span>
  - <span data-ttu-id="d7a92-146">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="d7a92-146">Characteristic</span></span>
  - <span data-ttu-id="d7a92-147">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d7a92-147">Bookable Resource</span></span>
  - <span data-ttu-id="d7a92-148">Keterkaitan Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d7a92-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="d7a92-149">Karakteristik Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d7a92-149">Bookable Resource Characteristic</span></span>

![Impor Selesai](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="d7a92-151">Memperbarui konfigurasi Project Operations</span><span class="sxs-lookup"><span data-stu-id="d7a92-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="d7a92-152">Telusuri ke lingkungan CE.</span><span class="sxs-lookup"><span data-stu-id="d7a92-152">Navigate to the CE environment.</span></span> <span data-ttu-id="d7a92-153">Anda dapat menemukannya dengan membuka [Pusat admin Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih lingkungan, lalu memilih **buka lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Buka Lingkungan](./media/7OpenEnvironment.png)

2. <span data-ttu-id="d7a92-155">Buka **proyek** > **sumber daya**, lalu pilih **baru** untuk membuat sumber daya yang dapat dipesan untuk pengguna Anda.</span><span class="sxs-lookup"><span data-stu-id="d7a92-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Sumber Daya yang Dapat Dipesan](./media/8BookableResources.png)

3. <span data-ttu-id="d7a92-157">Pada tab **Umum**, pilih pengguna admin.</span><span class="sxs-lookup"><span data-stu-id="d7a92-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="d7a92-158">Verifikasikan bahwa zona waktu sesuai dengan yang Anda miliki.</span><span class="sxs-lookup"><span data-stu-id="d7a92-158">Verify that the time zone matches the one you are in.</span></span> 

![Sumber Daya Dapat Dipesan Baru](./media/9NewBookableResource.png)

4. <span data-ttu-id="d7a92-160">Pada tab **penjadwalan**, di bidang **perusahaan**, pilih perusahaan **USPM**, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tab Penjadwalan](./media/10SchedulingTab.png)

5. <span data-ttu-id="d7a92-162">Pilih tab **Jam kerja**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-162">Select the **Work hours** tab.</span></span>  

![Waktu Kerja](./media/11WorkHours.png)

6. <span data-ttu-id="d7a92-164">Klik dua kali pada nilai yang ada di kalender dan pilih **Edit** > **semua aktivitas dalam rangkaian**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalender Kerja](./media/12WorkCalendar.png)

7. <span data-ttu-id="d7a92-166">Ubah jam kerja menjadi hari kerja selama delapan (8) jam, tandai akhir pekan sebagai hari non-kerja, dan pastikan zona waktu cocok dengan Anda.</span><span class="sxs-lookup"><span data-stu-id="d7a92-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="d7a92-167">Pilih **Simpan dan Tutup**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-167">Select **Save and close**.</span></span>

![Perbarui Kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="d7a92-169">Buka **pengaturan** > **template kalender** dan pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Template Kalender](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="d7a92-171">Masukkan nama, pilih sumber daya template yang Anda buat, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Simpan Template kalender](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="d7a92-173">Buka **parameter** dan klik dua kali rekaman.</span><span class="sxs-lookup"><span data-stu-id="d7a92-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parameter Proyek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="d7a92-175">Perbarui bidang berikut:</span><span class="sxs-lookup"><span data-stu-id="d7a92-175">Update the following fields:</span></span>

 - <span data-ttu-id="d7a92-176">**Perusahaan Default**: USPM</span><span class="sxs-lookup"><span data-stu-id="d7a92-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="d7a92-177">**Unit organisasi default**:Aswono Robotics global</span><span class="sxs-lookup"><span data-stu-id="d7a92-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="d7a92-178">**Frekuensi faktur**: hari ketujuh dan terakhir</span><span class="sxs-lookup"><span data-stu-id="d7a92-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="d7a92-179">**Template jam kerja**: Ubah ke template yang Anda buat.</span><span class="sxs-lookup"><span data-stu-id="d7a92-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="d7a92-180">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="d7a92-180">Select **Save**.</span></span> 

![Pembaruan Parameter Proyek](./media/17UpdatedProjectParameters.png)

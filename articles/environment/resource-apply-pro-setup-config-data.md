---
title: Atur dan terapkan data konfigurasi di Common Data Service untuk Project Operations
description: Topik ini menyediakan informasi tentang mengonfigurasikan dan menerapkan data konfigurasi di Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948920"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="1f720-103">Atur dan terapkan data konfigurasi di Common Data Service untuk Project Operations</span><span class="sxs-lookup"><span data-stu-id="1f720-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="1f720-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="1f720-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="1f720-105">Menginstal data pengaturan dan konfigurasi</span><span class="sxs-lookup"><span data-stu-id="1f720-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="1f720-106">Unduh, buka blokir, dan buka [Paket paket data pengaturan dan konfigurasi](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="1f720-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="1f720-107">Arahkan ke folder zip terbuka dan Jalankan file eksekusi, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="1f720-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="1f720-108">Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.</span><span class="sxs-lookup"><span data-stu-id="1f720-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="1f720-110">Di Halaman 2 CMT Wizard, pilih **Office 365** sebagai **jenis penyebaran**.</span><span class="sxs-lookup"><span data-stu-id="1f720-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="1f720-111">Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.</span><span class="sxs-lookup"><span data-stu-id="1f720-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="1f720-112">Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="1f720-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Masuk untuk konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="1f720-114">Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="1f720-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="1f720-115">Pada halaman 4, pilih file zip, *SampleSetupAndConfigData* dari folder yang telah dibongkar.</span><span class="sxs-lookup"><span data-stu-id="1f720-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Pilihan file zip](./media/3ZipFile.png)

![Pilih file](./media/4SelectAFile.png)

9. <span data-ttu-id="1f720-118">Setelah file zip dipilih, pilih **impor data**.</span><span class="sxs-lookup"><span data-stu-id="1f720-118">After the zip file is selected, select **Import Data**.</span></span>

![Impor Data](./media/5ImportData.png)

10. <span data-ttu-id="1f720-120">Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda.</span><span class="sxs-lookup"><span data-stu-id="1f720-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="1f720-121">Setelah impor selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="1f720-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="1f720-122">Periksa organisasi Anda untuk data dalam 19 entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="1f720-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="1f720-123">Mata uang</span><span class="sxs-lookup"><span data-stu-id="1f720-123">Currency</span></span>
  - <span data-ttu-id="1f720-124">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="1f720-124">Organizational Unit</span></span>
  - <span data-ttu-id="1f720-125">Kontak</span><span class="sxs-lookup"><span data-stu-id="1f720-125">Contact</span></span>
  - <span data-ttu-id="1f720-126">Grup pajak</span><span class="sxs-lookup"><span data-stu-id="1f720-126">Tax Group</span></span>
  - <span data-ttu-id="1f720-127">Grup Pelanggan</span><span class="sxs-lookup"><span data-stu-id="1f720-127">Customer Group</span></span>
  - <span data-ttu-id="1f720-128">Unit</span><span class="sxs-lookup"><span data-stu-id="1f720-128">Unit</span></span>
  - <span data-ttu-id="1f720-129">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="1f720-129">Unit Group</span></span>
  - <span data-ttu-id="1f720-130">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="1f720-130">Price List</span></span>
  - <span data-ttu-id="1f720-131">Daftar Harga Parameter Proyek</span><span class="sxs-lookup"><span data-stu-id="1f720-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="1f720-132">Frekuensi Faktur</span><span class="sxs-lookup"><span data-stu-id="1f720-132">Invoice Frequency</span></span>
  - <span data-ttu-id="1f720-133">Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1f720-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="1f720-134">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1f720-134">Transaction Category</span></span>
  - <span data-ttu-id="1f720-135">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="1f720-135">Expense Category</span></span>
  - <span data-ttu-id="1f720-136">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="1f720-136">Role Price</span></span>
  - <span data-ttu-id="1f720-137">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1f720-137">Transaction Category Price</span></span>
  - <span data-ttu-id="1f720-138">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="1f720-138">Characteristic</span></span>
  - <span data-ttu-id="1f720-139">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1f720-139">Bookable Resource</span></span>
  - <span data-ttu-id="1f720-140">Keterkaitan Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1f720-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="1f720-141">Karakteristik Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1f720-141">Bookable Resource Characteristic</span></span>

![Impor Selesai](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="1f720-143">Memperbarui konfigurasi Project Operations</span><span class="sxs-lookup"><span data-stu-id="1f720-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="1f720-144">Telusuri ke lingkungan CE.</span><span class="sxs-lookup"><span data-stu-id="1f720-144">Navigate to the CE environment.</span></span> <span data-ttu-id="1f720-145">Anda dapat menemukannya dengan membuka [Pusat admin Power Platform](https://admin.powerplatform.microsoft.com/environments), memilih lingkungan, lalu memilih **buka lingkungan**.</span><span class="sxs-lookup"><span data-stu-id="1f720-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Buka Lingkungan](./media/7OpenEnvironment.png)

2. <span data-ttu-id="1f720-147">Buka **proyek** > **sumber daya**, lalu pilih **baru** untuk membuat sumber daya yang dapat dipesan untuk pengguna Anda.</span><span class="sxs-lookup"><span data-stu-id="1f720-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Sumber Daya yang Dapat Dipesan](./media/8BookableResources.png)

3. <span data-ttu-id="1f720-149">Pada tab **Umum**, pilih pengguna admin.</span><span class="sxs-lookup"><span data-stu-id="1f720-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="1f720-150">Verifikasikan bahwa zona waktu sesuai dengan yang Anda miliki.</span><span class="sxs-lookup"><span data-stu-id="1f720-150">Verify that the time zone matches the one you are in.</span></span> 

![Sumber Daya Dapat Dipesan Baru](./media/9NewBookableResource.png)

4. <span data-ttu-id="1f720-152">Pada tab **penjadwalan**, di bidang **perusahaan**, pilih perusahaan **USPM**, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="1f720-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Tab Penjadwalan](./media/10SchedulingTab.png)

5. <span data-ttu-id="1f720-154">Pilih tab **Jam kerja**.</span><span class="sxs-lookup"><span data-stu-id="1f720-154">Select the **Work hours** tab.</span></span>  

![Waktu Kerja](./media/11WorkHours.png)

6. <span data-ttu-id="1f720-156">Klik dua kali pada nilai yang ada di kalender dan pilih **Edit** > **semua aktivitas dalam rangkaian**.</span><span class="sxs-lookup"><span data-stu-id="1f720-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Kalender Kerja](./media/12WorkCalendar.png)

7. <span data-ttu-id="1f720-158">Ubah jam kerja menjadi hari kerja selama delapan (8) jam, tandai akhir pekan sebagai hari non-kerja, dan pastikan zona waktu cocok dengan Anda.</span><span class="sxs-lookup"><span data-stu-id="1f720-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="1f720-159">Pilih **Simpan dan Tutup**.</span><span class="sxs-lookup"><span data-stu-id="1f720-159">Select **Save and close**.</span></span>

![Perbarui Kalender](./media/13UpdateCalendar.png)

9. <span data-ttu-id="1f720-161">Buka **pengaturan** > **template kalender** dan pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="1f720-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Template Kalender](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="1f720-163">Masukkan nama, pilih sumber daya template yang Anda buat, lalu pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="1f720-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Simpan Template kalender](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="1f720-165">Buka **parameter** dan klik dua kali rekaman.</span><span class="sxs-lookup"><span data-stu-id="1f720-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parameter Proyek](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="1f720-167">Perbarui bidang berikut:</span><span class="sxs-lookup"><span data-stu-id="1f720-167">Update the following fields:</span></span>

 - <span data-ttu-id="1f720-168">**Perusahaan Default**: USPM</span><span class="sxs-lookup"><span data-stu-id="1f720-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="1f720-169">**Unit organisasi default**:Aswono Robotics global</span><span class="sxs-lookup"><span data-stu-id="1f720-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="1f720-170">**Frekuensi faktur**: hari ketujuh dan terakhir</span><span class="sxs-lookup"><span data-stu-id="1f720-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="1f720-171">**Template jam kerja**: Ubah ke template yang Anda buat.</span><span class="sxs-lookup"><span data-stu-id="1f720-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="1f720-172">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="1f720-172">Select **Save**.</span></span> 

![Pembaruan Parameter Proyek](./media/17UpdatedProjectParameters.png)

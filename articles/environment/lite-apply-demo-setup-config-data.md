---
title: Menerapkan konfigurasi demo dan data konfigurasi - lite
description: Topik ini menyediakan informasi tentang cara menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 762b0cf317d442565a033f56033a53a5b5cc435c
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089123"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="1eafe-103">Menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="1eafe-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="1eafe-104">_\*\*Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="1eafe-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1eafe-105">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="1eafe-105">Prerequisites</span></span>

<span data-ttu-id="1eafe-106">Sebelum Anda memulai konfigurasi, Anda harus memiliki lingkungan Common Data Service (CDS) yang tersedia untuk Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1eafe-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="1eafe-107">Petunjuk</span><span class="sxs-lookup"><span data-stu-id="1eafe-107">Instructions</span></span>

1. <span data-ttu-id="1eafe-108">Unduh [paket data induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="1eafe-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="1eafe-109">Arahkan ke folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* dan Jalankan file eksekusi, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="1eafe-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="1eafe-110">Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.</span><span class="sxs-lookup"><span data-stu-id="1eafe-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="1eafe-112">Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.</span><span class="sxs-lookup"><span data-stu-id="1eafe-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="1eafe-113">Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.</span><span class="sxs-lookup"><span data-stu-id="1eafe-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="1eafe-114">Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="1eafe-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Masuk untuk konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="1eafe-116">Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan kemudian pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="1eafe-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="1eafe-117">Pada halaman 4, pilih file zip, *MasterAndSetupData* dari folder yang dibongkar, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="1eafe-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![File Zip](./media/3ZipFile.png)

   ![Pilih file](./media/4SelectAFile.png)

9. <span data-ttu-id="1eafe-120">Setelah file zip dipilih, pilih **impor data**.</span><span class="sxs-lookup"><span data-stu-id="1eafe-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Impor data](./media/5ImportData.png)

10. <span data-ttu-id="1eafe-122">Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda.</span><span class="sxs-lookup"><span data-stu-id="1eafe-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="1eafe-123">Setelah selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="1eafe-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="1eafe-124">Periksa organisasi Anda untuk data dalam 20 entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="1eafe-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="1eafe-125">Mata uang</span><span class="sxs-lookup"><span data-stu-id="1eafe-125">Currency</span></span>
    -   <span data-ttu-id="1eafe-126">Akun</span><span class="sxs-lookup"><span data-stu-id="1eafe-126">Account</span></span>
    -   <span data-ttu-id="1eafe-127">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="1eafe-127">Organizational Unit</span></span>
    -   <span data-ttu-id="1eafe-128">Kontak</span><span class="sxs-lookup"><span data-stu-id="1eafe-128">Contact</span></span>
    -   <span data-ttu-id="1eafe-129">Unit</span><span class="sxs-lookup"><span data-stu-id="1eafe-129">Unit</span></span>
    -   <span data-ttu-id="1eafe-130">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="1eafe-130">Unit Group</span></span>
    -   <span data-ttu-id="1eafe-131">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="1eafe-131">Price List</span></span>
    -   <span data-ttu-id="1eafe-132">Daftar Harga Parameter Proyek</span><span class="sxs-lookup"><span data-stu-id="1eafe-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="1eafe-133">Frekuensi Faktur</span><span class="sxs-lookup"><span data-stu-id="1eafe-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="1eafe-134">Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1eafe-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="1eafe-135">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1eafe-135">Transaction Category</span></span>
    -   <span data-ttu-id="1eafe-136">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="1eafe-136">Expense Category</span></span>
    -   <span data-ttu-id="1eafe-137">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="1eafe-137">Role Price</span></span>
    -   <span data-ttu-id="1eafe-138">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="1eafe-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="1eafe-139">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="1eafe-139">Characteristic</span></span>
    -   <span data-ttu-id="1eafe-140">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1eafe-140">Bookable Resource</span></span>
    -   <span data-ttu-id="1eafe-141">Keterkaitan Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1eafe-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="1eafe-142">Karakteristik Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="1eafe-142">Bookable Resource Characteristic</span></span>

    ![Impor Selesai](./media/6CompleteImport.png)

---
title: Menerapkan konfigurasi demo dan data konfigurasi - lite
description: Topik ini menyediakan informasi tentang cara menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642097"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="d959c-103">Menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations - lite</span><span class="sxs-lookup"><span data-stu-id="d959c-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="d959c-104">_\*\*Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="d959c-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="d959c-105">Prasyarat</span><span class="sxs-lookup"><span data-stu-id="d959c-105">Prerequisites</span></span>

<span data-ttu-id="d959c-106">Sebelum Anda memulai konfigurasi, Anda harus memiliki lingkungan Common Data Service (CDS) yang tersedia untuk Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d959c-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="d959c-107">Petunjuk</span><span class="sxs-lookup"><span data-stu-id="d959c-107">Instructions</span></span>

1. <span data-ttu-id="d959c-108">Unduh [paket data induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="d959c-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="d959c-109">Arahkan ke folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* dan Jalankan file eksekusi, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="d959c-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="d959c-110">Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data**, lalu pilih **Lanjutkan**.</span><span class="sxs-lookup"><span data-stu-id="d959c-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="d959c-112">Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.</span><span class="sxs-lookup"><span data-stu-id="d959c-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="d959c-113">Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.</span><span class="sxs-lookup"><span data-stu-id="d959c-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="d959c-114">Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="d959c-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Masuk untuk konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="d959c-116">Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan kemudian pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="d959c-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="d959c-117">Pada halaman 4, pilih file zip, *MasterAndSetupData* dari folder yang dibongkar, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="d959c-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![File Zip](./media/3ZipFile.png)

![Pilih file](./media/4SelectAFile.png)

9. <span data-ttu-id="d959c-120">Setelah file zip dipilih, pilih **impor data**.</span><span class="sxs-lookup"><span data-stu-id="d959c-120">After the zip file is selected, select **Import Data**.</span></span>

![Impor data](./media/5ImportData.png)

10. <span data-ttu-id="d959c-122">Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda.</span><span class="sxs-lookup"><span data-stu-id="d959c-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="d959c-123">Setelah selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="d959c-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="d959c-124">Periksa organisasi Anda untuk data dalam 20 entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="d959c-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="d959c-125">Mata uang</span><span class="sxs-lookup"><span data-stu-id="d959c-125">Currency</span></span>
-   <span data-ttu-id="d959c-126">Akun</span><span class="sxs-lookup"><span data-stu-id="d959c-126">Account</span></span>
-   <span data-ttu-id="d959c-127">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="d959c-127">Organizational Unit</span></span>
-   <span data-ttu-id="d959c-128">Kontak</span><span class="sxs-lookup"><span data-stu-id="d959c-128">Contact</span></span>
-   <span data-ttu-id="d959c-129">Grup pajak</span><span class="sxs-lookup"><span data-stu-id="d959c-129">Tax Group</span></span>
-   <span data-ttu-id="d959c-130">Grup Pelanggan</span><span class="sxs-lookup"><span data-stu-id="d959c-130">Customer Group</span></span>
-   <span data-ttu-id="d959c-131">Unit</span><span class="sxs-lookup"><span data-stu-id="d959c-131">Unit</span></span>
-   <span data-ttu-id="d959c-132">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="d959c-132">Unit Group</span></span>
-   <span data-ttu-id="d959c-133">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="d959c-133">Price List</span></span>
-   <span data-ttu-id="d959c-134">Daftar Harga Parameter Proyek</span><span class="sxs-lookup"><span data-stu-id="d959c-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="d959c-135">Frekuensi Faktur</span><span class="sxs-lookup"><span data-stu-id="d959c-135">Invoice Frequency</span></span>
-   <span data-ttu-id="d959c-136">Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d959c-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="d959c-137">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="d959c-137">Transaction Category</span></span>
-   <span data-ttu-id="d959c-138">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="d959c-138">Expense Category</span></span>
-   <span data-ttu-id="d959c-139">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="d959c-139">Role Price</span></span>
-   <span data-ttu-id="d959c-140">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="d959c-140">Transaction Category Price</span></span>
-   <span data-ttu-id="d959c-141">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="d959c-141">Characteristic</span></span>
-   <span data-ttu-id="d959c-142">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d959c-142">Bookable Resource</span></span>
-   <span data-ttu-id="d959c-143">Keterkaitan Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d959c-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="d959c-144">Karakteristik Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="d959c-144">Bookable Resource Characteristic</span></span>

![Impor Selesai](./media/6CompleteImport.png)

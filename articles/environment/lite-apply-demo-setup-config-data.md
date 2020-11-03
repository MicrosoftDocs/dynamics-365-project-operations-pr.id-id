---
title: Menerapkan konfigurasi demo dan data konfigurasi
description: Topik ini menyediakan informasi tentang cara menerapkan konfigurasi demo dan data konfigurasi untuk Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078349"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="80389-103">Menerapkan konfigurasi demo dan data konfigurasi untuk penyebaran Project Operations Lite -menangani faktur proforma</span><span class="sxs-lookup"><span data-stu-id="80389-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="80389-104">_\*\*Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="80389-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="80389-105">Unduh [paket data induk](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="80389-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="80389-106">Arahkan ke folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* dan Jalankan file eksekusi, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="80389-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="80389-107">Di Halaman 1 Wizard Migrasi Konfigurasi Common Data Service (CMT), pilih **impor data** , lalu pilih **Lanjutkan**.</span><span class="sxs-lookup"><span data-stu-id="80389-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrasi Konfigurasi](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="80389-109">Di Halaman 2 CMT Wizard, pilih **Microsoft 365** sebagai **jenis penyebaran**.</span><span class="sxs-lookup"><span data-stu-id="80389-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="80389-110">Pilih **Tampilkan daftar organisasi tersedia** dan **Tampilkan kotak centang tingkat lanjut**.</span><span class="sxs-lookup"><span data-stu-id="80389-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="80389-111">Pilih kawasan penyewa Anda, masukkan kredensial, lalu pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="80389-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Masuk untuk konfigurasi](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="80389-113">Pada halaman 3, dari daftar organisasi pada penyewa, pilih organisasi yang akan diimpor data demo dan kemudian pilih **masuk**.</span><span class="sxs-lookup"><span data-stu-id="80389-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="80389-114">Pada halaman 4, pilih file zip, *MasterAndSetupData* dari folder yang dibongkar, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="80389-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![File Zip](./media/3ZipFile.png)

![Pilih file](./media/4SelectAFile.png)

9. <span data-ttu-id="80389-117">Setelah file zip dipilih, pilih **impor data**.</span><span class="sxs-lookup"><span data-stu-id="80389-117">After the zip file is selected, select **Import Data**.</span></span>

![Impor data](./media/5ImportData.png)

10. <span data-ttu-id="80389-119">Impor akan berjalan selama sekitar dua-sepuluh menit tergantung pada kecepatan jaringan Anda.</span><span class="sxs-lookup"><span data-stu-id="80389-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="80389-120">Setelah selesai, keluar dari Wizard CMT.</span><span class="sxs-lookup"><span data-stu-id="80389-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="80389-121">Periksa organisasi Anda untuk data dalam 20 entitas berikut:</span><span class="sxs-lookup"><span data-stu-id="80389-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="80389-122">Mata uang</span><span class="sxs-lookup"><span data-stu-id="80389-122">Currency</span></span>
- <span data-ttu-id="80389-123">Unit Organisasi</span><span class="sxs-lookup"><span data-stu-id="80389-123">Organizational Unit</span></span>
- <span data-ttu-id="80389-124">Kontak</span><span class="sxs-lookup"><span data-stu-id="80389-124">Contact</span></span>
- <span data-ttu-id="80389-125">Grup pajak</span><span class="sxs-lookup"><span data-stu-id="80389-125">Tax Group</span></span>
- <span data-ttu-id="80389-126">Grup Pelanggan</span><span class="sxs-lookup"><span data-stu-id="80389-126">Customer Group</span></span>
- <span data-ttu-id="80389-127">Unit</span><span class="sxs-lookup"><span data-stu-id="80389-127">Unit</span></span>
- <span data-ttu-id="80389-128">Grup Unit</span><span class="sxs-lookup"><span data-stu-id="80389-128">Unit Group</span></span>
- <span data-ttu-id="80389-129">Daftar Harga</span><span class="sxs-lookup"><span data-stu-id="80389-129">Price List</span></span>
- <span data-ttu-id="80389-130">Daftar Harga Parameter Proyek</span><span class="sxs-lookup"><span data-stu-id="80389-130">Project Parameter Price List</span></span>
- <span data-ttu-id="80389-131">Frekuensi Faktur</span><span class="sxs-lookup"><span data-stu-id="80389-131">Invoice Frequency</span></span>
- <span data-ttu-id="80389-132">Rincian Frekuensi Faktur</span><span class="sxs-lookup"><span data-stu-id="80389-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="80389-133">Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="80389-133">Bookable Resource Category</span></span>
- <span data-ttu-id="80389-134">Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="80389-134">Transaction Category</span></span>
- <span data-ttu-id="80389-135">Kategori Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="80389-135">Expense Category</span></span>
- <span data-ttu-id="80389-136">Harga Peran</span><span class="sxs-lookup"><span data-stu-id="80389-136">Role Price</span></span>
- <span data-ttu-id="80389-137">Harga Kategori Transaksi</span><span class="sxs-lookup"><span data-stu-id="80389-137">Transaction Category Price</span></span>
- <span data-ttu-id="80389-138">Karakteristik</span><span class="sxs-lookup"><span data-stu-id="80389-138">Characteristic</span></span>
- <span data-ttu-id="80389-139">Sumber Daya Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="80389-139">Bookable Resource</span></span>
- <span data-ttu-id="80389-140">Keterkaitan Kategori Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="80389-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="80389-141">Karakteristik Sumber Daya yang Dapat Dipesan</span><span class="sxs-lookup"><span data-stu-id="80389-141">Bookable Resource Characteristic</span></span>

![Impor Selesai](./media/6CompleteImport.png)

---
title: Jadwal pengeluaran dari penyelidikan dana pemberian Federal
description: Topik ini menyediakan informasi tentang jadwal pengeluaran dari penyelidikan dana pemberian Federal.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078468"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="ee23a-103">Jadwal pengeluaran dari penyelidikan dana pemberian Federal</span><span class="sxs-lookup"><span data-stu-id="ee23a-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ee23a-104">Menurut Surat edaran kantor manajemen dan anggaran A-133, lembaga yang menerima dana Federal tunduk pada persyaratan audit, yang juga dikenal sebagai audit tunggal.</span><span class="sxs-lookup"><span data-stu-id="ee23a-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="ee23a-105">Proses audit digunakan untuk melaporkan pendapatan dan pengeluaran hibah Federal secara berulang.</span><span class="sxs-lookup"><span data-stu-id="ee23a-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="ee23a-106">Bagian dari Laporan Audit tunggal mencakup jadwal pengeluaran dana pemberian Federal (SEFA).</span><span class="sxs-lookup"><span data-stu-id="ee23a-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="ee23a-107">Jadwal pengeluaran dari penyelidikan dana pemberian Federal mencakup judul Katalog bantuan domestik Federal (CFDA) dan nomor, nomor hibah, tahun hibah, nama badan federal yang menyediakan dana, dan nama entitas penerusan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="ee23a-108">Penyelidikan adalah untuk periode tertentu.</span><span class="sxs-lookup"><span data-stu-id="ee23a-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="ee23a-109">Biasanya, periode tersebut sama dengan periode laporan keuangan, yang merupakan tahun fiskal.</span><span class="sxs-lookup"><span data-stu-id="ee23a-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="ee23a-110">Penyelidikan mencakup hibah yang memiliki tanggal proyeksi dalam rentang tanggal yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="ee23a-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="ee23a-111">Kolom **lembaga pemberi hibah** dari penyelidikan menunjukkan pelanggan hibah atau, untuk lembaga penerusan hibah, pemberi hibah.</span><span class="sxs-lookup"><span data-stu-id="ee23a-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="ee23a-112">Untuk penerusan hibah, kolom **lembaga penerusan** menampilkan pelanggan hibah.</span><span class="sxs-lookup"><span data-stu-id="ee23a-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="ee23a-113">Jika hibah bukan penerusan hibah, kolom **lembaga penerusan** kosong.</span><span class="sxs-lookup"><span data-stu-id="ee23a-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="ee23a-114">Konfigurasikan kluster CFDA</span><span class="sxs-lookup"><span data-stu-id="ee23a-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="ee23a-115">Anda harus mengkonfigurasi kluster CFDA yang dapat dikaitkan dengan nomor CFDA dalam Penyelidikan jadwal pengeluaran pemberian dana federal.</span><span class="sxs-lookup"><span data-stu-id="ee23a-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="ee23a-116">Buka **manajemen proyek dan konfigurasi akuntansi \> Konfigurasi \> hibah \> Katalog kluster bantuan domestik Federal**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="ee23a-117">Untuk membuat kluster CFDA, pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="ee23a-118">Masukkan nama kluster.</span><span class="sxs-lookup"><span data-stu-id="ee23a-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="ee23a-119">Pilih **Simpan** untuk menerapkan perubahan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="ee23a-120">Mengkonfigurasi nomor CFDA</span><span class="sxs-lookup"><span data-stu-id="ee23a-120">Set up CFDA numbers</span></span>

<span data-ttu-id="ee23a-121">Anda harus mengkonfigurasi nomor CFDA yang dapat ditambahkan ke hibah dan disertakan dalam Penyelidikan jadwal pengeluaran pemberian dana federal.</span><span class="sxs-lookup"><span data-stu-id="ee23a-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="ee23a-122">Buka **manajemen proyek dan konfigurasi akuntansi \> Konfigurasi \> hibah \> nomor Katalog bantuan domestik Federal**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="ee23a-123">Untuk membuat nomor CFDA, pilih **Baru**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="ee23a-124">Dalam kolom **nomor** , masukkan nomor CFDA.</span><span class="sxs-lookup"><span data-stu-id="ee23a-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="ee23a-125">Tekan tombol **tab**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="ee23a-126">Dalam kolom **Deskripsi** , masukkan judul CFDA.</span><span class="sxs-lookup"><span data-stu-id="ee23a-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="ee23a-127">Tekan tombol **tab**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="ee23a-128">Opsional: di bidang **kluster program** , tambahkan kluster cfda yang sesuai.</span><span class="sxs-lookup"><span data-stu-id="ee23a-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="ee23a-129">Pilih **Simpan** untuk menerapkan perubahan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="ee23a-130">Atur hibah yang akan dilaporkan untuk Penyelidikan jadwal pengeluaran pemberian dana federal</span><span class="sxs-lookup"><span data-stu-id="ee23a-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="ee23a-131">Buka **manajemen proyek dan akuntansi \> hibah \> hibah** , lalu pilih hibah yang ada.</span><span class="sxs-lookup"><span data-stu-id="ee23a-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="ee23a-132">Pada fasttab **konfigurasi** , di bidang **Katalog Bantuan domestik Federal** , tetapkan nomor CFDA.</span><span class="sxs-lookup"><span data-stu-id="ee23a-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="ee23a-133">Nomor CFDA pada hibah menentukan kluster CFDA untuk pelaporan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="ee23a-134">Pada fasttab **informasi kontak** , masukkan informasi pemberi dengan mengikuti langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="ee23a-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="ee23a-135">Di bidang **pelanggan hibah** , masukkan Pelanggan yang bertanggung jawab atas hibah.</span><span class="sxs-lookup"><span data-stu-id="ee23a-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="ee23a-136">Untuk hibah yang ada, informasi ini mungkin sudah dimasukkan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="ee23a-137">Menunjukkan apakah pelanggan hibah adalah penyandang dana.</span><span class="sxs-lookup"><span data-stu-id="ee23a-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="ee23a-138">Jika pelanggan hibah adalah penyandang dana, biarkan kotak centang **Penerusan** dikosongkan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="ee23a-139">Jika pelanggan lain adalah penyandang dana, dan pelanggan hibah bertanggung jawab atas pembelanjaan dan pelacakan uang, pilih kotak centang **Penerusan**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="ee23a-140">Jika Anda memilih kotak centang **Penerusan** di langkah sebelumnya, di bidang **agen pemberi** , masukkan Pelanggan yang memberikan hibah.</span><span class="sxs-lookup"><span data-stu-id="ee23a-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="ee23a-141">Agen pemberi dan pelanggan hibah tidak dapat menjadi Pelanggan yang sama.</span><span class="sxs-lookup"><span data-stu-id="ee23a-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="ee23a-142">Berikut adalah contoh dari hibah penerusan:</span><span class="sxs-lookup"><span data-stu-id="ee23a-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="ee23a-143">Pemerintah federal mendanai proyek infrastruktur untuk suatu negara bagian.</span><span class="sxs-lookup"><span data-stu-id="ee23a-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="ee23a-144">Pemerintah federal memberikan uang kepada negara bagian itu untuk dibelanjakan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="ee23a-145">Dalam kasus ini, pemerintah federal adalah agen pemberi, dan negara bagian itu adalah pelanggan hibah.</span><span class="sxs-lookup"><span data-stu-id="ee23a-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="ee23a-146">Saat pertama kali mengaktifkan fitur, nomor CFDA awal akan dimasukkan menggunakan nomor yang ada pada hibah.</span><span class="sxs-lookup"><span data-stu-id="ee23a-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="ee23a-147">Kecualikan hibah dari pelaporan SEFA berdasarkan jenis hibah</span><span class="sxs-lookup"><span data-stu-id="ee23a-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="ee23a-148">Buka **manajemen proyek dan akuntansi \> Konfigurasi \> Hibah \> jenis Hibah**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="ee23a-149">Pada fasttab **informasi default** , pilih kotak centang **Kecualikan dari jadwal pengeluaran pemberian dana Federal**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="ee23a-150">Pilih **Simpan** untuk menerapkan perubahan.</span><span class="sxs-lookup"><span data-stu-id="ee23a-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="ee23a-151">Jalankan Jadwal pengeluaran dari penyelidikan dana pemberian Federal</span><span class="sxs-lookup"><span data-stu-id="ee23a-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="ee23a-152">Buka **manajemen proyek dan akuntansi \> Penyelidikan dan laporan \> Penyelidikan hibah \> jadwal pengeluaran pemberian dana Federal**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="ee23a-153">Di bagian **Parameter** , ikuti langkah berikut:</span><span class="sxs-lookup"><span data-stu-id="ee23a-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="ee23a-154">Pada bidang **interval tanggal** , pilih kode untuk interval tanggal.</span><span class="sxs-lookup"><span data-stu-id="ee23a-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="ee23a-155">Atau, di bidang **dari tanggal** dan **hingga tanggal** , tentukan interval tanggal.</span><span class="sxs-lookup"><span data-stu-id="ee23a-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="ee23a-156">Opsional: untuk mencakup hanya transaksi yang ditagih sebagai pendapatan dalam penyelidikan, atur pilihan **sertakan hanya pendapatan yang ditagihkan** ke **ya**.</span><span class="sxs-lookup"><span data-stu-id="ee23a-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="ee23a-157">Kolom</span><span class="sxs-lookup"><span data-stu-id="ee23a-157">Columns</span></span>

<span data-ttu-id="ee23a-158">Penyelidikan jadwal pengeluaran pemberian dana Federal mencakup kolom berikut:</span><span class="sxs-lookup"><span data-stu-id="ee23a-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="ee23a-159">Katalog nama kluster bantuan domestik Federal</span><span class="sxs-lookup"><span data-stu-id="ee23a-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="ee23a-160">Lembaga pemberi</span><span class="sxs-lookup"><span data-stu-id="ee23a-160">Grantor agency</span></span>
- <span data-ttu-id="ee23a-161">Lembaga penerusan</span><span class="sxs-lookup"><span data-stu-id="ee23a-161">Pass-through agency</span></span>
- <span data-ttu-id="ee23a-162">Nama hibah</span><span class="sxs-lookup"><span data-stu-id="ee23a-162">Grant name</span></span>
- <span data-ttu-id="ee23a-163">ID hibah</span><span class="sxs-lookup"><span data-stu-id="ee23a-163">Grant ID</span></span>
- <span data-ttu-id="ee23a-164">ID Aplikasi hibah</span><span class="sxs-lookup"><span data-stu-id="ee23a-164">Grant application ID</span></span>
- <span data-ttu-id="ee23a-165">Katalog bantuan domestik Federal</span><span class="sxs-lookup"><span data-stu-id="ee23a-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="ee23a-166">Tanda Terima</span><span class="sxs-lookup"><span data-stu-id="ee23a-166">Receipts</span></span>
- <span data-ttu-id="ee23a-167">Pengeluaran</span><span class="sxs-lookup"><span data-stu-id="ee23a-167">Expenditures</span></span>

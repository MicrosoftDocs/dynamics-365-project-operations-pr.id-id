---
title: Konfigurasi proyek faktur antarperusahaan
description: Topik ini menunjukkan cara menyiapkan faktur proyek antara dua perusahaan di organisasi anda.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078543"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="9a312-103">Konfigurasi proyek faktur antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="9a312-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9a312-104">Topik ini menunjukkan cara menyiapkan faktur proyek antara dua perusahaan di organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="9a312-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="9a312-105">Tugas ini menggunakan himpunan data USSI.</span><span class="sxs-lookup"><span data-stu-id="9a312-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9a312-106">Di panel navigasi, buka **modul > piutang > vendor > semua vendor**.</span><span class="sxs-lookup"><span data-stu-id="9a312-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="9a312-107">Di Daftar **semua vendor** , Cari dan pilih rekaman yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="9a312-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="9a312-108">Pada panel tindakan, pilih **umum**.</span><span class="sxs-lookup"><span data-stu-id="9a312-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="9a312-109">Pilih **Antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="9a312-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="9a312-110">Atur **aktif** ke **ya** untuk mengaktifkan perdagangan antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="9a312-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="9a312-111">Di bidang **Perusahaan pelanggan** , masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a312-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="9a312-112">Di bidang **Akun saya** , masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a312-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="9a312-113">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a312-113">Select **Save**.</span></span>
9. <span data-ttu-id="9a312-114">Tutup halaman untuk kembali ke halaman Beranda.</span><span class="sxs-lookup"><span data-stu-id="9a312-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="9a312-115">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > parameter manajemen proyek dan akuntansi**.</span><span class="sxs-lookup"><span data-stu-id="9a312-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="9a312-116">Pilih tab **Antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="9a312-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="9a312-117">Pindahkan slider ke **ya** untuk mengaktifkan penjadwalan dan lembar waktu sumber daya antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="9a312-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="9a312-118">Di daftar, Tandai baris yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="9a312-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9a312-119">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="9a312-119">Select **New**.</span></span>
15. <span data-ttu-id="9a312-120">Di bidang **Entitas hukum pinjaman** , masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a312-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="9a312-121">Pilih kotak centang **Akumulasikan penghasilan**.</span><span class="sxs-lookup"><span data-stu-id="9a312-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="9a312-122">Di bidang **Kategori lembar waktu default** , masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a312-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="9a312-123">Di bidang **Kategori pengeluaran default** , masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a312-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="9a312-124">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a312-124">Select **Save**.</span></span>
20. <span data-ttu-id="9a312-125">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="9a312-125">Close the page.</span></span>
21. <span data-ttu-id="9a312-126">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Posting > Konfigurasi posting buku besar**.</span><span class="sxs-lookup"><span data-stu-id="9a312-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="9a312-127">Di bidang **jenis akun buku besar** , pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="9a312-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="9a312-128">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="9a312-128">Select **New**.</span></span>
24. <span data-ttu-id="9a312-129">Di bidang **akun utama** baris baru, tentukan nilai yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="9a312-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="9a312-130">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a312-130">Select **Save**.</span></span>
26. <span data-ttu-id="9a312-131">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="9a312-131">Close the page.</span></span>
27. <span data-ttu-id="9a312-132">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Harga > Harga transfer**.</span><span class="sxs-lookup"><span data-stu-id="9a312-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="9a312-133">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="9a312-133">Select **New**.</span></span>
29. <span data-ttu-id="9a312-134">Di bidang **Tanggal efektif** , masukkan tanggal.</span><span class="sxs-lookup"><span data-stu-id="9a312-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="9a312-135">Di bidang **Entitas hukum pinjaman** , masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a312-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="9a312-136">Di bidang **model harga transfer** , pilih salah satu pilihan.</span><span class="sxs-lookup"><span data-stu-id="9a312-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="9a312-137">Di bidang **harga** , masukkan angka.</span><span class="sxs-lookup"><span data-stu-id="9a312-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="9a312-138">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a312-138">Select **Save**.</span></span>


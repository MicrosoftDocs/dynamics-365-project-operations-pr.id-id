---
title: Konfigurasi proyek faktur antarperusahaan
description: Topik ini menunjukkan cara menyiapkan faktur proyek antara dua perusahaan di organisasi anda.
author: KimANelson
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
ms.assetid: 72d6c257-f2d3-483b-8ff2-445263796963
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7b199c85736f6268bc5914fddaa10e4cabd44ef1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752394"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="9a02d-103">Konfigurasi proyek faktur antarperusahaan</span><span class="sxs-lookup"><span data-stu-id="9a02d-103">Configure intercompany project invoicing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9a02d-104">Topik ini menunjukkan cara menyiapkan faktur proyek antara dua perusahaan di organisasi anda.</span><span class="sxs-lookup"><span data-stu-id="9a02d-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="9a02d-105">Tugas ini menggunakan himpunan data USSI.</span><span class="sxs-lookup"><span data-stu-id="9a02d-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9a02d-106">Di panel navigasi, buka **modul > piutang > vendor > semua vendor**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="9a02d-107">Di Daftar **semua vendor**, Cari dan pilih rekaman yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="9a02d-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="9a02d-108">Pada panel tindakan, pilih **umum**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="9a02d-109">Pilih **Antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="9a02d-110">Atur **aktif** ke **ya** untuk mengaktifkan perdagangan antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="9a02d-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="9a02d-111">Di bidang **Perusahaan pelanggan**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a02d-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="9a02d-112">Di bidang **Akun saya**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a02d-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="9a02d-113">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-113">Select **Save**.</span></span>
9. <span data-ttu-id="9a02d-114">Tutup halaman untuk kembali ke halaman Beranda.</span><span class="sxs-lookup"><span data-stu-id="9a02d-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="9a02d-115">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > parameter manajemen proyek dan akuntansi**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="9a02d-116">Pilih tab **Antarperusahaan**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="9a02d-117">Pindahkan slider ke **ya** untuk mengaktifkan penjadwalan dan lembar waktu sumber daya antarperusahaan.</span><span class="sxs-lookup"><span data-stu-id="9a02d-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="9a02d-118">Di daftar, Tandai baris yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="9a02d-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="9a02d-119">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-119">Select **New**.</span></span>
15. <span data-ttu-id="9a02d-120">Di bidang **Entitas hukum pinjaman**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a02d-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="9a02d-121">Pilih kotak centang **Akumulasikan penghasilan**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="9a02d-122">Di bidang **Kategori lembar waktu default**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a02d-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="9a02d-123">Di bidang **Kategori pengeluaran default**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a02d-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="9a02d-124">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-124">Select **Save**.</span></span>
20. <span data-ttu-id="9a02d-125">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="9a02d-125">Close the page.</span></span>
21. <span data-ttu-id="9a02d-126">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Posting > Konfigurasi posting buku besar**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="9a02d-127">Di bidang **jenis akun buku besar**, pilih pilihan.</span><span class="sxs-lookup"><span data-stu-id="9a02d-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="9a02d-128">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-128">Select **New**.</span></span>
24. <span data-ttu-id="9a02d-129">Di bidang **akun utama** baris baru, tentukan nilai yang diinginkan.</span><span class="sxs-lookup"><span data-stu-id="9a02d-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="9a02d-130">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-130">Select **Save**.</span></span>
26. <span data-ttu-id="9a02d-131">Tutup halaman.</span><span class="sxs-lookup"><span data-stu-id="9a02d-131">Close the page.</span></span>
27. <span data-ttu-id="9a02d-132">Di panel navigasi, buka **modul > manajemen proyek dan akuntansi > konfigurasi > Harga > Harga transfer**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="9a02d-133">Pilih **baru**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-133">Select **New**.</span></span>
29. <span data-ttu-id="9a02d-134">Di bidang **Tanggal efektif**, masukkan tanggal.</span><span class="sxs-lookup"><span data-stu-id="9a02d-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="9a02d-135">Di bidang **Entitas hukum pinjaman**, masukkan atau pilih nilai.</span><span class="sxs-lookup"><span data-stu-id="9a02d-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="9a02d-136">Di bidang **model harga transfer**, pilih salah satu pilihan.</span><span class="sxs-lookup"><span data-stu-id="9a02d-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="9a02d-137">Di bidang **harga**, masukkan angka.</span><span class="sxs-lookup"><span data-stu-id="9a02d-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="9a02d-138">Pilih **Simpan**.</span><span class="sxs-lookup"><span data-stu-id="9a02d-138">Select **Save**.</span></span>


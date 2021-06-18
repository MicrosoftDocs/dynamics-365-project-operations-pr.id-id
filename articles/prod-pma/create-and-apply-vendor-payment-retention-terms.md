---
title: Membuat dan menerapkan persyaratan retensi pembayaran vendor
description: Topik ini menyediakan informasi tentang cara mengkonfigurasi dan memelihara persyaratan retensi untuk pembayaran vendor.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 09bb30f55ee8e1f24634e9d8b7dea95bd3dbd24f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006334"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="98e44-103">Membuat dan menerapkan persyaratan retensi pembayaran vendor</span><span class="sxs-lookup"><span data-stu-id="98e44-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="98e44-104">Mengatur persyaratan retensi pembayaran vendor untuk proyek berguna bila organisasi Anda ingin mempertahankan bagian dari pembayaran yang dilakukan ke vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="98e44-105">Misalnya, bila Anda ingin menyimpan pembayaran ke vendor hingga produk yang dikirim memenuhi harapan Anda.</span><span class="sxs-lookup"><span data-stu-id="98e44-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="98e44-106">Persyaratan retensi pembayaran vendor dapat ditentukan saat Anda menegosiasikan kontrak vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="98e44-107">Membuat persyaratan retensi pembayaran vendor</span><span class="sxs-lookup"><span data-stu-id="98e44-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="98e44-108">Anda dapat memasukkan persentase pembayaran vendor untuk retensi dan persentase dari jumlah disimpan sebelumnya yang akan dirilis.</span><span class="sxs-lookup"><span data-stu-id="98e44-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="98e44-109">Jumlah akan disimpan secara otomatis pada faktur vendor hingga kontrak mencapai status penyelesaian yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="98e44-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="98e44-110">Setelah mengkonfigurasi persyaratan retensi, Anda dapat menerapkannya ke proyek apa pun untuk vendor tersebut.</span><span class="sxs-lookup"><span data-stu-id="98e44-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="98e44-111">Gunakan langkah-langkah berikut untuk mengkonfigurasi dan memelihara persyaratan retensi untuk pembayaran vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="98e44-112">Buka **manajemen proyek dan akuntansi** > **Retensi** > **persyaratan retensi pembayaran vendor**.</span><span class="sxs-lookup"><span data-stu-id="98e44-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="98e44-113">Pilih **baru** untuk menambahkan persyaratan retensi vendor baru.</span><span class="sxs-lookup"><span data-stu-id="98e44-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="98e44-114">Nilai **id aturan** untuk persyaratan baru akan dimasukkan secara otomatis.</span><span class="sxs-lookup"><span data-stu-id="98e44-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="98e44-115">Masukkan deskripsi singkat di bidang **deskripsi**, dan pada fasttab **persyaratan**, pilih **Tambah baris** untuk memasukkan nilai persyaratan untuk berikut ini:</span><span class="sxs-lookup"><span data-stu-id="98e44-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="98e44-116">**Persentase unit yang dikirim**: masukkan persentase penyelesaian untuk persyaratan.</span><span class="sxs-lookup"><span data-stu-id="98e44-116">**Percentage of units delivered**: Enter a percentage of completion for the term.</span></span> <span data-ttu-id="98e44-117">Jumlah akan ditahan secara otomatis pada faktur vendor hingga tahapan penyelesaian proyek setara dengan persentase yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="98e44-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="98e44-118">Misalnya, jika Anda memasukkan 50,00, jumlah ditahan hingga proyek 50 persen selesai.</span><span class="sxs-lookup"><span data-stu-id="98e44-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="98e44-119">**Persentase untuk ditahan**: masukkan persentase jumlah faktur vendor yang akan ditahan.</span><span class="sxs-lookup"><span data-stu-id="98e44-119">**Percentage to retain**: Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="98e44-120">Misalnya, jika Anda memasukkan 10,00, maka 10 persen dari jumlah faktur vendor ditahan hingga proyek mencapai persentase Penyelesaian sebagaimana diatur dalam **bidang persentase unit yang dikirim**.</span><span class="sxs-lookup"><span data-stu-id="98e44-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="98e44-121">**Persentase untuk rilis** : Pilih **Tambah baris** untuk memasukkan persentase dari jumlah yang sebelumnya ditahan akan dirilis untuk tingkat penyelesaian proyek yang dipilih.</span><span class="sxs-lookup"><span data-stu-id="98e44-121">**Percentage to release**: Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="98e44-122">Jika Anda memiliki lebih dari satu tonggak untuk tingkat penyelesaian proyek yang berbeda, masukkan baris persyaratan retensi vendor terpisah untuk setiap aturan retensi.</span><span class="sxs-lookup"><span data-stu-id="98e44-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="98e44-123">Setiap baris dapat menentukan persentase retensi berbeda dan persentase rilis berbeda untuk setiap tingkat penyelesaian proyek yang ditentukan.</span><span class="sxs-lookup"><span data-stu-id="98e44-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="98e44-124">Setelah Anda membuat persyaratan retensi vendor, Anda dapat menerapkannya persyaratan tersebut ke sebuah proyek.</span><span class="sxs-lookup"><span data-stu-id="98e44-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="98e44-125">Terapkan persyaratan retensi vendor ke proyek</span><span class="sxs-lookup"><span data-stu-id="98e44-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="98e44-126">Buka **Management Proyek dan Akuntansi** > **Proyek** > **semua proyek** dan buka proyek dari halaman daftar proyek.</span><span class="sxs-lookup"><span data-stu-id="98e44-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="98e44-127">Pada fasttab **perjanjian vendor**, pilih **Tambah baris**.</span><span class="sxs-lookup"><span data-stu-id="98e44-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="98e44-128">Di **bidang kode akun**, pilih salah satu pilihan berikut:</span><span class="sxs-lookup"><span data-stu-id="98e44-128">In the **Account code field**, select one of the following options:</span></span> 

   - <span data-ttu-id="98e44-129">**Tabel**: persyaratan retensi vendor berlaku untuk satu vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-129">**Table**: The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="98e44-130">**Grup**: persyaratan retensi vendor berlaku untuk semua vendor dalam grup vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-130">**Group**: The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="98e44-131">**Semua**: persyaratan retensi vendor berlaku untuk semua vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-131">**All**: The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="98e44-132">Di **bidang vendor/grup vendor**, pilih vendor atau grup vendor yang menerapkan persyaratan retensi vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-132">In the **Vendor/Vendor group field**, select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="98e44-133">Jika Anda memilih **semua** di langkah sebelumnya, bidang ini tidak tersedia.</span><span class="sxs-lookup"><span data-stu-id="98e44-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="98e44-134">Di bidang **persyaratan retensi vendor**, pilih persyaratan retensi yang Anda buat di prosedur sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="98e44-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="98e44-135">Jika proyek juga memiliki persyaratan bayar-saat-dibayar (PWP) yang diatur untuk vendor, masukkan persentase ambang batas untuk proyek di bidang **persentase ambang PWP**.</span><span class="sxs-lookup"><span data-stu-id="98e44-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="98e44-136">Persyaratan retensi vendor juga ditampilkan pada pesanan pembelian yang Anda buat untuk vendor.</span><span class="sxs-lookup"><span data-stu-id="98e44-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
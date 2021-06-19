---
title: Rangkaian persetujuan
description: Pembaruan topik memberikan informasi tentang kumpulan persetujuan, permintaan, dan subset operasi tersebut.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116875"
---
# <a name="approval-sets"></a><span data-ttu-id="a1c77-103">Rangkaian persetujuan</span><span class="sxs-lookup"><span data-stu-id="a1c77-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a1c77-104">Rangkaian persetujuan mengelompokkan permintaan persetujuan grup ke dalam subset operasi yang lebih kecil.</span><span class="sxs-lookup"><span data-stu-id="a1c77-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="a1c77-105">Pengelompokan ini memungkinkan persetujuan diproses secara berurutan menurut Proyek dan memungkinkan untuk mencoba ulang dan mengurutkan.</span><span class="sxs-lookup"><span data-stu-id="a1c77-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="a1c77-106">Mengelompokkan akan meningkatkan keandalan dan keterlacakan pemrosesan persetujuan untuk volume persetujuan yang besar.</span><span class="sxs-lookup"><span data-stu-id="a1c77-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="a1c77-107">Rangkaian persetujuan menunjukkan status pemrosesan keseluruhan rekaman terkait.</span><span class="sxs-lookup"><span data-stu-id="a1c77-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="a1c77-108">Bila rekaman persetujuan diproses menggunakan rangkaian persetujuan, rekaman akan berpindah dari **Diajukan** ke **Disetujui**, dan tidak ditautkan dari rangkaian persetujuan.</span><span class="sxs-lookup"><span data-stu-id="a1c77-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="a1c77-109">Jika rekaman gagal saat diajukan untuk persetujuan, rekaman tetap dalam status **Diajukan** dan rangkaian persetujuan ditandai sebagai gagal.</span><span class="sxs-lookup"><span data-stu-id="a1c77-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="a1c77-110">Rangkaian persetujuan akan mencatat pesan kesalahan kegagalan.</span><span class="sxs-lookup"><span data-stu-id="a1c77-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="a1c77-111">Memproses persetujuan dan rangkaian persetujuan</span><span class="sxs-lookup"><span data-stu-id="a1c77-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="a1c77-112">Persetujuan yang diantrekan untuk pemrosesan dapat dilihat di tampilan **Pemrosesan Persetujuan**.</span><span class="sxs-lookup"><span data-stu-id="a1c77-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="a1c77-113">Sistem mencoba memproses semua entri beberapa kali secara asinkron, termasuk mencoba ulang persetujuan jika upaya sebelumnya gagal.</span><span class="sxs-lookup"><span data-stu-id="a1c77-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="a1c77-114">Bidang **Usia Rangkaian Persetujuan** mencatat jumlah upaya yang tersisa untuk memproses rangkaian sebelum ditandai sebagai gagal.</span><span class="sxs-lookup"><span data-stu-id="a1c77-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="a1c77-115">Persetujuan dan rangkaian persetujuan yang gagal</span><span class="sxs-lookup"><span data-stu-id="a1c77-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="a1c77-116">Tampilan **Persetujuan Gagal** mencantumkan semua persetujuan yang memerlukan intervensi pengguna.</span><span class="sxs-lookup"><span data-stu-id="a1c77-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="a1c77-117">Buka log rangkaian persetujuan yang terkait untuk mengidentifikasi penyebab kegagalan.</span><span class="sxs-lookup"><span data-stu-id="a1c77-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="a1c77-118">Memilih **Coba lagi** menambahkan ke jumlah usia rangkaian persetujuan, memindahkan rangkaian persetujuan kembali ke status **Pemrosesan**, dan mencoba memproses rekaman yang tersisa.</span><span class="sxs-lookup"><span data-stu-id="a1c77-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="a1c77-119">Konfigurasikan Rangkaian Persetujuan</span><span class="sxs-lookup"><span data-stu-id="a1c77-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="a1c77-120">Aktifkan fitur Rangkaian Persetujuan</span><span class="sxs-lookup"><span data-stu-id="a1c77-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="a1c77-121">Sebelum Anda mengaktifkan fitur rangkaian Persetujuan, pastikan tidak ada persetujuan yang saat ini diproses.</span><span class="sxs-lookup"><span data-stu-id="a1c77-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a1c77-122">Buka halaman **parameter Proyek**, lalu pilih **Kontrol Fitur** > **Aktifkan Persetujuan Modern**.</span><span class="sxs-lookup"><span data-stu-id="a1c77-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="a1c77-123">Nonaktifkan fitur Rangkaian Persetujuan</span><span class="sxs-lookup"><span data-stu-id="a1c77-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="a1c77-124">Sebelum Anda menonaktifkan fitur rangkaian Persetujuan, pastikan tidak ada persetujuan yang saat ini diproses.</span><span class="sxs-lookup"><span data-stu-id="a1c77-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="a1c77-125">Buka halaman **parameter Proyek**, lalu pilih **Kontrol Fitur** > **Nonaktifkan Persetujuan Modern**.</span><span class="sxs-lookup"><span data-stu-id="a1c77-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="a1c77-126">Mengkonfigurasi ambang batas asinkron</span><span class="sxs-lookup"><span data-stu-id="a1c77-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="a1c77-127">Bila rangkaian persetujuan dibuat, pemrosesan akan berpindah ke latar belakang bila jumlah rekaman yang dipilih untuk disetujui melebihi ambang batas yang ditunjukkan.</span><span class="sxs-lookup"><span data-stu-id="a1c77-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="a1c77-128">Gunakan bidang **Ambang Batas Asinkron** untuk mengkonfigurasi ketika pemrosesan persetujuan harus dijalankan secara sinkron atau asinkron.</span><span class="sxs-lookup"><span data-stu-id="a1c77-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="a1c77-129">Nilai yang valid adalah:</span><span class="sxs-lookup"><span data-stu-id="a1c77-129">Valid values are:</span></span>

  - <span data-ttu-id="a1c77-130">Nol: Semua permintaan harus diproses secara asinkron.</span><span class="sxs-lookup"><span data-stu-id="a1c77-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="a1c77-131">Angka yang lebih besar dari nol: Persetujuan diproses secara asinkron hanya bila jumlah persetujuan yang diajukan melebihi nilai ini.</span><span class="sxs-lookup"><span data-stu-id="a1c77-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]

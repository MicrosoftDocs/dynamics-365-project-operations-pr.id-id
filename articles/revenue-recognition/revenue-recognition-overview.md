---
title: Sekilas pengakuan pendapatan
description: Topik ini berisi informasi tentang pengakuan pendapatan dalam Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531458"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="723a7-103">Sekilas pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="723a7-103">Revenue recognition overview</span></span>

<span data-ttu-id="723a7-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="723a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="723a7-105">Di Dynamics 365 Project Operations, prinsip pengakuan pendapatan bervariasi berdasarkan pada metode penagihan yang dipilih untuk proyek atau bagian dari proyek.</span><span class="sxs-lookup"><span data-stu-id="723a7-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="723a7-106">Topik ini berisi informasi tentang pengakuan pendapatan dalam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="723a7-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="723a7-107">Transaksi yang dihitung menggunakan metode penagihan waktu dan material</span><span class="sxs-lookup"><span data-stu-id="723a7-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="723a7-108">Pengakuan biaya dan pendapatan terhubung.</span><span class="sxs-lookup"><span data-stu-id="723a7-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="723a7-109">Biaya transaksi dan penjualan yang belum ditagih diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="723a7-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="723a7-110">Biaya proyek dan profil pendapatan menentukan apakah transaksi penjualan yang belum ditagih diposting di buku besar.</span><span class="sxs-lookup"><span data-stu-id="723a7-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="723a7-111">Jika **Pendapatan yang terkumpul** dipilih, sistem menggunakan **Nilai penjualan WIP** dan akun **Nilai penjualan pendapatan yang terkumpul** saat posting dilakukan.</span><span class="sxs-lookup"><span data-stu-id="723a7-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="723a7-112">Berikut adalah contoh dari metode ini.</span><span class="sxs-lookup"><span data-stu-id="723a7-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="723a7-113">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="723a7-113">Transaction type</span></span> | <span data-ttu-id="723a7-114">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="723a7-114">Debit/Credit</span></span> | <span data-ttu-id="723a7-115">Jumlah</span><span class="sxs-lookup"><span data-stu-id="723a7-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="723a7-116">Nilai Penjualan WIP</span><span class="sxs-lookup"><span data-stu-id="723a7-116">WIP Sales value</span></span> | <span data-ttu-id="723a7-117">Debit</span><span class="sxs-lookup"><span data-stu-id="723a7-117">Debit</span></span> | <span data-ttu-id="723a7-118">100</span><span class="sxs-lookup"><span data-stu-id="723a7-118">100</span></span> |
  | <span data-ttu-id="723a7-119">pendapatan akrual - nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="723a7-119">Accrued revenue sales value</span></span> | <span data-ttu-id="723a7-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="723a7-120">Credit</span></span> | <span data-ttu-id="723a7-121">100</span><span class="sxs-lookup"><span data-stu-id="723a7-121">100</span></span> |

- <span data-ttu-id="723a7-122">Pendapatan direkognisi pada saat pembuatan faktur.</span><span class="sxs-lookup"><span data-stu-id="723a7-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="723a7-123">Sistem menggunakan akun **Pendapatan tertagih** pada saat diposting.</span><span class="sxs-lookup"><span data-stu-id="723a7-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="723a7-124">Berikut adalah contoh dari metode ini.</span><span class="sxs-lookup"><span data-stu-id="723a7-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="723a7-125">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="723a7-125">Transaction type</span></span> | <span data-ttu-id="723a7-126">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="723a7-126">Debit/Credit</span></span> | <span data-ttu-id="723a7-127">Jumlah</span><span class="sxs-lookup"><span data-stu-id="723a7-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="723a7-128">Saldo pelanggan</span><span class="sxs-lookup"><span data-stu-id="723a7-128">Customer balance</span></span> | <span data-ttu-id="723a7-129">Debit</span><span class="sxs-lookup"><span data-stu-id="723a7-129">Debit</span></span> | <span data-ttu-id="723a7-130">120</span><span class="sxs-lookup"><span data-stu-id="723a7-130">120</span></span> |
  | <span data-ttu-id="723a7-131">Pajak penjualan untuk dibayarkan</span><span class="sxs-lookup"><span data-stu-id="723a7-131">Sales tax payable</span></span> | <span data-ttu-id="723a7-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="723a7-132">Credit</span></span> | <span data-ttu-id="723a7-133">20</span><span class="sxs-lookup"><span data-stu-id="723a7-133">20</span></span> |
  | <span data-ttu-id="723a7-134">Pendapatan Tertagih</span><span class="sxs-lookup"><span data-stu-id="723a7-134">Invoiced Revenue</span></span> | <span data-ttu-id="723a7-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="723a7-135">Credit</span></span> | <span data-ttu-id="723a7-136">100</span><span class="sxs-lookup"><span data-stu-id="723a7-136">100</span></span> |

- <span data-ttu-id="723a7-137">Jika pendapatan diperoleh saat penjualan yang belum ditagih diposting, sistem akan membalikkan pendapatan yang diperoleh pada faktur.</span><span class="sxs-lookup"><span data-stu-id="723a7-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="723a7-138">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="723a7-138">Transaction type</span></span> | <span data-ttu-id="723a7-139">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="723a7-139">Debit/Credit</span></span> | <span data-ttu-id="723a7-140">Jumlah</span><span class="sxs-lookup"><span data-stu-id="723a7-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="723a7-141">Nilai Penjualan WIP</span><span class="sxs-lookup"><span data-stu-id="723a7-141">WIP Sales value</span></span> | <span data-ttu-id="723a7-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="723a7-142">Credit</span></span> | <span data-ttu-id="723a7-143">100</span><span class="sxs-lookup"><span data-stu-id="723a7-143">100</span></span> |
  | <span data-ttu-id="723a7-144">pendapatan akrual - nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="723a7-144">Accrued revenue sales value</span></span> | <span data-ttu-id="723a7-145">Debit</span><span class="sxs-lookup"><span data-stu-id="723a7-145">Debit</span></span> | <span data-ttu-id="723a7-146">100</span><span class="sxs-lookup"><span data-stu-id="723a7-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="723a7-147">Transaksi yang dihitung menggunakan metode penagihan harga tetap</span><span class="sxs-lookup"><span data-stu-id="723a7-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="723a7-148">Pengakuan biaya dan pendapatan terpisah.</span><span class="sxs-lookup"><span data-stu-id="723a7-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="723a7-149">Biaya transaksi diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="723a7-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="723a7-150">Transaksi penjualan yang belum ditagih tidak dibuat.</span><span class="sxs-lookup"><span data-stu-id="723a7-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="723a7-151">Pendapatan dapat direkognisi saat pembuatan faktur jika biaya proyek dan profil pendapatan memiliki **Prinsip yang digunakan untuk penghitungan penyelesaian proyek** yang diatur ke **Tanpa WIP**.</span><span class="sxs-lookup"><span data-stu-id="723a7-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="723a7-152">Hanya gunakan metode ini untuk proyek jangka pendek dan sederhana.</span><span class="sxs-lookup"><span data-stu-id="723a7-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="723a7-153">Pendapatan dapat direkognisi menggunakan estimasi pendapatan harga tetap, baik dengan metode **Kontrak yang selesai** maupun **Persen penyelesaian pengakuan pendapatan**.</span><span class="sxs-lookup"><span data-stu-id="723a7-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="723a7-154">Sumber daya tambahan</span><span class="sxs-lookup"><span data-stu-id="723a7-154">Additional resources</span></span>
[<span data-ttu-id="723a7-155">Mengonfigurasikan akuntansi untuk artikel yang bisa ditagih</span><span class="sxs-lookup"><span data-stu-id="723a7-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="723a7-156">Proyek estimasi pendapatan harga tetap</span><span class="sxs-lookup"><span data-stu-id="723a7-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="723a7-157">Mengelola estimasi pendapatan</span><span class="sxs-lookup"><span data-stu-id="723a7-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="723a7-158">Metode biaya penyelesaian</span><span class="sxs-lookup"><span data-stu-id="723a7-158">Cost to complete methods</span></span>](cost-complete-methods.md)

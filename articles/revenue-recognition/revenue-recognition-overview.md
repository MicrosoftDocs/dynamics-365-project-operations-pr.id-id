---
title: Sekilas pengakuan pendapatan
description: Topik ini berisi informasi tentang pengakuan pendapatan dalam Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368030"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="f8195-103">Sekilas pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="f8195-103">Revenue recognition overview</span></span>

<span data-ttu-id="f8195-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="f8195-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f8195-105">Di Dynamics 365 Project Operations, prinsip pengakuan pendapatan bervariasi berdasarkan pada metode penagihan yang dipilih untuk proyek atau bagian dari proyek.</span><span class="sxs-lookup"><span data-stu-id="f8195-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="f8195-106">Topik ini berisi informasi tentang pengakuan pendapatan dalam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f8195-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="f8195-107">Transaksi yang dihitung menggunakan metode penagihan waktu dan material</span><span class="sxs-lookup"><span data-stu-id="f8195-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="f8195-108">Pengakuan biaya dan pendapatan terhubung.</span><span class="sxs-lookup"><span data-stu-id="f8195-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="f8195-109">Biaya transaksi dan penjualan yang belum ditagih diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="f8195-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="f8195-110">Biaya proyek dan profil pendapatan menentukan apakah transaksi penjualan yang belum ditagih diposting di buku besar.</span><span class="sxs-lookup"><span data-stu-id="f8195-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="f8195-111">Jika **Pendapatan yang terkumpul** dipilih, sistem menggunakan **Nilai penjualan WIP** dan akun **Nilai penjualan pendapatan yang terkumpul** saat posting dilakukan.</span><span class="sxs-lookup"><span data-stu-id="f8195-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="f8195-112">Berikut adalah contoh dari metode ini.</span><span class="sxs-lookup"><span data-stu-id="f8195-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="f8195-113">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="f8195-113">Transaction type</span></span> | <span data-ttu-id="f8195-114">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="f8195-114">Debit/Credit</span></span> | <span data-ttu-id="f8195-115">Jumlah</span><span class="sxs-lookup"><span data-stu-id="f8195-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f8195-116">Nilai Penjualan WIP</span><span class="sxs-lookup"><span data-stu-id="f8195-116">WIP Sales value</span></span> | <span data-ttu-id="f8195-117">Debit</span><span class="sxs-lookup"><span data-stu-id="f8195-117">Debit</span></span> | <span data-ttu-id="f8195-118">100</span><span class="sxs-lookup"><span data-stu-id="f8195-118">100</span></span> |
  | <span data-ttu-id="f8195-119">pendapatan akrual - nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="f8195-119">Accrued revenue sales value</span></span> | <span data-ttu-id="f8195-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="f8195-120">Credit</span></span> | <span data-ttu-id="f8195-121">100</span><span class="sxs-lookup"><span data-stu-id="f8195-121">100</span></span> |

- <span data-ttu-id="f8195-122">Pendapatan direkognisi pada saat pembuatan faktur.</span><span class="sxs-lookup"><span data-stu-id="f8195-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="f8195-123">Sistem menggunakan akun **Pendapatan tertagih** pada saat diposting.</span><span class="sxs-lookup"><span data-stu-id="f8195-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="f8195-124">Berikut adalah contoh dari metode ini.</span><span class="sxs-lookup"><span data-stu-id="f8195-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="f8195-125">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="f8195-125">Transaction type</span></span> | <span data-ttu-id="f8195-126">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="f8195-126">Debit/Credit</span></span> | <span data-ttu-id="f8195-127">Jumlah</span><span class="sxs-lookup"><span data-stu-id="f8195-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f8195-128">Saldo pelanggan</span><span class="sxs-lookup"><span data-stu-id="f8195-128">Customer balance</span></span> | <span data-ttu-id="f8195-129">Debit</span><span class="sxs-lookup"><span data-stu-id="f8195-129">Debit</span></span> | <span data-ttu-id="f8195-130">120</span><span class="sxs-lookup"><span data-stu-id="f8195-130">120</span></span> |
  | <span data-ttu-id="f8195-131">Pajak penjualan untuk dibayarkan</span><span class="sxs-lookup"><span data-stu-id="f8195-131">Sales tax payable</span></span> | <span data-ttu-id="f8195-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="f8195-132">Credit</span></span> | <span data-ttu-id="f8195-133">20</span><span class="sxs-lookup"><span data-stu-id="f8195-133">20</span></span> |
  | <span data-ttu-id="f8195-134">Pendapatan Tertagih</span><span class="sxs-lookup"><span data-stu-id="f8195-134">Invoiced Revenue</span></span> | <span data-ttu-id="f8195-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="f8195-135">Credit</span></span> | <span data-ttu-id="f8195-136">100</span><span class="sxs-lookup"><span data-stu-id="f8195-136">100</span></span> |

- <span data-ttu-id="f8195-137">Jika pendapatan diperoleh saat penjualan yang belum ditagih diposting, sistem akan membalikkan pendapatan yang diperoleh pada faktur.</span><span class="sxs-lookup"><span data-stu-id="f8195-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="f8195-138">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="f8195-138">Transaction type</span></span> | <span data-ttu-id="f8195-139">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="f8195-139">Debit/Credit</span></span> | <span data-ttu-id="f8195-140">Jumlah</span><span class="sxs-lookup"><span data-stu-id="f8195-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="f8195-141">Nilai Penjualan WIP</span><span class="sxs-lookup"><span data-stu-id="f8195-141">WIP Sales value</span></span> | <span data-ttu-id="f8195-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="f8195-142">Credit</span></span> | <span data-ttu-id="f8195-143">100</span><span class="sxs-lookup"><span data-stu-id="f8195-143">100</span></span> |
  | <span data-ttu-id="f8195-144">pendapatan akrual - nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="f8195-144">Accrued revenue sales value</span></span> | <span data-ttu-id="f8195-145">Debit</span><span class="sxs-lookup"><span data-stu-id="f8195-145">Debit</span></span> | <span data-ttu-id="f8195-146">100</span><span class="sxs-lookup"><span data-stu-id="f8195-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="f8195-147">Transaksi yang dihitung menggunakan metode penagihan harga tetap</span><span class="sxs-lookup"><span data-stu-id="f8195-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="f8195-148">Pengakuan biaya dan pendapatan terpisah.</span><span class="sxs-lookup"><span data-stu-id="f8195-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="f8195-149">Biaya transaksi diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="f8195-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="f8195-150">Transaksi penjualan yang belum ditagih tidak dibuat.</span><span class="sxs-lookup"><span data-stu-id="f8195-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="f8195-151">Pendapatan dapat direkognisi saat pembuatan faktur jika biaya proyek dan profil pendapatan memiliki **Prinsip yang digunakan untuk penghitungan penyelesaian proyek** yang diatur ke **Tanpa WIP**.</span><span class="sxs-lookup"><span data-stu-id="f8195-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="f8195-152">Hanya gunakan metode ini untuk proyek jangka pendek dan sederhana.</span><span class="sxs-lookup"><span data-stu-id="f8195-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="f8195-153">Pendapatan dapat direkognisi menggunakan estimasi pendapatan harga tetap, baik dengan metode **Kontrak yang selesai** maupun **Persen penyelesaian pengakuan pendapatan**.</span><span class="sxs-lookup"><span data-stu-id="f8195-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8195-154">Sumber daya tambahan</span><span class="sxs-lookup"><span data-stu-id="f8195-154">Additional resources</span></span>
[<span data-ttu-id="f8195-155">Mengonfigurasikan akuntansi untuk artikel yang bisa ditagih</span><span class="sxs-lookup"><span data-stu-id="f8195-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="f8195-156">Proyek estimasi pendapatan harga tetap</span><span class="sxs-lookup"><span data-stu-id="f8195-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="f8195-157">Mengelola estimasi pendapatan</span><span class="sxs-lookup"><span data-stu-id="f8195-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="f8195-158">Metode biaya penyelesaian</span><span class="sxs-lookup"><span data-stu-id="f8195-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
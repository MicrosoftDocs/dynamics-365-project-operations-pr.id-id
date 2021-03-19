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
ms.openlocfilehash: 5e77a0442f634a50f8099fadec42ff400fee0e81
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278872"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="12b2b-103">Sekilas pengakuan pendapatan</span><span class="sxs-lookup"><span data-stu-id="12b2b-103">Revenue recognition overview</span></span>

<span data-ttu-id="12b2b-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="12b2b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="12b2b-105">Di Dynamics 365 Project Operations, prinsip pengakuan pendapatan bervariasi berdasarkan pada metode penagihan yang dipilih untuk proyek atau bagian dari proyek.</span><span class="sxs-lookup"><span data-stu-id="12b2b-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="12b2b-106">Topik ini berisi informasi tentang pengakuan pendapatan dalam Project Operations.</span><span class="sxs-lookup"><span data-stu-id="12b2b-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="12b2b-107">Transaksi yang dihitung menggunakan metode penagihan waktu dan material</span><span class="sxs-lookup"><span data-stu-id="12b2b-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="12b2b-108">Pengakuan biaya dan pendapatan terhubung.</span><span class="sxs-lookup"><span data-stu-id="12b2b-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="12b2b-109">Biaya transaksi dan penjualan yang belum ditagih diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="12b2b-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="12b2b-110">Biaya proyek dan profil pendapatan menentukan apakah transaksi penjualan yang belum ditagih diposting di buku besar.</span><span class="sxs-lookup"><span data-stu-id="12b2b-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="12b2b-111">Jika **Pendapatan yang terkumpul** dipilih, sistem menggunakan **Nilai penjualan WIP** dan akun **Nilai penjualan pendapatan yang terkumpul** saat posting dilakukan.</span><span class="sxs-lookup"><span data-stu-id="12b2b-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="12b2b-112">Berikut adalah contoh dari metode ini.</span><span class="sxs-lookup"><span data-stu-id="12b2b-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="12b2b-113">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="12b2b-113">Transaction type</span></span> | <span data-ttu-id="12b2b-114">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="12b2b-114">Debit/Credit</span></span> | <span data-ttu-id="12b2b-115">Jumlah</span><span class="sxs-lookup"><span data-stu-id="12b2b-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="12b2b-116">Nilai Penjualan WIP</span><span class="sxs-lookup"><span data-stu-id="12b2b-116">WIP Sales value</span></span> | <span data-ttu-id="12b2b-117">Debit</span><span class="sxs-lookup"><span data-stu-id="12b2b-117">Debit</span></span> | <span data-ttu-id="12b2b-118">100</span><span class="sxs-lookup"><span data-stu-id="12b2b-118">100</span></span> |
  | <span data-ttu-id="12b2b-119">pendapatan akrual - nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="12b2b-119">Accrued revenue sales value</span></span> | <span data-ttu-id="12b2b-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="12b2b-120">Credit</span></span> | <span data-ttu-id="12b2b-121">100</span><span class="sxs-lookup"><span data-stu-id="12b2b-121">100</span></span> |

- <span data-ttu-id="12b2b-122">Pendapatan direkognisi pada saat pembuatan faktur.</span><span class="sxs-lookup"><span data-stu-id="12b2b-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="12b2b-123">Sistem menggunakan akun **Pendapatan tertagih** pada saat diposting.</span><span class="sxs-lookup"><span data-stu-id="12b2b-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="12b2b-124">Berikut adalah contoh dari metode ini.</span><span class="sxs-lookup"><span data-stu-id="12b2b-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="12b2b-125">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="12b2b-125">Transaction type</span></span> | <span data-ttu-id="12b2b-126">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="12b2b-126">Debit/Credit</span></span> | <span data-ttu-id="12b2b-127">Jumlah</span><span class="sxs-lookup"><span data-stu-id="12b2b-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="12b2b-128">Saldo pelanggan</span><span class="sxs-lookup"><span data-stu-id="12b2b-128">Customer balance</span></span> | <span data-ttu-id="12b2b-129">Debit</span><span class="sxs-lookup"><span data-stu-id="12b2b-129">Debit</span></span> | <span data-ttu-id="12b2b-130">120</span><span class="sxs-lookup"><span data-stu-id="12b2b-130">120</span></span> |
  | <span data-ttu-id="12b2b-131">Pajak penjualan untuk dibayarkan</span><span class="sxs-lookup"><span data-stu-id="12b2b-131">Sales tax payable</span></span> | <span data-ttu-id="12b2b-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="12b2b-132">Credit</span></span> | <span data-ttu-id="12b2b-133">20</span><span class="sxs-lookup"><span data-stu-id="12b2b-133">20</span></span> |
  | <span data-ttu-id="12b2b-134">Pendapatan Tertagih</span><span class="sxs-lookup"><span data-stu-id="12b2b-134">Invoiced Revenue</span></span> | <span data-ttu-id="12b2b-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="12b2b-135">Credit</span></span> | <span data-ttu-id="12b2b-136">100</span><span class="sxs-lookup"><span data-stu-id="12b2b-136">100</span></span> |

- <span data-ttu-id="12b2b-137">Jika pendapatan diperoleh saat penjualan yang belum ditagih diposting, sistem akan membalikkan pendapatan yang diperoleh pada faktur.</span><span class="sxs-lookup"><span data-stu-id="12b2b-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="12b2b-138">Jenis transaksi</span><span class="sxs-lookup"><span data-stu-id="12b2b-138">Transaction type</span></span> | <span data-ttu-id="12b2b-139">Debit/Kredit</span><span class="sxs-lookup"><span data-stu-id="12b2b-139">Debit/Credit</span></span> | <span data-ttu-id="12b2b-140">Jumlah</span><span class="sxs-lookup"><span data-stu-id="12b2b-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="12b2b-141">Nilai Penjualan WIP</span><span class="sxs-lookup"><span data-stu-id="12b2b-141">WIP Sales value</span></span> | <span data-ttu-id="12b2b-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="12b2b-142">Credit</span></span> | <span data-ttu-id="12b2b-143">100</span><span class="sxs-lookup"><span data-stu-id="12b2b-143">100</span></span> |
  | <span data-ttu-id="12b2b-144">pendapatan akrual - nilai penjualan</span><span class="sxs-lookup"><span data-stu-id="12b2b-144">Accrued revenue sales value</span></span> | <span data-ttu-id="12b2b-145">Debit</span><span class="sxs-lookup"><span data-stu-id="12b2b-145">Debit</span></span> | <span data-ttu-id="12b2b-146">100</span><span class="sxs-lookup"><span data-stu-id="12b2b-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="12b2b-147">Transaksi yang dihitung menggunakan metode penagihan harga tetap</span><span class="sxs-lookup"><span data-stu-id="12b2b-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="12b2b-148">Pengakuan biaya dan pendapatan terpisah.</span><span class="sxs-lookup"><span data-stu-id="12b2b-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="12b2b-149">Biaya transaksi diposting menggunakan jurnal [Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="12b2b-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="12b2b-150">Transaksi penjualan yang belum ditagih tidak dibuat.</span><span class="sxs-lookup"><span data-stu-id="12b2b-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="12b2b-151">Pendapatan dapat direkognisi saat pembuatan faktur jika biaya proyek dan profil pendapatan memiliki **Prinsip yang digunakan untuk penghitungan penyelesaian proyek** yang diatur ke **Tanpa WIP**.</span><span class="sxs-lookup"><span data-stu-id="12b2b-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="12b2b-152">Hanya gunakan metode ini untuk proyek jangka pendek dan sederhana.</span><span class="sxs-lookup"><span data-stu-id="12b2b-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="12b2b-153">Pendapatan dapat direkognisi menggunakan estimasi pendapatan harga tetap, baik dengan metode **Kontrak yang selesai** maupun **Persen penyelesaian pengakuan pendapatan**.</span><span class="sxs-lookup"><span data-stu-id="12b2b-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="12b2b-154">Sumber daya tambahan</span><span class="sxs-lookup"><span data-stu-id="12b2b-154">Additional resources</span></span>
[<span data-ttu-id="12b2b-155">Mengonfigurasikan akuntansi untuk artikel yang bisa ditagih</span><span class="sxs-lookup"><span data-stu-id="12b2b-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="12b2b-156">Proyek estimasi pendapatan harga tetap</span><span class="sxs-lookup"><span data-stu-id="12b2b-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="12b2b-157">Mengelola estimasi pendapatan</span><span class="sxs-lookup"><span data-stu-id="12b2b-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="12b2b-158">Metode biaya penyelesaian</span><span class="sxs-lookup"><span data-stu-id="12b2b-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
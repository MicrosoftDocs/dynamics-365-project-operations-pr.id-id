---
title: Mengonfirmasikan faktur berbasis proyek proforma
description: Laporan topik memberikan informasi tentang mengkonfirmasikan faktur berbasis proyek proforma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012140"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="249bf-103">Mengonfirmasikan faktur berbasis proyek proforma</span><span class="sxs-lookup"><span data-stu-id="249bf-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="249bf-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="249bf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="249bf-105">Setelah faktur proforma dikonfirmasi, status faktur proyek diperbarui ke **Dikonfirmasi**.</span><span class="sxs-lookup"><span data-stu-id="249bf-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="249bf-106">Ketika faktur dikonfirmasi, itu menjadi baca-saja.</span><span class="sxs-lookup"><span data-stu-id="249bf-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="249bf-107">Selanjutnya, faktur hanya dapat diperbaiki jika ada koreksi atau kredit yang diawali pelanggan.</span><span class="sxs-lookup"><span data-stu-id="249bf-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="249bf-108">Tabel berikut ini mencantumkan aktual yang dibuat oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="249bf-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="249bf-109">Aktual ini dibuat ketika operasi tertentu dilakukan pada draf faktur proyek sebelum dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="249bf-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="249bf-110">
                    <strong>Skenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="249bf-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="249bf-111">
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="249bf-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-112">Faktur uang muka atau panjar</span><span class="sxs-lookup"><span data-stu-id="249bf-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-113">Jenis aktual penjualan yang ditagih, <strong>Panjar</strong> dibuat untuk jumlah uang muka atau panjar.</span><span class="sxs-lookup"><span data-stu-id="249bf-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-114">Aktual penjualan belum tertagih dengan jumlah negatif panjar atau uang muka yang akan digunakan untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="249bf-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-115">Setelah sepenuhnya merekonsiliasi panjar atau uang muka di faktur.</span><span class="sxs-lookup"><span data-stu-id="249bf-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-116">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="249bf-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="249bf-117">Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.</span><span class="sxs-lookup"><span data-stu-id="249bf-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-118">Aktual penjualan yang ditagih untuk jumlah pada faktur ini.</span><span class="sxs-lookup"><span data-stu-id="249bf-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="249bf-119">Setelah merekonsiliasi sebagian panjar atau uang muka di faktur.</span><span class="sxs-lookup"><span data-stu-id="249bf-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-120">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="249bf-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="249bf-121">Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.</span><span class="sxs-lookup"><span data-stu-id="249bf-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-122">Aktual penjualan yang ditagih untuk jumlah pada faktur ini.</span><span class="sxs-lookup"><span data-stu-id="249bf-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-123">Aktual penjualan negatif dari sisa jumlah panjar atau uang muka yang akan digunakan untuk rekonsiliasi di faktur mendatang.</span><span class="sxs-lookup"><span data-stu-id="249bf-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-124">Memfaktur transaksi waktu tanpa pengeditan pada faktur draf.</span><span class="sxs-lookup"><span data-stu-id="249bf-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-125">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-126">Aktual penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="249bf-127">Memfaktur transaksi waktu yang diedit untuk mengurangi kuantitas.</span><span class="sxs-lookup"><span data-stu-id="249bf-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-128">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-129">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-130">Aktual penjualan belum tertagih baru yang tidak dibebankan untuk jam dan jumlah yang tersisa setelah dikurangi angka yang diperbaiki pada detail baris faktur yang diedit, pembalikan aktual penjualan, dan aktual penjualan setara yang ditagih.</span><span class="sxs-lookup"><span data-stu-id="249bf-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-131">Memfaktur transaksi waktu yang diedit untuk meningkatkan kuantitas.</span><span class="sxs-lookup"><span data-stu-id="249bf-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-132">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-133">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-134">Memfaktur transaksi pengeluaran tanpa pengeditan pada faktur draf.</span><span class="sxs-lookup"><span data-stu-id="249bf-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-135">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-136">Aktual penjualan yang ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="249bf-137">Memfaktur transaksi pengeluaran yang diedit untuk mengurangi kuantitas.</span><span class="sxs-lookup"><span data-stu-id="249bf-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-138">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-139">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-140">Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa kuantitas dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-141">Memfaktur transaksi pengeluaran yang diedit untuk meningkatkan kuantitas.</span><span class="sxs-lookup"><span data-stu-id="249bf-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-142">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-143">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-144">Menagih transaksi bahan tanpa pengeditan pada draf faktur.</span><span class="sxs-lookup"><span data-stu-id="249bf-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-145">Pembalikan penjualan tak tertagih untuk kuantitas dan jumlah saat persetujuan penggunaan bahan asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-146">Aktual penjualan tertagih untuk kuantitas dan jumlah saat persetujuan penggunaan bahan asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="249bf-147">Menagih transaksi bahan yang diedit untuk mengurangi kuantitas.</span><span class="sxs-lookup"><span data-stu-id="249bf-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-148">Pembalikan penjualan tak tertagih untuk kuantitas dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-149">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-150">Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa kuantitas dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-151">Menagih transaksi bahan yang diedit untuk meningkatkan kuantitas.</span><span class="sxs-lookup"><span data-stu-id="249bf-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-152">Pembalikan penjualan tak tertagih untuk kuantitas dan jumlah saat persetujuan penggunaan bahan asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-153">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="249bf-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="249bf-154">Memfaktur ongkos.</span><span class="sxs-lookup"><span data-stu-id="249bf-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-155">Pembalikan penjualan yang belum ditagih untuk jumlah ongkos pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="249bf-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-156">Aktual penjualan yang ditagih untuk kuantitas dan jumlah pada baris jurnal ongkos asli.</span><span class="sxs-lookup"><span data-stu-id="249bf-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="249bf-157">Memfaktur tonggak pencapaian.</span><span class="sxs-lookup"><span data-stu-id="249bf-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="249bf-158">Aktual penjualan yang ditagih untuk jumlah tonggak pencapaian pada tonggak asli pada baris kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="249bf-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]

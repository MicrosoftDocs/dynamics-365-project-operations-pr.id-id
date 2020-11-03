---
title: Mengonfirmasikan faktur proforma
description: Topik ini memberikan informasi tentang mengonfirmasikan faktur proforma di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078392"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="b4328-103">Mengonfirmasikan faktur proforma</span><span class="sxs-lookup"><span data-stu-id="b4328-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="b4328-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="b4328-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b4328-105">Setelah faktur proforma dikonfirmasi, status faktur proyek diperbarui ke **Dikonfirmasi**.</span><span class="sxs-lookup"><span data-stu-id="b4328-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="b4328-106">Ketika faktur dikonfirmasi, itu menjadi baca-saja.</span><span class="sxs-lookup"><span data-stu-id="b4328-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="b4328-107">Ke depannya, faktur hanya dapat diperbaiki jika ada koreksi atau kredit yang dimulai pelanggan, atau jika faktur ditandai sebagai dibayar.</span><span class="sxs-lookup"><span data-stu-id="b4328-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="b4328-108">Tabel berikut ini mencantumkan aktual yang dibuat oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="b4328-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="b4328-109">Aktual ini dibuat ketika operasi tertentu dilakukan pada draf faktur proyek sebelum dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="b4328-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="b4328-110">
                    <strong>Skenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b4328-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="b4328-111">
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b4328-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b4328-112">Faktur uang muka atau panjar</span><span class="sxs-lookup"><span data-stu-id="b4328-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-113">Jenis aktual penjualan yang ditagih, <strong>Panjar</strong> dibuat untuk jumlah uang muka atau panjar.</span><span class="sxs-lookup"><span data-stu-id="b4328-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-114">Penjualan yang belum ditagih dari jumlah negatif panjar atau uang muka yang akan digunakan untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="b4328-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b4328-115">Setelah sepenuhnya merekonsiliasi panjar atau uang muka di faktur.</span><span class="sxs-lookup"><span data-stu-id="b4328-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-116">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="b4328-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b4328-117">Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.</span><span class="sxs-lookup"><span data-stu-id="b4328-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-118">Aktual penjualan yang ditagih untuk jumlah pada faktur ini.</span><span class="sxs-lookup"><span data-stu-id="b4328-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b4328-119">Setelah merekonsiliasi sebagian panjar atau uang muka di faktur.</span><span class="sxs-lookup"><span data-stu-id="b4328-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-120">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="b4328-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="b4328-121">Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.</span><span class="sxs-lookup"><span data-stu-id="b4328-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-122">Aktual penjualan yang ditagih untuk jumlah pada faktur ini.</span><span class="sxs-lookup"><span data-stu-id="b4328-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-123">Aktual penjualan negatif dari sisa jumlah panjar atau uang muka yang akan digunakan untuk rekonsiliasi di faktur mendatang.</span><span class="sxs-lookup"><span data-stu-id="b4328-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b4328-124">Memfaktur transaksi waktu tanpa pengeditan pada faktur draf.</span><span class="sxs-lookup"><span data-stu-id="b4328-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-125">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-126">Aktual penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b4328-127">Memfaktur transaksi waktu yang diedit untuk mengurangi kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b4328-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-128">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-129">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b4328-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-130">Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa jam dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b4328-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b4328-131">Memfaktur transaksi waktu yang diedit untuk meningkatkan kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b4328-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-132">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-133">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b4328-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b4328-134">Memfaktur transaksi pengeluaran tanpa pengeditan pada faktur draf.</span><span class="sxs-lookup"><span data-stu-id="b4328-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-135">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-136">Aktual penjualan yang ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli</span><span class="sxs-lookup"><span data-stu-id="b4328-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b4328-137">Memfaktur transaksi pengeluaran yang diedit untuk mengurangi kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b4328-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-138">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-139">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b4328-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-140">Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa kuantitas dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b4328-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b4328-141">Memfaktur transaksi pengeluaran yang diedit untuk meningkatkan kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b4328-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-142">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-143">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b4328-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b4328-144">Memfaktur ongkos.</span><span class="sxs-lookup"><span data-stu-id="b4328-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-145">Pembalikan penjualan yang belum ditagih untuk jumlah ongkos pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="b4328-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-146">Aktual penjualan yang ditagih untuk kuantitas dan jumlah pada baris jurnal ongkos asli.</span><span class="sxs-lookup"><span data-stu-id="b4328-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b4328-147">Memfaktur tonggak pencapaian.</span><span class="sxs-lookup"><span data-stu-id="b4328-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-148">Aktual penjualan yang ditagih untuk jumlah tonggak pencapaian pada tonggak asli pada baris kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="b4328-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b4328-149">Memfaktur baris kontrak berbasis produk.</span><span class="sxs-lookup"><span data-stu-id="b4328-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b4328-150">Aktual penjualan yang ditagihkan untuk baris produk dengan kuantitas dan jumlah yang berasal dari baris kontrak berbasis produk.</span><span class="sxs-lookup"><span data-stu-id="b4328-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>

---
title: Faktur koreksi - lite
description: Topik ini memberikan informasi tentang mengonfirmasikan faktur yang dikoreksi di Project Operations
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: eb949ff3a53bcba19d44e1c3d6fe08a6b368108d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274237"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="5bbe2-103">Faktur koreksi - lite</span><span class="sxs-lookup"><span data-stu-id="5bbe2-103">Corrected invoices - lite</span></span>

<span data-ttu-id="5bbe2-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="5bbe2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5bbe2-105">Faktur proyek yang dikonfirmasi dapat diperbaiki untuk memproses perubahan atau kredit seperti yang dinegosiasikan dengan pelanggan dan manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="5bbe2-106">Untuk melakukan pengeditan pada faktur yang dikonfirmasi, buka faktur yang dikonfirmasi dan pilih **Perbaiki Faktur ini**.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="5bbe2-107">Pilihan ini tidak tersedia kecuali faktur proyek dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="5bbe2-108">Faktur draf baru dibuat dari faktur yang dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="5bbe2-109">Semua detail baris faktur dari faktur yang dikonfirmasi sebelumnya disalin ke draf baru.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="5bbe2-110">Berikut ini adalah beberapa poin penting untuk dipahami tentang detail baris pada faktur baru yang dikoreksi:</span><span class="sxs-lookup"><span data-stu-id="5bbe2-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="5bbe2-111">Semua kuantitas diperbarui ke nol.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-111">All quantities are updated to zero.</span></span> <span data-ttu-id="5bbe2-112">Aplikasi ini mengasumsikan bahwa semua item yang ditagih sepenuhnya dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="5bbe2-113">Jika diperlukan, Anda dapat memperbarui jumlah ini secara manual untuk mencerminkan kuantitas yang sedang ditagih, dan bukan kuantitas yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="5bbe2-114">Berdasarkan kuantitas yang Anda masukkan, aplikasi menghitung jumlah yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="5bbe2-115">Jumlah ini tercermin dalam aktual yang dibuat ketika faktur yang dikoreksi dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="5bbe2-116">Jika Anda membuat perubahan pada jumlah pajak, Anda harus memasukkan jumlah pajak yang benar dan bukan jumlah pajak yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="5bbe2-117">Baris kontrak berbasis produk yang dikonfirmasi sebelumnya tidak disalin.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="5bbe2-118">Memproses koreksi pada faktur proyek berbasis produk tidak didukung.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="5bbe2-119">Koreksi tonggak pencapaian selalu diproses sebagai kredit penuh.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="5bbe2-120">Panjar atau jumlah uang muka dapat diperbaiki jika pelanggan ditagih dengan jumlah yang salah.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="5bbe2-121">Rekonsiliasi panjar dan uang muka dapat diperbaiki jika jumlah yang salah digunakan untuk merekonsiliasi terhadap biaya pada faktur yang dikonfirmasi sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5bbe2-122">Detail baris faktur yang merupakan koreksi biaya lain yang sudah ditagih memiliki bidang **Koreksi** yang diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="5bbe2-123">Faktur yang telah memperbaiki detail baris faktur memiliki bidang yang disebut **Memiliki koreksi** yang juga diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="5bbe2-124">Aktual yang dibuat pada Konfirmasi faktur korektif:</span><span class="sxs-lookup"><span data-stu-id="5bbe2-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="5bbe2-125">Di bawah ini adalah aktual yang dibuat oleh aplikasi pada konfirmasi korektif berdasarkan operasi yang dilakukan pada draf faktur korektif sebelum konfirmasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="5bbe2-126">
                    <strong>Skenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bbe2-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="5bbe2-127">
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bbe2-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="5bbe2-128">Konfirmasikan koreksi terhadap uang muka atau panjar yang ditagih.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="5bbe2-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-129">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5bbe2-130">Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-131">Aktual pembalikan penjualan yang ditagih dibuat untuk jumlah pada panjar atau uang muka untuk membalikkan penjualan asli yang ditagih.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-132">Aktual penjualan baru yang ditagih dibuat untuk jumlah yang dikoreksi di baris faktur yang dikoreksi berbasis uang muka atau panjar.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-133">Aktual penjualan yang belum ditagih dari baris faktur yang dikoreksi berbasis jumlah negatif panjar atau uang muka yang akan digunakan untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="5bbe2-134">Konfirmasi tentang koreksi panjar atau uang muka yang sebelumnya direkonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-135">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="5bbe2-136">Jumlah ini positif dan dimaksudkan untuk membatalkan negatif yang dibuat ketika rekonsiliasi sebelumnya terjadi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-137">Aktual pembalikan penjualan yang ditagih untuk jumlah pada faktur sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-138">Aktual penjualan baru yang ditagih untuk jumlah panjar yang dikoreksi yang diterapkan pada faktur yang dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-139">Aktual yang belum ditagih dengan jumlah negatif dari panjar atau uang muka tersisa yang dikoreksi, yang akan digunakan untuk rekonsiliasi pada faktur mendatang.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bbe2-140">Menagih kredit penuh dari transaksi waktu yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-141">Pembalikan penjualan yang ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-142">Aktual penjualan baru yang belum ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5bbe2-143">Memfaktur kredit parsial pada transaksi waktu.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-144">Pembalikan penjualan yang ditagih untuk jam dan jumlah yang ditagih pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-145">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-146">Aktual penjualan baru yang belum ditagih yang kena biaya untuk jam dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bbe2-147">Menagih kredit penuh dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-148">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-149">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="5bbe2-150">Menagih kredit parsial dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-151">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-152">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang dikoreksi, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-153">Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bbe2-154">Menagih kredit penuh dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-155">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-156">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="5bbe2-157">Menagih kredit parsial dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-158">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-159">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur koreksi yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5bbe2-160">Menagih kredit penuh dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-161">Pembalikan penjualan yang ditagih untuk jumlah pada detail baris faktur asli untuk tonggak pencapaian.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="5bbe2-162">Faktur tonggak pencapaian atau status penagihan pada baris kontrak proyek diperbarui untuk **siap faktur**.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5bbe2-163">Menagih kredit parsial dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-164">Tidak Didukung</span><span class="sxs-lookup"><span data-stu-id="5bbe2-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="5bbe2-165">Kredit dan koreksi baris kontrak berbasis produk yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="5bbe2-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="5bbe2-166">Tidak Didukung</span><span class="sxs-lookup"><span data-stu-id="5bbe2-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
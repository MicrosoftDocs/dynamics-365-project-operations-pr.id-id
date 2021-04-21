---
title: Membuat faktur koreksi
description: Laporan topik memberikan informasi tentang cara membuat dan mengkonfirmasikan faktur perbaikan di Project Operations.
author: rumant
manager: Annbe
ms.date: 04/05/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ae6d881e4e68b9f467478afe9735fc3186e6b0a8
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866595"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="9368d-103">Membuat faktur koreksi</span><span class="sxs-lookup"><span data-stu-id="9368d-103">Corrective project invoices</span></span>

<span data-ttu-id="9368d-104">_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_</span><span class="sxs-lookup"><span data-stu-id="9368d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9368d-105">Faktur proyek yang dikonfirmasi dapat diperbaiki untuk memproses perubahan atau kredit seperti yang dinegosiasikan dengan pelanggan dan manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="9368d-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="9368d-106">Untuk melakukan pengeditan pada faktur yang dikonfirmasi, buka faktur yang dikonfirmasi dan pilih **Perbaiki Faktur ini**.</span><span class="sxs-lookup"><span data-stu-id="9368d-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="9368d-107">Pilihan ini tidak tersedia kecuali faktur proyek dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="9368d-108">Faktur draf baru dibuat dari faktur yang dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="9368d-109">Semua detail baris faktur dari faktur yang dikonfirmasi sebelumnya disalin ke draf baru.</span><span class="sxs-lookup"><span data-stu-id="9368d-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="9368d-110">Berikut ini adalah beberapa poin penting untuk dipahami tentang detail baris pada faktur baru yang dikoreksi:</span><span class="sxs-lookup"><span data-stu-id="9368d-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="9368d-111">Semua kuantitas diperbarui ke nol.</span><span class="sxs-lookup"><span data-stu-id="9368d-111">All quantities are updated to zero.</span></span> <span data-ttu-id="9368d-112">Aplikasi ini mengasumsikan bahwa semua item yang ditagih sepenuhnya dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="9368d-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="9368d-113">Jika diperlukan, Anda dapat memperbarui jumlah ini secara manual untuk mencerminkan kuantitas yang sedang ditagih, dan bukan kuantitas yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="9368d-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="9368d-114">Berdasarkan kuantitas yang Anda masukkan, aplikasi menghitung jumlah yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="9368d-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="9368d-115">Jumlah ini tercermin dalam aktual yang dibuat ketika faktur yang dikoreksi dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="9368d-116">Jika Anda membuat perubahan pada jumlah pajak, Anda harus memasukkan jumlah pajak yang benar dan bukan jumlah pajak yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="9368d-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="9368d-117">Baris kontrak berbasis produk yang dikonfirmasi sebelumnya tidak disalin.</span><span class="sxs-lookup"><span data-stu-id="9368d-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="9368d-118">Memproses koreksi pada faktur proyek berbasis produk tidak didukung.</span><span class="sxs-lookup"><span data-stu-id="9368d-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="9368d-119">Koreksi tonggak pencapaian selalu diproses sebagai kredit penuh.</span><span class="sxs-lookup"><span data-stu-id="9368d-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="9368d-120">Panjar atau jumlah uang muka dapat diperbaiki jika pelanggan ditagih dengan jumlah yang salah.</span><span class="sxs-lookup"><span data-stu-id="9368d-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="9368d-121">Rekonsiliasi panjar dan uang muka dapat diperbaiki jika jumlah yang salah digunakan untuk merekonsiliasi terhadap biaya pada faktur yang dikonfirmasi sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9368d-122">Detail baris faktur yang merupakan koreksi biaya lain yang sudah ditagih memiliki bidang **Koreksi** yang diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="9368d-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="9368d-123">Faktur yang telah memperbaiki detail baris faktur memiliki bidang yang disebut **Memiliki koreksi** yang juga diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="9368d-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="9368d-124">Aktual yang dibuat ketika faktur korektif dikonfirmasi</span><span class="sxs-lookup"><span data-stu-id="9368d-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="9368d-125">Tabel berikut berisi daftar aktual yang dibuat saat faktur perbaikan dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9368d-126">
                    <strong>Skenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9368d-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9368d-127">
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9368d-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9368d-128">Konfirmasikan koreksi terhadap uang muka atau panjar yang ditagih.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="9368d-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-129">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9368d-130">Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.</span><span class="sxs-lookup"><span data-stu-id="9368d-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-131">Aktual pembalikan penjualan yang ditagih dibuat untuk jumlah pada panjar atau uang muka untuk membalikkan penjualan asli yang ditagih.</span><span class="sxs-lookup"><span data-stu-id="9368d-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-132">Aktual penjualan baru yang ditagih dibuat untuk jumlah yang dikoreksi di baris faktur yang dikoreksi berbasis uang muka atau panjar.</span><span class="sxs-lookup"><span data-stu-id="9368d-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-133">Aktual penjualan yang belum ditagih dari baris faktur yang dikoreksi berbasis jumlah negatif panjar atau uang muka yang akan digunakan untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="9368d-134">Konfirmasi tentang koreksi panjar atau uang muka yang sebelumnya direkonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-135">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="9368d-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9368d-136">Jumlah ini positif dan dimaksudkan untuk membatalkan negatif yang dibuat ketika rekonsiliasi sebelumnya terjadi.</span><span class="sxs-lookup"><span data-stu-id="9368d-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-137">Aktual pembalikan penjualan yang ditagih untuk jumlah pada faktur sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-138">Aktual penjualan baru yang ditagih untuk jumlah panjar yang dikoreksi yang diterapkan pada faktur yang dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="9368d-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-139">Aktual yang belum ditagih dengan jumlah negatif dari panjar atau uang muka tersisa yang dikoreksi, yang akan digunakan untuk rekonsiliasi pada faktur mendatang.</span><span class="sxs-lookup"><span data-stu-id="9368d-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9368d-140">Menagih kredit penuh dari transaksi waktu yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-141">Pembalikan penjualan yang ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="9368d-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-142">Aktual penjualan baru yang belum ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="9368d-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9368d-143">Memfaktur kredit parsial pada transaksi waktu.</span><span class="sxs-lookup"><span data-stu-id="9368d-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-144">Pembalikan penjualan yang ditagih untuk jam dan jumlah yang ditagih pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="9368d-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-145">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="9368d-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-146">Aktual penjualan baru yang belum ditagih yang kena biaya untuk jam dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="9368d-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9368d-147">Menagih kredit penuh dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-148">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="9368d-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-149">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="9368d-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9368d-150">Menagih kredit parsial dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-151">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="9368d-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-152">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang dikoreksi, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="9368d-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-153">Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="9368d-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9368d-154">Menagih kredit penuh dari transaksi bahan yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-155">Pembalikan penjualan tertagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="9368d-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-156">Aktual penjualan tak tertagih baru untuk kuantitas dan jumlah pada detail baris faktur asli untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="9368d-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9368d-157">Menagih kredit parsial pada transaksi bahan.</span><span class="sxs-lookup"><span data-stu-id="9368d-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-158">Pembalikan penjualan tertagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="9368d-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-159">Aktual penjualan belum teragih baru yang dibebankan untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikannya, dan aktual penjualan tertagih setara.</span><span class="sxs-lookup"><span data-stu-id="9368d-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-160">Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="9368d-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9368d-161">Menagih kredit penuh dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-162">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="9368d-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-163">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="9368d-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9368d-164">Menagih kredit parsial dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-165">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="9368d-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-166">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur koreksi yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="9368d-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9368d-167">Menagih kredit penuh dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-168">Pembalikan penjualan yang ditagih untuk jumlah pada detail baris faktur asli untuk tonggak pencapaian.</span><span class="sxs-lookup"><span data-stu-id="9368d-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="9368d-169">Status faktur pada tonggak pencapaian diperbarui dari <b>faktur Pelanggan diposting</b> ke <b>Siap untuk Faktur</b>.</span><span class="sxs-lookup"><span data-stu-id="9368d-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9368d-170">Menagih kredit parsial dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-171">Tidak Didukung</span><span class="sxs-lookup"><span data-stu-id="9368d-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9368d-172">Kredit dan koreksi baris kontrak berbasis produk yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="9368d-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9368d-173">Tidak Didukung</span><span class="sxs-lookup"><span data-stu-id="9368d-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

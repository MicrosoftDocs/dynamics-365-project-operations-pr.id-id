---
title: Membuat koreksi faktur berbasis proyek
description: Laporan topik memberikan informasi tentang faktur koreksi di Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788866"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="10e70-103">Membuat koreksi faktur berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="10e70-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="10e70-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="10e70-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="10e70-105">Faktur proyek yang dikonfirmasi dapat diperbaiki untuk memproses perubahan atau kredit seperti yang dinegosiasikan dengan pelanggan dan manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="10e70-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="10e70-106">Untuk melakukan pengeditan pada faktur yang dikonfirmasi, buka faktur yang dikonfirmasi dan pilih **Perbaiki Faktur ini**.</span><span class="sxs-lookup"><span data-stu-id="10e70-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="10e70-107">Pilihan ini tidak tersedia kecuali faktur proyek dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="10e70-108">Faktur draf baru dibuat dari faktur yang dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="10e70-109">Semua detail baris faktur dari faktur yang dikonfirmasi sebelumnya disalin ke draf baru.</span><span class="sxs-lookup"><span data-stu-id="10e70-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="10e70-110">Berikut ini adalah beberapa poin penting untuk membantu Anda memahami lebih lanjut tentang rincian baris pada faktur dikoreksi yang baru:</span><span class="sxs-lookup"><span data-stu-id="10e70-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="10e70-111">Semua kuantitas diperbarui ke nol.</span><span class="sxs-lookup"><span data-stu-id="10e70-111">All quantities are updated to zero.</span></span> <span data-ttu-id="10e70-112">Hal ini mengasumsikan bahwa semua item ditagih sepenuhnya dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="10e70-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="10e70-113">Jika diperlukan, Anda dapat memperbarui jumlah ini secara manual untuk mencerminkan kuantitas yang sedang ditagih, dan bukan kuantitas yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="10e70-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="10e70-114">Berdasarkan kuantitas yang Anda masukkan, aplikasi menghitung jumlah yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="10e70-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="10e70-115">Jumlah ini tercermin dalam aktual yang dibuat ketika faktur yang dikoreksi dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="10e70-116">Jika Anda membuat perubahan pada jumlah pajak, Anda harus memasukkan jumlah pajak yang benar dan bukan jumlah pajak yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="10e70-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="10e70-117">Koreksi tonggak pencapaian selalu diproses sebagai kredit penuh.</span><span class="sxs-lookup"><span data-stu-id="10e70-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="10e70-118">Panjar atau jumlah uang muka dapat diperbaiki jika pelanggan ditagih dengan jumlah yang salah.</span><span class="sxs-lookup"><span data-stu-id="10e70-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="10e70-119">Rekonsiliasi panjar dan uang muka dapat diperbaiki jika jumlah yang salah digunakan untuk merekonsiliasi terhadap biaya pada faktur yang dikonfirmasi sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10e70-120">Rincian baris faktur yang merupakan koreksi terhadap tagihan yang sudah ditagih memiliki bidang **Koreksi** yang diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="10e70-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="10e70-121">Faktur yang telah memperbaiki detail baris faktur memiliki bidang yang disebut **Memiliki koreksi** yang juga diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="10e70-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="10e70-122">Aktual yang dibuat pada Konfirmasi faktur korektif</span><span class="sxs-lookup"><span data-stu-id="10e70-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="10e70-123">Tabel berikut berisi daftar aktual yang dibuat saat faktur perbaikan dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="10e70-124">
                    <strong>Skenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10e70-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="10e70-125">
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10e70-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="10e70-126">Konfirmasikan koreksi terhadap uang muka atau panjar yang ditagih.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="10e70-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-127">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="10e70-128">Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.</span><span class="sxs-lookup"><span data-stu-id="10e70-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-129">Aktual pembalikan penjualan yang ditagih dibuat untuk jumlah pada panjar atau uang muka untuk membalikkan penjualan asli yang ditagih.</span><span class="sxs-lookup"><span data-stu-id="10e70-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-130">Aktual penjualan baru yang ditagih dibuat untuk jumlah yang dikoreksi di baris faktur yang dikoreksi berbasis uang muka atau panjar.</span><span class="sxs-lookup"><span data-stu-id="10e70-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-131">Aktual penjualan yang belum ditagih dari baris faktur yang dikoreksi berbasis jumlah negatif panjar atau uang muka yang akan digunakan untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="10e70-132">Konfirmasi tentang koreksi panjar atau uang muka yang sebelumnya direkonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-133">Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi.</span><span class="sxs-lookup"><span data-stu-id="10e70-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="10e70-134">Jumlah ini positif dan dimaksudkan untuk membatalkan negatif yang dibuat ketika rekonsiliasi sebelumnya terjadi.</span><span class="sxs-lookup"><span data-stu-id="10e70-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-135">Aktual pembalikan penjualan yang ditagih untuk jumlah pada faktur sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-136">Aktual penjualan baru yang ditagih untuk jumlah panjar yang dikoreksi yang diterapkan pada faktur yang dikoreksi.</span><span class="sxs-lookup"><span data-stu-id="10e70-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-137">Aktual yang belum ditagih dengan jumlah negatif dari panjar atau uang muka tersisa yang dikoreksi, yang akan digunakan untuk rekonsiliasi pada faktur mendatang.</span><span class="sxs-lookup"><span data-stu-id="10e70-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10e70-138">Menagih kredit penuh dari transaksi waktu yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-139">Pembalikan penjualan yang ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="10e70-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-140">Aktual penjualan baru yang belum ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="10e70-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10e70-141">Memfaktur kredit parsial pada transaksi waktu.</span><span class="sxs-lookup"><span data-stu-id="10e70-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-142">Pembalikan penjualan yang ditagih untuk jam dan jumlah yang ditagih pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="10e70-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-143">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="10e70-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-144">Aktual penjualan baru yang belum ditagih yang kena biaya untuk jam dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="10e70-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10e70-145">Menagih kredit penuh dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-146">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="10e70-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-147">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="10e70-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10e70-148">Menagih kredit parsial dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-149">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="10e70-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-150">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang dikoreksi, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="10e70-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-151">Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="10e70-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10e70-152">Menagih kredit penuh dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-153">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="10e70-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-154">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="10e70-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10e70-155">Menagih kredit parsial dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-156">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="10e70-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-157">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur koreksi yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="10e70-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="10e70-158">Menagih kredit penuh dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-159">Pembalikan penjualan yang ditagih untuk jumlah pada detail baris faktur asli untuk tonggak pencapaian.</span><span class="sxs-lookup"><span data-stu-id="10e70-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="10e70-160">Status faktur pada tonggak pencapaian diperbarui dari <b>faktur Pelanggan diposting</b> ke <b>Siap untuk Faktur</b>.</span><span class="sxs-lookup"><span data-stu-id="10e70-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="10e70-161">Menagih kredit parsial dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="10e70-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10e70-162">Tidak Didukung</span><span class="sxs-lookup"><span data-stu-id="10e70-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Koreksi faktur berbasis proyek
description: Laporan topik memberikan informasi tentang cara membuat dan mengkonfirmasikan faktur berbasis proyek perbaikan di Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867045"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="e2db8-103">Koreksi faktur berbasis proyek</span><span class="sxs-lookup"><span data-stu-id="e2db8-103">Corrective project-based invoices</span></span>

<span data-ttu-id="e2db8-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="e2db8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e2db8-105">Faktur proyek yang dikonfirmasi dapat diperbaiki untuk memproses perubahan atau kredit seperti yang dinegosiasikan dengan pelanggan dan manajer proyek.</span><span class="sxs-lookup"><span data-stu-id="e2db8-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="e2db8-106">Untuk melakukan pengeditan pada faktur yang dikonfirmasi, buka faktur yang dikonfirmasi dan pilih **Perbaiki Faktur ini**.</span><span class="sxs-lookup"><span data-stu-id="e2db8-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="e2db8-107">Pilihan ini tidak tersedia, kecuali jika faktur proyek dikonfirmasi atau faktur berbasis proyek memiliki uang muka atau panjar atau rekonsiliasi uang muka atau panjar.</span><span class="sxs-lookup"><span data-stu-id="e2db8-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="e2db8-108">Faktur draf baru dibuat dari faktur yang dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="e2db8-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="e2db8-109">Semua detail baris faktur dari faktur yang dikonfirmasi sebelumnya disalin ke draf baru.</span><span class="sxs-lookup"><span data-stu-id="e2db8-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="e2db8-110">Berikut ini adalah beberapa poin penting untuk dipahami tentang detail baris pada faktur baru yang dikoreksi:</span><span class="sxs-lookup"><span data-stu-id="e2db8-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="e2db8-111">Semua kuantitas diperbarui ke nol.</span><span class="sxs-lookup"><span data-stu-id="e2db8-111">All quantities are updated to zero.</span></span> <span data-ttu-id="e2db8-112">Dynamics 365 Project Operations mengasumsikan bahwa semua item ditagih sepenuhnya dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="e2db8-113">Jika diperlukan, Anda dapat memperbarui jumlah ini secara manual untuk mencerminkan kuantitas yang sedang ditagih, dan bukan kuantitas yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="e2db8-114">Berdasarkan kuantitas yang Anda masukkan, aplikasi menghitung jumlah yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="e2db8-115">Jumlah ini tercermin dalam aktual yang dibuat ketika faktur yang dikoreksi dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="e2db8-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="e2db8-116">Jika Anda membuat perubahan pada jumlah pajak, Anda harus memasukkan jumlah pajak yang benar dan bukan jumlah pajak yang dikreditkan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="e2db8-117">Koreksi tonggak pencapaian selalu diproses sebagai kredit penuh.</span><span class="sxs-lookup"><span data-stu-id="e2db8-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="e2db8-118">Untuk rincian baris faktur yang merupakan koreksi terhadap tagihan yang sudah ditagih, bidang **Koreksi** diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="e2db8-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="e2db8-119">Untuk faktur yang memiliki rincian baris faktur koreksi, bidang **Memiliki Koreksi** diatur ke **Ya**.</span><span class="sxs-lookup"><span data-stu-id="e2db8-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="e2db8-120">Aktual yang dibuat ketika faktur korektif dikonfirmasi</span><span class="sxs-lookup"><span data-stu-id="e2db8-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="e2db8-121">Tabel berikut berisi daftar aktual yang dibuat saat faktur perbaikan dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="e2db8-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="e2db8-122">
                    <strong>Skenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2db8-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="e2db8-123">
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e2db8-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2db8-124">Menagih kredit penuh dari transaksi waktu yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-125">Pembalikan penjualan yang ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="e2db8-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-126">Aktual penjualan baru yang belum ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="e2db8-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e2db8-127">Memfaktur kredit parsial pada transaksi waktu.</span><span class="sxs-lookup"><span data-stu-id="e2db8-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-128">Pembalikan penjualan yang ditagih untuk jam dan jumlah yang ditagih pada detail baris faktur asli untuk waktu.</span><span class="sxs-lookup"><span data-stu-id="e2db8-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-129">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="e2db8-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-130">Aktual penjualan baru yang belum ditagih yang kena biaya untuk jam dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="e2db8-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2db8-131">Menagih kredit penuh dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-132">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="e2db8-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-133">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="e2db8-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e2db8-134">Menagih kredit parsial dari transaksi pengeluaran yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-135">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk pengeluaran.</span><span class="sxs-lookup"><span data-stu-id="e2db8-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-136">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang dikoreksi, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="e2db8-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-137">Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="e2db8-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2db8-138">Menagih kredit penuh dari transaksi bahan yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-139">Pembalikan penjualan tertagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-140">Aktual penjualan tak tertagih baru untuk kuantitas dan jumlah pada detail baris faktur asli untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="e2db8-141">Menagih kredit parsial pada transaksi bahan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-142">Pembalikan penjualan tertagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk bahan.</span><span class="sxs-lookup"><span data-stu-id="e2db8-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-143">Aktual penjualan belum teragih baru yang dibebankan untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikannya, dan aktual penjualan tertagih setara.</span><span class="sxs-lookup"><span data-stu-id="e2db8-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-144">Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.</span><span class="sxs-lookup"><span data-stu-id="e2db8-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2db8-145">Menagih kredit penuh dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-146">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="e2db8-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-147">Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="e2db8-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e2db8-148">Menagih kredit parsial dari transaksi ongkos yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-149">Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk ongkos.</span><span class="sxs-lookup"><span data-stu-id="e2db8-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-150">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur koreksi yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="e2db8-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e2db8-151">Menagih kredit penuh dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-152">Pembalikan penjualan yang ditagih untuk jumlah pada detail baris faktur asli untuk tonggak pencapaian.</span><span class="sxs-lookup"><span data-stu-id="e2db8-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="e2db8-153">Status faktur pada tonggak pencapaian diperbarui dari <b>faktur Pelanggan diposting</b> ke <b>Siap untuk Faktur</b>.</span><span class="sxs-lookup"><span data-stu-id="e2db8-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="e2db8-154">Menagih kredit parsial dari tonggak pencapaian yang ditagih sebelumnya.</span><span class="sxs-lookup"><span data-stu-id="e2db8-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="e2db8-155">Skenario ini tidak didukung.</span><span class="sxs-lookup"><span data-stu-id="e2db8-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

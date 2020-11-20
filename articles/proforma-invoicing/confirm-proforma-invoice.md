---
title: Mengonfirmasikan faktur proforma
description: Topik ini menyediakan informasi tentang mengkonfirmasi faktur proforma.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128107"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="b0cd6-103">Mengonfirmasikan faktur proforma</span><span class="sxs-lookup"><span data-stu-id="b0cd6-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="b0cd6-104">_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_</span><span class="sxs-lookup"><span data-stu-id="b0cd6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b0cd6-105">Setelah faktur proforma dikonfirmasi, status faktur proyek diperbarui ke **Dikonfirmasi**.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="b0cd6-106">Ketika faktur dikonfirmasi, itu menjadi baca-saja.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="b0cd6-107">Ke depannya, faktur hanya dapat diperbaiki jika ada koreksi atau kredit yang dimulai pelanggan, atau ketika ditandai sebagai dibayar.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="b0cd6-108">Tabel berikut ini mencantumkan aktual yang dibuat oleh sistem.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="b0cd6-109">Aktual ini dibuat ketika operasi tertentu dilakukan pada draf faktur proyek sebelum dikonfirmasi.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="b0cd6-110">
                    <strong>Skenario</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0cd6-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="b0cd6-111">
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0cd6-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b0cd6-112">Memfaktur transaksi waktu tanpa pengeditan pada faktur draf.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-113">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-114">Aktual penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b0cd6-115">Memfaktur transaksi waktu yang diedit untuk mengurangi kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-116">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-117">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-118">Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa jam dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b0cd6-119">Memfaktur transaksi waktu yang diedit untuk meningkatkan kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-120">Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-121">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b0cd6-122">Memfaktur transaksi pengeluaran tanpa pengeditan pada faktur draf.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-123">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-124">Aktual penjualan yang ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b0cd6-125">Memfaktur transaksi pengeluaran yang diedit untuk mengurangi kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-126">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-127">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-128">Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa kuantitas dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b0cd6-129">Memfaktur transaksi pengeluaran yang diedit untuk meningkatkan kuantitas.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-130">Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-131">Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b0cd6-132">Memfaktur ongkos.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-133">Pembalikan penjualan yang belum ditagih untuk jumlah ongkos pada baris jurnal.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-134">Aktual penjualan yang ditagih untuk kuantitas dan jumlah pada baris jurnal ongkos asli.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b0cd6-135">Memfaktur tonggak pencapaian.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b0cd6-136">Aktual penjualan yang ditagih untuk jumlah tonggak pencapaian pada tonggak asli pada baris kontrak proyek.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>

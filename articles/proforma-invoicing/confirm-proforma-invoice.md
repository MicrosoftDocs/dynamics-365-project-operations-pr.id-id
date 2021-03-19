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
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287872"
---
# <a name="confirm-a-proforma-invoice"></a>Mengonfirmasikan faktur proforma

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Setelah faktur proforma dikonfirmasi, status faktur proyek diperbarui ke **Dikonfirmasi**. Ketika faktur dikonfirmasi, itu menjadi baca-saja. Ke depannya, faktur hanya dapat diperbaiki jika ada koreksi atau kredit yang dimulai pelanggan, atau ketika ditandai sebagai dibayar.

Tabel berikut ini mencantumkan aktual yang dibuat oleh sistem. Aktual ini dibuat ketika operasi tertentu dilakukan pada draf faktur proyek sebelum dikonfirmasi.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>Skenario</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Memfaktur transaksi waktu tanpa pengeditan pada faktur draf.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Memfaktur transaksi waktu yang diedit untuk mengurangi kuantitas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa jam dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Memfaktur transaksi waktu yang diedit untuk meningkatkan kuantitas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang belum ditagih untuk jam dan jumlah saat persetujuan waktu asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Memfaktur transaksi pengeluaran tanpa pengeditan pada faktur draf.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Memfaktur transaksi pengeluaran yang diedit untuk mengurangi kuantitas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara. 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa kuantitas dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Memfaktur transaksi pengeluaran yang diedit untuk meningkatkan kuantitas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang belum ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan yang belum ditagih, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Memfaktur ongkos.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang belum ditagih untuk jumlah ongkos pada baris jurnal.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang ditagih untuk kuantitas dan jumlah pada baris jurnal ongkos asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Memfaktur tonggak pencapaian.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang ditagih untuk jumlah tonggak pencapaian pada tonggak asli pada baris kontrak proyek.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
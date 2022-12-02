---
title: Mengonfirmasikan faktur proyek proforma
description: Artikel ini memberikan informasi tentang mengkonfirmasikan faktur proyek di Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 101e4564fcf57cbbfc713773ed760291b9d28410
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922226"
---
# <a name="confirm-a-proforma-project-invoice"></a>Mengonfirmasikan faktur proyek proforma 

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Setelah faktur proforma dikonfirmasi, status faktur proyek diperbarui ke **Dikonfirmasi**. Ketika faktur dikonfirmasi, itu menjadi baca-saja. Selanjutnya, faktur hanya dapat diperbaiki jika ada koreksi atau kredit yang diawali pelanggan.

Tabel berikut ini mencantumkan aktual yang dibuat oleh sistem. Aktual ini dibuat ketika operasi tertentu dilakukan pada draf faktur proyek sebelum dikonfirmasi.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>Skenario</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>Aktual dibuat saat konfirmasi</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Faktur uang muka atau panjar </p>
            </td>
            <td width="408" valign="top">
                <p>
Jenis aktual penjualan yang ditagih, <strong>Panjar</strong> dibuat untuk jumlah uang muka atau panjar.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Penjualan yang belum ditagih dari jumlah negatif panjar atau uang muka yang akan digunakan untuk rekonsiliasi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Setelah sepenuhnya merekonsiliasi panjar atau uang muka di faktur.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi. Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang ditagih untuk jumlah pada faktur ini.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Setelah merekonsiliasi sebagian panjar atau uang muka di faktur.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi. Jumlah ini positif karena dimaksudkan untuk membatalkan negatif yang dibuat ketika panjar atau uang muka ditagih.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang ditagih untuk jumlah pada faktur ini.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan negatif dari sisa jumlah panjar atau uang muka yang akan digunakan untuk rekonsiliasi di faktur mendatang.
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
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan aktual penjualan, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang tidak dikenakan biaya untuk sisa jam dan jumlah setelah mengurangkan angka yang dikoreksi pada detail baris faktur yang diedit, pembalikan aktual penjualan, dan aktual penjualan belum ditagih yang setara.
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
Aktual penjualan yang ditagih untuk kuantitas dan jumlah saat persetujuan pengeluaran asli </p>
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
Menagih transaksi bahan tanpa pengeditan pada draf faktur.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan tak tertagih untuk kuantitas dan jumlah saat persetujuan penggunaan bahan asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan tertagih untuk kuantitas dan jumlah saat persetujuan penggunaan bahan asli.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Menagih transaksi bahan yang diedit untuk mengurangi kuantitas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan tak tertagih untuk kuantitas dan jumlah saat persetujuan waktu asli.
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
Menagih transaksi bahan yang diedit untuk meningkatkan kuantitas.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan tak tertagih untuk kuantitas dan jumlah saat persetujuan penggunaan bahan asli.
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
        <tr>
            <td width="216" valign="top">
                <p>
Memfaktur baris kontrak berbasis produk.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang ditagihkan untuk baris produk dengan kuantitas dan jumlah yang berasal dari baris kontrak berbasis produk.
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

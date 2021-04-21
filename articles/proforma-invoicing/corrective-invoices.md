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
# <a name="corrective-project-based-invoices"></a>Koreksi faktur berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Faktur proyek yang dikonfirmasi dapat diperbaiki untuk memproses perubahan atau kredit seperti yang dinegosiasikan dengan pelanggan dan manajer proyek.

Untuk melakukan pengeditan pada faktur yang dikonfirmasi, buka faktur yang dikonfirmasi dan pilih **Perbaiki Faktur ini**. 

> [!NOTE]
> Pilihan ini tidak tersedia, kecuali jika faktur proyek dikonfirmasi atau faktur berbasis proyek memiliki uang muka atau panjar atau rekonsiliasi uang muka atau panjar.

Faktur draf baru dibuat dari faktur yang dikonfirmasi. Semua detail baris faktur dari faktur yang dikonfirmasi sebelumnya disalin ke draf baru. Berikut ini adalah beberapa poin penting untuk dipahami tentang detail baris pada faktur baru yang dikoreksi:

- Semua kuantitas diperbarui ke nol. Dynamics 365 Project Operations mengasumsikan bahwa semua item ditagih sepenuhnya dikreditkan. Jika diperlukan, Anda dapat memperbarui jumlah ini secara manual untuk mencerminkan kuantitas yang sedang ditagih, dan bukan kuantitas yang dikreditkan. Berdasarkan kuantitas yang Anda masukkan, aplikasi menghitung jumlah yang dikreditkan. Jumlah ini tercermin dalam aktual yang dibuat ketika faktur yang dikoreksi dikonfirmasi. Jika Anda membuat perubahan pada jumlah pajak, Anda harus memasukkan jumlah pajak yang benar dan bukan jumlah pajak yang dikreditkan.
- Koreksi tonggak pencapaian selalu diproses sebagai kredit penuh.


> [!IMPORTANT]
> Untuk rincian baris faktur yang merupakan koreksi terhadap tagihan yang sudah ditagih, bidang **Koreksi** diatur ke **Ya**. Untuk faktur yang memiliki rincian baris faktur koreksi, bidang **Memiliki Koreksi** diatur ke **Ya**.

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>Aktual yang dibuat ketika faktur korektif dikonfirmasi

Tabel berikut berisi daftar aktual yang dibuat saat faktur perbaikan dikonfirmasi.

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
Menagih kredit penuh dari transaksi waktu yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang belum ditagih untuk jam dan jumlah pada detail baris faktur asli untuk waktu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Memfaktur kredit parsial pada transaksi waktu.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang ditagih untuk jam dan jumlah yang ditagih pada detail baris faktur asli untuk waktu.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk jam dan jumlah pada detail baris faktur yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang belum ditagih yang kena biaya untuk jam dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menagih kredit penuh dari transaksi pengeluaran yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk pengeluaran.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Menagih kredit parsial dari transaksi pengeluaran yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk pengeluaran.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur yang dikoreksi, pembalikan ini, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menagih kredit penuh dari transaksi bahan yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan tertagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk bahan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan tak tertagih baru untuk kuantitas dan jumlah pada detail baris faktur asli untuk bahan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
Menagih kredit parsial pada transaksi bahan.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan tertagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk bahan.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan belum teragih baru yang dibebankan untuk kuantitas dan jumlah pada detail baris faktur yang diedit, pembalikannya, dan aktual penjualan tertagih setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang belum ditagih yang kena biaya untuk kuantitas dan jumlah yang tersisa setelah dikurangi angka yang dikoreksi pada detail baris faktur.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menagih kredit penuh dari transaksi ongkos yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang belum ditagih untuk kuantitas dan jumlah pada detail baris faktur asli untuk ongkos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
Menagih kredit parsial dari transaksi ongkos yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang ditagih untuk kuantitas dan jumlah yang ditagih pada detail baris faktur asli untuk ongkos.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru belum ditagih yang dikenakan biaya untuk kuantitas dan jumlah pada detail baris faktur koreksi yang diedit, pembalikan ini, dan aktual penjualan belum ditagih yang setara.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Menagih kredit penuh dari tonggak pencapaian yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan yang ditagih untuk jumlah pada detail baris faktur asli untuk tonggak pencapaian.
                </p>
                <p>
Status faktur pada tonggak pencapaian diperbarui dari <b>faktur Pelanggan diposting</b> ke <b>Siap untuk Faktur</b>.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
Menagih kredit parsial dari tonggak pencapaian yang ditagih sebelumnya.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Skenario ini tidak didukung.
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

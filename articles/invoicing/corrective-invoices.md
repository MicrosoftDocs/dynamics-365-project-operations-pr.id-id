---
title: Membuat koreksi faktur berbasis proyek
description: Laporan topik memberikan informasi tentang faktur koreksi di Project Operations.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cde82bb3c5777458a63a44a131af284e6ed5d7532de6aacbb5eb860c1fcddebd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006204"
---
# <a name="create-corrective-project-based-invoices"></a>Membuat koreksi faktur berbasis proyek 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Faktur proyek yang dikonfirmasi dapat diperbaiki untuk memproses perubahan atau kredit seperti yang dinegosiasikan dengan pelanggan dan manajer proyek.

Untuk melakukan pengeditan pada faktur yang dikonfirmasi, buka faktur yang dikonfirmasi dan pilih **Perbaiki Faktur ini**. 

> [!NOTE]
> Pilihan ini tidak tersedia kecuali faktur proyek dikonfirmasi.

Faktur draf baru dibuat dari faktur yang dikonfirmasi. Semua detail baris faktur dari faktur yang dikonfirmasi sebelumnya disalin ke draf baru. Berikut ini adalah beberapa poin penting untuk membantu Anda memahami lebih lanjut tentang rincian baris pada faktur dikoreksi yang baru:

- Semua kuantitas diperbarui ke nol. Hal ini mengasumsikan bahwa semua item ditagih sepenuhnya dikreditkan. Jika diperlukan, Anda dapat memperbarui jumlah ini secara manual untuk mencerminkan kuantitas yang sedang ditagih, dan bukan kuantitas yang dikreditkan. Berdasarkan kuantitas yang Anda masukkan, aplikasi menghitung jumlah yang dikreditkan. Jumlah ini tercermin dalam aktual yang dibuat ketika faktur yang dikoreksi dikonfirmasi. Jika Anda membuat perubahan pada jumlah pajak, Anda harus memasukkan jumlah pajak yang benar dan bukan jumlah pajak yang dikreditkan.
- Koreksi tonggak pencapaian selalu diproses sebagai kredit penuh.
- Panjar atau jumlah uang muka dapat diperbaiki jika pelanggan ditagih dengan jumlah yang salah.
- Rekonsiliasi panjar dan uang muka dapat diperbaiki jika jumlah yang salah digunakan untuk merekonsiliasi terhadap biaya pada faktur yang dikonfirmasi sebelumnya.

> [!IMPORTANT]
> Rincian baris faktur yang merupakan koreksi terhadap tagihan yang sudah ditagih memiliki bidang **Koreksi** yang diatur ke **Ya**. Faktur yang telah memperbaiki detail baris faktur memiliki bidang yang disebut **Memiliki koreksi** yang juga diatur ke **Ya**.

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>Aktual yang dibuat pada Konfirmasi faktur korektif

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
            <td width="216" rowspan="4" valign="top">
                <p>
Konfirmasikan koreksi terhadap uang muka atau panjar yang ditagih.<strong></strong>
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
Aktual pembalikan penjualan yang ditagih dibuat untuk jumlah pada panjar atau uang muka untuk membalikkan penjualan asli yang ditagih.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang ditagih dibuat untuk jumlah yang dikoreksi di baris faktur yang dikoreksi berbasis uang muka atau panjar.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan yang belum ditagih dari baris faktur yang dikoreksi berbasis jumlah negatif panjar atau uang muka yang akan digunakan untuk rekonsiliasi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
Konfirmasi tentang koreksi panjar atau uang muka yang sebelumnya direkonsiliasi.
                </p>
            </td>
            <td width="408" valign="top">
                <p>
Pembalikan penjualan belum ditagih dari panjar atau uang muka yang dibuat untuk rekonsiliasi. Jumlah ini positif dan dimaksudkan untuk membatalkan negatif yang dibuat ketika rekonsiliasi sebelumnya terjadi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual pembalikan penjualan yang ditagih untuk jumlah pada faktur sebelumnya.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual penjualan baru yang ditagih untuk jumlah panjar yang dikoreksi yang diterapkan pada faktur yang dikoreksi.
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
Aktual yang belum ditagih dengan jumlah negatif dari panjar atau uang muka tersisa yang dikoreksi, yang akan digunakan untuk rekonsiliasi pada faktur mendatang.
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
Tidak Didukung </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

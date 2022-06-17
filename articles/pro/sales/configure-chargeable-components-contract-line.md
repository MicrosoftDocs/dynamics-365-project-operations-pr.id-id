---
title: Mengonfigurasikan komponen yang dikenakan biaya di baris kontrak berbasis proyek
description: Artikel ini menyediakan informasi tentang cara menambahkan komponen yang dikenakan biaya ke jalur kontrak di Operasi Proyek.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0e4118e8e56d45ef75f53d828e267a8a9c1c903a
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922962"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Mengonfigurasikan komponen yang dikenakan biaya di baris kontrak berbasis proyek

_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_

Baris kontrak berbasis proyek telah *menyertakan* komponen dan komponen *yang dapat dikenakan biaya*.

Komponen yang disertakan adalah komponen yang tunduk pada:

  - Metode penagihan dan pemisahan pelanggan
  - Batas Jangan terlampaui 
  - Pengaturan frekuensi faktur yang didefinisikan pada baris kontrak berbasis proyek

Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya menggunakan bidang **Tipe Penagihan**. Bidang **Tipe Penagihan** adalah kumpulan opsi yang memungkinkan nilai berikut dalam konteks baris kontrak:

  - Dikenakan biaya
  - Tidak Dikenakan Biaya

Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori tugas, peran, dan transaksi.

Dapat dikenakan Biaya didefinisikan pada tugas untuk baris kontrak proyek dan berlaku untuk semua kelas transaksi yang disertakan di baris. Jika bidang **Sertakan Tugas** pada baris kontrak kosong atau diatur ke **Seluruh proyek**, tab **Tugas yang dapat dikenakan biaya** tidak akan tersedia.

Bisa dikenakan biaya yang didefinisikan pada peran untuk baris kontrak proyek hanya berlaku untuk kelas transaksi **waktu**. Jika bidang **Sertakan waktu** pada baris kontrak diatur ke **Tidak**, tab **Peran yang dapat dikenakan biaya** tidak akan tersedia.

Bisa dikenakan biaya yang didefinisikan pada kategori transaksi untuk baris kontrak proyek hanya berlaku untuk kelas transaksi **Pengeluaran**. Jika bidang **Sertakan Pengeluaran** pada diatur ke **Tidak**, tab **Kategori yang dapat dikenakan biaya** tidak akan tersedia.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Memperbarui tugas proyek sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Tugas proyek dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu yang memungkinkan pengaturan berikut:

Jika baris kontrak berbasis proyek mencakup **Waktu** dan tugas tertentu, **T1** dikaitkan dengannya sebagai dikenakan biaya. Jika ada baris kontrak kedua yang mencakup **Pengeluaran**, Anda dapat mengaitkan tugas T1 di baris kontrak sebagai tidak dikenakan biaya. Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran tidak dikenakan biaya.

Jenis penagihan tugas dapat dikonfigurasi pada tab **tugas kena biaya** pada baris kontrak dengan memperbarui bidang **jenis penagihan** pada subkisi tugas baris kontrak. Atau, Anda dapat memperbarui bidang **jenis penagihan** pada subkisi dari konfigurasi penagihan tugas proyek yang menunjukkan baris kontrak yang terkait dengan tugas.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Peran dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu.

Jenis penagihan peran dapat dikonfigurasi pada tab **Peran Kena Biaya** dari baris kontrak. Untuk melakukannya, perbarui bidang **jenis penagihan** pada subkisi **peran kena biaya**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya

Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kontrak tertentu.

Jenis penagihan transaksi dapat dikonfigurasi pada tab **Kategori Kena Biaya** dari baris kontrak berbasis proyek. Untuk melakukannya, perbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**.

### <a name="resolve-chargeability"></a>Menangani pengenaan biaya

Perkiraan atau aktual yang dibuat untuk waktu hanya dianggap dibebankan jika:

   - **Waktu** tercakup di baris kontrak.
   - **Peran** dikonfigurasi sebagai dibebankan pada baris kontrak.
   - **Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kontrak.
 
 Jika ketiga hal ini benar, maka tugas dikonfigurasi sebagai dikenakan biaya. 

Perkiraan atau aktual yang dibuat untuk pengeluaran hanya dianggap dibebankan jika:

   - **pengeluaran** tercakup di baris kontrak
   - **Kategori transaksi** dikonfigurasi sebagai dibebankan pada baris kontrak
   - **Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kontrak
  
 Jika ketiga hal ini benar, maka **tugas** dikonfigurasi sebagai dikenakan biaya. 

Perkiraan atau aktual yang dibuat untuk bahan hanya dianggap dibebankan jika:

   - **Bahan** tercakup di baris kontrak
   - **Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kontrak

Jika kedua hal ini benar, maka **tugas** dikonfigurasi sebagai dikenakan biaya. 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>Mencakup Waktu</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>Mencakup Pengeluaran</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>Mencakup Bahan</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>Tugas Disertakan</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Peran</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Kategori</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tugas</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>Dampak pengenaan biaya</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan proyek </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="70" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Dikenakan Biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: <strong>Dikenakan biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: <strong>Dikenakan biaya</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="70" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Dikenakan Biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: <strong>Dikenakan biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: <strong>Dikenakan biaya</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya </p>
                <p>
Jenis penagihan pada aktual bahan: Dikenakan biaya </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="70" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: <strong>Tidak Dikenakan biaya</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: <strong>Tidak Dikenakan biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: Dikenakan biaya </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan proyek </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Dikenakan biaya</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya </p>
                <p>
Jenis penagihan pada aktual bahan: Dikenakan biaya </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan proyek </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak tersedia</strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: <strong> Tidak Dikenakan biaya</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: Dikenakan biaya </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan proyek </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="70" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: Dikenakan Biaya </p>
                <p>
Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: Dikenakan biaya </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
Ya </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan proyek </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran:<strong> Tidak tersedia</strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: Dikenakan biaya </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan proyek </p>
            </td>
            <td width="65" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="70" valign="top">
                <p>
Dikenakan biaya </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: Dikenakan Biaya </p>
                <p>
Jenis penagihan pada aktual Pengeluaran: Dikenakan biaya </p>
                <p>
Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
Ya </p>
            </td>
            <td width="78" valign="top">
                <p>
Ya </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>No</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
Keseluruhan proyek </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>Tidak Dikenakan Biaya</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
Tidak dapat diatur </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: <strong>Tidak Dikenakan Biaya </strong>
                </p>
                <p>
Jenis penagihan pada aktual Pengeluaran:<strong> Tidak Dikenakan biaya </strong>
                </p>
                <p>
Jenis penagihan pada aktual bahan: <strong> Tidak tersedia</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Mengonfigurasikan komponen yang dikenakan biaya pada baris kuotasi
description: Artikel ini memberikan informasi tentang menyiapkan komponen yang dikenakan biaya dan tidak dikenakan biaya pada baris kutipan berbasis proyek.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d4829055f429546c7911a05a765bc28ae085afa1
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930046"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Mengonfigurasikan komponen yang dikenakan biaya pada baris kuotasi 

_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_

Baris kuotasi berbasis proyek memiliki konsep *menyertakan* komponen dan komponen *yang dapat dikenakan biaya*.

Komponen yang tergantung pada:

  - Metode penagihan dan pemisahan pelanggan
  - Batas Jangan terlampaui 
  - Pengaturan frekuensi faktur yang didefinisikan pada baris kuotasi berbasis proyek

Subkumpulan komponen yang disertakan dapat ditandai sebagai dikenakan biaya menggunakan bidang **Tipe Penagihan**. Bidang **Tipe Penagihan** adalah kumpulan opsi yang memungkinkan nilai berikut dalam konteks baris kuotasi:

  - Dikenakan biaya
  - Tidak Dikenakan Biaya

Komponen yang dapat dikenakan biaya dapat didefinisikan pada kategori tugas, peran, dan transaksi.

Dapat dikenakan Biaya didefinisikan pada tugas untuk baris kuotasi dan berlaku untuk semua kelas transaksi yang disertakan di baris itu. Jika bidang **Sertakan Tugas** diatur ke **Seluruh proyek** atau dibiarkan kosong, tab **Tugas yang dapat dikenakan biaya** tidak tersedia.

Bisa dikenakan biaya didefinisikan pada peran untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **waktu**. Jika bidang, **Sertakan waktu** diatur ke **Tidak** di baris kuotasi proyek, tab **Peran yang dapat dikenakan biaya** tidak tersedia.

Bisa dikenakan biaya didefinisikan pada kategori transaksi untuk baris kuotasi dan hanya berlaku untuk kelas transaksi **Pengeluaran**. Jika bidang, **Sertakan Pengeluaran** diatur ke **Tidak** di baris kuotasi proyek, tab **Kategori yang dapat dikenakan biaya** tidak tersedia.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Memperbarui tugas proyek yang akan dikenakan biaya atau tidak dapat dikenakan biaya

Tugas proyek dapat dikenakan biaya atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu yang memungkinkan pengaturan berikut.

Jika baris kuotasi berbasis proyek mencakup **waktu** dan tugas **T1**, tugas dikaitkan ke baris kuotasi sebagai dikenakan biaya. Jika ada baris kuotasi kedua yang mencakup **Pengeluaran**, Anda dapat mengaitkan tugas **T1** di baris kuotasi sebagai tidak dikenakan biaya. Hasilnya adalah bahwa semua waktu yang dicatat pada tugas dikenakan biaya dan semua pengeluaran yang dicatat di tugas adalah tidak dikenakan biaya.

Jenis penagihan tugas dapat dikonfigurasi pada tab **tugas kena biaya** pada baris kuotasi berbasis proyek dengan memperbarui bidang **jenis penagihan** pada subkisi **tugas tugas baris kuotasi**. Atau, Anda dapat memperbarui jenis penagihan untuk tugas proyek di bidang **jenis penagihan** pada subkisi dari konfigurasi penagihan tugas proyek yang menunjukkan baris kuotasi yang terkait dengan tugas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Memperbarui peran sebagai dapat dikenakan biaya atau tidak dapat dikenakan biaya

Peran dapat dikenakan atau tidak dikenakan biaya dalam konteks baris kuotasi berbasis proyek tertentu.

Jenis penagihan peran dapat dikonfigurasi pada tab **Peran kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **peran kena biaya**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Memperbarui kategori transaksi sebagai dikenakan biaya atau tidak dikenakan biaya

Kategori transaksi dapat dikenakan biaya atau tidak dikenakan biaya pada baris kuotasi tertentu.

Jenis penagihan transaksi dapat dikonfigurasi pada tab **Kategori kena biaya** pada baris kuotasi dengan memperbarui bidang **jenis penagihan** pada subkisi **Kategori kena biaya**.

### <a name="resolve-chargeability"></a>Menangani pengenaan biaya
Perkiraan atau aktual yang dibuat untuk waktu hanya akan dianggap dibebankan jika:

   - **Waktu** tercakup di baris kuotasi.
   - **Peran** dikonfigurasi sebagai dibebankan pada baris kuotasi.
   - **Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi. 

Jika ketiga hal ini benar, maka **tugas** juga dikonfigurasi sebagai dikenakan biaya. 

Perkiraan atau aktual yang dibuat untuk pengeluaran hanya dianggap dibebankan jika: 

   - **pengeluaran** tercakup di baris kuotasi.
   - **Kategori transaksi** dikonfigurasi sebagai dibebankan pada baris kuotasi.
   - **Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.

Jika ketiga hal ini benar, maka **tugas** juga dikonfigurasi sebagai dikenakan biaya. 

Perkiraan atau aktual yang dibuat untuk bahan hanya akan dianggap dibebankan jika:

   - **Bahan** tercakup di baris kuotasi.
   - **Tugas yang Tercakup** diatur ke **Tugas yang dipilih** pada baris kuotasi.

Jika kedua hal ini benar, maka **tugas** juga harus dikonfigurasi sebagai dikenakan biaya. 


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
Penagihan pada aktual Waktu: Dikenakan Biaya </p>
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
Dikenakan biaya </p>
            </td>
            <td width="350" valign="top">
                <p>
Penagihan pada aktual Waktu: Dikenakan Biaya </p>
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

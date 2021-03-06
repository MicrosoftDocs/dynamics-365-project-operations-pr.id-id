---
title: Baris kuotasi berbasis proyek
description: Topik ini memberikan informasi tentang menggunakan baris kuotasi berbasis proyek untuk pekerjaan proyek.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 06a47c45dc3b3b174658e2fba14d3d2050aabf85
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906211"
---
# <a name="project-based-quote-lines"></a>Baris kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Baris kuotasi berbasis proyek dirancang untuk membantu memperkirakan pekerjaan proyek pada keterlibatan. Struktur baris kuotasi berbasis proyek diperluas untuk perkiraan proyek dengan konsep berikut:

- Metode Penagihan
- Pemetaan proyek
- Termasuk kelas transaksi
- Batas Jangan terlampaui
- Konfigurasi ketertagihan
- Estimasi menggunakan rincian baris kuotasi
- Pelanggan Baris Kuotasi

Tabel berikut menyediakan informasi tentang bidang pada tab **Umum** baris kuotasi berbasis proyek. Bidang ini membantu membuat dasar untuk estimasi yang rinci dan komprehensif untuk pekerjaan proyek.

| **Bidang** | **Relevansi, tujuan, dan panduan** | **Dampak hilir** |
| --- | --- | --- |
| Nama | Nama baris kuotasi yang seharusnya membantu Anda mengidentifikasi komponen diskrit dari kuotasi yang sedang diperkirakan. | Disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Metode Penagihan | Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang yang sesuai pada baris peluang. Bidang ini mencakup dua model kontrak utama yang didukung oleh Dynamics 365 Project Operations:</br>- Harga tetap</br>- Waktu dan bahan.| Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Project | Gunakan bidang opsional ini untuk mengidentifikasi proyek yang akan digunakan untuk melakukan pekerjaan pada keterlibatan ini. Saat dipetakan ke baris kuotasi, proyek akan membantu dengan pengaturan tugas yang dapat dibebankan dan juga dengan mendatangkan estimasi berbasis proyek ke baris kuotasi sebagai rincian baris kuotasi. Ketika proyek tidak dipetakan ke baris kuotasi berbasis proyek, perkiraan harus dibuat secara manual dengan membuat detail setiap baris kuotasi. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Sertakan Waktu | Peringatan **ya**/**tidak** menunjukkan jika transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **Ya** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja akan dimasukkan dalam perkiraan baris kuotasi ini. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Sertakan Pengeluaran | Peringatan **ya**/**tidak** menunjukkan jika biaya pengeluaran pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **tidak** menunjukkan bahwa biaya pengeluaran tidak akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **tidak** menunjukkan bahwa biaya pengeluaran akan dimasukkan dalam perkiraan baris kuotasi ini. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Sertakan Tarif | Peringatan **ya**/**tidak** menunjukkan jika ongkos pada proyek yang dipilih akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **tidak** menunjukkan bahwa ongkos tidak akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **tidak** menunjukkan bahwa ongkos akan dimasukkan dalam perkiraan baris kuotasi ini. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Jumlah Kuotasi | Ini adalah jumlah yang akan ditawarkan untuk pelanggan untuk semua pekerjaan yang diperkirakan pada baris kuotasi berbasis proyek ini. Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang **Anggaran Pelanggan** pada baris peluang. Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kuotasi. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Perkiraan Pajak | Ini adalah bidang yang dapat diedit bagi pengguna untuk menambahkan estimasi jumlah pajak pada baris kuotasi. Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kuotasi. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Jumlah Kuotasi Setelah Pajak | Bidang ini adalah jumlah baris kuotasi setelah pajak dan bersifat hanya baca. Jumlah dalam bidang ini dihitung sebagai *jumlah yang ditawarkan + pajak*. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Batas Jangan terlampaui | Bidang ini dapat diedit dan hanya tersedia pada baris kuotasi berbasis proyek yang memiliki metode penagihan **waktu dan bahan**. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Anggaran Pelanggan | Bidang ini dapat diedit dan disalin dari bidang yang sesuai pada baris peluang jika kuotasi dibuat dari peluang. | Nilai bidang ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Aturan validasi untuk bidang pada tab Umum baris kuotasi berdasarkan proyek

**Aturan 1**: kelas transaksi tertentu pada proyek yang dipilih hanya dapat disertakan pada satu baris kuotasi berbasis proyek dari kuotasi.

**Aturan 2**: jika peluang memiliki beberapa kuotasi, ada baris kuotasi dari kuotasi berbeda yang semua mereferensi proyek yang sama dan mencakup kelas transaksi yang sama.

**Aturan 3**: jika kuotasi bukan milik peluang yang sama, mereka tidak dapat menyertakan kelas proyek dan transaksi yang sama.

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>Peluang</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Kuotasi</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Baris Kuotasi</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Sertakan Waktu</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>Sertakan Pengeluaran</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Sertakan</strong>
                </p>
                <p>
                    <strong>Biaya</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>Valid/tidak valid</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>Alasan</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #1. Waktu, pengeluaran, dan biaya pada proyek P1 disertakan pada baris kuotasi, QL1, dan QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #1. Waktu dan ongkos pada proyek P1 disertakan pada baris kuotasi, QL1, dan QL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
Waktu dan ongkos pada proyek P1 disertakan pada QL1.
pengeluaran pada proyek P1 disertakan pada QL2.
Tidak ada tumpang tindih dalam apa yang sedang dimasukkan pada setiap baris kuotasi sehingga ini valid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
No </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #1 di atas </p>
                <p>
Q1 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1.
                </p>
                <p>
QL2 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1 dan tumpang tindih dengan yang disertakan pada Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
                <p>
Valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Berdasarkan aturan #2, Q1 dan Q2 adalah dua kuotasi pada peluang yang sama, sehingga mereka dapat memperkirakan komponen yang sama dari suatu proyek.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K2 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 pada Q2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
                <p>
Valid </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
Berdasarkan aturan #3, Q1 dan Q2 adalah dua kuotasi pada peluang yang berbeda, sehingga mereka tidak dapat memperkirakan komponen yang sama dari suatu proyek yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
K1 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="48" valign="top">
                <p>
Ya </p>
            </td>
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="54" valign="top">
                <p>
Tidak valid </p>
            </td>
        </tr>
    </tbody>
</table>


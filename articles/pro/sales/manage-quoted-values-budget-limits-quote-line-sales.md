---
title: Sekilas baris kuotasi berbasis proyek
description: Artikel ini menyediakan informasi tentang penggunaan garis kutipan berbasis proyek untuk pekerjaan proyek.
author: rumant
ms.date: 03/30/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 90c5affa25b113476e43f0bbbadd5c9615f9c05c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934462"
---
# <a name="project-based-quote-lines-overview"></a>Sekilas baris kuotasi berbasis proyek 

_**Berlaku untuk:** Penyebaran Lite- faktur dari penawaran hingga proforma, Project Operations untuk skenario berbasis sumber daya/non-stok_

Baris kuotasi berbasis proyek dirancang untuk membantu memperkirakan pekerjaan proyek pada keterlibatan. Struktur baris kuotasi berbasis proyek diperluas untuk perkiraan proyek dengan konsep berikut:

- Metode Penagihan
- Pemetaan Proyek dan Tugas
- Termasuk kelas transaksi
- Batas Jangan terlampaui
- Konfigurasi ketertagihan
- Estimasi menggunakan rincian baris kuotasi
- Pelanggan Baris Kuotasi

Tabel berikut menyediakan informasi tentang bidang pada tab **Umum** baris kuotasi berbasis proyek. Bidang ini membantu membuat dasar untuk estimasi yang rinci dan komprehensif untuk pekerjaan proyek.

| **Bidang** | **Deskripsi** | **Dampak hilir** |
| --- | --- | --- |
| Nama | Nama baris kuotasi yang membantu Anda mengidentifikasi komponen terpisah dari kuotasi yang sedang diestimasi. | Disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Metode Penagihan | Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang yang sesuai pada baris peluang. Bidang ini mencakup dua model kontrak utama yang didukung oleh Dynamics 365 Project Operations:</br>- Harga tetap</br>- Waktu dan bahan.| Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Project | Gunakan bidang opsional ini untuk mengidentifikasi proyek yang akan digunakan untuk melakukan pekerjaan pada keterlibatan ini. Saat dipetakan ke baris kuotasi, proyek akan membantu dengan pengaturan tugas yang dapat dibebankan dan juga dengan mendatangkan estimasi berbasis proyek ke baris kuotasi sebagai rincian baris kuotasi. Ketika proyek tidak dipetakan ke baris kuotasi berbasis proyek, perkiraan harus dibuat secara manual dengan membuat detail setiap baris kuotasi. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan.|
| Tugas Disertakan | Menunjukkan jika baris kuotasi ini digunakan untuk semua atau sebagian tugas proyek untuk proyek yang dipilih. Bidang ini memiliki kemungkinan nilai berikut:</br>- Semua tugas proyek</br>- Hanya tugas proyek yang dipilih</br>Nilai kosong di bidang ini setara dengan pilihan **semua tugas proyek**. | Bila **Tugas proyek yang Dipilih saja** dipilih pada halaman proyek, tab **Konfigurasi penagihan Tugas** memungkinkan Anda memilih tugas tertentu untuk mengaitkannya ke baris kuotasi ini. Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Sertakan Waktu | Nilai **Ya**/**Tidak** menunjukkan apakah transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini. Nilai **tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **Ya** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja akan dimasukkan dalam perkiraan baris kuotasi ini. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Sertakan Pengeluaran | Nilai **Ya**/**Tidak** menunjukkan apakah biaya pengeluaran pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini. Nilai **tidak** menunjukkan bahwa biaya pengeluaran tidak akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **tidak** menunjukkan bahwa biaya pengeluaran akan dimasukkan dalam perkiraan baris kuotasi ini. | Nilai ini disalin pada baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Termasuk Materi | Nilai **Ya**/**Tidak** menunjukkan apakah biaya bahan pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini. Nilai **Tidak** menunjukkan bahwa biaya bahan tidak akan disertakan dalam estimasi di baris kuotasi ini. Nilai **Ya** menunjukkan bahwa biaya bahan akan disertakan dalam estimasi di baris kuotasi ini. | Nilai ini disalin pada baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Sertakan Tarif | Nilai **Ya**/**Tidak** menunjukkan apakah ongkos pada proyek yang dipilih akan disertakan dalam estimasi pada baris kuotasi ini. Nilai **tidak** menunjukkan bahwa ongkos tidak akan dimasukkan dalam perkiraan baris kuotasi ini. Nilai **tidak** menunjukkan bahwa ongkos akan dimasukkan dalam perkiraan baris kuotasi ini. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Jumlah Kuotasi | Ini adalah jumlah yang akan diberikan kuotasinya kepada pelanggan untuk semua pekerjaan yang diramalkan pada baris kuotasi berbasis proyek ini. Pada kuotasi yang dibuat dari peluang, nilai ini disalin dari bidang **Anggaran Pelanggan** pada baris peluang. Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kuotasi. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Perkiraan Pajak | Ini adalah bidang yang dapat diedit bagi pengguna untuk menambahkan estimasi jumlah pajak pada baris kuotasi. Bila baris kuotasi berbasis proyek memiliki detail baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kuotasi. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Jumlah Kuotasi Setelah Pajak | Bidang ini adalah jumlah baris kuotasi setelah pajak dan bersifat hanya baca. Jumlah dalam bidang ini dihitung sebagai *jumlah yang ditawarkan + pajak*. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Batas Jangan terlampaui | Bidang ini dapat diedit dan hanya tersedia pada baris kuotasi berbasis proyek yang memiliki metode penagihan **waktu dan bahan**. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |
| Anggaran Pelanggan | Bidang ini dapat diedit dan disalin dari bidang yang sesuai pada baris peluang jika kuotasi dibuat dari peluang. | Nilai ini disalin ke baris kontrak proyek yang dibuat dari baris kuotasi ini saat kuotasi dimenangkan. |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>Aturan validasi untuk bidang pada tab Umum baris kuotasi berdasarkan proyek

**Aturan 1**: jika bidang **tugas yang disertakan** kosong, atau jika diatur ke **semua tugas proyek**, proyek disertakan dalam baris kuotasi.

**Aturan 2**: jika bidang **tugas yang disertakan** kosong, atau jika diatur ke **semua tugas proyek**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada satu baris kuotasi berbasis proyek dari kuotasi.

**Aturan 3**: jika bidang **tugas yang disertakan** diatur ke **Hanya tugas proyek yang dipilih**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada beberapa baris kuotasi berbasis proyek dari kuotasi.

**Aturan 4**: jika peluang memiliki beberapa kuotasi, ada baris kuotasi dari kuotasi berbeda yang semua mereferensi proyek yang sama dan mencakup kelas transaksi yang sama.

**Aturan 5**: jika kuotasi bukan milik peluang yang sama, mereka tidak dapat menyertakan kelas proyek dan transaksi yang sama.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p>
                    <strong>Peluang</strong>
                </p>
            </td>
            <td width="39" valign="top">
                <p>
                    <strong>Kuotasi</strong>
                </p>
            </td>
            <td width="40" valign="top">
                <p>
                    <strong>Baris Kuotasi</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="77" valign="top">
                <p>
                    <strong>Tugas yang Disertakan</strong>
                </p>
            </td>
            <td width="45" valign="top">
                <p>
                    <strong>Sertakan Waktu</strong>
                </p>
            </td>
            <td width="46" valign="top">
                <p>
                    <strong>Sertakan Pengeluaran</strong>
                </p>
            </td>
            <td width="43" valign="top">
                <p>
                    <strong>Termasuk Materi</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>Sertakan</strong>
                </p>
                <p>
                    <strong>Biaya</strong>
                </p>
            </td>
            <td width="49" valign="top">
                <p>
                    <strong>Valid/tidak valid</strong>
                </p>
            </td>
            <td width="200" valign="top">
                <p>
                    <strong>Alasan</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #2. Waktu, pengeluaran, dan Ongkos pada proyek P1 disertakan pada baris kuotasi QL1 dan QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #2. Waktu, Bahan, dan Ongkos pada proyek P1 disertakan pada baris kuotasi QL1 dan QL2 </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
No </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Waktu, Bahan, dan Ongkos pada proyek P1 tercakup di QL1 <br>
pengeluaran pada proyek P1 disertakan pada QL2 <br>
Tidak ada tumpang tindih dalam hal yang tercakup di setiap baris kuotasi dan oleh karena itu valid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
No </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
No </p>
            </td>
            <td width="41" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #2 </p>
                <p>
Q1 mencakup Waktu, Bahan, Pengeluaran dan Ongkos pada subset tugas di proyek P1 </p>
                <p>
QL2 mencakup waktu, pengeluaran, dan ongkos untuk seluruh proyek P1 dan karena itu tumpang tindih dengan yang disertakan di Q1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per aturan #3, </p>
                <p>
Q1 mencakup Waktu, Bahan, Pengeluaran dan Ongkos pada subset tugas di proyek P1.
                </p>
                <p>
QL2 mencakup Waktu, Pengeluaran, Bahan, dan Ongkos untuk subset tugas di proyek P1.
                </p>
                <p>
Satu-satunya validasi tambahan adalah seputar subset tugas di QL1, yang berbeda dengan subset tugas di QL2 untuk memastikan tidak ada tumpang tindih di sana. Hal ini dilakukan oleh sistem saat tugas terkait.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Hanya tugas yang dipilih </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Semua Tugas Proyek atau kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per Aturan #5, Q1 dan Q2 adalah dua kuotasi pada peluang yang sama, sehingga mereka dapat memperkirakan untuk komponen proyek yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K2 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Semua Tugas Proyek atau kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O1 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Semua Tugas Proyek atau kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
Per Aturan #4, Q1 dan Q2 adalah dua kuotasi pada peluang yang berbeda, sehingga mereka tidak dapat memperkirakan untuk komponen proyek yang sama.
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
O2 </p>
            </td>
            <td width="39" valign="top">
                <p>
K1 </p>
            </td>
            <td width="40" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="41" valign="top">
                <p>
P1 </p>
            </td>
            <td width="77" valign="top">
                <p>
Semua Tugas Proyek atau kosong </p>
            </td>
            <td width="45" valign="top">
                <p>
Ya </p>
            </td>
            <td width="46" valign="top">
                <p>
Ya </p>
            </td>
            <td width="43" valign="top">
                <p>
Ya </p>
            </td>
            <td width="41" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

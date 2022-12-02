---
title: Sekilas baris kontrak berbasis proyek
description: Artikel ini menyediakan informasi tentang bekerja dengan baris kontrak berbasis proyek.
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d32edac6537a4b0f51e9d2f72cb4a7342606d2c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931426"
---
# <a name="project-based-contract-lines-overview"></a>Sekilas baris kontrak berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Baris kontrak berbasis proyek di Dynamics 365 Project Operations dirancang untuk menyimpan estimasi dan pengaturan penagihan untuk komponen tertentu dari pekerjaan proyek pada suatu kesepakatan. Struktur baris kontrak berbasis proyek diperluas untuk perkiraan proyek dan skenario penagihan dengan konsep berikut:

- Metode Penagihan
- Pemetaan Proyek dan Tugas
- Termasuk kelas transaksi
- Batas Jangan terlampaui
- Konfigurasi ketertagihan
- Memperkirakan penggunaan rincian baris kontrak
- Pelanggan Baris Kontrak

Tabel berikut mencakup bidang pada tab **Umum** baris kontrak berbasis proyek yang membantu mengkonfigurasikan dasar estimasi terperinci dan dari awal serta pengaturan penagihan untuk pekerjaan berbasis proyek.

| Bidang | KETERANGAN | Dampak hilir |
| --- | --- | --- |
| **Nama** | Nama rekaman baris kontrak. Ini mengidentifikasi komponen diskrit dari kontrak yang sedang diperkirakan. Untuk kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari nilai baris kuotasi berbasis proyek yang terkait. | Nilai yang disalin ke baris faktur proyek yang dibuat dari baris kontrak ini saat faktur dibuat. |
| **Metode Penagihan** | Di kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari bidang terkait di baris kuotasi. Ini adalah rangkaian pilihan yang menunjukkan dua model kontrak utama yang didukung oleh Project Operations:</br>- **Harga Tetap**</br>- **Waktu dan Materi** | Berdasarkan metode penagihan baris kontrak yang dirujuk, transaksi aktual akan diproses. Jika baris kontrak yang dirujuk oleh aktual memiliki metode penagihan waktu dan material, maka biaya dan rekaman aktual penjualan yang belum ditagih dibuat. Jika baris kontrak yang dirujuk oleh metode aktual memiliki metode penagihan harga tetap, hanya aktual biaya yang dibuat. |
| **Project** | Gunakan bidang ini untuk mengidentifikasi proyek yang akan digunakan untuk melaksanakan pekerjaan pada kesepakatan ini. | Nilai ini akan digunakan secara bersama-sama dengan **Kelas Transaksi Tercakup** dan **Tugas Tercakup** untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi. |
| **Tugas Disertakan** | Menunjukkan jika baris kontrak ini mencakup semua tugas proyek untuk proyek yang dipilih atau hanya subset dari tugas. Ini adalah rangkaian pilihan yang memiliki nilai yang mungkin berikut:</br>- **Semua Tugas Proyek**</br>- **Hanya tugas proyek yang dipilih**. Nilai kosong pada bidang ini sama dengan memilih **semua tugas proyek**. | Jika **tugas yang dipilih saja** dipilih, Anda dapat memilih tugas tertentu dan mengaitkannya ke baris kontrak ini di tab **penyiapan penagihan tugas** pada halaman **proyek**. Nilai ini akan digunakan bersama dengan **Proyek** dan kelas **Transaksi yang tercakup** untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi. |
| **Sertakan Waktu** | Nilai **Ya**/**Tidak** menunjukkan apakah transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan disertakan pada baris kontrak ini. Nilai **ya** menunjukkan bahwa akan disertakan. | Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi. |
| **Sertakan Pengeluaran** | Nilai **Ya**/**Tidak** menunjukkan apakah biaya pengeluaran pada proyek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahwa biaya pengeluaran tidak akan disertakan pada baris kontrak ini. Nilai **ya** menunjukkan bahwa akan disertakan. | Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi. |
| **Termasuk Bahan** | Nilai **Ya**/**Tidak** menunjukkan apakah biaya bahan pada proyek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahwa biaya bahan tidak akan disertakan pada baris kontrak ini. Nilai **ya** menunjukkan bahwa akan disertakan. | Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi. |
| **Sertakan Tarif** | Nilai **Ya**/**Tidak** menunjukkan apakah ongkos pada proyek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahwa ongkos tidak akan disertakan pada baris kontrak ini. Nilai **ya** menunjukkan bahwa akan disertakan. | Nilai ini digunakan secara bersama-sama dengan proyek untuk menangani referensi baris kontrak pada rekaman aktual atau baris estimasi. |
| **Jumlah yang Dikontrak** | Pada baris kontrak harga tetap, jumlah ini adalah nilai yang disepakati yang akan ditagih kepada pelanggan untuk semua komponen kerja yang terkait dengan baris kontrak ini. Pada baris kontrak waktu dan material, jumlah ini adalah nilai estimasi tentang apa yang akan ditagih kepada pelanggan untuk semua komponen kerja yang terkait pada baris kontrak ini. Di kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari bidang terkait di baris kuotasi. Bila baris kontrak berbasis proyek memiliki rincian baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kontrak. | Bila baris kontrak memiliki rincian baris, nilai ini dapat dimodifikasi dengan mengubah jumlah rincian baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan jumlah sebelum pajak pada tonggak pencapaian penagihan berkala. |
| **Perkiraan Pajak** | Pengguna dapat mengedit bidang ini untuk memasukkan estimasi jumlah pajak pada baris kontrak. Bila baris kontrak berbasis proyek memiliki rincian baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kontrak. | Bila baris kontrak memiliki rincian baris, nilai ini dapat dimodifikasi dengan mengubah jumlah pajak pada rincian baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan pajak pada tonggak pencapaian penagihan berkala. |
| **Jumlah Kontrak Setelah Pajak** | Jumlah baris kontrak setelah pajak. Bidang ini hanya baca dan dihitung sebagai **jumlah kontrak + pajak**. | Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan tonggak pencapaian penagihan berkala. |
| **Batas Jangan terlampaui** | Pengguna dapat mengedit bidang ini dan hanya tersedia pada baris kontrak berbasis proyek yang mengatur metode penagihan sebagai waktu dan material. | Pengguna dapat mengedit bidang ini. Bila aktual untuk waktu atau dan material merujuk baris kontrak ini untuk waktu dan material, jumlah pada aktual dievaluasi terhadap batas yang tidak boleh dilebihi pada baris kontrak ini. Evaluasi ini diselesaikan setelah jumlah pembelanjaan dan komitmen diperhitungkan. |
| **Anggaran Pelanggan** | Bidang ini dapat diedit dan disalin dari bidang terkait di baris kuotasi, jika kontrak dibuat dari kuotasi. | Bidang ini hanya digunakan untuk informasi dan tidak memiliki signifikansi hilir. |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Aturan validasi untuk pilihan pada tab Umum baris kontrak berbasis proyek

Aturan 1: jika bidang **tugas yang disertakan** kosong atau diatur ke **semua tugas proyek**, semua tugas proyek disertakan pada baris kontrak.

Aturan 2: bila bidang **tugas yang disertakan** kosong atau diatur secara eksplisit ke **semua tugas proyek**, proyek dan kelas transaksi tertentu hanya dapat disertakan pada satu baris kontrak berbasis proyek dari kontrak.

Aturan 3: bila bidang **tugas yang disertakan** diatur ke **tugas proyek yang dipilih saja**, proyek dan kelas transaksi tertentu dapat disertakan pada beberapa baris kontrak berbasis proyek dari kontrak.

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>Kontrak</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>Baris Kontrak</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>Tugas yang Disertakan</strong>
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
                    <strong>Termasuk Bahan</strong>
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
            <td width="53" valign="top">
                <p>
                    <strong>Valid/tidak valid</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>Alasan</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #2. Waktu, Pengeluaran, Bahan, dan Ongkos pada proyek P1 tercakup di baris Kontrak CL1 dan CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #2. Waktu, Bahan, dan Ongkos pada proyek P1 tercakup di baris Kontrak CL1 dan CL2.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Waktu, Bahan, dan Ongkos pada proyek P1 tercakup di CL1.
                </p>
                <ul>
                    <li>
pengeluaran pada proyek P1 disertakan pada CL2.
                    </li>
                </ul>
                <p>
Tidak ada tumpang tindih dalam hal yang tercakup di setiap baris Kontrak dan oleh karena itu valid.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
No </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Hanya tugas yang dipilih </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Tidak valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Pelanggaran aturan #2 </p>
                <p>
C1 mencakup Waktu, Bahan, Pengeluaran dan Ongkos pada subset tugas di proyek P1.
                </p>
                <p>
CL2 mencakup Waktu, Bahan, Pengeluaran dan Ongkos untuk seluruh proyek P1, sehingga tumpang tindih dengan yang tercakup di C1.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Kosong </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Hanya tugas yang dipilih </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
Valid </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
Per aturan #3 </p>
                <p>
C1 mencakup Waktu, Pengeluaran, Bahan, dan Ongkos pada subset tugas di proyek P1.
                </p>
                <p>
CL2 mencakup Waktu, Pengeluaran, Bahan, dan Ongkos untuk subset tugas di proyek P1.
                </p>
                <p>
Satu-satunya validasi tambahan adalah seputar subset tugas di CL1, berbeda dengan subset tugas di CL2 untuk memastikan tidak ada tumpang tindih di sana. Hal ini dilakukan oleh sistem saat tugas terkait.
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
Hanya tugas yang dipilih </p>
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
            <td width="42" valign="top">
                <p>
Ya </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

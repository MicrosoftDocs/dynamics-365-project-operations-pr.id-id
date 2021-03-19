---
title: Bekerja dengan Baris kontrak berbasis proyek
description: Topik ini menyediakan informasi tentang baris kontrak berbasis proyek.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2b856e280ac56c1cedd7d4966aca7e7f234bc520
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278107"
---
# <a name="work-with-projectbased-contract-lines"></a>Bekerja dengan Baris kontrak berbasis proyek

Baris kontrak berbasis proyek di Dynamics 365 Project Operations dirancang untuk menyimpan estimasi dan pengaturan penagihan untuk komponen tertentu dari pekerjaan proyek pada suatu kesepakatan. Struktur baris kontrak berbasis proyek diperluas untuk perkiraan proyek dan skenario penagihan dengan konsep berikut:

- Metode Penagihan
- Pemetaan Proyek dan Tugas
- Termasuk kelas transaksi
- Batas Jangan terlampaui
- Konfigurasi ketertagihan
- Memperkirakan penggunaan rincian baris kontrak
- Pelanggan Baris Kontrak

Bidang berikut disertakan pada tab **Umum** baris kontrak berbasis proyek. Bidang ini membantu menetapkan dasar untuk perkiraan rinci, sejak awal, dan pengaturan penagihan untuk pekerjaan berbasis proyek.

| Bidang | KETERANGAN | Dampak hilir |
| --- | --- | --- |
| **Nama** | Nama baris kontrak yang mengidentifikasi komponen diskrit dari kontrak yang sedang diperkirakan. Untuk kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari nilai baris kuotasi berbasis proyek yang terkait. | Nilai bidang ini akan disalin ke baris faktur proyek yang dibuat dari baris kontrak ini saat faktur dibuat. |
| **Metode Penagihan** | Di kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari bidang terkait di baris kuotasi. Ini adalah rangkaian pilihan yang menunjukkan dua model kontrak utama yang didukung oleh Project Operations:</br>- **Harga Tetap**</br>- **Waktu dan Materi** | Berdasarkan metode penagihan baris kontrak yang dirujuk, transaksi aktual akan diproses. Jika baris kontrak yang dirujuk oleh aktual memiliki metode penagihan waktu dan material, maka biaya dan rekaman aktual penjualan yang belum ditagih dibuat. Jika baris kontrak yang dirujuk oleh metode aktual memiliki metode penagihan harga tetap, hanya aktual biaya yang dibuat. |
| **Project** | Gunakan bidang ini untuk mengidentifikasi proyek yang akan digunakan untuk melaksanakan pekerjaan pada kesepakatan ini. | Nilai pada bidang ini digunakan bersama dengan bidang **tugas yang tercakup** dan **tercakup dalam kelas transaksi** untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi. |
| **Sertakan Waktu** | Bendera menunjukkan apakah transaksi waktu atau biaya tenaga kerja pada proyek yang dipilih disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahwa transaksi waktu atau biaya tenaga kerja tidak akan disertakan pada baris kontrak ini. Nilai **ya** menunjukkan bahwa akan disertakan. | Nilai bidang ini digunakan bersama dengan proyek untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi. |
| **Sertakan Pengeluaran** | Bendera menunjukkan apakah biaya pengeluaran pada proyek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahwa biaya pengeluaran tidak akan disertakan pada baris kontrak ini. Nilai **ya** menunjukkan bahwa akan disertakan. | Nilai bidang ini digunakan bersama dengan proyek untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi. |
| **Sertakan Tarif** | Bendera menunjukkan apakah ongkos pada proyek yang dipilih akan disertakan pada baris kontrak ini. Nilai **Tidak** menunjukkan bahwa ongkos tidak akan disertakan pada baris kontrak ini. Nilai **ya** menunjukkan bahwa akan disertakan. | Nilai bidang ini digunakan bersama dengan proyek untuk menangani referensi baris kontrak pada rekaman baris aktual atau estimasi. |
| **Jumlah yang Dikontrak** | Pada baris kontrak harga tetap, ini adalah nilai yang disepakati yang akan ditagih kepada pelanggan untuk semua komponen kerja yang terkait dengan baris kontrak ini. Pada baris kontrak waktu dan material, jumlah ini adalah nilai estimasi tentang apa yang akan ditagih kepada pelanggan untuk semua komponen kerja yang terkait pada baris kontrak ini. Di kontrak proyek yang dibuat dari kuotasi, nilai ini disalin dari bidang terkait di baris kuotasi. Bila baris kontrak berbasis proyek memiliki rincian baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pada rincian baris kontrak. | Bila baris kontrak memiliki rincian baris, nilai ini dapat dimodifikasi dengan mengubah jumlah rincian baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan jumlah sebelum pajak pada tonggak pencapaian penagihan berkala. |
| **Perkiraan Pajak** | Pengguna dapat mengedit bidang ini untuk memasukkan estimasi jumlah pajak pada baris kontrak. Bila baris kontrak berbasis proyek memiliki rincian baris, bidang ini dikunci untuk pengeditan dan diringkas dari jumlah pajak pada rincian baris kontrak. | Bila baris kontrak memiliki rincian baris, nilai ini dapat dimodifikasi dengan mengubah jumlah pajak pada rincian baris. Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan pajak pada tonggak pencapaian penagihan berkala. |
| **Jumlah Kontrak Setelah Pajak** | Jumlah baris kontrak setelah pajak. Bidang ini hanya baca dan dihitung sebagai **jumlah kontrak + pajak**. | Pada baris kontrak harga tetap, nilai ini digunakan untuk menghasilkan tonggak pencapaian penagihan berkala. |
| **Batas Jangan terlampaui** | Pengguna dapat mengedit bidang ini dan hanya tersedia pada baris kontrak berbasis proyek yang memiliki metode penagihan waktu dan material. | Pengguna dapat mengedit bidang ini. Bila waktu atau pengeluaran yang sebenarnya merujuk baris kontrak ini untuk waktu dan material, jumlah pada aktual dievaluasi terhadap batas yang tidak boleh dilebihi pada baris kontrak ini setelah memperhitungkan jumlah yang telah dibelanjakan dan ditindaklanjuti. |
| **Anggaran Pelanggan** | Bidang ini dapat diedit dan disalin dari bidang terkait di baris kuotasi, jika kontrak dibuat dari kuotasi. | Bidang ini hanya digunakan untuk informasi dan tidak memiliki signifikansi hilir. |

## <a name="validation-rule-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>Aturan validasi untuk pilihan pada tab Umum baris kontrak berbasis proyek

Aturan: proyek dan kelas transaksi tertentu hanya dapat disertakan pada satu baris kontrak berbasis proyek dalam kontrak.

| Kontrak | Baris Kontrak | Project | Sertakan Waktu | Sertakan Pengeluaran | Sertakan ongkos | Valid/tidak valid | Alasan                                                                                                                                                                                                  |
|----------|---------------|---------|--------------|-----------------|-------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| C1       | CL1           | P1      | Ya          | Ya             | Ya         | Tidak valid       | Melanggar aturan. Waktu, pengeluaran, dan ongkos pada proyek P1 disertakan pada baris kontrak, CL1, dan CL2.                                                                                       |
| C1       | CL2           | P1      | Ya          | Ya             | Ya         | Tidak valid       | Melanggar aturan. Waktu, pengeluaran, dan ongkos pada proyek P1 disertakan pada baris kontrak, CL1, dan CL2.                                                                                       |
| C1       | CL1           | P1      | Ya          | No              | Ya         | Tidak valid       | Melanggar aturan. Waktu dan ongkos pada proyek P1 disertakan pada baris kontrak, CL1, dan CL2.                                                                                                   |
| C1       | CL2           | P1      | Ya          | Ya             | Ya         | Tidak valid       | Melanggar aturan. Waktu dan ongkos pada proyek P1 disertakan pada baris kontrak, CL1, dan CL2.                                                                                                   |
| C1       | CL1           | P1      | Ya          | No              | Ya         | Valid           | Waktu dan ongkos pada proyek P1 disertakan pada CL1. pengeluaran pada proyek P1 disertakan pada CL2. </br>   Tidak ada tumpang tindih dalam apa yang sedang dimasukkan pada setiap baris kontrak dan karena itu valid.  |
| C1       | CL2           | P1      | No           | Ya             | No          | Valid           | Waktu dan ongkos pada proyek P1 disertakan pada CL1. pengeluaran pada proyek P1 disertakan pada CL2. </br>   Tidak ada tumpang tindih dalam apa yang sedang dimasukkan pada setiap baris kontrak dan karena itu valid.  |
| C1       | CL1           | P1      | Ya          | Ya             | Ya         | Tidak valid       | Melanggar aturan. Waktu, pengeluaran, dan ongkos pada proyek P1 disertakan pada baris dua kontrak.                                                                                               |
| CL2      | CL2           | P1      | Ya          | Ya             | Ya         | Tidak valid       | Melanggar aturan. Waktu, pengeluaran, dan ongkos pada proyek P1 disertakan pada baris dua kontrak.                                                                                               |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
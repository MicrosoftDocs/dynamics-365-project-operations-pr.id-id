---
title: Performa API Jadwal proyek
description: Topik ini memberikan informasi tentang tolok ukur performa API jadwal Proyek dan mengidentifikasi praktik terbaik untuk penggunaan optimal.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a1abadbae044ccbd40077c6937262f0f17387bad
ms.sourcegitcommit: 5c536cf05e2cbfc1d15982e4695d726064a074da
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/04/2021
ms.locfileid: "7750606"
---
# <a name="project-schedule-api-performance"></a>Performa API Jadwal proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-persediaan, penyebaran Lite - faktur penawaran hingga proforma, Project for the Web_

Topik ini memberikan informasi tentang tolok ukur performa API (antarmuka pemrograman aplikasi) jadwal Proyek dan mengidentifikasi praktik terbaik untuk penggunaan optimal.

## <a name="project-scheduling-service"></a>Layanan Penjadwalan proyek
Layanan Penjadwalan Proyek adalah layanan multi-penyewa yang berjalan di Microsoft Azure. ini didesain untuk meningkatkan interaksi dengan memberikan pengalaman cepat dan lancar saat pengguna mengerjakan proyek. Peningkatan ini dicapai dengan menerima permintaan perubahan, memprosesnya, dan kemudian dengan segera memberikan hasilnya. Layanan secara asinkron bertahan pada Dataverse dan tidak memblokir pengguna melakukan operasi lain.

API jadwal proyek mengandalkan Layanan Penjadwalan Proyek untuk menjalankan permintaan yang dijelaskan secara lebih rinci di bagian berikutnya dari topik ini.

API jadwal proyek dirancang untuk berfungsi dengan entitas WBS (struktur rincian kerja) berikut:

  - Project
  - Tugas Proyek
  - Dependensi Tugas Proyek
  - Anggota Tim Proyek
  - Penetapan Sumber Daya
  
Bidang standar dan bidang kustom didukung. Kecuali jika dinyatakan lain, semua operasi umum didukung, seperti membuat, memperbarui, dan menghapus. Untuk informasi lebih lanjut, lihat [Menggunakan API jadwal Proyek untuk melakukan operasi dan penjadwalan entitas](schedule-api-preview.md).

Sebagai bagian dari API jadwal Proyek, pola unit kerja telah ditambahkan. Pola ini dikenal sebagai OperationSet dan dapat digunakan ketika beberapa permintaan harus diproses dalam satu transaksi.

Ilustrasi berikut menunjukkan alur yang akan dialami oleh mitra bila fitur ini digunakan.

![Dataverse dan alur Layanan Penjadwalan proyek.](./media/dataverse-project-scheduling-service-flow.png)

**Langkah 1**: Klien membuat panggilan API ke titik akhir Protokol Data Terbuka (OData) di Dataverse untuk membuat OperationSet.

**Langkah 2**: Setelah OperationSet baru dibuat, nilai **OperationSetId** dihasilkan.

**Langkah 3**: Klien menggunakan nilai **OperationSetId** untuk membuat permintaan API jadwal Proyek lainnya. Hasilnya adalah permintaan buat, perbarui, atau hapus pada entitas penjadwalan. Setelah permintaan ini dibuat, validasi metadata dilakukan. Jika validasi gagal, permintaan dihentikan, dan kesalahan dikembalikan.

**Langkah 4a–4c**: Langkah ini menunjukkan fase ACCEPT. Klien memanggil **ExecuteOperationSetV1** API, yang mengirimkan semua perubahan ke Layanan Penjadwalan Proyek dalam satu kumpulan. Layanan Penjadwalan Proyek menjalankan validasi sendiri pada permintaan dalam kumpulan. Kegagalan validasi apa pun membatalkan kumpulan dan mengembalikan pengecualian ke pemanggil. Jika kumpulan berhasil diterima oleh Layanan Penjadwalan Proyek, status OperationSet diperbarui untuk menunjukkan fakta bahwa OperationSet sedang diproses oleh Layanan Penjadwalan Proyek.

**Langkah 5**: Langkah ini menunjukkan adalah fase PERSIST. Layanan Penjadwalan Proyek secara asinkron menulis kumpulan ke Dataverse dalam transaksi. Jika operasi penulisan berhasil, OperationSet ditandai sebagai **Selesai**. Kesalahan apa pun mengembalikan transaksi dan kumpulan, dan OperationSet ditandai sebagai **Gagal**

## <a name="performance-methodology"></a>Metodologi performa
Waktu eksekusi didefinisikan sebagai waktu dari panggilan ke **ExecuteOperationSetV1** API hingga Layanan Penjadwalan Proyek telah selesai ditulis ke Dataverse. Semua operasi menjalankan gabungan 2.200 kali dan pengukuran waktu eksekusi P99 dilaporkan. Operasi satu rekaman dan massal diukur.

Untuk operasi satu rekaman, OperationSet berisi satu permintaan. Untuk operasi massal, berisi 20, 50, atau 100 permintaan. Setiap ukuran massal dilaporkan secara terpisah.

Operasi ini berjalan pada penyebaran Project Operations Lite UR 15 di Amerika Utara.

## <a name="results"></a>Hasil
### <a name="create-operations"></a>Operasi buat
#### <a name="single-record-create-operations"></a>Operasi pembuatan rekaman tunggal
Tabel berikut menampilkan waktu eksekusi untuk pembuatan satu rekaman. Waktu adalah dalam detik.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Jenis&nbsp;&nbsp;&nbsp;rekaman</th>
    <th class="tg-0lax" colspan="2">Waktu</th>
  </tr>
  <tr>
    <th class="tg-0lax">Bidang yang diperlukan</th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Penugasan</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Anggota Tim</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependensi</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operasi pembuatan Massal
Tabel berikut menampilkan waktu eksekusi untuk pembuatan banyak rekaman. Khususnya, Microsoft mengukur waktu eksekusi untuk pembuatan 20, 50, dan 100 rekaman di satu OperationSet. Waktu adalah dalam detik.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Jenis&nbsp;&nbsp;&nbsp;rekaman</th>
    <th class="tg-0lax" colspan="6">Waktu</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 Rekaman</th>
    <th class="tg-0lax" colspan="2">50 Rekaman</th>
    <th class="tg-0lax" colspan="2">100 Rekaman</th>
  </tr>
  <tr>
    <th class="tg-0lax">Bidang yang diperlukan</th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
    <th class="tg-0lax">Bidang yang diperlukan</th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
    <th class="tg-0lax">Bidang yang diperlukan</th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Penugasan</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependensi</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Operasi pembuatan massal pada entitas **Proyek** dan **Anggota Tim** tidak tercakup dalam tabel ini, karena runtime untuk operasi tersebut akan mirip runtime saat API untuk membuat rekaman tunggal dipanggil beberapa kali. API ini akan segera dijalankan dalam Dataverse.

Ilustrasi berikut menampilkan plot waktu eksekusi untuk entitas **Tugas**, **Penugasan**, dan **Dependensi** bila 20, 50, dan 100 rekaman dibuat dan semua bidang yang didukung digunakan.

![Membuat grafik waktu eksekusi rekaman.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Operasi perbarui
#### <a name="single-record-update-operations"></a>Operasi perbarui rekaman tunggal
Tabel berikut menampilkan waktu eksekusi untuk memperbarui satu rekaman. Waktu adalah dalam detik.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Jenis&nbsp;&nbsp;&nbsp;rekaman</th>
    <th class="tg-0lax" colspan="2">Waktu</th>
  </tr>
  <tr>
    <th class="tg-0lax">Bidang yang diperlukan </th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Anggota Tim</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operasi pembaruan pada entitas **Penetapan Sumber Daya** dan **Dependensi Tugas Proyek** tidak didukung.

#### <a name="bulk-update-operations"></a>Operasi perbarui Massal
Tabel berikut menampilkan waktu eksekusi untuk perbarui banyak rekaman. Khususnya, Microsoft mengukur waktu eksekusi untuk memperbarui 20, 50, dan 100 rekaman di satu OperationSet. Waktu adalah dalam detik.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Jenis&nbsp;&nbsp;&nbsp;rekaman</th>
    <th class="tg-0lax" colspan="6">Waktu</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 Rekaman</th>
    <th class="tg-0lax" colspan="2">50 Rekaman</th>
    <th class="tg-0lax" colspan="2">100 Rekaman</th>
  </tr>
  <tr>
    <th class="tg-0lax">Bidang yang diperlukan</th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
    <th class="tg-0lax">Bidang yang diperlukan</th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
    <th class="tg-0lax">Bidang yang diperlukan</th>
    <th class="tg-0lax">Semua bidang yang Didukung</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Anggota Tim</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operasi pembaruan pada entitas **Penetapan Sumber Daya** dan **Dependensi Tugas Proyek** tidak didukung.

Ilustrasi berikut menampilkan plot waktu eksekusi untuk entitas Tugas dan Anggota Tim bila 20, 50, dan 100 rekaman diperbarui dan semua bidang yang didukung digunakan.

![Memperbarui grafik waktu eksekusi rekaman.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operasi hapus
#### <a name="single-record-delete-operations"></a>Operasi hapus rekaman tunggal
Tabel berikut menampilkan waktu eksekusi untuk penghapusan satu rekaman. Waktu adalah dalam detik.

| Jenis rekaman | Waktu  |
|-------------|-------|
| Tugas        | 20.12 |
| Penugasan  | 10.86 |
| Anggota Tim | 12.52 |
| Dependensi  | 20.89 |

> [!NOTE]
> Operasi hapus di entitas **Proyek** tidak didukung.

#### <a name="bulk-delete-operations"></a>Operasi Penghapusan Massal
Tabel berikut menampilkan waktu eksekusi untuk penghapusan banyak rekaman. Khususnya, Microsoft mengukur waktu eksekusi untuk penghapusan 20, 50, dan 100 rekaman di satu OperationSet. Waktu adalah dalam detik.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Jenis&nbsp;&nbsp;&nbsp;rekaman</th>
    <th class="tg-0lax" colspan="3">Waktu</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 Rekaman</th>
    <th class="tg-0lax">50 Rekaman</th>
    <th class="tg-0lax">100 Rekaman</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Tugas</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Penugasan</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Anggota Tim</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Dependensi</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Operasi hapus di entitas **Proyek** tidak didukung.

Ilustrasi berikut menampilkan plot waktu eksekusi untuk entitas **Tugas**, **Penugasan**, **anggota Tim** dan **Dependensi** bila 20, 50, dan 100 rekaman dihapus.

![Hapus grafik waktu eksekusi rekaman.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Pengamatan
Untuk setiap operasi rekaman, **ExecuteOperationSet** API memerlukan sekitar 800 milidetik untuk mengirim permintaan ke Layanan Penjadwalan Proyek. Layanan Penjadwalan Proyek kemudian memerlukan waktu sekitar lima detik untuk memproses muatan dan memanggil Dataverse. Sisa waktu eksekusi digunakan untuk menjalankan logika bisnis dan menulis data ke database dalam Dataverse.

Ketika 100 rekaman dibuat, diperbarui, atau dihapus, **ExecuteOperationSet** API memerlukan waktu sekitar tiga detik untuk mengirim permintaan ke Layanan Penjadwalan Proyek. Layanan Penjadwalan Proyek kemudian memerlukan waktu sekitar lima detik untuk memproses permintaan dan memanggil Dataverse. Operasi massal harus membayar **pajak layanan penjadwalan proyek** satu kali, untuk semua rekaman di OperationSet. Oleh karena itu, operasi massal memiliki waktu eksekusi rata-rata yang jauh lebih rendah daripada operasi rekaman tunggal.

## <a name="scenarios"></a>Skenario
Tabel berikut menampilkan waktu eksekusi saat API jadwal proyek digunakan untuk mencapai skenario tertentu. Waktu adalah dalam detik.

| Skenario                                                                   | Waktu  |
|----------------------------------------------------------------------------|-------|
| Buat proyek yang memiliki 40 tugas.                                      | 36.01 |
| Buat proyek yang memiliki 40 tugas dan 20 dependensi.                  | 38.11 |
| Buat proyek yang memiliki 40 tugas dan 30 penugasan.                   | 60.17 |
| Buat proyek yang memiliki 40 tugas, 20 dependensi, dan 30 penugasan. | 60.27 |

## <a name="best-practices"></a>Praktik terbaik
Berdasarkan hasil skenario yang berat, API berkinerja lebih baik dalam kondisi berikut:

  - Kelompokkan operasi sebanyak mungkin. Runtime rata-rata untuk operasi massal lebih baik daripada runtime rata-rata untuk operasi rekaman tunggal. Semakin kecil jumlah OperationSets yang digunakan, semakin cepat waktu eksekusi rata-rata.
  - Atur hanya atribut minimum yang diperlukan untuk mencapai skenario Anda. Selektiflah tentang jenis bidang yang tidak diperlukan yang tercakup dalam permintaan OperationSet. Bidang yang berisi kunci asing atau bidang rollup akan mempengaruhi kinerja secara negatif.

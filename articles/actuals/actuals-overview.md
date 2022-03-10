---
title: Aktual
description: Pembaruan topik ini menyediakan informasi tentang cara bekerja dengan aktual di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a086fe0be67c21ed73793b6f3b58b47ad08eaa4e8a4c98870b4b2264562e3dce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6991805"
---
# <a name="actuals"></a>Aktual 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-stok, penyebaran Lite -menangani faktur proforma_

Aktual menunjukkan progres keuangan dan jadwal yang ditinjau dan disetujui pada proyek. Entri dibuat sebagai hasil dari persetujuan waktu, pengeluaran, entri penggunaan bahan, serta entri jurnal dan faktur.

## <a name="journal-lines-and-time-submission"></a>Baris jurnal dan penyerahan waktu

Untuk informasi lebih lanjut tentang entri waktu, lihat [Ikhtisar entri waktu](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Waktu dan Material

Bila entri waktu yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.

### <a name="fixed-price"></a>Harga Tetap

Jika entri waktu yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.

### <a name="default-pricing"></a>Harga default

Logika untuk membuat harga default berada pada baris jurnal. Nilai bidang dari entri waktu akan disalin ke baris jurnal. Nilai ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.

Bidang yang mempengaruhi harga default, seperti **peran** dan **unit sumber daya**, digunakan untuk menentukan harga yang sesuai untuk dimasukkan secara default pada baris jurnal. Anda dapat menambahkan bidang kustom pada entri waktu. Jika Anda menginginkan nilai bidang disebarkan ke aktual, buat bidang dalam tabel **Aktual** dan **Baris Jurnal**. Gunakan kode kustom untuk menyebarkan nilai bidang yang dipilih dari Entri Waktu ke Aktual melalui baris jurnal menggunakan asal transaksi. Untuk informasi lebih lanjut tentang asal transaksi dan koneksi, lihat [Menautkan Aktual ke rekaman asli](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Baris jurnal dan pengajuan pengeluaran dasar

Untuk informasi lebih lanjut tentang entri pengeluaran, lihat [Ikhtisar pengeluaran](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Waktu dan Material

Bila entri pengeluaran dasar yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.

### <a name="fixed-price"></a>Harga Tetap

Jika entri pengeluaran dasar yang diajukan ditautkan ke suatu proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.

### <a name="default-pricing"></a>Harga default

Logika untuk memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran. Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai. Bidang yang mempengaruhi harga default, seperti **Kategori transaksi** dan **unit**, digunakan untuk menentukan harga yang sesuai untuk dimasukkan secara default pada baris jurnal. Namun, hal ini hanya berfungsi bila metode harga dalam daftar harga adalah **Harga per unit**. Jika metode harga **Pada biaya** atau **Markup atas biaya**, harga yang dimasukkan saat entri pengeluaran dibuat akan digunakan untuk biaya dan harga pada baris jurnal penjualan dihitung berdasarkan metode penetapan harga. 

Anda dapat menambahkan bidang kustom pada entri pengeluaran. Jika Anda menginginkan nilai bidang disebarkan ke aktual, buat bidang dalam tabel **Aktual** dan **Baris Jurnal**. Gunakan kode kustom untuk menyebarkan nilai bidang yang dipilih dari Entri Waktu ke Aktual melalui baris jurnal menggunakan asal transaksi. Untuk informasi lebih lanjut tentang asal transaksi dan koneksi, lihat [Menautkan Aktual ke rekaman asli](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Pengajuan Baris jurnal dan log penggunaan bahan

Untuk informasi lebih lanjut tentang entri pengeluaran, lihat [Log Penggunaan Bahan](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Waktu dan Material

Bila entri log penggunaan bahan yang diajukan ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan bahan, sistem membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum tertagih.

### <a name="fixed-price"></a>Harga Tetap

Jika entri log penggunaan bahan yang diajukan ditautkan ke suatu proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.

### <a name="default-pricing"></a>Harga default

Logika untuk memasukkan harga default untuk bahan didasarkan pada kombinasi produk dan unit. Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai. Bidang yang mempengaruhi harga default, seperti **ID produk** dan **unit**, digunakan untuk menentukan harga yang sesuai untuk dimasukkan secara default pada baris jurnal. Namun, ini hanya berfungsi untuk produk katalog. Untuk produk pilihan, harga yang dimasukkan saat entri log penggunaan bahan dibuat digunakan untuk biaya dan harga penjualan di baris jurnal. 

Anda dapat menambahkan bidang kustom pada entri **Log Penggunaan Bahan**. Jika Anda menginginkan nilai bidang disebarkan ke aktual, buat bidang dalam tabel **Aktual** dan **Baris Jurnal**. Gunakan kode kustom untuk menyebarkan nilai bidang yang dipilih dari Entri Waktu ke Aktual melalui baris jurnal menggunakan asal transaksi. Untuk informasi lebih lanjut tentang asal transaksi dan koneksi, lihat [Menautkan Aktual ke rekaman asli](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Menggunakan jurnal entri untuk mencatat biaya

Anda dapat menggunakan jurnal entri untuk merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak. Jurnal dapat digunakan untuk tujuan berikut:

- Pindahkan aktual transaksi dari sistem lain ke Microsoft Dynamics 365 Project Operations.
- Mencatat biaya yang terjadi di sistem lain. Biaya ini dapat mencakup biaya pengadaan atau subkontrak.

> [!IMPORTANT]
> Aplikasi tidak memvalidasi jenis baris jurnal atau harga terkait yang dimasukkan pada baris jurnal. Oleh karena itu, hanya pengguna yang sepenuhnya menyadari dampak akuntansi yang dimiliki aktual pada proyeklah yang harus menggunakan jurnal entri untuk membuat aktual. Karena dampak jenis jurnal ini, Anda harus hati-hati memilih siapa yang memiliki akses untuk membuat jurnal entri.

## <a name="record-actuals-based-on-project-events"></a>Mencatat aktual berdasarkan aktivitas proyek

Project Operations mencatat transaksi keuangan yang terjadi selama proyek berlangsung. Transaksi ini direkam sebagai aktual Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek

<table>
<thead>
<tr>
<th rowspan="3">Aktivitas</th>
<th colspan="4">Proyek yang dapat ditagih atau dijual</th>
<th rowspan="3">Proyek dalam tahap pra-penjualan</th>
<th rowspan="3">Proyek internal</th>
</tr>
<tr>
<th colspan="2">Waktu dan Material</th>
<th colspan="2">Harga Tetap</th>
</tr>
<tr>
<th>Aktual</th>
<th>mata uang transaksi</th>
<th>Harga Tetap</th>
<th>mata uang transaksi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Entri Waktu dibuat.</td>
<td colspan="6">Tidak ada aktivitas di entitas aktual</td>
</tr>
<tr>
<td>Entri Waktu diajukan.</td>
<td colspan="6">Tidak ada aktivitas di entitas aktual</td>
</tr>
<tr>
<td rowspan="2">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</td>
<td>Biaya Aktual</td>
<td>Mata uang Unit Kontrak</td>
<td rowspan="2">Biaya Aktual</td>
<td rowspan="2">Mata uang Unit Kontrak
<td rowspan="2">Biaya Aktual</td>
<td rowspan="2">Biaya Aktual</td>
</tr>
<tr>
<td>Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="3">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</td>
<td>Biaya Aktual</td>
<td>Mata uang Unit Kontrak</td>
<td rowspan="3">Biaya Aktual</td>
<td rowspan="3">Mata uang Unit Kontrak</td>
<td rowspan="3">Biaya Aktual</td>
<td rowspan="3">Biaya Aktual</td>
</tr>
<tr>
<td>Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="2">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</td>
<td>Pembalikan penjualan yang tidak ditagih</td>
<td>Mata uang Kontrak Proyek</td>
<td rowspan="2">Penjualan yang ditagih untuk tonggak waktu</td>
<td rowspan="2">Mata uang Kontrak Proyek</td>
<td rowspan="2">Tidak berlaku</td>
<td rowspan="2">Tidak berlaku</td>
</tr>
<tr>
<td>Penjualan yang Ditagih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="3">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</td>
<td>Pembalikan penjualan yang tidak ditagih</td>
<td>Mata uang Kontrak Proyek</td>
<td rowspan="3">Tidak berlaku</td>
<td rowspan="3">Tidak berlaku</td>
<td rowspan="3">Tidak berlaku</td>
<td rowspan="3">Tidak berlaku</td>
</tr>
<tr>
<td>Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="2">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</td>
<td>penjualan tertagih – Pembalikan</td>
<td>Mata uang Kontrak Proyek</td>
<td rowspan="5">
<ul>
<li>Pembalikan penjualan yang ditagih untuk tonggak waktu</li>
<li>Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></li>
</ul>
</td>
<td rowspan="5">Mata uang Kontrak Proyek</td>
<td rowspan="5">Tidak berlaku</td>
<td rowspan="5">Tidak berlaku</td>
</tr>
<tr>
<td>Penjualan yang Ditagih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="3">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</td>
<td>penjualan tertagih – Pembalikan</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Penjualan Tertagih untuk kuantitas baru</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek

<table>
<thead>
<tr>
<th rowspan="3">Aktivitas</th>
<th colspan="4">Proyek yang dapat ditagih atau dijual</th>
<th rowspan="3">Proyek dalam tahap pra-penjualan</th>
<th rowspan="3">Proyek internal</th>
</tr>
<tr>
<th colspan="2">Waktu dan Material</th>
<th colspan="2">Harga Tetap</th>
</tr>
<tr>
<th>Aktual</th>
<th>mata uang transaksi</th>
<th>Harga Tetap</th>
<th>mata uang transaksi</th>
</tr>
</thead>
<tbody>
<tr>
<td>Entri Waktu dibuat.</td>
<td colspan="6">Tidak ada aktivitas di entitas aktual</td>
</tr>
<tr>
<td>Entri Waktu diajukan.</td>
<td colspan="6">Tidak ada aktivitas di entitas aktual</td>
</tr>
<tr>
<td rowspan="4">Waktu disetujui, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi selama persetujuan.</td>
<td>Biaya Aktual</td>
<td>Mata uang Unit Kontrak</td>
<td rowspan="4">Biaya Aktual</td>
<td rowspan="4">Mata uang Unit Kontrak</td>
<td rowspan="4">Biaya Aktual</td>
<td rowspan="4">Biaya Aktual</td>
</tr>
<tr>
<td>Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Biaya Unit Sumber Daya</td>
<td>Mata uang Unit Sumber Daya</td>
</tr>
<tr>
<td>Penjualan Interorganisasi</td>
<td>Mata uang Unit Kontrak</td>
</tr>
<tr>
<td rowspan="5">Waktu disetujui, dan penurunan dalam jam yang dapat ditagih terjadi selama persetujuan.</td>
<td>Biaya Aktual</td>
<td>Mata uang Unit Kontrak</td>
<td rowspan="5">Biaya Aktual</td>
<td rowspan="5">Mata uang Unit Kontrak</td>
<td rowspan="5">Biaya Aktual</td>
<td rowspan="5">Biaya Aktual</td>
</tr>
<tr>
<td>Biaya Unit Sumber Daya</td>
<td>Mata uang Unit Sumber Daya</td>
</tr>
<tr>
<td>Penjualan Interorganisasi</td>
<td>Mata uang Unit Kontrak</td>
</tr>
<tr>
<td>Aktual penjualan Belum Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Aktual penjualan Belum Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="2">Faktur dikonfirmasi, dan tidak ada perubahan atau peningkatan dalam jam yang dapat ditagih terjadi.</td>
<td>Pembalikan penjualan yang tidak ditagih</td>
<td>Mata uang Kontrak Proyek</td>
<td rowspan="2">Penjualan yang ditagih untuk tonggak waktu</td>
<td rowspan="2">Mata uang Kontrak Proyek</td>
<td rowspan="2">Tidak berlaku</td>
<td rowspan="2">Tidak berlaku</td>
</tr>
<tr>
<td>Penjualan yang Ditagih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="3">Faktur dikonfirmasi, dan penurunan dalam jam yang dapat ditagih terjadi.</td>
<td>Pembalikan penjualan yang tidak ditagih</td>
<td>Mata uang Kontrak Proyek</td>
<td rowspan="3">Tidak berlaku</td>
<td rowspan="3">Tidak berlaku</td>
<td rowspan="3">Tidak berlaku</td>
<td rowspan="3">Tidak berlaku</td>
</tr>
<tr>
<td>Penjualan Tertagih – Dapat Dikenakan Biaya untuk kuantitas baru</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Penjualan Tertagih – Tidak Dapat Dikenakan Biaya untuk selisih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="2">Faktur diperbaiki untuk meningkatkan kuantitas yang dikenai biaya.</td>
<td>penjualan tertagih – Pembalikan</td>
<td>Mata uang Kontrak Proyek</td>
<td rowspan="5">
<ul>
<li>Pembalikan penjualan yang ditagih untuk tonggak waktu</li>
<li>Perubahan status tonggak waktu dari <strong>ditagih</strong> ke <strong>siap untuk faktur</strong></li>
</ul>
</td>
<td rowspan="5">Mata uang Kontrak Proyek</td>
<td rowspan="5">Tidak berlaku</td>
<td rowspan="5">Tidak berlaku</td>
</tr>
<tr>
<td>Penjualan yang Ditagih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td rowspan="3">Faktur diperbaiki untuk menurunkan kuantitas yang dikenai biaya.</td>
<td>penjualan tertagih – Pembalikan</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Penjualan Tertagih untuk kuantitas baru</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
<tr>
<td>Penjualan Tidak Tertagih – Dapat Dikenakan Biaya untuk selisih</td>
<td>Mata uang Kontrak Proyek</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

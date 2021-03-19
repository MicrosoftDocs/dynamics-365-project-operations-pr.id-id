---
title: Aktual
description: Pembaruan topik ini menyediakan informasi tentang cara bekerja dengan aktual di Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291803"
---
# <a name="actuals"></a>Aktual 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Nilai aktual adalah jumlah pekerjaan yang telah diselesaikan pada suatu proyek. Mereka dibuat sebagai hasil dari entri waktu dan pengeluaran, serta entri jurnal dan faktur.

## <a name="journal-lines-and-time-submission"></a>Baris jurnal dan penyerahan waktu

Untuk informasi lebih lanjut tentang entri waktu, lihat [Ikhtisar entri waktu](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Waktu dan Material

Bila entri waktu yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.

### <a name="fixed-price"></a>Harga Tetap

Jika entri waktu yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.

### <a name="default-pricing"></a>Harga default

Logika untuk membuat harga default berada pada baris jurnal. Nilai bidang dari entri waktu akan disalin ke baris jurnal. Nilai ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai.

Bidang yang mempengaruhi harga default, seperti **peran** dan **unit organisasi**, digunakan untuk menentukan harga yang sesuai pada baris jurnal. Anda dapat menambahkan bidang kustom pada entri waktu. Jika Anda ingin nilai bidang diterapkan ke aktual, buat bidang pada entitas aktual, dan gunakan pemetaan bidang untuk menyalin bidang dari entri waktu ke aktual.

## <a name="journal-lines-and-basic-expense-submission"></a>Baris jurnal dan pengajuan pengeluaran dasar

Untuk informasi lebih lanjut tentang entri pengeluaran, lihat [Ikhtisar pengeluaran](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Waktu dan Material

Bila entri pengeluaran dasar yang dikirim ditautkan ke proyek yang dipetakan ke baris kontrak waktu dan material, sistem akan membuat dua baris jurnal, satu untuk biaya dan satu untuk penjualan yang belum ditagih.

### <a name="fixed-price"></a>Harga Tetap

Jika entri pengeluaran dasar yang diajukan tertaut ke proyek yang dipetakan ke baris kontrak waktu harga tetap, sistem membuat satu baris jurnal untuk biaya.

### <a name="default-pricing"></a>Harga default

Logika untuk memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran. Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai. Namun, per default, jumlah yang dimasukkan untuk harga itu sendiri diatur secara langsung pada baris jurnal pengeluaran terkait untuk biaya dan penjualan.

Entri berdasarkan Kategori dari harga default per unit pada entri pengeluaran tidak tersedia.

## <a name="use-entry-journals-to-record-costs"></a>Menggunakan jurnal entri untuk mencatat biaya

Anda dapat menggunakan jurnal entri untuk merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak. Jurnal dapat digunakan untuk tujuan berikut:

- Mencatat biaya aktual material dan penjualan pada proyek.
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
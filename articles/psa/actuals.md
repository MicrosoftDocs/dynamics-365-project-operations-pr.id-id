---
title: Sekilas aktual
description: Topik ini menyediakan informasi tentang nilai aktual proyek.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129772"
---
# <a name="actuals-overview"></a>Sekilas aktual

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Nilai aktual adalah jumlah pekerjaan yang telah diselesaikan pada suatu proyek. Aktual proyek dapat ditelusuri kembali ke dokumen sumbernya. Dokumen sumber mencakup waktu, pengeluaran, dan entri jurnal, serta juga faktur.

![Bagaimana aktual proyek dilacak ke dokumen sumber](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Mengajukan entri waktu

Dalam PSA, bila entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat. Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih. Jika entri waktu diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya. 

Logika untuk memasukkan harga default berada pada baris jurnal. Semua nilai bidang dari entri waktu akan disalin ke baris jurnal. Bidang ini mencakup tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan hasil mata uang dalam daftar harga yang sesuai. 

Bidang yang mempengaruhi harga default, seperti **peran** dan **unit organisasi**, menyebabkan harga yang sesuai untuk dimasukkan secara default pada baris jurnal. Jika Anda menambahkan bidang kustom pada entri waktu, dan Anda ingin nilai bidang diterapkan ke aktual, buat bidang pada entitas aktual, dan gunakan pemetaan bidang untuk menyalin bidang dari entri waktu ke aktual.

## <a name="submitting-an-expense-entry"></a>Mengirimkan entri pengeluaran

Dalam PSA, bila entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu dan bahan, dua baris jurnal dibuat. Satu baris adalah untuk biaya, dan baris lainnya adalah untuk penjualan yang belum ditagih. Jika entri pengeluaran diajukan untuk proyek yang dipetakan ke baris kontrak waktu harga tetap, baris jurnal dibuat hanya untuk biaya.

Logika memasukkan harga default untuk pengeluaran didasarkan pada kategori pengeluaran yang dipilih pada halaman **entri pengeluaran**. Tanggal transaksi, baris kontrak yang dipetakan ke proyek, dan mata uang semua digunakan untuk menentukan daftar harga yang sesuai. Namun, untuk harga itu sendiri, jumlah yang dimasukkan pengguna diatur secara langsung pada baris jurnal pengeluaran terkait untuk biaya dan penjualan secara default.

Di versi saat ini PSA, entri berdasarkan Kategori dari harga default per unit pada entri pengeluaran tidak tersedia.

## <a name="using-entry-journals-to-record-costs"></a>Menggunakan jurnal entri untuk mencatat biaya

Dalam PSA, jurnal entri memungkinkan Anda merekam biaya atau pendapatan dalam materi, biaya, waktu, pengeluaran, atau kelas transaksi pajak. Jurnal memiliki header, baris, dan tindakan **konfirmasi**. Berikut adalah beberapa skenario di mana Anda dapat menggunakan jurnal:

- Anda harus mencatat biaya aktual material dan penjualan pada proyek.
- Anda harus memindahkan aktual transaksi dari sistem lain ke PSA.
- Anda harus mencatat biaya yang terjadi di sistem lain, seperti biaya pengadaan atau subkontrak.

> [!IMPORTANT]
> Menggunakan jurnal entri untuk membuat aktual harus dilakukan hanya oleh pengguna yang sepenuhnya menyadari dampak akuntansi yang dimiliki aktual pada proyek. Hal ini karena aplikasi tidak memvalidasi jenis baris jurnal, atau harga terkait yang dimasukkan pada baris jurnal. Karena dampak jenis jurnal ini, berhati-hatilah tentang siapa yang diberi akses untuk membuat jurnal entri.     


## <a name="recording-actuals-based-on-project-events"></a>Aktual rekaman berdasarkan aktivitas proyek

PSA mencatat transaksi keuangan yang terjadi selama proyek berlangsung. Transaksi ini direkam sebagai **aktual** Tabel berikut Menampilkan jenis aktual yang berbeda yang dibuat, tergantung apakah proyek adalah proyek waktu dan bahan atau proyek harga tetap, dalam tahap pra-penjualan, atau merupakan proyek internal.

**Sumber daya adalah milik unit organisasi yang sama dengan unit kontrak proyek**

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

**Sumber daya adalah milik unit organisasi yang berbeda dengan unit kontrak proyek**

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

---
title: Yang baru di bulan Oktober 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Oktober 2022 Microsoft Dynamics 365 Project Operations untuk skenario berbasis sumber daya/tidak stok.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806727"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Oktober 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.57.0.176
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.30

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

| Area fitur | Nama fitur | Informasi selengkapnya |
| --- | --- | --- |
| Perencanaan dan Pelacakan Proyek | **Penjadwalan Eksternal Operasi Proyek**<br>Mode penjadwalan eksternal memungkinkan pelanggan membuat, memperbarui, dan menghapus entitas yang terkait dengan struktur rincian kerja (WBS) secara native dengan menggunakan API asli Dataverse , tanpa batas saat ini yang diberlakukan oleh Project for the Web. | [Penjadwalan Eksternal](/dynamics365/project-operations/project-management/external-scheduling) |
| Penyebaran dan Konfigurasi | <p>**Izinkan pelanggan memilih jenis penyebaran**<br>Pembaruan berbasis produk (PDU) dari Operasi Proyek digunakan untuk menginstal solusi Penulisan ganda Operasi Proyek secara otomatis saat solusi inti dan orkestrasi tulis ganda diinstal di lingkungan.</p><p>Fitur ini memperkenalkan parameter perilaku **peningkatan Solusi baru** di parameter Project. Ketika parameter ini diatur ke **Lite saja**, PUD tidak akan lagi secara otomatis menginstal solusi Project Operations Dual-write, bahkan jika solusi inti dan orkestrasi Dual-write diinstal di lingkungan. Perilaku ini akan menguntungkan pelanggan yang berencana menggunakan solusi Dual-write untuk mengintegrasikan pesanan penjualan ke dalam aplikasi keuangan dan operasi, tetapi ingin menggunakan Operasi Proyek dalam mode Lite (yaitu, tanpa integrasi ke dalam aplikasi keuangan dan operasi).</p> | |
| Penagihan dan Harga | <p>**Konversi mata uang untuk transaksi penjualan yang tidak ditagih di lingkungan Terintegrasi**<br>Untuk pelanggan yang menggunakan Operasi Proyek yang terintegrasi dengan aplikasi keuangan dan operasi (yaitu, dalam jenis penyebaran sumber daya/non-stok), nilai tukar biasanya dikuasai dalam aplikasi keuangan dan operasi. Namun, jika kategori pengeluaran harus diberi harga dengan menggunakan metode perhitungan harga "at cost" atau "markup over cost" saat pelanggan ditagih, nilai tukar yang digunakan untuk menghitung jumlah penjualan menggunakan nilai tukar, bukan nilai Dataverse tukar dari aplikasi keuangan dan operasi.</p><p>Fitur ini memperkenalkan parameter Perilaku **konversi mata uang baru** di parameter Project. Ketika parameter ini diatur ke **Diperpanjang dengan fallback**, jumlah penjualan yang tidak ditagih pada transaksi pengeluaran dihitung dengan menggunakan nilai tukar dari aplikasi keuangan dan operasi.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2316317 | Sistem ini memungkinkan pembuatan faktur yang tidak memiliki transaksi yang dikenakan biaya. |
| Penagihan dan Harga | 2737300 | Validasi ketersediaan **bidang Pelanggan** sebelum formulir diakses. |
| Penagihan dan Harga | 2744948 | Tambahkan pemeriksaan nol untuk Metode penagihan. |
| Penagihan dan Harga | 2763515 | Kesalahan referensi nol menangani ketika kontrak penjualan faktur hilang. |
| Penagihan dan Harga | 2844301 | Pembuatan faktur batch gagal karena kesalahan. |
| Penagihan dan Harga | 2845869 | Penyimpanan Layanan Organisasi salah. |
| Penagihan dan Harga | 2853729 | Detail Peran dan Harga diperbarui saat Jenis penagihan diubah. |
| Penagihan dan Harga | 2940350 | Ketika aktual diberi harga, hanya daftar harga aktif yang harus dimasukkan secara otomatis. |
| Penyebaran dan Konfigurasi | 3001206 | Entitas replaylogheader msdyn\_ mencegah peningkatan Organisasi Pelanggan. |
| Manajemen peluang | 2755582 | Pengecualian referensi null menangani di Pembantu Aturan Penagihan Terpisah. |
| Manajemen peluang | 2761477 | Saat penagihan terpisah digunakan, penghapusan tonggak (header) meninggalkan tonggak yatim piatu. |
| Manajemen peluang | 2767595 | Saat catatan penggunaan material dibuka dalam formulir utama, sumber daya yang dapat dipesan untuk catatan diubah menjadi pengguna yang saat ini masuk. |
| Perencanaan dan Pelacakan Proyek | 2790384 | Batas waktu Operating Set yang Tertunda terlalu singkat. |
| Perencanaan dan Pelacakan Proyek | 2957840 | Tugas tidak dapat disimpan dan kolom tidak dapat ditambahkan ke **halaman Tugas** di Operasi Proyek Terintegrasi. |
| Manajemen sumber daya | 2751560 | Unit Organisasi Pilihan yang Tidak Konsisten dalam Kebutuhan Sumber Daya. |
| Membuat subkontrak | 2853245 | Pencocokan untuk aktual Vendor Invoice Line tidak memperbarui status verifikasi jika baris kontrak sudah ditautkan ke baris faktur vendor. |
| Membuat subkontrak | 2907231 | Tahap proses faktur vendor tidak dapat maju. |
| Waktu dan Pengeluaran | 2867363 | Catatan tidak keluar dari tampilan Absen/Liburan untuk Persetujuan saat mereka mengantre untuk persetujuan. |
| Waktu dan Pengeluaran | 2894405 | TESA: Direktori POC yang tidak digunakan menyebabkan masalah kepatuhan. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

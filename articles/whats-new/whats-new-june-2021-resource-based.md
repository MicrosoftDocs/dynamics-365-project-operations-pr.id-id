---
title: Yang baru di bulan Juni 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Topik ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam skenario Project Operations yang dirilis Pada Bulan Juni 2021 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 21a446fdb9526c1a2b110c5368516dafb64b5e01
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600792"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Juni 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

- Project Operations di lingkungan Dynamics 365 Dataverse versi 4.11.0.156 or 4.11.0.164.
- Manajemen proyek dan akuntansi di lingkungan aplikasi Keuangan dan Operasi versi 10.0.19.

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- Kemampuan untuk menghapus [baris proposal faktur proyek untuk skenario penyesuaian](../invoicing/correct-project-invoice-proposals.md).
- Baris pengeluaran terperinci mencerminkan nama subkategori dalam laporan pengeluaran [Fitur Baru Nuansa Baru Laporan Pengeluaran](../expense/expense-reports-reimagined.md#new-features).
- Metode pembayaran tersedia di panel pengeluaran baru saat membuat pengeluaran baru.
- Ketersediaan umum API jadwal Proyek. Fungsi baru ini memungkinkan pelanggan melakukan operasi pembuatan, pembaruan, dan penghapusan secara programatik pada tugas proyek, penetapan sumber daya, dependensi tugas, dan rekaman anggota tim proyek. Untuk informasi lebih lanjut, lihat [Menggunakan API jadwal Proyek untuk melakukan operasi dengan penjadwalan entitas](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. 

Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi aplikasi Keuangan dan Operasi. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta pada halaman **Penulisan ganda** pada kolom **Versi**. Aktifkan versi baru peta dengan memilih **versi peta Tabel**, memilih versi terbaru, lalu menyimpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Yang Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) di panduan pemecahan masalah Penulisan Ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan Harga | 2281417 | Memperbaiki masalah kegagalan tindakan pembuatan faktur otomatis melalui jadwal faktur. |
| Penagihan dan Harga | 2287835 | Peningkatan performa konfirmasi faktur. |
| Manajemen peluang | 2222555 | Kelayakan penagihan perkiraan bahan harus disalin dengan benar ke detail baris kuotasi saat menggunakan **Impor dari Estimasi Proyek**. |
| Manajemen peluang | 2223427 | Penyesuaian sekarang diizinkan untuk tindakan, **GenerateRetainersFromRetainerScheduleOptions**. |
| Manajemen peluang | 2277528 | Memperbaiki Penghitungan nilai tahapan penagihan untuk baris kontrak proyek dengan beberapa pelanggan. |
| Perencanaan dan Pelacakan Proyek | 2226110 | Memperbaiki masalah intermiten dengan fungsi **Buat Persyaratan** di kisi **tim Proyek**. |
| Perencanaan dan Pelacakan Proyek | 2208109 | Pengguna tidak dapat membuat proyek dalam satu mata uang dengan tugas terkait dalam mata uang lain. |
| Perencanaan dan Pelacakan Proyek | 2258228 | Daftar bidang yang diizinkan untuk dimodifikasi dengan entitas **Penjadwalan** yang menggunakan API Jadwal telah diperbarui. |
| Perencanaan dan Pelacakan Proyek | 2293989 | Pengaturan bahasa dan regional yang benar harus diteruskan ke kisi **Tugas Proyek**. |
| Manajemen sumber daya | 2220493 | Memperbaiki pengalaman pengguna di kisi **Tugas** saat dengan cepat menandai permintaan sumber daya sebagai selesai. |
| Manajemen sumber daya | 2330496 | Memperbaiki masalah pemuatan **Papan Jadwal**. (Pembaruan kualitas tersedia di versi 4.11.0.164) |
| Waktu dan Pengeluaran | 2194431 | Kisi **entri Waktu** harus memperhatikan awal minggu sebagaimana diatur dalam **pengaturan Sistem**. |
| Waktu dan Pengeluaran | 2277311 | Setelah Anda menghapus nilai di sel pada kisi **entri Waktu**, kursor tetap berada di kisi. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Catatan formulir** dan **konfigurasi Formulir** tidak dapat dilihat dalam **konfigurasi manajemen proyek** di entitas hukum Finance yang terintegrasi dengan Project Operations. |
| Manajemen proyek dan akuntansi | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Deskripsi default untuk PPN kosong saat **memposting jenis** = **pajak penjualan** untuk voucer faktur proyek. |
| Manajemen proyek dan akuntansi | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Transaksi ganda diposting saat penagihan berbasis tugas digunakan di Dataverse dengan integrasi Project Operations. |
| Manajemen proyek dan akuntansi | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Persentase lengkap dalam pengakuan pendapatan salah saat menggunakan integrasi Project Operations. |
| Manajemen proyek dan akuntansi | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Akrual pendapatan digandakan pada faktur vendor tertunda dalam skenario terintegrasi Project Operations. |
| Manajemen proyek dan akuntansi | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Tidak dapat memposting jurnal integrasi saat aturan profil pendapatan diatur ke konfigurasi **Grup**. |
| Manajemen proyek dan akuntansi | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Faktur pembelian tidak dapat diposting untuk pesanan pembelian proyek yang memiliki baris dengan beberapa satuan pengukuran. |
| Manajemen proyek dan akuntansi | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Dimensi keuangan default pada proyek tidak dapat diperbarui menggunakan entitas data **V2** proyek. |
| Manajemen proyek dan akuntansi | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Proses batch untuk membuat estimasi proyek memerlukan waktu terlalu lama untuk diselesaikan. |
| Manajemen proyek dan akuntansi | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Menghapus kontrak juga akan menghapus alamat yang terkait dengan pelanggan. |
| Perjalanan dan Pengeluaran | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Kondisi alur kerja persetujuan laporan pengeluaran tidak dievaluasi dengan benar. |
| Perjalanan dan Pengeluaran | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Kebijakan laporan pengeluaran tidak mengevaluasi ID proyek dengan benar. |
| Perjalanan dan Pengeluaran | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Tindakan, **Pecah ke pribadi untuk transaksi pengeluaran antarperusahaan** tidak berfungsi dengan benar. |
| Perjalanan dan Pengeluaran | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Justifikasi baris laporan pengeluaran tidak sengaja dihapus ketika permintaan perjalanan tertentu dihapus. Hal ini terjadi ketika recID laporan pengeluaran dan permintaan perjalanan sama. |
| Perjalanan dan Pengeluaran | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Ada masalah dalam aplikasi seluler Pengeluaran saat bidang **ID Proyek** diperlukan dalam kebijakan laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Pengeluaran antarperusahaan yang terkait dengan proyek tidak dapat diedit. Namun, pesan kesalahan berikut menampilkan, "Referensi objek tidak diatur ke instans objek." |
| Perjalanan dan Pengeluaran | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Setelah laporan pengeluaran diposting, mata uang dan jumlah yang salah tercantum di buku besar pembantu. |
| Perjalanan dan Pengeluaran | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Peningkatan telah dilakukan pada fitur *Hapus transaksi kartu kredit*.  |
| Perjalanan dan Pengeluaran | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Pajak penjualan yang tercakup dalam laporan pengeluaran tidak secara konsisten dihitung bila mata uang pelaporan yang berbeda ditentukan dalam entitas hukum. |
| Perjalanan dan Pengeluaran | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Kinerja terpengaruh saat menambahkan pengeluaran perjalanan tunai baru. |
| Perjalanan dan Pengeluaran | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Aturan kebijakan pengeluaran tidak dipicu pada laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Mengunggah kategori bersama baru dengan menggunakan Kerangka Kerja Manajemen Data akan menghilangkan semua subkategori untuk semua kategori bersama. |
| Perjalanan dan Pengeluaran | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Ketika Anda membuat baris pengeluaran dan kemudian memilih kategori, pesan kesalahan berikut ditampilkan, "Kombinasi dari grup pajak penjualan DOM dan grup pajak penjualan item STD tidak valid." |
| Perjalanan dan Pengeluaran | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Ada masalah sinkronisasi di aplikasi seluler Pengeluaran. |

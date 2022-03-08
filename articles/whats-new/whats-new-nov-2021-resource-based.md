---
title: Yang baru di bulan November 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Ini topik memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Operasi Proyek November 2021 untuk skenario berbasis sumber daya / non-stok.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827330"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan November 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Topik ini berlaku untuk komponen dan versi Microsoft berikut Dynamics 365 Project Operations:

- Operasi Proyek dalam versi lingkungan Dataverse 4.26.0.145, 4.26.0.148, atau 4.26.0.150
- Manajemen proyek dan akuntansi dalam lingkungan Dynamics 365 Finance versi 10.0.22

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- Penjadwalan Proyek antarmuka pemrograman aplikasi (API) sekarang mendukung kemampuan untuk membuat dan menghapus bucket Project.

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi operasi proyek Dataverse dan versi solusi Keuangan Anda. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel di luar kotak, aplikasikan kembali perubahannya. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti petunjuk dalam [masalah kolom tabel yang hilang di bagian peta dari panduan pemecahan masalah](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) Dual-write.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-in-dataverse"></a>Operasi Proyek di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2240080 | Bidang **persyaratan Pembayaran tidak boleh** diduplikasi pada faktur pro forma. |
| Penagihan dan Harga | 2358236 | Koreksi faktur harus memungkinkan koreksi yang memiliki garis harga nol. |
| Manajemen sumber daya | 2410072 | Izinkan penyiapan sumber daya yang ditugaskan ke tugas sebagai manajer proyek. |
| Penagihan dan Harga | 2430234 | Memperbaiki masalah perhitungan kinerja biaya. |
| Waktu dan Pengeluaran | 2436978 | Perbolehkan waktu untuk dimasukkan dalam format hh:mm. |
| Penagihan dan Harga | 2448623 | Memungkinkan daftar harga diperbarui setelah dikaitkan dengan unit organisasi. |
| Waktu dan Pengeluaran | 2460396 | Biarkan entri waktu dihapus dengan membersihkan sel. |
| Penagihan dan Harga | 2467386 | Izinkan proyek yang memiliki tugas untuk dihapus, bahkan ketika tugas dikaitkan dengan kutipan yang dimenangkan. |
| Waktu dan Pengeluaran | 2461744 | **Tampilan persetujuan saya yang gagal hanya berisi persetujuan proyek dalam tahap Yang** **Dikirimkan**. |
| Waktu dan Pengeluaran | 2464082 | Hapus tautan dari persetujuan proyek ke tanggal persetujuan yang ditetapkan saat status target dicocokkan. |
| Waktu dan Pengeluaran | 2468108 | Pekerjaan Jadwal tidak boleh menetapkan **status Pemrosesan untuk set** persetujuan. |
| Waktu dan Pengeluaran | 2471503 | Hapus set persetujuan yang berusia tujuh hari. |
| Penagihan dan Harga | 2480687 | Referensi garis penawaran tidak boleh dihapus ketika tonggak garis penawaran dibuat. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di bidang Keuangan

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Jumlah vendor yang disimpan dalam transaksi biaya proyek tidak ditampilkan dalam daftar transaksi. |
| Manajemen proyek dan akuntansi | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktur vendor antar komplotany rusak saat integrasi faktur vendor diaktifkan. |
| Manajemen proyek dan akuntansi | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Ketentuan pembayaran pada faktur proyek tidak berfungsi seperti yang diharapkan. |
| Manajemen proyek dan akuntansi | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ketika retensi vendor dirilis, posting voucher memiliki baris tambahan yang salah. |
| Manajemen proyek dan akuntansi | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Ketika jurnal integrasi Operasi Proyek diposting, itu gagal karena dimensi yang hilang untuk akun yang tidak diposting. |
| Manajemen proyek dan akuntansi | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Proyek tidak dapat diedit pada faktur vendor yang tertunda saat kategori pengadaan ditetapkan ke** item. |
| Manajemen proyek dan akuntansi | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panel navigasi hilang jika Anda tidak masuk ke Dataverse Operasi Proyek. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Ketika Anda memposting pendapatan dari faktur proyek dalam kasus punggawa yang diterapkan, masalah terjadi karena transaksi pada voucher tidak seimbang. |
| Manajemen proyek dan akuntansi | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Pembuatan perkiraan setelah Anda memposting proposal faktur memblokir jalur koreksi dari impor. |
| Manajemen proyek dan akuntansi | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modifikasi catatan tonggak yang sepenuhnya ditagih seharusnya tidak mungkin dilakukan. |
| Perjalanan dan Pengeluaran | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua laporan pengeluaran terlihat saat Anda mencari kategori di aplikasi seluler Expense. |
| Perjalanan dan Pengeluaran | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah yang salah pada transaksi vendor dan transaksi pajak penjualan diposting dari biaya yang dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Peringatan yang tidak relevan terjadi ketika Anda menyegarkan **halaman laporan** Pengeluaran. |
| Perjalanan dan Pengeluaran | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pengakuisan interim yang salah digunakan ketika Anda menghapus approver sementara dan kemudian mengirimkan kembali laporan pengeluaran melalui alur kerja. |
| Perjalanan dan Pengeluaran | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Kesalahan posting yang terkait dengan pengaturan jarak tempuh terjadi. |

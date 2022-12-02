---
title: Yang baru di bulan November 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis November 2021 penyebaran Project Operations Lite untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932898"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan November 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.22

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- API (antarmuka pemrograman aplikasi) Penjadwalan proyek sekarang mendukung kemampuan untuk membuat dan menghapus Wadah proyek.

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-in-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2240080 | Bidang **Persyaratan pembayaran** tidak boleh diduplikasikan pada faktur pro forma. |
| Penagihan dan Harga | 2358236 | Koreksi faktur harus memungkinkan koreksi yang memiliki baris harga nol. |
| Manajemen sumber daya | 2410072 | memungkinkan pengaturan sumber daya yang ditetapkan ke tugas sebagai manajer proyek. |
| Penagihan dan Harga | 2430234 | Memperbaiki masalah perhitungan performa biaya. |
| Waktu dan Pengeluaran | 2436978 | Memungkinkan waktu untuk dimasukkan dalam format hh:mm. |
| Penagihan dan Harga | 2448623 | Memungkinkan daftar harga diperbarui setelah dikaitkan dengan unit organisasi. |
| Waktu dan Pengeluaran | 2460396 | Memungkin entri waktu dihapus dengan mengosongkan sel. |
| Penagihan dan Harga | 2467386 | Memungkinkan proyek yang memiliki tugas untuk dihapus, bahkan saat tugas dikaitkan dengan kuotasi menang. |
| Waktu dan Pengeluaran | 2461744 | Tampilan **persetujuan saya yang gagal** hanya berisi persetujuan proyek dalam tahapan **Diajukan**. |
| Waktu dan Pengeluaran | 2464082 | Hilangkan tautan dari persetujuan proyek ke persetujuan yang ditetapkan bila status target cocok. |
| Waktu dan Pengeluaran | 2468108 | Pekerjaan jadwal tidak boleh menetapkan status **Pemrosesan** untuk set persetujuan. |
| Waktu dan Pengeluaran | 2471503 | Hapus set persetujuan yang telah berusia tujuh hari. |
| Penagihan dan Harga | 2480687 | Referensi baris kuotasi tidak boleh dihilangkan saat tahapan baris kuotasi dibuat. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Jumlah vendor yang dipertahankan dalam transaksi pengeluaran proyek tidak ditampilkan dalam daftar transaksi. |
| Manajemen proyek dan akuntansi | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktur vendor antarperusahaan rusak saat integrasi faktur vendor diaktifkan. |
| Manajemen proyek dan akuntansi | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Persyaratan pembayaran pada faktur proyek tidak berfungsi sebagaimana yang diharapkan. |
| Manajemen proyek dan akuntansi | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Saat penyimpanan vendor dirilis, posting voucher memiliki baris tambahan yang salah. |
| Manajemen proyek dan akuntansi | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Ketika jurnal integrasi Project Operations diposting, gagal karena dimensi tidak ada untuk akun yang tidak diposting. |
| Manajemen proyek dan akuntansi | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Proyek** tidak dapat diedit pada faktur vendor tertunda jika kategori pengadaan ditetapkan ke item. |
| Manajemen proyek dan akuntansi | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panel navigasi tidak ada jika Anda tidak masuk ke Project Operations Dataverse. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Jika Anda memposting pendapatan dari faktur proyek dalam kasus panjar yang diterapkan, masalah terjadi karena transaksi di voucher tidak seimbang. |
| Manajemen proyek dan akuntansi | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Pembuatan perkiraan setelah Anda memposting baris koreksi memblokir proposal faktur dari impor. |
| Manajemen proyek dan akuntansi | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modifikasi rekaman tahapan yang ditagih penuh tidak boleh dilakukan. |
| Perjalanan dan Pengeluaran | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua laporan pengeluaran dapat dilihat saat Anda mencari kategori dalam aplikasi seluler Expense. |
| Perjalanan dan Pengeluaran | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Kesalahan Jumlah transaksi vendor dan transaksi pajak penjualan diposting dari pengeluaran yang dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Peringatan yang tidak relevan terjadi saat Anda me-refresh halaman **laporan Pengeluaran**. |
| Perjalanan dan Pengeluaran | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pemberi izin interim yang salah digunakan saat Anda menghapus pemberi izin interim, lalu mengirimkan ulang laporan pengeluaran melalui alur kerja. |
| Perjalanan dan Pengeluaran | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Terjadi kesalahan posting terkait konfigurasi jarak tempuh. |

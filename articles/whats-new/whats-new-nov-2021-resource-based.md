---
title: Yang baru di bulan November 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Operasi Proyek November 2021 untuk skenario berbasis sumber daya/non-stok.
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

- Operasi Proyek dalam Dataverse versi lingkungan 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Manajemen dan akuntansi proyek dalam lingkungan Dynamics 365 Finance versi 10.0.22

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- Antarmuka pemrograman aplikasi (API) Penjadwalan Proyek sekarang mendukung kemampuan untuk membuat dan menghapus bucket Proyek.

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel out-of-box, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti instruksi di [bagian Kolom tabel hilang di](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) peta bagian Panduan pemecahan masalah penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-in-dataverse"></a>Operasi Proyek di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2240080 | Kolom **Ketentuan** pembayaran tidak boleh diduplikasi pada faktur pro forma. |
| Penagihan dan Harga | 2358236 | Koreksi faktur harus memungkinkan koreksi yang memiliki garis harga nol. |
| Manajemen sumber daya | 2410072 | Izinkan penyiapan sumber daya yang ditetapkan ke tugas sebagai manajer proyek. |
| Penagihan dan Harga | 2430234 | Memperbaiki masalah perhitungan kinerja biaya. |
| Waktu dan Pengeluaran | 2436978 | Berikan waktu untuk dimasukkan dalam format hh:mm. |
| Penagihan dan Harga | 2448623 | Izinkan daftar harga diperbarui setelah dikaitkan dengan unit organisasi. |
| Waktu dan Pengeluaran | 2460396 | Perbolehkan entri waktu dihapus dengan mengosongkan sel. |
| Penagihan dan Harga | 2467386 | Perbolehkan proyek yang memiliki tugas untuk dihapus, bahkan ketika tugas dikaitkan dengan kutipan yang dimenangkan. |
| Waktu dan Pengeluaran | 2461744 | Tampilan **Persetujuan** saya yang gagal hanya berisi persetujuan proyek dalam **tahap Dikirim**. |
| Waktu dan Pengeluaran | 2464082 | Hapus tautan dari persetujuan proyek ke persetujuan yang ditetapkan saat status target cocok. |
| Waktu dan Pengeluaran | 2468108 | Pekerjaan Jadwal tidak boleh menetapkan **status Pemrosesan** untuk kumpulan persetujuan. |
| Waktu dan Pengeluaran | 2471503 | Hapus set persetujuan yang berumur tujuh hari. |
| Penagihan dan Harga | 2480687 | Referensi baris kutipan tidak boleh dihapus saat tonggak garis kutipan dibuat. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di bidang Keuangan

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Jumlah vendor yang ditahan dalam transaksi biaya proyek tidak ditampilkan dalam daftar transaksi. |
| Manajemen proyek dan akuntansi | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Faktur vendor antar perusahaan rusak saat integrasi faktur vendor diaktifkan. |
| Manajemen proyek dan akuntansi | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Ketentuan pembayaran pada faktur proyek tidak berfungsi seperti yang diharapkan. |
| Manajemen proyek dan akuntansi | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Ketika retensi vendor dirilis, posting voucher memiliki baris tambahan yang salah. |
| Manajemen proyek dan akuntansi | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Ketika jurnal integrasi Operasi Proyek diposting, jurnal tersebut gagal karena dimensi yang hilang untuk akun yang tidak diposting. |
| Manajemen proyek dan akuntansi | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Tab **Proyek** tidak dapat diedit pada faktur vendor yang tertunda saat kategori pengadaan ditetapkan ke item. |
| Manajemen proyek dan akuntansi | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Panel navigasi hilang jika Anda tidak masuk ke Operasi Dataverse Proyek. |
| Manajemen proyek dan akuntansi | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Saat Anda memposting pendapatan dari faktur proyek dalam kasus retainer yang diterapkan, masalah terjadi karena transaksi pada voucher tidak seimbang. |
| Manajemen proyek dan akuntansi | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Pembuatan perkiraan setelah Anda memposting proposal faktur memblokir garis koreksi dari impor. |
| Manajemen proyek dan akuntansi | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Modifikasi catatan tonggak pencapaian yang ditagih sepenuhnya seharusnya tidak dimungkinkan. |
| Perjalanan dan Pengeluaran | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Semua laporan pengeluaran akan terlihat saat Anda mencari kategori di aplikasi seluler Pengeluaran. |
| Perjalanan dan Pengeluaran | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Jumlah yang salah pada transaksi vendor dan transaksi pajak penjualan diposting dari pengeluaran yang dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Peringatan yang tidak relevan terjadi saat Anda me-refresh **halaman Laporan** pengeluaran. |
| Perjalanan dan Pengeluaran | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Pemberi persetujuan sementara yang salah digunakan saat Anda menghapus pemberi persetujuan sementara lalu mengirim ulang laporan pengeluaran melalui alur kerja. |
| Perjalanan dan Pengeluaran | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Terjadi kesalahan posting yang terkait dengan penyiapan jarak tempuh. |

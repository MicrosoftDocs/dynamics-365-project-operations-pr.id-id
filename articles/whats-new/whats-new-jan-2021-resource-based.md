---
title: Yang baru di bulan Januari 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Topik ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis Januari 2021 penyebaran Project Operations Lite untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 50874d771afe03b08bd95b670f7095bc2d61509d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599550"
---
# <a name="whats-new-january-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Januari 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

  - Lingkungan Project Operations untuk Dataverse versi 4.6.0.154
  - Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi 10.0.16

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| **Penyebaran dan Konfigurasi** | 2106818 | Memperbaiki nama sumber daya web yang menyebabkan masalah terkait penyesuaian halaman. |
| **Penagihan dan Harga** | 2091908 | Memperbaiki visibilitas **Kunci harga** dan **Gunakan pilihan Harga Saat** Ini di halaman **Faktur** saat Project Operations diinstal bersama dengan Dynamics 365 Field Service. |
| **Penagihan dan Harga** | 2103058 | Menyegarkan **Total Proyek** untuk menangani nilai nihil untuk biaya aktual pada tugas. |
| **Penagihan dan Harga** | 2116100 | Memperbaiki Pesan kesalahan yang digunakan dengan fungsi, **Perbaiki Entri pada Aktual**. |
| **Penagihan dan Harga** | 2116129 | memperbaiki Visibilitas estimasi pengeluaran pada tab **Estimasi** di halaman **Proyek**. |
| **Penagihan dan Harga** | 2119112 | Memperbaiki agregasi tetap untuk penjualan aktual dan biaya aktual bila nilai tukar yang berbeda digunakan. |
| **Penagihan dan Harga** | 2134705 | Memperbaiki kesalahan, "Tidak dapat membaca properti **getResourceString** dari tak tertentu jika halaman **Faktur** dibuka dan Field Service diinstal. |
| **Manajemen peluang** | 2022195 | Kisi penagihan berbasis tugas di halaman **Proyek** mencakup ikon yang menunjukkan bahwa ada kontrak atau baris kuotasi yang ditautkan ke tugas tersebut. |
| **Manajemen peluang** | 2029135 | Memperbaiki kesalahan proses bisnis yang terjadi saat pengguna mencoba membuka baris faktur di faktur terkonfirmasi yang menagih jumlah uang muka. |
| **Manajemen peluang** | 2040713 | Memperbaiki kesalahan skrip yang terjadi saat membuat faktur dari kontrak dan Field Service diinstal. |
| **Perencanaan dan Pelacakan Proyek** | 2090202 | Menandai aturan bisnis yang tidak lagi digunakan sebagai **tidak digunakan lagi**. |
| **Waktu dan Pengeluaran** | 2091249 | Memperketat kontrol sehingga pengguna tidak dapat mengubah tugas pada entri waktu yang telah diajukan atau disetujui. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| **Manajemen proyek dan akuntansi** | [478667](https://fix.lcs.dynamics.com/Issue/Details/?bugId=478667) | Jumlah kontrak yang salah pada halaman **Kredit** untuk proyek harga tetap dengan beberapa sumber dana. |
| **Manajemen proyek dan akuntansi** | [480260](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480260) | Placeholder **Invoiceproposal.PSAnfRefProjId** tidak menampilkan ID Proyek untuk alur kerja, **Tinjau proposal faktur proyek**. |
| **Manajemen proyek dan akuntansi** | [481227](https://fix.lcs.dynamics.com/Issue/Details/?bugId=481227) | Tanggal diskon tunai yang salah digunakan saat posting proposal faktur proyek. |
| **Manajemen proyek dan akuntansi** | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558) | Menghapus dan membaca penetapan sumber daya di Project Operations menggandakan entri prakiraan proyek di Finance. |
| **Manajemen proyek dan akuntansi** | [484468](https://fix.lcs.dynamics.com/Issue/Details/?bugId=484468) | Di Project Operations, Anda tidak dapat membuat estimasi proyek di Dataverse tanpa memiliki baris kontrak pada proyek. |
| **Manajemen proyek dan akuntansi** | [485871](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485871) | Dimensi keuangan pada transaksi pengeluaran proyek tidak disinkronisasikan dengan voucher terkait dan distribusi akuntansi laporan pengeluaran ketika biaya diposting ke Saldo. |
| **Manajemen proyek dan akuntansi** | [488382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488382) | Filter **status faktur** di transaksi proyek yang diposting untuk proyek harga tetap tidak berfungsi. |
| **Manajemen proyek dan akuntansi** | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Penghapusan perkiraan mundur tidak berfungsi pada bagian **Berkala**. |
| **Manajemen proyek dan akuntansi** | [509989](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509989) | Baris proposal faktur dapat dihapus dalam Project Operations ketika terintegrasi dengan Dataverse. |
| **Manajemen proyek dan akuntansi** | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041) | Mencegah pengaktifan fitur baris kontrak ganda tanpa integrasi Dataverse. |
| **Manajemen proyek dan akuntansi** | [510527](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510527) | Bila faktur akun sama dengan laba dan rugi, pendapatan ter ditagih didaftarkan sebagai nol pada halaman Estimasi. |
| **Manajemen proyek dan akuntansi** | [514167](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514167) | Koreksi faktur tidak berfungsi di lingkungan yang terintegrasi. |
| **Manajemen proyek dan akuntansi** | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Saat memposting WIP - nilai penjualan yang diposting dalam pembuatan faktur proyek antarperusahaan, akun salah dipilih. |
| **Manajemen proyek dan akuntansi** | [514385](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514385) | Dalam Project Operations, dependensi pada tugas perkiraan di Dataverse tidak dapat diperbarui. |
| **Manajemen proyek dan akuntansi** | [515258](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515258) | Berulang kali menghapus jurnal integrasi Project Operations di Finance akan mengakibatkan hilangnya data. |
| **Manajemen proyek dan akuntansi** | [519716](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519716) | Kesalahan berikut ini terjadi ketika memposting proposal faktur proyek, "Transaksi tidak seimbang pada mata uang pelaporan saat faktur uang muka yang dikurangi ditambahkan". |
| **Manajemen proyek dan akuntansi** | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | ID proyek yang salah disertakan pada pengurangan setelah kontrak proyek default diperbarui di Project Operations. |
| **Manajemen proyek dan akuntansi** | [522799](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522799) | Perkiraan dan pengakuan pendapatan tidak dapat diselesaikan saat Project Operations diaktifkan. |
| **Manajemen proyek dan akuntansi** | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Di Project Operations, menghapus proyek dari kontrak tidak mengatur ulang proyek default pada kontrak. |
| **Manajemen proyek dan akuntansi** | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Di Project Operations, pada faktur antarperusahaan, baris pengeluaran yang salah muncul di daftar **Tambah baris**. |
| **Perjalanan dan Pengeluaran** | [515334](https://fix.lcs.dynamics.com/Issue/Details/?bugId=515334) | Baris pengeluaran tidak dapat diposting karena konfigurasi jam tidak ada di baris kontrak. |
| **Perjalanan dan Pengeluaran** | [437673](https://fix.lcs.dynamics.com/Issue/Details/?bugId=437673) | Bila validasi proyek/kategori adalah wajib, kategori pengeluaran yang terkait dengan proyek tidak terlihat dalam laporan pengeluaran. |
| **Perjalanan dan Pengeluaran** | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Keseimbangan uang muka tunai tidak diperbarui saat laporan pengeluaran diposting berdasarkan baris. |
| **Perjalanan dan Pengeluaran** | [465396](https://fix.lcs.dynamics.com/Issue/Details/?bugId=465396) | Pekerjaan **Perbarui informasi pembayaran** gagal setelah membalikkan penyelesaian di mana faktur diselesaikan dengan dua atau lebih transaksi pembayaran. |
| **Perjalanan dan Pengeluaran** | [472892](https://fix.lcs.dynamics.com/Issue/Details/?bugId=472892) | Ada masalah dengan perhitungan pengurangan biaya makan di hari terakhir untuk kategori pengeluaran uang saku. |
| **Perjalanan dan Pengeluaran** | [477714](https://fix.lcs.dynamics.com/Issue/Details/?bugId=477714) | Laporan **Jenis pengeluaran per karyawan** tidak menampilkan pengeluaran item jika sambungan pertama pengguna berada dalam bahasa es-MX. |
| **Perjalanan dan Pengeluaran** | [487516](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487516) | Pembayaran vendor untuk faktur laporan pengeluaran menggunakan akun ringkasan yang salah untuk posting penyelesaian. |
| **Perjalanan dan Pengeluaran** | [487531](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487531) | Ketika sebuah laporan pengeluaran diposting dengan **Izinkan pengelompokan transaksi berdasarkan akun pembayaran pengimbang** dan **Mengoreksi Tanggal Akuntansi saat diposting** diaktifkan, tanggal akuntansi tidak dikelompokkan pada tabel **Distribusi akuntansi**, dan memengaruhi rekaman pajak penjualan. |
| **Perjalanan dan Pengeluaran** | [488292](https://fix.lcs.dynamics.com/Issue/Details/?bugId=488292) | Pemetaan subkategori pengeluaran dihilangkan saat kotak centang Gunakan dalam pengeluaran dicentang dan kemudian dipilih lagi. |
| **Perjalanan dan Pengeluaran** | [506175](https://fix.lcs.dynamics.com/Issue/Details/?bugId=506175) | Laporan pengeluaran antarperusahaan tidak dapat dibuat jika ID proyek ditambahkan pada tingkat header. |
| **Perjalanan dan Pengeluaran** | [509491](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509491) | Ada masalah dengan pembayaran pengeluaran apabila jumlah pengeluaran lebih besar dibandingkan jumlah uang muka. |
| **Perjalanan dan Pengeluaran** | [509556](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509556) | Bidang **ID Proyek** pada laporan pengeluaran antarperusahaan akan kosong jika peran pengguna ditetapkan ke organisasi tertentu. |
| **Perjalanan dan Pengeluaran** | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategori pengeluaran terkunci saat menambahkan baris pengeluaran baru. |
| **Perjalanan dan Pengeluaran** | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Perincian baris laporan pengeluaran yang telah dipecah mengakibatkan tidak lengkapnya voucher utang\buku besar Umum yang diposting. Karena duplikasi **TRVEXPTRANS. SOURCEDOCUMENTLINE**, Penjelajah Sumber Akuntansi juga rusak. |
| **Perjalanan dan Pengeluaran** | [521768](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521768) | Indeks yang ditambahkan pada tabel **TRVREQUISITIONLINE** dengan duplikat pelanggan mengakibatkan kesalahan saat peningkatan. |
| **Perjalanan dan Pengeluaran** | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Di Project Operations, waktu dengan tugas antarperusahaan di Dataverse di tidak dapat dibuat atau disetujui. |

## <a name="regulatory-updates"></a>Pembaruan wajib

Untuk informasi tentang pembaruan peraturan untuk aplikasi Keuangan dan Operasi, lihat [Pembaruan peraturan](/dynamics365/finance/localizations/regulatory-updates). Anda juga dapat masuk ke LCS dan melihat pembaruan regulasi yang direncanakan dengan menggunakan alat pencarian Masalah. Pencarian Masalah memungkinkan Anda mencari berdasarkan negara, jenis fitur, dan rilis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
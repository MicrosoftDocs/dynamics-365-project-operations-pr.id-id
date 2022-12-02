---
title: Yang baru di bulan Juli 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di perilisan Microsoft Dynamics 365 Project Operations pada Juli 2022 untuk skenario berbasis sumber daya/non-stok.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403955"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Juli 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.44.0.22
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penyebaran dan Konfigurasi | 2761472 | Kesalahan penginstalan Project Operations ditangani. |
| Penagihan dan Harga | 2746940 | Nama baris subkontrak harus memiliki panjang maksimum 100 karakter. |
| Penagihan dan Harga | 2739162 | Pelanggan harus dapat melihat tombol pita di tampilan kisi aktual. |
| Perencanaan dan Pelacakan Proyek | 2730318 | Validasi yang diperbarui untuk karakter yang tidak didukung dalam subjek proyek. |
| Penagihan dan Harga | 2705361 | Aktual penjualan tertagih tahapan harus disertakan dalam bidang pelacakan proyek. |
| Penagihan dan Harga | 2675880 | Cegah proyek ditautkan ke baris kontrak yang tidak berbasis kerja. |
| Penagihan dan Harga | 2664396 | Jika daftar harga kuotasi disimpan tanpa kuotasi, pasti ada kesalahan yang menyatakan bahwa kuotasi tidak dapat kosong. |
| Penagihan dan Harga | 2184019 | Tab **Penagihan Berdasarkan Tugas** tidak boleh ditampilkan untuk proyek yang tidak memiliki kontrak dukungan atau kuotasi. |
| Waktu dan Pengeluaran | 2754459 | Bila alur cloud penjadwalan ulang tidak aktif, tampilkan banner dan lewati pemrosesan asinkron. |
| Penagihan dan Harga | 2724391 | Pengecualian yang salah terjadi saat aturan penagihan terpisah kontrak proyek tidak memiliki nilai pelanggan. |
| Penagihan dan Harga | 2708638 | Rekaman tidak ditemukan saat mencari menggunakan pencarian kisi dalam Penggunaan bahan dan perjanjian untuk Penggunaan bahan.|
| Penagihan dan Harga | 2686977 | Cegah validasi baris faktur selama pembuatan faktur. |
| Penagihan dan Harga | 2683032 | Penyalinan peran dan kategori yang dibebankan tidak menskalakan lebih dari 5000 rekaman.|
| Penagihan dan Harga | 2673363 | % Biaya Pemakaian pada Proyek rusak ketika estimasi Upaya dan Pengeluaran dan aktual ada untuk proyek. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Fitur diaktifkan secara default di rilis mendatang

Tabel berikut berisi daftar fitur yang diaktifkan secara default di versi 10.0.29. Sebagian besar fitur yang telah secara otomatis diaktifkan dapat dinonaktifkan dalam [manajemen Fitur](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Di masa mendatang, sejumlah fitur yang telah secara otomatis diaktifkan dapat dihilangkan dari manajemen Fitur dan menjadi wajib. Perubahan ini akan memastikan bahwa pelanggan menggunakan fungsi saat ini, sehingga peningkatan dapat dibuat pada fungsi saat ini saat ditambahkan. Fitur tidak akan diaktifkan secara otomatis dalam waktu kurang dari satu tahun, kecuali jika ditentukan untuk menjadi penting.

| Nama fitur | Tanggal aktifkan | Fitur ditambahkan | Status fitur | Modul |
| --- | --- | --- |--- |--- |
| Aktifkan penyesuaian transaksi per jam berdasarkan perubahan alokasi aturan dana | 16 September 2022 | 7 Oktober 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Fitur pembalikan faktur pembayaran di muka pesanan pembelian proyek | 16 September 2022 | 6 Oktober 2021 | Aktif secara default | Manajemen proyek dan akuntansi |
| Menghapus baris proposa faktur ketika menggunakan Project Operations untuk skenario berbasis sumber daya/non-stok | 16 September 2022 | 6 Oktober 2021 | Aktif secara default | Manajemen proyek dan akuntansi |
| Menyesuaikan akuntansi pada transaksi proyek yang diposting | 16 September 2022 | 10 Mei 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Aktifkan konfigurasi akuntansi default untuk proyek | 16 September 2022 | 19 Februari 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Aktifkan beberapa baris kontrak untuk proyek | 16 September 2022 | 29 Juni 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Buat jurnal Jam Proyek hanya dapat dibaca jika status persetujuan saat ini tidak memungkinkan pengeditan | 16 September 2022 | 6 Oktober 2021 | Aktif secara default | Manajemen proyek dan akuntansi |
| Aktifkan sinkronisasi baris penjualan dari baris pembelian saat baris pembelian diperbarui dan parameter manajemen perubahan pesanan pembelian diaktifkan | 16 September 2022 | 7 Oktober 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Aktifkan Project Operations di Dynamics 365 Customer Engagement | 16 September 2022 | 29 Juni 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Fitur koreksi pembalikan transaksi proyek | 16 September 2022 | 13 Juli 2020 | Aktif secara default | Manajemen proyek dan akuntansi |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Fitur yang menjadi wajib di rilis mendatang

Tabel berikut berisi daftar fitur yang wajib dari versi 10.0.29 ke atas.

| Nama fitur | Tanggal aktifkan | Fitur ditambahkan | Status fitur | Modul |
| --- | --- | --- | --- | --- |
| Menghitung nilai komitmen pada sumber dana tanpa membulatkan nilai tukar | 16 September 2022 | 14 Juni 2020 | Wajib | Manajemen proyek dan akuntansi |
| Aktifkan posting penyesuaian proyek dengan akun buku besar yang sama seperti transaksi asli | 16 September 2022 | 14 Juni 2020 | Wajib | Manajemen proyek dan akuntansi |
| Detail jumlah komitmen kontrak proyek | 16 September 2022 | 31 Agustus 2019 | Wajib | Manajemen proyek dan akuntansi |
| Aktifkan pengurutan berdasarkan sumber daya selama pembuatan proposal faktur proyek | 16 September 2022 | 31 Agustus 2019 | Wajib | Manajemen proyek dan akuntansi |

---
title: Yang baru di bulan Juli 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Juli 2022 Microsoft Dynamics 365 Project Operations untuk skenario berbasis sumber daya/non-stok.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183906"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Juli 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam Dataverse versi lingkungan 4.44.0.22
- Manajemen dan akuntansi proyek dalam lingkungan Dynamics 365 Finance versi 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel out-of-box, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti instruksi di [bagian Kolom tabel hilang di](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) peta bagian Panduan pemecahan masalah penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penyebaran dan Konfigurasi | 2761472 | Kesalahan penginstalan Operasi Proyek ditangani. |
| Penagihan dan Harga | 2746940 | Nama baris subkontrak harus memiliki panjang maksimum 100 karakter. |
| Penagihan dan Harga | 2739162 | Pelanggan harus dapat melihat tombol pita dalam tampilan kisi aktual. |
| Perencanaan dan Pelacakan Proyek | 2730318 | Validasi yang diperbarui untuk karakter yang tidak didukung dalam subjek proyek. |
| Penagihan dan Harga | 2705361 | Tonggak pencapaian aktual penjualan yang ditagih harus disertakan dalam bidang pelacakan proyek. |
| Penagihan dan Harga | 2675880 | Mencegah proyek ditautkan ke jalur kontrak yang tidak berbasis kerja. |
| Penagihan dan Harga | 2664396 | Jika daftar harga kutipan disimpan tanpa kutipan, pasti ada kesalahan yang menyatakan bahwa kutipan tidak boleh kosong. |
| Penagihan dan Harga | 2184019 | Tab **Penagihan** Berbasis Tugas tidak boleh ditampilkan untuk proyek yang tidak memiliki kontrak atau penawaran dukungan. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di bidang Keuangan

Untuk informasi tentang perbaikan bug yang disertakan dalam pembaruan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Fitur diaktifkan secara default dalam rilis mendatang

Tabel berikut mencantumkan fitur yang diaktifkan secara default di versi 10.0.29. Sebagian besar fitur yang telah diaktifkan secara otomatis dapat dinonaktifkan di [Manajemen fitur](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Di masa mendatang, beberapa fitur yang telah diaktifkan secara otomatis mungkin akan dihapus dari Pengelolaan fitur dan menjadi wajib. Perubahan ini memastikan bahwa pelanggan menggunakan fungsionalitas saat ini, sehingga peningkatan dapat dibangun di atas fungsionalitas saat ini saat ditambahkan. Fitur tidak akan pernah diaktifkan secara otomatis dalam waktu kurang dari satu tahun, kecuali jika ditentukan penting.

| Nama fitur | Aktifkan tanggal | Fitur ditambahkan | Status fitur | Modul |
| --- | --- | --- |--- |--- |
| Memungkinkan penyesuaian transaksi jam berdasarkan perubahan alokasi aturan pendanaan | 16 September 2022 | 7 Oktober 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Fitur pembalikan faktur pembayaran di muka pesanan pembelian proyek | 16 September 2022 | 6 Oktober 2021 | Aktif secara default | Manajemen proyek dan akuntansi |
| Menghapus baris proposal faktur saat menggunakan Operasi Proyek untuk skenario berbasis sumber daya/tidak tersedia | 16 September 2022 | 6 Oktober 2021 | Aktif secara default | Manajemen proyek dan akuntansi |
| Menyesuaikan akuntansi pada transaksi proyek yang diposting | 16 September 2022 | 10 Mei 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Aktifkan penyiapan akuntansi default untuk proyek | 16 September 2022 | 19 Februari 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Aktifkan beberapa baris kontrak untuk proyek | 16 September 2022 | 29 Juni 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Membuat jurnal Project Hour baca-saja jika status persetujuan saat ini tidak mengizinkan pengeditan | 16 September 2022 | 6 Oktober 2021 | Aktif secara default | Manajemen proyek dan akuntansi |
| Aktifkan sinkronkan jalur penjualan dari jalur pembelian saat baris pembelian diperbarui dan parameter manajemen perubahan pesanan pembelian diaktifkan | 16 September 2022 | 7 Oktober 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Mengaktifkan Operasi Proyek di Dynamics 365 Customer Engagement | 16 September 2022 | 29 Juni 2020 | Aktif secara default | Manajemen proyek dan akuntansi |
| Fitur koreksi pembalikan transaksi proyek | 16 September 2022 | 13 Juli 2020 | Aktif secara default | Manajemen proyek dan akuntansi |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Fitur yang menjadi wajib dalam rilis mendatang

Tabel berikut mencantumkan fitur-fitur yang wajib dari versi 10.0.29 dan seterusnya.

| Nama fitur | Aktifkan tanggal | Fitur ditambahkan | Status fitur | Modul |
| --- | --- | --- | --- | --- |
| Hitung nilai komitmen pada sumber pendanaan tanpa membulatkan nilai tukar | 16 September 2022 | 14 Juni 2020 | Wajib | Manajemen proyek dan akuntansi |
| Aktifkan posting penyesuaian proyek dengan akun buku besar yang sama dengan transaksi asli | 16 September 2022 | 14 Juni 2020 | Wajib | Manajemen proyek dan akuntansi |
| Detail jumlah komitmen kontrak proyek | 16 September 2022 | 31 Agustus 2019 | Wajib | Manajemen proyek dan akuntansi |
| Mengaktifkan pengurutan menurut sumber daya selama pembuatan proposal faktur proyek | 16 September 2022 | 31 Agustus 2019 | Wajib | Manajemen proyek dan akuntansi |

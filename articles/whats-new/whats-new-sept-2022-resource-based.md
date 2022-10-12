---
title: Yang baru di bulan September 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis September 2022 Microsoft Dynamics 365 Project Operations untuk skenario berbasis sumber daya/non-stok.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621344"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan September 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam Dataverse versi lingkungan 4.46.0.60
- Manajemen dan akuntansi proyek dalam lingkungan Dynamics 365 Finance versi 10.0.29

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

| Area fitur | Nama fitur | Informasi selengkapnya |
| --- | --- | --- |
| Manajemen peluang | **Revisi dan Aktivasi Kuotasi**<br>Operasi Proyek membawa dukungan penuh dari proses penjualan. Kutipan proyek dapat diaktifkan untuk mewakili keadaan di mana kutipan hanya-baca dan sedang ditinjau. Kutipan yang diaktifkan dapat direvisi untuk membuat kutipan baru yang memiliki nomor revisi yang bertambah. Kutipan proyek yang diaktifkan atau revisi kutipan dapat ditutup sebagai menang atau kalah. | [Mengaktifkan dan merevisi kuotasi proyek](/dynamics365/project-operations/sales/activation-and-revision) |
| Penagihan dan Harga | **Default harga agnostik zona waktu**<br>Operasi Proyek telah memperkenalkan konsep tanggal agnostik zona waktu pada semua aktual proyek. Bidang baru, **Tanggal** transaksi, sekarang tersedia di baris jurnal dan aktual, dan akan digunakan untuk menyimpan tanggal ketika transaksi terjadi, tetapi tanpa mengonversi tanggal tersebut menjadi Waktu Universal Terkoordinasi. Tanggal ini akan digunakan untuk proses hilir seperti default harga dan pembuatan faktur. | <p>[Menentukan tarif biaya untuk perkiraan dan aktual berbasis proyek](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Menentukan harga penjualan untuk perkiraan dan aktual berbasis proyek](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Penagihan dan Harga | **Penggantian harga efektif tanggal dalam Operasi Proyek**<br>Penggantian harga efektif tanggal memberikan cara untuk mengganti atau mengubah harga tertentu dalam daftar harga. | [Penggantian harga efektif tanggal](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subkontrak | **Subkontrak dan rekonsiliasi faktur vendor**<br>Fitur ini memungkinkan pelanggan untuk membuat subkontrak untuk membeli waktu sumber daya, kategori pengeluaran, dan bahan yang digunakan untuk pekerjaan proyek. Ini juga memungkinkan pelanggan untuk mencatat, dalam aplikasi keuangan dan operasi, faktur vendor yang akan tersedia untuk manajer proyek untuk Dataverse verifikasi. | <p>[Manajemen subkontrak](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Buat faktur vendor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Waktu dan Pengeluaran | **Pemberi Persetujuan Global**<br>Fitur ini memungkinkan vendor perangkat lunak independen (ISV) dan persetujuan terpusat, terlepas dari status proyek atau anggota tim dalam proyek. | [Keamanan dan persetujuan](/dynamics365/project-operations/approvals/approvals-security) |
| Manajemen pengeluaran | **Kemampuan untuk memposting kewajiban biaya dalam mata uang vendor**<br>Fitur ini memungkinkan laporan pengeluaran untuk diposting dalam mata uang vendor untuk metode pembayaran tunai. | [Kemampuan untuk memposting kewajiban biaya dalam mata uang vendor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Pengadaan Proyek | **Membayar saat pembayaran vendor berbayar**<br>Fitur ini memungkinkan fitur Bayar saat dibayar (PWP) untuk digunakan dengan lingkungan non-stok Operasi Proyek. Ini memungkinkan pembayaran vendor untuk diblokir/disimpan, berdasarkan persyaratan retensi, hingga pembayaran diterima dari pelanggan. | [Membayar saat pembayaran vendor berbayar](/dynamics365/project-operations/procurement/pay-when-paid) |
| Pengadaan Proyek | **Permintaan pembelian proyek**<br>Fitur ini memungkinkan pengguna untuk membuat pesanan pembelian terkait proyek di badan hukum di mana Operasi Proyek pada integrasi Dynamics 365 Customer Engagement diaktifkan. Pesanan pembelian proyek dapat digunakan untuk mencatat pengadaan material yang tidak ditebar terhadap proyek oleh persona departemen Pengadaan. Pesanan pembelian proyek tidak akan disinkronkan ke Dataverse. Namun, Anda dapat menggunakan entitas virtual untuk memunculkan baris pesanan pembelian Proyek untuk Dataverse informasi manajer proyek. Biaya faktur vendor terkait proyek terintegrasi dengan entitas Project Actuals di Dataverse. Biaya proyek dicatat dalam subledger Proyek dengan menggunakan jurnal Integrasi Operasi Proyek. | |

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tabel berikut menunjukkan peta tulis ganda yang telah dimodifikasi atau ditambahkan dalam rilis Operasi Proyek September 2022.

| Peta entitas | Pembaruan versi | Komentar |
| -------------- | ------------------- | ------------|
| Aktual Integrasi Project Operations (msdyn_actuals) | 1.0.0.15 | Peta ini mendukung pemrosesan aktual subkontrak dengan Operasi Proyek untuk skenario berbasis sumber daya. |
| Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Peta ini mendukung pemrosesan aktual subkontrak dengan Operasi Proyek untuk skenario berbasis sumber daya. |
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Peta ini mendukung pemrosesan aktual subkontrak dengan Operasi Proyek untuk skenario berbasis sumber daya. |

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel out-of-box, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti instruksi di [bagian Kolom tabel hilang di](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) peta bagian Panduan pemecahan masalah penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2754422 | Perkiraan Material dan Biaya tidak mengalir ke Keuangan ketika proyek disalin di Dataverse. |
| Waktu dan Pengeluaran | 2787409 | Pemberi persetujuan yang tidak valid dapat menyetujui entri waktu non-proyek. |
| Manajemen peluang | 2788907 | Pesan kesalahan yang diperbarui pada validasi keunikan untuk baris pesanan yang menyertakan bendera. |
| Waktu dan Pengeluaran | 2842253 | Penanganan pengecualian nol untuk persetujuan waktu. |
| Penagihan dan Harga | 2844181 | Kegagalan untuk mendapatkan ID korelasi memblokir pembuatan faktur. |
| Penagihan dan Harga | 2876628 | QLD, CLD - Perkiraan resolusi daftar harga harus menggunakan bidang rentang tanggal lama dari daftar harga. |
| Subkontrak | 2893222 | Jika tidak ada peran yang ditentukan untuk baris subkontrak, seharusnya dimungkinkan untuk memilih baris tersebut pada anggota tim untuk peran apa pun. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di bidang Keuangan

Untuk informasi tentang perbaikan bug yang disertakan dalam pembaruan ini, masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Fitur diaktifkan secara default dalam rilis mendatang

Tabel berikut mencantumkan fitur yang diaktifkan secara default di versi 10.0.30. Sebagian besar fitur yang telah diaktifkan secara otomatis dapat dinonaktifkan di [Manajemen](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview) fitur. Di masa mendatang, beberapa fitur yang telah diaktifkan secara otomatis mungkin akan dihapus dari Pengelolaan fitur dan menjadi wajib. Perubahan ini memastikan bahwa pelanggan menggunakan fungsionalitas saat ini, sehingga peningkatan dapat dibangun di atas fungsionalitas saat ini saat ditambahkan. Fitur tidak akan pernah diaktifkan secara otomatis dalam waktu kurang dari satu tahun, kecuali jika ditentukan penting.

| Nama fitur | Aktifkan tanggal | Fitur ditambahkan | Status fitur | Modul |
| --- | --- | --- |--- |--- |
| Mengaktifkan operasi asinkron saat pengguna perlu beralih antara operasi sinkronisasi dan asinkron | 21 Oktober 2022 | 9 April 2021 | Aktif secara default | Manajemen pengeluaran |
| Evaluasi kebijakan pengeluaran untuk penerimaan yang diperlukan | 21 Oktober 2022 | 20 Desember 2021 | Aktif secara default | Manajemen pengeluaran |
| Tampilan daftar laporan pengeluaran yang dibuat dengan mendelegasikan pekerja | 21 Oktober 2022 | 19 Februari 2020 | Aktif secara default | Manajemen pengeluaran |
| Perhitungan total jarak tempuh berdasarkan tahun fiskal | 21 Oktober 2022 | 10 Mei 2022 | Aktif secara default | Manajemen pengeluaran |

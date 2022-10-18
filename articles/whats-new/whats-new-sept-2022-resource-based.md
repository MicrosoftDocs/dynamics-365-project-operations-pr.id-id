---
title: Yang baru di bulan September 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis September 2022 Microsoft Dynamics 365 Project Operations untuk skenario berbasis sumber daya/tidak tersedia.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634809"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan September 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam versi lingkungan 4.46.0.60 Dataverse
- Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi 10.0.29

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

| Area fitur | Nama fitur | Informasi selengkapnya |
| --- | --- | --- |
| Manajemen peluang | **Revisi dan Aktivasi Quotes**<br>Operasi Proyek membawa dukungan penuh dari proses penjualan. Kutipan proyek dapat diaktifkan untuk mewakili keadaan di mana kutipan bersifat baca-saja dan sedang ditinjau. Kutipan yang diaktifkan dapat direvisi untuk membuat kutipan baru yang memiliki nomor revisi tambahan. Kutipan proyek yang diaktifkan atau revisi kutipan dapat ditutup sebagai menang atau kalah. | [Mengaktifkan dan merevisi kuotasi proyek](/dynamics365/project-operations/sales/activation-and-revision) |
| Penagihan dan Harga | **Harga agnostik zona waktu default**<br>Operasi Proyek telah memperkenalkan konsep tanggal agnostik zona waktu pada semua aktual proyek. Bidang baru, Tanggal **transaksi, sekarang tersedia di baris jurnal dan aktual, dan akan digunakan untuk menyimpan tanggal ketika transaksi terjadi,** tetapi tanpa mengubah tanggal tersebut menjadi Waktu Universal Terkoordinasi. Tanggal ini akan digunakan untuk proses hilirisasi seperti default harga dan pembuatan faktur. | <p>[Tentukan tarif biaya untuk estimasi dan aktual berbasis proyek](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Tentukan harga penjualan untuk perkiraan dan aktual berbasis proyek](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Penagihan dan Harga | **Penggantian harga efektif tanggal dalam Operasi Proyek**<br>Penggantian harga efektif tanggal menyediakan cara untuk mengganti atau mengubah harga tertentu dalam daftar harga. | [Penggantian harga efektif tanggal](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subkontrak | **Subkontrak dan rekonsiliasi faktur vendor**<br>Fitur ini memungkinkan pelanggan membuat subkontrak untuk membeli waktu sumber daya, kategori pengeluaran, dan bahan yang digunakan untuk pekerjaan proyek. Ini juga memungkinkan pelanggan untuk merekam, dalam aplikasi keuangan dan operasi, faktur vendor yang akan tersedia untuk manajer proyek untuk Dataverse verifikasi. | <p>[Manajemen subkontrak](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Buat faktur vendor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Waktu dan Pengeluaran | **Pemberi Persetujuan Global**<br>Fitur ini memungkinkan vendor perangkat lunak independen (ISV) dan persetujuan terpusat, terlepas dari status proyek atau anggota tim dalam proyek. | [Keamanan dan persetujuan](/dynamics365/project-operations/approvals/approvals-security) |
| Manajemen pengeluaran | **Kemampuan untuk memposting kewajiban biaya dalam mata uang vendor**<br>Fitur ini memungkinkan laporan pengeluaran diposting dalam mata uang vendor untuk metode pembayaran tunai. | [Kemampuan untuk memposting kewajiban biaya dalam mata uang vendor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Pengadaan Proyek | **Bayar saat pembayaran vendor berbayar**<br>Fitur ini memungkinkan fitur Pay when paid (PWP) untuk digunakan dengan lingkungan non-stok Operasi Proyek. Ini memungkinkan pembayaran vendor untuk diblokir/dipertahankan, berdasarkan persyaratan retensi, hingga pembayaran diterima dari pelanggan. | [Bayar saat pembayaran vendor berbayar](/dynamics365/project-operations/procurement/pay-when-paid) |
| Pengadaan Proyek | **Permintaan pembelian proyek**<br>Fitur ini memungkinkan pengguna untuk membuat pesanan pembelian terkait proyek di badan hukum tempat Operasi Proyek pada integrasi Dynamics 365 Customer Engagement diaktifkan. Pesanan pembelian proyek dapat digunakan untuk mencatat pengadaan material yang tidak ditebar terhadap proyek oleh persona departemen Pengadaan. Pesanan pembelian proyek tidak akan disinkronkan ke Dataverse. Namun, Anda dapat menggunakan entitas virtual untuk memunculkan baris pesanan pembelian Project untuk Dataverse informasi manajer proyek. Biaya faktur vendor terkait proyek terintegrasi dengan entitas Project Actuals di Dataverse. Biaya proyek dicatat dalam subledger Proyek dengan menggunakan jurnal Integrasi Operasi Proyek. | |
|Perencanaan dan Pelacakan Proyek|**Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan** </br> </br>API pengeditan kontur penugasan sumber daya memungkinkan pengembang secara terprogram menentukan upaya penerima tugas di seluruh rentang tanggal yang didukung untuk perencanaan upaya bertahap waktu yang lebih terperinci.|[Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tabel berikut menunjukkan peta tulis ganda yang telah dimodifikasi atau ditambahkan dalam rilis Operasi Proyek September 2022.

| Peta entitas | Pembaruan versi | Komentar |
| -------------- | ------------------- | ------------|
| Aktual Integrasi Project Operations (msdyn_actuals) | 1.0.0.15 | Peta ini mendukung pemrosesan aktual subkontrak dengan Operasi Proyek untuk skenario berbasis sumber daya. |
| Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Peta ini mendukung pemrosesan aktual subkontrak dengan Operasi Proyek untuk skenario berbasis sumber daya. |
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Peta ini mendukung pemrosesan aktual subkontrak dengan Operasi Proyek untuk skenario berbasis sumber daya. |

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Proyek Dataverse dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel siap pakai, terapkan kembali perubahannya. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti petunjuk di bagian Masalah kolom tabel hilang di [peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari Panduan pemecahan masalah penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2754422 | Perkiraan Material dan Pengeluaran tidak mengalir ke Keuangan ketika proyek disalin dalam Dataverse format. |
| Waktu dan Pengeluaran | 2787409 | Pemberi persetujuan yang tidak valid dapat menyetujui entri waktu non-proyek. |
| Manajemen peluang | 2788907 | Pesan kesalahan yang diperbarui pada validasi keunikan untuk baris pesanan yang menyertakan bendera. |
| Waktu dan Pengeluaran | 2842253 | Penanganan pengecualian nol untuk persetujuan waktu. |
| Penagihan dan Harga | 2844181 | Kegagalan untuk mendapatkan ID korelasi memblokir pembuatan faktur. |
| Penagihan dan Harga | 2876628 | QLD, CLD - Resolusi daftar harga perkiraan harus menggunakan bidang rentang tanggal lama dari daftar harga. |
| Subkontrak | 2893222 | Jika tidak ada peran yang ditentukan untuk baris subkontrak, seharusnya dimungkinkan untuk memilih baris tersebut pada anggota tim untuk peran apa pun. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di bidang Keuangan

Untuk informasi tentang perbaikan bug yang disertakan dalam pembaruan ini, masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559) KB.

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Fitur diaktifkan secara default di rilis mendatang

Tabel berikut mencantumkan fitur yang diaktifkan secara default di versi 10.0.30. Sebagian besar fitur yang telah diaktifkan secara otomatis dapat dinonaktifkan di [Manajemen fitur](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Di masa mendatang, beberapa fitur yang telah diaktifkan secara otomatis mungkin akan dihapus dari Manajemen fitur dan menjadi wajib. Perubahan ini memastikan bahwa pelanggan menggunakan fungsionalitas saat ini, sehingga peningkatan dapat dibangun di atas fungsionalitas saat ini saat ditambahkan. Fitur tidak akan pernah diaktifkan secara otomatis dalam waktu kurang dari satu tahun, kecuali jika ditentukan penting.

| Nama fitur | Tanggal aktifkan | Fitur ditambahkan | Status fitur | Modul |
| --- | --- | --- |--- |--- |
| Mengaktifkan operasi asinkron saat pengguna perlu beralih antara operasi sinkronisasi dan asinkron | 21 Oktober 2022 | 9 April 2021 | Aktif secara default | Manajemen pengeluaran |
| Evaluasi kebijakan biaya untuk penerimaan yang diperlukan | 21 Oktober 2022 | 20 Desember 2021 | Aktif secara default | Manajemen pengeluaran |
| Tampilan daftar laporan pengeluaran yang dibuat oleh mendelegasikan pekerja | 21 Oktober 2022 | 19 Februari 2020 | Aktif secara default | Manajemen pengeluaran |
| Total mileage dihitung berdasarkan tahun fiskal | 21 Oktober 2022 | 10 Mei 2022 | Aktif secara default | Manajemen pengeluaran |

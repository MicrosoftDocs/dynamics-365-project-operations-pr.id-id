---
title: Yang baru di bulan September 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di perilisan Microsoft Dynamics 365 Project Operations pada September 2022 untuk skenario berbasis sumber daya/non-stok.
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

- Project Operations dalam lingkungan Dataverse versi 4.46.0.60
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.29

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

| Area fitur | Nama fitur | Informasi selengkapnya |
| --- | --- | --- |
| Manajemen peluang | **Revisi dan Aktivasi Kuotasi**<br>Project Operations menghadirkan dukungan penuh proses penjualan. Kuotasi proyek dapat diaktifkan untuk menunjukkan status lokasi kuotasi hanya baca dan sedang ditinjau. Kuotasi yang diaktifkan dapat direvisi untuk membuat kuotasi baru yang memiliki penambahan jumlah revisi. Kuotasi proyek yang diaktifkan atau revisi kuotasi bisa ditutup sebagai menang atau kalah. | [Mengaktifkan dan merevisi kuotasi proyek](/dynamics365/project-operations/sales/activation-and-revision) |
| Penagihan dan Harga | **Default harga agnostis zona waktu**<br>Project Operations telah memperkenalkan konsep tanggal agnostis zona waktu pada semua aktual proyek. Bidang baru, **Tanggal transaksi**, sekarang tersedia pada baris dan lini jurnal, dan akan digunakan untuk menyimpan tanggal transaksi terjadi, namun tanpa mengkonversi tanggal tersebut ke Waktu Universal Terkoordinasi. Tanggal ini akan digunakan untuk proses hilir seperti default harga dan pembuatan faktur. | <p>[Menentukan harga penjualan untuk estimasi proyek dan aktual](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Menentukan harga penjualan untuk estimasi dan aktual berbasis proyek](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Penagihan dan Harga | **Penimpaan harga tanggal berlaku dalam Project Operations**<br>Penimpaan harga tanggal berlaku memberikan cara menimpa atau mengubah harga tertentu dalam daftar harga. | [Penimpaan harga tanggal berlaku](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Membuat subkontrak | **Rekonsiliasi subkontrak dan faktur vendor**<br>Fitur ini memungkinkan pelanggan membuat subkontrak untuk membeli waktu sumber daya, kategori pengeluaran, dan materi yang digunakan untuk pekerjaan proyek. Hal ini juga memungkinkan pelanggan untuk merekam, dalam aplikasi keuangan dan operasi, faktur vendor yang akan tersedia untuk manajer proyek di Dataverse untuk verifikasi. | <p>[Manajemen subkontrak](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Buat faktur vendor](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Waktu dan Pengeluaran | **Pemberi Izin Global**<br>Fitur ini memungkinkan vendor perangkat lunak independen (ISV) dan persetujuan terpusat, tanpa melihat status proyek atau anggota tim dalam proyek. | [Keamanan dan persetujuan](/dynamics365/project-operations/approvals/approvals-security) |
| Manajemen pengeluaran | **Kemampuan untuk memposting tanggung jawab pengeluaran dalam mata uang vendor**<br>Fitur ini memungkinkan laporan pengeluaran diposting dalam mata uang vendor untuk metode pembayaran tunai. | [Kemampuan untuk memposting tanggung jawab pengeluaran dalam mata uang vendor](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Pengadaan Proyek | **Pembayaran vendor "bayar jika dibayar"**<br>Fitur ini memungkinkan fitur Bayar bila dibayar (PWP) yang akan digunakan dengan lingkungan non-stok Project Operations. Hal ini memungkinkan pembayaran vendor diblokir/dipertahankan, berdasarkan persyaratan retensi, hingga pembayaran diterima dari pelanggan. | [Pembayaran vendor "bayar jika dibayar"](/dynamics365/project-operations/procurement/pay-when-paid) |
| Pengadaan Proyek | **Permintaan pembelian proyek**<br>Fitur ini memungkinkan pengguna membuat pesanan pembelian terkait proyek dalam entitas hukum dengan integrasi Project Operations on Dynamics 365 Customer Engagement yang diaktifkan. Pesanan pembelian proyek dapat digunakan untuk merekam pengadaan materi non-stok terhadap proyek oleh Persona departemen Pengadaan. Pesanan pembelian proyek tidak akan disinkronisasikan ke Dataverse Namun, Anda dapat menggunakan entitas virtual untuk menampilkan baris pesanan pembelian dalam Dataverse untuk informasi manajer proyek. Biaya faktur vendor yang terkait dengan proyek diintegrasikan dengan entitas Project Actuals dalam Dataverse. Biaya proyek direkam dalam buku besar pembantu Proyek dengan menggunakan jurnal Integrasi Project Operations. | |
|Perencanaan dan Pelacakan Proyek|**Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan** </br> </br>API pengeditan kontur penugasan sumber daya memungkinkan pengembang secara terprogram menentukan upaya penerima tugas di semua rentang tanggal yang didukung untuk perencanaan upaya bertahap waktu yang lebih terperinci.|[Menggunakan API jadwal proyek untuk melakukan operasi dengan entitas Penjadwalan](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tabel berikut menampilkan peta penulisan ganda yang telah dimodifikasi atau ditambahkan perilisan Project Operations pada September 2022.

| Peta entitas | Pembaruan versi | Komentar |
| -------------- | ------------------- | ------------|
| Aktual Integrasi Project Operations (msdyn_actuals) | 1.0.0.15 | Peta ini mendukung pemrosesan aktual subkontrak dengan Project Operations untuk skenario berbasis sumber daya. |
| Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Peta ini mendukung pemrosesan aktual subkontrak dengan Project Operations untuk skenario berbasis sumber daya. |
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Peta ini mendukung pemrosesan aktual subkontrak dengan Project Operations untuk skenario berbasis sumber daya. |

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2754422 | Estimasi Materi dan Pengeluaran tidak mengalir ke Finance saat proyek disalin dalam Dataverse. |
| Waktu dan Pengeluaran | 2787409 | Pemberi izin yang tidak valid dapat menyetujui entri waktu non-proyek. |
| Manajemen peluang | 2788907 | Pesan kesalahan yang diperbarui pada validasi keunikan untuk baris pesanan yang mencakup tanda bendera. |
| Waktu dan Pengeluaran | 2842253 | Penanganan pengecualian nihil untuk persetujuan waktu. |
| Penagihan dan Harga | 2844181 | Gagal mendapatkan blok ID korelasi memblokir pembuatan faktur. |
| Penagihan dan Harga | 2876628 | QLD, CLD - Memperkirakan resolusi daftar harga harus menggunakan bidang rentang tanggal warisan dari daftar harga. |
| Membuat subkontrak | 2893222 | Jika tidak ada peran yang ditentukan untuk baris subkontrak, maka baris tersebut dapat dipilih pada anggota tim untuk peran apa pun. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Fitur diaktifkan secara default di rilis mendatang

Tabel berikut berisi daftar fitur yang diaktifkan secara default di versi 10.0.30. Sebagian besar fitur yang telah secara otomatis diaktifkan dapat dinonaktifkan dalam [manajemen Fitur](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Di masa mendatang, sejumlah fitur yang telah secara otomatis diaktifkan dapat dihilangkan dari manajemen Fitur dan menjadi wajib. Perubahan ini akan memastikan bahwa pelanggan menggunakan fungsi saat ini, sehingga peningkatan dapat dibuat pada fungsi saat ini saat ditambahkan. Fitur tidak akan diaktifkan secara otomatis dalam waktu kurang dari satu tahun, kecuali jika ditentukan untuk menjadi penting.

| Nama fitur | Tanggal aktifkan | Fitur ditambahkan | Status fitur | Modul |
| --- | --- | --- |--- |--- |
| Mengaktifkan operasi asinkron saat pengguna harus beralih antara operasi sinkronisasi dan asinkron | 21 Oktober 2022 | 9 April 2021 | Aktif secara default | Manajemen pengeluaran |
| Evaluasi kebijakan pengeluaran untuk penerimaan yang diperlukan | 21 Oktober 2022 | 20 Desember 2021 | Aktif secara default | Manajemen pengeluaran |
| Tampilan daftar laporan pengeluaran yang dibuat dengan mendelegasi pekerja | 21 Oktober 2022 | 19 Februari 2020 | Aktif secara default | Manajemen pengeluaran |
| Penghitungan total jarak tempuh berdasarkan tahun fiskal | 21 Oktober 2022 | 10 Mei 2022 | Aktif secara default | Manajemen pengeluaran |

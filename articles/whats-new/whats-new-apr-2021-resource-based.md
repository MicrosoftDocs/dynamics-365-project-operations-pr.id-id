---
title: Yang baru di April 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di rilis Project Operations april 2021 untuk skenario berbasis sumber daya/non stok.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 490b7aa38bfdfbcdce21a21e582296e4ce15aeeb
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029258"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di April 2021 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

- Lingkungan Project Operations untuk Dataverse versi 4.9.0.221
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.17

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- Bahan tanpa stok untuk proyek. Kemampuan utama mencakup:
  - Memperkirakan dan menentukan harga bahan yang tidak tersedia selama siklus penjualan untuk proyek. Untuk informasi lebih lanjut, lihat [Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Melacak penggunaan bahan yang tidak tersedia selama pelaksanaan proyek. Untuk informasi lebih lanjut, lihat [Merekam penggunaan bahan pada proyek dan tugas proyek](../material/material-usage-log.md).
  - Menagih biaya bahan non stok yang digunakan. Untuk informasi lebih lanjut, [lihat Mengelola akumulasi penagihan](../proforma-invoicing/manage-billing-backlog.md).
  - Untuk informasi tentang cara mengkonfigurasi fitur ini, lihat [Mengkonfigurasi bahan non-stok dan faktur vendor tertunda](../procurement/configure-materials-nonstocked.md)
- Penagihan berbasis tugas: Menambahkan kemampuan untuk mengaitkan tugas proyek dengan baris kontrak proyek, sehingga tergantung pada metode penagihan, frekuensi faktur, dan pelanggan yang sama seperti yang ada di baris kontrak. Keterkaitan ini memastikan faktur, akuntansi, estimasi pendapatan, dan pengakuan yang akurat untuk berfungsi sesuai dengan konfigurasi ini pada tugas proyek.
- API baru di Dynamics 365 Dataverse memungkinkan operasi buat, perbarui, dan hapus dengan **entitas Penjadwalan**. Untuk informasi lebih lanjut, lihat [Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Daftar berikut menampilkan peta penulisan ganda yang telah dimodifikasi atau ditambahkan dalam rilis Project Operations April 2021.

| **Peta entitas** | **Pembaruan versi** | **Komentar** |
| --- | --- | --- |
| Aktual Integrasi Project Operations (msdyn\_actuals) | 1.0.0.14 | Petakan dimodifikasi untuk mensinkronisasi aktual proyek bahan. |
| Entitas integrasi Project Operations untuk estimasi pengeluaran (msdyn\_estimateslines) | 1.0.0.2 | Menambahkan sinkronisasi baris kontrak proyek ke aplikasi keuangan dan operasi untuk dukungan penagihan berbasis tugas. |
| Entitas integrasi Project Operations untuk estimasi jam (msdyn\_resourceassignments) | 1.0.0.5 | Menambahkan sinkronisasi baris kontrak proyek ke aplikasi keuangan dan operasi untuk dukungan penagihan berbasis tugas. |
| Tabel integrasi Project Operations untuk estimasi bahan (msdyn\_estimatelines) | 1.0.0.0 | Peta tabel baru untuk mensinkronisasikan estimasi bahan dari Dataverse ke aplikasi keuangan dan operasi. |
| Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Peta tabel baru untuk mensinkronisasikan header faktur vendor dari aplikasi aplikasi keuangan dan operasi ke Dataverse. |
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Peta tabel baru untuk mensinkronisasikan baris faktur vendor dari aplikasi aplikasi keuangan dan operasi ke Dataverse. |

Anda harus selalu menjalankan versi peta terbaru di lingkungan Anda dan mengaktifkan semua peta tabel terkait saat memperbarui solusi Project Operations Dataverse dan versi solusi keuangan dan operasi Anda. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta pada kolom **Versi** pada halaman **Penulisan ganda**. Anda dapat mengaktifkan versi baru peta dengan memilih **versi peta Tabel**, memilih versi terbaru, kemudian menyimpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations di Dynamics 365 Dataverse

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan harga | 2124532 | Tombol **Koreksi Faktur** ditampilkan pada faktur proforma saat jumlah panjar atau jumlah panjar yang diterapkan ada di faktur asli. Tombol tersebut ditampilkan hanya untuk lingkungan dengan Finance versi 10.0.19 atau yang lebih tinggi. |
| Penagihan dan harga | 2224568 | Menambahkan logika untuk mengaktifkan penyesuaian yang melibatkan faktur plug-in konfirmasi faktur. |
| Penagihan dan harga | 2101098 | Meningkatkan logika bidang default ke faktur proforma: **Alamat Tagihan**, **Tagihan ke Nama**, dan **Persyaratan Pembayaran** sekarang default dari rekaman pelanggan kontrak proyek yang terkait. |
| Penagihan dan harga | 2021413 | Memperbarui bidang **Biaya Aktual** dan **Penjualan** pada entitas **Tugas** untuk mencakup nilai penjualan dari pengeluaran yang belum ditagih dan ditagih pada tugas. |
| Penagihan dan harga | 2182110 | Saat menyalin kontrak proyek, ID baris kontrak diregenerasi dalam kontrak proyek tujuan untuk memastikan keunikannya. |
| Manajemen peluang | 2186741 | Menambahkan validasi untuk memastikan bidang **Asal** dan **Jenis Transaksi** tidak dapat diperbarui pada rincian baris kuotasi yang ada. |
| Manajemen peluang | 2191353 | Tahapan tidak boleh dibuat pada baris kontrak waktu dan bahan. |
| Manajemen peluang | 2216956 | Memperbaiki masalah **Pembaruan Harga**. |
| Perencanaan dan Pelacakan | 2182979 | Fungsi salinan proyek ditingkatkan untuk memastikan baris estimasi pengeluaran disalin dari proyek asli. |
| Perencanaan dan Pelacakan | 2184144 | Fungsi salinan proyek ditingkatkan untuk memastikan nama posisi sumber daya disalin dari proyek asli. |
| Perencanaan dan Pelacakan | 2184799 | Salinan proyek: Kontrol yang dikuatkan untuk memastikan perkiraan tanggal mulai tidak dapat diubah saat penyalinan sedang berlangsung. |
| Perencanaan dan Pelacakan | 2185134 | Salinan proyek: Tanggal mulai perkiraan proyek tujuan diatur ke tanggal hari ini. |
| Perencanaan dan Pelacakan | 2196373 | Salinan proyek: Memastikan rekaman manajer proyek dan anggota tim tidak diduplikasikan dalam tim proyek. |
| Perencanaan dan Pelacakan | 2211833 | Salinan proyek: Penugasan sumber daya disalin dari tugas proyek sumber ke proyek tujuan. |
| Perencanaan dan Pelacakan | 2186541 | Memperbaiki masalah di kisi **Estimasi** saat mengelompokkan berdasarkan sumber daya. |
| Perencanaan dan Pelacakan | 2166906 | Kategori transaksi dari tugas harus disalin ke entitas **Penetapan Sumber Daya**. |
| Manajemen sumber daya | 2125362 | Memperbaiki masalah saat membuat anggota tim generik menggunakan metode alokasi berbasis jam. |
| Waktu dan Pengeluaran | 2113603 | Memperbaiki masalah yang terkait dengan penyesuaian dengan menghapus atribut dari halaman **Entri Waktu**. Sistem sekarang memeriksa apakah atribut sudah ada pada halaman sebelum mengaksesnya menggunakan skrip. |
| Waktu dan Pengeluaran | 2204377 | Lembar waktu yang disalin harus ditampilkan secara otomatis bila Anda memilih **Salin Pekan** selama entri waktu. |
| Waktu dan Pengeluaran | 2209059 | Bidang **status** dapat diedit untuk entri waktu Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Manajemen proyek dan akuntansi | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Penghapusan perkiraan mundur tidak berfungsi pada bagian **Berkala**.  |
| Manajemen proyek dan akuntansi | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Fitur **penyesuaian akuntansi** membuat masalah dengan akun buku besar yang **tidak mengizinkan entri manual** dipilih. |
| Manajemen proyek dan akuntansi | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Menambahkan logika bisnis untuk memproses faktur koreksi termasuk jumlah panjar atau jumlah panjar yang diterapkan. |
| Manajemen proyek dan akuntansi | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | WIP - nilai penjualan yang diposting dalam pembuatan faktur proyek antarperusahaan memilih akun yang tidak terduga. |
| Manajemen proyek dan akuntansi | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Ketika bekerja dengan panjar di Project Operations, mengubah proyek default pada kontrak setelah pembayaran di muka ditagihkan menyebabkan masalah dengan potongan yang masuk. |
| Manajemen proyek dan akuntansi | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Di Project Operations, menghapus proyek dari kontrak harus mengatur ulang proyek default kontrak, jika diperlukan. |
| Manajemen proyek dan akuntansi | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | Di Project Operations, baris pengeluaran yang salah ditampilkan di daftar **Tambah baris** di faktur antarperusahaan. |
| Manajemen proyek dan akuntansi | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | Dalam Project Operations, halaman **Perjanjian Pembelian** tidak dapat dilihat dalam entitas hukum Finance yang terintegrasi dengan Project Operations. |
| Manajemen proyek dan akuntansi | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Karena kesalahan integrasi Dataverse, Anda tidak dapat mengkonversi kuotasi untuk dimenangkan di Project Operations. |
| Manajemen proyek dan akuntansi | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** dapat mengatur alamat faktur sumber dana dari pelanggan yang berbeda.  |
| Manajemen proyek dan akuntansi | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Di Project Operations, tidak ada dimensi yang dipilih saat Anda membuat faktur posting untuk transaksi. |
| Perjalanan dan pengeluaran | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Saldo kasbon tunai tidak diperbarui untuk laporan pengeluaran jika disetujui dan diposting baris demi baris. |
| Perjalanan dan Pengeluaran | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Pajak untuk laporan pengeluaran antarperusahaan item tidak dihitung dengan benar. |
| Perjalanan dan Pengeluaran | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Bidang tambahan yang terkait dengan proyek ditampilkan di halaman **laporan pengeluaran antar perusahaan** konsep ulang. |
| Perjalanan dan Pengeluaran | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Pesan kesalahan yang salah terjadi pada header tanda terima laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Laporan pengeluaran tidak diposting dengan benar dalam skenario antarperusahaan jika pajak penjualan diposting ke entitas hukum tujuan. |
| Perjalanan dan Pengeluaran | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Tanggal pengajuan laporan tidak dicetak pada laporan pengeluaran yang disetujui. |
| Perjalanan dan Pengeluaran | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Bidang **Tanggal Disetujui** dan **Tanggal Ditolak** tidak diisi setelah pengeluaran disetujui. |
| Perjalanan dan Pengeluaran | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Permintaan ulang perjalanan yang dibuat untuk satu pekerja dapat digunakan untuk laporan pengeluaran pekerja lain. |
| Perjalanan dan Pengeluaran | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Kategori pengeluaran terkunci saat menambahkan baris pengeluaran baru. |
| Perjalanan dan Pengeluaran | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Meringkas baris laporan pengeluaran yang sudah terpisah mengakibatkan posting tidak lengkap dari voucher utang dagang\buku besar Umum dan memecah Penjelajah Sumber Akuntansi karena **TRVEXPTRANS. SOURCEDOCUMENTLINE** diduplikasikan. |
| Perjalanan dan Pengeluaran | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Kebijakan permintaan perjalanan tidak berfungsi sebagaimana yang diharapkan. |
| Perjalanan dan Pengeluaran | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Nama akun vendor tidak ditampilkan pada transaksi proyek yang diposting untuk laporan pengeluaran. |
| Perjalanan dan Pengeluaran | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Dalam Project Operations, Anda tidak dapat menyetujui waktu dengan tugas untuk proyek antarperusahaan. |
| Perjalanan dan Pengeluaran | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategori pengembalian kasbon tunai tidak memperbarui saldo kasbon saat diposting. |
| Perjalanan dan Pengeluaran | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Harga penjualan dihitung dengan keliru pada laporan pengeluaran yang dibuat dalam mata uang asing menggunakan transaksi kartu kredit impor dan dikaitkan dengan proyek. |
| Perjalanan dan Pengeluaran | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Mengembalikan entitas data **TrvRequisitionLine** dan indeks unik terkait. |
| Perjalanan dan Pengeluaran | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Menambahkan instrumentasi ke pembuatan **SOURCEDOCUMENTLINE**. |
| Perjalanan dan Pengeluaran | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Jurnal buku besar pembantu keliru ditampilkan dalam skenario antarperusahaan jika pajak penjualan diposting ke entitas hukum tujuan. |
| Perjalanan dan Pengeluaran | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Dalam Project Operations, estimasi pengeluaran tidak akan dihapus dari Finance bila dihapus dari Dataverse. |
| Perjalanan dan Pengeluaran | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Bila kategori pengeluaran adalah kategori non-proyek, dimensi keuangan yang dipilih pada halaman **Pengeluaran** tidak disalin ke laporan pengeluaran. |

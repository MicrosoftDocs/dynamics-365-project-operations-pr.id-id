---
title: Konsep unik untuk kuotasi berbasis proyek
description: Artikel ini menyediakan informasi tentang kutipan proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 89867cfbe92f47d58b16da40b62d3d9dd6a15b64
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824331"
---
# <a name="concepts-unique-to-project-based-quotes"></a>Konsep unik untuk kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Sebelum Anda mulai menggunakan kutipan proyek di Microsoft Dynamics 365 Project Operations, Anda harus menyadari konsep-konsep kunci berikut.

## <a name="owning-company"></a>Perusahaan Pemilik

Perusahaan pemilik mewakili badan hukum yang memiliki pengiriman proyek. Pelanggan pada penawaran harus menjadi pelanggan yang sah dalam badan hukum tersebut dalam aplikasi keuangan dan operasi. Mata uang perusahaan pemilik dan mata uang unit kontrak yang dipilih pada kutipan berbasis proyek harus cocok.

## <a name="contracting-unit"></a>Unit Kontrak

Unit kontrak mewakili divisi atau praktik yang memiliki pengiriman proyek. Anda dapat mengatur biaya sumber daya untuk setiap unit kontrak. Saat Anda menentukan biaya sumber daya untuk sumber daya dalam unit kontrak, Anda dapat menyiapkan tarif biaya yang berbeda untuk sumber daya yang dipinjam oleh unit kontraktor, atau untuk divisi atau praktik lain di perusahaan. Tarif biaya ini disebut sebagai harga transfer, pinjaman sumber daya, atau harga tukar. Ketika Anda mengatur biaya meminjam sumber daya dari divisi lain, Anda dapat mengatur tingkat biaya dalam mata uang divisi pinjaman.

## <a name="cost-currency"></a>Mata uang biaya

Mata uang biaya dalam Operasi Proyek adalah mata uang yang dilaporkan biayanya. Mata uang ini berasal dari mata uang yang dilampirkan ke **bidang unit** Kontrak pada kuotasi, kontrak, dan proyek. Biaya terhadap proyek dapat dicatat dalam mata uang apa pun. Namun, ada konversi mata uang dari mata uang yang biaya dicatat ke mata uang biaya proyek.

Karena nilai tukar di Dataverse platform tidak dapat efektif untuk tanggal, total biaya di layar mungkin berubah seiring waktu jika Anda memperbarui nilai tukar mata uang. Namun, biaya yang dicatat dalam database tetap tidak berubah, karena jumlahnya disimpan dalam mata uang yang dikeluarkan.

## <a name="sales-currency"></a>Mata Uang Penjualan

Mata uang penjualan dalam Operasi Proyek adalah mata uang yang dicatat dan ditampilkan dalam jumlah perkiraan dan penjualan aktual. Ini juga merupakan mata uang yang ditagih oleh pelanggan untuk kesepakatan tersebut. Untuk kutipan proyek, mata uang penjualan default diatur dari catatan pelanggan atau akun, dan dapat diubah saat kutipan dibuat. Namun, mata uang penjualan tidak dapat diubah setelah kuotasi disimpan. Daftar harga produk dan proyek default ditetapkan berdasarkan mata uang penjualan kuotasi.

Tidak seperti biaya, nilai penjualan hanya **dapat dicatat** dalam mata uang penjualan.

## <a name="billing-method"></a>Metode Penagihan

Proyek biasanya memiliki model kontrak berbasis biaya tetap dan konsumsi. Dalam Operasi Proyek, model kontrak proyek diwakili oleh metode penagihan. Metode penagihan memiliki dua nilai: waktu dan material dan harga tetap.

- **Waktu dan material** – Model kontrak berbasis konsumsi di mana setiap biaya yang dikeluarkan didukung oleh pendapatan yang sesuai. Saat Anda memperkirakan atau mengeluarkan lebih banyak biaya, estimasi penjualan dan penjualan aktual juga meningkat. Anda dapat menentukan batas yang tidak melebihi batas pada baris kuotasi yang memiliki metode penagihan ini. Dengan cara ini, Anda dapat membatasi pendapatan aktual. Estimasi pendapatan tidak dipengaruhi oleh batas yang tidak terlampaui.
- **Harga**  tetap– Model kontrak biaya tetap di mana nilai penjualan tidak tergantung pada biaya yang dikeluarkan. Nilai penjualan adalah tetap dan tidak berubah saat Anda memperkirakan atau menimbulkan lebih banyak biaya.

## <a name="project-price-lists"></a>Daftar harga proyek

Daftar harga proyek adalah daftar harga yang digunakan untuk memasukkan harga default, bukan tarif biaya, untuk waktu, pengeluaran, dan komponen terkait proyek lainnya. Terdapat beberapa daftar harga, dan setiap daftar dapat memiliki efektifitas tanggalnya sendiri untuk setiap kuotasi proyek. Operasi Proyek tidak mendukung efektivitas tanggal yang tumpang tindih untuk daftar harga proyek.

## <a name="product-price-lists"></a>Daftar harga produk

Daftar harga produk adalah daftar harga yang digunakan untuk memasukkan harga default, bukan tarif biaya, untuk baris berbasis produk pada kutipan. Hanya ada satu daftar harga produk per penawaran.

## <a name="transaction-classes"></a>Kelas Transaksi

Project Operations mendukung empat jenis kelas transaksi:

- Waktu
- Pengeluaran
- Materi
- Biaya

Nilai biaya dan penjualan dapat diperkirakan dan dikeluarkan pada **kelas transaksi Time**, Expense **,** dan **Material** . **Biaya** adalah kelas transaksi khusus pendapatan.

## <a name="work-entities-and-billing-entities"></a>Entitas kerja dan entitas penagihan

Proyek dan Tugas adalah entitas yang mewakili pekerjaan. Garis kutipan dan Garis kontrak adalah entitas yang mewakili penagihan. Anda dapat menautkan entitas kerja yang berbeda ke opsi penagihan dengan mengaitkannya dengan baris Kutipan atau baris Kontrak.

## <a name="multi-customer-deals"></a>Penawaran Multi-pelanggan

Transaksi multi-pelanggan terjadi ketika ada lebih dari satu pelanggan per faktur. Berikut adalah beberapa contoh umum:

- **Perusahaan produsen peralatan asli (OEM) dan mitra**  mereka– Mitra dan pengecer menjual produk yang mencakup layanan bernilai tambah. Selama kesepakatan dengan pelanggan, OEM biasanya menawarkan untuk membiayai bagian dari proyek.
- **Proyek**  sektor publik– Beberapa departemen pemerintah daerah setuju untuk mendanai proyek dan ditagih sesuai dengan perpecahan yang telah disepakati sebelumnya. Misalnya, distrik sekolah dan kota atau departemen pemerintah daerah setuju untuk mendanai pembangunan kolam renang.

## <a name="invoice-schedules"></a>Jadwal faktur

Jadwal faktur khusus untuk setiap baris kutipan dan bersifat opsional. Jadwal faktur dibuat berdasarkan tanggal mulai dan akhir tertentu dan frekuensi faktur. Mereka digunakan selama tahap kontrak, ketika proses pembuatan faktur otomatis dikonfigurasi. Selama tahap penawaran, jadwal faktur bersifat opsional. Jika dibuat selama tahap kutipan, mereka disalin ke kontrak proyek yang dibuat saat penawaran proyek dimenangkan.

## <a name="differences-from-dynamics-365-sales-quotes"></a>Perbedaan dari penawaran Dynamics 365 Sales

Kutipan Operasi Proyek dibangun di atas kutipan Dynamics 365 Sales. Namun, ada beberapa perbedaan penting dalam fungsi yang harus Anda sadari:

- Kutipan Operasi Proyek memiliki dua jenis baris yang berbeda: satu untuk proyek dan satu untuk produk.
- Kutipan Operasi Proyek memiliki halaman dan elemen antarmuka pengguna (UI), aturan bisnis, logika bisnis dalam plug-in, dan skrip sisi klien yang membuatnya berbeda dari kutipan Penjualan.
- Dalam Penjualan, Anda dapat melampirkan beberapa pesanan ke satu penawaran penjualan. Dalam Operasi Proyek, Anda hanya dapat melampirkan satu kontrak proyek ke penawaran proyek.
- Ketika Anda memenangkan penawaran penjualan, peluang terkait dapat tetap terbuka. Setelah kuotasi proyek dimenangkan, peluang terkait ditutup.
- Kutipan penjualan tidak menyertakan beberapa bidang dan konsep yang disertakan dalam kutipan proyek. Bidang mencakup **unit kontrak**, **manajer akun**, dan **nama tagihan ke kontak**.
- Kutipan penjualan dan kutipan proyek diidentifikasi oleh bidang Jenis **berbasis** rangkaian pilihan. Untuk penawaran penjualan, nilai bidang ini berbasis **Item**. Untuk kutipan proyek, nilainya adalah **Berbasis** pekerjaan.

Karena perbedaan ini, kami tidak menyarankan Anda menggunakan kutipan Penjualan dan kutipan Operasi Proyek secara bergantian.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

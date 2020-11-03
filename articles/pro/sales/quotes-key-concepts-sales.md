---
title: Konsep kunci kuotasi proyek
description: Topik ini memberikan informasi tentang cara menggunakan kuotasi proyek di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 64d2fd9bab9452d71e8cd194fbab70edadf00b93
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078408"
---
# <a name="project-quote-key-concepts"></a>Konsep kunci kuotasi proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_


Berikut adalah konsep penting yang perlu diperhatikan sebelum Anda mulai menggunakan kuotasi proyek di Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unit Kontrak

Unit kontrak menunjukkan pembagian atau praktik yang bertanggung jawab atas hasil proyek. Anda dapat mengatur biaya sumber daya untuk setiap unit kontrak. Bila Anda menentukan biaya sumber daya untuk sumber daya di unit kontrak, Anda juga akan dapat menetapkan tarif biaya yang berbeda untuk sumber daya yang dipinjam oleh unit kontrak ini, atau divisi atau praktik lain di dalam perusahaan. Ini disebut sebagai harga transfer, peminjaman sumber daya, atau harga pertukaran. Bila Anda mengatur biaya sumber daya pinjaman dari divisi lain, Anda juga dapat memilih untuk mengatur tarif biaya tersebut dalam mata uang Divisi pemberi pinjaman.

## <a name="cost-currency"></a>Mata uang biaya

Mata uang biaya dalam Project Operations adalah mata uang di mana biaya dilaporkan. Mata uang ini berasal dari mata uang yang melekat pada bidang **unit kontrak** pada kuotasi, kontrak, dan proyek. Biaya dapat dicatat dalam mata uang apa pun terhadap proyek. Namun, ada konversi mata uang dari biaya mata uang yang direkam, ke mata uang biaya proyek.

Karena nilai tukar di platform CDS tidak bisa efektif tanggal, total di layar untuk biaya dapat berubah seiring waktu jika Anda memperbarui nilai tukar mata uang. Namun, biaya yang tercatat di database tetap tidak berubah karena jumlah disimpan dalam mata uang pembebanannya.

## <a name="sales-currency"></a>Mata Uang Penjualan

Mata uang penjualan dalam Project Operations adalah mata uang di mana perkiraan dan jumlah penjualan yang sebenarnya dicatat dan ditampilkan. Mata uang ini juga merupakan mata uang penagihan pelanggan untuk transaksi. Pada kuotasi proyek, mata uang penjualan default dari rekaman pelanggan atau akun dan dapat diubah saat kuotasi dibuat. Setelah kuotasi disimpan, mata uang penjualan tidak dapat diubah. Produk dan daftar harga proyek di-default berdasarkan mata uang penjualan kuotasi.

Tidak seperti biaya, nilai penjualan hanya dapat direkam dalam mata uang penjualan.

## <a name="billing-method"></a>Metode Penagihan

Proyek biasanya memiliki ongkos tetap dan model kontrak berbasis konsumsi. Ini ditunjukkan dalam Project Operations sebagai **metode penagihan** dan memiliki dua nilai, waktu dan bahan serta harga tetap.

- **Waktu dan bahan:** ini adalah model kontrak berbasis konsumsi di mana setiap biaya yang dikeluarkan didukung oleh pendapatan yang sesuai. Saat Anda memperkirakan atau mengeluarkan lebih banyak biaya, estimasi penjualan dan penjualan aktual juga akan meningkat. Anda dapat menentukan batas yang tidak melebihi batas pada baris kuotasi yang memiliki metode penagihan ini. Ini akan menjadi batas untuk pendapatan yang sebenarnya. Estimasi pendapatan tidak dipengaruhi oleh batas yang tidak boleh terlampaui.
- **Harga tetap:** ini adalah model kontrak biaya tetap yang menunjukkan nilai penjualan akan independen dari biaya yang dikeluarkan. Nilai penjualan adalah tetap dan tidak berubah saat Anda memperkirakan atau menimbulkan lebih banyak biaya.

## <a name="project-price-lists"></a>Daftar harga proyek

Daftar harga proyek adalah daftar harga yang digunakan untuk harga default, bukan tarif biaya, untuk waktu, pengeluaran, dan komponen terkait proyek lainnya. Terdapat beberapa daftar harga, dan setiap daftar dapat memiliki efektifitas tanggalnya sendiri untuk setiap kuotasi proyek. Tumpang-tindih efektivitas tanggal di daftar harga proyek tidak didukung di Project Operations.

## <a name="product-price-lists"></a>Daftar harga produk

Daftar harga produk adalah daftar harga yang digunakan untuk harga default, bukan tarif biaya, untuk baris berdasarkan produk pada kuotasi. Hanya ada satu daftar harga produk per kuotasi.

## <a name="transaction-classes"></a>Kelas Transaksi

Project Operations mendukung empat jenis kelas transaksi:

- Waktu
- Pengeluaran
- Materi
- Biaya

Nilai biaya dan penjualan dapat diperkirakan dan ditimbulkan pada kelas transaksi waktu, pengeluaran, dan material. Ongkos adalah kelas transaksi hanya pendapatan.

## <a name="work-entities-and-billing-entities"></a>Entitas kerja dan entitas penagihan

Entitas yang menunjukkan pekerjaan adalah proyek dan tugas. Entitas yang menunjukkan penagihan adalah baris kuotasi dan baris kontrak. Anda dapat menautkan berbagai entitas kerja ke pilihan penagihan dengan mengasosiasinya dengan baris kuotasi atau kontrak.

## <a name="multi-customer-deals"></a>Penawaran Multi-pelanggan

penawaran multi-pelanggan terjadi ketika ada lebih dari satu pelanggan untuk faktur. Contoh umum mencakup:

- **Perusahaan OEM dan mitra mereka:** mitra dan pengecer menjual produk dengan layanan bernilai tambah. Biasanya ini adalah skenario saat menangani kesepakatan tertentu dengan pelanggan, OEM menawarkan untuk membiayai sebagian dari proyek. 

- **Proyek sektor publik:** beberapa Departemen dari pemerintah daerah setuju untuk mendanai proyek dan ditagih sesuai dengan pembagian yang disetujui sebelumnya. Misalnya, distrik sekolah dan kota atau departemen pemerintah daerah setuju untuk mendanai pembangunan kolam renang.

## <a name="invoice-schedules"></a>Jadwal faktur

Jadwal faktur khusus untuk setiap baris kuotasi dan juga opsional. Jadwal faktur dibuat berdasarkan tanggal mulai dan selesai dan frekuensi faktur tertentu. Jadwal faktur digunakan dalam tahap kontrak saat proses pembuatan faktur otomatis dikonfigurasi. Pada tahapan kuotasi, jadwalnya opsional. Ketika jadwal faktur dibuat dalam tahap **kuotasi** , mereka akan disalin ke kontrak proyek yang dibuat saat kuotasi proyek dimenangkan.

## <a name="changes-from-dynamics-365-sales-quote"></a>Perubahan dari kuotasi Dynamics 365 Sales:

Kuotasi Project Operations dibuat berdasarkan kuotasi Dynamics 365 Sales. Namun, ada beberapa perbedaan penting dalam fungsi yang harus Anda sadari:

- Tindakan **merevisi** dan **mengaktifkan** tidak didukung.
- Kuotasi Project Operations memiliki dua jenis baris. Satu untuk proyek dan lainnya untuk produk.
- Kuotasi Project Operations memiliki formulir dan elemen UI sendiri, aturan Bisnis, logika bisnis di plug-in, dan skrip sisi klien yang membuatnya unik dari kuotasi Sales.

Untuk alasan ini, tidak disarankan untuk menggunakan kuotasi Sales dan kuotasi Project Operations secara bergantian.

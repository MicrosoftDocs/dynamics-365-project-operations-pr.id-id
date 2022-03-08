---
title: Konsep kunci kontrak proyek
description: Topik ini menyediakan informasi tentang konsep kunci kontrak proyek.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 66d6b72b19a90ecc9161cd16ce9d4dd22798803b
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078390"
---
# <a name="key-concepts-of-project-contracts"></a>Konsep kunci kontrak proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Topik ini memberikan konsep penting yang perlu diperhatikan sebelum Anda mulai menggunakan kontrak proyek di Dynamics 365 Project Operations:

## <a name="contracting-unit"></a>Unit Kontrak

Unit kontrak menunjukkan pembagian atau praktik yang bertanggung jawab atas hasil proyek. Anda dapat mengatur biaya sumber daya untuk setiap unit kontrak. Ketika Anda menentukan biaya sumber daya untuk sumber daya, Anda juga akan dapat mengatur tarif biaya yang berbeda untuk sumber daya. Unit kontrak ini meminjam sumber daya ini dari divisi atau praktik lain dalam perusahaan. Tarif biaya untuk sumber daya disebut sebagai harga transfer, peminjaman sumber daya, atau harga pertukaran. Bila Anda mengatur tarif biaya untuk meminjam sumber daya dari divisi lain, gunakan mata uang Divisi pemberi pinjaman.

## <a name="cost-currency"></a>Mata uang biaya

Mata uang biaya adalah mata uang di mana biaya dilaporkan di layar. Mata uang ini berasal dari mata uang yang melekat pada bidang **unit kontrak** pada kontrak dan proyek. Biaya dapat dicatat dalam mata uang apa pun terhadap proyek. Namun, ada konversi mata uang dari biaya mata uang yang direkam, ke mata uang biaya proyek jika ditampilkan di layar.

Karena nilai tukar di platform Common Data Service (CDS) tidak bisa efektif tanggal, total di layar untuk biaya dapat berubah seiring waktu jika Anda memperbarui nilai tukar mata uang. Namun, biaya yang tercatat di database tetap tidak berubah karena jumlah disimpan dalam mata uang pembebanannya.

## <a name="sales-currency"></a>Mata Uang Penjualan

Mata uang penjualan dalam Project Operations adalah mata uang di mana perkiraan dan jumlah penjualan yang sebenarnya dicatat dan ditampilkan. Mata uang penjualan ini juga merupakan mata uang penagihan pelanggan untuk transaksi. Pada kontrak proyek, mata uang penjualan default dari rekaman pelanggan atau akun dan dapat diubah selama kontrak dibuat. Ketika kontrak dibuat dengan menutup penawaran harga sebagai dimenangkan, mata uang pada kontrak di-default dari mata uang pada penawaran harga.

Saat Anda membuat kontrak proyek dari awal, bidang **Mata Uang Penjualan** tidak dapat diedit. Produk dan daftar harga proyek di-default berdasarkan mata uang ini di kontrak.

Tidak seperti biaya, nilai penjualan hanya dapat direkam dalam mata uang penjualan.

## <a name="billing-method"></a>Metode Penagihan

Biasanya ada dua jenis model kontrak untuk proyek, ongkos tetap dan berbasis konsumsi. Model-model ini diwakili dalam Project Operations sebagai metode penagihan dengan dua nilai yang mungkin:

- Waktu dan bahan: Model kontrak berbasis konsumsi di mana setiap biaya yang dikeluarkan didukung oleh pendapatan yang sesuai. Saat Anda memperkirakan atau mengeluarkan lebih banyak biaya, estimasi penjualan dan penjualan aktual juga meningkat. Tentukan batas yang tidak boleh dilebihi pada baris kontrak yang memiliki metode penagihan ini, yang menutup pendapatan aktual. Estimasi pendapatan tidak dipengaruhi oleh batas yang tidak boleh terlampaui.
- Harga tetap: Model kontrak ongkos tetap yang menunjukkan nilai penjualan akan independen dari biaya yang dikeluarkan. Nilai penjualan adalah tetap dan tidak berubah saat Anda memperkirakan atau menimbulkan lebih banyak biaya.

## <a name="project-price-lists"></a>Daftar harga proyek

Daftar harga proyek igunakan untuk harga default, bukan tarif biaya, untuk waktu, pengeluaran, dan komponen terkait proyek lainnya. Mungkin ada beberapa daftar harga. Setiap daftar harga memiliki efektivitas tanggalnya sendiri untuk setiap kontrak proyek. Tumpang-tindih efektivitas tanggal di daftar harga proyek tidak didukung di Project Operations.

Ketika kontrak proyek dibuat dengan memenangkan kuotasi proyek, daftar harga proyek disalin dengan nama kontrak dan tanggal disertakan. Menyalin informasi ini merupakan harga khusus untuk komponen proyek pada kontrak proyek ini.

## <a name="product-price-lists"></a>Daftar harga produk

Daftar harga produk digunakan untuk harga default, bukan tarif biaya, untuk baris berdasarkan produk pada kontrak. Hanya ada satu daftar harga produk per kontrak.

## <a name="transaction-classes"></a>Kelas Transaksi

Project Operations mendukung empat jenis kelas transaksi:

- Waktu
- Pengeluaran
- Materi
- Biaya

Nilai biaya dan penjualan dapat diperkirakan dan ditimbulkan pada kelas transaksi waktu, pengeluaran, dan material. Ongkos adalah kelas transaksi hanya pendapatan.

## <a name="work-entities-and-billing-entities"></a>Entitas kerja dan entitas penagihan

Entitas yang menunjukkan pekerjaan adalah proyek dan tugas. Entitas yang menunjukkan aspek penagihan adalah baris kontrak. Anda dapat menautkan berbagai entitas kerja ke pilihan penagihan dengan mengikatnya ke baris kontrak.

## <a name="multi-customer-deals"></a>Penawaran Multi-pelanggan

penawaran multi-pelanggan memiliki lebih dari satu pelanggan untuk ditagih pada suatu penawaran. Contoh umumnya termasuk:

- Perusahaan OEM dan mitra mereka: Mitra dan penjual menjual produk dengan beberapa layanan bernilai tambah, biasanya melibatkan kesepakatan tertentu dengan pelanggan. OEM menawarkan untuk membiayai sebagian proyek. 

- Proyek sektor publik: beberapa Departemen dari pemerintah daerah setuju untuk mendanai proyek dan ditagih sesuai dengan pembagian yang disetujui sebelumnya. Misalnya, distrik sekolah dan pemerintah daerah setuju untuk mendanai pembangunan kolam renang.

## <a name="invoice-schedules"></a>Jadwal faktur

Jadwal faktur adalah spesifik untuk setiap baris kontrak dan diperlukan agar faktur otomatis berfungsi. Jadwal faktur dibuat berdasarkan tanggal mulai dan selesai dan frekuensi faktur tertentu. Jadwal digunakan dalam tahap kontrak saat proses pembuatan faktur otomatis dikonfigurasi. Ketika kontrak proyek dibuat dari kuotasi, jadwal faktur disalin ke kontrak proyek dari kuotasi.

## <a name="changes-from-the-dynamics-365-sales-contract"></a>Perubahan dari kontrak Dynamics 365 Sales

Kontrak Project Operations dibuat berdasarkan kontrak di Dynamics 365 Sales. Namun, ada beberapa perbedaan dan penyimpangan penting dalam fungsi yang harus Anda sadari:

- Kontrak Project Operations memiliki dua jenis baris yang berbeda, satu untuk proyek, dan satu untuk produk.
- Kontrak Project Operations memiliki formulir dan elemen UI sendiri, aturan Bisnis, logika bisnis di plug-in, dan skrip sisi klien yang membuatnya unik dari Kontrak Sales.

Untuk alasan ini, Anda tidak boleh menggunakan kontrak penjualan dan kontrak proyek secara bergantian.

---
title: Kontrak proyek - Konsep kunci
description: Topik ini memberikan informasi tentang konsep kunci kontrak proyek di Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ce84984f873e6336a6d065f0aa7a72f1474404a84d3dbb614c09d58bff66d83d
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986945"
---
# <a name="concepts-unique-to-project-based-contracts"></a>Konsep unik untuk kontrak berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Topik ini memberikan konsep penting yang perlu diperhatikan sebelum Anda mulai menggunakan kontrak Proyek di Dynamics 365 Project Operations:

## <a name="owning-company"></a>Perusahaan Pemilik

Perusahaan pemilik merupakan entitas hukum dari modul **manajemen proyek dan akuntansi** untuk Project Operations dari Dynamics 365 Finance. Perusahaan pemilik mewakili entitas hukum yang akan memperhitungkan biaya dan pendapatan yang Diperoleh dari transaksi.

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

penawaran multi-pelanggan memiliki lebih dari satu pelanggan untuk ditagih pada suatu penawaran. Contoh umum mencakup:

- Perusahaan OEM dan mitra mereka: Mitra dan penjual menjual produk dengan beberapa layanan bernilai tambah, biasanya melibatkan kesepakatan tertentu dengan pelanggan. OEM menawarkan untuk membiayai sebagian proyek. 

- Proyek sektor publik: beberapa Departemen dari pemerintah daerah setuju untuk mendanai proyek dan ditagih sesuai dengan pembagian yang disetujui sebelumnya. Misalnya, distrik sekolah dan pemerintah daerah setuju untuk mendanai pembangunan kolam renang.

## <a name="invoice-schedules"></a>Jadwal faktur

Jadwal faktur adalah spesifik untuk setiap baris kontrak dan diperlukan agar faktur otomatis berfungsi. Jadwal faktur dibuat berdasarkan tanggal mulai dan selesai dan frekuensi faktur tertentu. Jadwal digunakan dalam tahap kontrak saat proses pembuatan faktur otomatis dikonfigurasi. Ketika kontrak proyek dibuat dari kuotasi, jadwal faktur disalin ke kontrak proyek dari kuotasi.

## <a name="changes-from-dynamics-365-sales-orders"></a>Perubahan dari Pesanan Dynamics 365 Sales

Kontrak dalam Project Operations dibuat berdasarkan pesanan di Dynamics 365 Sales. Namun, ada penyimpangan penting dan perbedaan fungsi. Kontrak memiliki formulir dan elemen UI sendiri, aturan Bisnis, logika bisnis di plug-in, dan skrip sisi klien yang membuatnya unik dari Pesanan. Untuk alasan ini, jangan gunakan perintah penjualan, dan kontrak Project Operations secara bergantian.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Yang baru di bulan Oktober 2022 - Penyebaran Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Oktober 2022 penyebaran Microsoft Dynamics 365 Project Operations lite.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806736"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Yang baru di bulan Oktober 2022 - Penyebaran Project Operations lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.57.0.176

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

| Area fitur | Nama fitur | Informasi selengkapnya |
| --- | --- | --- |
| Perencanaan dan Pelacakan Proyek | **Penjadwalan Eksternal Operasi Proyek**<br>Mode penjadwalan eksternal memungkinkan pelanggan membuat, memperbarui, dan menghapus entitas yang terkait dengan struktur rincian kerja (WBS) secara native dengan menggunakan API asli Dataverse , tanpa batas saat ini yang diberlakukan oleh Project for the Web. | [Penjadwalan Eksternal](/dynamics365/project-operations/project-management/external-scheduling) |
| Penyebaran dan Konfigurasi | <p>**Izinkan pelanggan memilih jenis penyebaran**<br>Pembaruan berbasis produk (PDU) dari Operasi Proyek digunakan untuk menginstal solusi Penulisan ganda Operasi Proyek secara otomatis saat solusi inti dan orkestrasi tulis ganda diinstal di lingkungan.</p><p>Fitur ini memperkenalkan parameter perilaku **peningkatan Solusi baru** di parameter Project. Ketika parameter ini diatur ke **Lite saja**, PUD tidak akan lagi secara otomatis menginstal solusi Project Operations Dual-write, bahkan jika solusi inti dan orkestrasi Dual-write diinstal di lingkungan. Perilaku ini akan menguntungkan pelanggan yang berencana menggunakan solusi Dual-write untuk mengintegrasikan pesanan penjualan ke dalam aplikasi keuangan dan operasi, tetapi ingin menggunakan Operasi Proyek dalam mode Lite (yaitu, tanpa integrasi ke dalam aplikasi keuangan dan operasi).</p> | |

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2316317 | Sistem ini memungkinkan pembuatan faktur yang tidak memiliki transaksi yang dikenakan biaya. |
| Penagihan dan Harga | 2737300 | Validasi ketersediaan bidang Pelanggan sebelum formulir diakses. |
| Penagihan dan Harga | 2744948 | Tambahkan pemeriksaan nol untuk Metode penagihan. |
| Penagihan dan Harga | 2763515 | Kesalahan referensi nol menangani ketika kontrak penjualan faktur hilang. |
| Penagihan dan Harga | 2844301 | Pembuatan faktur batch gagal karena kesalahan. |
| Penagihan dan Harga | 2845869 | Penyimpanan Layanan Organisasi salah. |
| Penagihan dan Harga | 2853729 | Detail Peran dan Harga diperbarui saat Jenis penagihan diubah. |
| Penagihan dan Harga | 2940350 | Ketika aktual diberi harga, hanya daftar harga aktif yang harus dimasukkan secara otomatis. |
| Penyebaran dan Konfigurasi | 3001206 | Entitas replaylogheader msdyn\_ mencegah peningkatan Organisasi Pelanggan. |
| Manajemen peluang | 2755582 | Pengecualian referensi null menangani di Pembantu Aturan Penagihan Terpisah. |
| Manajemen peluang | 2761477 | Saat penagihan terpisah digunakan, penghapusan tonggak (header) meninggalkan tonggak yatim piatu. |
| Manajemen peluang | 2767595 | Saat catatan penggunaan material dibuka dalam formulir utama, sumber daya yang dapat dipesan untuk catatan diubah menjadi pengguna yang saat ini masuk. |
| Perencanaan dan Pelacakan Proyek | 2790384 | Batas waktu Operating Set yang Tertunda terlalu singkat. |
| Manajemen sumber daya | 2751560 | Unit Organisasi Pilihan yang Tidak Konsisten dalam Kebutuhan Sumber Daya. |
| Membuat subkontrak | 2907231 | Tahap proses faktur vendor tidak dapat maju. |
| Waktu dan Pengeluaran | 2867363 | Catatan tidak keluar dari tampilan Absen/Liburan untuk Persetujuan saat mereka mengantre untuk persetujuan. |
| Waktu dan Pengeluaran | 2894405 | TESA: Direktori POC yang tidak digunakan menyebabkan masalah kepatuhan. |

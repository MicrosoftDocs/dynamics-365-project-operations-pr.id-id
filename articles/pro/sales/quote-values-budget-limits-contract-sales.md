---
title: Informasi ringkasan tentang kuotasi proyek - lite
description: Topik ini menyediakan informasi tentang informasi dan pengaturan yang berlaku untuk dan berdampak pada kuotasi proyek. (Sales)
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddc85d8c475dc7cdbe910fad31b5a6d8b617512c8a19cbae9543cb7a3e1d409e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989645"
---
# <a name="header-details-for-project-quotes"></a>Rincian header untuk kuotasi proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Artikel ini menjelaskan informasi yang berlaku untuk kuotasi proyek. Ini mencakup pengaturan yang mempengaruhi semua kuotasi baris, dan informasi tentang kuotasi yang diringkas di seluruh item baris untuk mendorong KPI kuotasi proyek.

Tabel berikut berisi daftar bidang informasi ringkasan pada kuotasi proyek yang unik untuk Dynamics 365 Project Operations atau memiliki beberapa perubahan penting dalam perilaku dari kuotasi Dynamics 365 Sales.

| **Bidang** | **Lokasi** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- | --- |
| Tipe | Tab ringkasan (tersembunyi) | Bidang rangkaian pilihan ini memiliki pilihan berikut:</br>- berbasis Pekerjaan (tersedia hanya bila Project Operations diinstal)</br>- berbasis item (tersedia hanya bila Project Operations dan Sales diinstal)</br>- Berbasis pemeliharaan layanan (tersedia saat Dynamics 365 Field Service diinstal) | Bila Anda menggunakan aplikasi Project Operations, nilai bidang ini secara otomatis diatur ke **berbasis pekerjaan**. Ini mengklasifikasikan kuotasi sebagai kuotasi berbasis proyek. Kuotasi harus berbasis proyek untuk memungkinkan semua ekstensi dan fungsi khusus proyek. |
| Calon Pelanggan | tab Ringkasan | Merujuk pada perusahaan atau rekaman akun pelanggan. Ketika kuotasi dibuat dari peluang, bidang ini disalin dari bidang yang sesuai pada peluang. | Mata uang pada kuotasi proyek dibatalkan berdasarkan mata uang pelanggan. Namu, hal ini tidak dapat diubah sebelum kuotasi disimpan. |
| Manajer Akun | tab Ringkasan | Nama Manajer akun untuk penawaran ini. Ketika kuotasi dibuat dari peluang, bidang ini disalin dari bidang yang sesuai pada peluang. | Manajer akun bertanggung jawab untuk mengelola hubungan dengan pelanggan melalui penyelesaian proyek ini. Berdasarkan rekaman sumber daya yang dapat dipesan terkait dengan manajer akun, unit kontrak ter-default pada kuotasi proyek. |
| Unit Kontrak | tab Ringkasan | Unit organisasi yang bertanggung jawab atas pelaksanaan proyek atau proyek-proyek yang terkait dengan kuotasi ini. Ketika kuotasi dibuat dari peluang, bidang ini disalin dari bidang yang sesuai pada peluang. | Unit kontrak adalah divisi perusahaan yang akan melaksanakan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang, dan mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang timbul selama eksekusi proyek. |
| Daftar Harga Produk | tab Ringkasan | Ini adalah daftar harga yang digunakan untuk harga default pada baris kuotasi berdasarkan produk. Daftar pilihan untuk bidang ini menampilkan daftar daftar harga dengan mata uang daftar harga yang sesuai dengan mata uang pada kuotasi. Ketika kuotasi dibuat dari peluang, bidang ini disalin dari bidang yang sesuai pada peluang. Bidang pada peluang ini diatur default dari rekaman akun namun dapat diubah. | Jika kuotasi dimenangkan, nilai bidang ini disalin ke kontrak proyek yang dibuat. |
| Mata uang | tab Ringkasan | Ini menunjukkan mata uang yang akan digunakan untuk melaporkan nilai penawaran ini. Ini juga merupakan mata uang penagihan pelanggan jika penawaran dimenangkan. Ketika kuotasi dibuat dari peluang, bidang ini disalin dari bidang yang sesuai pada peluang. Bidang pada peluang ini diatur default dari rekaman akun namun dapat diubah oleh pengguna. | Setelah kuotasi disimpan, bidang ini tidak lagi dapat diedit. Ini digunakan untuk men-default daftar harga proyek dan produk di kuotasi. Mata uang pada kuotasi digunakan untuk disesuaikan dengan mata uang pada daftar harga. |
| Batas Jangan terlampaui | tab Ringkasan | Ini menunjukkan batas negosiasi tentang nilai akhir yang disepakati pelanggan untuk penawaran ini. | Batas ini dievaluasi selama eksekusi dan berlaku di semua item baris dan proyek yang terkait dengan transaksi ini. |
| Tanggal Pengiriman yang Diminta | tab Ringkasan | Ketika kuotasi dibuat dari peluang, bidang ini disalin dari bidang yang sesuai pada peluang. | Tanggal ini digunakan sebagai tanggal akhir untuk membuat jadwal faktur. |

Di bawah ini adalah tab dan KPI yang tersedia pada kuotasi proyek yang unik untuk Project Operations atau memiliki beberapa perubahan penting dalam perilaku dari kuotasi Sales:

| **Bidang** | **Lokasi** | **Keterangan** |
| --- | --- | --- |
| Analisis Profitabilitas | Tab pada kuotasi | tab ini menunjukkan metrik berikut:</br>- Total Biaya yang dapat ditagih</br></br>- Total Biaya yang Tidak dapat ditagih</br>- Pendapatan Total</br>- Pendapatan Total (Dasar)</br>- margin kotor</br>- Penyesuaian Margin Kotor|
| Perbandingan Dengan Harapan Pelanggan | Tab pada kuotasi | Tab ini menunjukkan metrik berikut:</br>- Perkiraan Penyelesaian</br>- Penyelesaian yang Diminta</br>- Anggaran Pelanggan</br>- Nilai Kuotasi |
| Analisis Kuotasi | Tab pada kuotasi | Tab ini meringkas KPI teratas berikut untuk kuotasi proyek</br>- Perbandingan dengan ekspektasi pelanggan untuk anggaran dan jadwal</br>- margin kotor</br>- Penyesuaian Margin Kotor |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

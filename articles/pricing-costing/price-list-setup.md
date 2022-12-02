---
title: Mengonfigurasikan daftar harga
description: Artikel ini menyediakan informasi tentang cara mengonfigurasikan biaya dan daftar harga penjualan.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8a6d96f4a5a8d97e86bbd00413e21f69255a48c5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917672"
---
# <a name="set-up-price-lists"></a>Mengonfigurasikan daftar harga

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Daftar harga di Dynamics 365 Project Operations menunjukkan katalog tingkat. Tarif menyatakan biaya, penjualan, dan tarif tagihan. Tergantung pada apakah daftar harga mengekspresikan tarif biaya atau penjualan dan tarif tagihan, konteks daftar harga adalah **Penjualan** atau **Biaya**.

Ekstensi berikut ini khusus untuk Project Operations dan diterapkan ke daftar harga dari Dynamics 365 Sales.

- **Konteks**: Bidang ini memiliki nilai, **Biaya**, dan **Penjualan** yang didukung. Nilai, **Pembelian** tidak didukung. Atur konteks ke **Biaya** untuk membuat daftar harga biaya atau atur konteks ke **Penjualan** untuk daftar harga penjualan. Daftar harga biaya menyelesaikan harga untuk jenis biaya pada estimasi dan rekaman aktual. Daftar harga penjualan menyelesaikan harga pada estimasi dan rekaman aktual dari jenis penjualan yang belum ditagih dan ditagih.
- **Unit Waktu**: Ini adalah satuan waktu default yang harganya diatur dalam tabel **Harga Peran** terkait untuk Daftar harga ini.
- **Entitas Daftar Harga**: Bidang tersembunyi ini adalah oleh Project Operations untuk membedakan daftar harga yang spesifik kuotasi atau atau spesifik kontrak dari yang standar dan berlaku secara global.

## <a name="price-list-header"></a>Tajuk Daftar Harga

Tabel berikut ini menyertakan bidang pada tab **Umum** dari daftar harga yang unik untuk Project Operations atau memiliki perubahan perilaku yang signifikan dari daftar harga di Penjualan.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| Nama | Tab **Umum** dan formulir **Buat Cepat** | Identitas daftar harga. | Daftar Harga ditampilkan dengan nilai ini di semua halaman daftar dan pilihan menurun.|
| Konteks | Tab **Umum** dan formulir **Buat Cepat** | Bidang ini tidak dapat diatur ke **Biaya** atau **Penjualan**. | Daftar harga yang diatur ke **biaya** digunakan untuk mencari harga untuk perkiraan biaya dan aktual biaya. Daftar harga yang diatur ke **Penjualan** digunakan untuk mencari harga untuk perkiraan penjualan dan aktual penjualan. Hanya daftar harga yang memiliki konteks yang diatur ke **penjualan** yang dapat dilampirkan ke daftar harga proyek untuk pelanggan, kuotasi proyek, atau kontrak proyek. |
| Tanggal Mulai | Tab **Umum** dan formulir **Buat Cepat** | Tanggal mulai dari periode di mana daftar harga efektif. | Dengan bidang **tanggal berakhir**, bidang ini digunakan untuk menentukan daftar harga yang berlaku untuk estimasi tertentu atau baris aktual. |
| Tanggal Akhir | Tab **Umum** dan formulir **Buat Cepat** | Tanggal akhir dari periode di mana daftar harga efektif. | Dengan bidang **tanggal Mulai**, bidang ini digunakan untuk menentukan daftar harga yang berlaku untuk estimasi tertentu atau baris aktual. |
| Mata uang | Tab **Umum** dan formulir **Buat Cepat** | Bidang ini digunakan untuk default mata uang pada setiap peran, kategori, atau baris item daftar harga yang terkait dengan daftar harga ini. | Pada daftar harga **penjualan**, peran, kategori, atau baris item daftar harga tidak dapat dibuat dalam mata uang apa pun selain mata uang ini. Pada daftar harga **biaya**, Anda dapat membuat garis harga peran dalam mata uang apa pun. Mata uang yang didefinisikan di sini digunakan sebagai default. Pengaturan pengguna yang terkait dengan harga peran dapat menimpa nilai ini untuk memungkinkan pengaturan tarif biaya tenaga kerja dalam mata uang apa pun. Tarif biaya kategori dan biaya item daftar harga hanya dapat diatur dalam mata uang yang ditentukan di sini. |
| Satuan Waktu | Tab **Umum** dan formulir **Buat Cepat** | Bidang ini digunakan untuk default unit waktu pada setiap baris peran yang terkait dengan daftar harga ini. | Nilai bidang ini hanya digunakan pada pengaturan harga peran terkait. Pada daftar harga **biaya** dan **Penjualan**, Anda dapat membuat garis harga peran dalam unit waktu apa pun. Unit waktu yang didefinisikan di sini digunakan sebagai default. Pengaturan pengguna yang terkait dengan harga peran dapat menimpa nilai ini untuk memungkinkan pengaturan tarif tagihan dan biaya tenaga kerja dalam unit waktu apa pun. |
| KETERANGAN | Tab **Umum** dan formulir **Buat Cepat** | Bidang teks ini memungkinkan Anda memberikan deskripsi multi-baris dari daftar harga. | Bidang ini diperlihatkan dalam tampilan **Terkait** pada daftar harga di berbagai entitas yang memiliki daftar harga terkait. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
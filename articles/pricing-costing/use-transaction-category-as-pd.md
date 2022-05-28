---
title: Menggunakan Kategori Transaksi sebagai dimensi harga
description: Topik ini berisi informasi tentang cara menggunakan bidang Kategori Transaksi sebagai dimensi harga.
author: rumant
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a7fe9bfc87db992252f8ef3f0f688e7426cafebb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591132"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a>Menggunakan Kategori Transaksi sebagai dimensi harga


_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Topik ini menjelaskan cara menggunakan bidang **Kategori Transaksi** sebagai dimensi harga. 

## <a name="prerequisites"></a>Prasyarat
Sebelum menyelesaikan prosedur di topik ini, Anda harus memiliki solusi dimensi harga baru untuk organisasi Anda. Jika Anda belum membuatnya, lihat [Membuat bidang dan entitas kustom sebagai dimensi harga](create-custom-fields-entities-pricing-dimensions.md).

## <a name="add-the-transaction-category-field-to-forms-and-views"></a>Menambahkan bidang Kategori Transaksi ke formulir dan tampilan
Agar bidang **Kategori Transaksi** terlihat di solusi dimensi harga, Anda harus menambahkan bidang ke semua formulir dan tampilan sebagai entitas.

Tabel berikut mencantumkan semua formulir dan tampilan siap pakai, berdasarkan entitas. Anda juga harus menambahkan bidang baru pada formulir atau tampilan tambahan di entitas yang disesuaikan.

|  Entity        | Formlir     |Tampilan        |
| ------------------------------|---------------------------------|----------------------------------|
|  Harga Peran| Informasi |- Harga Kategori Sumber Daya Aktif<br> - Terkait Harga Kategori Sumber Daya |
|  Markup Harga Peran| Informasi|- Markup Harga Peran Aktif<br>- Terkait Markup Harga Peran |
|  Rincian Baris Kuotasi|- Informasi Proyek<br>- Pembuatan Cepat Proyek| - Rincian Baris Kuotasi Aktif<br>- Gabungan Rincian Baris Kuotasi<br>- Terkait Rincian Baris Kuotasi |
|  Rincian Baris Kontrak Proyek|- Informasi Proyek<br>- Pembuatan Cepat Proyek|- Rincian Baris Kontrak Gabungan<br>- Rincian Baris Kontrak Aktif<br>- Terkait Rincian Baris Kontrak |
|  Tugas Proyek|- Informasi<br>- Formulir Baru| &nbsp; |
|  Anggota Tim Proyek|- Informasi<br>- Formulir Baru|- Anggota Tim Proyek Aktif<br>- Anggota Tim Proyek<br>- Terkait Anggota Tim Proyek |
|  Entri Waktu|- Informasi<br>- Buat Entri Waktu|- Entri Waktu Saya Menurut Tanggal<br>- Entri Waktu Saya untuk Pekan Ini<br>- Entri Waktu untuk Persetujuan|
|  Lini Jurnal|- Informasi<br>- Buat Cepat|- Lini Jurnal Aktif<br>- Terkait Lini Jurnal|
|  Rincian Baris Faktur|- Informasi<br>- Buat Cepat|- Rincian Baris Faktur Aktif<br>- Transaksi Faktur Kena Biaya<br>- Transaksi Faktur Gratis<br>- Terkait Rincian Baris Faktur <br>- Transaksi Faktur Tidak Kena Biaya|
|  Aktual|- Informasi<br>- Aktual Aktif| Aktual Terkait |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a>Mengonfigurasikan bidang Kategori Transaksi sebagai dimensi harga

1. Buka **Pengaturan** > **Parameter**. 
2. Pada halaman **Parameter**, di tab **Dimensi Harga Berbasis Jumlah**, pastikan kisi menampilkan record di entitas **Dimensi Harga**.
3. Tambahkan **Kategori Transaksi** ke daftar ini dan atur bidang **Berlaku untuk Biaya** dan **Berlaku untuk Penjualan** ke **Ya**.
4. Di bidang **Jenis Dimensi**, pilih **Berbasis jumlah**, lalu pilih prioritas untuk **Kategori Transaksi** yang terkait dengan biaya dan penjualan.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
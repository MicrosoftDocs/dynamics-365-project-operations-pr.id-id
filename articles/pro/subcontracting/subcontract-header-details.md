---
title: Rincian header untuk subkontrak
description: Topik ini menjelaskan fungsi yang diberikan pada header subkontrak dalam Project Operations.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 49158af1a430033db3a5db57a840512c45bc17e2
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323645"
---
# <a name="header-details-for-subcontracts"></a>Rincian header untuk subkontrak

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Topik ini menjelaskan fungsi yang diberikan pada header subkontrak dalam Dynamics 365 Project Operations.

Saat Manajer Proyek merencanakan dan mengeksekusi proyek, mereka mungkin mempekerjakan subkontraktor dan membeli produk maupun layanan dari vendor. Bila Manajer Proyek harus membeli produk atau layanan, mereka dapat membuat subkontrak dalam Project Operations.

Untuk membuat subkontrak, selesaikan langkah-langkah berikut.

1. Di panel navigasi, pilih **Subkontrak**, dan pada halaman **Subkontrak**, pilih **Baru**.
2. Masukkan informasi yang diperlukan dan kemudian pilih **Simpan**.

    Tabel berikut memberikan informasi tentang bidang pada halaman header Subkontrak.

    | **Bidang** | **Deskripsi** |
    | --- | --- | 
    | Nama | Nama Subkontrak. |
    | KETERANGAN | Deskripsi singkat tentang layanan dan produk yang dibeli pada subkontrak. |
    | Vendor | Nama perusahaan tempat membeli produk dan layanan. Rekaman Akun ini memiliki jenis relasi **Vendor** atau **Pemasok**. |
    | Tanggal Subkontrak | Tanggal subkontrak dibuat. |
    | Alasan Status | Status Subkontrak. |
    | Mata uang | Mata uang untuk pembelian produk dan layanan. Nilai pada bidang ini default dari akun vendor tetapi dapat diubah. Daftar harga proyek yang digunakan untuk menentukan harga produk dan layanan pada subkontrak harus dalam mata uang ini. Daftar harga dalam mata uang lain tidak dapat dikaitkan ke subkontrak. Biaya produk dan layanan yang dibebankan pada subkontrak ini akan dicatat pada proyek dalam mata uang ini. |
    | Unit Kontrak | Divisi perusahaan yang menandatangani kontrak pembelian atau subkontrak dengan vendor. |
    | Syarat Pembayaran | Persyaratan pembayaran pada faktur vendor yang dikeluarkan pada subkontrak ini. Nilai pada bidang ini default dari rekaman akun vendor. |
    | Alamat Pembayaran | Alamat pengiriman pembayaran pada faktur vendor. Nilai pada bidang ini default dari rekaman akun vendor. |
    | Nama Penagihan | Nama orang atau divisi di perusahaan vendor yang akan mengirim faktur. Nilai pada bidang ini default dari rekaman akun vendor dan akan digunakan sebagai nama kontak utama pada faktur vendor yang dibuat untuk subkontrak ini. |
    | Alamat Penagihan | Alamat yang digunakan pada faktur dari vendor ini. Nilai pada bidang ini default dari rekaman akun vendor. Alamat ini juga digunakan sebagai faktur dari alamat pada faktur vendor yang dibuat untuk subkontrak ini. |
    | Subtotal | Jika subkontrak tidak memiliki baris, masukkan nilai pada bidang ini yang menunjukkan subtotal pesanan sebelum pajak. Jika subkontrak memiliki baris, bidang ini hanya dapat dibaca. Jumlah yang ditampilkan adalah jumlah subtotal dari semua baris pada subkontrak. |
    | Total Pajak | Jika subkontrak tidak memiliki baris, masukkan nilai pada bidang ini yang menunjukkan pajak di subkontrak ini. Jika subkontrak memiliki baris, bidang ini hanya dapat dibaca. Jumlah yang ditampilkan adalah jumlah pajak dari semua baris pada subkontrak. |
    | Jumlah Total |  Data bidang terhitung ini menunjukkan jumlah total subkontrak setelah pajak disertakan.  |
    | Tanggal Dikonfirmasi | Tanggal konfirmasi subkontrak.  |
    | Diminta Oleh | Nilai di bidang ini akan default ke nama pengguna yang membuat subkontrak. Nilai ini dapat diubah oleh pembuat subkontrak untuk menunjukkan orang yang mereka atas namakan dalam membuat subkontrak.  |
    | Manajer Akun Vendor | Nama kontak utama akun vendor. Nilai pada bidang ini default dari rekaman akun vendor. Nilai bidang ini dapat diubah oleh pengguna untuk memilih kontak yang berbeda sebagai manajer akun vendor subkontrak. Email pemberitahuan dan negosiasi harga dapat dikonfigurasi dan dikirim oleh kontak ini. |



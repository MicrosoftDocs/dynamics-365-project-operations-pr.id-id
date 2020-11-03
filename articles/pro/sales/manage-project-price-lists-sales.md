---
title: Mengelola daftar harga proyek pada kuotasi proyek
description: Topik ini menyediakan informasi tentang menangani daftar harga proyek di kuotasi. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4013d2e8cc0d2329f824a17484ee6f4a054a390e
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078407"
---
# <a name="manage-project-price-lists-on-project-quotes-sales"></a>Mengelola daftar harga proyek pada kuotasi proyek (Sales)

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Kuotasi proyek dirancang untuk mendukung beberapa daftar harga penjualan efektif tanggal. Dengan Dynamics 365 Project Operations, entitas baru yang terkait dan disebut **Daftar harga proyek** ditambahkan. Entitas ini memiliki relasi 1 ke banyak untuk kuotasi proyek.

Daftar harga proyek digunakan untuk transaksi waktu harga dan pengeluaran pada suatu proyek. Bila kuotasi memiliki satu atau beberapa daftar harga proyek, daftar harga ini digunakan untuk estimasi waktu harga dan pengeluaran dan aktual pada proyek yang terkait dengan kuotasi melalui baris kuotasi.

Bila tidak ada daftar harga proyek pada kuotasi proyek, Anda akan menerima pesan peringatan. Pesan menyatakan bahwa karena tidak ada daftar harga proyek, perkiraan dan pekerjaan proyek dan pengeluaran Anda tidak akan dihargai. Namun, mereka akan memiliki harga nol (0) untuk nilai penjualan.

## <a name="associate-or-disassociate-a-project-price-list-on-a-project-quote"></a>Mengaitkan atau memisahkan daftar harga proyek pada kuotasi proyek

Untuk membuat atau memilih daftar harga tertentu untuk memperkirakan pekerjaan dan biaya berdasarkan proyek, selesaikan langkah-langkah berikut.

1. Pada kuotasi, pilih tab **harga proyek** dan di subkisi, pilih **+ Tambah daftar harga proyek baru**.
2. Pada halaman Buat cepat, pilih daftar harga. Daftar drop-down menampilkan semua daftar harga yang memiliki konteks yang diatur ke **penjualan** dan mata uang sesuai dengan mata uang pada kuotasi.
4. Masukkan Deskripsi untuk Asosiasi daftar harga proyek dan pilih **Simpan dan tutup**.

Asosiasi Daftar Harga Proyek dibuat.

Anda dapat mengulangi proses ini jika Anda perlu mengaitkan lebih dari satu daftar harga proyek ke kuotasi proyek. Cukup buat beberapa daftar harga proyek jika Anda memiliki tanggal efektif yang berbeda pada masing-masing daftar harga proyek terkait.

> [!NOTE]
> Project Operations tidak mendukung efektivitas tanggal tumpang tindih dari daftar harga proyek. Jika ada beberapa daftar harga proyek untuk transaksi dengan tanggal yang ditentukan, harga pada transaksi akan dibatalkan ke nol (0).
Untuk menghapus Asosiasi daftar harga proyek, pilih daftar harga proyek, lalu pilih **Hapus daftar harga proyek kuotasi**. Daftar harga akan dihapus dari daftar harga proyek kuotasi, namun daftar harga itu sendiri tidak dihapus. Hanya Asosiasi ke kuotasi yang akan dihapus.

## <a name="set-up-default-project-price-lists-on-a-quote"></a>Mengkonfigurasi daftar harga proyek default pada kuotasi

Daftar harga proyek dapat diatur ke default pada kuotasi proyek. Konfigurasi ini memastikan bahwa semua kuotasi di organisasi Anda selalu diawali dengan daftar harga standar untuk periode harga tersebut.

### <a name="set-up-organizational-default-for-project-price-lists"></a>Mengkonfigurasi default organisasi untuk daftar harga proyek

1. Buka **pengaturan** > **umum** > **parameter**.
2. Pada halaman daftar **parameter aktif** , Cari rekaman dan klik dua kali untuk membukanya. 
3. Pada halaman **parameter** , pilih tab **daftar harga**. Anda dapat melihat daftar harga default ditampilkan. Daftar ini adalah daftar harga biaya dan penjualan standar. Memiliki daftar harga penjualan yang terkait di sini untuk setiap mata uang penjualan akan memastikan bahwa daftar harga penjualan memiliki default pada setiap kuotasi yang Anda buat untuk pelanggan yang bertransaksi dalam mata uang ini.

### <a name="set-up-customer-specific-project-price-lists"></a>Mengkonfigurasi daftar harga proyek khusus pelanggan

Daftar harga proyek khusus pelanggan juga dapat diatur saat Anda menegosiasikan perjanjian harga induk dengan pelanggan Anda.

Untuk membuat daftar harga proyek khusus pelanggan, selesaikan langkah berikut.

1. Di area **penjualan** , pilih **pelanggan**.
2. Di daftar akun aktif, pilih dan buka rekaman Pelanggan yang memiliki daftar harga khusus.
3. Pada tab **daftar harga proyek** , Anda dapat membuat Asosiasi daftar harga baru agar memiliki daftar harga proyek yang spesifik untuk pelanggan ini.

## <a name="create-custom-pricing-on-a-project-quote"></a>Membuat harga kustom pada kuotasi proyek

Setelah Anda memiliki daftar harga proyek default organisasi dan pelanggan spesifik, kuotasi proyek Anda akan secara otomatis dibuat dengan Asosiasi daftar harga proyek ini. Namun, dalam kasus tertentu, Anda mungkin perlu membuat harga kustom untuk kuotasi proyek tertentu. 

1. Pada **kuotasi proyek** , pada tab **daftar harga proyek** , Verifikasikan di subkisi bahwa tidak ada rekaman daftar harga tertentu yang dipilih.
2. Pilih **Buat Harga Kustom**. Ini akan membuat salinan semua daftar harga standar yang saat ini terkait dengan kuotasi dan mengaitkan salinan ini ke kuotasi. Asosiasi yang ada pada daftar harga standar akan dihapus. Staf penjualan kemudian dapat mulai membuat pengeditan pada harga pada salinan ini. Harga yang telah diubah ini akan berlaku hanya untuk kuotasi Proyek ini.

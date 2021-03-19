---
title: Mengelola daftar harga proyek pada kontrak proyek
description: Topik ini menyediakan informasi tentang mengelola daftar harga proyek pada kontrak proyek.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278602"
---
# <a name="manage-project-price-lists-on-project-contracts"></a>Mengelola daftar harga proyek pada kontrak proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kontrak proyek di Dynamics 365 Project Operations dirancang untuk mendukung beberapa daftar harga penjualan efektif tanggal pada kontrak. Dalam Project Operations, ada entitas baru yang terkait disebut **Daftar harga proyek**. Entitas ini memiliki relasi satu ke banyak dengan kontrak proyek.

Daftar harga proyek digunakan untuk transaksi waktu harga dan pengeluaran pada suatu proyek. Bila kontrak memiliki satu atau beberapa daftar harga proyek, daftar harga ini digunakan untuk harga untuk perkiraan waktu dan biaya dan aktual pada proyek yang terkait dengan kontrak melalui baris kontrak.

Bila tidak ada daftar harga proyek pada kontrak proyek, Anda akan melihat pesan peringatan bahwa tidak ada daftar harga proyek dan estimasi, pekerjaan proyek yang sebenarnya, dan pengeluaran Anda tidak akan diberi harga. Tidak akan ada harga untuk nilai penjualan.

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a>Mengaitkan atau membatalkan kaitan daftar harga proyek pada kontrak proyek

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a>Membuat atau mengaitkan daftar harga tertentu untuk memperkirakan pekerjaan dan pengeluaran berbasis proyek

1. Pada kontrak proyek, pilih tab **daftar harga proyek**.
2. Di subkisi, pilih **+ Tambah daftar harga proyek baru**.
3. Di slider **buat cepat**, pilih daftar harga. 

  Daftar drop-down menampilkan semua daftar harga yang memiliki konteks yang diatur ke **penjualan**, dengan mata uang pada daftar harga sesuai dengan mata uang pada kontrak.
  
4. Masukkan Deskripsi untuk Asosiasi daftar harga proyek, pilih **Simpan**, lalu tutup penggeser **buat cepat**.

   Asosiasi Daftar Harga Proyek dibuat.
   
5. Ulangi langkah 1-4 untuk mengaitkan lebih dari satu daftar harga proyek ke kontrak proyek. Cukup buat beberapa daftar harga proyek jika Anda memiliki efektivitas tanggal yang berbeda pada setiap daftar harga proyek terkait.

> [!NOTE]
> Project Operations tidak mendukung tumpang tindih efektivitas tanggal daftar harga proyek. Jika ada beberapa daftar harga proyek untuk transaksi dengan tanggal tertentu, harga pada transaksi tersebut akan default ke nol.

### <a name="remove-a-project-price-list-association"></a>Hapus asosiasi daftar harga proyek

- Pilih daftar harga proyek, lalu pilih **Hapus daftar harga proyek kontrak** pada subkisi. 

  Daftar harga akan dihapus dari daftar harga proyek pada kontrak. Daftar harga itu sendiri tidak akan dihapus. Hanya Asosiasi ke kontrak yang akan dihapus.

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a>Mengkonfigurasi default otomatis daftar harga proyek pada kontrak

Daftar harga proyek dapat diatur sebagai daftar default pada kontrak proyek. Konfigurasi ini dapat membantu memastikan bahwa semua kontrak di organisasi Anda selalu diawali dengan daftar harga standar untuk periode harga tersebut.

### <a name="set-up-the-organizational-default-for-project-price-lists"></a>Mengkonfigurasi default organisasi untuk daftar harga proyek

1. Buka **Pengaturan** > **Umum** lalu pilih **Parameter**.
2. Di halaman daftar **parameter aktif**, pilih dan klik dua kali rekaman untuk membukanya. Sementara mengklik gand, pastikan bahwa Anda tidak mengklik nilai bidang yang merupakan hyperlink. 
3. Pada halaman **parameter aktif**, pilih tab **daftar harga**. Subkisi menampilkan daftar daftar harga default. Daftar ini adalah daftar harga standar dan daftar harga penjualan. Memiliki Daftar harga **penjualan** yang terkait di sini untuk setiap mata uang yang Anda Jual memastikan bahwa daftar harga penjualan adalah default pada kontrak apa pun yang Anda buat untuk pelanggan yang bertransaksi dalam mata uang ini.

### <a name="set-up-a-customer-specific-project-price-list"></a>Mengkonfigurasi daftar harga proyek khusus pelanggan

Anda juga dapat mengkonfigurasi daftar harga proyek tertentu pelanggan saat Anda menegosiasikan perjanjian harga induk dengan pelanggan Anda.

1. Buka **Penjualan** > **Pelanggan**.
2. Dari daftar akun aktif, pilih Pelanggan yang memiliki daftar harga khusus.
3. Pilih rekaman pelanggan untuk membukanya, lalu pilih tab **daftar harga proyek**. Subkisi menampilkan daftar daftar harga proyek yang spesifik untuk pelanggan ini. 
4. Buat Asosiasi daftar harga baru di sini untuk memiliki daftar harga proyek khusus untuk pelanggan ini.

## <a name="custom-pricing-on-a-project-contract"></a>Harga kustom pada kontrak proyek

Setelah Anda memiliki daftar harga proyek default organisasi dan spesifik pelanggan, kontrak proyek Anda akan dibuat dengan Asosiasi daftar harga proyek ini secara otomatis. Namun, daftar harga proyek pada kontrak proyek selalu disalin dengan nama tanggal dan kontrak yang ditambahkan. Manajer akun dan proyek kemudian dapat mulai membuat pengeditan pada harga pada salinan ini. Harga yang telah diubah ini akan berlaku hanya untuk kontrak proyek ini.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Estimasi keuangan untuk bahan pada proyek
description: Laporan topik memberikan informasi tentang mendefinisikan atau memperkirakan bahan berbasis proyek.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 768da6adb83b4593a227f60182179b3036f4c040
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002690"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Estimasi keuangan untuk bahan pada proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations memungkinkan manajer proyek menentukan biaya bahan berbasis proyek untuk setiap proyek atau tugas. Setiap estimasi bahan dapat dikaitkan dengan tugas proyek tertentu. Pengeluaran dikategorikan ke dalam berbagai kategori pengeluaran, yang ditentukan pada tingkat organisasional. Harga dan biaya untuk setiap kategori pengeluaran ditentukan dalam daftar harga. 

Lengkapi langkah-langkah berikut untuk melihat, menambah, atau menghapus estimasi bahan proyek.

1. Buka **Proyek**, lalu pilih proyek yang akan diperbarui.
2. Pada tab **Estimasi Bahan**, lihat daftar estimasi bahan proyek.
3. Pilih **Estimasi Bahan Baru** untuk membuat perkiraan bahan baru. Atau, pilih estimasi bahan untuk dihapus, lalu pilih **Hapus Perkiraan Bahan**.

Tabel berikut memberikan informasi tentang bidang pada **baris estimasi bahan** di Proyek. 

| **Bidang** | **Deskripsi** | **Dampak hilir** |
| --- | --- | --- |
| Tugas | Semua tugas dalam proyek. Ini mencakup tugas node leaf dan ringkasan. | Bila Anda memilih tugas untuk baris estimasi bahan, perkiraan biaya bahandan perkiraan penjualan bahan untuk tugas akan terpengaruh. Jika bidang ini kosong, perkiraan bahan dilacak dan diringkas hanya pada tingkat proyek. |
| Pilih Produk |  Anda dapat menentukan apakah baris estimasi ini adalah untuk produk yang Ada (katalog) atau produk pilihan. | Bidang ini menentukan apakah Anda memilih produk dari katalog atau produk pilihan. |
| Produk | ID produk dari katalog produk. Bila Anda memilih ID produk, nilai di bidang **Pilih Produk** akan secara otomatis diperbarui ke **produk yang ada**. ID tersebut digunakan untuk mengambil harga biaya dan penjualan dari daftar harga. | Tidak ada dampak hilir untuk bidang ini. |
| Deskripsi Produk Pilihan | Bidang teks untuk menulis nama produk. Bidang harus digunakan jika **Pilihan** dipilih dalam bidang **pilih Produk**.| Tidak ada dampak hilir untuk bidang ini. |
| Tanggal mulai | Tanggal perkiraan untuk digunakannya bahan. | Tidak ada dampak hilir untuk bidang ini. |
| Grup Unit | Nilai default pada bidang ini berasal dari grup unit default pada produk katalog. Anda dapat memperbarui bidang ini untuk memilih grup unit lain. | Tidak ada dampak hilir untuk bidang ini. |
| Unit | Nilai di bidang ini akan berasal dari unit default dari produk yang dipilih. Anda dapat memperbarui bidang ini untuk memilih unit lain. | Mengubah unit menghasilkan biaya dan harga per unit default yang berbeda. |
| Quantity | Estimasi kuantitas produk yang akan digunakan pada proyek. | Tidak ada dampak hilir untuk bidang ini. |
| Biaya Unit | Biaya per unit dari kombinasi produk dan unit yang dipilih sebagaimana diatur dalam daftar harga biaya yang berlaku. | Biaya unit selalu ditampilkan dalam mata uang biaya proyek. Jika tidak ada konfigurasi biaya per unit untuk kombinasi produk dan konfigurasi unit dalam daftar harga, maka biaya unit akan diatur default ke 0,00. |
| Harga Unit | Harga produk dan kombinasi unit yang dipilih sebagaimana diatur dalam daftar harga penjualan yang berlaku. | Harga per unit selalu ditampilkan dalam mata uang penjualan proyek. Jika tidak ada konfigurasi harga per unit untuk kombinasi produk dan konfigurasi unit dalam daftar harga, maka harga per unit akan diatur default ke 0,00.|
| Biaya Total | Jumlah biaya yang dihitung sebagai kuantitas \* biaya per unit.| Jumlah Biaya selalu ditampilkan dalam mata uang biaya proyek. |
| Penjualan Total | Jumlah penjualan yang dihitung sebagai kuantitas \* harga per unit. | Jumlah penjualan selalu ditampilkan dalam mata uang penjualan proyek. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]

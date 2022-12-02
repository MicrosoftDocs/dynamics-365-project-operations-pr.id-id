---
title: Menentukan tarif biaya pada estimasi dan aktual proyek
description: Artikel ini memberikan informasi tentang bagaimana tarif biaya untuk estimasi berbasis proyek dan aktual ditentukan.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475235"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Menentukan tarif biaya pada estimasi dan aktual proyek

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Untuk menentukan tarif biaya pada perkiraan dan aktual di Microsoft Dynamics 365 Project Operations, sistem terlebih dahulu menggunakan tanggal dan mata uang dalam perkiraan atau konteks aktual yang masuk untuk menentukan daftar harga penjualan. Dalam konteks aktual secara khusus, sistem menggunakan bidang **tanggal Transaksi** untuk menentukan daftar harga yang berlaku. Nilai **tanggal transaksi** dari perkiraan masuk atau aktual dibandingkan dengan **nilai Mulai Efektif (independen zona waktu)** dan **Berakhir Efektif (independen zona waktu)** pada daftar harga. Setelah daftar harga biaya ditentukan, aplikasi menentukan tarif biaya. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Menentukan tarif biaya dalam konteks estimasi dan konteks aktual untuk Waktu

Konteks perkiraan untuk **Waktu** mengacu pada:

- Detail baris kuotasi untuk **waktu**.
- Detail baris kontrak untuk **waktu**.
- penugasan sumber daya pada proyek.

Konteks aktual untuk **Waktu** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Waktu**.
- Baris jurnal yang dibuat saat entri waktu diajukan.

Setelah daftar harga biaya untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif biaya default.

1. Sistem mencocokkan kombinasi bidang **Peran** dan **Unit Sumber Daya**, dan Unit Sumber Daya dalam konteks estimasi atau aktual untuk **Waktu** terhadap baris harga peran pada daftar harga. Kecocokan ini mengasumsikan bahwa Anda menggunakan dimensi harga standar untuk biaya tenaga kerja. Jika Anda telah mengonfigurasi sistem untuk mencocokkan bidang selain atau selain **Peran** dan **Unit Sumber Daya**, kombinasi berbeda akan digunakan untuk mengambil baris harga peran yang cocok.
1. Jika sistem menemukan baris harga peran yang memiliki tarif biaya untuk kombinasi **Peran** dan **Unit Sumber Daya**, tarif biaya tersebut digunakan sebagai tarif biaya default.
1. Jika sistem tidak dapat mencocokkan nilai **Peran** dan **Unit Sumber Daya**, sistem akan mengambil baris harga peran yang memiliki nilai yang cocok untuk bidang **Peraan** tetapi nilai null **Unit Sumber Daya**. Setelah sistem sudah menemukan rekaman harga peran yang cocok, tarif biaya dari rekaman tersebut kan digunakan sebagai tarif biaya default.

> [!NOTE]
> Jika Anda mengonfigurasi prioritas bidang **Peran** dan **Unit Sumber Daya** yang berbeda, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku sebelumnya ini akan berubah sesuai dengan itu. Sistem mengambil rekaman harga peran yang memiliki nilai yang sesuai dengan setiap nilai dimensi harga dalam urutan prioritas. Baris yang memiliki nilai null untuk dimensi tersebut akan terlihat terakhir.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan tarif biaya pada baris estimasi dan aktual untuk Pengeluaran

Konteks perkiraan untuk **pengeluaran** mengacu pada:

- Detail baris kuotasi untuk **pengeluaran**.
- Detail baris kontrak untuk **pengeluaran**.
- Estimasi pengeluaran pada proyek

Konteks aktual untuk **pengeluaran** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **pengeluaran**.
- Baris jurnal yang dibuat saat entri pengeluaran diajukan.

Setelah daftar harga biaya untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif biaya default.

1. Sistem mencocokkan kombinasi bidang **Kategori** dan **Unit** dalam konteks estimasi atau konteks aktual untuk **Pengeluaran** tehadap baris harga kategori pada daftar harga.
1. Jika sistem menemukan garis harga kategori yang memiliki tarif biaya untuk kombinasi bidang **Kategori** dan **Unit**, tarif biaya tersebut digunakan sebagai tarif biaya default.
1. Jika sistem tidak dapat mencocokkan nilai **Kategori** lan **Unit**, harga ditetapkan ke **0** (nol) secara default.
1. Dalan konteks estimasi, jika sistem bisa menemukan kategori yang sesuai dengan baris harga, tetapi metode penentuan harga bukan **Harga per Unit**, tarif biaya diatur k **0** (nol) secara default.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan tingkat biaya pada baris aktual dan estimasi untuk Bahan

Konteks perkiraan untuk **Bahan** mengacu pada:

- Detail baris kuotasi untuk **Bahan**.
- Detail baris kontrak untuk **Bahan**.
- Estimasi bahan proyek.

Konteks aktual untuk **Bahan** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Bahan**.
- Baris jurnal yang dibuat saat log penggunaan bahan diajukan.

Setelah daftar harga biaya untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif biaya default.

1. Sistem menggunakan kombinasi bidang **Produk** dan **Unit** dalam konteks estimasi atau aktual untuk **Bahan** terhadap baris item daftar harga pada daftar harga.
1. Jika sistem menemukan baris item daftar harga yang memiliki tarif biaya untuk kombinasi **Produk** dan **Unit**, tarif biaya digunakan sebagai tarif biaya default.
1. Jika sistem tidak bisa mencocokan nilai **Produk** dan **Unit**, biaya unit diatur ke **0** (nol) sebagai default.
1. Dalan konteks estimasi, jika sistem bisa menemukan baris item daftar harga yang cocok, tetapi metode penentuan harga bukan **Jumlah mata uang**, biaya unit diatur ke **0** secara default. Perilaku ini terjadi karena Project Operations hanya mendukung metode harga **jumlah mata uang** untuk bahan yang digunakan pada proyek.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

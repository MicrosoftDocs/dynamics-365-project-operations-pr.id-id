---
title: Menentukan harga penjualan untuk estimasi dan aktual berbasis proyek
description: Artikel ini memberikan informasi tentang bagaimana harga penjualan untuk estimasi dan aktual berbasis proyek ditentukan.
author: rumant
ms.date: 09/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f0b95c651983230cbf340f2c06089a287b2c8a10
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475373"
---
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Menentukan harga penjualan untuk estimasi dan aktual berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menentukan harga penjualan pada perkiraan dan aktual di Microsoft Dynamics 365 Project Operations, sistem terlebih dahulu menggunakan tanggal dan mata uang dalam perkiraan masuk atau konteks aktual untuk menentukan daftar harga penjualan. Dalam konteks aktual secara khusus, sistem menggunakan bidang **tanggal Transaksi** untuk menentukan daftar harga yang berlaku. Nilai **tanggal transaksi** dari perkiraan masuk atau aktual dibandingkan dengan **nilai Mulai Efektif (independen zona waktu)** dan **Berakhir Efektif (independen zona waktu)** pada daftar harga. Setelah daftar harga penjualan ditentukan, sistem akan menentukan tingkat penjualan atau tagihan.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Menentukan tarif penjualan pada baris aktual dan estimasi untuk Waktu

Konteks perkiraan untuk **Waktu** mengacu pada:

- Detail baris kuotasi untuk **waktu**.
- Detail baris kontrak untuk **waktu**.
- penugasan sumber daya pada proyek.

Konteks aktual untuk **Waktu** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Waktu**.
- Baris jurnal yang dibuat saat entri waktu diajukan.
- Detail baris faktur untuk **waktu**. 

Setelah daftar harga untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif tagihan default.

1. Sistem mencocokkan kombinasi bidang **Peran**, **Perusahaan Sumber Daya**, dan **Unit Sumber Daya** dalam konteks estimasi atau aktual untuk **Waktu** terhadap baris harga peran pada daftar harga. Kecocokan ini mengasumsikan bahwa Anda menggunakan dimensi harga bawaan untuk tingkat tagihan. Jika Anda telah mengonfigurasi harga sehingga didasarkan pada selain atau sebagai tambahan untuk **Peran**, **Perusahaan Sumber Daya**, dan **Unit Sumber Daya**, kombinasi bidang tersebut digunakan untuk mengambil baris harga peran yang cocok.
1. Jika sistem menemukan baris harga peran yang memiliki tarif tagihan untuk kombinasi bidang **Peran**, **Perusahaan Sumber Daya**, dan **Unit Sumber daya**, tarif tagihan tersebut digunakan sebagai tarif tagihan default.

> [!NOTE]
> Jika Anda mengonfigurasi prioritas **Peran**, **Perusahaan Sumber Daya**, dan **Unit Sumber Daya** yang berbeda, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku ini akan berubah sesuai dengan itu. Sistem mengambil rekaman harga peran yang memiliki nilai yang sesuai dengan setiap nilai dimensi harga dalam urutan prioritas. Baris yang memiliki nilai null untuk dimensi tersebut akan terlihat terakhir.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan Menyelesaikan tarif penjualan pada baris aktual dan estimasi untuk pengeluaran

Konteks perkiraan untuk **pengeluaran** mengacu pada:

- Detail baris kuotasi untuk **pengeluaran**.
- Detail baris kontrak untuk **pengeluaran**.
- Baris Estimasi pengeluaran pada proyek

Konteks aktual untuk **pengeluaran** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **pengeluaran**.
- Baris jurnal yang dibuat saat entri pengeluaran diajukan.
- Detail baris faktur untuk **pengeluaran**. 

Setelah daftar harga untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan harga penjualan unit default.

1. Sistem mencocokkan kombinasi bidang **Kategori** dan **Unit** pada baris estimasi untuk **pengeluaran** untuk dicocokkan dengan baris Harga Kategori di daftar harga.
1. Jika sistem menemukan garis harga kategori yang memiliki tarif penjualan untuk kombinasi **Kategori** dan **Unit**, maka tarif penjualan digunakan sebagai tarif penjualan default.
1. Jika sistem menemukan baris harga kategori yang cocok, metode harga dapat digunakan untuk memasukkan default harga penjualan. Tabel berikut menunjukkan perilaku default untuk harga pengeluaran dalam Project Operations.

    | Konteks | Metode Penetapan Harga | Harga default |
    | --- | --- | --- |
    | Perkiraan | Harga Per unit | Berdasarkan baris Harga Kategori. |
    |        | Berdasarkan biaya | 0.00 |
    |        | Markup atas biaya | 0.00 |
    | Aktual | Harga Per unit | Berdasarkan baris Harga Kategori. |
    |        | Berdasarkan biaya | Berdasarkan aktual biaya terkait. |
    |        | Markup atas biaya | Markup diterapkan, sebagaimana didefinisikan oleh baris harga kategori pada tingkat biaya unit dari aktual biaya terkait. |

1. Jika sistem tidak dapat mencocokkan nilai **Kategori** dan **Unit**, tarif penjualan ditetapkan ke **0** (nol) secara default.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan tingkat penjualan pada baris aktual dan estimasi untuk bahan

Konteks perkiraan untuk **Bahan** mengacu pada:

- Detail baris kuotasi untuk **Bahan**.
- Detail baris kontrak untuk **Bahan**.
- Baris Estimasi bahan proyek.

Konteks aktual untuk **Bahan** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Bahan**.
- Baris jurnal yang dibuat saat log penggunaan bahan diajukan.
- Detail baris faktur untuk **Bahan**. 

Setelah daftar harga untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan harga penjualan unit default.

1. Sistem mencocokkan kombinasi bidang **Produk** dan **Unit** pada baris perkiraan untuk **bahan** yang cocok dengan baris item daftar harga pada daftar harga.
1. Jika sistem menemukan baris item daftar harga yang memiliki tingkat penjualan untuk kombinasi bidang **Produk** dan **Unit** dan jika metode harga adalah **Jumlah mata uang**, harga penjualan yang ditentukan pada baris daftar harga akan digunakan. 
1. Jika nilai bidang **Produk** dan **Unit** tidak sesuai, atau jika metode harga merupakan sesuatu selain **jumlah Mata Uang,**. tingkat penjualan diatur ke **0** (nol) secara default. Perilaku ini terjadi karena Project Operations hanya mendukung metode harga **jumlah mata uang** untuk bahan yang digunakan pada proyek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

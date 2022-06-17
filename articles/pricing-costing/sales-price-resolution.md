---
title: Menyelesaikan harga penjualan untuk estimasi dan aktual
description: Artikel ini memberikan informasi tentang cara mengatasi tingkat penjualan untuk perkiraan dan aktual.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ee750b93a5be7be09ed76942c7c235f8c811e8bb
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911830"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Menyelesaikan harga penjualan untuk estimasi dan aktual

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Ketika harga penjualan pada estimasi dan aktual ditangani dalam Dynamics 365 Project Operations, sistem terlebih dulu menggunakan tanggal dan mata uang dari kuotasi proyek terkait atau kontrak untuk menangani daftar harga penjualan. Setelah daftar harga penjualan ditangani, sistem akan menyelesaikan tingkat penjualan atau tagihan.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Menyelesaikan tarif penjualan pada baris aktual dan estimasi untuk Waktu

Dalam Project Operations, baris estimasi untuk waktu digunakan untuk menunjukkan baris kuotasi, dan rincian baris kontrak untuk waktu dan penetapan sumber daya pada proyek.

Setelah daftar harga untuk penjualan teratasi, sistem menyelesaikan langkah-langkah berikut untuk default tingkat tagihan.

1. Sistem menggunakan bidang **Peran**, **Perusahaan Sumber Daya**, dan **Unit Sumber daya** pada baris estimasi untuk waktu, untuk dicocokkan dengan baris harga peran dalam daftar harga yang diselesaikan. Kecocokan ini mengasumsikan bahwa dimensi harga bawaan untuk tingkat tagihan digunakan. Jika Anda telah mengonfigurasi harga berdasarkan bidang lainnya, atau selain **Peran**, **Perusahaan Sumber daya**, dan **Unit sumber daya**, maka kombinasi itulah yang akan digunakan untuk mengambil garis harga peran yang cocok.
2. Jika sistem menemukan baris harga peran yang memiliki tarif tagihan untuk kombinasi bidang **Peran**, **Perusahaan Sumber daya**, dan **Unit Sumber daya**, maka tarif biaya itu menjadi default.
3. Jika sistem tidak dapat mencocokkan nilai bidang **Peran**, **Unit Sumber daya**, dan **Unit Sumber daya** maka aplikasi mengambil baris harga peran dengan peran yang cocok, tetapi nilai null **Unit Sumber Daya**. Setelah sistem menemukan rekaman harga peran yang cocok, maka ia akan men-default nilai tagihan dari rekaman tersebut. Pencocokan ini mengasumsikan konfigurasi Bawaan untuk prioritas relatif **peran** vs **Unit sumber daya** sebagai dimensi harga penjualan.

> [!NOTE]
> Jika Anda mengonfigurasi prioritas **Peran** yang berbeda, **Perusahaan Sumber Daya**, dan **Unit Sumber Daya**, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku ini akan berubah sesuai dengan itu. Sistem mengambil rekaman harga peran dengan nilai yang cocok dengan setiap nilai dimensi harga dalam urutan prioritas dengan baris yang memiliki nilai kosong untuk dimensi tersebut diletakkan di akhir.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Menyelesaikan tarif penjualan pada baris aktual dan estimasi untuk pengeluaran

Dalam Project Operations, baris estimasi untuk pengeluaran digunakan untuk menunjukkan baris kuotasi dan rincian baris kontrak untuk pengeluaran dan baris estimasi pengeluaran pada proyek.

Setelah daftar harga untuk penjualan teratasi, sistem menyelesaikan langkah-langkah berikut untuk default harga penjualan unit .

1. Sistem menggunakan kombinasi bidang **Kategori** dan **Unit** pada baris estimasi untuk pengeluaran untuk dicocokkan dengan baris Harga Kategori di daftar harga yang telah diselesaikan.
2. Jika sistem menemukan garis harga kategori yang memiliki tarif penjualan untuk kombinasi bidang **Kategori** dan **Unit**, maka tarif penjualan adalah default.
3. Jika sistem menemukan baris harga kategori yang cocok, metode harga dapat digunakan untuk default harga penjualan. Tabel berikut di bawah ini menunjukkan perilaku default harga pengeluaran dalam Project Operations.

    | Konteks | Metode Penetapan Harga | Harga yang menjadi default |
    | --- | --- | --- |
    | Perkiraan | Harga per unit | Berdasarkan baris Harga Kategori |
    | &nbsp; | Berdasarkan biaya | 0.00 |
    | &nbsp; | Markup atas biaya | 0.00 |
    | Aktual | Harga per unit | Berdasarkan baris Harga Kategori |
    | &nbsp; | Berdasarkan biaya | Berdasarkan aktual biaya terkait |
    | &nbsp; | Markup atas biaya | Dengan menerapkan markup sebagaimana didefinisikan oleh baris harga kategori pada tingkat biaya unit dari aktual biaya terkait |

4. Jika sistem tidak dapat mencocokkan nilai bidang **kategori** dan **unit**, tarif penjualan default ke nol (0).

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Menangani tingkat penjualan pada baris aktual dan estimasi untuk bahan

Dalam Project Operations, Baris estimasi untuk bahan digunakan untuk menunjukkan detail baris kuotasi dan kontrak untuk bahan dan baris estimasi bahan pada proyek.

Setelah daftar harga untuk penjualan teratasi, sistem menyelesaikan langkah-langkah berikut untuk default harga penjualan unit .

1. Sistem menggunakan kombinasi bidang **Produk** dan **Unit** pada baris perkiraan untuk bahan yang cocok dengan baris item daftar harga pada daftar harga yang ditangani.
2. Jika sistem menemukan baris item daftar harga yang memiliki tingkat penjualan untuk kombinasi bidang **Produk** dan **Unit** dan metode harga adalah **Jumlah mata uang**, harga penjualan yang ditentukan pada baris daftar harga akan digunakan.
3. Jika nilai bidang **Produk** dan **Unit** tidak cocok, tingkat penjualan akan default ke nol.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

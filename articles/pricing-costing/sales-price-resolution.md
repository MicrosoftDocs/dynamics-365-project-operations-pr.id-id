---
title: Menentukan harga penjualan untuk perkiraan dan aktual berbasis proyek
description: Artikel ini memberikan informasi tentang bagaimana harga jual untuk perkiraan dan aktual berbasis proyek ditentukan.
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
#  <a name="determine-sales-prices-for-project-based-estimates-and-actuals"></a>Menentukan harga penjualan untuk perkiraan dan aktual berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menentukan harga penjualan pada perkiraan dan aktual di Microsoft Dynamics 365 Project Operations, sistem pertama-tama menggunakan tanggal dan mata uang dalam perkiraan masuk atau konteks aktual untuk menentukan daftar harga penjualan. Dalam konteks aktual secara khusus, sistem menggunakan **bidang Tanggal** transaksi untuk menentukan daftar harga mana yang berlaku. Nilai **tanggal** Transaksi dari perkiraan masuk atau aktual dibandingkan dengan **nilai Efektif Mulai (Timezone independen)** dan **Akhir Efektif (Timezone independent)** pada daftar harga. Setelah daftar harga penjualan ditentukan, sistem menentukan tingkat penjualan atau tagihan.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Menentukan tingkat penjualan pada garis aktual dan perkiraan untuk Waktu

Konteks perkiraan untuk **Waktu** mengacu pada:

- Kutip detail baris untuk **Waktu**.
- Detail garis kontrak untuk **Waktu**.
- Tugas sumber daya pada proyek.

Konteks aktual untuk **Waktu** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Waktu**.
- Baris jurnal yang dibuat saat entri waktu dikirimkan.
- Detail baris faktur untuk **Waktu**. 

Setelah daftar harga untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif tagihan default.

1. Sistem ini cocok dengan kombinasi **bidang Peran**, **Perusahaan** Sumber Daya, dan **Unit** Sumber Daya dalam perkiraan atau konteks aktual untuk **Waktu** terhadap garis harga peran pada daftar harga. Pencocokan ini mengasumsikan bahwa Anda menggunakan dimensi harga out-of-box untuk tarif tagihan. Jika Anda telah mengonfigurasi harga sehingga didasarkan pada bidang selain atau selain **Peran, Perusahaan** Sumber Daya, **dan** Unit **Sumber Daya, kombinasi bidang tersebut digunakan untuk mengambil garis harga** peran yang cocok.
1. Jika sistem menemukan garis harga peran yang memiliki tingkat tagihan untuk **kombinasi Peran**, **Perusahaan** Sumber Daya, dan **Unit** Sumber Daya, tarif tagihan tersebut digunakan sebagai tarif tagihan default.

> [!NOTE]
> Jika Anda mengonfigurasi prioritas yang berbeda dari **bidang Peran**, **Perusahaan** Sumber Daya, dan **Unit** Sumber Daya, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku sebelumnya akan berubah sesuai dengan itu. Sistem mengambil catatan harga peran yang memiliki nilai yang cocok dengan setiap nilai dimensi harga dalam urutan prioritas. Baris yang memiliki nilai nol untuk dimensi tersebut adalah yang terakhir.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan tingkat penjualan pada jalur aktual dan perkiraan untuk Biaya

Konteks estimasi untuk **Pengeluaran** mengacu pada:

- Kutip detail baris untuk **Biaya**.
- Detail garis kontrak untuk **Biaya**.
- Garis perkiraan biaya pada suatu proyek.

Konteks aktual untuk **Pengeluaran** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Biaya**.
- Baris jurnal yang dibuat saat entri pengeluaran dikirimkan.
- Detail baris faktur untuk **Pengeluaran**. 

Setelah daftar harga untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan harga jual unit default.

1. Sistem ini mencocokkan kombinasi **bidang Kategori** dan **Unit** pada garis perkiraan pengeluaran **terhadap** garis harga kategori pada daftar harga.
1. Jika sistem menemukan garis harga kategori yang memiliki tingkat penjualan untuk kombinasi Kategori **dan** Unit **, tingkat penjualan tersebut** digunakan sebagai tingkat penjualan default.
1. Jika sistem menemukan garis harga kategori yang cocok, metode penetapan harga dapat digunakan untuk memasukkan harga jual default. Tabel berikut menunjukkan perilaku default untuk harga pengeluaran dalam Operasi Proyek.

    | Konteks | Metode Penetapan Harga | Harga default |
    | --- | --- | --- |
    | Perkiraan | Harga Per unit | Berdasarkan garis harga kategori. |
    |        | Berdasarkan biaya | 0.00 |
    |        | Markup atas biaya | 0.00 |
    | Aktual | Harga Per unit | Berdasarkan garis harga kategori. |
    |        | Berdasarkan biaya | Berdasarkan biaya aktual terkait. |
    |        | Markup atas biaya | Markup diterapkan, sebagaimana didefinisikan oleh garis harga kategori, ke tingkat biaya satuan dari biaya aktual terkait. |

1. Jika sistem tidak dapat menandingi **nilai Kategori** dan **Unit**, tingkat penjualan diatur ke **0** (nol) secara default.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan tingkat penjualan pada baris aktual dan perkiraan untuk Material

Perkiraan konteks untuk **Materi** mengacu pada:

- Kutip detail baris untuk **Materi**.
- Detail garis kontrak untuk **Material**.
- Garis perkiraan material pada suatu proyek.

Konteks aktual untuk **Materi** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Materi**.
- Baris jurnal yang dibuat saat log penggunaan Material dikirimkan.
- Detail baris faktur untuk **Materi**. 

Setelah daftar harga untuk penjualan ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan harga jual unit default.

1. Sistem mencocokkan kombinasi **bidang Produk** dan **Unit** pada garis perkiraan untuk **Material** dengan baris item daftar harga pada daftar harga.
1. Jika sistem menemukan baris item daftar harga yang memiliki tingkat penjualan untuk **kombinasi Produk** dan **Unit**, dan jika metode penetapan harga adalah **jumlah** Mata Uang, harga penjualan yang ditentukan pada baris daftar harga akan digunakan. 
1. **Jika nilai bidang Produk** dan **Unit** tidak cocok, atau jika metode penetapan harga adalah sesuatu selain **jumlah** Mata Uang, nilai penjualan diatur ke **0** (nol) secara default. Perilaku ini terjadi karena Operasi Proyek hanya **mendukung metode penetapan harga jumlah** mata uang untuk materi yang digunakan pada proyek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Menentukan tarif biaya untuk perkiraan dan aktual berbasis proyek
description: Artikel ini memberikan informasi tentang bagaimana tarif biaya untuk perkiraan dan aktual berbasis proyek ditentukan.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475277"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Menentukan tarif biaya untuk perkiraan dan aktual berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Untuk menentukan harga biaya pada perkiraan dan aktual di Microsoft Dynamics 365 Project Operations, sistem pertama-tama menggunakan tanggal dan mata uang dalam perkiraan masuk atau konteks aktual untuk menentukan daftar harga penjualan. Dalam konteks aktual secara khusus, sistem menggunakan **bidang Tanggal** transaksi untuk menentukan daftar harga mana yang berlaku. Nilai **tanggal** Transaksi dari perkiraan masuk atau aktual dibandingkan dengan **nilai Efektif Mulai (Timezone independen)** dan **Akhir Efektif (Timezone independent)** pada daftar harga. Setelah daftar harga biaya ditentukan, sistem menentukan tingkat biaya.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Menentukan tarif biaya dalam perkiraan dan konteks aktual untuk Waktu

Konteks perkiraan untuk **Waktu** mengacu pada:

- Kutip detail baris untuk **Waktu**.
- Detail garis kontrak untuk **Waktu**.
- Tugas sumber daya pada proyek.

Konteks aktual untuk **Waktu** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Waktu**.
- Baris jurnal yang dibuat saat entri waktu dikirimkan.

Setelah daftar harga biaya ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif biaya default.

1. Sistem ini cocok dengan kombinasi **bidang Peran**, **Perusahaan** Sumber Daya, dan **Unit** Sumber Daya dalam perkiraan atau konteks aktual untuk **Waktu** terhadap garis harga peran pada daftar harga. Pencocokan ini mengasumsikan bahwa Anda menggunakan dimensi harga standar untuk biaya tenaga kerja. Jika Anda telah mengonfigurasi sistem agar sesuai dengan bidang selain atau selain **Peran, Perusahaan** Sumber Daya, **dan** Unit **Sumber Daya, kombinasi yang berbeda digunakan untuk mengambil garis harga** peran yang cocok.
1. Jika sistem menemukan garis harga peran yang memiliki tingkat biaya untuk **kombinasi Peran**, **Perusahaan** Sumber Daya, dan **Unit** Sumber Daya, tarif biaya tersebut digunakan sebagai tarif biaya default.
1. Jika sistem tidak dapat menandingi **nilai Peran**, **Perusahaan** Sumber Daya, dan **Unit** Sumber Daya, sistem akan menjatuhkan dimensi yang memiliki prioritas terendah, mencari garis harga peran yang memiliki kecocokan dengan dua nilai dimensi lainnya, dan terus secara progresif menurunkan dimensi hingga baris harga peran yang cocok ditemukan. Tarif biaya dari catatan tersebut akan digunakan sebagai tarif biaya default. Jika sistem tidak menemukan baris harga peran yang cocok, harga akan ditetapkan ke **0** (nol) secara default.

> [!NOTE]
> Jika Anda mengonfigurasi prioritas yang berbeda dari **bidang Unit** Peran **dan** Sumber Daya, atau jika Anda memiliki dimensi lain yang memiliki prioritas lebih tinggi, perilaku sebelumnya akan berubah sesuai dengan itu. Sistem mengambil catatan harga peran yang memiliki nilai yang cocok dengan setiap nilai dimensi harga dalam urutan prioritas. Baris yang memiliki nilai nol untuk dimensi tersebut adalah yang terakhir.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Menentukan tarif biaya pada garis aktual dan perkiraan untuk Biaya

Konteks estimasi untuk **Pengeluaran** mengacu pada:

- Kutip detail baris untuk **Biaya**.
- Detail garis kontrak untuk **Biaya**.
- Perkiraan biaya pada suatu proyek.

Konteks aktual untuk **Pengeluaran** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Biaya**.
- Baris jurnal yang dibuat saat entri pengeluaran dikirimkan.

Setelah daftar harga biaya ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif biaya default.

1. Sistem ini mencocokkan kombinasi **bidang Kategori** dan **Unit** dalam perkiraan atau konteks aktual untuk **Pengeluaran** terhadap garis harga kategori pada daftar harga.
1. Jika sistem menemukan garis harga kategori yang memiliki tarif biaya untuk kombinasi Kategori **dan** Unit **, tarif biaya tersebut** digunakan sebagai tarif biaya default.
1. Jika sistem tidak dapat mencocokkan **nilai Kategori** dan **Unit**, harga diatur ke **0** (nol) secara default.
1. Dalam konteks estimasi, jika sistem dapat menemukan garis harga kategori yang cocok, tetapi metode penetapan harga adalah sesuatu selain **Harga Per Unit**, tarif biaya diatur ke **0** (nol) secara default.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Menentukan tarif biaya pada garis aktual dan perkiraan untuk Material

Perkiraan konteks untuk **Materi** mengacu pada:

- Kutip detail baris untuk **Materi**.
- Detail garis kontrak untuk **Material**.
- Perkiraan material pada suatu proyek.

Konteks aktual untuk **Materi** mengacu pada:

- Baris jurnal Entri dan Koreksi untuk **Materi**.
- Baris jurnal yang dibuat saat log penggunaan Material dikirimkan.

Setelah daftar harga biaya ditentukan, sistem menyelesaikan langkah-langkah berikut untuk memasukkan tarif biaya default.

1. Sistem ini menggunakan kombinasi **bidang Produk** dan **Unit** dalam perkiraan atau konteks aktual untuk **Material** terhadap baris item daftar harga pada daftar harga.
1. Jika sistem menemukan baris item daftar harga yang memiliki tarif biaya untuk kombinasi Produk **dan** Unit **, tarif biaya tersebut** digunakan sebagai tarif biaya default.
1. Jika sistem tidak dapat mencocokkan **nilai Produk** dan **Unit**, biaya unit diatur ke **0** (nol) secara default.
1. Dalam perkiraan atau konteks aktual, jika sistem dapat menemukan baris item daftar harga yang cocok, tetapi metode penetapan harga adalah sesuatu selain **jumlah** Mata Uang, biaya unit diatur ke **0** secara default. Perilaku ini terjadi karena Operasi Proyek hanya **mendukung metode penetapan harga jumlah** mata uang untuk materi yang digunakan pada proyek.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

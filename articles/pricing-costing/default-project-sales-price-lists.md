---
title: Daftar harga default
description: Artikel ini menyediakan informasi tentang daftar harga biaya dan penjualan default dalam Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410266"
---
# <a name="default-price-lists"></a>Daftar harga default

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

## <a name="sales-price-lists"></a>Daftar harga penjualan

Setiap kuotasi dan kontrak proyek di Dynamics 365 Project Operations berisi daftar harga penjualan default. 

### <a name="price-list-default-on-project-quotes"></a>Daftar harga default pada kuotasi proyek
Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang default pada kuotasi proyek:

1. Sistem melihat daftar harga yang dilampirkan ke daftar harga proyek akun. 
1. Jika tidak ada daftar harga proyek yang melekat pada rekaman akun, sistem melihat daftar harga penjualan yang melekat pada parameter proyek yang sesuai dengan mata uang kuotasi proyek.
1. Selanjutnya, sistem memeriksa efektivitas tanggal daftar harga yang cocok dengan rentang tanggal kuotasi proyek. Khususnya, tanggal kuotasi dibuat.
1. Jika ada beberapa daftar harga yang efektif untuk tanggal kuotasi proyek, semua daftar harga default pada kuotasi proyek.
1. Jika tidak ada daftar harga yang berlaku untuk tanggal kuotasi proyek, tidak ada daftar harga proyek default pada kuotasi proyek. Pesan peringatan akan terjadi pada kuotasi proyek. Pesan menyatakan bahwa aktual dan estimasi pada proyek tidak akan diberi harga karena tidak ada daftar harga proyek terlampir.

### <a name="price-list-default-on-project-contracts"></a>Daftar harga default pada kontrak proyek 
Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang default pada kontrak proyek:

1. Jika kontrak dibuat dari kuotasi, daftar harga proyek pada kuotasi disalin secara terpisah dan dilampirkan ke kontrak proyek.
1. Jika kontrak dibuat dari awal, sistem melihat daftar harga yang dilampirkan ke daftar harga proyek akun. Jika tidak ada daftar harga proyek yang melekat pada rekaman akun, sistem mencari daftar harga penjualan yang melekat pada parameter proyek yang sesuai dengan mata uang kontrak proyek.
1. Selanjutnya, sistem memeriksa efektivitas tanggal daftar harga yang cocok dengan rentang tanggal kontrak proyek. Khususnya, tanggal kontrak dibuat.
1. Jika ada beberapa daftar harga yang efektif untuk tanggal kontrak, semua daftar harga default pada kontrak.
1. Jika tidak ada daftar harga yang berlaku untuk tanggal kontrak, tidak ada daftar harga proyek default pada kontrak. Pesan peringatan akan terjadi pada kontrak proyek. Pesan menyatakan bahwa aktual dan estimasi pada proyek tidak akan diberi harga karena tidak ada daftar harga proyek terlampir.

## <a name="cost-price-lists"></a>Daftar Harga Biaya

Daftar harga biaya tidak default ke entitas mana pun dalam Project Operations. Menentukan daftar harga biaya yang akan digunakan untuk biaya proyek selalu dilakukan per transaksi. Sistem menyelesaikan proses berikut untuk menentukan daftar harga mana yang digunakan untuk biaya proyek:

1. Sistem ini melihat daftar harga yang melekat pada unit organisasi kontrak proyek.
1. Selanjutnya sistem melihat efektivitas tanggal dari daftar harga yang cocok dengan konteks tanggal estimasi masuk atau konteks aktual.

    - *Konteks estimasi* mengacu pada salah satu dari ketiga konteks estimasi dalam Project Operations:

        - Baris estimasi proyek
        - Detail baris kuotasi
        - Rincian Baris Kontrak

    - *Konteks aktual* mengacu pada salah satu dari tiga sumber aktual di Project Operations:

       - Baris jurnal entri yang dibuat secara manual, atau baris jurnal koreksi yang dibuat dalam jurnal koreksi
       - Baris jurnal yang dibuat selama pengajuan log waktu, pengeluaran, atau penggunaan bahan
       - Rincian Baris Faktur

    Bila Project Operations cocok dengan pengaruh tanggal dari baris jurnal masuk atau detail baris faktur dalam *konteks yang sebenarnya*, operasi akan menggunakan bidang **Tanggal transaksi**.

    - Jika beberapa daftar harga yang efektif untuk tanggal konteks estimasi masuk atau konteks aktual, daftar harga yang paling baru dibuat akan dipilih.
    - Jika tidak ada daftar harga proyek yang melekat pada unit organisasi kontrak proyek, sistem melihat daftar harga biaya yang melekat pada parameter proyek yang sesuai dengan mata uang proyek.

## <a name="enable-multi-currency-cost-price-list"></a>Aktifkan daftar harga biaya multi-mata uang

Pengaturan ini dapat ditemukan di **Parameter** \> **Pengaturan**. Nilai default adalah **Tidak**.

Bila pengaturan ini diaktifkan (artinya, nilai diatur ke **Ya**), sistem akan berperilaku dengan cara berikut:

- Unit ini memungkinkan daftar harga biaya dalam mata uang apa pun untuk dikaitkan dengan unit organisasional. Misalnya, daftar harga biaya dalam mata uang EUR dapat dilampirkan ke unit organisasional dalam mata uang USD. Sistem akan terus memvalidasi bahwa daftar harga biaya yang dilampirkan ke unit organisasional tidak memiliki efektivitas tanggal tumpang tindih.
- Program ini memvalidasi bahwa daftar harga biaya yang dilampirkan ke parameter proyek tidak memiliki efektivitas tanggal tumpang tindih, meskipun memiliki mata uang yang berbeda. Perilaku ini berbeda dengan perilaku default (artinya perilaku saat nilai diatur ke **Tidak**). Dalam perilaku default, hanya daftar harga biaya yang memiliki mata uang yang **sama** divalidasi untuk efektivitas tanggal yang tidak tumpang tindih.
- Untuk konteks transaksi masuk, ia menentukan daftar harga biaya berdasarkan hanya efektivitas tanggal. Perilaku ini berbeda dengan perilaku default, di mana sistem memilih daftar harga biaya yang sesuai dengan mata uang proyek dan efektivitas tanggal.

Karena perubahan perilaku ini, pelanggan Project Operations akan dapat mengelola daftar harga biaya global yang akan relevan untuk seluruh perusahaan. Mereka tidak akan memiliki daftar harga dalam setiap mata uang operasi. Daftar harga global akan memiliki pengaruh tanggal dan akan memungkinkan pengaturan tarif biaya dalam mata uang apa pun untuk kombinasi nilai dimensi harga yang spesifik. Mata uang dari daftar harga biaya digunakan hanya untuk memasukkan nilai default saat rekaman item **harga Peran**, **harga Kategori**, dan **daftar harga** dibuat. Item tidak akan digunakan untuk menentukan daftar harga.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

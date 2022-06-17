---
title: Daftar harga produk
description: Artikel ini menyediakan informasi tentang daftar harga dalam harga katalog yang digunakan untuk kutipan dan kontrak proyek.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 68203f5adf7bf41d97e662e335d481ccac959ed6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917626"
---
# <a name="product-price-lists"></a>Daftar harga produk

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

 Dalam Project Operations, **Daftar harga produk** dan entitas item daftar harga terkait mendukung fungsi untuk produk penetapan harga pada kuotasi berbasis produk dan baris kontrak. Untuk produk yang digunakan pada proyek, rekaman item daftar harga untuk daftar harga proyek digunakan. 

Produk harus diatur sehingga mereka memiliki biaya default dan daftar harga dalam Katalog Produk. Gunakan harga banderol, biaya standar, dan biaya saat ini untuk mengkonfigurasi biaya default dan harga banderol. Harga banderol default digunakan pada baris kuotasi atau baris kontrak proyek hanya bila sistem tidak dapat menemukan baris daftar harga untuk produk tersebut dalam daftar harga produk untuk kuotasi atau kontrak proyek.

Harga biaya baris Katalog Produk dapat diubah antara kuotasi. Kemampuan ini penting, karena jika Anda tidak melacak secara akurat biaya, Anda tidak dapat menentukan keuntungan operasional pada keterlibatan proyek. Per default, biaya standar produk digunakan sebagai harga biaya. Namun, harga default dapat diperbarui pada baris kuotasi jika ada harga yang berbeda untuk kuotasi tersebut.

## <a name="price-list-items"></a>Item Daftar Harga

Anda dapat menambahkan produk dari Katalog Produk ke daftar harga yang berbeda. Baris daftar harga untuk produk selalu merujuk unit tertentu. Harga untuk produk pada item daftar harga dapat dikonfigurasi sebagai jumlah mata uang. Atau, dapat dikonfigurasi sebagai fungsi dari daftar harga, biaya saat ini, atau biaya standar.

Fungsi penetapan harga mendukung berbagai pilihan pembulatan saat harga produk dikonfigurasi sebagai fungsi dari daftar harga, biaya standar, atau biaya saat ini. Selain mengambil keuntungan dari beberapa metode harga dan pilihan pembulatan, Anda dapat mengaitkan daftar diskon dengan item daftar harga. 

 
## <a name="default-product-price-list"></a>Daftar Harga produk Default
Setiap rekaman pelanggan memiliki bidang **daftar harga default**, di mana Anda dapat menentukan daftar harga yang sesuai dengan mata uang pelanggan. Nilai default tidak secara otomatis dimasukkan dalam bidang ini. Bila ada perjanjian harga kustom dengan pelanggan tertentu, Anda dapat menggunakan bidang ini untuk mengaitkan daftar harga dengan pelanggan tersebut.

Entitas kontrak proyek, peluang, dan kuotasi menggunakan urutan berikut untuk memasukkan daftar harga produk default. Urutan yang sama digunakan untuk daftar harga proyek.

1.  Kuotasi
2.  Peluang
3.  Pelanggan
4.  Pengaturan global 

Secara default, bidang **produk** pada baris kuotasi mencantumkan semua produk aktif dalam daftar harga produk kuotasi. Jika produk telah diaktifasi, atau jika produk tersebut adalah produk draf, maka produk tersebut tidak terdaftar, meskipun di dalam daftar harga. 

Baris Katalog Produk ditambahkan sebagai baris faktur pada faktur pertama yang dibuat untuk kontrak proyek. Pada faktur draf, baris faktur tersebut dapat dihapus. Dalam kasus tersebut, baris akan muncul pada faktur berikutnya hingga ditagih, atau hingga faktur dikirim ke pelanggan. Anda tidak dapat menagih kuantitas parsial baris faktur produk. Saat lini produk dari kontrak proyek ditagih, nilai aktual dibuat. Namun, aktual tersebut tidak ditautkan ke entitas proyek terkait. Dengan kata lain, baris kontrak proyek berbasis produk terlepas dari penggunaan berbasis proyek. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]

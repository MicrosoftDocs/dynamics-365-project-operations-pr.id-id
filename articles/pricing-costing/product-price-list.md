---
title: Daftar harga produk
description: Topik ini menyediakan informasi tentang daftar harga dalam harga katalog yang digunakan untuk kuotasi dan kontrak proyek.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 702402854c0787dae0bde854c9c274f5c23c131f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119602"
---
# <a name="product-price-lists"></a>Daftar harga produk

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Entitas item daftar harga dan daftar harga mendukung harga Katalog Produk. Untuk sebagian besar, fungsi ini digunakan untuk baris berbasis Katalog pada kuotasi proyek dan kontrak proyek.

Untuk baris berbasis proyek, kontrak menunjukkan kesepakatan setelah menang. Karena proses negosiasi biasanya mendahului menang, harga yang melekat pada kuotasi selalu disalin sebagaimana adanya daftar harga baru dan dilampirkan ke kontrak. Daftar harga baru ini tidak dapat diubah di luar cakupan kontrak. Pembatasan ini membantu melindungi kartu tarif yang dinegosiasikan dari setiap perubahan harga yang terjadi pada daftar harga Master.

Produk harus diatur sehingga mereka memiliki biaya default dan daftar harga dalam Katalog Produk. Gunakan harga banderol, biaya standar, dan biaya saat ini untuk mengkonfigurasi biaya default dan harga banderol. Harga banderol default digunakan pada baris kuotasi atau baris kontrak proyek hanya bila sistem tidak dapat menemukan baris daftar harga untuk produk tersebut dalam daftar harga produk untuk kuotasi atau kontrak proyek.

Harga biaya baris Katalog Produk dapat diubah antara kuotasi. Kemampuan ini penting, karena jika Anda tidak melacak secara akurat biaya, Anda tidak dapat menentukan keuntungan operasional pada keterlibatan proyek. Per default, biaya standar produk digunakan sebagai harga biaya. Namun, harga default dapat diperbarui pada baris kuotasi jika ada harga yang berbeda untuk kuotasi tersebut.

## <a name="price-list-items"></a>Item Daftar Harga

Anda dapat menambahkan produk dari Katalog Produk ke daftar harga yang berbeda. Baris daftar harga untuk produk selalu merujuk unit tertentu. Harga untuk produk pada item daftar harga dapat dikonfigurasi sebagai jumlah mata uang. Atau, dapat dikonfigurasi sebagai fungsi dari daftar harga, biaya saat ini, atau biaya standar.

PSA mendukung berbagai pilihan pembulatan saat harga dikonfigurasi sebagai fungsi dari daftar harga, biaya standar, atau biaya saat ini. Selain mengambil keuntungan dari beberapa metode harga dan pilihan pembulatan, Anda dapat mengaitkan daftar diskon dengan item daftar harga. 

Bila Anda membuat daftar harga kustom baru untuk kuotasi dengan memilih **Buat harga kustom** pada halaman **Kuotasi proyek**, salinan daftar harga dibuat, dan bidang **entitas** pada header dari daftar harga baru diatur ke **entitas penjualan**. Nama daftar harga baru ditambahkan dengan nama kuotasi dan stempel waktu. Anda juga dapat menggunakan nama daftar harga baru dan nama kuotasi di alur kerja kustom untuk memicu peninjauan dan persetujuan tambahan untuk kuotasi yang menggunakan harga kustom.

 
## <a name="default-product-price-list"></a>Daftar Harga produk Default
Setiap rekaman pelanggan memiliki bidang **daftar harga default**, di mana Anda dapat menentukan daftar harga yang sesuai dengan mata uang pelanggan. Nilai default tidak secara otomatis dimasukkan dalam bidang ini. Bila ada perjanjian harga kustom dengan pelanggan tertentu, Anda dapat menggunakan bidang ini untuk mengaitkan daftar harga dengan pelanggan tersebut.

Entitas kontrak proyek, peluang, dan kuotasi menggunakan urutan berikut untuk memasukkan daftar harga produk default. Urutan yang sama digunakan untuk daftar harga proyek.

1.  Kuotasi
2.  Peluang
3.  Pelanggan
4.  Pengaturan global 

Secara default, bidang **produk** pada baris kuotasi mencantumkan semua produk aktif dalam daftar harga produk kuotasi. Jika produk telah diaktifasi, atau jika produk tersebut adalah produk draf, maka produk tersebut tidak terdaftar, meskipun di dalam daftar harga. 

Baris Katalog Produk ditambahkan sebagai baris faktur pada faktur pertama yang dibuat untuk kontrak proyek. Pada faktur draf, baris faktur tersebut dapat dihapus. Dalam kasus tersebut, baris akan muncul pada faktur berikutnya hingga ditagih, atau hingga faktur dikirim ke pelanggan. Anda tidak dapat menagih kuantitas parsial baris faktur produk. Saat lini produk dari kontrak proyek ditagih, nilai aktual dibuat. Namun, aktual tersebut tidak ditautkan ke entitas proyek terkait. Dengan kata lain, baris kontrak proyek berbasis produk terlepas dari penggunaan berbasis proyek. Konsumsi material pada proyek tidak dilacak.

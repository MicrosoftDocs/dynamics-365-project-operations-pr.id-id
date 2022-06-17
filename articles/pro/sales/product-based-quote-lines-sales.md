---
title: Sekilas baris kuotasi berbasis produk - lite
description: Artikel ini memberikan informasi tentang bekerja dengan garis kutipan berbasis produk.
author: rumant
ms.date: 10/30/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: db0700e789202a8fdd0ef3b49959421ac54fb9ad
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914314"
---
# <a name="product-based-quote-lines-overview---lite"></a>Sekilas baris kuotasi berbasis produk - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Anda dapat membuat baris kuotasi berbasis produk di Dynamics 365 Project Operations. Anda Baris kuotasi berbasis produk dapat ditambahkan secara manual, atau dapat berupa item dari Katalog Produk.

## <a name="product-catalog"></a>Katalog produk

Setiap produk dalam Katalog Produk memiliki unit default dan grup unit. Jika beberapa produk memiliki rangkaian atribut yang sama, Anda dapat membuat rangkaian produk yang juga memiliki atribut serupa. 

Misalnya, perusahaan menjual lisensi langganan untuk berbagai jenis perangkat lunak. Semua perangkat lunak langganan memiliki dua atribut berikut:

- Jumlah pengguna
- Durasi langganan yang diukur dalam bulan

Untuk mengelola Katalog jenis, buat rangkaian produk yang diberi nama **perangkat lunak langganan**, dan tambahkan jumlah pengguna dan durasi langganan sebagai atribut. Selanjutnya, Anda dapat menambahkan produk individual ke keluarga produk **perangkat lunak langganan**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Tambahkan item Katalog Produk ke kuotasi proyek

Halaman **kuotasi proyek** dan **kontrak proyek** memiliki bagian untuk baris berbasis proyek dan baris berbasis produk. Untuk baris berbasis produk, daftar drop-down pada baris kuotasi atau baris kontrak proyek mencakup semua produk dan unit dalam daftar harga produk. Anda juga dapat menambahkan produk yang bukan bagian dari daftar harga produk.

Selain itu, Anda dapat memilih produk dari daftar harga lain atau langsung dari Katalog Produk. Bila Anda memilih produk secara langsung dari Katalog Produk, daftar harga default produk tersebut digunakan untuk mendapatkan harga penjualan produk. Jika daftar harga default tidak diatur, harga diatur ke 0 (nol).

Jika baris kuotasi didasarkan pada Katalog Produk, Anda dapat menimpa harga penjualan secara langsung pada baris kuotasi. Baris kuotasi dalam bidang **harga** dengan dua nilai yang tersedia:

- **Timpa Harga**
- **Gunakan Default**

Jika Anda memilih **Timpa Harga**, harga default tidak diatur. Namun, Anda harus memasukkan harga untuk produk pada baris kuotasi. Jika Anda memilih **gunakan default**, harga penjualan default akan digunakan dan bidang terkunci untuk pengeditan.

Harga penjualan default dimasukkan pada baris berbasis produk pada kuotasi. Bidang **harga** kemudian diatur ke **Timpa Harga** sehingga Anda dapat mengedit harga default pada baris kuotasi. Ini adalah penimpaan khusus Project Operations pada perilaku baris berbasis produk di Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
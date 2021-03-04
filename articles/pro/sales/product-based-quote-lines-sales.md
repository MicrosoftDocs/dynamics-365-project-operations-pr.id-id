---
title: Sekilas baris kuotasi berbasis produk - lite
description: Topik ini menyediakan informasi tentang bekerja dengan baris kuotasi berbasis produk.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178192"
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
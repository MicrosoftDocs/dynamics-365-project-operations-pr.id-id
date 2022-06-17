---
title: Ikhtisar baris kontrak berbasis produk - lite
description: Artikel ini menyediakan informasi tentang jalur kontrak berbasis produk.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4ad1fe6d5d56468d887535ddf107eefed3cbd28d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919880"
---
# <a name="product-based-contract-lines-overview---lite"></a>Ikhtisar baris kontrak berbasis produk - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Anda dapat membuat baris kontrak berbasis produk di Dynamics 365 Project Operations. Baris kontrak berbasis produk dapat berupa baris yang dibuat secara manual, atau dapat berupa item dari Katalog Produk.

## <a name="product-catalog"></a>Katalog produk

Produk dalam Katalog Produk memiliki unit default dan grup unit. Jika beberapa produk memiliki rangkaian atribut yang sama, Anda dapat membuat rangkaian produk yang juga memiliki atribut tersebut. Semua produk dalam satu rangkaian produk mewarisi rangkaian atribut yang sama.

Misalnya, perusahaan menjual lisensi langganan untuk berbagai jenis perangkat lunak. Semua perangkat lunak langganan memiliki dua atribut berikut:

- Jumlah pengguna
- Durasi langganan (dalam bulan)

Untuk mengelola jenis Katalog ini, buat rangkaian produk yang diberi nama **perangkat lunak langganan**. Tambahkan atribut, **jumlah pengguna,** dan **durasi langganan** ke rangkaian produk. Selanjutnya, tambahkan produk individual ke rangkaian produk **perangkat lunak langganan**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Tambahkan item Katalog Produk ke kontrak proyek

Kontrak proyek memiliki bagian untuk dua jenis baris: berbasis proyek dan produk. Baris berbasis produk mencakup semua produk dan unit dalam daftar harga produk pada kontrak. Produk yang bukan bagian dari daftar harga produk kontrak dapat ditambahkan.

Anda dapat memilih produk dari daftar harga lainnya, atau langsung dari Katalog Produk. Bila Anda memilih produk secara langsung dari Katalog Produk, daftar harga default produk tersebut digunakan untuk harga penjualan produk. Jika daftar harga default tidak diatur, harga diatur ke 0 (nol).

Jika baris kontrak didasarkan pada Katalog Produk, Anda dapat menimpa harga penjualan secara langsung pada baris tersebut. Baris kontrak memiliki bidang **harga** dengan dua nilai:

- **Timpa Harga**
- **Gunakan default**

Jika Anda menetapkan bidang **Harga** ke **Timpa Harga**, harga default tidak ditetapkan. Masukkan harga untuk produk pada baris kontrak. Jika Anda mengatur bidang ke **Gunakan default**, harga penjualan default akan digunakan dan bidang tidak dapat diedit.

Setelah Anda menginstal Project Operations, harga penjualan default dimasukkan pada baris berbasis produk pada kontrak. Bidang **harga** kemudian diatur ke **Timpa Harga** sehingga Anda dapat mengedit harga default pada baris kontrak. Ini adalah penimpaan spesifik Project Operations pada perilaku baris berbasis produk di Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
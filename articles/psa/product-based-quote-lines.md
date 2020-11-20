---
title: Baris kuotasi berbasis produk
description: Topik ini menyediakan informasi tentang kuotasi berbasis produk.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 9c3b2b35abe894e79d6f55a7ddd6e5c64d0f12f2
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123203"
---
# <a name="product-based-quote-lines"></a>Baris kuotasi berbasis produk

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Anda dapat membuat baris kuotasi berbasis produk di Dynamics 365 Project Service Automation. Baris kuotasi berbasis produk dapat berupa baris "tulis", atau dapat berupa item dari Katalog Produk.

## <a name="product-catalog"></a>Katalog produk

Produk dalam Katalog Produk Dynamics 365 memiliki unit default dan grup unit. Jika beberapa produk memiliki rangkaian atribut yang sama, Anda dapat membuat rangkaian produk yang juga memiliki atribut tersebut. Semua produk dalam satu rangkaian produk mewarisi rangkaian atribut yang sama.

Misalnya, perusahaan menjual lisensi langganan untuk berbagai perangkat lunak. Semua perangkat lunak langganan memiliki dua atribut berikut:

- Jumlah Pengguna 
- Durasi langganan (dalam bulan)

Cara yang baik untuk mempertahankan Katalog jenis ini adalah dengan membuat rangkaian produk yang diberi nama **perangkat lunak langganan**, dan memiliki **jumlah pengguna** dan **durasi langganan** sebagai atribut. Selanjutnya, Anda dapat menambahkan produk individual, seperti **Dynamics 365 Sales** atau **Dynamics 365 Field Service** ke rangkaian produk **perangkat lunak langganan**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Menambahkan item Katalog Produk ke kuotasi proyek

Halaman kuotasi proyek dan kontrak proyek memiliki bagian untuk dua jenis baris: baris berbasis proyek dan lini produk. Untuk baris berbasis produk, Dynamics 365 digunakan untuk menambahkan item dari Katalog Produk ke kuotasi. Daftar drop-down pada baris kuotasi atau kontrak proyek mencakup semua produk dan unit dalam daftar harga produk yang dilampirkan pada kuotasi atau kontrak proyek. Anda juga dapat menambahkan produk yang bukan bagian dari daftar harga produk kuotasi.

Selain itu, Anda dapat memilih produk dari daftar harga lain, atau Anda dapat memilih produk langsung dari Katalog Produk. Bila Anda memilih produk secara langsung dari Katalog Produk, daftar harga default produk tersebut digunakan untuk mendapatkan harga penjualan produk. Jika daftar harga default tidak diatur, harga diatur ke 0 (nol).

Jika baris kuotasi didasarkan pada Katalog Produk, Anda dapat menimpa harga penjualan secara langsung pada baris kuotasi. Perhatikan bahwa baris kuotasi di Dynamics 365 memiliki bidang **harga**. Tersedia dua nilai:

- Timpa Harga  
- Gunakan default

Jika Anda menetapkan bidang ini ke **Timpa Harga**, Dynamics 365 tidak menetapkan harga default. Anda harus memasukkan harga untuk produk pada baris kuotasi. Jika Anda menetapkan bidang ini ke **Gunakan default**, maka Dynamics 365 menggunakan harga penjualan default dan mengunci bidang untuk mencegah pengeditan.

Setelah Anda menginstal PSA, harga penjualan default dimasukkan pada baris berbasis produk pada kuotasi. Bidang **harga** kemudian diatur ke **Timpa Harga** sehingga Anda dapat mengedit harga default pada baris kuotasi.

> ![Mengatur Timpa Harga](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Faktor kuantitas untuk produk

PSA menggunakan faktor kuantitas untuk mendukung penjualan produk berbasis langganan. Untuk produk berbasis langganan, kuantitas pada kuotasi atau baris kontrak proyek dinyatakan sebagai jumlah bulan pengguna.

Biasanya, harga perangkat lunak langganan disimpan dalam Katalog sebagai harga per pengguna per bulan. Namun, Anda dapat menggunakan Deskripsi waktu lain. Selama proses penjualan, harga pada baris kuotasi biasanya adalah per-pengguna, per bulan harga yang dinegosiasikan dan didiskon oleh agen penjualan TI. Setiap transaksi memiliki jumlah pengguna yang berbeda dan jumlah bulan langganan yang berbeda. Kuantitas yang digunakan untuk menghitung jumlah baris kuotasi adalah produk dari jumlah pengguna dan jumlah bulan langganan.

Untuk mendukung jenis penjualan, PSA memperkenalkan konsep faktor kuantitas. Faktor kuantitas mengandalkan atribut produk di Dynamics 365. Bila Anda mengkonfigurasi properti tertentu untuk suatu produk, PSA memungkinkan Anda menandai subset properti tersebut, atau semua properti, sebagai faktor kuantitas.

PSA memvalidasi bahwa hanya properti numerik atau properti produk yang menandai jenis data numerik sebagai faktor kuantitas. Bila produk yang memiliki faktor kuantitas dikonfigurasi untuk ditambahkan ke baris kuotasi, bidang **kuantitas** pada baris kuotasi menjadi bidang hanya baca. Setelah Anda memasukkan nilai untuk properti produk yang merupakan faktor kuantitas, PSA menghitung kuantitas baris kuotasi.

Misalnya, Dynamics 365 mungkin memiliki properti berikut: 

- **Jumlah pengguna** -jumlah pengguna 
- **Jumlah bulan** -jumlah bulan langganan
- **SKU Produk** 

Properti **Jumlah pengguna** dan **Jumlah bulan** dapat ditandai sebagai faktor kuantitas dengan mengedit properti lini produk. 

> ![Menandai Jumlah pengguna dan Jumlah bulan sebagai faktor kualitas](media/basic-guide-11.png)
 

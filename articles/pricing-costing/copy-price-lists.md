---
title: Menyalin daftar harga
description: Topik ini menyediakan informasi tentang cara menyalin daftar harga produk dalam Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003730"
---
# <a name="copy-price-lists"></a>Menyalin daftar harga

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda dapat membuat salinan daftar harga di Dynamics 365 Project Operations. Misalnya, Anda dapat membuat daftar harga untuk tahun mendatang menggunakan daftar harga dari tahun berjalan.  Atau, Anda dapat menyalin daftar harga untuk tarif tagihan dan harga penjualan dari daftar harga untuk biaya. 

Untuk membuat salinan daftar harga, selesaikan langkah berikut.

1. Buka daftar harga yang Anda ingin Buat salinan dan pilih **Salin**.
2. Masukkan informasi yang diperlukan untuk menyalin daftar harga. Tabel berikut menunjukkan pertimbangan yang perlu diingat saat memasukkan informasi.

| Bidang | KETERANGAN | Dampak hilir |
| --- | --- | --- |
| Nama | Nama dari daftar harga sumber dengan kata **-copy** ditambahkan. | Daftar Harga mencakup nilai ini di semua halaman daftar dan pilihan menurun. |
| Konteks | Masukkan konteks yang diinginkan untuk daftar harga target. | Daftar harga yang memiliki konteks diatur ke **biaya** digunakan untuk mencari harga untuk perkiraan biaya dan aktual biaya. Daftar harga yang memiliki konteks diatur ke **Penjualan** digunakan untuk mencari harga untuk estimasi penjualan dan aktual penjualan. Hanya daftar harga yang memiliki konteks yang diatur ke **penjualan** yang dapat dilampirkan ke daftar harga proyek untuk pelanggan, kuotasi, atau kontrak. |
| Tanggal Mulai | Tanggal mulai dari periode di mana daftar harga efektif. | Bersama dengan **tanggal berakhir**, bidang ini digunakan untuk menentukan daftar harga yang berlaku untuk estimasi tertentu atau baris aktual. |
| Tanggal Akhir | Tanggal akhir dari periode di mana daftar harga efektif. | Bersama dengan **tanggal Mulai**, bidang ini digunakan untuk menentukan daftar harga yang berlaku untuk estimasi tertentu atau baris aktual. |
| Mata uang | Mata uang dari daftar harga sumber. Pilihan ini dapat diubah. | Saat ini diubah, Semua baris harga yang dihasilkan untuk item Katalog tenaga kerja, pengeluaran, dan produk dikonversi ke mata uang daftar harga target selama penyalinan. |
| Satuan Waktu | Mata uang dari daftar harga sumber. Pilihan ini dapat diubah. | Saat ini diubah, Semua baris harga yang dihasilkan untuk item tenaga kerja dikonversi ke unit daftar harga target selama penyalinan. Konversi dari konfigurasi unit untuk unit waktu daftar harga sumber dan unit waktu daftar harga target digunakan. |
| KETERANGAN | Deskripsi dari daftar harga sumber dengan kata **-copy** ditambahkan. Ini adalah bidang teks dan memungkinkan Anda untuk memiliki deskripsi multi-baris dari daftar harga. | Bidang ini diperlihatkan dalam tampilan **Terkait** pada daftar harga di berbagai entitas yang memiliki daftar harga terkait. |

3. Simpan daftar harga. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Perbarui daftar harga dengan menerapkan mark-up untuk semua harga

1. Pada tab **peran**, **kategori**, dan **item Daftar Harga** dari daftar harga, Anda dapat memilih **Perbarui harga** untuk menerapkan markup untuk semua harga di subkisi. 
2. Pada halaman dialog yang terbuka, masukkan mark-up. Anda juga dapat memasukkan persentase mark-up negatif untuk menurunkan harga dengan persentase tertentu. 
3. Pilih **OK** pada halaman dialog, lalu Verifikasikan bahwa harga di subkisi mencerminkan perubahan yang Anda buat.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
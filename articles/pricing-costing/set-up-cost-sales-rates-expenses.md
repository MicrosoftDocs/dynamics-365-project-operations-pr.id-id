---
title: Mengonfigurasikan biaya dan tarif penjualan untuk pengeluaran
description: Artikel ini memberikan informasi tentang cara mengatur tarif biaya dan penjualan untuk kategori transaksi dan pengeluaran.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c503230348750af246f6ee7a4af1176d7bf22ba4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911876"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Mengonfigurasikan biaya dan tarif penjualan untuk pengeluaran

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda dapat mengkonfigurasi biaya dan harga penjualan untuk kategori transaksi di Dynamics 365 Project Operations. Karena biaya dan harga penjualan dirancang untuk pengeluaran, setiap kategori transaksi yang mencakup ini, juga harus diatur sebagai kategori pengeluaran. Pengaturan ini memastikan akurasi di fungsi hilir. Biaya dan harga penjualan untuk kategori transaksi hanya dapat didaftarkan dalam satu mata uang, yang harus berupa mata uang pada header daftar harga.

Untuk mengatur biaya dan tarif penjualan untuk kategori transaksi, selesaikan langkah berikut. 

1. Buka **Penjualan** > **Pelanggan** > **Daftar Harga**.
2. Untuk membuat daftar harga baru, pilih **Baru**. 
3. Pada **kategori harga**, pada menu subkisi, pilih **harga kategori baru**. 
4. Pada halaman **Buat cepat**, masukkan kategori transaksi dan unit yang Anda buat dengan harga baru.

Tabel berikut mencantumkan bidang pada tab **Umum** dan halaman **Buat cepat** dari baris harga kategori yang harus diingat saat Anda membuat harga kategori pada daftar harga penjualan atau biaya.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| Kategori Transaksi | Halaman **Umum** dan panel **Buat Cepat** | Pilih kategori transaksi yang Anda buat harga penjualan atau biayanya. | Kategori transaksi pada perkiraan yang masuk atau yang sebenarnya untuk pengeluaran akan dicocokkan dengan baris ini ke default biaya atau tarif penjualan dari kategori transaksi. |
| Jadwal Unit | Halaman **Umum** dan panel **Buat Cepat** | Jadwal unit di-default dari jadwal unit kategori transaksi. | Tidak ada dampak hilir dari bidang ini. |
| Unit | Halaman **Umum** dan panel **Buat Cepat** | Pilih unit dengan tarif sedang disiapkan. | Unit pada estimasi masuk atau aktual dicocokkan dengan unit pada baris ini untuk men-default tarif pada estimasi pengeluaran atau aktual. |
| Metode Penetapan Harga | Halaman **Umum** dan panel **Buat Cepat** | Nilai yang mungkin dari bidang **metode harga** adalah, **harga per unit**, **Pada biayanya**, dan **markup atas biaya**. | Selama pengaturan harga, memilih **harga per unit** akan mengunci bidang **persen** pada baris harga kategori. Jika **pada biayanya** yang dipilih, bidang **harga** dan **persen** terkunci pada daftar harga penjualan. Memilih **markup atas Biaya** mengunci bidang **harga** pada daftar harga penjualan. Pada baris aktual masuk untuk pengeluaran, metode harga **pada biayanya** atau **markup atas biaya** pada baris penjualan belum ditagih yang terkait diberi harga yang sama dengan harga pada aktual biaya atau dihitung sebagai markup atas harga. |
| Harga | Halaman **Umum** dan panel **Buat Cepat** | Atur tingkat per unit untuk kategori transaksi dan kombinasi unit. Misalnya, tarif untuk jarak tempuh adalah 10 USD per mil dan 8 USD per kilometer. | Tingkat jarak tempuhakan menjadi tingkat yang default pada harga per unit atau biaya estimasi masuk atau baris aktual untuk kelas transaksi pengeluaran.|
| Persen | Halaman **Umum** dan panel **Buat Cepat** | Atur persentase atas biaya untuk kategori transaksi dan kombinasi unit. Misalnya, tarif penjualan tiket pesawat harus ditandai 10 persen dari biaya pengeluaran pesawat yang terjadi. | Persentase atas biaya ini hanyalah berlaku pada daftar harga penjualan bila metode harga yang dipilih adalah **Markup atas biaya**. |
| Mata uang | Halaman **Umum** dan panel **Buat Cepat** | Secara default, nilai ini berasal dari mata uang pada header dari daftar harga. Untuk harga kategori transaksi, mata uang tidak dapat diganti. | Mata uang ini default pada harga per unit baris aktual masuk untuk kelas transaksi pengeluaran untuk biaya dan penjualan. |

## <a name="pricing-methods-for-expenses"></a>Metode harga untuk pengeluaran

Bila Anda menyiapkan harga kategori yang hanya relevan dalam konteks harga pengeluaran, Anda dapat menggunakan salah satu dari tiga metode harga berikut:

- **Harga Per unit**
- **Berdasarkan biaya**
- **Markup atas biaya**

### <a name="price-per-unit"></a>Harga per unit
Bila metode harga ini dipilih pada baris harga kategori yang ditautkan ke daftar harga penjualan, harga di-default untuk kategori dan kombinasi unit di estimasi maupun aktual. Estimasi adalah baris estimasi proyek untuk pengeluaran, detail baris kuotasi, dan detail baris kontrak untuk pengeluaran.

### <a name="at-cost"></a>Berdasarkan biaya
Bila metode harga ini dipilih pada baris harga kategori yang ditautkan ke daftar harga penjualan, harga di-default untuk kategori dan kombinasi unit hanya untuk aktual pengeluaran. Misalnya, aktual penjualan yang belum ditagih untuk kelas transaksi pengeluaran. Harga unit ditetapkan pada aktual penjualan yang belum ditagih dari harga unit pada aktual biaya untuk pengeluaran tersebut. Harga yang di-default berdasarkan biaya tidak dilakukan pada estimasi proyek untuk pengeluaran atau baris kuotasi dan rincian baris kontrak untuk pengeluaran.

### <a name="markup-over-cost"></a>Markup atas biaya
Bila metode harga ini dipilih pada baris harga kategori yang ditautkan ke daftar harga penjualan, harga di-default untuk kategori dan kombinasi unit hanya untuk aktual pengeluaran. Misalnya, aktual penjualan yang belum ditagih untuk kelas transaksi pengeluaran. Harga unit ini ditetapkan pada aktual penjualan yang belum ditagih ke nilai yang dihitung dari harga unit pada aktual biaya untuk pengeluaran tersebut setelah persen markup yang ditetapkan diterapkan. Harga yang di-default berdasarkan biaya tidak dilakukan pada estimasi proyek untuk pengeluaran atau baris kuotasi dan rincian baris kontrak untuk pengeluaran.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

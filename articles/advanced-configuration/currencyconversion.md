---
title: Menyiapkan konversi mata uang untuk menghitung harga penjualan dari tarif biaya
description: Artikel ini menjelaskan cara mengkonfigurasi perilaku konversi mata uang yang akan digunakan di Microsoft Dynamics 365 Project Operations ketika transaksi penjualan dihasilkan dari transaksi biaya.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816692"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Menyiapkan konversi mata uang untuk menghitung harga penjualan dari tarif biaya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Di Microsoft Dynamics 365 Project Operations, harga penjualan untuk kategori pengeluaran dapat diatur sebagai nilai numerik, atau dapat disiapkan sehingga dihitung berdasarkan biaya yang dikeluarkan.

Saat disiapkan untuk dihitung berdasarkan biaya yang dikeluarkan, opsi berikut tersedia:

- Berdasarkan biaya
- Persentase mark up di atas biaya

Dalam skenario di mana biaya pengeluaran dikeluarkan dalam mata uang yang berbeda dari mata uang penjualan untuk kontrak proyek, konversi mata uang diperlukan untuk menghitung harga penjualan berdasarkan biaya.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Perilaku konversi mata uang yang menggunakan nilai tukar asli Dataverse 

Secara default, Operasi Proyek menggunakan nilai tukar mata uang yang disimpan dalam tabel Mata Uang di Dataverse. Untuk mengonfigurasi Operasi Proyek agar menggunakan nilai tukar asli untuk menghitung harga penjualan dari biaya, ikuti langkah-langkah berikut.

1.  **Buka Parameter Pengaturan \> Operasi \> Proyek**.
1.  **Buka halaman detail Parameter** Proyek.
1.  **Atur bidang Logika** konversi mata uang ke nilai kosong.

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Perilaku konversi mata uang yang menggunakan nilai tukar dari aplikasi keuangan dan operasi

Nilai tukar dalam tabel Mata Uang yang tersedia secara native tidak Dataverse berlaku tanggal. Oleh karena itu, mereka mungkin tidak selalu diskalakan ke persyaratan yang Anda miliki untuk perhitungan harga penjualan dari tarif biaya.

Anda dapat menggunakan nilai tukar dari lingkungan keuangan dan operasi untuk menghitung harga penjualan dalam mata uang penjualan dari tingkat biaya dalam mata uang biaya. Untuk mengonfigurasi perilaku konversi mata uang ini, ikuti langkah-langkah berikut.

1.  **Pada halaman Parameter** proyek, tambahkan **bidang Logika** konversi mata uang. Kemudian simpan dan publikasikan penyesuaian.
1.  **Buka Parameter Pengaturan \> Operasi \> Proyek**.
1.  **Buka halaman detail Parameter** Proyek. 
1.  **Atur bidang Perilaku** konversi mata uang ke Diperluas dengan fallback ke **default**.
1.  **Berikan izin Baca** Dual-write user **peran keamanan**  Global ke tabel berikut:

    - Mata Uang MSDYNKenamTukarkur\_
    - Mata Uang MSDYNParbelakangpairs\_
    - Jenis Tukar MSDYN\_

1. Di lingkungan keuangan dan operasi Anda, jalankan peta tulis ganda berikut dengan sinkronisasi awal:

    - Jenis nilai tukar (msdyn\_ exchangeratetypes)
    - Pasangan mata uang nilai tukar (msdyn\_ currencyexchangeratepairs)
    - Nilai Tukar CDS (msdyn\_ currencyexchangerates)

Setelah perubahan ini selesai, dual-write akan membuat nilai tukar dari lingkungan keuangan dan operasi tersedia di Dataverse. Operasi Proyek kemudian akan menggunakan nilai tukar tersebut untuk mengonversi nilai tukar ke dalam mata uang penjualan kontrak.

> [!NOTE]
> Perilaku konversi mata uang ini hanya berlaku untuk perhitungan harga penjualan dari tingkat biaya. Ini tidak akan digunakan untuk menghitung nilai mata uang dasar secara umum. Nilai mata uang dasar akan selalu menggunakan nilai tukar asli Dataverse , terlepas dari apakah Anda menyelesaikan prosedur ini.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

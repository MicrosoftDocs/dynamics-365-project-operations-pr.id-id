---
title: Skenario beberapa mata uang (versi 3. x)
description: Topik ini menyediakan informasi tentang skenario beberapa mata uang.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 89a91cf3dbbcf81dbb089ee88c8c177c73afb694914ca7d95eae96776d38abed
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005125"
---
# <a name="multiple-currency-scenarios"></a>Skenario beberapa mata uang

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 memiliki dua konsep mata uang:

- **Mata uang transaksi** - mata uang terjadinya transaksi. 
- **Mata uang dasar** - mata uang dari instans Dynamics 365. Mata uang ini diatur saat instans Dynamics 365 ditetapkan. Ini tidak dapat diubah.

Misalnya, Contoso AS menjual 100 t-shirt kepada pelanggan di Inggris seharga 15 ponsterling (GBP) masing-masing. Tabel berikut ini menunjukkan cara transaksi ini dicatat dalam entitas produk pesanan.

| Produk | Kuantitas | Harga per unit | Mata Uang | Jumlah | Kurs | Harga Per Unit (Dasar)| Jumlah (Dasar)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Kaos | 100      | 15             | GBP      | 1500   | 0.94          | $17,25               | $17,25       |

Kolom **mata uang** menunjukkan mata uang transaksi, yang merupakan mata uang terjadinya penjualan. Kolom **nilai tukar** adalah nilai tukar antara mata uang transaksi dan mata uang dasar. Mata uang dasar adalah dolar AS (USD). Mata uang dasar diatur saat instans Dynamics 365 ditetapkan.
Seperti ditunjukkan tabel, setiap transaksi tercatat di mata uang transaksi maupun mata uang dasar. Dynamics 365 menggunakan nilai tukar mata uang untuk menghitung jumlah mata uang dasar.

## <a name="project-service-automation-extensions"></a>Ekstensi Project Service Automation

Dynamics 365 Project Service Automation mempengaruhi transaksi mata uang, karena transaksi bisnis biasanya memiliki dua aspek: biaya dan penjualan.

Entitas berikut dianggap sebagai transaksi bisnis:

- Rincian baris kuotasi
- Rincian Baris Kontrak Proyek
- Baris Perkiraan
- Lini Jurnal
- Rincian Baris Faktur
- Aktual

Di setiap entitas ini, ada rekaman yang menunjukkan jumlah biaya atau jumlah penjualan. Seperti untuk entitas Dynamics 365 yang memiliki bidang **jumlah**, setiap rekaman mencakup jumlah pada mata uang transaksi dan mata uang dasar. 

PSA memperluas konsep mata uang transaksi untuk biaya dan penjualan dengan cara berikut:

- Mata uang transaksi biaya untuk transaksi waktu selalu berasal dari mata uang unit organisasi yang memiliki atau mengelola proyek. Unit organisasi ini dikenal sebagai unit kontrak.
- Mata uang transaksi penjualan untuk transaksi waktu dan pengeluaran selalu berasal dari mata uang kontrak proyek.
- Mata uang transaksi biaya untuk pengeluaran berasal dari mata uang untuk pembuatan entri pengeluaran.

## <a name="multiple-currency-scenario"></a>Skenario beberapa mata uang

Bagian ini menjelaskan contoh proyek yang disediakan Contoso Inggris untuk pelanggan yang dinamai fabrikam, Jepang. Berikut adalah cara mengkonfigurasi skenario:

1. GBP dan Yen Jepang (JPY) diatur dalam **pengaturan** \> **manajemen bisnis** \> **mata uang**. 
2. Akun pelanggan yang dinamai **fabrikam-Japan** diatur, dan JPY dipilih sebagai mata uang pada akun.
3. Unit organisasi yang bernama **Contoso UK** diatur, dan GBP dipilih sebagai mata uang.
4. Kontrak proyek dibuat, dengan **Contoso Inggris** ditetapkan sebagai unit kontrak dan **Fabrikam – Jepang** ditetapkan sebagai pelanggan.
5. Baris kontrak proyek dibuat berdasarkan pengaturan penagihan untuk berbagai kelas transaksi pada proyek, seperti penagihan untuk waktu versus penagihan biaya.
6. Proyek dibuat dengan **Contoso Inggris** ditetapkan sebagai unit kontrak. Proyek ini dibuat dan dipetakan ke baris kontrak proyek.


Selama estimasi yang menggunakan detail baris kuotasi, detail baris kontrak proyek, atau pada baris perkiraan jadwal, dua rekaman selalu dibuat di entitas. Satu rekaman adalah untuk biaya, dan rekaman lainnya adalah untuk penjualan.

- Secara default, mata uang transaksi pada rekaman biaya diatur ke mata uang unit kontrak proyek. Dalam contoh ini, mata uangnya adalah GBP.
- Secara default, mata uang transaksi pada rekaman penjualan diatur ke mata uang kontrak proyek. Dalam contoh ini, mata uangnya adalah JPY.

Ketika nilai aktual dibuat untuk waktu dengan menggunakan entri waktu atau baris jurnal, terjadi perilaku berikut ini:

- Secara default, mata uang transaksi pada rekaman biaya diatur ke mata uang unit kontrak proyek.
- Secara default, mata uang transaksi pada rekaman penjualan diatur ke mata uang kontrak proyek.

Ketika nilai aktual dibuat untuk pengeluaran dengan entri pengeluaran atau baris jurnal, terjadi perilaku berikut ini:

- Anda dapat merekam jumlah pengeluaran dalam mata uang apa pun. Pilih mata uang dengan menggunakan pemilih mata uang pada halaman **entri pengeluaran** atau halaman **baris jurnal**. Secara default, mata uang transaksi untuk rekaman biaya diatur ke mata di entri pengeluaran. 
- Secara default, mata uang transaksi untuk rekaman penjualan adalah mata uang kontrak proyek. Untuk mengatur mata uang ini, sistem pertama mengkonversi jumlah transaksi dalam mata uang yang dimasukkan pengguna ke mata uang dasar. Kemudian ini mengonversi jumlah ke mata uang kontrak proyek. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Hitungan diakumulasikan saat nilai aktual proyek direkam dalam beberapa mata uang transaksi

Dynamics 365 secara otomatis menangani akumulasi dari jumlah dalam mata uang yang berbeda. Berikut adalah contohnya.

| Kelas Transaksi | Jenis Transaksi| Date   | Sumber daya | Kategori Transaksi | Kuantitas | Harga per Unit | Jumlah      | Kurs | Jumlah dalam Dasar |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Penjualan Belum Tertagih   | 14 Jun | Panji  |                      | 8 jam    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Time              | Penjualan Belum Tertagih   | 15 Jun | Panji  |                      | 8 jam    | 20.000 JPY    | 160.000 JPY | 123           | 1.300,81 USD    |
| Pengeluaran           | Penjualan Belum Tertagih   | 16 Jun | Panji  | Hotel                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Pengeluaran           | Penjualan Belum Tertagih   | 17 Jun | Panji  | Rental Mobil           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Untuk menghitung total nilai penjualan yang belum ditagih pada proyek, Anda dapat membuat bidang Roll-up untuk bidang **jumlah** pada semua aktual penjualan belum tertagih yang terkait. Bidang Roll-up adalah konstruksi dari Dynamics 365 yang memungkinkan untuk rumus cepat pada rekaman terkait.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
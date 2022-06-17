---
title: Mengonfigurasikan tarif biaya tenaga kerja
description: Artikel ini memberikan informasi tentang cara mengatur tarif untuk biaya Operasi Proyek tenaga kerja
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5216c0af29eb33ce664857b1f42b4a3130f02c50
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924250"
---
# <a name="set-up-labor-cost-rates"></a>Mengonfigurasikan tarif biaya tenaga kerja

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_


Setiap daftar harga memiliki seperangkat tarif tenaga kerja (harga peran) yang selaras dengan konten dan efektivitas tanggal di daftar harga.

1. Buat daftar harga dan pada tab **peran harga**, di subkisi, pilih **peran baru**.
2. Pada halaman **Buat Cepat**, pilih peran dan unit organisasi.
3. Masukkan informasi bidang lainnya yang diperlukan.

Tabel berikut ini mencakup beberapa bidang yang penting saat membuat tarif tenaga kerja pada daftar harga biaya.

| Bidang | Lokasi | KETERANGAN | Dampak hilir |
| --- | --- | --- | --- |
| Peran | Halaman **Umum** dan panel **Buat Cepat** | Pilih peran untuk menerapkan tarif biaya. | Peran pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke biaya default peran. |
| Perusahaan Sumber Daya | Halaman **Umum** dan panel **Buat Cepat** | Pilih entitas hukum yang ditetapkan peran. Misalnya, pengembang dari Fabrikam India atau pengembang dari Fabrikam AS. | Perusahaan sumber daya pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke tarif biaya default peran. |
| Unit Sumber Daya | Halaman **Umum** dan panel **Buat Cepat** | Pilih unit organisasi atau divisi dari perusahaan tempat menggunakan peran ini. Misalnya, pengembang dari divisi Robotika Fabrikam India atau pengembang dari divisi perangkat lunak Fabrikam AS. | Unit sumber daya pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke biaya default peran. |
| Harga | Halaman **Umum** dan panel **Buat Cepat** | Mengatur tarif biaya untuk perusahaan sumber daya peran dan kombinasi unit sumber daya. Misalnya, pengembang dari Fabrikam India bernilai 1000 INR atau pengembang dari Fabrikam AS seharga 150 USD. | Harga ini adalah tarif biaya yang di-default pada biaya per unit baris aktual atau estimasi masuk untuk kelas transaksi pengeluaran **waktu**. |
| Mata uang | Halaman **Umum** dan panel **Buat Cepat** | Secara default, nilai mata uang ini berasal dari mata uang pada header daftar harga biaya, tetap dapat ditimpa. Misalnya, pengembang dari Fabrikam India bernilai 1000 INR. Pengembang dari Fabrikam USA berharga 150 USD. | Mata uang ini di-default pada biaya per unit daftar biaya aktual masuk untuk kelas transaksi **waktu**. Pada estimasi proyek, nilai mata uang dikonversi ke mata uang proyek dan ditunjukkan pada tampilan estimasi bertahap waktu. |
| Jadwal Unit | Halaman **Umum** dan panel **Buat Cepat** | Jadwal unit di-default ke waktu dan tidak dapat diubah pada entitas harga peran karena digunakan untuk mengekspresikan tarif berdasarkan satuan waktu. | Tidak ada dampak hilir. |
| Unit | Halaman **Umum** dan panel **Buat Cepat** | Per default, nilai ini berasal dari bidang **Unit waktu** pada header daftar harga biaya. Nilai ini tidak dapat ditimpa. Misalnya, pengembang dari fabrikam India berbiaya 1000 INR per **hari India**. Pengembang dari Fabrikam USA berbiaya 150 USD per **Hari AS**. | Sistem menggunakan sistem unit dan konversi di unit dasar untuk menghitung biaya per unit guna menghitung harga per unit pada estimasi masuk atau baris aktual. Misalnya, estimasi adalah untuk 10 **hari India** senilai pekerjaan untuk pengembang dari India, dan unit, **hari India** didefinisikan sebagai 10 jam. Ketika menetapkan biaya baris estimasi itu, aplikasi menghitung biaya unit pada perkiraan sebagai: 1000 INR / 10 jam = 100 INR per jam yang dikonversi menjadi USD dan ditampilkan sebagai biaya unit pada halaman **Estimasi Proyek**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Transfer harga dan biaya untuk sumber daya di luar divisi atau badan hukum Anda

Di perusahaan berbasis proyek, umum untuk menggunakan karyawan dari berbagai entitas hukum dan divisi untuk mengerjakan proyek. Proyek dapat dijalankan oleh satu entitas hukum, tetapi karyawan atau konsultan yang bekerja pada proyek dapat berasal dari entitas hukum dan divisi yang sama atau dari yang berbeda, atau mungkin kombinasinya. Dalam Dynamics 365 Project Operations, entitas hukum yang bertanggung jawab atas pelaksanaan proyek adalah **Perusahaan Pemilik** dan divisi yang bertanggung jawab atas pelaksanaannya adalah **Unit Kontrak**. Badan hukum lain yang menyediakan sumber daya disebut **perusahaan sumber daya** dan divisi yang menyediakan sumber daya disebut **unit sumber daya**. Di sebagian besar negara, perusahaan diharuskan untuk memastikan bahwa badan hukum atau divisi sumber daya membebankan biaya kepada perusahaan pemilik dan unit kontrak untuk penggunaan sumber daya.

Misalnya, perusahaan Fabrikam harus memastikan bahwa Fabrikam India-Robotika memiliki kartu tarif biaya hasil negosiasi dengan Fabrikam US-Robotics atau Fabrikam UK-Robotics.

Seorang pengembang dari Fabrikam India-Robotic berbiaya $100 ketika dipinjamkan ke Fabrikam US-Robotics dan $150 ketika dipinjamkan ke Fabrikam UK-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Menyiapkan biaya untuk sumber daya luar

1. Buat daftar harga biaya yang disebut, *Tarif biaya Fabrikam AS-Robotika* dan tetapkan rentang efektif tanggal.
2. Dalam daftar harga biaya, siapkan tarif menggunakan informasi dari tabel berikut. 

| Peran | Perusahaan Sumber Daya | Unit Sumber Daya | Tarif biaya |
| --- | --- | --- | --- |
| Pengembang | Fabrikam India | Fabrikam India-Robotika | $100 |
| Pengembang | Fabrikam Filipina | Fabrikam Filipina-Robotika | $90 |
| Pengembang | Fabrikam AS | Fabrikam AS-Robotika | $150 |

3. Lampirkan daftar harga biaya ini ke unit organisasi Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Siapkan harga transfer untuk sumber daya dalam mata uang yang sesuai 

Dalam Project Operations, harga sumber daya dapat diatur dalam mata uang apa pun. Mata uang di-default ke apa yang ada di header daftar harga, tetapi dapat diubah.

Menggunakan contoh untuk pengaturan harga transfer, informasi dapat diubah menjadi:

Perusahaan Fabrikam harus memastikan bahwa Fabrikam India-Robotika memiliki tarif biaya hasil negosiasi dengan Fabrikam US-Robotics atau Fabrikam UK-Robotics.

Seorang pengembang dari Fabrikam India-Robotic berbiaya 5000 INR ketika dipinjamkan ke Fabrikam US-Robotics dan 5500 INR ketika dipinjamkan ke Fabrikam UK-Robotics.

Dalam daftar harga biaya untuk Fabrikam US-Robotics, tarif biaya dapat dinyatakan sebagai:

| Peran | Perusahaan Sumber Daya | Biaya |
| --- | --- | --- |
| Pengembang | Fabrikam India | 5000 INR |
| Pengembang | Fabrikam AS | 115 USD |

Dalam daftar harga biaya untuk Fabrikam UK-Robotics, tarif biaya dapat dinyatakan berikut ini:

| Peran | Perusahaan Pencari Sumber Daya | Biaya |
| --- | --- | --- |
| Pengembang | Fabrikam India | 5500 INR |
| Pengembang | Fabrikam UK | 115 GBP |

Daftar harga biaya dapat memberikan tarif tenaga kerja dalam beberapa mata uang. Saat menghasilkan estimasi biaya pada proyek, Project Operations akan mengonversi tarif biaya ini ke dalam mata uang proyek, dan menampilkannya kepada pengguna. Ketika entri waktu disetujui dan biaya aktual dibuat, biaya aktual dihargai dalam mata uang dari baris harga peran yang cocok pada daftar harga biaya. Biaya aktual untuk waktu pada satu proyek dapat dicatat dalam beberapa mata uang. Namun, ketika mengakumulasikan atau meringkas biaya tenaga kerja aktual di tingkat proyek, Project Operations akan mengonversi semua jumlah biaya tenaga kerja ke dalam mata uang proyek, yang dapat dilihat pengguna.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
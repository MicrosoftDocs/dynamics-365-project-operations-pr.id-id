---
title: Mengonfigurasikan tarif tagihan tenaga kerja
description: Topik ini memberikan informasi tentang cara mengatur tarif tagihan tenaga kerja di Project Operations.
author: rumant
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f0267fce673bbd0080022a8abf2dd0020cc8b662
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877404"
---
# <a name="set-up-labor-bill-rates"></a>Mengonfigurasikan tarif tagihan tenaga kerja

**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok

Setiap daftar harga memiliki seperangkat harga peran, atau tarif tenaga kerja, yang efektif untuk konteks dan efektivitas tanggal yang disertakan pada header daftar harga. Tingkat tagihan untuk waktu di Dynamics 365 Project Operations dapat diatur dalam hanya satu mata uang, yang merupakan mata uang pada header Daftar harga.

1. Untuk mengkonfigurasi tingkat tagihan tenaga kerja untuk daftar harga penjualan, buka **Penjualan** > **Pelanggan** > **Daftar Harga**, dan pilih **Baru** untuk membuat daftar harga baru. 
2. Pada tab **harga peran**, di subkisi, pilih **harga peran baru**. 
3. Pada panel **buat cepat**, masukkan peran dan kombinasi unit organisasi yang harus Anda konfigurasikan tarif tagihannya.

   Tabel berikut mencantumkan bidang pada tab **Umum** dan panel **Buat cepat** dari baris harga peran yang harus diingat saat Anda membuat harga peran pada daftar harga penjualan:

    | Bidang | Lokasi | KETERANGAN | Dampak hilir |
    | --- | --- | --- | --- |
    | Peran | Tab **Umum** dan panel **Buat Cepat** | Pilih peran yang Anda tetapkan tarif tagihannya. | Peran pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke tarif tagihan default peran. |
    | Perusahaan Sumber Daya | Tab **Umum** dan panel **Buat Cepat** | Pilih perusahaan atau entitas hukum yang menjadi asal perannya. Misalnya, pengembang dari Fabrikam India atau pengembang dari Fabrikam AS. | Perusahaan sumber daya pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke tarif tagihan default peran. |
    | Unit Sumber Daya | Tab **Umum** dan panel **Buat Cepat** | Pilih unit organisasi atau divisi dari perusahaan yang mana peran berasal darinya. Misalnya, pengembang dari divisi Robotika Fabrikam India atau pengembang dari divisi perangkat lunak Fabrikam AS. | Unit sumber daya pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke tarif tagihan default peran. |
    | Harga | Tab **Umum** dan panel **Buat Cepat** | Mengatur tarif tagihan untuk perusahaan sumber daya peran dan kombinasi unit sumber daya. Contohnya, pengembang dari fabrikam India memiliki tarif tagihan 100 USD atau pengembang dari fabrikam USA memiliki tarif tagihan 150 USD. | Harga ini adalah tarif tagihan default pada harga per unit baris aktual atau estimasi masuk untuk kelas transaksi pengeluaran waktu. |
    | Mata uang | Tab **Umum** dan panel **Buat Cepat**| Secara default, nilai mata uang ini berasal dari mata uang pada header daftar harga penjualan. Pada daftar harga penjualan, mata uang tidak dapat ditimpa. | Mata uang ini adalah mata uang default pada harga per unit baris penjualan aktual masuk untuk kelas transaksi waktu. |
    | Jadwal Unit | Tab **Umum** dan panel **Buat Cepat** | Jadwal unit di-default ke waktu dan tidak dapat diubah pada entitas harga peran karena digunakan untuk mengekspresikan tarif berdasarkan satuan waktu. | Tidak ada dampak hilir untuk bidang ini. |
    | Unit | Tab **Umum** dan panel **Buat Cepat** | Nilai unit berasal dari bidang **Unit waktu** pada header daftar harga penjualan. Tetapi Nilai ini tidak dapat ditimpa. Misalnya, pengembang dari fabrikam India memiliki nilai tagihan 1000 USD per **hari India**. Pengembang dari fabrikam USA memiliki tingkat tagihan 1500 USD per **hari AS**. | Bila harga per unit di-default pada perkiraan masuk atau baris aktual, sistem menggunakan sistem unit dan konversi di unit dasar untuk menghitung harga per unit. Misalnya, estimasi adalah untuk 10 **hari India** senilai pekerjaan untuk pengembang dari India, dan hari unit India didefinisikan sebagai 10 jam. Saat menetapkan harga untuk baris estimasi itu, aplikasi menghitung harga unit pada estimasi sebagai 1000 USD/10 jam = 100 USD per jam. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Mentransfer harga atau mengatur tarif tagihan untuk sumber daya dari unit organisasi atau divisi lain 

Perusahaan berbasis proyek sering menggunakan karyawan dari berbagai badan hukum dan divisi yang berbeda dalam badan hukum untuk mengerjakan proyek. Proyek dapat dijalankan dari entitas hukum dan divisi tertentu sementara karyawan atau konsultan yang bekerja pada proyek dapat berasal dari entitas hukum dan divisi yang sama atau dari yang berbeda. Proyek juga dapat terdiri dari kombinasi dari orang-orang dari berbagai badan hukum dan divisi. Dalam Project Operations, entitas hukum yang memiliki proyek yang dilaksanakan disebut **perusahaan pemilik**, dan divisi yang bertanggung jawab atas pelaksanaan disebut **unit kontrak**. Semua badan hukum lain yang menyediakan sumber daya disebut **perusahaan sumber daya** dan divisi yang menyediakan sumber daya disebut **unit sumber daya**. Karena perbedaan dalam biaya tenaga kerja di berbagai geografi dan pasar tenaga kerja di seluruh dunia, tarif untuk tenaga kerja juga diatur berbeda untuk geografi yang berbeda.

Contohnya, seorang pengembang dari Divisi Robotika fabrikam India yang bekerja pada proyek AS ditagih pada tingkat 100 USD per jam. Seorang pengembang dari Divisi Robotika fabrikam AS yang bekerja pada proyek AS ditagih pada tingkat 150 USD per jam. 

### <a name="example-set-up-a-bill-rate"></a>Contoh: mengkonfigurasi tarif tagihan 

1. Buat daftar harga penjualan yang disebut *tarif tagihan fabrikam AS* dan atur efektivitas tanggal.
2. Dalam daftar harga penjualan, masukkan informasi tarif berikut:

    | Peran | Perusahaan Pencari Sumber Daya | Unit sumber daya | Tarif tagihan |
    | --- | --- | --- | --- |
    | Pengembang | Fabrikam India | Fabrikam India-Robotika | $100 |
    | Pengembang | Fabrikam Filipina | Fabrikam Filipina-Robotika | $90 |
    | Pengembang | Fabrikam AS | Fabrikam AS-Robotika | $150 |

3. Lampirkan daftar harga penjualan, **tarif tagihan Fabrikam AS** ke daftar harga proyek dari kontrak proyek atau ke akun tertentu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

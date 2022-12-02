---
title: Mengonfigurasikan tarif tagihan tenaga kerja - lite
description: Artikel ini memberikan informasi tentang cara mengatur tarif tagihan tenaga kerja di Project Operations.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 443132797f20c961b42ed20340e74f420965526f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917442"
---
# <a name="set-up-labor-bill-rates---lite"></a>Mengonfigurasikan tarif tagihan tenaga kerja - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Setiap daftar harga memiliki seperangkat harga peran, atau tarif tenaga kerja, yang efektif untuk konteks dan efektivitas tanggal yang disertakan pada header daftar harga. Tingkat tagihan untuk waktu di Dynamics 365 Project Operations dapat diatur dalam hanya satu mata uang, yang merupakan mata uang pada header Daftar harga.

1. Untuk mengkonfigurasikan tarif tagihan tenaga kerja untuk daftar harga penjualan, buat daftar harga berdasarkan header daftar harga. 
2. Pada tab **harga peran**, di subkisi, pilih **+ harga peran baru**. 
3. Pada panel **buat cepat**, masukkan peran dan kombinasi unit organisasi yang harus Anda konfigurasikan tarif tagihannya.

  Tabel berikut mencantumkan bidang pada tab **Umum** dan panel **Buat cepat** dari baris harga peran yang harus diingat saat Anda membuat harga peran pada daftar harga penjualan:

  | Bidang | Lokasi | KETERANGAN | Dampak hilir |
  | --- | --- | --- | --- |
  | Peran | Tab **Umum** dan panel **Buat Cepat** | Pilih peran yang Anda tetapkan tarif tagihannya. | Peran pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke tarif tagihan default peran. |
  | Unit Sumber Daya | Tab **Umum** dan panel **Buat Cepat** | Pilih unit organisasi atau divisi dari perusahaan yang mana peran berasal darinya. Misalnya, pengembang dari divisi Robotika Fabrikam India atau pengembang dari divisi perangkat lunak Fabrikam AS. | Unit sumber daya pada estimasi masuk atau aktual akan disesuaikan dengan baris ini ke tarif tagihan default peran. |
  | Harga | Tab **Umum** dan panel **Buat Cepat** | Mengatur tarif tagihan untuk perusahaan sumber daya peran dan kombinasi unit sumber daya. Contohnya, pengembang dari fabrikam India memiliki tarif tagihan 100 USD atau pengembang dari fabrikam USA memiliki tarif tagihan 150 USD. | Harga ini adalah tarif tagihan default pada harga per unit baris aktual atau estimasi masuk untuk kelas transaksi pengeluaran waktu. |
  | Mata uang | Tab **Umum** dan panel **Buat Cepat**| Secara default, nilai mata uang ini berasal dari mata uang pada header daftar harga penjualan. Pada daftar harga penjualan, mata uang tidak dapat ditimpa. | Mata uang ini adalah mata uang default pada harga per unit baris penjualan aktual masuk untuk kelas transaksi waktu. |
  | Jadwal Unit | Tab **Umum** dan panel **Buat Cepat** | Jadwal unit di-default ke waktu dan tidak dapat diubah pada entitas harga peran karena digunakan untuk mengekspresikan tarif berdasarkan satuan waktu. | Tidak ada dampak hilir untuk bidang ini. |
  | Unit | Tab **Umum** dan panel **Buat Cepat** | Nilai unit berasal dari bidang **Unit waktu** pada header daftar harga penjualan. Tetapi Nilai ini tidak dapat ditimpa. Misalnya, pengembang dari fabrikam India memiliki nilai tagihan 1000 USD per **hari India**. Pengembang dari fabrikam USA memiliki tingkat tagihan 1500 USD per **hari AS**. | Bila harga per unit di-default pada perkiraan masuk atau baris aktual, sistem menggunakan sistem unit dan konversi di unit dasar untuk menghitung harga per unit. Misalnya, estimasi adalah untuk 10 **hari India** senilai pekerjaan untuk pengembang dari India, dan hari unit India didefinisikan sebagai 10 jam. Saat menetapkan harga untuk baris estimasi itu, aplikasi menghitung harga unit pada estimasi sebagai 1000 USD/10 jam = 100 USD per jam. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Mentransfer harga atau mengatur tarif tagihan untuk sumber daya dari unit organisasi atau divisi lain 

Perusahaan berbasis proyek untuk menggunakan karyawan dari berbagai divisi perusahaan untuk mengerjakan proyek. Proyek dapat dieksekusi dari satu divisi sementara karyawan atau konsultan berasal dari divisi perusahaan yang berbeda. Proyek juga dapat terdiri dari kombinasi dari orang-orang dari divisi berbeda. Dalam Project Operations, perusahaan yang bertanggung jawab atas pelaksanaan proyek disebut **Unit Kontrak**. Semua divisi lain yang menyediakan sumber daya disebut **Unit Sumber daya**. Karena perbedaan dalam biaya tenaga kerja di berbagai geografi dan pasar tenaga kerja di seluruh dunia, tarif untuk tenaga kerja juga diatur berbeda untuk geografi yang berbeda.

Contohnya, seorang pengembang dari Fabrikam India yang bekerja pada proyek AS ditagih pada tingkat 100 USD per jam. Seorang pengembang dari Fabrikam AS yang bekerja pada proyek AS ditagih pada tingkat 150 USD per jam.

### <a name="example-set-up-a-bill-rate"></a>Contoh: mengkonfigurasi tarif tagihan

1. Buat daftar harga penjualan yang disebut *tarif tagihan fabrikam AS* dan atur efektivitas tanggal.
2. Dalam daftar harga penjualan, masukkan informasi tarif berikut:

    | Peran | Unit Organisasi | Tarif tagihan |
    | --- | --- | --- |
    | Pengembang | Fabrikam India | $100 |
    | Pengembang | Fabrikam Filipina | $90 |
    | Pengembang | Fabrikam AS | $150 |

3. Lampirkan daftar harga penjualan, **tarif tagihan Fabrikam AS** ke daftar harga proyek dari kontrak proyek atau ke akun tertentu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
---
title: Penimpaan harga tanggal berlaku
description: Artikel ini menjelaskan cara mengatur penimpaan harga untuk harga tertentu dalam daftar harga.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 41af5176c0809c9621fc0fa946a04492da7d152b
ms.sourcegitcommit: 37293b0b28f072deafc00112ddbbea91c48a7802
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/08/2022
ms.locfileid: "9446003"
---
# <a name="date-effective-price-overrides"></a>Penimpaan harga tanggal berlaku 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

*Penimpaan harga tanggal berlaku* memberikan cara menimpa atau mengubah harga tertentu dalam daftar harga. Misalnya, Anda memiliki daftar harga standar yang berlaku mulai 1 Januari 2022 hingga 31 Desember 2022. Daftar harga ini memiliki harga untuk berbagai peran. Harga yang diatur untuk peran **Teknisi Jaringan** adalah 100 US dolar (USD) per jam. Bila teknisi jaringan mencatat waktu antara 1 Januari 2022 hingga 31 Desember 2022, waktu akan ditentukan sebesar 100 USD. Pada tanggal 1 Oktober 2022, Anda harus menyesuaikan harga *hanya* untuk peran **Teknisi Jaringan**, dari 100 USD per jam menjadi 110 USD per jam. Fitur **Penimpaan harga tanggal berlaku** memungkinkan Anda mengatur perubahan ini sebagai menimpa baris untuk harga peran tertentu tersebut. Karenanya, Anda tidak perlu menyalin seluruh daftar harga dan mengubah harga hanya pada satu baris itu saja.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Penimpaan harga tanggal berlaku untuk harga tenaga kerja

Proses pengaturan penimpaan harga tanggal berlaku untuk waktu tenaga kerja pada proyek terdiri dari dua langkah dasar.

1. Aktifkan fitur **Penimpaan harga tanggal berlaku**.
1. Mengatur penimpaan harga tanggal berlaku.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Aktifkan fitur Penimpaan harga tanggal berlaku

> [!NOTE]
> Setelah fitur **Tanggal berlaku penimpaan harga** diaktifkan, fitur tidak dapat dinonaktifkan.

Untuk mengaktifkan fitur **Penimpaan harga tanggal berlaku,** ikuti langkah-langkah ini.

1. Buka **Pengaturan** \> **Parameter**.
1. Buka rekaman **parameter**.
1. Pada Panel Tindakan, pada tab **Kontrol Fitur**, pilih **Aktifkan penimpaan harga tanggal berlaku**.
1. Pilih **OK** di kotak dialog konfirmasi.
1. Setelah beberapa saat, refresh browser Anda. Kemampuan penimpaan harga tanggal berlaku harus tersedia sekarang. Anda akan mengetahui bahwa kemampuan ini telah diaktifkan jika tombol **Aktifkan penimpaan harga tanggal berlaku** tidak muncul lagi di Panel Tindakan.

### <a name="set-up-a-date-effective-price-override"></a>Mengatur penimpaan harga tanggal berlaku

Penimpaan harga tanggal berlaku bisa diatur di **Biaya**, **Penjualan**, atau daftar harga **Penjualan**.

> [!NOTE]
>Aktivitas **Penimpaan harga tanggal berlaku** saat ini memiliki batasan berikut:
>
> - Hanya harga peran dan markup harga peran yang mendukung fitur **Penimpaan harga tanggal berlaku** di Project Operations.
> - Bila Anda menyalin daftar harga menggunakan tindakan **Salin** pada halaman **Rincian daftar harga** dan ketika Anda membuat daftar harga proyek dari daftar harga standar atau kustom selama pembuatan kontrak, penimpaan harga tanggal berlaku **tidak** tidak disalin dari daftar harga sumber.

Untuk menyiapkan penggantian harga efektif tanggal untuk harga peran atau markup harga peran, ikuti langkah-langkah berikut.

1. Buka halaman untuk daftar harga yang akan ditimpa harga mulai berlaku.
1. Pilih tab **Harga peran**. Tab ini mendaftar semua rekaman **Harga peran** dalam daftar harga.
1. Pilih rekaman **Harga peran** yang ingin Anda atur penimpaan harga tanggal berlaku baru untuk, kemudian ketuk dua kali (atau klik dua kali) **Harga peran** untuk membuka halaman **Rincian harga peran**.
1. Pilih tab **Penimpaan tanggal berlaku**. Kisi pada tab ini mendaftar semua penimpaan harga tanggal berlaku untuk rekaman **Harga peran** yang dipilih.
1. Di toolbar di atas kisi, pilih **Penimpaan harga peran baru**. Geser **Penimpaan harga peran baru** terbuka.
1. Tentukan awal tanggal berlaku, unit, dan harga baru untuk menimpa harga. Lalu pilih **Simpan** lalu tutup formulir.

> [!NOTE]
> - Penimpaan harga tanggal berlaku untuk harga peran atau markup harga peran diterapkan untuk kombinasi nilai dimensi harga yang sama yang ada pada **Harga peran** induk atau baris **Markup harga peran**.
> - Tanggal yang dipilih dalam bidang **Berlaku mulai** harus dalam tanggal berlaku dari daftar harga induk. Penimpaan harga akan berlaku di tanggal yang dipilih dalam bidang **Berlaku dari** dan akan diterapake hingga akhir dari tanggal berakhir daftar harga induk. Jika Anda menyiapkan penimpaan harga tanggal berlaku lain untuk harga peran yang sama, penimpaan harga pertama akan berlaku pada tanggal yang dipilih dalam bidang **Berlaku dari** dan akan diterapkan hingga awal penimpaan kedua.

## <a name="examples"></a>Contoh

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Contoh 1: Menentukan tanggal berlaku untuk harga peran yang mengalami penimpaan harga peran

Contoh berikut menunjukkan penetapan tanggal berlaku untuk harga peran tertentu yang menimpa harga peran.

**Daftar harga A: 1 Januari hingga 30 Juni**

*Harga peran*

| Harga peran | Unit | Harga | Berlaku pada harga untuk transaksi masuk |
|---|---|---|---|
| Teknisi Jaringan | Jam | 100 | Harga ini akan digunakan pada setiap transaksi dengan tanggal transaksi antara 1 Januari hingga 14 Maret. |

*Penimpaan harga peran*

| Berlaku mulai | Unit | Harga | Berlaku pada harga untuk transaksi masuk |
|---|---|---|---|
| Maret 15 | Jam | 110 | Harga ini akan digunakan pada setiap transaksi dengan tanggal transaksi antara 15 Maret hingga 30 Maret. |
| April 1 | Jam | 120 | Harga ini akan digunakan pada setiap transaksi dengan tanggal transaksi antara 1 April hingga 30 Juni. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Contoh 2: Menentukan berlakunya tanggal untuk markup harga peran yang memiliki penimpaan markup harga peran

Contoh berikut menunjukkan bagaimana tanggal berlaku ditentukan untuk markup harga peran tertentu yang diatur untuk penimpaan markup harga peran.

**Daftar harga A: 1 Januari hingga 30 Juni**

*Harga peran*

| Harga peran | Jam kerja | Unit | Harga | Berlaku pada harga untuk transaksi masuk |
|---|---|---|---|---|
| Teknisi jaringan | Reguler | Jam | 100 | Harga ini akan digunakan pada setiap transaksi dengan tanggal transaksi antara 1 Januari hingga 14 Maret. |

*Markup harga peran*

| Unit organisasi | Jam kerja | Mark up % |
|---|---|---|
| Contoso AS | Lembur | 10% |

*Penimpaan markup harga peran*

| Berlaku mulai | Harga | Berlaku pada harga untuk transaksi masuk |
|---|---|---|
| Maret 15 | 20% | Persen markup akan digunakan pada setiap transaksi dengan tanggal transaksi antara 15 Maret hingga 30 Maret. |
| April 1 | 25% | Markup ini akan digunakan pada setiap transaksi dengan tanggal transaksi antara 1 April hingga 30 Juni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

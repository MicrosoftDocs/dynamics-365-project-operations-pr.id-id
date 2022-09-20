---
title: Penggantian harga efektif tanggal
description: Artikel ini menjelaskan cara mengatur penggantian harga untuk harga tertentu dalam daftar harga.
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
# <a name="date-effective-price-overrides"></a>Penggantian harga efektif tanggal 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

*Penggantian harga efektif tanggal* memberikan cara untuk mengganti atau mengubah harga tertentu dalam daftar harga. Misalnya, Anda memiliki daftar harga standar yang berlaku mulai 1 Januari 2022 hingga 31 Desember 2022. Daftar harga ini memiliki harga untuk banyak peran. Harga yang ditetapkan untuk **peran Teknisi** Jaringan adalah 100 dolar AS (USD) per jam. Saat teknisi jaringan mencatat waktu antara 1 Januari 2022 dan 31 Desember 2022, waktu tersebut dihargai 100 USD. Pada tanggal 1 Oktober 2022, Anda harus menyesuaikan harga *hanya* untuk **peran Teknisi** Jaringan, dari 100 USD per jam hingga 110 USD per jam. Fitur **Penggantian** harga efektif tanggal memungkinkan Anda mengatur perubahan ini sebagai penggantian baris untuk harga peran tertentu. Oleh karena itu, Anda tidak perlu menyalin seluruh daftar harga dan mengubah harga hanya satu baris itu.

## <a name="date-effective-price-overrides-for-labor-pricing"></a>Penggantian harga efektif tanggal untuk harga tenaga kerja

Proses pengaturan penggantian harga efektif tanggal untuk waktu tenaga kerja pada suatu proyek terdiri dari dua langkah dasar.

1. Aktifkan **tanggal efektif harga menimpa** fitur.
1. Siapkan penggantian harga efektif tanggal.

### <a name="enable-the-date-effective-price-overrides-feature"></a>Aktifkan fitur penggantian harga efektif Tanggal

> [!NOTE]
> Setelah fitur Penggantian **harga efektif Tanggal diaktifkan, fitur tersebut** tidak dapat dinonaktifkan.

Untuk mengaktifkan **fitur Penggantian** harga efektif tanggal, ikuti langkah-langkah berikut.

1. Buka **Parameter** Pengaturan \>**·**.
1. Buka **catatan Parameter**.
1. Pada Panel Tindakan, pada tab **Kontrol** Fitur, pilih **Aktifkan penggantian** harga efektif tanggal.
1. Pilih **OK** di kotak dialog konfirmasi.
1. Setelah beberapa saat, segarkan browser Anda. Kemampuan penggantian harga efektif tanggal sekarang harus tersedia. Anda akan tahu bahwa kemampuan ini telah diaktifkan jika **Aktifkan penggantian** harga efektif tanggal tidak lagi muncul di Panel Tindakan.

### <a name="set-up-a-date-effective-price-override"></a>Menyiapkan penggantian harga efektif tanggal

Penggantian harga efektif tanggal dapat diatur pada **daftar harga Biaya**, **Penjualan**, atau **Pembelian**.

> [!NOTE]
>Perilaku **penggantian harga** efektif Tanggal saat ini memiliki batasan berikut:
>
> - Hanya harga peran dan markup harga peran yang **mendukung fitur penggantian** harga efektif Tanggal dalam Operasi Proyek.
> - Saat Anda menyalin daftar harga dengan menggunakan **tindakan Salin** pada **halaman detail** Daftar Harga, dan saat Anda membuat daftar harga proyek dari daftar harga standar atau kustom selama pembuatan kontrak, penggantian **harga efektif tanggal tidak** disalin dari daftar harga sumber.

Untuk menyiapkan penggantian harga efektif tanggal untuk harga peran atau markup harga peran, ikuti langkah-langkah berikut.

1. Buka halaman untuk daftar harga yang ingin Anda atur untuk penggantian harga efektif tanggal.
1. Pilih tab **Harga** peran. Tab ini mencantumkan semua **catatan harga** Peran dalam daftar harga.
1. **Pilih Catatan harga** peran yang ingin Anda siapkan untuk harga penggantian efektif tanggal baru, lalu ketuk dua kali (atau klik dua kali) **Harga** peran untuk membuka **halaman Detail** harga peran.
1. Pilih tab **Tanggal efektif penggantian**. Kisi pada tab ini mencantumkan semua penggantian harga efektif tanggal untuk catatan harga **Peran yang** dipilih.
1. Pada toolbar di atas kisi, pilih **Penggantian harga peran baru**. Penggeser **Penggantian** harga peran baru terbuka.
1. Tentukan tanggal efektif-dari, unit, dan harga baru untuk penggantian harga. Kemudian pilih **Simpan**, dan tutup formulir.

> [!NOTE]
> - Penggantian harga efektif tanggal untuk harga peran atau markup harga peran berlaku untuk kombinasi nilai dimensi harga yang sama yang ada pada baris Harga peran induk **atau** Markup **harga** peran.
> - Tanggal yang dipilih di **bidang Efektif dari** harus berada dalam tanggal efektif daftar harga induk. Penggantian harga akan berlaku pada tanggal yang dipilih di **bidang Efektif dari** dan akan berlaku hingga akhir tanggal akhir daftar harga induk. Jika Anda mengatur penggantian harga efektif tanggal lain untuk harga peran yang sama, penggantian harga pertama akan berlaku pada tanggal yang dipilih di **bidang Efektif dari** dan akan berlaku hingga dimulainya penggantian kedua.

## <a name="examples"></a>Contoh

### <a name="example-1-determining-date-effectivity-for-a-role-price-that-has-role-price-overrides"></a>Contoh 1: Menentukan efektivitas tanggal untuk harga peran yang memiliki perubahan harga peran

Contoh berikut menunjukkan bagaimana efektivitas tanggal ditentukan untuk harga peran tertentu yang ditetapkan untuk penggantian harga peran.

**Daftar harga A: 1 Januari hingga 30 Juni**

*Harga peran*

| Harga peran | Unit | Harga | Efek pada harga untuk transaksi masuk |
|---|---|---|---|
| Teknisi Jaringan | Jam | 100 | Harga ini akan digunakan pada setiap transaksi di mana tanggal transaksi antara 1 Januari dan 14 Maret. |

*Penggantian harga peran*

| Efektif dari | Unit | Harga | Efek pada harga untuk transaksi masuk |
|---|---|---|---|
| Maret 15 | Jam | 110 | Harga ini akan digunakan pada setiap transaksi di mana tanggal transaksi antara 15 Maret dan 30 Maret. |
| April 1 | Jam | 120 | Harga ini akan digunakan pada setiap transaksi di mana tanggal transaksi antara 1 April dan 30 Juni. |

### <a name="example-2-determining-date-effectivity-for-a-role-price-markup-that-has-role-price-markup-overrides"></a>Contoh 2: Menentukan efektivitas tanggal untuk markup harga peran yang memiliki markup harga peran diganti

Contoh berikut menunjukkan bagaimana efektivitas tanggal ditentukan untuk markup harga peran tertentu yang disiapkan untuk penggantian markup harga peran.

**Daftar harga A: 1 Januari hingga 30 Juni**

*Harga peran*

| Harga peran | Jam kerja | Unit | Harga | Efek pada harga untuk transaksi masuk |
|---|---|---|---|---|
| Teknisi jaringan | Reguler | Jam | 100 | Harga ini akan digunakan pada setiap transaksi di mana tanggal transaksi antara 1 Januari dan 14 Maret. |

*Markup harga peran*

| Unit organisasi | Jam kerja | Tandai % |
|---|---|---|
| Contoso AS | Lembur | 10% |

*Penggantian markup harga peran*

| Efektif dari | Harga | Efek pada harga untuk transaksi masuk |
|---|---|---|
| Maret 15 | 20% | Persentase markup ini akan digunakan pada setiap transaksi di mana tanggal transaksi antara 15 Maret dan 30 Maret. |
| April 1 | 25% | Markup ini akan digunakan pada setiap transaksi di mana tanggal transaksi antara 1 April dan 30 Juni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]

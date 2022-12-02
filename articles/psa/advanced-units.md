---
title: Grup unit dan unit
description: Artikel ini menyediakan informasi tentang grup unit dan unit.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ed413cc927901308a111263dbad1a59af8fce620
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933404"
---
# <a name="unit-groups-and-units"></a>Grup unit dan unit

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Grup unit dan unit adalah entitas dasar di Microsoft Dynamics 365. Unit adalah satuan ukuran tunggal, dan beberapa unit dapat dikelompokkan ke dalam grup unit. Grup unit terkadang disebut sebagai jadwal unit di antarmuka pengguna Dynamics 365 (UI). 

Berikut adalah beberapa contoh unit dan grup unit:
 
- **grup unit**: Jarak 
    - **Unit**: mil, kilometer, dan sebagainya.
- **grup unit**: waktu
    - **Unit**: jam, hari, Minggu, dan sebagainya. 

Bila Anda mengkonfigurasi beberapa unit di grup unit, Anda juga harus menyiapkan faktor konversi di antara keduanya dengan menunjuk unit pertama yang Anda konfigurasikan sebagai unit default atau utama untuk grup unit. 

Misalnya, di grup unit **waktu**, jika Anda mengatur **jam** sebagai unit pertama, sistem akan menunjukkan **jam** sebagai unit default. Jika unit berikutnya yang Anda konfigurasikan adalah **hari**, Anda harus mengkonfigurasi faktor konversi untuk **hari** ke **jam**. Jika **Anda menambahkan minggu** sebagai unit ketiga, Anda harus mengkonfigurasi faktor konversi untuk **minggu** dalam hal **hari** atau **jam**. 

Gambar berikut menunjukkan contoh konfigurasi untuk unit **hari**, dengan bidang **kuantitas** menampilkan jumlah jam yang berada dalam satu hari, dan **minggu**, dengan bidang **kuantitas** menampilkan jumlah hari dalam seminggu.

> ![Grup unit: Halaman informasi.](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Menggunakan grup unit dan unit

Dynamics 365 Project Service Automation menggunakan unit dan grup unit untuk memproses perkiraan dan entri untuk biaya dan waktu. 

Untuk pengeluaran, setiap kategori pengeluaran memiliki unit dan grup unit default. Nilai ini dimasukkan sebagai nilai default pada entri daftar harga untuk kategori pengeluaran. 

Misalnya, Anda memiliki kategori pengeluaran yang diberi nama **jarak tempuh**. Ia memiliki grup unit yang diberi nama **jarak** dan unit default bernama **Mil**. Jika Anda mengkonfigurasi grup unit **jarak** sehingga memiliki dua unit (**Mil** dan **kilometer**), Anda dapat menetapkan dua harga untuk kategori **jarak tempuh** pada satu daftar harga: harga per mil dan harga per kilometer.

| Kategori Pengeluaran  | Grup Unit  | Unit      | Metode Penetapan Harga  | Harga per unit  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Jarak Tempuh           | Jarak      | Mil      | Harga per unit    | 10 USD            |
| Jarak Tempuh           | Jarak      | Kilometer | Harga per unit    |  6 USD            |

Bila Anda memasukkan pengeluaran pada suatu proyek, sistem akan menentukan harga melalui kombinasi kategori dan unit pada biaya. 

| Deskripsi pengeluaran        | Kategori Pengeluaran  | Unit  | Kuantitas  | Harga per Unit   |
|----------------------------|---------------------|-------|-----------|----------------|
| Berkendara ke lokasi klien | Jarak Tempuh             | Mil  | 10        | 10 USD         |

Untuk waktu, setiap header daftar harga memiliki bidang **unit waktu default**. Nilai diatur saat Anda membuat header daftar harga. Unit ini kemudian digunakan untuk mengatur semua harga berdasarkan peran pada daftar harga tersebut.

Baris perkiraan untuk bidang **waktu pada kuotasi** dapat dinyatakan dalam satuan waktu. Namun, perkirakan baris pada entri proyek dan waktu untuk proyek hanya dapat menggunakan satuan waktu **jam**. Jika unit pada baris entri waktu atau perkiraan tidak sesuai dengan unit pada baris daftar harga untuk peran tersebut, sistem akan mengkonversi harga ke unit yang ditentukan dalam perkiraan proyek atau transaksi aktual proyek.

Contoh berikut menunjukkan cara PSA menggunakan grup unit, unit, dan faktor konversi.
- Unit

   - **grup unit**: waktu 
   - **Unit**: jam 
    
    - **hari** – Faktor konversi: 8 jam       
    - **Minggu** – Faktor konversi: 40 jam  
        
- Konfigurasi daftar harga pada proyek A:

    - **Nama**: harga penjualan UK 2016 
    - **Unit waktu default**: hari 
    - **Mata Uang**: GBP

| Peran      | Grup Unit | Unit | Unit Organisasi | Harga   |
|-----------|------------|------|---------------------|---------|
| Pengembang | Time       | Day  | Aswono AS          | 800 GBP |

### <a name="time-entry"></a>Entri Waktu

Tabel berikut Menampilkan hasil transaksi penjualan yang dibuat oleh PSA selama proyek tiga jam.


| Proyek   | Tugas    | Peran      | Kuantitas | Unit  | Harga per Unit | Jumlah Penjualan Tak Tertagih |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| Proyek A | Rancang  | Pengembang | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>Tanya-Jawab unit Waktu

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Apakah PSA dikonversi ke unit yang berbeda dalam kasus pengeluaran?
Tidak. Konversi unit berfungsi hanya untuk waktu. Untuk pengeluaran, jika sistem tidak dapat menemukan harga untuk kombinasi kategori pengeluaran dan unit, harga diatur ke 0,00 secara default.

### <a name="why-does-psa-convert-time-units"></a>Mengapa PSA mengkonversi unit waktu?
Di beberapa negara atau kawasan, ada persyaratan hukum yang mengatur tarif tagihan dalam hari. Negosiasi harga dan diskon selama siklus kuotasi dilakukan dengan menggunakan tarif harian untuk setiap peran yang dapat ditagih. Estimasi jadwal dan entri waktu dilakukan dalam jam. Untuk mendukung perbedaan dalam unit waktu ini, PSA mengkonversi unit waktu.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Apakah unit waktu dapat diubah pada perkiraan proyek?
Tidak. Perkiraan jadwal saat saat ini dibatasi hingga jam dan tidak dapat diubah.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Apakah unit dan grup unit dapat diedit, dihapus, dan ditambahkan?
Ya. Dengan pengecualian grup unit **waktu** dan unit **jam**, Semua unit dapat dihapus atau diedit, dan unit baru dapat ditambahkan. Dalam PSA, grup unit **waktu** dan unit **jam** tidak dapat dihapus. Namun, mereka dapat diperbarui dengan teks terjemahan untuk bidang **nama**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Konfigurasikan Papan Jadwal untuk menampilkan pekerja kontrak dan kapasitas subkontrak
description: Artikel ini menjelaskan cara mengkonfigurasi Papan Jadwal di Microsoft Dynamics 365 Project Operations untuk menunjukkan kapasitas sumber daya yang dikurangi saat mengatur persyaratan sumber daya proyek.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262220"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurasikan Papan Jadwal untuk menampilkan pekerja kontrak dan kapasitas subkontrak 

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Papan Jadwal di Microsoft Dynamics 365 Project Operations dapat digunakan untuk mencari sumber daya dengan dua cara:

- Pencarian sumber daya umum tanpa konteks persyaratan sumber daya berbasis proyek tertentu.
- Pencarian sumber daya khusus persyaratan dengan persyaratan proyek akan memberikan konteks untuk sumber daya yang disarankan.

Untuk memberitahukan papan jadwal kapasitas sumber daya subkontrak dan pekerja kontrak, Anda harus melakukan pembaruan pengaturan Papan Jadwal. Pembaruan ini antara lain: 
- Pengaturan pembaruan Papan Jadwal untuk pencarian sumber daya umum.
- Pengaturan pembaruan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Pengaturan pembaruan Papan Jadwal untuk pencarian sumber daya umum
### <a name="update-filters-for-general-resource-search"></a>Filter pembaruan untuk pencarian sumber daya umum
Saat mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua yang berikut:
  - Jenis pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
  - Perusahaan vendor yang memiliki Sumber Daya.
  - Sumber daya yang ada di baris subkontrak atau subkontrak tertentu.
    
### <a name="update-retrieve-resource-query"></a>Pembaruan mengambil Kueri sumber daya
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya umum:  
1. Buka **Pengaturan Papan Jadwal** untuk Papan Jadwal tertentu.
2. Buka tab **Pengaturan umum** dan gulir ke **Pengaturan lain**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak Filter** ke **Tata Letak Filter Default untuk Project Operations Lite**.
4. Perbarui **Ambil Kueri Sumber Daya** ke **Kueri Sumber Daya Default untuk Project Operations Lite**.

![Pengaturan pembaruan Papan Jadwal untuk pencarian sumber daya umum](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Pengaturan pembaruan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Filter pembaruan untuk pencarian sumber daya spesifik persyaratan 
Saat mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua yang berikut:
 - Jenis pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
 - Perusahaan vendor yang memiliki Sumber Daya.
 - Sumber daya yang ada di baris subkontrak atau subkontrak tertentu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Memperbarui pengambilan kueri sumber daya untuk pencarian sumber daya khusus persyaratan 
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya berbasis persyaratan:

1. Buka **Pengaturan Papan Jadwal** untuk Papan Jadwal tertentu, lalu pilih **Buka pengaturan Default** untuk membuka pengaturan untuk pencarian khusus persyaratan.
2. Buka tab **Pengaturan umum** dan gulir ke **Pengaturan lain**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak Filter** ke **Tata Letak Filter Default untuk Project Operations Lite**.
4. Perbarui **Ambil Kueri Sumber Daya** ke **Kueri Sumber Daya Default untuk Project Operations Lite**.
5. Buka tab **Jenis Jadwal**, lalu buka **Project**.
6. Dalam pengaturan untuk **Proyek**, perbarui **Asisten Jadwalkan Ambil Kueri Sumber Daya** ke **Default Ambil Kueri Sumber Daya untuk Project Operations Lite** dan perbarui **Asisten Jadwal Ambil Kueri Batasan** ke **Kueri batasan Pengambilan Default untuk Project Operations Lite**.

![Pengaturan pembaruan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

---
title: Konfigurasikan Papan Jadwal untuk menampilkan pekerja kontrak dan kapasitas subkontrak
description: Ini topik menjelaskan cara mengonfigurasi Schedule Board di Microsoft Dynamics 365 Project Operations untuk menampilkan kapasitas sumber daya subkontrak saat menangani persyaratan sumber daya proyek.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6e382b33fafe91c8b96a91d033fe12b998114bdc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587828"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurasikan Papan Jadwal untuk menampilkan pekerja kontrak dan kapasitas subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Papan Jadwal di Microsoft Dynamics 365 Project Operations dapat digunakan untuk mencari sumber daya dengan dua cara:

- Pencarian sumber daya umum tanpa konteks persyaratan sumber daya berbasis proyek tertentu.
- Pencarian sumber daya khusus persyaratan di mana persyaratan proyek akan memberikan konteks untuk sumber daya yang disarankan.

Untuk memberi tahu dewan jadwal tentang kapasitas sumber daya subkontrak dan pekerja kontrak, Anda perlu membuat pembaruan pada pengaturan Dewan Jadwal. Pembaruan ini meliputi: 
- Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum.
- Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum
### <a name="update-filters-for-general-resource-search"></a>Memperbarui filter untuk pencarian sumber daya umum
Saat Anda mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua hal berikut:
  - Tipe pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
  - Perusahaan vendor yang sumber dayanya harus dimiliki.
  - Sumber daya yang termasuk dalam subkontrak atau subkontrak tertentu.
    
### <a name="update-retrieve-resource-query"></a>Memperbarui kueri ambil sumber daya
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya umum:  
1. Buka **Pengaturan** Papan Jadwal untuk Papan Jadwal tertentu.
2. **Buka tab Pengaturan** umum dan gulir ke **Pengaturan lainnya**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak** Filter ke **Tata Letak Filter Default untuk Project Operations Lite**.
4. Perbarui **Kueri** Ambil Sumber Daya ke **Kueri Ambil Sumber Daya Default untuk Operasi Proyek Lite**.

![Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Memperbarui filter untuk pencarian sumber daya khusus persyaratan 
Saat Anda mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua hal berikut:
 - Tipe pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
 - Perusahaan vendor yang sumber dayanya harus dimiliki.
 - Sumber daya yang termasuk dalam subkontrak atau subkontrak tertentu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Memperbarui kueri ambil sumber daya untuk pencarian sumber daya khusus persyaratan 
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya berbasis persyaratan:

1. Buka **Pengaturan** Papan Jadwal untuk Papan Jadwal tertentu lalu pilih **Buka Pengaturan** default untuk membuka pengaturan untuk pencarian khusus persyaratan.
2. **Buka tab Pengaturan** umum dan gulir ke **Pengaturan lainnya**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak** Filter ke **Tata Letak Filter Default untuk Project Operations Lite**.
4. Perbarui **Kueri** Ambil Sumber Daya ke **Kueri Ambil Sumber Daya Default untuk Operasi Proyek Lite**.
5. **Buka tab Tipe** Jadwal dan buka **Proyek**.
6. Di bawah pengaturan untuk **Proyek**, perbarui **Jadwal Asisten Mengambil Kueri** Sumber Daya ke **Kueri Sumber Daya Ambil Default untuk Operasi Proyek Lite** dan perbarui **Jadwal Asisten Mengambil Kueri** Kendala untuk **Mengambil Kueri Kendala Default untuk Operasi Proyek Lite**.

![Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

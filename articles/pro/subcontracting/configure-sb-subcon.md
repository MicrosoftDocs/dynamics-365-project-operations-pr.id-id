---
title: Konfigurasikan Papan Jadwal untuk menampilkan pekerja kontrak dan kapasitas subkontrak
description: Artikel ini menjelaskan cara mengonfigurasi Papan Jadwal di Microsoft Dynamics 365 Project Operations untuk memperlihatkan kapasitas sumber daya yang disubkontrakkan saat mengelola persyaratan sumber daya proyek.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b965fd5011a575354f50c47081be198ab43248f9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919834"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurasikan Papan Jadwal untuk menampilkan pekerja kontrak dan kapasitas subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Papan Jadwal di Microsoft Dynamics 365 Project Operations dapat digunakan untuk mencari sumber daya dengan dua cara:

- Pencarian sumber daya umum tanpa konteks persyaratan sumber daya berbasis proyek tertentu.
- Pencarian sumber daya khusus persyaratan di mana persyaratan proyek akan memberikan konteks untuk sumber daya yang disarankan.

Untuk memberi tahu dewan jadwal tentang kapasitas sumber daya yang disubkontrakkan dan pekerja kontrak, Anda perlu membuat pembaruan pada pengaturan Papan Jadwal. Pembaruan ini meliputi: 
- Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum.
- Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum
### <a name="update-filters-for-general-resource-search"></a>Memperbarui filter untuk pencarian sumber daya umum
Saat Anda mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua hal berikut:
  - Tipe pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
  - Perusahaan vendor tempat sumber daya harus dimiliki.
  - Sumber daya yang termasuk dalam subkontrak atau garis subkontrak tertentu.
    
### <a name="update-retrieve-resource-query"></a>Memperbarui kueri sumber daya pengambilan
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya umum:  
1. Buka **Pengaturan** Papan Jadwal untuk Papan Jadwal tertentu.
2. Buka tab **Pengaturan** umum dan gulir ke **Pengaturan lainnya**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak Filter ke** Tata **Letak Filter Default untuk Operasi Proyek Lite**.
4. Perbarui **Retrieve Resources Query** ke **Default Retrieve Resources Query for Project Operations Lite**.

![Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Memperbarui filter untuk pencarian sumber daya khusus persyaratan 
Saat Anda mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua hal berikut:
 - Tipe pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
 - Perusahaan vendor tempat sumber daya harus dimiliki.
 - Sumber daya yang termasuk dalam subkontrak atau garis subkontrak tertentu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Memperbarui mengambil kueri sumber daya untuk pencarian sumber daya khusus persyaratan 
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya berbasis persyaratan:

1. Buka **Pengaturan** Papan Jadwal untuk Papan Jadwal tertentu lalu pilih **Buka pengaturan** Default untuk membuka pengaturan untuk pencarian khusus persyaratan.
2. Buka tab **Pengaturan** umum dan gulir ke **Pengaturan lainnya**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak Filter ke** Tata **Letak Filter Default untuk Operasi Proyek Lite**.
4. Perbarui **Retrieve Resources Query** ke **Default Retrieve Resources Query for Project Operations Lite**.
5. Buka tab **Jenis** Jadwal dan buka **Proyek**.
6. Di bawah pengaturan untuk **Proyek**, perbarui **Jadwalkan Asisten Mengambil Kueri** Sumber Daya untuk **Mengambil Kueri Sumber Daya Secara Default untuk Operasi Proyek Lite** dan memperbarui **Jadwalkan Asisten Mengambil Kueri** Batasan untuk **Kueri Batasan Pengambilan Default untuk Operasi Proyek Lite**.

![Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

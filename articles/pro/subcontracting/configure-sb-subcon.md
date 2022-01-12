---
title: Mengonfigurasi Papan Jadwal untuk menunjukkan pekerja kontrak dan kapasitas subkontrak
description: Ini topik menjelaskan cara mengonfigurasi Papan Jadwal di Microsoft Dynamics 365 Project Operations untuk menunjukkan kapasitas sumber daya subkontrak saat kepegawaian persyaratan sumber daya proyek.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903688"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Mengonfigurasi Papan Jadwal untuk menunjukkan pekerja kontrak dan kapasitas subkontrak 

[!include [banner](../../includes/dataverse-preview.md)]

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Papan Jadwal di Microsoft Dynamics 365 Project Operations dapat digunakan untuk mencari sumber daya dengan dua cara:

- Pencarian sumber daya umum tanpa konteks persyaratan sumber daya berbasis proyek tertentu.
- Persyaratan - pencarian sumber daya khusus di mana persyaratan proyek akan memberikan konteks untuk sumber daya yang disarankan.

Untuk memberi tahu papan jadwal kapasitas sumber daya subkontrak dan pekerja kontrak, Anda perlu melakukan pembaruan pada pengaturan Papan Jadwal. Pembaruan ini meliputi: 
- Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum.
- Perbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum
### <a name="update-filters-for-general-resource-search"></a>Memperbarui filter untuk pencarian sumber daya umum
Ketika Anda mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua hal berikut:
  - Jenis pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
  - Perusahaan vendor tempat sumber daya harus menjadi milik.
  - Sumber daya yang termasuk dalam garis subkontrak atau subkontrak tertentu.
    
### <a name="update-retrieve-resource-query"></a>Memperbarui kueri sumber daya ambil
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya umum:  
1. Buka **Pengaturan Papan Jadwal untuk Papan Jadwal** tertentu.
2. Buka **tab Pengaturan** umum dan gulir ke **pengaturan lainnya**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak Filter ke Tata Letak Filter Default untuk Operasi Proyek Lite** **·**.
4. Perbarui **Ambil Kueri Sumber Daya ke Kueri Sumber Daya Bawaan untuk Operasi Proyek Lite** **·**.

![Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya umum](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan
### <a name="update-filters-for-requirement-specific-resource-search"></a>Memperbarui filter untuk pencarian sumber daya khusus persyaratan 
Ketika Anda mencari sumber daya, filter yang tersedia di papan jadwal harus diperbarui sehingga Anda juga dapat mencari sumber daya eksternal dengan menentukan salah satu atau semua hal berikut:
 - Jenis pekerja, apakah sumber daya yang ditampilkan harus pekerja kontrak atau karyawan.
 - Perusahaan vendor tempat sumber daya harus menjadi milik.
 - Sumber daya yang termasuk dalam garis subkontrak atau subkontrak tertentu.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Memperbarui permintaan sumber daya untuk pencarian sumber daya khusus persyaratan 
Kueri yang digunakan untuk pencarian juga harus diperbarui untuk menggunakan atribut filter tambahan ini. Gunakan langkah-langkah berikut untuk memperbarui konfigurasi Papan Jadwal untuk pencarian sumber daya berbasis persyaratan:

1. Buka **Pengaturan Papan Jadwal untuk Papan Jadwal tertentu lalu pilih Buka pengaturan Default untuk membuka pengaturan untuk** pencarian khusus **persyaratan**.
2. Buka **tab Pengaturan** umum dan gulir ke **pengaturan lainnya**.
3. Dalam daftar pengaturan di bagian ini, perbarui **Tata Letak Filter ke Tata Letak Filter Default untuk Operasi Proyek Lite** **·**.
4. Perbarui **Ambil Kueri Sumber Daya ke Kueri Sumber Daya Bawaan untuk Operasi Proyek Lite** **·**.
5. Buka **tab Tipe Jadwal** dan buka **Project**.
6. Di bawah pengaturan untuk **Project**, perbarui **Asisten Jadwal Ambil Kueri Sumber Daya untuk Default Mengambil Kueri Sumber Daya untuk Operasi Proyek Lite** dan memperbarui Kueri Batasan Pengambilan Asisten Jadwal ke Kueri Batasan Pengambilan Default **untuk Operasi Proyek Lite** **·** **·**.

![Memperbarui pengaturan Papan Jadwal untuk pencarian sumber daya berbasis persyaratan](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

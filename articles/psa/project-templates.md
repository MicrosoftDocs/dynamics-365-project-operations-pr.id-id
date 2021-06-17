---
title: Template Proyek
description: Topik ini menyediakan informasi tentang cara menggunakan template proyek untuk konfigurasi proyek cepat.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998280"
---
# <a name="project-templates"></a>Template Proyek 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Template proyek adalah kerangka kerja standar yang membantu Anda dengan cepat dan mudah memulai proyek. Anda dapat menggunakan template yang telah ditetapkan untuk membuat proyek baru dengan sekali klik. Untuk proyek, Anda harus menentukan prasyarat untuk template proyek. Anda harus menentukan kalender proyek untuk setiap template proyek, dan peran dan daftar harga harus ditentukan dalam organisasi, sehingga komponen template memiliki data yang berguna.

Template proyek terdiri dari tiga komponen: jadwal, perkiraan proyek, dan anggota tim proyek.

## <a name="schedule"></a>Jadwal

Jadwal dalam template proyek memiliki rangkaian elemen yang sama dengan jadwal di proyek. Anda dapat membuat hierarki tugas, mengaitkan peran dengan tugas, menetapkan atribut jadwal, dan mengatur dependensi. Jadwal dalam template proyek juga mendukung mode tugas untuk setiap tugas. Oleh karena itu, alat ini mendukung mesin penjadwalan. Anda harus mengaitkan kalender proyek dengan proyek. Tidak ada perbedaan antara template proyek dan sebuah proyek ketika membuat jadwal kerja.

## <a name="project-estimates"></a>Perkiraan proyek

Perkiraan proyek dalam template proyek berfungsi sama seperti perkiraan proyek dalam suatu proyek. Namun, harga dan harga penjualan ditarik dari daftar harga penjualan dan biaya default yang ditentukan dalam parameter.

## <a name="creating-a-project-from-a-template"></a>Membuat Proyek dari Template
 
Ada beberapa cara membuat proyek dari template proyek:

- Ketika Anda membuat proyek dari kuotasi, Anda dapat memilih template proyek dalam kotak dialog **Buat cepat: proyek**.

> ![Kotak dialog buat cepat: proyek](media/project-11.png)

- Saat membuat proyek dengan memilih **proyek baru**, halaman **proyek** akan ditampilkan sebelum rekaman disimpan. Di bidang **pilih template**, pilih salah satu template proyek yang telah ditetapkan dalam organisasi.
- Gunakan **buat proyek dari template** di halaman **entitas template**.

## <a name="copying-components-of-template-to-project"></a>Menyalin komponen template ke proyek

Bila Anda menyalin komponen template proyek ke proyek, beberapa penimpaan dapat terjadi, tergantung pada pengaturan dalam proyek.

### <a name="copying-the-schedule"></a>Menyalin jadwal

Ketika Anda menyalin jadwal dari template proyek, jika proyek memiliki kalender proyek yang berbeda dari template, jam kerja dari kalender proyek akan diterapkan ke jadwal tugas. Dengan demikian, jadwal disesuaikan agar cocok dengan kalendar proyek cadangan. Demikian pula, tugas pertama pada jadwal mengambil tanggal mulai proyek, dan jadwal sisa jadwal hierarki tugas diperbarui berdasarkan durasi dan dependensi yang ditentukan dalam struktur rincian kerja template. 

### <a name="copying-project-estimates"></a>Menyalin Perkiraan proyek 

Bila Anda menyalin seluruh baris perkiraan proyek, daftar harga akan diperbarui. Untuk daftar harga biaya, pembaruan ini didasarkan pada unit kepemilikan proyek. Untuk daftar harga penjualan, mereka didasarkan pada pelanggan. Unit biaya dan harga penjualan ditentukan dari daftar harga ini pada proyek-proyek yang terkait ke entitas penjualan.

### <a name="copying-a-project-team"></a>Menyalin tim proyek

Bila Anda menyalin tim proyek dari template proyek untuk sebuah proyek, sumber daya generik akan disalin di seluruhnya, bersama dengan keterampilan dan penguasaan yang didefinisikan dalam template. Tugas sumber generik juga dikelola seperti template proyek. Sumber daya bernama tidak didukung dalam template proyek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
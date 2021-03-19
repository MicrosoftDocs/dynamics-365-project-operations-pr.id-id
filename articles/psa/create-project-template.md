---
title: Buat Template Proyek
description: Bagaimana membuat template proyek di Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e8a9b75aa0721c6e7c85c2bca8796bf9f2c6d3db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285127"
---
# <a name="create-a-project-template-project-service"></a>Buat Template proyek (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Template proyek menghemat waktu Anda jika perusahaan Anda secara teratur mengajukan penawaran pada jenis proyek yang serupa. Mereka memberikan set standar peran dan perkiraan jam untuk jenis proyek. Manajer akun dan manajer proyek dapat membuat proyek-proyek berdasarkan template proyek, atau mereka dapat menyalin template dan membuatnya sendiri.  
  
## <a name="components-of-project-template"></a>Komponen template proyek
 Template proyek terdiri dari tiga komponen:  
  
- **Struktur rincian kerja**: struktur rincian kerja dalam sebuah template proyek memiliki serangkaian elemen yang sama seperti dalam proyek. Anda dapat membuat hierarki tugas, mengaitkan peran untuk tugas, menetapkan atribut jadwal, mengatur dependensi dan melihat semua data di Gantt. Struktur rincian kerja dalam template proyek juga mendukung mode tugas untuk setiap tugas. Tidak ada perbedaan antara template proyek dan sebuah proyek ketika membuat jadwal kerja.  
  
- **Perkiraan proyek**: Perkiraan proyek dalam template berfungsi dengan cara yang sama seperti yang mereka lakukan dalam proyek-proyek, kecuali daftar harga untuk default biaya dan harga penjualan selalu merupakan default biaya dan daftar harga penjualan yang didefinisikan dalam parameter [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Fungsi lainnya adalah sama seperti dalam sebuah proyek.  
  
- **Pembentukan tim proyek**: ketika membentuk sebuah tim proyek untuk template proyek, Anda tidak dapat memesan sumber daya bernama dalam sebuah template. Anda dapat menggunakan **Buat tim proyek** dalam struktur rincian kerja untuk menghasilkan set sumber daya generik. Anda juga dapat menentukan keterampilan dan penguasaan yang diperlukan untuk sumber daya generik. Anda tidak dapat menggantikan sumber daya generik dengan sumber daya yang dapat dipesan dalam template proyek.  
  
## <a name="create-a-project-from-a-template"></a>Buat Proyek dari Template  
 Anda dapat membuat sebuah proyek dari template dengan cara berikut ini:  
  
-   Ketika membuat sebuah proyek dari kuotasi, Anda dapat memilih template proyek dalam formulir membuat cepat proyek.  
  
-   Ketika membuat sebuah proyek dengan mengklik **Proyek baru**, formulir proyek ditampilkan sebelum menyimpan rekaman. Dari sini, Anda dapat mengklik bidang **pilih template** untuk memilih dari daftar template proyek yang telah ditetapkan di organisasi Anda.  
  
-   Klik **buat proyek dari template** di halaman **Template proyek** untuk membuat sebuah proyek dari template.  
  
## <a name="copying-components-of-a-template-to-a-project"></a>Menyalin komponen template ke proyek  
 Bila Anda menyalin komponen template menjadi proyek, ada beberapa hal yang harus Anda ketahui.  
  
 **Menyalin struktur rincian kerja**: ketika Anda menyalin struktur rincian kerja dari template proyek, jika proyek memiliki kalender proyek yang berbeda dari template, jam kerja dari kalender proyek akan diterapkan ke jadwal tugas. Ini menyesuaikan jadwal untuk kalendar proyek dukungan. Demikian pula, tugas pertama pada struktur rincian kerja mengambil tanggal mulai proyek, sehingga sisa jadwal hirarki tugas diperbarui berdasarkan durasi dan dependensi yang ditentukan dalam struktur rincian kerja template.  
  
 **Menyalin perkiraan proyek**: ketika Anda menyalin seluruh baris perkiraan proyek, daftar harga diperbarui berdasarkan unit penanggung jawab proyek untuk daftar harga biaya dan pelanggan untuk daftar harga penjualan. Unit biaya dan harga penjualan ditentukan dari daftar harga ini pada proyek-proyek yang terkait ke entitas penjualan.  
  
 **Menyalin tim proyek**: bila Anda menyalin tim proyek dari template untuk sebuah proyek, sumber daya generik akan disalin di seluruhnya, bersama dengan keterampilan dan penguasaan yang didefinisikan dalam template. Tugas sumber generik juga dikelola seperti template proyek.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan Manajer Proyek](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
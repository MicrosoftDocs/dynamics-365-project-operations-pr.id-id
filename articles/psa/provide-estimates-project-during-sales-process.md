---
title: Memberikan estimasi kerja untuk sebuah proyek selama proses penjualan
description: Bagaimana memberikan estimasi kerja untuk sebuah proyek selama proses penjualan di Project Service
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
ms.openlocfilehash: 49ea8327ae34a69eba1585f1b1b4e557fd4eac93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283552"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a>Memberikan estimasi kerja untuk sebuah proyek selama proses penjualan (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Selama proses penjualan, Anda dapat melaksanakan perkiraan penjualan dari bawah dengan baris kuotasi. Kemampuan [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] di [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] memberikan cara yang lebih ilmiah dan deterministik mendapatkan perkiraan penjualan dengan memecah item pekerjaan dan mengasosiasikan atribut relevan yang berkontribusi terhadap perkiraan untuk proyek dalam struktur rincian kerja.  
  
 Setelah Anda mendapatkan penjualan, Anda dapat menggunakan struktur rincian kerja terkait dalam rencana proyek Anda, menyempurnakannya sesuai kebutuhan untuk berhasil menyelesaikan proyek Anda.  
  
## <a name="link-a-project-to-a-quote-line"></a>Tautkan proyek ke baris kuotasi  
 Ketika membuat baris kuotasi berbasis proyek, Anda dapat membuat sebuah proyek baru dari baris kuotasi. Anda dapat menggunakan template proyek, yang adalah rencana proyek standar pra-konfigurasi maupun perkiraan keuangan yang umum untuk organisasi Anda, atau salinan rencana proyek dan perkiraan dari proyek masa lalu. Ketika Anda membuat sebuah proyek, memilih template proyek menyediakan dasar untuk memperbaiki rencana proyek, perkiraan, dan persyaratan peran. Dengan membuat proyek Anda dari kuotasi, proyek ini otomatis dikaitkan dengan baris kuotasi.  
  
## <a name="project-estimate-components"></a>Komponen perkiraan proyek  
 Struktur rincian kerja dalam proyek menyediakan cara untuk memecah kerja ke dalam tugas-tugas, mempertahankan hirarki tugas, dan menetapkan perkiraan usaha yang dibutuhkan untuk menyelesaikan setiap tugas. Anda juga dapat mengaitkan peran dengan tugas untuk menunjukkan perkiraan jenis sumber daya yang diperlukan untuk menyelesaikan tugas dan jadwal.  
  
 Struktur rincian kerja membantu Anda menentukan usaha kerja dan perkiraan jadwal. Secara default, proyek menggunakan daftar harga standar yang Anda tetapkan sebelumnya. Harga penjualan dan biaya yang didefinisikan dalam daftar harga membantu menentukan perkiraan keuangan untuk rincian kerja proyek.  
  
 Jika proyek Anda terkait dengan kuotasi, dan kuotasi memiliki daftar harga yang berbeda dari default, daftar harga kuotasi itu digunakan untuk perkiraan keuangan.  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a>Impor perkiraan dari sebuah proyek ke kuotasi  
 Setelah Anda memiliki perkiraan proyek dalam proyek, Anda dapat mengimpor perkiraan ini ke dalam baris kuotasi:  
  
-   Dalam **rincian baris kuotasi**, klik **impor dari perkiraan**. 

-   Pilih apakah mengimpor perkiraan proyek yang diringkas menurut jenis transaksi, peran atau tingkat node struktur rincian kerja.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan Manajer Proyek](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
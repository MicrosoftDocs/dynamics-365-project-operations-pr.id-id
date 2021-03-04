---
title: Tentukan Perkiraan biaya dan pendapatan proyek
description: Bagaimana menentukan perkiraan biaya dan pendapatan proyek di Project Service
author: ruhercul
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148827"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>Tentukan Perkiraan biaya dan pendapatan proyek 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Perkiraan proyek memberikan tampilan keuangan untuk pekerjaan yang diperkirakan dan dijadwalkan pada struktur rincian kerja proyek. Tampilan perkiraan memberitahu Anda dampak biaya dan pendapatan dari pekerjaan yang direncanakan. Tampilan perkiraan menyediakan alat untuk melihat informasi pada sejumlah dimensi yang telah ditetapkan untuk memberitahu Anda sebaik-baiknya tentang dampak keuangan proyek.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Biaya dan nilai penjualan proyek  
Daftar harga [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] mendefinisikan biaya dan tarif tagihan untuk peran yang digunakan proyek. Berdasarkan peran yang terkait dengan tugas-tugas di struktur rincian kerja proyek, Anda dapat menentukan dampak biaya dan pendapatan dari pekerjaan yang terlibat.  
  
## <a name="cost-price-defaulting"></a>Standar harga biaya  
Setiap proyek adalah milik sebuah organisasi (ditunjukkan dalam **Unit Pemilik** dalam proyek). Daftar harga yang terkait dengan unit organisasi pemilik menentukan harga biaya per unit. [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] menentukan harga biaya untuk peran dengan mencari kombinasi dari peran, unit dan unit organisasi dalam daftar harga biaya untuk mendapatkan harga biaya yang benar untuk tanggal efektif pada baris perkiraan.  
  
Jika kombinasi peran, unit, dan unit organisasi tidak mengakibatkan harga biaya dari daftar harga unit pemilikdaftar harga, unit diabaikan untuk mendukung kombinasi peran dan unit organisasi. Jika ada harga biaya, harga ini dikonversi ke unit yang Anda pilih di baris perkiraan.  
  
Jika kombinasi peran dan unit organisasi tidak menghasilkan harga biaya, unit organisasi tersebut akan diabaikan dalam mendukung peran dan kombinasi unit, dan harga menjadi standar setelah menerapkan setiap konversi, jika diperlukan.  
  
 Jika tidak ada harga untuk peran, maka harga default adalah 0,00 pada baris perkiraan.  
  
 Semua biaya di jumlah baris perkiraan biaya proyek ada dalam mata uang unit organisasi pemilik.  
  
## <a name="sales-price-defaulting"></a>Standar harga Penjualan  
Daftar harga penjualan didasarkan pada entitas penjualan yang melekat pada proyek. Daftar harga Penjualan yang terkait dengan kuotasi atau kontrak menentukan harga Penjualan. Jika kuotasi atau kontrak memiliki daftar harga kustom, ini adalah daftar harga penjualan default untuk perkiraan proyek. Jika tidak ada Asosiasi untuk entitas penjualan, maka daftar harga penjualan default yang dikonfigurasi dalam pengaturan parameter akan menjadi daftar harga penjualan default untuk proyek. Setiap baris perkiraan memiliki unit organisasi sumber daya yang terkait untuk menunjukkan unit organisasi dari mana sumber daya yang akan dipesan untuk menyelesaikan tugas. Harga penjualan untuk peran yangterkait ditentukan dengan mencari kombinasi dari peran, unit dan unit organisasi sumber daya dalam daftar harga penjualan untuk mendapatkan harga penjualan yang benar untuk tanggal efektif pada baris perkiraan.  
  
Jika kombinasi peran, unit, dan unit organisasi sumber daya tidak menghasilkan harga penjualan dari daftar harga penjualan, sistem akan mengabaikan unit dan mencari kombinasi dari unit organisasi sumber daya dan peran. Jika ada harga Penjualan, ini dikonversi ke unit yang Anda pilih di baris perkiraan Penjualan.  
  
Jika sistem tidak menemukan harga untuk peran, maka harga default penjualan adalah 0,00 pada baris perkiraan.  
  
Tampilan perkiraan memiliki tampilan grid yang menampilkan grid datar baris perkiraan dengan biaya total dan unit dan harga penjualan.  
  
## <a name="time-phased-view-of-project-estimates"></a>Tampilan bertahap waktu dari estimasi proyek  
Dalam tampilan bertahapan waktu untuk perkiraan proyek, data perkiraan dari tampilan grid diputar secara default oleh peran, dan menunjukkan penyebaran data perkiraan di garis waktu dalam skala waktu pilihan.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Alokasi perkiraan upaya berdasarkan tugas mode  
Di tampilan bertahap waktu, usaha total yang diperkirakan untuk tugas didistribusikan dengan mengalokasikan jumlah tertentu jam upaya per unit periode waktu skala waktu pilihan. Dalam project service, modus tugas menentukan bagaimana upaya dialokasikan di masa tugas. Dua jenis alokasi adalah alokasi merata dan jam kerja berdasarkan alokasi. 
  
## <a name="work-hours-based-allocation"></a>Jam kerja berbasis alokasi  
Mode tugas penjadwalan otomatis untuk tugas mengatur bahwa untuk jumlah sumber daya yang diperkirakan pada tugas, mereka diperkirakan untuk dimanfaatkan untuk jam kerja penuh setiap hari. Hal ini berlaku ketika mengalokasikan upaya dengan memisahkan seluruh durasi tugas dalam tampilan bertahap waktu juga. Misalnya, pada skala waktu 'Hari', untuk tugas yang diperkirakan akan selesai pada satu sumber daya, upaya yang dialokasikan setiap hari tidak akan melebihi jam kerja per hari yang didefinisikan dalam kalender proyek. Oleh karena itu, alokasi usaha selalu memastikan bahwa sumber daya diperkirakan untuk dimanfaatkan untuk sehari penuh.  
  
## <a name="even-distribution"></a>Distribusi merata  
Mode tugas terjadwal secara manual tidak menghormati jam kerja, kalender proyek, atau jumlah sumber daya yang didefinisikan pada tugas. Jadwal tugas didasarkan pada input pengguna. Untuk tugas tersebut, alokasi upaya per unit jangka waktu skala waktu pilihan tidak memiliki faktor pembatas apapun. Upaya total pada tugas dipecah dan dialokasikan dengan sama untuk masing-masing unit jangka waktu pada skala waktu pilihan.  
  
Dengan cara ini, modus tugas yang didefinisikan pada tugas menentukan distribusi usaha atau alokasi usaha per unit jangka waktu di perkiraan bertahap waktu.  
  
## <a name="grouping-and-time-phasing-options"></a>Pengelompokan dan opsi pentahapan waktu  
Tampilan ini membantu Anda memahami distribusi usaha, biaya, dan perkiraan penjualan pada per hari, Minggu, bulan, atau tahun dasar. Opsi Kelompokkan menurut memungkinkan memutar data perkiraan pada dua dimensi lain: Kategori dan sumber daya. Pada tampilan grid dan tampilan bertahap waktu Anda dapat memilih kolom yang akan ditampilkan. Total untuk setiap kali blok ditampilkan di bagian bawah yang menunjukkan upaya perkiraan total, biaya, dan penjualan harian, pekanan, bulanan, atau tahunan.  
  
Harga penjualan dan biaya default adalah efektif tanggal. Ketika tingkat untuk peran berubah, ia akan lebih transparan dalam tampilan bertahapan waktu ketika melihat data perkiraan yang diputar pada 'Sumber' dan waktu bertahapan minggu.  
  
## <a name="expense-estimates"></a>Perkiraan pengeluaran  
Setiap biaya yang akan dikenakan dalam proyek yang tidak secara langsung berhubungan dengan tenaga kerja yang akan digunakan dapat direkam dalam perkiraan proyek dalam tampilan grid. Menggunakan opsi **Tambahkan perkiraan biaya** di tampilan grid, Anda dapat mencapai hal ini. Estimasi pengeluaran dapat direkam untuk tugas tertentu atau untuk seluruh proyek. Anda dapat memilih kategori pengeluaran pada baris ini dan memilih tanggal tentatif ketika biaya diperkirakan akan dikeluarkan. Jika biaya yang terkait dan daftar harga penjualan memiliki harga default, atau persentase markup yang didefinisikan untuk kategori pengeluaran, itu akan memiliki default baris perkiraan pada Asosiasi.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan Manajer Proyek](../psa/project-manager-guide.md)

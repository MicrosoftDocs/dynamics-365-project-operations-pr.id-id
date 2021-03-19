---
title: Jadwalkan proyek dengan struktur rincian kerja
description: Cara menjadwalkan proyek dengan struktur rincian kerja di Project Service
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
ms.openlocfilehash: a00e39f78890426721a49cd569ba8ce4accb30a9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282697"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a>Jadwalkan proyek dengan struktur rincian kerja (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Jadwal proyek mengomunikasikan apa pekerjaan yang perlu dilakukan, sumber daya yang akan melakukan pekerjaan, dan jangka waktu di mana pekerjaan perlu diselesaikan. Jadwal proyek mencerminkan semua pekerjaan yang berkaitan dengan penyampaian proyek tepat waktu. Salah satu langkah pertama dalam fase inisiasi proyek adalah untuk menghasilkan jadwal proyek. Untuk menetapkan jadwal proyek, Anda perlu membuat struktur rincian kerja.  
  
 Buat struktur proyek dengan struktur rincian kerja, yang akan membantu Anda:  
  
- Memecah kerja ke dalam tugas-tugas yang bisa dikelola  
  
- Memperkirakan waktu yang dibutuhkan untuk menyelesaikan tugas  
  
- Mengatur ketergantungan tugas dan durasi tugas  
  
- Menentukan peran yang diperlukan untuk menyelesaikan setiap tugas  
  
  Jadwal proyek dalam struktur rincian kerja memiliki tampilan dan nuansa akrab, lengkap dengan diagram Gantt interaktif.  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a>Buat struktur rincian kerja untuk proyek  
 Buat struktur rincian kerja untuk mewakili urutan tugas dalam sebuah proyek. Struktur rincian kerja termasuk tugas-tugas, persyaratan untuk setiap tugas, dan informasi pendapatan dan biaya. Dalam struktur rincian kerja Anda, Anda dapat menambahkan:  
  
-   Urutan tugas dalam hirarki  
  
-   Tugas-tugas lain, jika ada, yang harus diselesaikan sebelum tugas dapat dimulai  
  
-   Tanggal mulai, tanggal berakhir, dan durasi tugas  
  
-   Jumlah jam yang dibutuhkan untuk tugas  
  
-   Segala keterampilan dan pendidikan pekerja yang diperlukan  
  
-   Para pekerja yang diberi tugas  
  
-   Perkiraan penerimaan dan biaya  
  
## <a name="task-types"></a>Jenis Tugas  
Anda akan menggunakan jenis tugas berikut saat membuat struktur rincian kerja Anda:  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| **Node akar proyek**. | Ringkasan tugas tingkat atas untuk proyek. Semua tugas-tugas proyek lain yang dibuat di bawahnya. Nama tugas akar adalah nama proyek. Usaha, tanggal, dan durasi dari node akar didasarkan pada nilai-nilai pada hirarki di bawahnya. Anda tidak dapat mengedit properti node akar atau menghapus node akar. | 
| **Ringkasan atau tugas wadah** | Ringkasan tugas adalah tugas yang memiliki sub-tugas di bawahnya. Ringkasan tugas tidak memiliki usaha kerja atau biaya sendiri. Usaha kerja dan biayanya adalah rollup sub tugas. Anda dapat mengubah nama tugas ringkasan, tetapi Anda tidak dapat mengubah usaha, tanggal, atau durasi, karena mereka secara otomatis dihitung. Menghapus tugas ringkasan menghapus tugas dan semua sub-tugas.|  
| **Tugas node leaf** | Tugas node leaf merupakan karya yang paling rinci pada proyek. Ini memiliki upaya perkiraan, jumlah sumber daya yang direncanakan, durasi dan tanggal akhir dan awal yang direncanakan.|

  
## <a name="task-hierarchy"></a>Hierarki tugas  
 Anda memiliki pilihan berikut saat membuat hierarki tugas:  
  
- **Menambahkan tugas**.   Anda dapat menambahkan tugas pada posisi yang Anda pilih dalam hirarki tugas. Jika Anda tidak memilih posisi, tugas baru muncul pada akhir.  
  
- **Indentasi tugas**.   Indentasi tugas untuk membuat anak tugas langsung di atasnya.  
  
- **Outdentasi tugas**.   Outdentasi tugas untuk membuatnya sedemikian rupa sehingga tidak lagi menjadi sub-tugas induk yang asli.  
  
- **Naik dan bergerak ke bawah**.   Pindahkan tugas naik dan turun dalam hirarki tugas induknya. Memindahkan tugas naik atau turun tidak berpengaruh pada upaya, biaya, tanggal, atau durasi.  
  
## <a name="task-attributes"></a>Atribut tugas  
 Nama tugas menjelaskan pekerjaan yang perlu diselesaikan. Anda menggunakan berbagai tugas atribut untuk menggambarkan persyaratan staf dan jadwal untuk tugas.  
  
### <a name="schedule-attributes"></a>Atribut jadwal

 - Tetapkan nilai-nilai untuk **jam usaha**, **jumlah sumber daya**, **tanggal mulai**, **tanggal berakhir**, dan **durasi** untuk menentukan jadwal tugas. 
 - **Upaya** merupakan perkiraan jam yang dibutuhkan untuk menyelesaikan tugas.
 - **Jumlah sumber daya** merupakan perkiraan yang manajer proyek tempatkan dalam tugas untuk membantu menghasilkan jadwal sebaik mungkin. 
 - **Durasi** (dalam hari) menunjukkan jumlah hari kerja yang dibutuhkan untuk menyelesaikan tugas.  
  
### <a name="staffing-attributes"></a>Atribut staf

 - **Peran**, **unit organisasi sumber daya**, **jumlah sumber daya**, dan **sumber daya** menjelaskan persyaratan staf untuk tugas. 
 - **Peran** menjelaskan jenis sumber daya yang diperlukan untuk melakukan tugas. 
 - **Unit organisasi sumber daya** menunjukkan unit organisasi dari mana sumber daya harus diisi stafnya untuk tugas itu; ini juga berdampak pada biaya dan perkiraan penjualan tugas, karena ini diperhitungkan ketika menentukan harga penjualan unit untuk sumber daya. 
 - **Sumber daya** memegang sumber daya generik atau sumber daya yang bernama ketika ditemukan.  
  
## <a name="task-dependencies"></a>Dependensi tugas  
 Anda dapat membuat hubungan pendahulu antara satu atau lebih tugas dalam struktur rincian kerja. Anda dapat mengatur nilai satu atau lebih bidang pendahulu pada tugas-tugas untuk menunjukkan tugas-tugas yang akan bergantung padanya. Bila Anda menetapkan nilai pendahulu tugas, tugas hanya dapat mulai ketika menyelesaikan semua tugas-tugas pendahulunya. Mengatur ketergantungan ini pada tugas akan mengakibatkan perhitungan kembali tanggal mulai tugas yang direncanakan sebagai akhir terbaru dari semua pendahulunya. Dampak terkait dengan pendahulu pada jadwal tidak dibatasi oleh modus tugas yang didefinisikan pada tugas.  
  
## <a name="task-mode"></a>Modus tugas  
 Mode tugas adalah salah satu faktor penting yang menentukan penjadwalan tugas node leaf. Ada dua mode tugas untuk setiap tugas: modus penjadwalan otomatis dan modus manual penjadwalan.  
  
-   **Penjadwalan Otomatis**.   Ketika Anda mengatur modus tugas untuk secara otomatis dijadwalkan, mesin penjadwalan tugas menggunakan aturan penjadwalan pada atribut tugas berikut untuk menentukan jadwal tugas:  
  
    -   Pendahulu  
  
    -   Upaya  
  
    -   Jumlah sumber daya  
  
    -   Tanggal Mulai dan Berakhir  
  
-   **Aturan Penjadwalan**.   Tanggal mulai tugas node leaf yang tidak memiliki default pendahulu untuk tanggal mulai penjadwalan proyek. Masa tugas node leaf selalu dihitung sebagai jumlah hari kerja antara tanggal yang awal dan akhir. Ketika tugas dijadwalkan secara otomatis, Mesin penjadwalan mengikuti aturan di bawah ini:  
  
    -   Tanggal mulai dan akhir dari tugas yang harus selalu hari kerja menurut kalender penjadwalan proyek  
  
    -   Tanggal mulai tugas yang pendahulunya memiliki default tanggal akhir terbaru dari pendahulunya  
  
    -   Upaya = jumlah orang * durasi * jam dalam satu hari kerja standar kalendar proyek  
  
-   **Penjadwalan manual**.   Dalam beberapa kasus, Anda mungkin ingin menyimpang dari aturan-aturan ini. Dalam kasus ini, Anda dapat mengatur modus tugas untuk tugas untuk secara manual dijadwalkan. Ini menghentikan mesin penjadwalan menghitung nilai untuk atribut penjadwalan lainnya. Mengatur pendahulu pada tugas-tugas selalu berdampak pada tanggal mulai tugas yang tergantung.  
  
## <a name="create-a-work-breakdown-structure"></a>Buat struktur rincian kerja  
  
1.  Pergi ke **Project Service > Proyek**.  
  
2.  Klik proyek yang ingin Anda kerjakan.  
  
3.  Di bar di bagian atas layar, pilih panah bawah di sebelah nama proyek, dan kemudian klik struktur rincian kerja.  
  
4.  Untuk menambahkan tugas, klik **Tambahkan tugas**. Isi bidang untuk tugas, lalu klik **Simpan**.  
  
5.  Terus menambahkan tugas sampai struktur rincian kerja Anda selesai. Sementara membuat struktur rincian kerja Anda, Anda dapat melakukan hal berikut untuk mengatur tugas-tugas Anda:  
  
    -   Pilih tugas dan klik **Indent** untuk memindahkannya di bawah tugas lain atau klik Outdent untuk memindahkannya keluar tingkat.  
  
    -   Pilih tugas dan klik **Naik** atau **Turun** untuk bergerak naik atau turun dalam daftar.  
  
    -   Klik **Sembunyikan Gantt** untuk menyembunyikan Gantt chart, dan klik **Tunjukkan Gantt** untuk menampilkan lagi.  
  
    -   Pilih jangka waktu untuk Gantt chart di **skala waktu** berbeda.  
  
6.  Untuk menambahkan peran yang Anda tentukan dalam struktur rincian kerja Anda ke anggota tim proyek Anda, klik **Hasilkan tim proyek**.  
  
7.  Klik **Simpan** di sudut kanan bawah layar Setelah selesai melakukan perubahan.  
  
### <a name="see-also"></a>Lihat Juga  
 [Panduan Manajer Proyek](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
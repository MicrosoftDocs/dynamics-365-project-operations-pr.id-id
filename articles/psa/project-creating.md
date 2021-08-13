---
title: Jadwal proyek
description: Topik ini menyediakan informasi tentang cara membuat jadwal.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
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
ms.openlocfilehash: 192fbe7f26a2bd060ffe9bc0b1eea50b9431bca4696e3da1d94bf53158e026a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998420"
---
# <a name="project-schedules"></a>Jadwal proyek 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Jadwal proyek mengomunikasikan apa pekerjaan yang perlu dilakukan, sumber daya yang akan melakukan pekerjaan, dan jangka waktu di mana pekerjaan perlu diselesaikan. Ia mencerminkan semua pekerjaan yang berkaitan dengan penyampaian proyek tepat waktu. Di Dynamics 365 Project Service Automation, Anda membuat jadwal proyek dengan memecah pekerjaan menjadi tugas yang dapat dikelola, memperkirakan waktu yang diperlukan untuk melakukan setiap tugas, mengatur dependensi tugas, mengatur durasi tugas, dan memperkirakan sumber daya generik yang akan melakukan tugas. Jadwal proyek dibuat pada tab **jadwal** halaman proyek.
 
## <a name="tasks"></a>Tugas

Langkah pertama dalam membuat jadwal proyek adalah memisahkan pekerjaan menjadi bagian yang dapat dikelola. Jadwal dalam PSA mendukung fitur berikut:

- Node akar proyek.
- Ringkasan atau tugas wadah
- Tugas node leaf

### <a name="project-root-node"></a>Node akar proyek.

Node root proyek adalah tugas Rangkuman tingkat atas untuk proyek. Semua tugas-tugas proyek lain yang dibuat di bawahnya. Nama tugas node selalu diatur menjadi nama proyek. Usaha, tanggal, dan durasi dari node akar dirangkum berdasarkan nilai-nilai pada hierarki di bawahnya. Anda tidak dapat mengedit properti node root. Anda juga tidak dapat menghapus node root.

### <a name="summary-or-container-tasks"></a>Ringkasan atau tugas wadah 

Tugas ringkasan memiliki tugas sub-tugas atau kontainer di bawahnya. Mereka tidak memiliki usaha kerja atau biaya sendiri. Sebaliknya, usaha dan biaya kerja mereka adalah Rollup dari upaya kerja dan biaya tugas kontainer mereka. Tanggal mulai tugas ringkasan adalah tanggal mulai dari tugas kontainer, dan tanggal akhir adalah tanggal akhir dari tugas kontainer. Nama tugas ringkasan dapat diedit, namun properti penjadwalan (upaya, tanggal, dan durasi) tidak dapat diedit. Jika Anda menghapus tugas ringkasan, Anda juga akan menghapus semua tugas wadahnya.

### <a name="leaf-node-tasks"></a>Tugas node leaf

Tugas node leaf merupakan karya yang paling rinci pada proyek. Mereka memiliki upaya perkiraan, sumber daya, durasi, dan tanggal akhir dan awal yang direncanakan.
 
## <a name="creating-a-task-hierarchy"></a>Membuat hierarki tugas

Anda dapat membuat hierarki tugas dengan opsi berikut ini:

- Tombol **Tambahkan tugas**
- Tombol **tugas indentasi**
- Tombol **tugas outdentasi**
- Tombol **Naik** dan **turun**
- Cara pintas keyboard dan aksesibilitas

### <a name="add-task"></a>Tambahkan tugas

Tombol **Tambah tugas** memungkinkan Anda membuat tugas baru dalam hierarki. Jika Anda tidak memilih posisi, tugas dimasukkan pada akhir. 

ID jadwal ditetapkan ke setiap tugas. ID jadwal menunjukkan kedalaman tugas dan posisi dalam hirarki. Ia menggunakan penomoran kisi-kisi. Untuk tugas di tingkat pertama di bawah node root proyek, skema penomoran 1, 2, 3, dan sebagainya, digunakan. Untuk tugas di bawah tingkat pertama, skema penomoran 1.1, 1.2, 1.3, dan sebagainya, digunakan.

### <a name="indent-task"></a>tugas Indentasi.

Bila tugas diindentasi, tugas akan menjadi anak dari tugas yang langsung di atasnya. ID jadwal tugas kemudian dihitung ulang sehingga didasarkan pada ID jadwal dari induk barunya dan mengikuti skema penomoran kisi-kisi. Tugas induk sekarang adalah tugas ringkasan atau tugas kontainer. Oleh karena itu, ia menjadi Rollup tugas anaknya.

### <a name="outdent-task"></a>Outdentasi tugas. 

Ketika tugas di outdentasi, ia tidak lagi anak dari tugas yang menjadi induknya. ID jadwal kemudian dihitung ulang sehingga mencerminkan kedalaman tugas yang diperbarui dan posisi dalam hirarki. Upaya, biaya, dan tanggal tugas induk sebelumnya dihitung ulang sehingga mereka tidak menyertakan tugas ini.

### <a name="move-up-and-move-down"></a>Naik dan turun 

Tombol **Pindahkan ke atas** dan **Pindahkan ke bawah** mengubah posisi tugas dalam hierarki induknya. Perubahan jenis ini tidak mempengaruhi upaya, biaya, tanggal, atau durasi tugas. Hanya ID jadwal tugas yang terpengaruh. ID jadwal dihitung ulang sehingga mencerminkan posisi tugas yang baru di daftar induk tugas anak.

### <a name="accessibility-and-keyboard-shortcuts"></a>Cara pintas keyboard dan aksesibilitas

Kisi **jadwal** sepenuhnya dapat diakses dan dapat digunakan dengan pembaca layar seperti narrator, JAWS, atau NVDA. Anda dapat berpindah melalui area kisi dengan menggunakan tombol panah (sebagaimana di Microsoft Excel), Anda dapat menggunakan tombol tab untuk memajukan melalui elemen UI interaktif, dan Anda dapat menggunakan tombol panah bawah, tombol Enter, atau spasi untuk memilih dan menjalankan menu drop-down. Header kolom juga interaktif. Anda dapat menyembunyikan dan menampilkan kolom, menggunakan tombol tab dan tombol panah untuk berpindah di antara header kolom, dan menggunakan tombol tindakan pada Toolbar. Selain itu, Anda dapat menggunakan pintasan keyboard berikut:

- **Refresh**: ALT+SHIFT+F5
- **Tambah**: Alt + Shift + insert
- **Hapus**: Alt + Shift + Delete
- **Naik/turun**: ALT+SHIFT+panah bawah/atas
- **Indent/Outdent**: ALT_SHIFT + panah kiri/kanan
- **Perluas/Ciutkan hierarki**: Alt + Shift + tombol minus/Plus

## <a name="task-attributes"></a>Atribut tugas

Nama tugas menjelaskan pekerjaan yang perlu diselesaikan. Dalam PSA, atribut yang terkait dengan tugas menjelaskan jadwal tugas dan persyaratan staf.

> ![Atribut tugas.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Atribut jadwal

**Upaya** , **tanggal mulai**, **tanggal berakhir**, dan **durasi** menentukan jadwal tugas.

Atribut jadwal tambahan mencakup:

- **Jam kerja**: masukkan perkiraan jam yang diperlukan untuk menyelesaikan tugas. 
- **Durasi**: Tentukan jumlah hari kerja yang diperlukan untuk menyelesaikan tugas.
- **ID jadwal**: id yang dibuat secara otomatis ini digunakan untuk memesan tugas dalam hirarki. Dependensi antara tugas mengelola urutan aktual tugas yang dikerjakan.
 
### <a name="staffing-attributes"></a>Atribut staf

Atribut staf diakses melalui bidang **sumber daya** dalam jadwal. Anda dapat mencari sumber daya yang ada, atau mengeklik **buat** dan di panel **buat cepat**, tambahkan anggota tim proyek sebagai sumber daya baru.

**Peran**, **unit sumber daya**, dan bidang **nama posisi** digunakan untuk menjelaskan persyaratan staf untuk tugas. Atribut staf ini bersama dengan jadwal tugas digunakan untuk menemukan sumber daya yang tersedia untuk melakukan tugas ini.

**Peran** -Tentukan jenis sumber daya yang diperlukan untuk melakukan tugas.

**Unit sumber daya** -Tentukan unit asal penetapan sumber daya untuk tugas. Atribut ini mempengaruhi perkiraan biaya dan penjualan untuk tugas jika tingkat biaya dan tagihan untuk sumber daya diatur berdasarkan unit sumber daya.

**Nama posisi** – masukkan nama bersahabat untuk sumber daya generik yang berfungsi sebagai placeholder untuk sumber daya yang pada akhirnya akan melakukan pekerjaan.

Bidang **sumber daya** memegang nama posisi sumber daya generik atau sumber daya yang bernama saat ditemukan.

Bidang **kategori** memiliki nilai yang menunjukkan jenis pekerjaan yang lebih luas yang dapat dikelompokkan dalam tugas. Bidang ini tidak mempengaruhi penjadwalan atau staf. Hanya digunakan untuk pelaporan.

### <a name="task-dependencies"></a>Dependensi tugas 

Anda dapat menggunakan jadwal dalam PSA untuk membuat Relasi pendahulu antara tugas. Bidang **sebelumnya** di dalam **tugas** memerlukan satu atau beberapa nilai untuk menunjukkan tugas yang tergantung pada tugas. Bila Anda menetapkan nilai pendahulu tugas, tugas hanya dapat mulai ketika menyelesaikan semua tugas-tugas pendahulunya. Karena dependensi, tanggal mulai yang direncanakan untuk tugas diatur ulang ke tanggal saat tugas pendahulunya selesai.

Mode tugas tidak berpengaruh pada pembaruan yang dibuat pada tanggal mulai dan berakhir dari tugas pendahulu/tergantung.

## <a name="task-mode"></a>Modus tugas 

Mode tugas menentukan penjadwalan tugas node leaf. PSA mendukung dua mode tugas untuk setiap tugas: modus penjadwalan otomatis dan modus manual penjadwalan.

### <a name="auto-scheduling"></a>Penjadwalan Otomatis 
 
Ketika Anda mengatur modus tugas ke **secara otomatis dijadwalkan** untuk tugas, mesin penjadwalan tugas menggunakan aturan penjadwalan pada atribut tugas untuk menentukan jadwal tugas:

#### <a name="scheduling-rules"></a>Aturan Penjadwalan

Per default, node leaf tidak memiliki pendahulu, tanggal mulainya diatur ke tanggal mulai penjadwalan proyek. Masa tugas node leaf selalu dihitung sebagai jumlah hari kerja antara tanggal yang awal dan akhir. Ketika tugas dijadwalkan secara otomatis, Mesin penjadwalan mengikuti aturan ini:

- Tanggal mulai dan akhir dari tugas yang harus hari kerja menurut kalender penjadwalan proyek 
- Untuk setiap tugas yang memiliki tugas pendahulu, tanggal mulainya otomatis diatur ke tanggal akhir terbaru dari pendahulunya.
- Upaya dihitung dengan menggunakan rumus ini: jumlah orang × durasi × jam di hari kerja standar dalam kalender proyek.

### <a name="manual-scheduling"></a>Penjadwalan manual

Jika aturan penjadwalan otomatis tidak memenuhi kebutuhan Anda, Anda dapat mengatur mode tugas untuk tugas yang **dijadwalkan secara manual**. Pengaturan ini menghentikan mesin penjadwalan menghitung nilai untuk atribut penjadwalan lainnya. Terlepas dari mode tugas, jika Anda mengatur pendahulunya pada tugas, Anda selalu mempengaruhi tanggal mulai tugas dependen.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Membuat struktur rincian kerja
description: Artikel topik menjelaskan cara membuat WBS (struktur perincian kerja) yang mencakup kontrol dasar di antarmuka penjadwalan baru.
author: ruhercul
manager: tfehr
ms.date: 01/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d7fa645e78d2206e333d9f85fcec0f7a9c213c23
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841355"
---
# <a name="create-a-work-breakdown-structure-wbs"></a>Membuat struktur rincian kerja (WBS)

Jadwal proyek mengomunikasikan apa pekerjaan yang perlu dilakukan, sumber daya yang akan melakukan pekerjaan, dan jangka waktu di mana pekerjaan harus diselesaikan. Jadwal mencerminkan semua pekerjaan yang berkaitan dengan penyampaian proyek tepat waktu. Di Dynamics 365 Project Operations, Anda membuat jadwal proyek dengan:

  - Memecah kerja ke dalam tugas-tugas yang bisa dikelola.
  - Memperkirakan waktu yang diperlukan untuk melakukan setiap tugas.
  - Dependensi Tugas pengaturan.
  - Mengatur durasi tugas.
  - Memperkirakan sumber daya umum yang akan melakukan tugas. 

Jadwal proyek dibuat pada tab **jadwal** pada halaman **proyek**.

## <a name="tasks"></a>Tugas

Langkah pertama dalam membuat jadwal proyek adalah memisahkan pekerjaan menjadi bagian yang dapat dikelola. Jadwal dalam Project Operations mendukung fitur berikut:

- Ringkasan atau tugas wadah
- Tugas node leaf

### <a name="summary-tasks"></a>Tugas Ringkasan

Tugas ringkasan dapat menyimpan tugas ringkasan atau tugas node leaf lainnya. Mereka tidak memiliki usaha kerja atau biaya sendiri. Sebaliknya, usaha dan biaya kerja mereka adalah Rollup dari upaya kerja dan biaya tugas kontainer mereka. Tanggal mulai tugas ringkasan adalah tanggal mulai dari tugas kontainer, dan tanggal akhir adalah tanggal akhir dari tugas kontainer. Nama tugas ringkasan dapat diedit, namun properti penjadwalan, termasuk upaya, tanggal, dan durasi, tidak dapat diedit. Jika Anda menghapus tugas ringkasan, Anda juga akan menghapus semua tugas wadahnya.

### <a name="leaf-node-tasks"></a>Tugas node leaf

Tugas node leaf merupakan karya yang paling rinci pada proyek. Mereka memiliki upaya perkiraan, sumber daya, durasi, dan tanggal akhir dan awal yang direncanakan.

## <a name="create-a-task-hierarchy"></a>Membuat hierarki tugas

### <a name="add-a-task"></a>Menambahkan tugas

Lakukan langkah-langkah berikut untuk menambahkan satu atau lebih tugas.

1. Buka **Proyek**, pilih dan buka rekaman proyek yang akan dibuat jadwalnya. 
2. Pilih tab **Tugas**. 
3. Pilih **Tambah tugas baru**, masukkan nama untuk tugas, lalu tekan Enter.
2. Masukkan nama tugas lain, lalu tekan Enter lagi hingga Anda memiliki daftar tugas lengkap.

### <a name="manage-hierarchy-of-a-task"></a>Mengelola hierarki tugas

Bila tugas diindentasi, tugas akan menjadi anak dari tugas yang langsung di atasnya. ID jadwal tugas kemudian dihitung ulang sehingga didasarkan pada ID jadwal dari induk barunya dan mengikuti skema penomoran kisi-kisi. Tugas induk sekarang merupakan tugas ringkasan. Oleh karena itu, ia menjadi Rollup tugas anaknya. Ketika tugas dipromosikan, ia tidak lagi anak dari tugas yang menjadi induknya. ID jadwal kemudian dihitung ulang sehingga mencerminkan kedalaman tugas yang diperbarui dan posisi dalam hirarki. Upaya, biaya, dan tanggal tugas induk sebelumnya dihitung ulang sehingga mereka tidak menyertakan tugas ini.

Lakukan langkah-langkah berikut untuk mengidentasi atau mempromosikan tugas.

1. Di halaman **Proyek**, di tab **tugas**, di **tugas Rangkuman**, pilih tiga titik vertikal sesuai nama tugas, lalu pilih **Buat Subtugas**. 
2. Pilih tugas untuk mengindentasi atau mempromosikan. Untuk memilih lebih dari satu tugas, pilih tugas, tekan dan tahan Ctrl, lalu pilih tugas tambahan.
2. Pilih **Indentasi** atau **Promosikan subtugas**  untuk memindahkan tugas di bawah atau di luar tugas Rangkuman.

### <a name="move-tasks-up-and-down"></a>Naik dan turunkan tugas

Tugas dapat saya pindahkan ke tingkat apa pun dalam struktur rincian kerja dengan salah satu dari dua cara:

- Pilih satu tugas lagi, lalu tarik ke lokasi yang diinginkan.
- Pilih satu atau beberapa tugas, klik kanan dan pilih **Potong**, pilih sel tujuan dalam jadwal, lalu klik kanan dan pilih **Rekat**.

## <a name="task-attributes"></a>Atribut tugas

Nama tugas menjelaskan pekerjaan yang perlu diselesaikan. Dalam Project Operations, atribut yang terkait dengan tugas menjelaskan jadwal tugas dan persyaratan staf.

## <a name="schedule-attributes"></a>Atribut jadwal

**Upaya** , **tanggal mulai**, **tanggal berakhir**, dan **durasi** menentukan jadwal tugas.

Tabel berikut menampilkan atribut jadwal tambahan.

| **Nama Tampilan final** | **Deskripsi File** |
| --- | --- |
| Upaya Selesai (Jam) | Pekerjaan yang diselesaikan pada tugas tersebut dalam jam. |
| Durasi | Menampilkan durasi dalam hari untuk tugas. |
| Upaya Total | Pekerjaan total pada tugas tersebut dalam jam. |
| Selesai | Tanggal dan Waktu Selesai. |
| % Selesai | Persentase tugas yang selesai. |
| Wadah Proyek | Papan tugas dapat dikelompokkan berdasarkan kelompok, sehingga setiap kelompok memiliki kolom sendiri. |
| Upaya Tersisa (Jam) | Pekerjaan tersisa pada tugas tersebut dalam jam. |
| Pangkal | Tanggal dan Waktu Mulai. |
| Nama | Nama tugas. |
| ID | ID tugas dalam struktur rincian kerja. |

## <a name="staffing-attributes"></a>Atribut staf

Atribut staf diakses melalui bidang **sumber daya** dalam jadwal. Anda dapat mencari sumber daya yang ada, atau memilih **buat**, dan di panel **buat cepat**, tambahkan anggota tim proyek sebagai sumber daya baru.

**Peran**, **unit sumber daya**, dan bidang **nama posisi** digunakan untuk menjelaskan persyaratan staf untuk tugas. Atribut staf ini bersama dengan jadwal tugas digunakan untuk menemukan sumber daya yang tersedia untuk melakukan tugas ini.

   - **Peran**: Tentukan jenis sumber daya yang diperlukan untuk melakukan tugas.
   - **Unit sumber daya**: Tentukan unit asal penetapan sumber daya untuk tugas. Atribut ini mempengaruhi perkiraan biaya dan penjualan untuk tugas jika tingkat biaya dan tagihan untuk sumber daya diatur berdasarkan unit sumber daya.
   - **Nama posisi**: masukkan nama untuk sumber daya generik yang berfungsi sebagai placeholder untuk sumber daya yang pada akhirnya akan melakukan pekerjaan.

Bidang **sumber daya** memegang nama posisi sumber daya generik atau sumber daya yang bernama saat ditemukan.

Bidang **kategori** memiliki nilai yang menunjukkan jenis pekerjaan yang lebih luas yang dapat dikelompokkan dalam tugas. Bidang ini tidak mempengaruhi penjadwalan atau staf. Malah, bidang tersebut hanya digunakan untuk pelaporan.

## <a name="task-dependencies"></a>Dependensi tugas

Anda dapat menggunakan jadwal dalam Project Operations untuk membuat Relasi pendahulu antara tugas. Bidang **sebelumnya** menggunakan satu atau beberapa nilai untuk menunjukkan tugas yang tergantung pada tugas. Bila Anda menetapkan nilai pendahulu tugas, tugas hanya dapat mulai ketika menyelesaikan semua tugas-tugas pendahulunya. Karena dependensi, tanggal mulai yang direncanakan untuk tugas diatur ulang ke tanggal saat tugas pendahulunya selesai.

Mode tugas tidak berpengaruh pada pembaruan yang dibuat pada tanggal mulai dan berakhir dari tugas pendahulu/tergantung.

## <a name="accessibility-and-keyboard-shortcuts"></a>Cara pintas keyboard dan aksesibilitas

Kisi **jadwal** sepenuhnya dapat diakses dan dapat digunakan dengan pembaca layar seperti narrator, JAWS, atau NVDA. Anda dapat berpindah melalui area kisi dengan menggunakan tombol panah (sebagaimana di Microsoft Excel), Anda dapat menggunakan tombol tab untuk memajukan melalui elemen antarmuka pengguna interaktif, dan Anda dapat menggunakan tombol panah bawah, tombol Enter, atau spasi untuk memilih dan membuka menu drop-down.
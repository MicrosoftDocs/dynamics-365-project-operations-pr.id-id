---
title: Parameter manajemen pengeluaran
description: Parameter berikut mengontrol perilaku dalam manajemen Pengeluaran.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 498d597fe811192ce313a1b0384de81e7ef55c58
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271917"
---
# <a name="expense-management-parameters"></a>Parameter manajemen pengeluaran


Parameter mengontrol perilaku umum dalam manajemen Pengeluaran.

### <a name="general"></a>Umum

| **Bidang**                                                | **KETERANGAN**                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| **Tingkat standar jarak tempuh**                             | Masukkan tarif penggantian uang untuk pengeluaran jarak tempuh. Tarif ini akan dikalikan dengan jarak tempuh yang dimasukkan untuk menghitung jumlah pengeluaran yang akan diganti untuk biaya perjalanan.                       |
|**Pengeluaran pribadi dibayarkan oleh**                             | Pilih siapa yang bertanggung jawab untuk membayar jumlah transaksi kartu kredit yang dikategorikan sebagai pribadi.                                                                                                     |
|**Menampilkan seluruh laporan pengeluaran untuk penelusuran**               | Pilih pilihan ini untuk menampilkan semua pengeluaran untuk laporan biaya bila rincian dokumen asli dilihat untuk voucher tertentu yang dihasilkan saat laporan pengeluaran telah diposting.              |
|**Pra-otorisasi perjalanan adalah wajib**                 | Pilih pilihan ini untuk mewajibkan agar permintaan perjalanan diajukan dan disetujui sebelum karyawan dapat mengajukan laporan biaya.                                                                    |
|**Memungkinkan pengeditan distribusi sebelum posting**            | Pilih apakah distribusi laporan pengeluaran dapat diedit sebelum diposting.                                                                                                                 |
|**Evaluasi kebijakan manajemen pengeluaran**                     | Pilih bila pengeluaran dievaluasi untuk menentukan apakah kebijakan pengeluaran telah dilanggar. Biaya dapat diperiksa untuk pelanggaran saat entri pengeluaran masuk dan disimpan, atau bila pengeluaran diajukan untuk disetujui. Aturan kebijakan untuk kuitansi yang diperlukan akan diperiksa bila baris pengeluaran disimpan.                   |
|**Memungkinkan baris pengeluaran Antarperusahaan**                         | Pilih apakah entri pengeluaran untuk entitas hukum lain dapat dimasukkan pada laporan pengeluaran.                                                                                                          |
|**Memungkinkan pengeditan nilai tukar untuk pengeluaran kartu kredit** | Pilih pilihan ini untuk memungkinkan pengguna mengedit nilai tukar untuk pengeluaran kartu kredit impor.                                                                        |
|**Bidang hierarki multi-tingkat untuk menampilkan**                  | Pilih bidang pemberi persetujuan mana yang ditampilkan saat jenis penetapan alur kerja laporan pengeluaran diatur menjadi hierarki, dan pemilihan hierarki diatur untuk menggunakan hierarki persetujuan multi-level pengeluaran. Bila hierarki persetujuan multi-level digunakan untuk alur kerja, bidang yang dipilih akan ditampilkan dan dapat diedit dalam laporan pengeluaran. |
|**Masukkan nomor kartu kredit karyawan (pembaruan Juli 2017)**     | Pilih nomor 15 atau 16 karakter yang dapat dimasukkan dan disimpan dalam bidang **id kartu** pada halaman **kartu kredit** untuk karyawan.                                                                          |

### <a name="financial"></a>Keuangan

| **Bidang**                                                            | **Keterangan**     |
|----------------------------------------------------------------------|------------------------------------|
|**Nama jurnal harian buku besar**                                         | Pilih nama jurnal buku besar untuk memposting laporan pengeluaran yang disetujui.            |
|**Aktifkan pemulihan pajak dari pengeluaran**                                  | Pilih pilihan ini untuk mengaktifkan pemulihan pajak pengeluaran untuk pengeluaran yang memenuhi syarat. Pilihan ini tidak dapat diaktifkan jika pajak penjualan AS dan aturan pajak penggunaan diaktifkan.      |
|**Segera posting kasbon**                                     | Pilih pilihan ini untuk memposting kasbon yang disetujui setelah proses pembayaran dan transfer selesai. Jika pilihan ini tidak dipilih, proses bayar dan transfer menghasilkan jurnal umum yang belum diposting. |
|**Koreksi tanggal akuntansi selama posting**                             | Pilih pilihan ini untuk memperbarui tanggal akuntansi saat pengeluaran diposting, jika periode saat ini ditahan atau ditutup. Tanggal akuntansi akan diatur ke periode buka berikutnya.   |
|**Memungkinkan pengelompokan transaksi berdasarkan akun offset yang ditentukan dalam metode pembayaran**      | Pilih pilihan ini untuk meringkas transaksi pengeluaran untuk laporan pengeluaran, berdasarkan akun offset yang ditentukan dalam metode pembayaran untuk pengeluaran.   
|**Termasuk pajak**                                                   | Pilih pilihan ini untuk menyertakan pajak penjualan dalam jumlah pengeluaran secara default.             |
|**Hilangkan hambatan pada penutupan permintaan perjalanan**            | Pilih pilihan ini untuk melepaskan dana yang terhalang bila permintaan perjalanan yang disetujui ditutup.                                                                                   |
|**Memungkinkan permintaan perjalanan mengajukan kelebihan anggaran untuk daftar anggaran dan anggaran proyek** | Pilih pilihan ini agar karyawan dapat mengirimkan permintaan perjalanan untuk mendapatkan persetujuan yang melebihi anggaran yang diizinkan dan diatur dalam daftar anggaran atau anggaran yang diizinkan untuk proyek.            |
|**Memungkinkan laporan pengeluaran diajukan untuk kelebihan anggaran untuk daftar anggaran dan anggaran proyek**    | Pilih pilihan ini agar karyawan dapat mengajukan laporan pengeluaran untuk mendapatkan persetujuan yang melebihi anggaran yang diizinkan dan diatur dalam daftar anggaran atau anggaran yang diizinkan untuk proyek.                |
|**Memungkinkan persetujuan laporan pengeluaran untuk kelebihan anggaran untuk daftar anggaran saja**                | Pilih pilihan ini untuk mengizinkan pemberi persetujuan menyetujui pengeluaran laporan yang melebihi anggaran yang diizinkan dan diatur dalam daftar anggaran.                                                                       |

### <a name="per-diem"></a>Pembayaran harian

| **Bidang**                             | **KETERANGAN**             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|**Jam minimum untuk uang saku**           | Masukkan jumlah jam minimum default yang harus dilakukan karyawan dalam satu hari agar memenuhi syarat untuk menerima uang saku untuk pengeluaran terkait perjalanan.  Nilai ini hanya digunakan sebagai nilai default untuk bidang jam minimum pada tingkat tarif uang saku.                                                                                      |
|**Persentase makan**                          | Masukkan persentase default uang makan yang digunakan pada hari pertama dan terakhir dari pengeluaran terkait perjalanan bila bidang **hitung pengurangan makan berdasarkan** diatur ke **jenis makanan per hari** atau **jumlah makan per hari**. Hari kerja pada hari pertama dan terakhir mungkin lebih singkat dari hari kerja standar. Oleh karena itu, jumlah uang saku pada hari tersebut mungkin berbeda dari jumlah standar. Jika persentase diatur ke 0 (nol), pengurangan untuk hari pertama dan terakhir akan menjadi 0,00. |
|**Persentase hotel**                        | Masukkan persentase default uang saku untuk hotel yang digunakan pada hari pertama dan terakhir dari pengeluaran terkait perjalanan. Hari kerja pada hari pertama dan terakhir mungkin lebih singkat dari hari kerja standar. Oleh karena itu, jumlah uang saku pada hari tersebut mungkin berbeda dari jumlah standar. Jika persentase diatur ke 0 (nol), pengurangan untuk hari pertama dan terakhir akan menjadi 0,00.                                              |
|**Persentase lainnya**                        | Masukkan persentase default uang saku untuk pengeluaran lain-lain yang digunakan pada hari pertama dan terakhir dari pengeluaran terkait perjalanan. Hari kerja pada hari pertama dan terakhir mungkin lebih singkat dari hari kerja standar. Oleh karena itu, jumlah uang saku pada hari tersebut mungkin berbeda dari jumlah standar. Jika persentase diatur ke 0 (nol), pengurangan untuk hari pertama dan terakhir akan menjadi 0,00.                                                                                                     |
|**Pengurangan persentase untuk sarapan** | Masukkan jumlah uang saku yang dikurangi untuk sarapan. Misalnya, jika karyawan menerima sarapan gratis, Anda mungkin ingin mengurangi jumlah uang saku sebesar 10 persen.                               |
|**Pengurangan persentase untuk makan siang**    | Masukkan jumlah uang saku yang dikurangi untuk makan siang. Misalnya, jika karyawan menerima makan siang gratis, Anda mungkin ingin mengurangi jumlah uang saku sebesar 15 persen.                                       |
|**Pengurangan persentase untuk makan malam**   | Masukkan jumlah uang saku yang dikurangi untuk makan malam. Misalnya, jika karyawan menerima makan malam gratis, Anda mungkin ingin mengurangi jumlah uang saku sebesar 25 persen.                                     |
|**Hitung potongan makanan dengan**         | Pilih bagaimana sistem harus menghitung pengurangan uang makan, dengan memilih apakah pengurangan didasarkan pada jenis makan per perjalanan atau per hari, atau apakah berdasarkan jumlah makanan yang diizinkan per hari.|
|**Pembulatan uang saku**                  | Pilih jenis pembulatan yang digunakan untuk pengeluaran uang saku. Jika Anda memilih pembulatan normal, pengeluaran uang saku yang memiliki jumlah 0,50 dibulatkan menjadi 1,00, dan pengeluaran uang saku yang memiliki jumlah yang kurang dari 0,50 dibulatkan ke 0,00.                                                                                              |
|**Perhitungan uang saku dasar pada**         | Pilih apakah jumlah uang saku didasarkan pada hari kalender atau periode 24 jam.       |

### <a name="fax-cover-pages"></a>Halaman sampul Faks

| **Bidang**                      | **KETERANGAN**            |
|--------------------------------|-----------------------------------------------------------------------------|
| **Petunjuk**                   | Masukkan petunjuk yang harus diikuti karyawan saat membuat halaman sampul untuk Faks yang digunakan untuk mengirim tanda terima yang terkait dengan laporan pengeluaran. Untuk memasukkan teks spesifik bahasa yang akan ditampilkan, berdasarkan bahasa pengguna, klik tombol **terjemahan**. |
|**ID pengguna (informasi kode batang)** | Pilih pilihan ini untuk menyimpan pengidentifikasi unik karyawan dalam kode batang yang digunakan di halaman sampul Faks.                 |
|**Kode batang**                      | Pilih kode batang yang digunakan pada halaman sampul Faks. Kode batang 39 dan 128 didukung dengan manajemen pengeluaran.               |

### <a name="anti-corruption"></a>Anti-korupsi

|                 <strong>Bidang</strong>                 |                                                                                                                                                                                            <strong>Keterangan</strong>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <strong>Tampilkan pengesahan anti-korupsi</strong>  | Pilih pilihan ini untuk menampilkan teks antikorupsi saat laporan pengeluaran dibuat. Kategori pengeluaran tertentu kemudian dapat diaktifkan yang akan memerlukan pengesahan antikorupsi untuk dipilih pada laporan pengeluaran. Misalnya, kategori hadiah yang terkait dengan pengeluaran resmi pemerintah mungkin mengharuskan karyawan mengkonfirmasi bahwa pengeluaran tersebut memenuhi kebijakan perusahaan yang terkait dengan pejabat pemerintah. |
| <strong>Pesan antikorupsi untuk pemohon</strong> |                                                                                             Masukkan teks yang akan ditampilkan kepada karyawan saat membuat laporan pengeluaran baru. Untuk memasukkan teks spesifik bahasa yang akan ditampilkan, berdasarkan bahasa pengguna, klik tombol <strong>terjemahan</strong>.                                                                                             |
| <strong>Pesan antikorupsi untuk pemberi persetujuan</strong>  |                                                                                             Masukkan teks yang akan ditampilkan kepada pemberi persetujuan saat membuat laporan pengeluaran baru. Untuk memasukkan teks spesifik bahasa yang akan ditampilkan, berdasarkan bahasa pengguna, klik tombol <strong>terjemahan</strong>.                                                                                             |



[!INCLUDE[footer-include](../includes/footer-banner.md)]
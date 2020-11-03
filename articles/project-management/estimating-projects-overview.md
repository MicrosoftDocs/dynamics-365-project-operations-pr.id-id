---
title: Ikhtisar estimasi proyek
description: Topik ini menyediakan informasi tentang estimasi di Dynamics 365 Project operations.
author: ruhercul
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8e7ee4888a907b9d8c3ce06c1597f6b05be84477
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078373"
---
# <a name="estimate-projects-overview"></a>Ikhtisar estimasi proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Pada kuotasi berbasis proyek, Anda dapat menggunakan entitas **detail baris kuotasi** untuk memperkirakan pekerjaan yang diperlukan untuk melaksanakan proyek. Selanjutnya Anda dapat berbagi perkiraan dengan pelanggan.

Baris kuotasi berbasis proyek tidak boleh memiliki nol pada banyak detail baris kuotasi. Rincian baris kuotasi digunakan untuk memperkirakan waktu, pengeluaran, atau biaya. Microsoft Dynamics 365 Project Operations tidak memungkinkan perkiraan material pada rincian baris kuotasi. Ini disebut kelas transaksi. Jumlah perkiraan pajak juga dapat dimasukkan pada kelas transaksi.

Selain kelas transaksi, rincian baris kuotasi memiliki jenis transaksi. Dua jenis transaksi didukung untuk rincian baris kuotasi: **biaya** dan **kontrak proyek**.

## <a name="estimate-by-using-a-contract"></a>Perkirakan menggunakan kontrak

Jika Anda menggunakan kuotasi saat membuat kontrak berbasis proyek, perkiraan yang Anda lakukan untuk setiap baris kuotasi pada kuotasi disalin ke kontrak proyek. Struktur kontrak proyek itu seperti struktur kuotasi proyek yang memiliki baris, rincian baris, dan jadwal faktur.

Perkiraan dapat dilakukan secara langsung dalam kontrak proyek, seperti dalam kuotasi proyek. Untuk kuotasi proyek, perkiraan dilakukan dengan menggunakan baris kontrak dan rincian baris kontrak. Rincian baris kontrak juga dapat dibuat dari rencana proyek yang dibuat dengan menggunakan pendekatan perkiraan bottom-up.

Rincian baris kontrak dapat digunakan untuk memperkirakan waktu, pengeluaran, atau biaya. Jumlah perkiraan pajak juga dapat dimasukkan pada rincian baris kontrak.

Estimasi material tidak diizinkan pada rincian baris kontrak.

Proses yang didukung pada kontrak proyek adalah pembuatan faktur dan konfirmasi. Pembuatan faktur membuat draf faktur berbasis proyek yang mencakup semua aktual penjualan yang tidak ditagih hingga tanggal saat ini.

Konfirmasi membuat kontrak hanya baca dan mengubah statusnya dari **draf** menjadi **dikonfirmasi**. Setelah melakukan tindakan ini, Anda tidak dapat mengurungkannya. Karena tindakan ini bersifat permanen, praktik terbaik adalah menjaga kontrak tetap dalam status **draf**.

Satu-satunya perbedaan antara kontrak draft dan kontrak yang dikonfirmasi adalah status mereka dan fakta bahwa kontrak draft dapat diedit sedangkan kontrak yang dikonfirmasi tidak dapat. Pembuatan faktur dan aktual pelacakan dapat dilakukan pada kontrak draf maupun kontrak yang dikonfirmasi.

Project Operations tidak mendukung perubahan perintah pada kontrak atau proyek.

## <a name="estimating-projects"></a>Perkiraan Proyek

Anda dapat memperkirakan waktu dan biaya pada proyek. Project Operations tidak memungkinkan perkiraan material atau biaya pada proyek.

Perkiraan waktu dihasilkan saat Anda membuat tugas dan mengidentifikasi atribut sumber daya umum yang diperlukan untuk melakukan tugas. Perkiraan waktu dihasilkan dari tugas jadwal. Perkiraan waktu tidak dibuat jika Anda membuat anggota tim generik di luar konteks jadwal.

Perkiraan biaya dimasukkan di kisi pada halaman **Perkiraan**.

## <a name="understanding-estimation"></a>Memahami estimasi

Gunakan tabel berikut sebagai panduan untuk memahami logika bisnis dalam fase estimasi.

| Skenario                                                                                                                                                                                                                                                                                                                                          | Rekaman Entitas                                                                                                                                                                                                       | Jenis Transaksi | Kelas Transaksi | Informasi tambahan                                                            |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------|-------------|-----------------------------------------------------------------------------------|
| Bila Anda perlu memperkirakan nilai penjualan waktu pada kuotasi                                                                                                                                                                                                                                                                                    | Rekaman detail baris kuotasi (QLD) dibuat                                                                                                                                                                               | Kontrak proyek | Time        | Bidang asal transaksi pada baris QLD sisi penjualan merujuk pada sisi biaya QLD |
|                                                                                                                                                                                                                                                                                     | Rekaman QLD kedua dibuat oleh sistem untuk menyimpan nilai biaya yang terkait. Semua bidang non-uang disalin dari penjualan QLD ke QLD biaya oleh sistem.                                                                                                                                                                               | Biaya | Time        | Bidang asal transaksi pada baris detail baris kuotasi (QLD) sisi penjualan merujuk pada sisi biaya QLD |
| Bila Anda perlu memperkirakan nilai penjualan waktu pada kontrak                                                                                                                                                                                                                                                                                 | Rekaman detail baris kontrak proyek (CLD) dibuat                                                                                                                                                                    | Kontrak Proyek | Time        | Bidang asal transaksi pada baris CLD sisi penjualan merujuk pada CLD biaya      |
|                                                                                                                                                                                                                                                                                  | Rekaman CLD kedua dibuat oleh sistem untuk menyimpan nilai biaya yang terkait. Semua bidang non-uang disalin dari penjualan CLD ke CLD biaya oleh sistem.                                                                                                                                                                    | Biaya | Time        | Bidang asal transaksi pada baris CLD sisi penjualan merujuk pada CLD biaya      |
| Bila pengguna menjelaskan sumber daya pada tugas proyek                                                                                                                                                                                                                                                                                            | Rekaman baris perkiraan untuk menampilkan nilai penjualan tugas dibuat saat tugas dibuat dengan semua dimensi harga yang diperlukan. Peran dan unit organisasi adalah dimensi harga | Kontrak Proyek | Waktu        |                                                                                   |
|     | Rekaman baris perkiraan untuk menampilkan nilai biaya tugas dibuat saat tugas dibuat dengan semua dimensi harga yang diperlukan. Semua bidang non-uang disalin dari baris perkiraan penjualan ke baris perkiraan biaya oleh sistem. Peran dan unit organisasi adalah dimensi harga baik untuk biaya maupun tarif tagihan.                                                                                                                                                                                                                | Biaya             | Waktu           |                                                                                   |



## <a name="customize-the-quote-line-detail-and-contract-line-detail-entities"></a>Menyesuaikan detail baris kuotasi dan entitas detail baris kontrak

Jika Anda menambahkan bidang kustom pada detail baris kuotasi dan ingin sistem memasukkan nilai bidang sebagai nilai default pada baris biaya terkait yang dibuat, gunakan Alat registrasi plug-in **PreOperationContractLineDetailUpdate** dan **PreOperationQuoteLineDetailUpdate**. Plug-in ini harus didaftarkan ulang setelah detail baris kuotasi atau detail baris kontrak diubah. Untuk menyelesaikan proses ini, ikuti langkah berikut ini.

1. Buka PluginRegistrationTool, dan Sambungkan ke instans online Anda.
2. Pilih **pencarian** , dan Cari plug-in untuk memperbarui.
3. Pilih plug-in, lalu, di halaman utama, klik **pilih**.
4. Pilih langkah plug-in untuk memperbarui, klik kanan, lalu pilih **Perbarui**.
5. Di kotak dialog **Perbarui langkah yang ada** , di bidang **atribut filter** , pilih tombol elipsis ( **...** ):
6. Di kotak dialog **Pilih atribut** , pilih kotak centang untuk atribut kustom.
7. Pilih **OK** untuk menutup kotak dialog, lalu pilih **Perbarui langkah**.
8. Ulangi langkah 1 hingga 7 untuk plug-in kedua.
9. Tutup **PluginRegistrationTool**.

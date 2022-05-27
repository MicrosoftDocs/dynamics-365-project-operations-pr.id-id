---
title: Itemisasi pengeluaran
description: Ini topik menjelaskan cara merinci pengeluaran menggunakan ruang kerja Pengeluaran yang ditata ulang.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 34b11c6bd8be729957973a60fccccc2dd32c2669
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574526"
---
# <a name="expense-itemization"></a>Itemisasi pengeluaran

[!include [banner](../includes/banner.md)]

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Organisasi sering mengharuskan karyawan untuk memberikan rincian rinci biaya yang dikeluarkan selama perjalanan. Misalnya, folio hotel mungkin berisi beberapa jalur terperinci untuk tarif kamar, pajak, parkir, dan biaya lain-lain yang dikeluarkan setiap hari selama durasi menginap. Atau biaya makan mungkin mengharuskan Anda memberikan rincian yang lebih terperinci untuk sarapan, makan siang, atau makan malam. Apa pun kebutuhan organisasi, setiap kategori pengeluaran dapat diatur untuk mencerminkan subkategori atau item baris yang membentuk biaya. Meskipun itemisasi selalu didukung dalam **manajemen Pengeluaran,** ruang kerja pengeluaran **reimagined memungkinkan perincian yang lebih efisien saat fitur,** Kemampuan untuk merinci pengeluaran berulang dengan cepat **diaktifkan**.  

## <a name="enable-quick-itemization"></a>Mengaktifkan perincian cepat 

Anda dapat menggunakan **Kemampuan untuk merinci pengeluaran berulang dengan cepat** untuk merinci pengeluaran berulang dengan cepat sambil menghindari kebutuhan untuk memasukkan pengeluaran harian setiap kali selama masa tinggal. Selesaikan langkah-langkah berikut untuk mengaktifkan itemisasi cepat.

1. Buka **ruang kerja Manajemen** Fitur dan dalam daftar fitur, temukan dan pilih, **Laporan Pengeluaran Yang Ditata Ulang**. 
2. Klik **Aktifkan sekarang**. 
3. Dalam daftar fitur, cari dan pilih, **Kemampuan untuk merinci pengeluaran berulang dengan cepat**.
4. Klik **Aktifkan sekarang**. 

## <a name="itemization-grid"></a>Kisi itemisasi 

Jika kategori pengeluaran memiliki subkategori atau komponen berbeda yang membentuk biaya itu, maka itu dapat dirinci. Untuk merinci pengeluaran, pilih garis pengeluaran dalam laporan pengeluaran, dan di **panel Detail** pengeluaran, pilih **Tindakan** > **Yang Merinci**. Slider **Itemisasi** mengungkapkan kisi dengan bidang. Tabel berikut memberikan contoh setiap bidang dalam kisi dan bagaimana bidang dirender dalam laporan pengeluaran. 

|     Bidang          |     Deskripsi                                                                                  |     Contoh              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subkategori    |     Daftar subkategori yang dikonfigurasi di bawah jenis kategori pengeluaran, **Hotel**.             |     Tarif kamar harian      |
|     Tanggal mulai     |     Tanggal ketika item pengeluaran pertama kali dikeluarkan.                                           |     09/13/2021           |
|     Tarif Harian     |     Jumlah yang dikeluarkan untuk item pengeluaran.                                                    |     200                  |
|     Jumlah       |     Berapa kali muatan diulang selama periode kontinu.                       |     3                    |

![Merinci biaya.](media/Itemization%20screen%201.png)

Saat Anda menyimpan itemisasi, Anda akan melihat baris terperinci individual untuk jumlah yang ditentukan dalam kisi Itemisasi. Setiap baris dimulai pada tanggal yang ditentukan dalam grid.

![Laporan terperinci.](media/Itemization%20screen%202.png)


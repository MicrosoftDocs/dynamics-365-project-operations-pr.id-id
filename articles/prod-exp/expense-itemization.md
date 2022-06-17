---
title: Itemisasi pengeluaran
description: Artikel ini menjelaskan cara merinci pengeluaran menggunakan ruang kerja Biaya yang dirancang ulang.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920938"
---
# <a name="expense-itemization"></a>Itemisasi pengeluaran

[!include [banner](../includes/banner.md)]

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Organisasi sering mengharuskan karyawan untuk memberikan rincian rinci tentang biaya yang dikeluarkan selama perjalanan. Misalnya, folio hotel dapat berisi beberapa baris terperinci untuk tarif kamar, pajak, parkir, dan biaya lain-lain yang dikeluarkan setiap hari selama durasi menginap. Atau biaya makan mungkin mengharuskan Anda memberikan perincian yang lebih terperinci untuk sarapan, makan siang, atau makan malam. Apa pun kebutuhan organisasi, setiap kategori pengeluaran dapat diatur untuk mencerminkan subkategori atau item baris yang membentuk pengeluaran. Meskipun itemisasi selalu didukung dalam **manajemen Pengeluaran,** ruang kerja biaya **yang dirancang ulang memungkinkan itemisasi yang lebih efisien ketika fitur,** Kemampuan untuk merinci pengeluaran berulang dengan cepat **diaktifkan**.  

## <a name="enable-quick-itemization"></a>Aktifkan itemisasi cepat 

Anda dapat menggunakan **fitur Kemampuan untuk merinci pengeluaran berulang dengan cepat** untuk merinci pengeluaran berulang dengan cepat sambil menghindari kebutuhan untuk memasukkan pengeluaran harian setiap kali selama masa tinggal. Selesaikan langkah-langkah berikut untuk mengaktifkan itemisasi cepat.

1. Buka ruang **kerja Manajemen** Fitur dan dalam daftar fitur, temukan dan pilih, **Laporan Pengeluaran Dirancang Ulang**. 
2. Klik **Aktifkan sekarang**. 
3. Dalam daftar fitur, temukan dan pilih, **Kemampuan untuk merinci pengeluaran berulang dengan cepat**.
4. Klik **Aktifkan sekarang**. 

## <a name="itemization-grid"></a>Kisi itemisasi 

Jika kategori pengeluaran memiliki subkategori atau komponen berbeda yang membentuk pengeluaran itu, maka itu dapat dirinci. Untuk merinci pengeluaran, pilih baris pengeluaran dalam laporan pengeluaran, dan di **panel Detail** pengeluaran, pilih **Itemisasi** > **Tindakan**. Penggeser **Itemisasi** mengungkapkan kisi dengan bidang. Tabel berikut ini menyediakan contoh setiap bidang dalam kisi dan bagaimana bidang tersebut dirender dalam laporan pengeluaran. 

|     Bidang          |     Deskripsi                                                                                  |     Contoh              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subkategori    |     Daftar subkategori yang dikonfigurasi di bawah jenis kategori pengeluaran, **Hotel**.             |     Tarif kamar harian      |
|     Tanggal mulai     |     Tanggal ketika item biaya pertama kali dikeluarkan.                                           |     09/13/2021           |
|     Tarif Harian     |     Jumlah yang dikeluarkan untuk item biaya.                                                    |     200                  |
|     Jumlah       |     Berapa kali muatan diulangi dalam periode berkelanjutan.                       |     3                    |

![Perinci pengeluaran.](media/Itemization%20screen%201.png)

Saat Anda menyimpan itemisasi, Anda akan melihat baris individual yang diperinci untuk kuantitas yang ditentukan dalam kisi Itemisasi. Setiap baris dimulai pada tanggal yang ditentukan dalam kisi.

![Laporan terperinci.](media/Itemization%20screen%202.png)


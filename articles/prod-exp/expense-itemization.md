---
title: Itemisasi pengeluaran
description: Artikel ini menjelaskan cara memerinci pengeluaran menggunakan ruang kerja Pengeluaran yang dikaji ulang.
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

Organisasi sering mengharuskan karyawan memberikan perincian pengeluaran terperinci yang dikeluarkan selama perjalanan. Misalnya, tagihan hotel dapat berisi beberapa baris terperinci untuk tarif kamar, pajak, tempat parkir, dan biaya lain yang dikeluarkan setiap hari selama masa tinggal. Atau pengeluaran makan mungkin mengharuskan Anda menyediakan perincian lebih rinci untuk makan pagi, makan siang, atau makan malam. Apa pun kebutuhan organisasi, setiap kategori pengeluaran dapat diatur untuk mencerminkan subkategori atau item baris yang merupakan pengeluaran. Meskipun itemisasi selalu didukung dalam **manajemen Pengeluaran**, ruang kerja **pengeluaran yang dikaji ulang** memungkinkan itemisasi yang lebih efisien saat fitur ini, **Kemampuan untuk memerinci pengeluaran berulang dengan cepat** diaktifkan.  

## <a name="enable-quick-itemization"></a>Aktifkan itemisasi cepat 

Anda dapat menggunakan fitur **Kemampuan untuk memerinci item pengeluaran berulang dengan cepat** untuk memerinci pengeluaran berulang secara cepat, sekaligus menghindari kebutuhan untuk memasukkan pengeluaran harian setiap kali selama durasi tinggal. Selesaikan langkah-langkah berikut untuk mengaktifkan itemisasi cepat.

1. Buka ruang kerja **manajemen fitur** dan di daftar fitur, cari dan pilih **laporan pengeluaran yang dikaji ulang**. 
2. Klik **Aktifkan sekarang**. 
3. Dalam daftar fitur, cari dan pilih, **Kemampuan untuk memerinci pengeluaran berulang dengan cepat**.
4. Klik **Aktifkan sekarang**. 

## <a name="itemization-grid"></a>Kisi itemisasi 

Jika kategori pengeluaran memiliki subkategori atau komponen lain yang membuat pengeluaran tersebut, maka ia dapat diperinci. Untuk memerinci pengeluaran, pilih baris pengeluaran dalam laporan pengeluaran, dan di panel **Rincian pengeluaran**, pilih Tindakan **Itemize** > **Perinci**. Panel geser **Itemisasi** akan membuka kisi dengan bidang. Tabel berikut memberikan contoh tentang setiap bidang pada kisi dan tampilan bidang dalam laporan pengeluaran. 

|     Bidang          |     Description                                                                                  |     Contoh              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Subkategori    |     Daftar subkategori yang dikonfigurasi dalam jenis kategori pengeluaran, **Hotel**.             |     Harga kamar harian      |
|     Tanggal mulai     |     Tanggal saat item pengeluaran dibebankan pertama kali.                                           |     13/09/2021           |
|     Tarif Harian     |     Jumlah yang dibebankan untuk item pengeluaran.                                                    |     200                  |
|     Jumlah       |     Jumlah kali tagihan berulang selama periode kontinu.                       |     3                    |

![Perinci pengeluaran.](media/Itemization%20screen%201.png)

Saat menyimpan itemisasi, Anda akan melihat baris terperinci individual untuk kuantitas yang ditentukan di kisi Itemisasi. Setiap baris dimulai pada tanggal yang ditentukan di kisi.

![Laporan terperinci.](media/Itemization%20screen%202.png)


---
title: Pelacakan penjualan proyek
description: Laporan topik ini berisi informasi tentang cara Project Operations melacak kemajuan terhadap pendapatan tenaga kerja pada proyek.
author: rumant
ms.date: 03/24/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 78d7bdaf9f5ca1757273cb81a1303befb0357ba547eb354097786fc3c38962b9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995585"
---
# <a name="project-sales-tracking"></a>Pelacakan penjualan proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations melacak estimasi tenaga kerja dan pendapatan pada perincian terendah yang diperlukan pada rencana proyek. Estimasi pendapatan tenaga kerja didasarkan pada upaya terencana dan sumber daya generik atau bernama yang ditetapkan ke setiap tugas node leaf dalam rencana proyek. Ketika proyek dimulai dan orang-orang mulai melaporkan waktu pada berbagai tugas proyek, pendapatan aktual pada tenaga kerja diringkas yang memulai perhitungan perkiraan.

## <a name="labor-revenue-tracking-view"></a>Tampilan Pelacakan pendapatan tenaga kerja

Pada halaman **Proyek**, pada tab **Pelacakan**, Anda dapat memilih **Pelacakan** > **Biaya** untuk membuka tampilan Pelacakan **Biaya**. Atau, Anda dapat memilih **Gunakan** > **Tingkat Tagihan** untuk membuka tampilan **Pelacakan Pendapatan**, yang menunjukkan kemajuan pendapatan tenaga kerja pada setiap tugas dalam rencana proyek. Tampilan ini juga membandingkan pendapatan tenaga kerja sebenarnya yang dihabiskan pada suatu tugas dengan pendapatan tenaga kerja yang direncanakan untuk tugas tersebut. Project Operations menggunakan rumus berikut untuk menghitung metrik pendapatan tenaga kerja:

- **Pendapatan yang direncanakan**: Perkiraan nilai penjualan semua penetapan sumber daya pada setiap tugas node leaf
- **Pendapatan Aktual**: Jumlah semua aktual penjualan tak tertagih untuk waktu yang direkam pada tugas
- **Pendapatan Dapat Ditagih%**: Perkiraan pendapatan ÷ perkiraan pendapatan saat selesai
- **Pendapatan Sisa**: perkiraan pendapatan saat selesai – pendapatan aktual
- **Perkiraan Pendapatan saat selesai**: pendapatan sisa + pendapatan aktual
- **Varians Pendapatan**: pendapatan yang direncanakan + perkiraan pendapatan saat selesai


> [!NOTE]
> Project Operations hanya menampilkan pendapatan tenaga kerja pada halaman **Proyek** pada tab **Pelacakan**. Meski bahan dan pengeluaran dapat dianggarkan dan dilacak untuk pemakaian, namun pendapatan tersebut tidak tercakup dalam pendapatan yang ditampilkan di tab **Pelacakan**. Tab ini dirancang untuk berfungsi hanya untuk proyeksi ulang pendapatan tenaga kerja dengan proyeksi ulang upaya.  
> Semua jumlah pendapatan yang ditampilkan dikonversi ke mata uang biaya proyek. Mata uang biaya proyek adalah mata uang dari unit kontrak pada proyek. Untuk proyek harga tetap, angka pendapatan pada tampilan **pelacakan pendapatan Tenaga Kerja** tidak relevan karena aktual penjualan belum tertagih tidak dicatat pada persetujuan waktu.
> Perkiraan nilai penjualan untuk waktu yang ditampilkan pada tab **Estimasi** proyek mungkin tidak akan ditambahkan ke nilai pendapatan terencana di tab **Pelacakan**. Sumber perbedaan ini disebabkan oleh dua kemungkinan alasan:
><ol>
   ><li> Tab <b>Estimasi</b> menampilkan perkiraan pendapatan dalam mata uang penjualan, sedangkan tab <b>Pelacakan</b> menampilkan pendapatan terencana yang dikonversi ke mata uang biaya. </li>
   ><li> Bila perkiraan penjualan dikonversi ke mata uang kontrak seperti ditampilkan pada tab <b>Estimasi</b>, ke mata uang proyek, konversi akan melibatkan langkah-langkah yang dapat mengakibatkan hilangnya keakuratan: </li>
><ol>
><li> Perkiraan jumlah penjualan dalam mata uang kontrak mula-mula dikonversi ke mata uang dasar (konversi 1).</li>
><li> Perkiraan jumlah penjualan dalam mata uang dasar dikonversi ke mata uang biaya proyek (konversi 2). </li>
></ol>
></ol>
> Presisi mata uang diterapkan di kedua langkah tersebut, yang mengakibatkan penyimpangan pendapatan yang direncanakan dalam mata uang proyek dari penjualan yang direncanakan dalam mata uang kontrak.
   

## <a name="reprojecting-revenues-on-leaf-node-tasks"></a>Memproyeksikan ulang pendapatan pada tugas node leaf

Pendapatan tenaga kerja pada tugas node leaf tidak dapat secara langsung diproyeksikan ulang pada tab **Pelacakan** pada halaman **Proyek**. Namun, Anda dapat menggunakan tampilan **Pelacakan Upaya** untuk memproyeksikan ulang upaya lainnya pada tugas. Hal ini menyebabkan penghitungan ulang pendapatan yang tersisa pada tugas. Berikut adalah deskripsi cara kerjanya.

1. Manajer proyek dapat memproyeksikan ulang upaya pada tugas dengan memperbarui nilai default dalam bidang **Upaya Sisa** dengan estimasi baru pada upaya tersisa pada tugas. Memproyeksikan ulang menyebabkan penghitungan ulang estimasi upaya tugas saat selesai (EAC), persentase progres, dan varians upaya perkiraan pada tugas. EAC, estimasi hingga selesai (ETC), dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.
2. Berdasarkan nilai baru untuk upaya yang tersisa dalam tugas, sistem menghitung pendapatan tersisa pada tampilan **Pelacakan Pendapatan**. Untuk menghitung pendapatan yang tersisa berdasarkan upaya yang tersisa, sistem terlebih dulu menghitung pendapatan rata-rata satu jam upaya pada tugas ringkasan sebagai pendapatan terencana atau upaya yang direncanakan. Pendapatan yang direncanakan adalah jumlah pendapatan semua penugasan sumber daya pada tugas. pendapatan rata-rata per jam digunakan untuk menghitung pendapatan tersisa untuk upaya sisa yang baru diproyeksikan pada tugas.
3. Estimasi pendapatan selesai dan pemakaian pendapatan pada tugas node leaf dihitung ulang.
4. Nilai pendapatan saat selesai dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.

## <a name="reprojecting-revenues-on-summary-tasks"></a>Memproyeksikan ulang pendapatan pada tugas ringkasan

Anda dapat mengurangi pendapatan tenaga kerja pada tugas ringkasan atau tugas wadah. Namun, Anda tidak dapat secara langsung memproyeksikan ulang pendapatan tenaga kerja pada tugas proyek ringkasan di tab **Pelacakan** pada halaman **Proyek**. Serupa dengan tugas node leaf, memproyeksikan ulang tugas wadah dan ringkasan dapat dilakukan menggunakan tampilan **Pelacakan Upaya**. Dalam tampilan ini, Anda dapat membuat ulang upaya yang tersisa pada tugas ringkasan yang menyebabkan penghitungan ulang pendapatan yang tersisa pada tugas ringkasan. Berikut adalah deskripsi cara kerjanya.

1. Manajer proyek dapat memproyeksikan ulang upaya pada tugas dengan memperbarui nilai default dalam bidang **Upaya Sisa** dengan estimasi baru pada **upaya tersisa** pada tugas. Memproyeksikan ulang menyebabkan penghitungan ulang estimasi tugas saat selesai (EAC), persentase progres, dan varians upaya perkiraan pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.
2. Berdasarkan nilai baru dalam bidang **upaya yang tersisa** dalam tugas, sistem menghitung pendapatan tersisa pada tampilan **Pelacakan Pendapatan**. Untuk menghitung pendapatan yang tersisa berdasarkan upaya yang tersisa, sistem terlebih dulu menghitung pendapatan rata-rata satu jam upaya pada tugas ringkasan sebagai pendapatan terencana atau upaya yang direncanakan. Pendapatan yang direncanakan adalah jumlah pendapatan semua penugasan sumber daya pada tugas. Pendapatan rata-rata per jam kemudian digunakan untuk menghitung pendapatan untuk upaya sisa yang baru diproyeksikan pada tugas.
3. Estimasi pendapatan selesai dan pemakaian pendapatan pada tugas ringkasan dihitung ulang.
4. Nilai baru untuk estimasi pendapatan saat selesai didistribusikan ke tugas anak di proporsi yang sama seperti pendapatan direncanakan asli pada tugas.
5. Estimasi pendapatan baru saat selesai pada setiap tugas individual hingga tugas node leaf dihitung. Berdasarkan nilai ini, tugas anak yang terpengaruh hingga node leaf akan memiliki sisa pendapatan dan persentase pemakaian pendapatan akan dihitung ulang berdasarkan nilai pendapatan saat selesai. Ini menghasilkan proyeksi baru untuk varians pendapatan dari tugas. 
6. Nilai pendapatan saat selesai dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.


[!INCLUDE[footer-include](../includes/footer-banner.md)]


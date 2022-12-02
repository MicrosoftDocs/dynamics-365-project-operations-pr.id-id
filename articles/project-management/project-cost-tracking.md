---
title: Pelacakan biaya proyek
description: Artikel ini berisi informasi tentang cara Project Operations melacak kemajuan terhadap biaya tenaga kerja dan pengeluaran untuk proyek.
author: rumant
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c069a28c6dc546e5e632c4dff29686dc7965f23e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923744"
---
# <a name="labor-cost-tracking-on-projects"></a>Pelacakan biaya tenaga kerja pada proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations melacak estimasi tenaga kerja dan pengeluaran pada perincian terendah yang diperlukan pada rencana proyek. Estimasi keuangan biaya tenaga kerja didasarkan pada upaya terencana dan sumber daya generik atau bernama yang ditetapkan ke setiap tugas node leaf dalam rencana proyek. Ketika proyek dimulai dan orang-orang mulai melaporkan waktu pada berbagai tugas proyek, belanja aktual pada tenaga kerja diringkas yang memulai perhitungan perkiraan.

## <a name="labor-cost-tracking-view"></a>Tampilan Pelacakan Biaya tenaga kerja

Pada halaman **Proyek**, pada tab **Pelacakan**, Anda dapat memilih **Pelacakan** > **Biaya** untuk membuka tampilan **Pelacakan Biaya** dan melihat kemajuan tenaga kerja yang dihabiskan untuk setiap tugas dalam rencana proyek. Tampilan ini juga membandingkan biaya tenaga kerja sebenarnya yang dihabiskan pada suatu tugas dengan biaya tenaga kerja yang direncanakan untuk tugas tersebut. Project Operations menggunakan rumus berikut untuk menghitung metrik biaya tenaga kerja:

- **Biaya yang direncanakan**: Perkiraan biaya semua penetapan sumber daya pada setiap tugas node leaf
- **Biaya Aktual**: Jumlah semua aktual biaya untuk waktu yang direkam pada tugas
- **Persentase pemakaian biaya**: Perkiraan biaya ÷ Perkiraan biaya saat selesai
- **Biaya Sisa**: Perkiraan biaya saat selesai – biaya aktual
- **Biaya saat Selesai**: biaya sisa + biaya aktual
- **Varians Biaya**: biaya yang direncanakan – estimasi biaya saat selesai

Setiap tugas menampilkan Proyeksi varians biaya terhadap tugas. Jika perkiraan biaya selesai lebih dari biaya yang direncanakan, maka tugas tersebut diproyeksikan akan melebihi anggaran. Jika perkiraan biaya selesai kurang dari biaya yang direncanakan, maka tugas tersebut diproyeksikan selesai di bawah anggaran.

>[!NOTE]
> Project Operations hanya menampilkan biaya tenaga kerja pada halaman **Proyek** pada tab **Pelacakan**. Meski bahan dan pengeluaran dapat dianggarkan dan dilacak untuk pemakaian, namun biaya tersebut tidak tercakup dalam biaya yang ditampilkan di tab **Pelacakan**. Tab ini dirancang untuk berfungsi hanya untuk proyeksi ulang biaya tenaga kerja dengan proyeksi ulang upaya.
Semua jumlah biaya yang ditampilkan dikonversi ke mata uang biaya proyek dari mata uang harga biaya proyek yang digunakan untuk menentukan tingkat biaya. Mata uang biaya proyek adalah mata uang dari unit kontrak pada proyek. Perkiraan nilai biaya untuk waktu yang ditampilkan pada tab **Estimasi** pada halaman **Proyek** mungkin tidak akan ditambahkan ke biaya yang direncanakan pada tab **Pelacakan**. Alasan perbedaan ini adalah karena perbedaan dalam ringkasan perkiraan biaya pada kisi **Estimasi** dan perhitungan biaya yang direncanakan pada kisi diagram **Pelacakan**. 
>
> - **Tab Estimasi** menghitung perkiraan biaya dengan menggunakan mata uang yang sama pada tingkat biaya dalam daftar harga. Kemudian, perkiraan biaya dalam mata uang daftar harga dikonversi ke perkiraan biaya dalam mata uang biaya proyek. Perkiraan biaya dalam mata uang proyek ditampilkan bulat hingga 2 tempat desimal. Pada titik apa pun selama konversi ini, presisi mata uang diterapkan. 
> - Pada tab **Pelacakan**, perhitungan biaya yang direncanakan mengikuti urutan perhitungan yang sedikit berbeda dan melibatkan presisi mata uang yang diterapkan dalam dua tahapan: 
   ><ol>
   ><li>Perkiraan jumlah biaya dalam mata uang daftar harga dikonversi ke mata uang dasar (konversi 1).</li>
   ><li>Perkiraan jumlah biaya dalam mata uang dasar dikonversi ke mata uang biaya proyek (konversi 2). </li>
   ></ol>
   >Presisi mata uang diterapkan di kedua langkah tersebut untuk mendapatkan biaya terencana (pada tab **Pelacakan**) yang menyimpang sedikit sedikit dari perkiraan biaya (pada tampilan **Waktu - fase** pada tab **Estimasi**). 
   
## <a name="reprojecting-costs-on-leaf-node-tasks"></a>Memproyeksikan ulang biaya pada tugas node leaf

Biaya tenaga kerja pada tugas node leaf tidak dapat secara langsung diproyeksikan ulang pada tab **Pelacakan** pada **halaman Proyek**. Namun, Anda dapat menggunakan tampilan **Pelacakan Upaya** untuk memproyeksikan ulang upaya lainnya pada tugas. Hal ini menyebabkan penghitungan ulang biaya yang tersisa pada tugas. Berikut adalah deskripsi cara kerjanya.

1. Manajer proyek dapat memproyeksikan ulang upaya pada tugas dengan memperbarui nilai default dalam bidang **Upaya Sisa** dengan estimasi baru pada upaya tersisa pada tugas. Memproyeksikan ulang menyebabkan penghitungan ulang estimasi upaya tugas saat selesai (EAC), persentase progres, dan varians upaya perkiraan pada tugas. EAC, estimasi hingga selesai (ETC), dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.
2. Berdasarkan nilai baru untuk upaya yang tersisa dalam tugas, sistem menghitung biaya lainnya pada tampilan **Pelacakan Biaya**. Untuk menghitung biaya yang tersisa berdasarkan upaya yang tersisa, sistem terlebih dulu menghitung biaya rata-rata satu jam upaya pada tugas sebagai biaya terencana atau upaya yang direncanakan. Biaya yang direncanakan adalah jumlah biaya semua penugasan sumber daya pada tugas. Biaya rata-rata per jam digunakan untuk menghitung biaya tersisa untuk upaya sisa yang baru diproyeksikan pada tugas.
3. Persentase biaya selesai dan pemakaian biaya pada tugas node leaf dihitung ulang.
4. Nilai biaya saat selesai dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.

## <a name="reprojecting-costs-on-summary-tasks"></a>Memproyeksikan ulang biaya pada tugas ringkasan

Anda dapat mengurangi biaya tenaga kerja pada tugas ringkasan atau tugas wadah. Namun, Anda tidak dapat secara langsung memproyeksikan ulang biaya tenaga kerja pada tugas proyek ringkasan di tab **Pelacakan** pada halaman **Proyek**. Serupa dengan tugas node leaf, memproyeksikan ulang tugas wadah dan ringkasan dapat dilakukan menggunakan tampilan **Pelacakan Upaya**. Dalam tampilan ini, Anda dapat membuat ulang upaya yang tersisa pada tugas ringkasan yang menyebabkan penghitungan ulang biaya yang tersisa pada tugas ringkasan. Berikut adalah deskripsi cara kerjanya.

1. Manajer proyek dapat memproyeksikan ulang upaya pada tugas ringkasan dengan memperbarui nilai default dari upaya yang tersisa dengan estimasi baru pada tugas. Pembaruan ini menyebabkan penghitungan ulang estimasi tugas ringkasan saat selesai (EAC), persentase progres, dan varians upaya perkiraan pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.
2. Berdasarkan nilai baru untuk upaya yang tersisa dalam tugas ringkasan, sistem menghitung biaya lainnya pada tampilan **Pelacakan Biaya**. Untuk menghitung biaya yang tersisa berdasarkan upaya yang tersisa, sistem terlebih dulu menghitung biaya rata-rata satu jam upaya pada tugas ringkasan sebagai biaya terencana atau upaya yang direncanakan. Biaya rata-rata per jam digunakan untuk menghitung biaya untuk upaya sisa yang baru diproyeksikan pada tugas ringkasan.
3. Persentase biaya selesai dan pemakaian biaya pada tugas ringkasan dihitung ulang.
4. Biaya baru saat selesai didistribusikan ke tugas anak di proporsi yang sama seperti biaya direncanakan asli pada tugas.
5. Nilai biaya baru saat selesai pada setiap tugas individual hingga tugas node leaf dihitung. Berdasarkan nilai ini, tugas anak yang terpengaruh hingga node leaf akan memiliki sisa biaya dan persentase pemakaian biaya akan dihitung ulang berdasarkan nilai biaya saat selesai. Nilai ini menghasilkan proyeksi baru untuk varians biaya dari tugas. 


Bidang **performa biaya** dapat diatur dari data pelacakan. Bila varians biaya untuk node root dalam tampilan **pelacakan Biaya** negatif, Anda dapat mengatur bidang ini ke **Di bawah Anggaran**. Bila varians biaya untuk node root positif, Anda dapat mengatur nilai ke **Di atas anggaran**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Mengapa harga diatur default ke nol pada pengeluaran penjualan aktual?
description: Tiga pemeriksaan berikut akan membantu Anda memecahkan masalah mengapa harga diatur default ke 0 pada pengeluaran penjualan aktual.
author: rumant
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d4910d3727085a45036f3b438ecd69abc3e99836
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146307"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Mengapa harga diatur default ke nol pada pengeluaran penjualan aktual?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

FAQ ini berlaku untuk pengeluaran aktual di mana kelas transaksi diatur ke pengeluaran dan jenis transaksi adalah Penjualan Tak Ditagih. Tiga pemeriksaan berikut akan membantu Anda memecahkan masalah mengapa harga (tarif tagihan) diatur default ke 0 pada pengeluaran penjualan aktual.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Periksa 1: Mengidentifikasi daftar harga penjualan untuk proyek

Temukan proyek dari bidang proyek aktual dan buka halaman proyek. Lalu buka tab penjualan. Pada kisi baris kontrak proyek, klik link dalam bidang kontrak proyek. Halaman kontrak proyek akan terbuka. Di halaman kontrak proyek, buka tab daftar harga proyek. centang jika ada minimal satu daftar harga yang terlampir di sini.

Jika tidak ada daftar harga dilampirkan dalam kisi daftar harga proyek kontrak proyek:

- Lampirkan daftar harga untuk kisi daftar harga proyek. Daftar harga yang diizinkan untuk dilampirkan di sini harus memiliki bidang konteks diatur ke penjualan dan bidang mata uang pada daftar harga harus sesuai dengan bidang mata uang kontrak proyek. Setelah Anda membuat perbaikan diperlukan, buat ulang entri pengeluaran, setujui, dan verifikasi bahwa penjualan tertagih aktual menunjukkan harga yang valid.
- Jika Anda memiliki satu atau beberapa daftar harga terlampir dalam kisi daftar harga proyek kontrak proyek, buka Centang 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Periksa 2: Apakah salah satu daftar harga yang tercantum di atas berlaku untuk tanggal tertentu pengeluaran aktual?

Agar project service mempertimbangkan daftar harga untuk default harga, daftar harga tersebut harus berlaku untuk tanggal di pengeluaran penjualan aktual. Periksa berikut untuk melihat apakah daftar harga yang tercantum di atas berlaku:

- Mulai dengan memeriksa apakah tanggal mulai dan berakhir pada tab Umum untuk daftar harga yang terlampir tidak kosong. Jika tanggal mulai dan berakhir pada harga yang tercantum di atas daftar kosong, Anda telah mengisolasi masalah. 
- Buat catatan dari bidang tanggal mulai pada pengeluaran penjualan aktual dan periksa apakah salah satu daftar harga yang tercantum berlaku untuk tanggal itu. Misalnya, tanggal pengeluaran aktual harus berada dalam tanggal mulai dan tanggal berakhir pada daftar harga. 
    - Jika tidak ada daftar harga yang mencakup tanggal di pengeluaran penjualan aktual, Anda telah mengisolasi masalah. Modifikasi tanggal mulai dan berakhir daftar harga untuk memastikan bahwa daftar harga mencakup tanggal pengeluaran aktual. 
    - Jika lebih dari atu daftar harga yang mencakup tanggal di pengeluaran penjualan aktual, Anda telah mengisolasi masalah. Edit tanggal berakhir dan mulai dari daftar harga sehingga ada hanya satu daftar harga yang mencakup tanggal pengeluaran aktual. 
    - Jika ada hanya satu daftar harga yang mencakup tanggal pengeluaran aktual, beralih ke Centang 3.
Setelah Anda membuat perbaikan diperlukan, buat ulang entri pengeluaran, setujui, dan verifikasi bahwa penjualan tertagih aktual menunjukkan harga yang valid.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Centang 3: Apakah ada harga yang valid untuk kategori pengeluaran dalam daftar harga proyek berlaku? 

Jika Anda telah berhasil menyelesaikan Centang 1 dan Centang 2, sekarang Anda seharusnya memiliki hanya satu daftar harga proyek yang dapat diterapkan pada tanggal penjualan pengeluaran aktual. Buka daftar harga proyek dan buka tab kategori harga. Pastikan bahwa terdapat baris di kisi untuk kategori pengeluaran tertentu pada biaya aktual.
 
- Jika tidak ada baris, maka Anda telah mengisolasi masalah. Buat baris di kisi harga kategori untuk kategori pada pengeluaran aktual Anda. Kemudian, buat ulang entri pengeluaran, setujui, dan verifikasi bahwa penjualan tertagih aktual menunjukkan harga yang valid. 
- Jika ada baris untuk kategori pengeluaran dalam kisi harga kategori, periksa apakah memiliki harga yang valid.

Untuk memahami apa itu harga yang valid, gunakan metode ini:

- Jika bidang metode harga pada baris harga kategori diatur ke pada biayanya, maka tarif per unit pada penjualan pengeluaran aktual akan distandarkan ke nilai dalam entri pengeluaran.
- Jika bidang metode harga pada baris harga kategori diatur ke persentase Markup, Periksa apakah bidang persen diatur ke nilai yang valid. Tingkat tarif per unit pada penjualan pengeluaran aktual distandarkan dengan menerapkan persen markup ini pada harga dalam entri pengeluaran.
- Jika bidang metode harga pada baris harga kategori diatur ke harga per unit, Periksa apakah bidang harga diatur ke nilai yang valid. Tarif per unit pada penjualan pengeluaran aktual akan distandarkan dengan jumlah mata uang yang ditentukan di bidang harga.

Jika konfigurasi harga kategori pengeluaran tidak valid, maka Anda telah mengisolasi masalah. Solusinya adalah untuk mengedit baris harga kategori dengan harga yang valid untuk kategori pengeluaran sesuai dengan aturan di atas. Setelah ini dilakukan, buat ulang entri pengeluaran, setujui, dan verifikasi bahwa penjualan tertagih aktual mendapatkan harga yang valid.

Jika Anda tetap tidak melihat harga yang valid pada pengeluaran penjualan aktual setelah melakukan pemeriksaan tiga di atas, buat log tiket dukungan.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
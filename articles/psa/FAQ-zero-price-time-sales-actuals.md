---
title: Mengapa harga diatur default ke nol pada waktu penjualan aktual?
description: Pemecahan masalah mengapa harga diatur default ke nol pada penjualan waktu aktual.
author: rumant
manager: kfend
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
ms.openlocfilehash: 5106e8c1a059bbb0efbeb73dc63e03e8bc9e4b7b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125947"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Mengapa harga diatur default ke nol pada waktu penjualan aktual?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

FAQ ini berlaku untuk nilai aktual di mana kelas transaksi diatur ke waktu dan jenis transaksi adalah Penjualan Tak Ditagih. Tiga pemeriksaan berikut akan membantu Anda memecahkan masalah mengapa harga (tarif tagihan) diatur default ke 0 pada waktu penjualan aktual.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Periksa 1: Mengidentifikasi daftar harga penjualan untuk proyek

Temukan proyek dari bidang proyek aktual dan buka halaman proyek. Lalu buka tab penjualan dan pada kisi baris kontrak proyek, klik link dalam bidang kontrak proyek. Halaman kontrak proyek akan terbuka. Di halaman kontrak proyek, buka tab daftar harga proyek. centang jika ada minimal satu daftar harga yang terlampir di sini. Jika tidak ada daftar harga dilampirkan dalam kisi daftar harga proyek kontrak proyek, Anda telah mengisolasi masalah. Lampirkan daftar harga untuk kisi daftar harga proyek. Daftar harga yang diizinkan untuk dilampirkan di sini harus memiliki bidang konteks diatur ke penjualan dan bidang mata uang pada daftar harga harus sesuai dengan bidang mata uang kontrak proyek. Setelah Anda membuat perbaikan diperlukan, buat ulang entri waktu, setujui, dan verifikasi bahwa penjualan tertagih aktual menunjukkan harga yang valid. 

Jika Anda memiliki satu atau beberapa daftar harga terlampir dalam kisi daftar harga proyek kontrak proyek, lanjutkan ke centang berikutnya dalam dokumen ini.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Centang 2: Apakah salah satu daftar harga yang tercantum di atas berlaku untuk tanggal tertentu penjualan waktu aktual?

Agar project service mempertimbangkan daftar harga untuk default harga, daftar harga tersebut harus berlaku untuk tanggal di penjualan waktu aktual. Periksa berikut untuk melihat apakah daftar harga yang tercantum di atas berlaku:
- Periksa apakah tanggal mulai dan berakhir pada tab Umum untuk daftar harga yang terlampir tidak kosong. Jika tanggal mulai dan berakhir pada harga yang tercantum di atas daftar kosong, Anda telah mengisolasi masalah. 
- Buat catatan dari bidang tanggal mulai pada penjualan waktu aktual dan periksa apakah salah satu daftar harga yang tercantum berlaku untuk tanggal itu. Misalnya, tanggal penjualan waktu aktual harus berada dalam tanggal mulai dan tanggal berakhir pada daftar harga. 
    - Jika tidak ada daftar harga yang mencakup tanggal di penjualan waktu aktual, Anda telah mengisolasi masalah. Modifikasi tanggal mulai dan berakhir daftar harga untuk memastikan bahwa daftar harga mencakup tanggal penjualan waktu aktual. 
    - Jika lebih dari atu daftar harga yang mencakup tanggal di penjualan waktu aktual, Anda telah mengisolasi masalah. Anda dapat memperbaiki ini dengan mengedit tanggal berakhir dan mulai dari daftar harga sehingga ada hanya satu daftar harga yang mencakup tanggal penjualan waktu aktual. 
    - Jika ada hanya satu daftar harga yang mencakup tanggal penjualan waktu aktual, beralih ke Centang 3.
Setelah Anda membuat perbaikan diperlukan, buat ulang entri waktu, setujui, dan verifikasi bahwa penjualan waktu aktual menunjukkan harga yang valid.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Centang 3: Apakah ada harga dalam daftar harga untuk dimensi harga pada penjualan waktu aktual?

Jika Anda telah berhasil menyelesaikan Centang 1 dan Centang 2, sekarang Anda seharusnya memiliki hanya satu daftar harga yang dapat diterapkan pada tanggal penjualan waktu aktual. Buka daftar harga proyek dan telusuri ke tab Harga Peran. Pastikan bahwa terdapat baris di kisi untuk dimensi harga pada penjualan waktu aktual.

Jika tidak ada baris di kisi harga peran untuk dimensi harga pada penjualan waktu aktual, Anda telah mengisolasi masalah. Buat baris di kisi harga peran untuk dimensi harga pada penjualan waktu aktual Anda. Setelah ini dilakukan, buat ulang entri waktu, setujui, dan verifikasi bahwa penjualan waktu aktual menunjukkan harga yang valid.

Jika Anda tetap tidak melihat harga yang valid pada penjualan waktu aktual setelah melakukan pemeriksaan tiga di atas, buat log tiket dukungan. 


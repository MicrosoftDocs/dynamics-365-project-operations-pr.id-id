---
title: Mengapa harga diatur default ke nol pada biaya waktu aktual?
description: Pemecahan masalah mengapa harga diatur default ke nol pada biaya waktu aktual.
author: rumant
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 1421f83458cf0aee4e70858e83d4c54179ff87e3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8588234"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Mengapa harga diatur default ke nol pada biaya waktu aktual?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

FAQ ini berlaku untuk nilai aktual di mana kelas transaksi diatur ke waktu dan jenis transaksi adalah biaya. Tiga pemeriksaan berikut akan membantu Anda memecahkan masalah mengapa harga diatur default ke 0 pada biaya waktu aktual.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Periksa 1: Mengidentifikasi daftar harga biaya untuk proyek

Temukan proyek dari bidang proyek aktual lalu buka halaman proyek. Klik link unit kontrak pada bidang. Pada halaman Unit kontrak, periksa apakah unit kontrak memiliki daftar harga dalam kisi daftar harga biaya.

Jika lebih dari satu daftar harga, Anda telah mengisolasi masalah. Project Service hanya mendukung satu daftar harga per unit organisasional. Hapus semua daftar harga dari entitas ini hingga ada hanya satu daftar harga yang terlampir di kisi daftar harga biaya unit organisasional.

Jika tidak ada daftar harga yang dilampirkan ke Unit organisasional, catat mata uang unit organisasional. Buka project service dan parameter, lalu buka tab daftar harga. Centang jika ada daftar harga dengan konteks diatur ke biaya dan mata uang yang sesuai dengan mata uang Unit organisasional.
 
Jika tidak ada daftar harga yang sesuai dengan kriteria tersebut, Anda telah mengisolasi masalah. Pastikan Anda memiliki minimal satu daftar harga dengan konteks yang diatur ke biaya dan mata uang yang sesuai dengan mata uang Unit organisasional.

Jika terdapat lebih dari satu daftar harga yang cocok dengan kriteria, Lanjutkan membaca dokumen ini untuk membuat lebih banyak pemeriksaan.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Centang 2: Apakah salah satu daftar harga yang tercantum di atas berlaku untuk tanggal tertentu biaya waktu aktual?

Agar project service mempertimbangkan daftar harga untuk default harga, daftar harga tersebut harus berlaku untuk tanggal di biaya waktu aktual. Periksa berikut untuk melihat apakah daftar harga yang tercantum di atas berlaku:

- Periksa apakah tanggal mulai dan berakhir pada tab Umum untuk daftar harga yang terlampir tidak kosong. Jika tanggal mulai dan berakhir pada harga yang tercantum di atas daftar kosong, Anda telah mengisolasi masalah. 
- Buat catatan dari bidang tanggal mulai pada biaya waktu aktual dan periksa apakah salah satu daftar harga yang tercantum berlaku untuk tanggal itu. Misalnya, tanggal biaya waktu aktual harus berada dalam tanggal mulai dan tanggal berakhir pada daftar harga. 
    - Jika tidak ada daftar harga yang mencakup tanggal di biaya waktu aktual, Anda telah mengisolasi masalah. Modifikasi tanggal mulai dan berakhir daftar harga untuk memastikan bahwa daftar harga mencakup tanggal biaya waktu aktual. 
    - Jika lebih dari atu daftar harga yang mencakup tanggal di biaya waktu aktual, Anda telah mengisolasi masalah. Anda dapat memperbaiki ini dengan mengedit tanggal berakhir dan mulai dari daftar harga sehingga ada hanya satu daftar harga yang mencakup tanggal biaya waktu aktual. 
    - Jika ada hanya satu daftar harga yang mencakup tanggal waktu biaya aktual, beralih ke Centang berikutnya dalam dokumen.
Setelah Anda membuat perbaikan diperlukan, buat ulang entri waktu, setujui, dan verifikasi bahwa biaya waktu aktual menunjukkan harga yang valid.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Periksa 3: Apakah ada harga dalam daftar harga untuk dimensi harga pada biaya waktu aktual?

Jika Anda telah berhasil menyelesaikan Centang 1 dan Centang 2, sekarang Anda seharusnya memiliki hanya satu daftar harga yang dapat diterapkan pada tanggal biaya waktu aktual. Buka daftar harga proyek dan buka tab Harga Peran. Pastikan bahwa terdapat baris di kisi untuk dimensi harga pada biaya waktu aktual.

Jika tidak ada baris di kisi harga peran untuk dimensi harga pada waktu biaya aktual, Anda telah mengisolasi masalah. Buat baris di kisi harga peran untuk dimensi harga pada biaya waktu aktual Anda. Setelah ini dilakukan, buat ulang entri waktu, setujui, dan verifikasi bahwa biaya waktu aktual menunjukkan harga yang valid.
 
Jika Anda tetap tidak melihat harga yang valid pada biaya waktu aktual setelah melakukan pemeriksaan tiga di atas, buat log tiket dukungan.





[!INCLUDE[footer-include](../includes/footer-banner.md)]

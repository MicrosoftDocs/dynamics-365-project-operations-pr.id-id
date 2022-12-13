---
title: Menutup kuotasi berbasis proyek
description: Artikel ini memberikan informasi tentang menutup kuotasi proyek di Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7b35417d4258a1e837fdf7a61bbcc303ec04a900
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824221"
---
# <a name="close-project-based-quotes"></a>Menutup kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Kutipan proyek dapat ditutup sebagai **menang** atau **kalah**. 

## <a name="close-a-quote-as-won"></a>Menutup kuotasi sebagai Menang

Penutupan kuotasi proyek sebagai menang akan menentukan status kuotasi ke **ditutup** dan alasan status ke **menang**. Menutup kuotasi membuatnya hanya baca dan membuat kontrak proyek draf dengan semua informasi kuotasi. Karena kuotasi yang ditutup tidak dapat dibuka kembali, sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.

Kontrak proyek yang dibuat dari kuotasi proyek juga dibuat tersedia di modul manajemen proyek dan Akuntansi dari Project Operations. Jika kontrak proyek tidak dipetakan ke proyek pada salah satu baris, kontrak proyek ini dibuat tersedia sebagai kontrak proyek tidak aktif dan menjadi aktif segera setelah proyek dipetakan ke setidaknya satu baris kontraknya.

Jika kuotasi dilampirkan pada peluang, setiap proyek lain pada peluang ditutup secara otomatis sebagai Kalah.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Dampak keuangan menutup kuotasi sebagai menang

Jika ada aktual apa pun untuk waktu yang direkam pada proyek saat masih dilampirkan pada kuotasi draf, hanya biaya waktu atau pengeluaran yang tercatat. Setelah kuotasi ditutup sebagai menang, aplikasi akan merefaktorisasi biaya dengan membalik aktual biaya yang lebih lama dan membuat ulang aktual biaya baru. Aplikasi akan memproses aktual biaya ini berdasarkan metode penagihan pada baris kontrak proyek terkait. Jika aktual biaya merujuk pada baris waktu dan kontrak material, sistem akan secara otomatis membuat aktual penjualan tidak tertagih yang sesuai saat kuotasi ditutup dan kontrak proyek dibuat. Jika aktual biaya merujuk baris kontrak harga tetap, aplikasi akan menghentikan pemrosesan ulang aktual biaya berdasarkan aturan penagihan terpisah untuk pelanggan kontrak proyek.

Semua aktual yang diproses ulang tersedia dalam modul manajemen proyek dan akuntansi agar akuntan proyek dapat meninjau, memperbarui, dan mengeposkan ke buku besar. 

## <a name="close-a-quote-as-lost"></a>Menutup kuotasi sebagai kalah

Penutupan kuotasi proyek sebagai kalah akan menentukan status ke **ditutup** dan alasan status ke **kalah**. Menutup kuotasi membuatnya hanya baca. Karena kuotasi yang ditutup tidak dapat dibuka kembali, dan sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.

Jika kuotasi proyek yang ditutup sebagai hilang kalah memiliki proyek yang dirujuk pada salah satu baris, proyek tersebut juga ditandai sebagai Ditutup dan setiap Pemesanan sumber daya dari hari itu ke depan dibatalkan.

> [!NOTE]
> Dalam Project Operations, penutupan kuotasi karena menang atau kalah tidak akan memengaruhi status peluang, yang akan tetap terbuka hingga ditutup secara manual.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

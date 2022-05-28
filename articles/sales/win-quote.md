---
title: Tutup kuotasi
description: Topik ini memberikan informasi tentang menutup kuotasi proyek di Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 25f5a515769b97e963b2a2ac8738884b3f0db2fb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598584"
---
# <a name="close-a-quote"></a>Tutup kuotasi

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Kuotasi proyek dapat ditutup sebagai menang atau kalah. Karena fungsi Aktifkan dan Revisi tidak didukung pada kuotasi di Microsoft Dynamics 365 Project Operations, Anda dapat menutup kuotasi draf.

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
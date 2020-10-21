---
title: Tutup kuotasi
description: Topik ini memberikan informasi tentang menutup kuotasi proyek di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896195"
---
# <a name="close-quotes"></a>Tutup kuotasi 

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Kuotasi proyek dapat ditutup sebagai menang atau kalah. Operasi mengaktifkan dan merevisi pada kuotasi tidak didukung dalam Microsoft Dynamics 365 Project Operations, sehingga Anda dapat menutup draf kuotasi.

## <a name="close-a-quote-as-won"></a>Menutup kuotasi sebagai Menang

Penutupan kuotasi proyek sebagai menang akan menutup kuotasi dengan status diatur ke ditutup dan alasan status ke menang. Menutup kuotasi membuat kuotasi proyek hanya bisa dibaca dan membuat kontrak proyek draf yang berisi informasi kuotasi. Karena kuotasi yang ditutup tidak dapat dibuka kembali, ada dialog konfirmasi sebelum perubahan dilakukan karena kuotasi yang ditutup tidak dapat dibuka kembali dan perubahannya tidak dapat diubah.

Jika kuotasi dilampirkan pada peluang, setiap proyek lain pada peluang ditutup secara otomatis sebagai Kalah.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Dampak keuangan menutup kuotasi sebagai menang

Jika ada aktual apa pun untuk waktu yang direkam pada proyek saat masih dilampirkan pada kuotasi draf, hanya biaya waktu atau pengeluaran yang tercatat. Setelah kuotasi ditutup sebagai menang, aplikasi akan merefaktorisasi biaya dengan membalik aktual biaya yang lebih lama dan membuat ulang aktual biaya baru. Aplikasi akan memproses aktual biaya ini berdasarkan metode penagihan pada baris kontrak proyek terkait. Jika aktual biaya merujuk pada baris waktu dan kontrak material, sistem akan secara otomatis membuat aktual penjualan tidak tertagih yang sesuai saat kuotasi ditutup dan kontrak proyek dibuat. Jika aktual biaya merujuk baris kontrak harga tetap, aplikasi akan menghentikan pemrosesan ulang aktual biaya berdasarkan aturan penagihan terpisah untuk pelanggan kontrak proyek.

## <a name="closing-a-quote-as-lost"></a>Menutup kuotasi sebagai kalah:

Penutupan kuotasi proyek sebagai kalah akan menentukan status ke ditutup dan alasan status ke kalah. Penutupan kuotasi membuat kuotasi proyek hanya bisa dibaca. Karena kuotasi yang ditutup tidak dapat dibuka kembali, dan sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.

Jika kuotasi proyek yang ditutup sebagai hilang kalah memiliki proyek yang dirujuk pada salah satu baris, proyek tersebut juga ditandai sebagai Ditutup dan setiap Pemesanan sumber daya dari hari itu ke depan dibatalkan.

> [!NOTE]
> Dalam Project Operations, penutupan kuotasi karena menang atau kalah tidak akan memengaruhi status peluang, yang akan tetap terbuka hingga ditutup secara manual.

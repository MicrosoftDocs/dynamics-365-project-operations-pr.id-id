---
title: Menutup kuotasi - lite
description: Topik ini memberikan informasi tentang menutup kuotasi proyek di Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: bde4794c19dd69b6dd77abf5483c674cd7503d23
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574710"
---
# <a name="close-a-quote---lite"></a>Menutup kuotasi - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Kuotasi proyek dapat ditutup sebagai menang atau kalah. Kuotasi draf dapat ditutup karena operasi Aktifkan dan Revisi pada kuotasi tidak didukung di Microsoft Dynamics 365 Project Operations.

## <a name="close-a-quote-as-won"></a>Menutup kuotasi sebagai Menang

Bila Anda menutup kuotasi proyek sebagai Menang, status diatur ke Ditutup dan alasan status adalah Menang. Menutup kuotasi membuat kuotasi proyek hanya bisa dibaca dan membuat kontrak proyek draf yang berisi informasi kuotasi. Karena kuotasi tertutup tidak dapat dibuka kembali, dialog konfirmasi akan mengkonfirmasikan perubahan Anda.

Jika kuotasi dilampirkan pada peluang, setiap proyek lain pada peluang ditutup secara otomatis sebagai Kalah.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Dampak keuangan menutup kuotasi sebagai menang

Jika ada aktual selama waktu proyek saat masih terlampir pada draf kuotasi, hanya biaya waktu atau pengeluaran yang dicatat. Setelah kuotasi ditutup sebagai menang, aplikasi akan merefaktorisasi biaya dengan membalik aktual biaya yang lebih lama dan membuat ulang aktual biaya baru. Aplikasi akan memproses aktual biaya ini berdasarkan metode penagihan pada baris kontrak proyek terkait. Jika aktual biaya mengacu ke waktu dan baris kontrak material, aktual penjualan tidak tertagih yang tidak terkait dibuat untuk saat kuotasi ditutup dan kontrak proyek dibuat. Jika aktual biaya mengacu ke baris kontrak harga tetap, aplikasi akan berhenti memproses ulang aktual biaya yang didasarkan pada aturan penagihan terpisah untuk pelanggan kontrak proyek.

## <a name="closing-a-quote-as-lost"></a>Menutup kuotasi sebagai kalah:

Bila Anda menutup kuotasi proyek sebagai Kalah, status diatur ke Ditutup dan alasan status adalah Kalah. Penutupan kuotasi membuat kuotasi proyek hanya bisa dibaca. Karena kuotasi yang ditutup tidak dapat dibuka kembali, dan sebelum Anda menutup kuotasi, dialog konfirmasi akan mengonfirmasi perubahan Anda.

Jika kuotasi proyek yang ditutup sebagai Kalah mengacu ke proyek pada salah satu barisnya, proyek tersebut juga ditandai sebagai Ditutup. Setiap Pemesanan sumber daya dari waktu itu ke depan dibatalkan.

> [!NOTE]
> Dalam Project Operations, penutupan kuotasi karena menang atau kalah tidak akan memengaruhi status peluang, yang akan tetap terbuka hingga ditutup secara manual.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
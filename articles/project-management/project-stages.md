---
title: Tahapan proyek
description: Topik ini memberikan informasi tentang tahapan proyek yang tersedia dalam Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: aa3d692a46165b01eafbd7619578cead8dd912d6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127477"
---
# <a name="project-stages"></a>Tahapan proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Tahapan proyek didesain untuk mencerminkan status proyek seiring kemajuannya. Penyesuaian dapat digunakan untuk secara otomatis memperbarui tahapan dengan alur proses bisnis, Power Automate, atau ekstensi plug-in.

Tahapan berikut ditentukan dalam alur proses bisnis default:

- Baru
- Kuotasi
- Rencana
- Kirim
- Selesaikan
- Tutup 

## <a name="new"></a>Baru

Bila Anda membuat sebuah proyek, tahapan proyek diatur ke **Baru**. Jika proyek dibuat dari template, mungkin memiliki jadwal, perkiraan, dan data tim. Jika tidak, itu adalah garis besar proyek, dan komponen lainnya harus dimasukkan.

## <a name="quote"></a>Kuotasi

Ketika Anda menghubungkan sebuah proyek dengan kuotasi, atau ketika membuat proyek dari kuotasi, tahapan proyek diatur ke **kuotasi**, dan perkiraan awal dan akhir tanggal diperbarui. Ketika proyek pada tahapan **kuotasi**, tab **Penjualan** pada halaman **entitas proyek** menampilkan detail kuotasi.

## <a name="plan"></a>Rencana

Ketika Anda memenangkan kuotasi yang berkaitan dengan proyek, dan proyek itu dipindahkan ke fase **Kontrak**, tahapan proyek diperbarui ke **rencana**. Ketika proyek pada tahapan **Rencana**, halaman **entitas proyek** menampilkan detail kontrak.

## <a name="deliver"></a>Kirim

Setelah rencana proyek selesai, dan Anda siap memulai proyek, manajer proyek harus memperbarui tahapan proyek ke **dilaksanakan** untuk menunjukkan bahwa proyek telah dimulai.

## <a name="complete"></a>Selesai 

Saat pekerjaan untuk proyek selesai, manajer proyek dapat memperbarui tahapan ke **Selesai**. Dengan memperbarui tahap proyek ke **Selesai**, manajer proyek menunjukkan bahwa pekerjaan 100 persen selesai, namun proyek tetap terbuka sehingga setiap entri waktu atau biaya yang tertunda dapat direkam.

## <a name="close"></a>Tutup

Bila semua transaksi direkam untuk proyek, manajer proyek dapat memperbarui tahapan ke **Tutup**. Pada titik tersebut, tidak ada transaksi yang dapat direkam, dan proyek diatur ke hanya baca.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
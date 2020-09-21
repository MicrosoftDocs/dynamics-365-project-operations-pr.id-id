---
title: Tahapan Proyek
description: Topik ini menyediakan informasi tentang tahapan proyek.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752410"
---
# <a name="project-stages"></a>Tahapan Proyek 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tahapan proyek diperbarui untuk mencerminkan status proyek seiring kemajuannya. Default alur proses bisnis secara otomatis memperbarui beberapa tahapan proyek sementara yang lainnya diperbarui secara manual oleh manajer proyek. 

Tahapan berikut ditentukan dalam BPF default:

- Baru
- Kuotasi
- Rencana
- Kirim
- Selesai
- Tutup 

## <a name="new"></a>Baru

Bila Anda membuat sebuah proyek, tahapan proyek diatur ke **Baru**. Jika proyek dibuat dari template, mungkin memiliki jadwal, perkiraan, dan data tim. Jika tidak, itu hanya garis besar proyek, dan komponen lainnya harus dimasukkan.

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

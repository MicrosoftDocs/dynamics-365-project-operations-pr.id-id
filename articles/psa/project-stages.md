---
title: Jenis Tahapan proyek
description: Topik ini menyediakan informasi tentang tahapan proyek.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283687"
---
# <a name="project-stage-types"></a>Jenis Tahapan proyek 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tahapan proyek didesain untuk mencerminkan status proyek seiring kemajuannya. Penyesuaian dapat digunakan untuk secara otomatis memperbarui tahapan dengan alur proses bisnis, Power Automate, atau ekstensi plug-in.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
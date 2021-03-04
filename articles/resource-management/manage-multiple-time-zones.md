---
title: Mengelola zona waktu
description: Saat proyek dibuat, zona waktunya didasarkan pada zona waktu yang ditentukan dalam template jam kerja yang diterapkan.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 278b226c88c2f441262eb5be0504f34a1964848c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119827"
---
# <a name="manage-time-zones"></a>Mengelola zona waktu

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


## <a name="projects"></a>Proyek

Saat proyek dibuat, zona waktunya didasarkan pada zona waktu yang ditentukan dalam template jam kerja yang diterapkan. Pada **proyek** untuk, tanggalnya selalu relatif terhadap zona waktu pengguna yang masuk pada setiap tab, kecuali tab **tugas**. Bila Anda melihat struktur rincian kerja, tanggal akan selalu ditampilkan di zona waktu proyek.

## <a name="tasks"></a>Tugas

Bila tugas dibuat, waktu mulai, waktu berakhir, dan jam/hari dikontrol oleh jam kerja proyek. Misalnya, jika tugas dibuat dengan proyek yang zona waktunya adalah -8 PST dan memiliki jam kerja berikut: 9:00 pagi hingga 5:00 sore Senin hingga Jumat, tugas apa pun yang dibuat tanpa penetapan akan menghormati waktu mulai dan waktu berakhir kalender proyek.

## <a name="manage-resources-with-time-zones"></a>Mengelola sumber daya dengan zona waktu

Untuk hasil yang akurat dan dapat diprediksi saat menggunakan **memperpanjang Pemesanan**, ada dua prasyarat utama yang harus dipenuhi:  

- Pengguna harus mengkonfigurasi zona waktu perangkat mereka untuk mencocokkan zona waktu yang ditentukan di **Pengaturan personalisasi** sistem.
 
  ![Pengaturan zona waktu di Windows 10](media/reconcile-assignments-03.png)

  ![Pengaturan zona waktu di Pengaturan personalisasi](media/reconcile-assignments-04.png)
 
- Sumber daya yang dapat dipesan harus memiliki minimal satu menit waktu kerja yang tumpang tindih dengan kontur yang digunakan untuk menentukan ekstensi yang diminta. Misalnya, sumber daya berikut dengan jam kerja yang jatuh antara 9:00 pagi dan 7:00 sore. 

  ![Perbandingan kontur sumber daya](media/reconcile-assignments-05.png)

Tabel berikut menampilkan:

- Template kalender Proyek
- Sumber daya A: sumber daya ini memiliki kalender yang sama dan berada di zona waktu yang sama dengan proyek. Waktu mulai pemesanan adalah 9:00.
- Sumber daya B: sumber daya ini terletak di zona waktu yang berbeda dari proyek dan dimulai pada 7:00 pagi di zona waktu mereka. Namun, Pemesanan akan dimulai pada pukul 9:00 karena itu adalah waktu mulai terawal kontur tugas.
- Sumber daya C dan D: sumber daya berada di zona waktu yang berbeda, keduanya berbeda dari satu sama lain dan proyek, dan Pemesanan mereka tidak dimulai lebih awal dari waktu mulai masing-masing yang tersedia.

|Entitas  |Kalender  |
|-|-|
|Template kalender Proyek   | ![Kalender Proyek](media/reconcile-assignments-06.png) |
|Sumber Daya A  | ![Kalender Sumber Daya A](media/reconcile-assignments-06.png) |
|Sumber Daya B  |  ![Kalender Sumber Daya B](media/reconcile-assignments-07.png) |
|Sumber Daya C  |  ![Kalender Sumber Daya C](media/reconcile-assignments-08.png) |
|Sumber Daya D  | ![Kalender Sumber Daya D](media/reconcile-assignments-09.png)  |
 
Bila Anda menavigasi ke tampilan **rekonsiliasi**, penetapan sumber daya dan kekurangan Pemesanan terkait ditampilkan.

![Tampilan rekonsiliasi sebelum perpanjangan](media/reconcile-assignments-10.png)

Setelah fungsi perpanjangan Pemesanan telah digunakan untuk setiap sumber daya, Pemesanan akan berhasil diperpanjang untuk setiap sumber daya karena setiap jam kerja sumber daya saling tumpang tindih dengan kontur kekurangan.

![Tampilan rekonsiliasi setelah ekstensi pemesanan](media/reconcile-assignments-11.png) 

Perhatikan bahwa melihat lebih dekat rincian pemesanan menunjukkan perbedaan dalam waktu mulai pemesanan. Pemesanan tidak dimulai lebih awal dari waktu mulai kontur penetapan dan tidak lebih awal dari waktu mulai yang tersedia untuk sumber daya.

![Pemesanan baru sumber daya di papan jadwal](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
---
title: Pelacakan upaya proyek
description: Topik ini menyediakan informasi tentang cara melacak upaya proyek dan kemajuan pekerjaan.
author: ruhercul
ms.date: 03/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 6fe381470326fc4000a9ed096b91fde56c045c38
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369200"
---
# <a name="project-effort-tracking"></a>Pelacakan upaya proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kebutuhan untuk melacak kemajuan terhadap jadwal bervariasi menurut industri. Beberapa industri melacak pada tingkat rinci, sedangkan industri lainnya melacak pada tingkat yang lebih tinggi. Topik ini menunjukkan cara menjadwalkan untuk memenuhi kebutuhan organisasi anda.

## <a name="effort-tracking-view"></a>Tampilan Pelacakan Upaya

Tampilan **pelacakan upaya** melacak kemajuan tugas dalam jadwal dengan membandingkan jam kerja aktual yang dihabiskan pada tugas ke jam kerja yang direncanakan untuk tugas. Dynamics 365 Project Operations menggunakan rumus berikut untuk menghitung metrik pelacakan:

- **Persentase Kemajuan**: upaya yang sebenarnya yang dihabiskan sampai saat ini ÷Estimasi saat penyelesaian (EAC) 
- **Upaya tersisa**: Estimasi upaya saat selesai – upaya yang sebenarnya digunakan sampai saat ini 
- **EAC**: usaha tersisa + upaya yang sebenarnya yang dihabiskan sampai saat ini 
- **Varian proyeksi upaya**: upaya yang direncanakan – EAC

Project Operations menunjukkan proyeksi dari varians upaya terhadap tugas. Jika EAC lebih dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih banyak waktu daripada yang direncanakan dan terlambat dari jadwal. Jika EAC lebih sedikit dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih sedikit waktu daripada yang direncanakan dan maju dari jadwal.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Memproyeksikan ulang upaya pada tugas node leaf

Manajer proyek sering merevisi perkiraan asli pada tugas. Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini. Namun, kami tidak menyarankan manajer proyek mengubah jumlah upaya yang direncanakan. Hal ini karena upaya yang direncanakan proyek menunjukkan sumber sebenarnya yang ditetapkan untuk jadwal proyek dan perkiraan biaya, dan semua pemangku kepentingan proyek telah menyetujuinya.

Manajer proyek dapat memproyeksikan ulang upaya pada tugas dengan memperbarui **Upaya Sisa** default dengan estimasi baru pada tugas. Pembaruan ini menyebabkan penghitungan ulang estimasi tugas saat selesai (EAC), persentase progres, dan varians upaya perkiraan pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Proyeksi ulang upaya pada tugas ringkasan

Upaya pada ringkasan tugas atau tugas kontainer dapat diproyeksikan ulang. Manajer proyek dapat memperbarui upaya lainnya pada tugas ringkasan. Memperbarui upaya yang tersisa memicu rangkaian perhitungan berikut di aplikasi:

- EAC dan persentase kemajuan tugas dihitung.
- EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti EAC asli pada tugas.
- EAC baru pada setiap tugas individual hingga tugas node leaf dihitung. 
- Tugas anak yang terpengaruh hingga node leaf memiliki persentase upaya tersisa mereka dan kemajuan yang akan dihitung ulang berdasarkan nilai EAC. Ini menghasilkan proyeksi baru untuk varians upaya dari tugas. 
- EAC dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.


## <a name="project-status-summary"></a>Ringkasan Status Proyek

Pelacakan data dalam tampilan **pelacakan upaya** dan **pelacakan biaya** menampilkan kemajuan dan konsumsi biaya pada node root proyek, tugas ringkasan, dan tingkat tugas node daun. Bagian **status** pada halaman **entitas proyek** menunjukkan ringkasan status tingkat proyek.

## <a name="status-summary-fields"></a>Bidang ringkasan status

Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek. Menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko. Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status. Bidang **Status diperbarui pada** tidak dapat diedit dan nilainya adalah stempel waktu yang menunjukkan Kapan status diperbarui terakhir.

Bidang **performa jadwal** dan **performa biaya** ditetapkan dari tanggal pelacakan. Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat menetapkan bidang ini ke **depan**. Bila jadwal dan varians biaya untuk node root negatif, Anda dapat mengaturnya ke **belakang**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

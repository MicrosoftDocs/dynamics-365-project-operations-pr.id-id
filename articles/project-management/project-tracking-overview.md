---
title: Sekilas pelacakan proyek
description: Topik ini menyediakan informasi tentang cara melacak kemajuan proyek dan konsumsi biaya.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907367"
---
# <a name="project-tracking-overview"></a>Sekilas pelacakan proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Kebutuhan untuk melacak kemajuan terhadap jadwal bervariasi menurut industri. Beberapa industri melacak pada tingkat rinci, sedangkan industri lainnya melacak pada tingkat yang lebih tinggi. Topik ini menunjukkan cara menjadwalkan untuk memenuhi kebutuhan organisasi anda.

## <a name="effort-tracking-view"></a>Tampilan Pelacakan Upaya

Tampilan **pelacakan upaya** melacak kemajuan tugas dalam jadwal dengan membandingkan jam kerja aktual yang dihabiskan pada tugas ke jam kerja yang direncanakan untuk tugas. Dynamics 365 Project Operations menggunakan rumus berikut untuk menghitung metrik pelacakan:

- **Persentase Kemajuan**: upaya yang sebenarnya yang dihabiskan sampai saat ini ÷Estimasi saat penyelesaian (EAC) 
- **Perkiraan untuk menyelesaikan (ETC)**: rencana upaya – upaya yang sebenarnya yang dihabiskan sampai saat ini 
- **EAC**: usaha tersisa + upaya yang sebenarnya yang dihabiskan sampai saat ini 
- **Varian proyeksi upaya**: upaya yang direncanakan – EAC

Project Operations menunjukkan proyeksi dari varians upaya terhadap tugas. Jika EAC lebih dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih banyak waktu daripada yang direncanakan dan terlambat dari jadwal. Jika EAC lebih sedikit dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih sedikit waktu daripada yang direncanakan dan maju dari jadwal.

## <a name="reprojecting-effort"></a>Upaya memproyeksikan ulang

Manajer proyek sering merevisi perkiraan asli pada tugas. Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini. Namun, kami tidak menyarankan agar manajer proyek mengubah angka dasar. Ini karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.

Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:

- Menimpa ETC default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas. 
- Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.

Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, EAC tugas, persentase progres, serta proyeksi varians upaya pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Proyeksi ulang upaya pada tugas ringkasan

Upaya pada ringkasan tugas atau tugas kontainer dapat diproyeksikan ulang. Terlepas dari apakah pengguna memproyeksikan kembali menggunakan usaha yang tersisa atau persentase kemajuan pada tugas ringkasan, rangkaian perhitungan berikut dimulai:

- EAC, ETC, dan persentase kemajuan tugas dihitung.
- EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti EAC asli pada tugas.
- EAC baru pada setiap tugas individual hingga tugas node leaf dihitung. 
- Tugas anak yang terpengaruh hingga node leaf memiliki persentase ETC dan kemajuan yang akan dihitung ulang berdasarkan nilai EAC. Ini menghasilkan proyeksi baru untuk varians upaya dari tugas. 
- EAC dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.

### <a name="cost-tracking-view"></a>Tampilan Pelacakan Biaya 

Tampilan **pelacakan biaya** membandingkan biaya aktual yang dihabiskan pada tugas dengan rencana biaya pada tugas. 

> [!NOTE]
> Tampilan ini hanya menampilkan biaya tenaga kerja dan tidak mencakup biaya dari perkiraan pengeluaran. Project Operations menggunakan rumus berikut untuk menghitung metrik pelacakan:

- **Persentase dari biaya yang dihabiskan**: biaya aktual yang dibelanjakan hingga sekarang ÷ Estimasi biaya saat penyelesaian
- **Biaya untuk menyelesaikan (CTC)**: rencana biaya – biaya sebenarnya yang dihabiskan sampai saat ini
- **EAC**: Sisa Biaya + Biaya Aktual yang digunakan hingga sekarang
- **varians Biaya diproyeksikan**: biaya direncanakan - EAC

Proyeksi varians biaya ditampilkan terhadap tugas. Jika EAC lebih dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih banyak biaya daripada yang direncanakan semula. Oleh karena itu, tren lebih dari anggaran. Jika EAC kurang dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih sedikit biaya daripada yang direncanakan semula. Oleh karena itu, tren di bawah anggaran.

## <a name="project-managers-reprojection-of-cost"></a>Proyeksi ulang biaya manajer proyek

Bila upaya diproyeksikan ulang, CTC, EAC, persentase biaya yang dihabiskan, dan variasi biaya yang diproyeksikan akan dihitung ulang dalam tampilan **pelacakan biaya**.

## <a name="project-status-summary"></a>Ringkasan Status Proyek

Pelacakan data dalam tampilan **pelacakan upaya** dan **pelacakan biaya** menampilkan kemajuan dan konsumsi biaya pada node root proyek, tugas ringkasan, dan tingkat tugas node daun. Bagian **status** pada halaman **entitas proyek** menunjukkan ringkasan status tingkat proyek.

## <a name="status-summary-fields"></a>Bidang ringkasan status

Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek. Menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko. Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status. Bidang **Status diperbarui pada** tidak dapat diedit dan nilainya adalah stempel waktu yang menunjukkan Kapan status diperbarui terakhir.

Bidang **performa jadwal** dan **performa biaya** ditetapkan dari tanggal pelacakan. Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat menetapkan bidang ini ke **depan**. Bila jadwal dan varians biaya untuk node root negatif, Anda dapat mengaturnya ke **belakang**.

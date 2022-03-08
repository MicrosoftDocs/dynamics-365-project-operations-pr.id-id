---
title: Kemajuan proyek dan konsumsi biaya
description: Topik ini menyediakan informasi tentang melacak kemajuan proyek dan konsumsi biaya.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 8bde19fbf1dd9f0c760455ecb7f7f2bd14a358d441bf024ec0cdefa42866f53e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987170"
---
# <a name="project-progress-and-cost-consumption"></a>Kemajuan proyek dan konsumsi biaya

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Kebutuhan untuk melacak kemajuan terhadap jadwal bervariasi menurut industri. Beberapa industri melacak pada tingkat rinci, sedangkan industri lainnya melacak pada tingkat yang lebih tinggi. Topik ini menunjukkan cara menjadwalkan untuk memenuhi kebutuhan organisasi anda.

## <a name="effort-tracking-view"></a>Tampilan Pelacakan Upaya

Tampilan **pelacakan upaya** melacak kemajuan tugas dalam jadwal. Ini membandingkan waktu aktual upaya yang digunakan dalam tugas terhadap jam upaya yang direncanakan pada tugas. Project Service Automation menggunakan rumus berikut untuk menghitung metrik pelacakan:

Awalnya pada pembuatan tugas: rencana biaya akan diatur ke perkiraan biaya saat selesai. Setelah aktual direkam pada tugas, berikut ini akan menjadi perhitungan tentang tampilan pelacakan untuk upaya

- Persentase Kemajuan = upaya yang sebenarnya yang dihabiskan sampai saat ini ÷Estimasi saat penyelesaian (EAC) 
- Estimasi untuk menyelesaikan (ETC) = Estimasi saat penyelesaian (EAC)-upaya yang sebenarnya dihabiskan hingga saat ini 
- EAC = usaha tersisa + upaya yang sebenarnya yang dihabiskan sampai saat ini 
- Diproyeksikan variance usaha = usaha yang direncanakan – EAC

Project Service Automation menunjukkan proyeksi dari varians upaya terhadap tugas. Jika EAC lebih dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih banyak waktu daripada yang direncanakan semula. Oleh karena itu, terlambat dari jadwal. Jika EAC kurang dari upaya yang direncanakan, tugas diproyeksikan untuk mengambil lebih sedikit waktu daripada yang direncanakan semula. Oleh karena itu, lebih dini dari jadwal.

## <a name="reprojecting-effort"></a>Upaya memproyeksikan ulang

biasanya manajer proyek merevisi perkiraan asli pada tugas. Proyeksi proyek kembali adalah persepsi manajer proyek tentang perkiraan, mengingat status proyek saat ini. Akan tetapi, sebaiknya manajer proyek tidak mengubah angka dasar, karena dasar proyek mewakili sumber kebenaran yang mapan untuk jadwal proyek dan perkiraan biaya yang mana semua stakeholder proyek telah setuju.

Ada dua cara manajer proyek dapat melakukan proyeksi ulang upaya pada tugas:

- Menimpa ETC default dengan perkiraan baru dari upaya tersisa yang sebenarnya pada tugas. 
- Menimpa persentase kemajuan default dengan perkiraan baru dari kemajuan sebenarnya pada tugas.

Masing-masing pendekatan ini menyebabkan penghitungan ulang dari ETC, EAC tugas, dan persentase progres, serta proyeksi varians upaya pada tugas. EAC, ETC, dan persentase kemajuan pada ringkasan tugas juga dihitung ulang, dan menghasilkan proyeksi baru dari varians upaya.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Proyeksi ulang upaya pada tugas ringkasan

Upaya pada ringkasan tugas atau tugas kontainer dapat diproyeksikan ulang. Terlepas dari apakah pengguna memproyeksikan kembali menggunakan usaha yang tersisa atau persentase kemajuan pada tugas ringkasan, rangkaian perhitungan berikut dimulai:

- EAC, ETC, dan persentase kemajuan tugas dihitung.
- EAC baru didistribusikan ke tugas anak di proporsi yang sama seperti EAC asli pada tugas.
- EAC baru pada setiap tugas individual hingga tugas node leaf dihitung. 
- Tugas anak yang terpengaruh hingga node leaf memiliki persentase ETC dan kemajuan yang akan dihitung ulang berdasarkan nilai EAC. Ini menghasilkan proyeksi baru untuk varians upaya dari tugas. 
- EAC dari tugas ringkasan sepenuhnya hingga node root dihitung ulang.

### <a name="cost-tracking-view"></a>Tampilan Pelacakan Biaya 

Tampilan **pelacakan biaya** membandingkan biaya aktual yang dihabiskan pada tugas dengan rencana biaya. 

> [!NOTE]
> Tampilan ini hanya menampilkan biaya tenaga kerja dan tidak mencakup biaya dari perkiraan pengeluaran. 

Project Service Automation menggunakan rumus berikut untuk menghitung metrik pelacakan:

Bila tugas dibuat, biaya yang direncanakan sama dengan perkiraan biaya saat penyelesaian. Setelah aktual direkam pada tugas, berikut ini akan dihitung pada tampilan **pelacakan** untuk biaya:

 - Persentase dari biaya yang dihabiskan = biaya aktual yang dibelanjakan hingga sekarang ÷ Estimasi biaya saat penyelesaian untuk tugas
 - Biaya untuk menyelesaikan (CTC) = Estimasi biaya saat penyelesaian – biaya sebenarnya yang dihabiskan sampai saat ini
 - Biaya untuk menyelesaikan = CTC + biaya sebenarnya yang dihabiskan sampai saat ini
 - varians Biaya terproyeksi = biaya yang direncanakan - Estimasi biaya saat penyelesaian

Proyeksi varians biaya ditampilkan terhadap tugas. Jika estimasi biaya saat penyelesaian lebih dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih banyak biaya daripada yang direncanakan semula. Oleh karena itu, tren lebih dari anggaran. Jika estimasi biaya saat penyelesaian kurang dari biaya yang direncanakan, tugas diproyeksikan untuk menghabiskan lebih sedikit biaya daripada yang direncanakan semula dan cenderung di bawah anggaran.

## <a name="project-managers-reprojection-of-cost"></a>Proyeksi ulang biaya manajer proyek

Bila upaya diproyeksikan ulang, CTC, Estimasi biaya saat penyelesaian, persentase biaya yang dihabiskan, dan variasi biaya yang diproyeksikan akan dihitung ulang dalam tampilan **pelacakan biaya**.

## <a name="project-status-summary"></a>Ringkasan Status Proyek

Pelacakan data dalam tampilan **pelacakan upaya** dan **pelacakan biaya** menampilkan kemajuan dan konsumsi biaya pada node root proyek, tugas ringkasan, dan tingkat tugas node daun. Bagian **status** pada halaman **entitas proyek** menunjukkan ringkasan status tingkat proyek.

## <a name="status-summary-fields"></a>Bidang ringkasan status

Bidang **status proyek secara keseluruhan** adalah bidang yang dapat diedit yang menampilkan status keseluruhan proyek. Menggunakan pengkodean warna, seperti hijau, kuning, dan lainnya, untuk menunjukkan peningkatan risiko. Bidang **komentar** memungkinkan manajer proyek memasukkan komentar tertentu tentang status. Bidang **Status diperbarui pada** tidak dapat diedit dan nilainya adalah stempel waktu yang menunjukkan Kapan status diperbarui terakhir.

Bidang **performa jadwal** dan **performa biaya** ditetapkan dari tanggal pelacakan. Bila jadwal dan varians biaya untuk node root dalam tampilan **pelacakan upaya** positif, Anda dapat menetapkan bidang ini ke **depan**. Bila jadwal dan varians biaya untuk node root negatif, Anda dapat mengaturnya ke **belakang**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
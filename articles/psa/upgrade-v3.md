---
title: Pertimbangan peningkatan - Microsoft Dynamics 365 Project Service Automation versi 2.x atau 1.x ke versi 3
description: Artikel ini menyediakan informasi tentang pertimbangan yang harus anda buat saat melakukan upgrade dari versi Project Service Automation 2. x atau 1. x ke versi 3.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 11/13/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3f67b2fe39c9d0224207e7c655892318ec7e09b8
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918914"
---
# <a name="upgrade-considerations---psa-version-2x-or-1x-to-version-3"></a>Pertimbangan peningkatan – PSA versi 2.x atau 1.x ke versi 3

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="project-service-automation-and-field-service"></a>Project Service Automation dan Field Service
Baik Dynamics 365 Project Service Automation maupun Dynamics 365 Field Service menggunakan solusi Universal Resource Scheduling (Urs) untuk penjadwalan sumber daya. Bila Anda memiliki Project Service Automation dan Field Service di instans Anda, tingkatkan kedua solusi itu ke versi terbarunya. Untuk Project Service Automation, ia adalah versi 3.x. Untuk Field Service, ini adalah versi 8.x. Memutakhirkan Project Service Automation atau Field Service akan menginstal URS versi terbaru. Jika solusi Project Service Automation dan Field Service dalam instans yang sama tidak ditingkatkan ke versi terbaru, mungkin ada beberapa perilaku yang tidak konsisten.

## <a name="resource-assignments"></a>Penetapan sumber daya
Di Project Service Automation versi 2 dan versi 1, penetapan tugas disimpan sebagai tugas anak (juga disebut tugas baris di **) entitas tugas**, dan tidak langsung terkait dengan entitas **penetapan sumber daya**. Tugas baris terlihat di jendela pop-up tugas di struktur rincian kerja (WBS).

![Tugas baris di WBS di Project Service Automation versi 2 dan versi 1.](media/upgrade-line-task-01.png)

Dalam versi 3 dari Project Service Automation, skema yang mendasari penetapan sumber daya yang dapat dipesan untuk tugas telah diubah. Tugas baris telah ditolak dan ada relasi 1:1 langsung antara tugas di **entitas tugas** dan anggota tim di entitas **penetapan sumber daya**. Tugas yang ditetapkan ke anggota tim proyek sekarang disimpan langsung dalam entitas tugas sumber daya.  

Perubahan ini mempengaruhi peningkatan proyek yang ada yang memiliki tugas sumber daya untuk nama sumber daya dapat dipesan bernama dan sumber daya generik pada tim proyek. Artikel ini memberikan pertimbangan bahwa anda akan perlu memperhitungkan proyek anda saat anda mengupgrade ke versi 3. 

### <a name="tasks-assigned-to-named-resources"></a>Tugas ditetapkan ke sumber daya bernama
Menggunakan entitas tugas yang mendasari, tugas di versi 2 dan versi 1 memungkinkan anggota tim untuk menggambarkan peran selain dari peran yang ditentukan default. Misalnya, Pramudita Cahyadewi, yang secara default menetapkan peran manajer program, dapat ditetapkan ke tugas dengan peran pengembang. Di versi 3, peran anggota tim yang disebutkan selalu default, sehingga tugas yang diberikan pada Pramudita Cahyadewi menggunakan peran default Pramudita sebagai manajer program.

Jika Anda telah menetapkan sumber daya untuk tugas di luar peran default mereka dalam versi 2 dan versi 1, saat Anda meningkatkan, sumber daya bernama akan ditetapkan peran default untuk semua penetapan tugas, terlepas dari penetapan peran di versi 2. Hasil penetapan ini akan mengakibatkan perbedaan dalam perkiraan perkiraan dari versi 2 atau versi 1 ke versi 3 karena perkiraan dihitung berdasarkan peran sumber daya dan bukan penetapan tugas baris. Misalnya, di versi 2, dua tugas telah ditetapkan ke Latisha Aquina. Peran pada tugas baris untuk tugas 1 adalah Developer dan untuk tugas 2, manajer program. Latisha Aquina memiliki peran default manajer program.

![Peran ganda ditetapkan ke satu sumber daya.](media/upgrade-multiple-roles-02.png)

Karena peran pengembang dan manajer program berbeda, perkiraan biaya dan penjualan adalah sebagai berikut:

![Perkiraan biaya untuk peran sumber daya.](media/upggrade-cost-estimates-03.png)

![Perkiraan penjualan untuk peran sumber daya.](media/upgrade-sales-estimates-04.png)

Bila Anda mengupgrade ke versi 3, tugas baris digantikan dengan tugas sumber daya pada tugas anggota tim sumber daya yang dapat dipesan. Tugas akan menggunakan peran default sumber daya yang dapat dipesan. Dalam grafik berikut, Latisha Aquina yang memiliki peran manajer program, adalah sumber daya.

![Penetapan sumber daya.](media/resource-assignment-v2-05.png)

Karena perkiraan didasarkan pada peran default untuk sumber daya, perkiraan penjualan dan biaya dapat berubah. Dalam grafik berikut, Anda tidak lagi melihat peran **pengembang** karena peran sekarang diambil dari peran default sumber daya yang dapat dipesan.

![Perkiraan biaya untuk peran default.](media/resource-assignment-cost-estimate-06.png)
![Perkiraan penjualan untuk peran default.](media/resource-assignment-sales-estimate-07.png)

Setelah pembaruan selesai, Anda dapat mengedit peran anggota tim untuk menjadi yang lain selain default yang ditetapkan. Namun, jika Anda mengubah peran anggota tim, itu akan diubah pada semua tugas yang ditetapkan karena anggota tim tidak dapat ditetapkan peran ganda di versi 3.

![Memperbarui peran sumber daya.](media/resource-role-assignment-08.png)

Hal ini juga berlaku untuk tugas baris yang ditetapkan ke sumber daya bernama saat Anda mengubah unit organisasi sumber daya dari default ke unit organisasi lain. Setelah versi peningkatan 3 selesai, tugas akan menggunakan unit organisasi default sumber daya, bukan yang ditetapkan pada tugas baris.

### <a name="tasks-assigned-to-generic-resources"></a>Tugas ditetapkan ke sumber daya generik
Di versi 2 dan versi 1, Anda dapat mengatur peran dan unit organisasi pada tugas, lalu menggunakan fitur **Buat tim** untuk menghasilkan sumber daya umum berdasarkan atribut yang diatur pada tugas. Di versi 3, Anda membuat anggota tim generik dengan peran dan unit organisasi, lalu menetapkan anggota tim ke tugas.

Di versi 2 dan versi 1, proyek dengan sumber daya generik bisa memiliki dua keadaan, atau campuran keduanya pada tingkat tugas. Contohnya, Anda bisa memiliki skenario berikut:

- Tugas dengan peran dan unit organisasi diatur, namun tidak ada penetapan sumber daya terafiliasi yang dihasilkan.
- Tugas dengan penetapan sumber daya anggota tim generik yang ditetapkan dengan membuat sumber daya umum menggunakan fitur **buat tim**.

Sebelum memulai peningkatan, sebaiknya buat ulang tim untuk setiap proyek yang memiliki tugas yang ditetapkan ke sumber daya generik atau belum menghasilkan proses tim yang berjalan.

Untuk tugas yang ditetapkan ke anggota tim umum yang dihasilkan dengan **Buat tim**, peningkatan akan meninggalkan sumber daya generik pada tim dan meninggalkan tugas ke anggota tim generik. Sebaiknya buat persyaratan sumber daya untuk anggota tim generik setelah peningkatan, namun sebelum Anda memesan atau mengajukan permintaan sumber daya. Tindakan ini akan mempertahankan penetapan unit organisasi pada anggota tim generik yang berbeda dengan unit organisasi kontrak proyek.

Misalnya, dalam proyek proyek Z, unit organisasi kontrak adalah Aswono AS. Dalam rencana proyek, tugas pengujian dalam fase penerapan telah ditetapkan peran Konsultan teknis, dan unit organisasi yang ditetapkan adalah Aswono India.

![Tahap penerapan penugasan organisasi.](media/org-unit-assignment-09.png)

Setelah tahap penerapan, tugas uji integrasi ditetapkan ke konsultan teknis peran, namun org diatur ke Aswono AS.  

![Uji integrasi penetapan organisasi tugas.](media/org-unit-generate-team-10.png)

Bila Anda membuat tim untuk proyek, dua anggota tim umum dibuat karena unit organisasi yang berbeda pada tugas. Konsultan teknis 1 akan ditugasi tugas Aswono India dan konsultan teknik 2 akan memiliki tugas Aswono AS.  

![Anggota tim generik dihasilkan.](media/org-unit-assignments-multiple-resources-11.png)

> [!NOTE]
> Dalam Project Service Automation versi 2 dan versi 1, anggota tim tidak memegang unit organisasi, yang dikelola pada tugas baris.

![Tugas baris versi 2 dan versi 1 di Project Service Automation.](media/line-tasks-12.png)

Anda dapat melihat unit organisasi pada tampilan perkiraan. 

![Perkiraan unit organisasi.](media/org-unit-estimates-view-13.png)
 
Setelah peningkatan selesai, unit organisasi pada tugas baris yang terkait dengan anggota tim generik ditambahkan ke anggota tim generik, dan tugas baris akan dihapus. Oleh karena itu, sebaiknya lakukan sebelum meningkatkan, buat atau buat ulang tim pada setiap proyek yang berisi sumber daya generik.

Untuk tugas yang ditetapkan ke peran dengan unit organisasi yang berbeda dari unit organisasi proyek kontrak, dan tim belum dihasilkan, peningkatan akan membuat anggota tim generik untuk peran tersebut, namun akan menggunakan unit kontrak proyek untuk unit organisasi anggota tim. Merujuk kembali ke contoh dengan Project Z, unit organisasi kontrak Aswono AS, dan tugas pengujian rencana proyek dalam fase penerapan telah ditetapkan peran Konsultan teknis dengan unit organisasi yang ditetapkan ke Aswono India. Tes integrasi yang diselesaikan setelah fase implementasi telah ditugaskan ke konsultan teknis peran. Unit organisasi Aswono AS dan tim belum dibuat. Peningkatan akan membuat satu anggota tim generik, konsultan teknis yang memiliki jam penugasan dari ketiga tugas, dan unit organisasi Aswono AS, unit organisasi kontrak proyek.   
 
Mengubah default unit organisasi sumber daya berbeda pada anggota tim yang belum dibuat adalah alasan kami menyarankan Anda membuat atau membuat ulang tim pada setiap proyek yang berisi sumber daya generik sebelum peningkatan sehingga tugas unit organisasi tidak hilang.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

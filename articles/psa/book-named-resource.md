---
title: Pesan sumber daya bernama dari persyaratan sumber daya.
description: Artikel ini memberikan informasi tentang pemesanan sumber daya bernama untuk persyaratan sumber daya umum.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 9598490da1905227e517da8ba90f8ffd1df88566
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916246"
---
# <a name="book-named-resources-from-resource-requirements"></a>Pesan sumber daya bernama dari persyaratan sumber daya.

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda dapat memesan sumber daya bernama untuk menggantikan sumber daya generik yang memiliki persyaratan sumber daya.

1. Di Project Service Automation (PSA), di halaman **proyek**, klik tab **tim**.
2. Pilih sumber daya generik yang memiliki persyaratan sumber daya dari daftar, lalu klik **pesan**. Atau, buka persyaratan sumber daya, lalu klik **pesan**.


![Memesan anggota tim generik.](media/RM-how-to-14.png)


3. Di halaman **asisten jadwal**, pilih sumber daya bernama untuk melakukan pemesanan ke tim proyek, lalu klik **pesan**.

![Memesan anggota tim generik menggunakan Asisten jadwal.](media/RM-how-to-15.png)

Bila Pemesanan selesai dan dipenuhi oleh sumber daya bernama, sumber daya generik digantikan dengan sumber daya bernama.

![Anggota tim bernama menggantikan anggota tim generik.](media/RM-how-to-16.png)

Tugas pada jadwal diperbarui dengan sumber daya bernama juga.

![Anggota tim bernama ditetapkan ke tugas proyek.](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a>Penuhi sumber daya generik dengan beberapa sumber daya bernama
Memenuhi persyaratan untuk sumber daya generik dengan beberapa sumber daya bernama serupa dengan menetapkan satu sumber daya bernama. Misalnya, ada tugas dengan durasi lima hari dan 120 jam upaya. Tugas ini tidak dapat diselesaikan dengan satu sumber daya yang bekerja selama delapan jam sehari selama lima hari seminggu. 

![Sebuah tugas memerlukan 120 jam kerja selama lima hari.](media/RM-how-to-21.png)

Persyaratannya adalah untuk 120 jam rekayasa Robotika selama lima hari, yang merupakan 24 jam per hari.

![Persyaratan per hari.](media/RM-how-to-22.png)

Ini adalah contoh bila beberapa sumber daya bernama diperlukan untuk memenuhi permintaan sumber daya generik. Anda perlu memesan beberapa sumber daya untuk memenuhi persyaratan.

![Pemesanan beberapa sumber daya untuk memenuhi persyaratan.](media/RM-how-to-23.png)

Perbedaan utama dalam skenario ini adalah bahwa sumber daya generik tetap pada tim yang ditetapkan untuk tugas, dan anggota tim sumber daya bernama yang dipesan tidak ditetapkan sebagai bagian dari posisi. Manajer proyek dapat menetapkan pekerjaan yang sesuai dengan sumber daya bernama. Tampilan **rekonsiliasi** dapat membantu manajer proyek dalam memecah Pemesanan di beberapa sumber daya menjadi penetapan tugas. Hal ini tidak dilakukan secara otomatis karena dalam skenario apa pun yang lebih rumit daripada contoh sederhana di atas, seperti di mana Anda memiliki bundel tugas yang membuat persyaratan, maksud dari bagaimana manajer proyek ingin menugaskan, harus diasumsikan oleh sistem. Karena sistem tidak dapat memahami maksud, kemungkinannya adalah asumsi yang akan berbeda dari yang dimaksudkan dan hasil yang tidak tepat atau tidak terduga akan terjadi. Hasil yang dapat diprediksi adalah bahwa sumber daya generik tetap ditugaskan hingga manajer proyek dengan sengaja membuat tugas, dengan bantuan tampilan **rekonsiliasi**.




[!INCLUDE[footer-include](../includes/footer-banner.md)]

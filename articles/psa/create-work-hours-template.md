---
title: Membuat template jam kerja
description: Artikel ini menjelaskan cara membuat templat jam kerja di Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 8f3ac17a29e79f86f7c3ce127edb4b02ca63ea04
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916062"
---
# <a name="create-a-work-hours-template-project-service"></a>Buat template jam kerja (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Untuk membuat dan mengelola proyek, Anda harus menerapkan template kalender ke proyek. Template kalender menentukan atribut proyek berikut:

- Jam kerja, termasuk waktu mulai dan berakhir
- Hari kerja
- Pengecualian kalender seperti non-hari kerja

Template kalender yang diterapkan ke proyek adalah salinan template kalender yang ditentukan dalam pengaturan organisasi Anda.

> [!NOTE]
> Jika Anda mengubah template kalender, perubahan tersebut tidak akan diterapkan ke jam kerja proyek. Untuk mengubah jam kerja proyek, template baru harus diterapkan.

Untuk membuat template kalender untuk organisasi Anda, ada dua persyaratan utama:

- Tentukan jam kerja yang diinginkan dari template menggunakan sumber daya baru atau saat ini yang dapat dipesan.
- Buat template kalender baru dan kaitkan template dengan sumber daya yang dapat dipesan.

**Tentukan jam kerja template**

1. Buka **Sumber Daya** \> **Sumber daya**.
2. Buat sumber daya baru untuk referensi di template kalender, atau pilih sumber daya yang ada.
3. Pilih tab **Jam Kerja** sumber daya, lalu lengkapi petunjuk dalam [Atur jam kerja untuk sumber daya](/dynamics365/field-service/set-work-hours-resource) agar dapat mengkonfigurasi aturan kalender.

**Membuat template kalender baru**

1. Buka **Pengaturan** \> **Template Kalender**.
2. Pilih **Baru**, lalu masukkan nama, deskripsi, dan sumber daya template.


> [!NOTE]
> Bila sumber daya direferensikan di template kalender, salinan kalender sumber daya dikaitkan dengan template kalender. Jika jam kerja template yang disalin berubah, perubahan tersebut tidak akan diperbanyak ke template kalender.


### <a name="see-also"></a>Lihat Juga  
 [Konfigurasi sumber daya](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

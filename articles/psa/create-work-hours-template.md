---
title: Membuat template jam kerja
description: Topik ini mendeskripsikan bagaimana membuat template jam kerja di Project Service.
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
ms.openlocfilehash: 90525cf1e7cd487a03b064466ad1b13f8afb7819443fc4bacf9c7d3eee86f0b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987395"
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
3. Pilih tab **Jam Kerja** sumber daya, lalu lengkapi petunjuk dalam [Atur jam kerja untuk sumber daya](/dynamics365/field-service/set-work-hours-resource.md) agar dapat mengkonfigurasi aturan kalender.

**Membuat template kalender baru**

1. Buka **Pengaturan** \> **Template Kalender**.
2. Pilih **Baru**, lalu masukkan nama, deskripsi, dan sumber daya template.


> [!NOTE]
> Bila sumber daya direferensikan di template kalender, salinan kalender sumber daya dikaitkan dengan template kalender. Jika jam kerja template yang disalin berubah, perubahan tersebut tidak akan diperbanyak ke template kalender.


### <a name="see-also"></a>Lihat Juga  
 [Konfigurasi sumber daya](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]

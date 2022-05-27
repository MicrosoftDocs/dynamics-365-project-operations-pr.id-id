---
title: Menentukan kalender proyek
description: Halaman topik ini menyediakan informasi tentang cara menerapkan template kalender ke proyek untuk melacak jadwal proyek.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0e31fcaf039ae214394b08b60b5d41987dc648e7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578942"
---
# <a name="define-project-calendars"></a>Menentukan kalender proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

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

Sekarang Anda dapat mengaitkan template kerja dengan template kalender proyek.


[!INCLUDE[footer-include](../includes/footer-banner.md)]


---
title: Yang baru atau yang diubah di Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan informasi tentang apa yang baru dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 5110679038ae7ed1e21a3e7dc80a4657e0752b49
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150942"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Yang baru atau yang diubah di Project Service Automation versi 3 gelombang 1 2020

[!include [banner](../includes/psa-now-project-operations.md)]

Topik ini menyoroti pertimbangan peningkatan utama saat beralih ke rilis terbaru dari Project Service Automation (PSA) versi 3. x wave 1 2020.

## <a name="time-entry"></a>Entri Waktu
Pengalaman entri waktu diperpanjang untuk memberikan kemampuan untuk memperpanjang entri waktu ke skenario pelanggan lainnya. Ini mencakup kemampuan untuk menambahkan jenis entri, yang sekarang mendorong perilaku tertentu berdasarkan nama skema bidang, **Pengaturan Entri Waktu** yang ditampilkan sebagai **sumber waktu**. Solusi baru, disebut waktu, pengeluaran, Penstatusan, dan persetujuan (TESA) telah ditambahkan untuk mendukung fungsi ini.

### <a name="upgrade-consideration"></a>Pertimbangan upgrade
Untuk mendukung fungsi ini, peran dalam PSA telah diperbarui untuk mencakup hak istimewa baru. Hak istimewa ini memberikan akses baca ke entitas baru, **pengaturan entri waktu**.

Pengguna yang memerlukan kemampuan untuk mencatat waktu harus diberikan peran pengguna **Pengguna entri waktu** selain peran yang ada. Peran ini mencakup fungsi baru dan memastikan bahwa entri waktu akan terus berfungsi.

Selain itu, jika Anda memiliki modul aplikasi kustom yang mencakup semua formulir untuk entitas entri waktu, Anda akan diminta untuk menghapus **formulir pembuatan cepat waktu TESA** dari modul.

### <a name="currently-extended-time-entry-changes"></a>Perubahan entri waktu perpanjangan saat ini
Untuk meminimalkan dampak terhadap pengguna waktu masuk saat ini, perubahan peran ini adalah satu-satunya persyaratan inti yang diperlukan untuk terus memanfaatkan entri waktu. Jika Anda telah membuat tampilan kustom atau pengalaman entri waktu terpisah, Anda harus menetapkan bidang **pengaturan entri waktu** ke nilai PSA yang benar.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
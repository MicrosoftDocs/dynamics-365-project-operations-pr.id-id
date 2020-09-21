---
title: Yang baru atau yang diubah di Project Service Automation versi 3.x gelombang 1 2020
description: Topik ini menyediakan informasi tentang apa yang baru dan diubah dalam Project Service Automation versi 3 gelombang 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 03/24/2020
ms.locfileid: "3752431"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Yang baru atau yang diubah di Project Service Automation versi 3 gelombang 1 2020
Topik ini menyoroti pertimbangan peningkatan utama saat beralih ke rilis terbaru dari Project Service Automation (PSA) versi 3. x wave 1 2020.

## <a name="time-entry"></a>Entri Waktu
Pengalaman entri waktu diperpanjang untuk memberikan kemampuan untuk memperpanjang entri waktu ke skenario pelanggan lainnya. Ini mencakup kemampuan untuk menambahkan jenis entri, yang sekarang mendorong perilaku tertentu berdasarkan nama skema bidang, **Pengaturan Entri Waktu** yang ditampilkan sebagai **sumber waktu**.

### <a name="upgrade-consideration"></a>Pertimbangan upgrade
Untuk mendukung fungsi ini, peran dalam PSA telah diperbarui untuk mencakup hak istimewa baru. Hak istimewa ini memberikan akses baca ke entitas baru, **pengaturan entri waktu**.

Pengguna yang memerlukan kemampuan untuk mencatat waktu harus diberikan peran pengguna **Pengguna entri waktu** selain peran yang ada. Peran ini mencakup fungsi baru dan memastikan bahwa entri waktu akan terus berfungsi.

### <a name="currently-extended-time-entry-changes"></a>Perubahan entri waktu perpanjangan saat ini
Untuk meminimalkan dampak terhadap pengguna waktu masuk saat ini, perubahan peran ini adalah satu-satunya persyaratan inti yang diperlukan untuk terus memanfaatkan entri waktu. Jika Anda telah membuat tampilan kustom atau pengalaman entri waktu terpisah, Anda harus menetapkan bidang **pengaturan entri waktu** ke nilai PSA yang benar.

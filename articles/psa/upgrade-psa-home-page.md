---
title: Laman beranda peningkatan
description: Topik ini menunjukkan lokasi untuk menemukan informasi penting tentang fitur baru dan yang diubah di Dynamics 365 Project Service Automation, serta proses peningkatan ke versi terbaru.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a2e17fbdfb71eb62053236bf6c8a3d1aedf332df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012365"
---
# <a name="upgrade-home-page"></a>Laman beranda peningkatan

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Tingkatkan dari PSA versi 2.x atau 1.x ke versi 3.x

### <a name="new-instances"></a>Instans baru

Per tanggal 17 Mei 2019, ketika Project Service Automation dipilih selama penyediaan instans baru, versi 3. x diinstal secara default.

### <a name="existing-instances"></a>Instans yang Ada

Sebelumnya, pelanggan yang memiliki instans PSA versi 2.x dan perlu meng-upgrade ke versi 3. x, yang merupakan versi berbasis antarmuka klien terpadu (UCI) PSA, harus menghubungi Dukungan Microsoft dan memberikan rincian instans mereka, sehingga dukungan dapat mengaktifkan instans untuk ditingkatkan ke versi 3. x. Pada tanggal 1 Maret 2020, pelanggan yang memiliki instans PSA versi 2.x dan perlu meningkatkan ke versi 3.x, akan dapat meningkatkan instans mereka langsung dari portal Admin tanpa harus menghubungi Dukungan Microsoft.  

> [!NOTE]
> PSA versi 3. x mencakup perubahan signifikan. Telah dibangun di atas kerangka kerja Antarmuka Terpadu untuk membantu memberikan pengalaman pengguna yang lebih baik. Aplikasi yang didesain ulang memberikan antarmuka pengguna yang konsisten dan seragam (UI), dan mengikuti prinsip desain responsif untuk tampilan optimal pada ukuran layar atau perangkat apa pun. Ada perubahan lain di seluruh aplikasi. Beberapa area yang telah diubah mencakup harga, pemesanan, dan penetapan sumber daya, waktu, pengeluaran, dan persetujuan.

Sebelum memulai proses peningkatan, sebaiknya selesaikan tugas berikut:

- Verifikasikan Apakah baik Dynamics 365 Field Service maupun Project Service Automation diinstal pada instans yang teridentifikasi. Jika solusi kedua terinstal, Anda harus merencanakan untuk meng-upgrade keduanya sebelum Anda melanjutkan penggunaan instans secara teratur.
- Tinjau topik berikut dengan cermat. Kesadaran dan pemahaman tentang perubahan antara versi akan membantu Anda dengan proses peningkatan. Topik ini memberikan informasi tentang perubahan besar dalam PSA, bersama dengan pertimbangan dan rekomendasi untuk merencanakan peningkatan Anda ke versi 3. x.

    - [Yang baru atau yang diubah di Project Service Automation versi 3](whats-new-changed-v3.md)
    - [Pertimbangan peningkatan – Project Service Automation versi 2.x atau 1.x ke versi 3.x](upgrade-v3.md)

- Tingkatkan instans sandbox anda untuk mengevaluasi perubahan dalam penerapan sebelum meningkatkan instans produksi.

Setelah Anda meninjau topik yang telah disebutkan sebelumnya dan siap mengupgrade ke versi PSA 3. x atau versi berbasis UCI, Kirim permintaan ke dukungan Microsoft untuk membuat peningkatan tersedia dari Pusat admin. Dalam permintaan Anda, berikan rincian instans Anda.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Versi lama PSA (PSA versi 2. x) di instans yang baru dibuat

Pada tanggal 17 Mei 2019, Semua instance baru akan memiliki UCI sebagai klien default. Untuk penyelarasan dengan perubahan ini, versi PSA 3. x dan Field Service 8. x akan ditetapkan secara default, karena versi ini dirancang untuk bekerja dengan klien UCI.

Mulai 1 Maret 2020, pelanggan Dynamics PSA tidak akan lagi dapat membuat lingkungan baru dengan PSA versi lama, misalnya PSA versi 2.x atau yang lebih rendah. Lingkungan baru hanya mendapatkan versi 3.x dari PSA.

> [!NOTE]
> Untuk pengalaman terbaik saat Anda menggunakan versi lama dari aplikasi Field Service dan PSA, buka halaman **pengaturan sistem**, dan untuk bidang, bidang **gunakan Antarmuka Terpadu baru saja (disarankan)**, pilih **tidak** karena versi ini tidak dirancang untuk dimuat dengan benar di UCI. Setelah Anda telah menonaktifkan UCI, Anda dapat membuka dan menjalankan versi Field Service dan PSA menggunakan klien web lama. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
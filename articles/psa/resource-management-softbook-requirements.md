---
title: Persyaratan pesanan tentatif
description: Topik ini menyediakan informasi tentang cara memenuhi persyaratan pesanan tentatif.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 95f064e0f83d2052ac4ae9673b4fcdcd16a2574246d3320e1ed3798cd6ff062b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007015"
---
# <a name="soft-book-requirements"></a>Persyaratan pesanan tentatif

[!include [banner](../includes/psa-now-project-operations.md)]

Persyaratan sumber daya dapat dipesan secara definitif. Pemesanan definitif membuat proposal yang menghabiskan kapasitas sumber daya. Usulan ini kemudian dikirim kembali ke pemohon untuk disetujui. Pemesanan tentatif menambahkan sumber daya ke tim proyek dan memiliki status yang berbeda di papan jadwal, namun tidak mengkonsumsi kapasitas sumber daya. Untuk melakukan pesanan tentatif sumber daya dari papan jadwal, atur bidang **status Pemesanan** menjadi **tentatif**.

![Status pemesanan diatur ke tentatif.](media/Resource-Management-image77.png)

Saat tab **tim** berada di tampilan **anggota tim bernama**, sumber daya ditampilkan di sana. Jam yang dipesan dengan tentatif dilaporkan di kolom **jam pesanan tentatif**.

![Jam pesanan tentatif di tampilan anggota tim bernama.](media/Resource-Management-image78.png)

Anggota tim dipesan terlebih dulu tidak dapat ditetapkan ke tugas.

![Anggota tim dipesan tentatif ditetapkan ke tugas.](media/Resource-Management-image79.png)

Pada tab **rekonsiliasi**, tidak ada Pemesanan yang ditampilkan untuk sumber daya pesanan tentatif, karena tab **rekonsiliasi** hanya mempertimbangkan Pemesanan definitif.

![Sumber daya yang dipesan dengan tentatif tanpa pemesanan pada tab rekonsiliasi.](media/Resource-Management-image80.png)

> [!NOTE]
> Anda tidak dapat memesan sumber daya secara tentatif dari persyaratan yang dihasilkan dari anggota tim generik.

Di papan jadwal, pewarnaan yang berbeda digunakan untuk pemesanan tentatif untuk sumber daya.

![Melakukan pemesanan tentatif di papan jadwal.](media/Resource-Management-image81.png)

Untuk mengkonversi Pemesanan tentatif ke Pemesanan definitif, di papan jadwal, klik kanan Pemesanan tentatif, lalu pilih **Ubah status** \> **Pesanan definitif** \> **Definitif**.

![Mengubah status pemesanan menjadi Definitif.](media/Resource-Management-image82.png)

Pemesanan diubah, dan status berubah di papan jadwal. Karena status pemesanan sekarang **Definitif**, sumber daya ditampilkan sebagai dipesan, dan kapasitas serta ketersediaannya disesuaikan.

Anda dapat menggunakan metode yang sama untuk membatalkan pemesanan definitif atau Pemesanan tentatif dari papan jadwal.

Untuk mengkonversi sumber daya yang dipesan dengan tentatif ke definitif pada tab **tim** proyek, pilih sumber daya, lalu pilih **konfirmasikan**.

![Perintah Konfirmasi.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
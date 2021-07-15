---
title: Ikhtisar pemanfaatan sumber daya
description: Topik ini menyediakan informasi tentang tampilan pemanfaatan sumber daya di Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367940"
---
# <a name="resource-utilization-overview"></a>Ikhtisar pemanfaatan sumber daya

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Sumber daya dapat memiliki pemanfaatan yang dapat ditagih. Pemanfaatan target ini didefinisikan sebagai atribut pada peran default sumber daya atau diatur pada rekaman sumber daya yang dapat dipesan individual. Penghitungan pemanfaatan didasarkan pada jam aktual yang dilaporkan sumber daya menggunakan entri waktu yang disetujui.

Rumus berikut digunakan untuk menghitung pemanfaatan:

  - Pemanfaatan dapat ditagih = Jam aktual dapat ditagih ÷ kapasitas sumber daya
  - Pemanfaatan tidak dapat ditagih = waktu aktual dengan ID jenis penagihan = tidak dikenakan biaya, gratis, atau tidak tersedia ÷ kapasitas sumber daya
  - Internal = waktu aktual tanpa kontrak penjualan ÷ kapasitas sumber daya
  - Kapasitas sumber daya = jam kerja sumber daya – izin absen – hari tidak bekerja

Anda dapat menemukan tampilan **pemanfaatan sumber daya** di panel **sumber daya**.

Setiap sel di kisi mewakili persentase pemanfaatan yang dapat ditagih dari sumber daya dalam periode tertentu, seperti hari, pekan atau bulan. Rumus berikut digunakan untuk mewarnai sel:

  - **Hijau**: Pemanfaatan yang ditagih > = pemanfaatan target sumber daya
  - **Kuning**: target pemanfaatan – 20 < = pemanfaatan yang bisa ditagih < target pemanfaatan.
  - **Merah**: Pemanfaatan yang bisa ditagih < pemanfaatan target – 20.

Karena tampilan **pemanfaatan sumber daya** didasarkan pada papan jadwal, Anda dapat menggunakan kemampuan pemfilteran papan jadwal untuk memfilter hasil.

Kisi-kisi mengharuskan Anda menetapkan Pemanfaatan peran atau sumber daya individual. Untuk melakukan konfigurasi ini, buka **sumber daya** > **peran sumber daya**.

Selain itu, peran default harus ditetapkan ke setiap sumber daya yang dapat dipesan. Buka **Sumber Daya** > **Sumber daya**. Pada tab **Project Service**, periksa apakah peran sumber daya ditentukan, dan bidang **merupakan default** diatur ke **ya**. Anda dapat menambahkan peran tambahan di mana **merupakan default** = **Tidak**. Peran jika **merupakan default** = **Ya** digunakan untuk mengevaluasi pemanfaatan sumber daya terhadap target untuk peran tersebut.

Di tab **Project Service**, Anda juga dapat menetapkan pemanfaatan target individual untuk sumber daya. Perhitungan pemanfaatan kemudian menggunakan pemanfaatan target untuk mengevaluasi target sumber daya bukan target dari peran default sumber daya.

Pemanfaatan hanya ditampilkan untuk sumber daya hanya jika sumber daya telah disetujui, waktu yang dapat ditagih selama periode yang ditampilkan di kisi.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
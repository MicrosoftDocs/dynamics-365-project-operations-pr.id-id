---
title: Tinjau sumber daya yang diusulkan
description: Artikel ini menyediakan informasi tentang cara mengusulkan sumber daya proyek.
author: ruhercul
ms.date: 08/18/2021
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
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183978"
---
# <a name="review-proposed-resources"></a>Tinjau sumber daya yang diusulkan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Manajer sumber daya dapat mengusulkan sumber daya untuk manajer proyek menggunakan permintaan sumber daya.

Untuk memeriksa sumber daya yang diajukan, ikuti langkah-langkah berikut:

1. Dari kisi **permintaan** atau permintaan itu sendiri, pilih **Cari sumber daya**.
2. Pada halaman **Asisten Jadwal**, pilih sumber daya, lalu konfirmasikan bahwa semua jam yang diajukan tercakup dalam pemesanan yang diusulkan.
3. Di panel **Buat Pemesanan Sumber Daya**, atur bidang **Status Pemesanan** ke **Diusulkan**, lalu pilih **Pesan**.

    > [!NOTE]
    > Pengaturan **Status Pemesanan** ke **Diusulkan** tidak akan memesan sumber daya secara definitif dan tidak mengganti sumber daya generik dengan anggota tim yang bernama.

    Terjadi pembaruan status berikut:

    - Di halaman **asisten jadwal**, indikator status diperbarui untuk menunjukkan bahwa Pemesanan diajukan, bukan pesanan definitif.
    - Atas permintaan sumber daya, penguji permintaan harus mengubah status menjadi **Perlu Ditinjau**.
    - Pada tab **tim** proyek , nilai **status permintaan** anggota tim generik diubah otomatis ke **perlu ditinjau**.

Manajer proyek dapat menerima atau menolak usulan tersebut.

Bila manajer sumber daya memproses permintaan sumber daya, mereka dapat menggunakan salah satu dari pendekatan berikut:

- Mengusulkan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk memenuhi jam yang diperlukan. Jam yang diusulkan kemudian dipecah di antara beberapa sumber daya yang dapat memenuhi jam yang diperlukan. Dalam skenario ini, jam tidak dapat tumpang tindih.
- Mengusulkan sumber daya yang lebih sedikit daripada yang diperlukan. Dalam skenario ini, kapasitas sumber daya yang diusulkan kurang dari jam yang diperlukan yang ditentukan pemohon. Bila pemohon menerima sumber daya yang diusulkan, persyaratan sumber daya yang tidak terpenuhi dibuat untuk merekam permintaan yang tersisa.
- Memesan beberapa sumber daya untuk memenuhi permintaan jika tidak ada sumber daya yang tersedia untuk menyelesaikan pekerjaan.
- Memesan sumber daya yang lebih sedikit daripada yang diperlukan. Dalam skenario ini, jam yang dipesan kurang dari jam yang diperlukan. Sistem akan memandu Anda mengajukan sumber daya dan bukan Pemesanan, sehingga pemohon dapat memverifikasi dan melacak permintaan yang tersisa.

## <a name="resource-availability"></a>Ketersediaan Sumber Daya

Manajer sumber daya harus dapat melihat ketersediaan sumber daya dan memperbarui Pemesanan. Dalam kasus tertentu, tidak ada permintaan resmi (permintaan sumber daya). Namun, manajer sumber daya harus merespons permintaan tidak terencana yang masuk melalui saluran lain seperti email, panggilan telepon, atau pesan instan. Manajer sumber daya menggunakan **papan jadwal** untuk memperbarui sumber daya dan Pemesanan.

Jam kerja sumber daya digunakan sebagai dasar untuk menghitung ketersediaan sumber daya. Pemesanan sumber daya menghabiskan kapasitas sumber daya.

**Papan jadwal** menggunakan warna dan arsiran untuk menampilkan Pemesanan, ketersediaan, dan pesanan berlebihan, dan status pemesanan. Pengaturan di **Papan Jadwal** memungkinkan Anda menampilkan legenda.

Jika tanda panah menunjuk ke kanan muncul di samping sumber daya yang dapat dipesan individual pada **papan jadwal**, sumber daya dapat diperluas untuk menampilkan rincian pekerjaan yang dipesan sumber dayanya.

Karena Dynamics 365 Project Operations menggunakan mesin Universal Resource Scheduling, jika Anda juga telah menginstal Dynamics 365 Field Service, Anda dapat melihat rincian pemesanan sumber daya untuk proyek, perintah kerja, dan entitas lain yang telah Anda gunakan untuk memperpanjang penjadwalan.

Untuk melihat rincian tambahan tentang sumber daya individual, klik kanan untuk membuka kartu sumber daya.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

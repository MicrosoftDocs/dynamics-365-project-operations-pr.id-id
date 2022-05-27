---
title: Lakukan pemesanan pendahuluan sumber daya
description: Topik ini menyediakan informasi tentang cara menjadwal secara tentatif atau pemesanan pendahuluan anggota tim proyek.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/25/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.app:
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7940409db69259785268778b6f6b0b67f4b2812d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577976"
---
# <a name="soft-book-a-resource"></a>Lakukan pemesanan pendahuluan sumber daya

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Anda dapat menjadwalkan tentatif atau melakukan pemesanan pendahuluan sumber daya ke proyek tim untuk menunjukkan bahwa Anda berencana untuk menetapkan sumber daya proyek. Pemesanan pendahuluan tidak menggunakan kapasitas sumber daya yang tersedia, dan Anda dapat menetapkan anggota tim yang dipesan lebih dulu ini ke tugas proyek. Namun, karena pemesanan pendahuluan tidak menggunakan kapasitas sumber daya, Anda dapat tetap "melakukan pemesanan pasti" sumber daya untuk tugas lainnya dalam periode yang sama. Sumber daya generik tidak dapat dipesan terlebih dulu, dan pemesanan pendahuluan tidak dapat memenuhi permintaan sumber daya generik.

Anggota tim proyek yang dipesan terlebih dulu tercantum pada tab **tim** dari halaman **Proyek**, dengan jam pemesanan pendahuluan mereka ditunjukkan dalam kolom **jam pemesanan pendahuluan** dalam tampilan **anggota tim bernama**. Anggota tim dipesan terlebih dulu juga tercantum di papan jadwal. Karena mereka dipesan terlebih dulu, papan jadwal tidak menampilkan kapasitas sumber daya untuk penggunaan apa pun. Waktu dipesan terlebih dulu tidak ditampilkan pada tab **rekonsiliasi**, dan tidak ditampilkan di bidang **memperluas Pemesanan** pada tab **rekonsiliasi** di papan jadwal. 

Ada dua cara pemesanan pendahuluan anggota tim ke proyek: langsung dari papan jadwal, atau dengan menambahkan anggota tim pada tab **tim**. 

## <a name="soft-book-from-the-schedule-board"></a>Melakukan pemesanan pendahuluan dari papan jadwal
Selesaikan langkah-langkah berikut untuk memesan terlebih dulu sumber daya dari papan jadwal. 

1. Buka papan jadwal, kemudian di panel **Persyaratan Pemesanan**, pilih tab **Proyek**.
2. Temukan proyek yang Anda ingin lakukan pemesanan pendahuluan sumber daya padanya. Jika ada sejumlah besar proyek dalam daftar, pilih header kolom **proyek**, lalu gunakan filter untuk mencari satu atau beberapa proyek.
3. Pilih proyek, kemudian menarik dan menjatuhkan di kisi waktu sumber daya.
5. Di panel **buat Pemesanan sumber daya**, Sesuaikan tanggal mulai dan berakhir, Atur **Status Pemesanan** menjadi **Pemesanan pendahuluan**, lalu Atur jam. 
6. Klik **Pesan**. Sumber daya sekarang ditampilkan pada tab **tim** sebagai sumber daya untuk proyek. Pada tampilan **anggota tim bernama** Anda akan melihat jam dipesan terlebih dulu di kolom **jam dipesan terlebih dulu**.

> [!NOTE]
> Anda kini dapat menetapkan tugas yang dipesan terlebih dulu untuk tugas pada tab **jadwal**. Pada tab **rekonsiliasi**, sumber daya menunjukkan Pemesanan defisit relatif terhadap penetapan tugas mereka seperti tab **rekonsiliasi** hanya mempertimbangkan Pemesanan yang telah pasti. Anda dapat menggunakan fitur **perluas Pemesanan** ke pemesanan pasti sumber daya untuk menghilangkan defisit pemesanan pasti dibandingkan penugasan sumber daya. Anda harus secara manual membatalkan pemesanan pendahuluan sumber daya dengan menggunakan **Mengelola Pemesanan**.

## <a name="soft-book-on-the-team-tab"></a>Melakukan pemesanan pendahuluan pada tab tim

Anda dapat menambahkan anggota tim secara langsung pada tab **tim**, dan kemudian mengubah status pemesanan mereka dari **definitif** ke **tentatif** dengan **Mengelola Pemesanan**. Bila Anda menambahkan anggota tim cara ini, akan selalu mengakibatkan Pemesanan definitif kecuali jika Anda memilih metode alokasi sebagai **tidak ada**.

Untuk menggunakan metode ini, selesaikan langkah-langkah berikut.

1. Pada halaman **proyek**, pada tab **tim**, klik **baru**.
2. Pilih sumber daya dapat dipesan, peran, serta tanggal awal dan akhir.
3. Pilih metode alokasi selain **Tidak Ada**.
4. Pilih **Simpan**. Anda akan melihat sumber daya di kisi dan jam mereka di kolom **jam pesanan definitif**.
5. Kelola Pemesanan sumber daya dengan memilih **Mengelola Pemesanan**.
6. Jika papan jadwal terbuka, Perluas sumber daya untuk menampilkan Pemesanan mereka. Anda akan melihat Pemesanan yang ditampilkan sebagai **Definitif**.
7. Klik kanan pemesanan, dalam **Ubah Status**, pilih melakukan **pemesanan pendahuluan** \> **tentatif**. Status Pemesanan kini **tentatif**.
8. Setelah Anda menutup papan jadwal, Anda akan melihat bahwa jam untuk sumber daya telah berpindah dari kolom **jam pesanan definitif** ke **jam pesanan tentatif** pada kisi tab **tim**, saat melihat tampilan **anggota tim bernama**.

> [!NOTE]
> Jika Anda menggunakan **Mengelola Pemesanan** untuk mengubah status **definitif** ke **tentatif**, jika Anda melakukan pemesanan definitif sumber daya ke tim dan kemudian menetapkan tugas untuk sumber daya itu, itu akan mempertahankan tugas untuk sumber daya tersebut. Namun, pada tab **rekonsiliasi**, sumber daya akan memiliki kekurangan Pemesanan karena hanya Pemesanan definitif yang dipertimbangkan saat rekonsiliasi Pemesanan dibandingkan tugas. Anda dapat menggunakan fitur **perluas Pemesanan** di tab **Rekonsiliasi** ke pemesanan pasti sumber daya untuk menghilangkan defisit pemesanan pasti dibandingkan penugasan sumber daya. Anda harus membatalkan pemesanan pendahuluan sumber daya dengan menggunakan **Mengelola Pemesanan**.

Saat Anda siap untuk mengubah sumber daya anggota tim yang dipesan terlebih dulu ke anggota tim yang dipesan definitif, lakukan langkah berikut:

1. Di papan jadwal, Perluas sumber daya untuk menampilkan Pemesanan mereka. Anda akan melihat Pemesanan yang ditampilkan sebagai **Tentatif**.
2. Klik kanan pemesanan, dalam **Ubah Status**, pilih melakukan **pemesanan definitif** \> **definitif**. Status Pemesanan kini **Definitif**.
3. Setelah Anda menutup papan jadwal, kembali ke proyek serta buka tab **Tim**, Anda akan melihat bahwa jam untuk sumber daya telah berpindah dari kolom **jam pesanan tentatif** ke kolom **jam pesanan definitif** pada kisi tab **tim**, saat melihat tampilan **anggota tim bernama**. Jika sumber daya ditetapkan untuk tugas, mereka akan tidak lagi menunjukkan defisit Pemesanan pada tab **rekonsiliasi** karena Pemesanan mereka sekarang definitif.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

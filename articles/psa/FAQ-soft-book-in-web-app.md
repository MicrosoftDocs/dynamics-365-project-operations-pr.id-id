---
title: Bagaimana cara "melakukan pemesanan pendahuluan" sumber daya di aplikasi versi 2.x?
description: Artikel ini menjelaskan cara melakukan "pemesanan pendahuluan" anggota tim proyek dengan Project Service.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
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
ms.openlocfilehash: d7eb9e3baea3c3f696845905a2522940d14bba8a8d42917f8fe1b90c7c443747
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993920"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Bagaimana cara "melakukan pemesanan pendahuluan" sumber daya di aplikasi web (Project Service aplikasi v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Anda dapat menjadwalkan tentatif atau melakukan pemesanan pendahuluan sumber daya ke proyek tim untuk menunjukkan bahwa Anda berencana untuk menetapkan sumber daya proyek. Pemesanan pendahuluan tidak menggunakan kapasitas sumber daya yang tersedia. Anggota tim dipesan terlebih dulu tidak dapat ditetapkan ke tugas proyek. Hanya sumber daya dengan Status dipesan secara definitif dan melakukan jenis berkomitmen dapat ditetapkan ke tugas (dengan asumsi mereka memiliki jam pemesanan definitif jam untuk mencakup upaya tugas).

Anggota tim proyek dipesan terlebih dulu ditampilkan di kisi anggota tim dengan jam dipesan terlebih dulu mereka ditunjukkan dalam bidang melakukan pemesanan pendahuluan. Mereka juga akan ditampilkan di papan jadwal. Lagi, mereka tidak menunjukkan bahwa apa pun pemakaian kapasitas sebagai pemesanan pendahuluan tidak menggunakan kapasitas sumber daya.

Ada tiga cara untuk melakukan pemesanan pendahuluan anggota tim ke proyek dengan Project Service versi 2.x. Anda dapat melakukan pemesanan pendahuluan dengan papan jadwal, menggunakan fitur Mengelola Pemesanan, atau dengan membuat sumber daya generik. Metode ini dijelaskan di bawah ini.

## <a name="soft-book-with-the-schedule-board"></a>Melakukan pemesanan pendahuluan dengan papan jadwal

Untuk melakukan pemesanan pendahuluan dengan papan jadwal, ikuti prosedur ini: 
1. Buka papan jadwal.
2. Pilih tab Proyek di bawah panel di bawah Persyaratan Pemesanan di papan jadwal.
3. Temukan proyek yang Anda ingin melakukan pemesanan pendahuluan sumber daya padanya. Jika Anda memiliki banyak proyek, klik pada header kolom proyek dan kemudian menggunakan filter untuk mencari proyek Anda.
4. Klik proyek, kemudian menarik dan menjatuhkan di kisi waktu sumber daya.
5. Ini akan membuka membuat pemesanan sumber daya panel di sebelah kanan. Sesuaikan tanggal mulai dan berakhir, pilih Status Pemesanan sebagai tentatif dan atur jam. 
6. Klik Pesan.
7. Kembali pada proyek, sumber daya sekarang akan ditampilkan sebagai anggota tim dengan jam tercatat tentatif di bidang melakukan pemesanan pendahuluan.

Perhatikan bahwa Anda tidak dapat menetapkan mereka di tugas pada struktur rincian kerja (WBS) karena sumber daya harus dipesan definitif di tim yang akan ditetapkan.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Pesan terlebih dulu dengan fitur Mengelola Pemesanan

Untuk melakukan pemesanan pendahuluan dengan Mengelola Pemasangan, ikuti prosedur ini:
1. Dari kisi anggota tim, klik baru.
2. Pilih sumber daya dapat dipesan, peran, tanggal awal/akhir.
3. Pilih metode alokasi selain Nihil:
- Kapasitas Penuh
- Kapasitas Persentase
- Menurut Jam Distribusikan secara merata
- Menurut Jam Muat di depan
4. Klik Simpan. Anda akan melihat sumber daya di kisi tim dan jam ditunjukkan sebagai definitif.
5. Kelola Pemesanan sumber daya dengan mengklik Mengelola Pemesanan.
6. Jika papan jadwal terbuka, Perluas sumber daya untuk menampilkan Pemesanan mereka. Anda akan melihat Pemesanan yang ditampilkan sebagai Definitif.
7. Klik kanan pemesanan, dalam Ubah Status, pilih melakukan pemesanan pendahuluan, dan kemudian tentatif. Status Pemesanan kini tentatif.
8. Setelah menutup papan jadwal, Anda akan melihat bahwa jam untuk sumber yang telah diubah dari Definitif ke Tentatif pada kisi anggota tim.
Perlu diketahui bahwa jika Anda melakukan pemesanan definitif ke tim dan kemudian menetapkan mereka tugas dalam WBS, bila Anda menggunakan Mengelola Pemesanan untuk mengubah status definitif ke tentatif, itu akan menghapus tugs dari sumber daya tu, karena hanya sumber daya yang dipesan definitif dapat ditetapkan untuk tugas.

## <a name="soft-book-by-creating-a-generic-resource"></a>Melakukan pemesanan pendahuluan dengan membuat sumber daya generik

Anda dapat membuat pemesanan tentatif dengan membuat anggota tim sumber daya generik, memenuhi dengan papan jadwal, atau permintaan sumber daya, dan mengubah jenis selama Pemesanan.
Untuk melakukannya, ikuti prosedur berikut:

1. Pada WBS proyek, tetapkan peran untuk tugas yang Anda inginkan untuk menghasilkan anggota tim generik.
2. Klik Buat tim proyek.
3. Pada kisi anggota tim proyek, pilih sumber daya generik dan klik Pesan.
4. Di papan jadwal, pilih sumber daya yang Anda ingin pesan.
5. Pada panel membuat pemesanan sumber daya di papan jadwal, Ubah Status Pemesanan ke Tentatif.
6. Klik Pesan atau Pesan dan keluar.

Setelah menutup papan jadwal, Anda akan melihat sumber daya yang dipilih ditambahkan ke tim dengan jam dipesan tentatif, serta jam ditetapkan. Anda juga akan melihat bahwa sumber daya generik tetap dalam tim sebagai indikator bahwa tugas ditetapkan ke anggota tim yang dipesan tentatif.

Saat Anda siap untuk mengubah sumber daya anggota tim yang dipesan terlebih dulu ke anggota tim yang dipesan definitif, sehingga Anda dapat menetapkan tugas, lakukan langkah berikut:

1. Pilih sumber daya tersebut, lalu klik Mengelola Pemesanan.
2. Jika papan jadwal terbuka, Perluas sumber daya untuk menampilkan Pemesanan mereka. Anda akan melihat Pemesanan yang ditandai sebagai Tentatif.
3. Klik kanan pemesanan, dalam Ubah Status, pilih melakukan pemesanan definitif, dan kemudian definitif. Status Pemesanan kini Definitif.
4. Setelah menutup papan jadwal, Anda akan melihat bahwa jam untuk sumber yang telah diubah dari Tentatif ke Definitif pada kisi anggota tim. Anda kini dapat menetapkan sumber daya untuk tugas (asalkan ada kesejajaran antara jam dipesan definitif dan jam upaya tugas untuk tugas). Perlu diketahui bahwa jika Anda mengikuti langkah-langkah pemenuhan sumber daya generik di item #3 atas, bila Anda mengubah status sumber daya dapat dipesan tentatif ke definitif, anggota tim generik dihapus dari tim.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
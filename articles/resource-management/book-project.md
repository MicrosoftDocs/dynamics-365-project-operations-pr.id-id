---
title: Pesan untuk proyek
description: Topik ini menyediakan informasi tentang cara memesan sumber daya untuk proyek.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b47ae8cb38be6d29804aec8b069e6a8aec0ffb70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591372"
---
# <a name="book-to-a-project"></a>Pesan untuk proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Ada saat di mana manajer proyek atau manajer sumber daya harus mengalokasikan sumber daya untuk proyek tanpa persyaratan tertentu yang ditentukan dari anggota tim umum. Hal ini dapat dicapai dengan salah satu dari tiga cara.

- Memesan dari kisi anggota tim
- Memesan dari papan jadwal
- Pesan dari formulir **proyek**

## <a name="book-from-the-team-member-grid"></a>Memesan dari kisi anggota tim

Jika organisasi Anda beroperasi dalam mode alokasi sumber daya hibrid, manajer proyek dapat memesan sumber daya langsung ke proyek dengan menyelesaikan langkah-langkah berikut.

1. Dari proyek, buka kisi anggota tim, lalu pilih **baru**.
2. Tentukan nama posisi dan peran sumber daya.
3. Pilih sumber daya yang dapat dipesan dari pencarian yang tersedia.
4. Setelah Anda memilih sumber daya, tentukan informasi bidang berikut untuk memesan sumber daya:

    - Tanggal mulai
    - Tanggal Berakhir
    - Metode alokasi
    - Jam, jika berlaku
    - Pemberi Persetujuan Proyek

6. Pilih **Simpan dan Tutup**

## <a name="book-from-the-schedule-board"></a>Memesan dari papan jadwal

Bila manajer sumber daya perlu memesan sumber daya secara langsung ke proyek, mereka dapat menggunakan papan jadwal dan persyaratan proyek. Persyaratan proyek adalah persyaratan sumber daya yang selalu tersedia untuk dipesan. Selesaikan langkah-langkah berikut untuk memesan langsung ke formulir proyek dari papan jadwal.

1. Navigasi ke papan jadwal dan di halaman kiri, filter untuk sumber daya yang Anda pertimbangkan untuk kebutuhan.
2. Di panel bawah, pilih tab **proyek** untuk melihat daftar persyaratan proyek.
3. Tarik persyaratan ke sumber daya dan tentukan informasi berikut:

    - Tanggal mulai
    - Tanggal Berakhir
    - Status pemesanan
    - Metode Pemesanan
    - Durasi
   
   > [!NOTE]
   > Saat ini, Dynamics 365 Project Operations tidak mendukung papan jadwal.   

## <a name="book-from-the-project-form"></a>Pesan dari formulir proyek

Sebagai manajer proyek, Anda mungkin perlu memesan sumber daya untuk proyek, namun hanya mengetahui kriteria daripada nama sumber daya. Selesaikan langkah-langkah berikut untuk menggunakan Asisten jadwal untuk menemukan sumber daya berdasarkan atribut sumber daya yang tersedia. 

1. Navigasi ke proyek dan pilih **Pesan** untuk membuka asisten jadwal.
2. Menggunakan filter di sisi kiri asisten jadwal, Persempit kriteria, lalu pilih **Cari.**
3. Berdasarkan sumber daya yang dikembalikan dalam hasil, Anda dapat memesan sumber daya.

> [!NOTE]
> Metode ini tidak membuat pemesanan untuk sumber daya. Justru, ia menambahkan sumber daya ke tim. Setelah anggota tim ditambahkan ke proyek, manajer proyek dapat menggunakan memelihara Pemesanan atau memperpanjang Pemesanan untuk menambahkan Pemesanan yang diperlukan ke sumber daya.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

---
title: Buat pemesanan proyek dari papan jadwal
description: Artikel ini menyediakan informasi tentang cara membuat pemesanan proyek dari papan jadwal.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.reviewer: johnmichalak
ms.openlocfilehash: f231f7a862420fc4f20b4eb86e4067cbf2ed3425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930920"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Buat pemesanan proyek dari papan jadwal

[!include [banner](../includes/psa-now-project-operations.md)]

Anda dapat memesan sumber daya ke proyek baik secara langsung dari tab **tim** proyek atau dengan membuat persyaratan sumber daya dari tugas anggota tim generik dan kemudian memenuhi persyaratan yang dihasilkan dengan anggota tim proyek.

Anda juga dapat memesan sumber daya ke proyek secara langsung dari papan jadwal. Ada tiga cara untuk melakukannya:

- **Pesan dari persyaratan sumber daya yang dihasilkan** : Anda dapat membuat persyaratan sumber daya setelah membuat sumber daya generik dan menetapkan tugas dalam suatu proyek.

- **Pesan dari persyaratan utama:** persyaratan utama ditampilkan di papan jadwal pada tab **Project**. 

- **Pesan dari persyaratan sumber daya baru:** Anda dapat membuat persyaratan sumber daya dari awal dan mengaitkannya dengan proyek. Di papan jadwal, persyaratan sumber daya akan ditampilkan pada tab **persyaratan terbuka**.

## <a name="book-from-a-generated-resource-requirement"></a>Pesan dari persyaratan sumber daya yang dihasilkan.

Anda dapat membuat sumber daya generik dan menetapkan satu atau lebih tugas dalam proyek. Kemudian Anda dapat membuat persyaratan sumber daya dari anggota tim generik. 

1.  Di papan jadwal, sumber daya ini akan muncul pada tab **persyaratan terbuka**. Anda mungkin harus menggunakan filter kolom pada kisi jika Anda memiliki banyak persyaratan terbuka. 

    ![Buka tab Persyaratan di papan jadwal.](media/FAQ-Project-Booking-Schedule-Board-1.png "Tangkapan layar tabel Pemesanan dan tugas")

2. Pilih Persyaratan. Tab **cari ketersediaan** akan muncul di bagian atas baris yang dipilih.
 
3. Ketika Anda memilih tab, mode asisten jadwal papan jadwal terbuka kemudian memfilter sumber daya yang tersedia yang memenuhi persyaratan sumber daya. Setelah itu, Anda dapat memesan sumber daya.

4. Anda juga dapat tarik dan jatuhkan baris yang dipilih dari bawah papan jadwal ke sel sumber daya dalam kisi di atas. Saat Anda melepas itu, buka **membuat pemesanan sumber daya** panel di sebelah kanan.

    Memilih **Pesan** akan memesan sumber daya ke tim proyek.

![Buat panel Pemesanan Sumber Daya.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Pesan dari persyaratan utama

Membuat proyek dalam Project Service secara otomatis membuat persyaratan sumber daya yang disebut persyaratan utama. Hal ini adalah persyaratan kosong yang digunakan untuk dengan cepat memesan sumber daya dengan papan jadwal tanpa membuat persyaratan atau membuatnya dari awal. Karena persyaratan kosong, Anda harus menentukan tanggal serta metode alokasi dan jam jika berlaku. 

1. Untuk memesan sumber daya dengan persyaratan Utam, di papan jadwal, pilih tab **proyek**. Anda mungkin perlu menggunakan filter kolom di kolom **Proyek** jika Anda punya banyak proyek.

   ![Filter kolom di papan jadwal.](media/FAQ-Project-Booking-Schedule-Board-2.png "Tangkapan layar tabel Pemesanan dan tugas")

2. Pilih persyaratan yang hanya memiliki nama proyek sebagai nama dan memiliki durasi nol (0).

3. Pilih Tab **cari ketersediaan** yang akan muncul di baris. Hal ini menempatkan papan jadwal dalam mode asisten jadwal dan menampilkan sumber daya yang dapat dipesan ke proyek.

4. Karena **persyaratan utama** adalah persyaratan kosong dengan durasi nol (0), Anda harus mengatur durasi pada panel **membuat pemesanan sumber daya** saat memilih dan Pemesanan sumber daya.

5. Anda juga dapat memilih **persyaratan utama proyek** di bagian bawah papan jadwal dan tarik dan letakkan di sumber daya untuk memesannya.
 
    Karena **persyaratan utama** adalah persyaratan kosong dengan durasi nol (0), Anda harus mengatur durasi pada panel **membuat pemesanan sumber daya** saat memilih dan Pemesanan sumber daya.
 
    Bila Anda memesan sumber daya melalui **persyaratan utama** di papan jadwal, Anda menambahkannya ke tim proyek tanpa tugas apa pun.
 
## <a name="book-from-a-new-resource-requirement"></a>Pesan dari persyaratan sumber daya yang baru.
Selesaikan langkah-langkah berikut untuk memesan dari persyaratan sumber daya baru. 

1. Buka **persyaratan sumber daya** kemudian pilih **baru** untuk membuat persyaratan sumber daya baru.

2. Pada tab **proyek**, pilih proyek untuk mengaitkan persyaratan ke proyek.
 
    Di papan jadwal, persyaratan yang baru dibuat ini ditampilkan sebagai **persyaratan terbuka** yang Anda dapat memenuhi.

3. Pesan sumber daya untuk menambahkannya ke tim proyek.

4. Karena sumber daya sudah dipesan, Anda harus menetapkan tugas secara manual.



[!INCLUDE[footer-include](../includes/footer-banner.md)]

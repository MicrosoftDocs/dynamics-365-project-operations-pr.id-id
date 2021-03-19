---
title: Cara menetapkan sumber daya dapat dipesan untuk tugas di aplikasi web
description: Ikhtisar cara menetapkan sumber daya yang dapat dipesan.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b4296837cabd4c6f7e2d2924079658e45ce8b87c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286297"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a>Cara menetapkan sumber daya yang dapat dipesan untuk tugas di aplikasi web (aplikasi Project Service v2.x)?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Ada dua cara untuk menetapkan sumber daya tugas di Project Service. Anda dapat memesan sumber daya sebagai anggota tim dan menetapkan sumber daya untuk tugas. Atau, Anda dapat membuat anggota tim generik melalui penetapan peran pada tugas, membuat tim, dan kemudian memenuhi persyaratan dukungan dengan sumber daya bernama.

Perlu diketahui bahwa jika Anda ingin menetapkan sumber daya yang dapat dipesan untuk tugas, anggota tim sumber daya dapat dipesan harus memiliki Pemesanan yang cukup tersedia. Status pemesanan harus melakukan Pemesanan Nyata Jenis Komitmen dan Status berkomitmen. Jika tidak ada cukup Pemesanan sumber daya, Project Service menghilangkan tugas dan menampilkan pesan kesalahan berikut:

*Tidak dapat menetapkan sumber daya untuk tugas - sumber daya berikut ini tidak memiliki cukup jam tercatat terhadap proyek*

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Pesan sumber daya sebagai anggota tim lalu tetapkan sumber daya untuk tugas

Dengan metode ini Anda dapat menambahkan sumber daya untuk tim proyek dan kemudian menetapkan tugas ke sumber daya dalam jadwal proyek. Berikut adalah cara Anda melakukan hal ini:
1.  Pada tab Team Member, Anda dapat menambahkan anggota tim baru dengan memilih **baru**.
2.  Pada layar Team Member Quick Create, pilih nama sumber daya dapat dipesan dan tetapkan peran.
3.  Pilih tanggal **dari** dan **hingga**.

    > [!div class="mx-imgBorder"] 
    > ![Tangkapan layar menambahkan anggota tim](media/FAQ-Resources-to-Tasks2-1.png "Tangkapan layar menambahkan anggota tim")
 
4.  Pilih salah satu metode alokasi berikut untuk pemesanan sumber daya:
    - **Kapasitas Penuh** Metode ini memesan kapasitas penuh sumber daya untuk tanggal dari dan hingga yang ditentukan.
    - **Kapasitas Persentase** memesan sumber daya untuk persentase kapasitas sumber daya untuk tanggal dari dan hingga yang ditentukan.
    - **Distribusi merata Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, menyebarkannya secara merata setiap hari lebih dari yang ditentukan tanggal dari dan hingga.
    - **Muat Depan Per Jam** memesan sumber daya untuk jumlah jam yang ditentukan, memuat dulu jam per hari lebih dari yang ditentukan tanggal dari dan hingga.

    Jangan pilih **Nihil** karena ini menambahkan sumber daya ke tim, namun tidak membuat pemesanan yang menyerap kapasitas sumber daya.
5.  Pilih **Simpan**.

    Perlu diketahui bahwa jam Pemesanan harus cukup untuk menutup jam upaya dan rentang tanggal tugas yang Anda tetapkan dengan sumber daya ini. Jika mereka tidak sejajar, Anda tidak dapat menetapkan sumber daya untuk tugas.

6.  Pada struktur rincian kerja (WBS) untuk tugas, klik dropdown sel sumber daya. lalu: 

    1. Pilih **Tambahkan**.
    2. Pilih dropdown dalam **sumber daya** dan pilih anggota tim yang Anda tambahkan di atas.
    3. Pilih **OK**. Anggota tim sekarang ditetapkan ke tugas.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot menambahkan sumber daya dengan WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot menambahkan sumber daya dengan WBS")
 
Pada kisi anggota tim, Anda akan melihat agregat jam sumber daya yang ditetapkan dalam jam yang ditetapkan. Ini akan menjadi kurang dari atau sama dengan jam tercatat untuk sumber daya. 

> [!div class="mx-imgBorder"] 
> ![Screenshot jam yang ditetapkan untuk sumber daya](media/FAQ-Resources-to-Tasks2-3.png "Screenshot jam yang ditetapkan untuk sumber daya")
 
Jika tugas yang Anda coba untuk tetapkan sumber dayanya dimulai setelah tanggal berakhir Pemesanan sumber daya, sumber daya tidak akan muncul di dropdown.

Perlu diketahui bahwa Anda dapat menetapkan sumber daya untuk lebih lama daripada jam mereka tercatat jika sumber daya memiliki kapasitas belum ditugaskan yang tersisa. Dalam kasus ini sumber daya hanya akan ditetapkan sebagian hingga Pemesanan mereka. Anda dapat melihat jam tugas belum ditugaskan yang tersisa tersebut dengan menambahkan kolom jam kosong untuk struktur rincian kerja.

Jika sumber daya ditetapkan ke jam mereka dipesan (jam mereka dipesan sama dengan jam mereka ditetapkan), Anda akan melihat pesan kesalahan berikut bila Anda mencoba menetapkan mereka lebih lanjut dengan tugas:

*Tidak dapat menetapkan sumber daya untuk tugas - sumber daya berikut ini tidak memiliki cukup jam tercatat terhadap proyek.*

Selain itu, anggota tim manajer proyek default yang ditambahkan ke tim saat Anda membuat proyek ditambahkan tanpa Pemesanan apa pun dan tidak dapat ditetapkan ke tugas apa pun. Mereka tidak akan ditampilkan di dropdown sumber daya untuk tugas.

Jika Anda ingin menetapkan sumber daya ini, Anda harus menghapusnya dari tim dan kemudian kembali menambahkannya dengan alokasi metode Selain Nihil. Alasan ditambahkan ke tim ketika proyek dibuat adalah sehingga proyek memiliki minimal satu pemberi izin proyek secara default.

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a>Membuat anggota tim generik melalui penetapan peran di tugas

Metode ini menjamin bahwa sumber daya memiliki cukup Pemesanan untuk tugas. Pertama, dengan metode ini Anda membuat placeholder atau sumber daya generik yang menjelaskan karakteristik sumber daya bernama yang pada akhirnya akan bekerja pada tugas dengan membuat tim setelah menetapkan peran untuk tugas. Berikut adalah cara Anda melakukan hal ini:

1. Pada struktur rincian kerja, pilih tugas.
2. Pilih ikon dropdown **Peran yang ditetapkan** di sel sumber daya.
3. Pilih **peran** dropdown dan memilih peran untuk sumber daya generik.
4. Pilih **OK**.

    > [!div class="mx-imgBorder"] 
    > ![Screenshot menggunakan WBS untuk menambahkan sumber daya](media/FAQ-Resources-to-Tasks2-4.png "Screenshot menggunakan WBS untuk menambahkan sumber daya")
 
Setelah menyelesaikan penugasan peran untuk tugas dalam WBS, pilih **membuat tim proyek**. Project Service membuat jumlah minimum anggota tim generik berdasarkan peran, unit organisasi sumber daya, dan kalender proyek dengan menggabungkan penugasan tugas.

> [!div class="mx-imgBorder"] 
> ![Tangkapan layar membuat tim proyek](media/FAQ-Resources-to-Tasks2-5.png "Tangkapan layar membuat tim proyek")
 
Pada kisi Team Member, Anda akan melihat sumber daya jenis sumber daya generik dengan nama peran dan posisi. Jika dua sumber daya diperlukan untuk peran untuk menyelesaikan pekerjaan, fitur membuat tim membuat dua anggota tim dan menggunakan nama posisi untuk membedakan mereka.

> [!div class="mx-imgBorder"] 
> ![Screenshot menambahkan dua sumber daya umum](media/FAQ-Resources-to-Tasks2-6.png "Screenshot menambahkan dua sumber daya umum")
 
Anda dapat membuka persyaratan sumber daya dukungan untuk anggota generik tim dengan memilih link dalam persyaratan sumber daya.

> [!div class="mx-imgBorder"] 
> ![Gambar layar membuka persyaratan sumber daya pendukung](media/FAQ-Resources-to-Tasks2-7.png "Gambar layar membuka persyaratan sumber daya pendukung")

Pilih **Pesan** untuk sumber daya generik, dan kemudian Anda dapat menggunakan papan jadwal untuk mencari dan memesan sumber daya nyata. Anda juga dapat mengajukan persyaratan untuk pemenuhannya dengan memilih **Ajukan Permintaan**.

Ketika sumber daya generik dipenuhi dengan sumber daya bernama, sumber daya generik dihilangkan dari tim dan penugasan tugas untuk sumber daya generik ditetapkan ke sumber daya bernama yang memenuhi persyaratan sumber daya generik itu.
 



[!INCLUDE[footer-include](../includes/footer-banner.md)]
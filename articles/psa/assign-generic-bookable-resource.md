---
title: Tetapkan sumber daya yang dapat dipesan generik ke tim tugas dan proyek
description: Topik ini menyediakan informasi tentang pemesanan sumber daya umum untuk tugas dan tim proyek.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078499"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a>Tetapkan sumber daya yang dapat dipesan generik ke tugas dan buat persyaratan sumber daya 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Selain memesan dan menetapkan sumber daya bernama atau sumber daya nyata ke proyek Anda, Anda dapat menetapkan sumber daya umum untuk tugas proyek. Sumber daya ini dapat berfungsi sebagai placeholder untuk sumber daya bernama hingga Anda siap dengan staf proyek Anda dengan sumber daya bernama. 

1. Di Project Service Automation (PSA), buka halaman **proyek** dan pada tab **jadwal** , masukkan nama posisi sumber daya generik di sel **sumber daya** jadwal. Atau, klik ikon **sumber daya** di sel untuk membuka pemilih sumber daya, lalu masukkan nama sumber daya umum yang ingin Anda buat.

![Membuat dan menetapkan anggota tim Umum](media/RM-how-to-9.png)

Ini akan membuka panel **Buat Cepat: Anggota Tim Proyek**. 

2. Masukkan peran dan unit organisasi anggota tim sumber daya generik, lalu klik **Simpan**.

![Buat cepat anggota tim generik](media/RM-how-to-10.png)

3. Setelah Anda membuat anggota tim sumber daya generik baru, maka ditetapkan ke tugas. Anda dapat terus menetapkan sumber daya generik untuk tugas lain dalam jadwal tugas.

![Menetapkan anggota tim generik yang ada ke tugas](media/RM-how-to-11.png)

4. Setelah Anda menetapkan sumber daya generik, Anda dapat membuat persyaratan sumber daya dan memenuhinya dengan langsung memesan atau mengajukan permintaan sumber daya ke manajer sumber daya.

![Menghasilkan persyaratan untuk anggota tim generik](media/RM-how-to-12.png)

Pada kisi anggota tim, selain dapat menggunakan pemilih sumber daya sebagaimana disebutkan di atas, Anda dapat menambahkan sumber daya generik secara langsung. Sumber daya ditambahkan dengan persyaratan sumber daya yang didasarkan pada tanggal mulai/akhir dan metode alokasi yang ditentukan dalam panel **Buat Cepat: Anggota Tim Proyek**.

Anda dapat melihat perbedaan jika Anda menambahkan anggota tim umum secara langsung, lalu menetapkan lebih banyak tugas ke sumber daya umum daripada waktu yang diperlukan untuk menutupi. Klik **buat persyaratan** untuk membuat ulang persyaratan untuk menyeimbangkan jam kerja yang diperlukan terhadap tugas.

Anda juga dapat mengeklik tautan **persyaratan sumber daya** di kisi tim untuk membuka persyaratan dan menambahkan keahlian, sumber daya pilihan, dll.

![Persyaratan Sumber Daya](media/RM-how-to-13.png)


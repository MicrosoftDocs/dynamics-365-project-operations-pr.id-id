---
title: Tanya-Jawab Manajemen sumber daya
description: Topik ini memberikan jawaban atas pertanyaan umum tentang manajemen sumber daya.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078695"
---
# <a name="resource-management-faq"></a>Tanya-Jawab Manajemen sumber daya

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a>Apa perbedaan antara persyaratan anggota tim dan sumber daya?

Anggota tim proyek dapat ditetapkan ke tugas, memesan atau memesan berlebihan, dan diatur sebagai pemberi izin. Persyaratan sumber daya dapat ada tanpa anggota tim proyek, sebagai catatan draf permintaan. 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a>Apa perbedaan antara jam yang diusulkan dan dipesan tentatif?

Jam yang diusulkan dan jam yang dipesan tentatif berbeda dalam hal visibilitas. Jam yang diusulkan hanya dapat dilihat oleh Manajer sumber daya dan manajer proyek yang memulai permintaan menggunakan permintaan sumber daya. Jam pesanan tentatif dapat dilihat oleh siapa pun yang memiliki akses ke papan jadwal.

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a>Bagaimana cara melihat jam pesanan tentatif untuk sumber daya pada tim?

Pesanan tentatif dapat dilakukan ketika melakukan pemesanan persyaratan sumber daya. Sumber daya yang dipesan dengan tentatif pada tim proyek akan muncul sebagai anggota tim yang memiliki jam yang telah dipesan dengan tentatif. Mereka juga akan ditampilkan di papan jadwal.

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a>Bagaimana cara mengubah jam yang diperlukan, dan tanggal mulai dan berakhir, untuk sumber daya (generik atau bernama) yang saya pesan?

Setelah sumber daya dipesan, pilih **Kelola Pemesanan** untuk melakukan perubahan yang diperlukan.

## <a name="what-resources-types-does-project-service-automation-support"></a>Jenis sumber daya Apakah yang didukung oleh dukungan Project Service Automation?

**Pengguna** dan **kontak** adalah satu-satunya jenis sumber daya yang didukung Dynamics 365 Project Service Automation. Walaupun Anda dapat membuat jenis sumber daya lain (misalnya, **perlengkapan** , dan **grup** ), tidak ada penggunaan ujung ke ujung yang didukung.

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a>Apa antara penetapan dan Pemesanan?

Penetapan adalah Penetapan sumber daya untuk tugas proyek dalam jadwal proyek. Sumber daya dapat merupakan sumber daya riil atau generik. Pemesanan adalah alokasi sumber daya definitif atau tentatif ke proyek. Pemesanan definitif mengkonsumsi kapasitas sumber daya. Idealnya, untuk sumber daya riil, Pemesanan dan penetapan harus sesuai, karena tidak berbeda. Namun, PSA tidak menegakkan Perjanjian ini. Tampilan rekonsiliasi menunjukkan manajer proyek tempat di mana Pemesanan sumber daya dan penetapan tidak sesuai.

---
title: Metode alokasi Pemesanan di Project Service Automation
description: Topik ini menyediakan informasi tentang berbagai cara untuk memesan alokasi.
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
ms.openlocfilehash: f0f4f5c68698fbe88de968e65a65b316b10872d9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590120"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>Metode alokasi Pemesanan di Project Service Automation

[!include [banner](../includes/psa-now-project-operations.md)]

Apakah Anda menambahkan anggota tim secara langsung ke proyek pada tab **tim**, atau memesan sumber daya proyek atau persyaratan dari papan jadwal, ada beberapa metode alokasi Pemesanan yang berbeda yang dapat Anda gunakan. topik ini menjelaskan cara masing-masing metode bekerja, dan metode yang dapat menyebabkan pemesanan berlebih sumber daya.

## <a name="full-capacity"></a>Kapasitas Penuh 
Metode Kapasitas Penuh memesan kapasitas penuh sumber daya untuk tanggal dari dan hingga yang ditentukan. Misalnya, jika sumber daya memiliki kalender yang diatur ke 8 jam setiap hari kerja, 5 hari dalam seminggu, pengaturan tanggal mulai dan berakhir yang mencakup 5 hari kerja akan memesan sumber daya untuk 40 jam. Pemesanan dilakukan tanpa memperhatikan kapasitas tersisa sumber daya. Jika sumber daya sudah tercatat selama periode tersebut pada proyek lain, 40 jam dipesan sebagai tambahan jam, berpotensi menyebabkan kelebihan pemesanan.

## <a name="remaining-capacity"></a>Sisa Kapasitas
Metode Kapasitas Tersisa hanya tersedia saat Anda memesan langsung ke proyek menggunakan papan jadwal. Metode ini memesan kapasitas sumber daya yang tersedia dalam rentang tanggal yang ditentukan. Misalnya, jika sumber daya memiliki kapasitas 40 jam per minggu dan telah tercatat 10 jam, Pemesanan untuk hasil minggu yang sama dalam Pemesanan 30 jam tersisa kapasitas untuk minggu tersebut.

## <a name="percentage-capacity"></a>Kapasitas Persentase
Metode Kapasitas Persentase memesan sumber daya untuk persentase kapasitas untuk tanggal dari dan hingga yang ditentukan. Misalnya, jika sumber daya memiliki kalender yang diatur ke 8 jam setiap hari kerja, 5 hari dalam seminggu, pengaturan tanggal mulai dan berakhir yang mencakup 5 hari kerja pada kapasitas 50% akan memesan sumber daya untuk 20 jam. Masing-masing Pemesanan setiap hari adalah disebar merata di seluruh periode, empat jam sehari dalam contoh ini. Pemesanan dilakukan tanpa memperhatikan kapasitas tersisa sumber daya. Jika sumber daya sudah tercatat selama periode tersebut pada proyek lain, 20 jam dipesan sebagai tambahan jam, berpotensi menyebabkan kelebihan pemesanan.

## <a name="evenly-distribute-hours"></a>Distribusikan Jam Secara Merata
Metode Distribusi Jam merata memesan sumber daya untuk jumlah jam yang ditentukan, menyebarkan waktu secara merata setiap hari lebih dari yang ditentukan tanggal dari dan hingga. Misalnya, jika Anda memesan sumber daya untuk 20 jam selama periode waktu 5 hari, metode ini mendistribusikan 20 jam secara merata pada 4 jam sehari. Pemesanan dilakukan tanpa memperhatikan kapasitas tersisa sumber daya. Jika sumber daya sudah tercatat selama periode tersebut pada proyek lain, 20 jam dipesan sebagai tambahan jam, berpotensi menyebabkan kelebihan pemesanan.

## <a name="front-load-hours"></a>Jam Muatan Depan
Metode Jam Muat Depan memesan sumber daya untuk jumlah jam yang ditentukan, memuat dulu jam per hari lebih dari yang ditentukan tanggal dari dan hingga. Memuat dulu memakan kapasitas sumber daya yang tersedia dalam urutan "yang masuk dulu adalah yang digunakan terlebih dulu". Misalnya, jika jadwal kerja sumber daya adalah 8 jam sehari, 5 hari seminggu, dan mereka tidak memiliki Pemesanan saat ini, Pemesanan sumber daya untuk 20 jam selama periode waktu 5 hari kerja hasil dalam pola Pemesanan harian adalah seperti berikut: 

|         Pemesanan          |    Hari 1    |    Hari 2    |    Hari 3    |    Hari 4    |    Hari 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Pemesanan yang ada    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Pemesanan Baru          |    8        |    8        |    4        |    0        |    0        |    20       |

Metode memuat di depan mempertimbangkan Pemesanan yang sudah ada dan kapasitas yang tersedia. Misalnya, jika sumber daya yang sama sudah memiliki 20 jam Pemesanan dalam seminggu bekerja, Pemesanan baru menggunakan kapasitas yang tersisa sebagai berikut:

|   Pemesanan          | Hari 1 | Hari 2 | Hari 3 | Hari 4 | Hari 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| Pemesanan yang ada | 8     | 8     | 4     | 0     | 0     | 20    |
| Pemesanan Baru       | 0     | 0     | 4     | 8     | 8     | 20    |

Karena kapasitas yang tersedia dipertimbangkan, Anda mungkin mendapatkan pesan kesalahan jika sumber daya tidak mempunyai kapasitas tersisa yang dapat diserap oleh Pemesanan. Dengan cara ini, Anda tidak dapat kelebihan pesanan.

## <a name="none"></a>Tidak ada
Metode tidak ada hanya tersedia saat Anda memesan dari tab **tim** dalam proyek. Metode ini menambahkan sumber daya sebagai anggota tim proyek, namun tidak membuat pemesanan yang menyerap kapasitas sumber daya. Metode ini digunakan saat anggota tim manajer proyek default ditambahkan saat proyek dibuat. Pengguna manajer proyek yang membuat proyek ditambahkan secara default ke proyek, sehingga rekaman entitas proyek memiliki pemilik dan ada satu pemberi izin proyek. Karena pengguna ini tidak memiliki Pemesanan apa pun, jika Anda ingin memesan sumber daya Anda dapat menghapus dan kemudian kembali menambahkan mereka menggunakan metode alokasi yang berbeda, atau menambahkan sumber daya untuk tugas dan kemudian menggunakan **Perluas Pemesanan** pada tab **rekonsiliasi** untuk membuat pemesanan untuk tugas.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Metode alokasi yang menyebabkan kelebihan pemesanan
Untuk meringkas, metode alokasi berikut menyebabkan kelebihan pemesanan jika sumber daya sudah berkomitmen dalam proyek lainnya (atau untuk perintah kerja atau entitas yang dapat dijadwalkan lain):

- Kapasitas Penuh
- Kapasitas Persentase
- Distribusikan Jam Secara Merata

Saat menggunakan salah satu dari tiga metode alokasi ini, Anda tidak akan diberi tahu bahwa sumber daya kelebihan pemesanan. Untuk memperbaiki kelebihan pemesanan, Anda harus menggunakan papan jadwal.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

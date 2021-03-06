---
title: Metode alokasi pemesanan
description: Topik ini memberikan informasi tentang cara kerja metode alokasi pemesanan dalam Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 74f8889022e42a7bbd37879df870401c0e103446
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897680"
---
# <a name="booking-allocation-methods"></a>Metode alokasi pemesanan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Apakah Anda menambahkan anggota tim secara langsung ke proyek pada tab **tim**, atau memesan sumber daya proyek atau persyaratan dari papan jadwal, ada beberapa metode alokasi Pemesanan yang berbeda yang dapat Anda gunakan. topik ini menjelaskan cara masing-masing metode bekerja, dan metode yang dapat menyebabkan pemesanan berlebih sumber daya.

## <a name="booking-allocation-methods"></a>Metode alokasi pemesanan

Ada enam metode alokasi Pemesanan yang dapat Anda gunakan:

- [Kapasitas penuh](#full)
- [Kapasitas tersisa](#remaining)
- [Kapasitas persentase](#percentage)
- [Distribusikan Jam secara Merata](#evenly)
- [Jam Muatan Depan](#front)
- [Tidak ada](#none)

### <a name="full-capacity"></a><a name="full"></a>Kapasitas penuh 
Metode Kapasitas Penuh memesan kapasitas penuh sumber daya untuk tanggal dari dan hingga yang ditentukan. Misalnya, jika sumber daya memiliki kalender yang diatur ke 8 jam setiap hari kerja, 5 hari dalam seminggu, pengaturan tanggal mulai dan berakhir yang mencakup 5 hari kerja akan memesan sumber daya untuk 40 jam. Pemesanan dilakukan tanpa memperhatikan kapasitas tersisa sumber daya. Jika sumber daya sudah tercatat selama periode tersebut pada proyek lain, 40 jam dipesan sebagai tambahan jam, berpotensi menyebabkan kelebihan pemesanan.

### <a name="remaining-capacity"></a><a name="remaining"></a>Kapasitas tersisa
Metode Kapasitas Tersisa hanya tersedia saat Anda memesan langsung ke proyek menggunakan papan jadwal. Metode ini memesan kapasitas sumber daya yang tersedia dalam rentang tanggal yang ditentukan. Misalnya, jika sumber daya memiliki kapasitas 40 jam per minggu dan telah tercatat 10 jam, Pemesanan untuk hasil minggu yang sama dalam Pemesanan 30 jam tersisa kapasitas untuk minggu tersebut.

### <a name="percentage-capacity"></a><a name="percentage"></a>Kapasitas persentase
Metode Kapasitas Persentase memesan sumber daya untuk persentase kapasitas untuk tanggal dari dan hingga yang ditentukan. Misalnya, jika sumber daya memiliki kalender yang diatur ke 8 jam setiap hari kerja, 5 hari dalam seminggu, pengaturan tanggal mulai dan berakhir yang mencakup 5 hari kerja pada kapasitas 50% akan memesan sumber daya untuk 20 jam. Masing-masing Pemesanan setiap hari adalah disebar merata di seluruh periode, empat jam sehari dalam contoh ini. Pemesanan dilakukan tanpa memperhatikan kapasitas tersisa sumber daya. Jika sumber daya sudah tercatat selama periode tersebut pada proyek lain, 20 jam dipesan sebagai tambahan jam, berpotensi menyebabkan kelebihan pemesanan.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Distribusikan Jam secara Merata
Metode Distribusi Jam merata memesan sumber daya untuk jumlah jam yang ditentukan, menyebarkan waktu secara merata setiap hari lebih dari yang ditentukan tanggal dari dan hingga. Misalnya, jika Anda memesan sumber daya untuk 20 jam selama periode waktu 5 hari, metode ini mendistribusikan 20 jam secara merata pada 4 jam sehari. Pemesanan dilakukan tanpa memperhatikan kapasitas tersisa sumber daya. Jika sumber daya sudah tercatat selama periode tersebut pada proyek lain, 20 jam dipesan sebagai tambahan jam, berpotensi menyebabkan kelebihan pemesanan.

### <a name="front-load-hours"></a><a name="front"></a>Jam Muatan Depan
Metode Jam Muat Depan memesan sumber daya untuk jumlah jam yang ditentukan, memuat dulu jam per hari lebih dari yang ditentukan tanggal dari dan hingga. Memuat dulu memakan kapasitas sumber daya yang tersedia dalam urutan "yang masuk dulu adalah yang digunakan terlebih dulu". Misalnya, jika jadwal kerja sumber daya adalah 8 jam sehari, 5 hari seminggu, dan mereka tidak memiliki Pemesanan saat ini, Pemesanan sumber daya untuk 20 jam selama periode waktu 5 hari kerja hasil dalam pola Pemesanan harian adalah seperti berikut: 

|                           |    Hari 1    |    Hari 2    |    Hari 3    |    Hari 4    |    Hari 5    |    Total    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Pemesanan yang ada**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Pemesanan Baru**          |    8        |    8        |    4        |    0        |    0        |    20       |

Metode memuat di depan mempertimbangkan Pemesanan yang sudah ada dan kapasitas yang tersedia. Misalnya, jika sumber daya yang sama sudah memiliki 20 jam Pemesanan dalam seminggu bekerja, Pemesanan baru menggunakan kapasitas yang tersisa sebagai berikut:

|                     | Hari 1 | Hari 2 | Hari 3 | Hari 4 | Hari 5 | Total |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Pemesanan yang ada** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Pemesanan Baru**       | 0     | 0     | 4     | 8     | 8     | 20    |

Karena kapasitas yang tersedia dipertimbangkan, Anda mungkin mendapatkan pesan kesalahan jika sumber daya tidak mempunyai kapasitas tersisa yang dapat diserap oleh Pemesanan. Dengan cara ini, Anda tidak dapat kelebihan pesanan.

### <a name="none"></a><a name="none"></a>Tidak ada
Metode tidak ada hanya tersedia saat Anda memesan dari tab **tim** dalam proyek. Metode ini menambahkan sumber daya sebagai anggota tim proyek, namun tidak membuat pemesanan yang menyerap kapasitas sumber daya. Metode ini digunakan saat anggota tim manajer proyek default ditambahkan saat proyek dibuat. Pengguna manajer proyek yang membuat proyek ditambahkan secara default ke proyek, sehingga rekaman entitas proyek memiliki pemilik dan ada satu pemberi izin proyek. Karena pengguna ini tidak memiliki Pemesanan apa pun, jika Anda ingin memesan sumber daya Anda dapat menghapus dan kemudian kembali menambahkan mereka menggunakan metode alokasi yang berbeda, atau menambahkan sumber daya untuk tugas dan kemudian menggunakan **Perluas Pemesanan** pada tab **rekonsiliasi** untuk membuat pemesanan untuk tugas.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Metode alokasi yang menyebabkan kelebihan pemesanan
Untuk meringkas, metode alokasi berikut menyebabkan kelebihan pemesanan jika sumber daya sudah berkomitmen dalam proyek lainnya (atau untuk perintah kerja atau entitas yang dapat dijadwalkan lain):

- Kapasitas Penuh
- Kapasitas Persentase
- Distribusikan Jam Secara Merata

Saat menggunakan salah satu dari tiga metode alokasi ini, Anda tidak akan diberi tahu bahwa sumber daya kelebihan pemesanan. Untuk memperbaiki kelebihan pemesanan, Anda harus menggunakan papan jadwal.

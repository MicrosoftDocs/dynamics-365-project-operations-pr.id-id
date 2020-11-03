---
title: Buat tim proyek
description: Topik ini menyediakan informasi tentang cara membuat dan mengeluarkan tim proyek.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7eb9101352afd27b527bf6b8acc6f92198f44ea
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078649"
---
# <a name="create-a-project-team"></a>Membuat tim proyek

[!include [banner](../includes/banner.md)]

Untuk menggunakan peran yang sebelumnya diatur dalam proyek, manajer proyek harus mengaitkan peran dengan proyek. Peran ganda dapat ditetapkan untuk proyek. Untuk mencegah kebingungan, peran ini akan secara otomatis dilabeli saat reservasi. Misalnya, jika manajer proyek memerlukan tiga insinyur perangkat lunak, tiga peran insinyur perangkat lunak yang memiliki label **insinyur perangkat lunak 1** , **insinyur perangkat lunak 2** , dan **insinyur perangkat lunak 3** yang akan dibuat secara otomatis. Jika karakteristik peran sebelumnya diatur untuk peran, peran akan diterapkan sebagai filter selama pencarian untuk sumber daya. Karakteristik tambahan dapat ditambahkan sebagaimana diperlukan untuk lebih menyempurnakan pencarian.

Pengaturan tampilan juga dapat disesuaikan untuk memberikan tampilan yang lebih baik ketersediaan sumber daya. Tersedia pilihan untuk menampilkan ketersediaan per jam, harian, mingguan, bulanan, kuartalan, dan tahunan. Ada juga pilihan untuk menunjukkan kapasitas yang tersedia dan tersisa pada sumber daya. Pilihan ini berguna untuk manajemen waktu, saat Anda memperkirakan waktu yang tersedia untuk aktivitas atau ketersediaan sumber daya.

Manajer proyek dapat memilih peran pada halaman dan kemudian, jika ada sumber daya yang tersedia yang sesuai dengan persyaratan, pilih untuk mencadangkan sumber daya untuk mengisi peran. Perhatikan bahwa sumber daya tidak harus dicadangkan pada saat ini dalam tahap perencanaan. Bila Anda membuat WBS, Anda dapat mengganti peran dengan sumber daya staf untuk proyek. Jika peran diganti dengan sumber daya staf di WBS, pengaturan sumber daya secara otomatis memperbarui daftar tim proyek dan penjadwalan.

[![Daftar tim proyek yang mencakup peran dan sumber daya aktual](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Manajer Proyek memiliki berbagai pilihan untuk memesan sumber daya untuk proyek, seperti **kapasitas yang tersisa** , **kapasitas penuh** , **persentase kapasitas** , dan **Tentukan jam**. Pilihan Pemesanan ini dapat dibatalkan sewaktu-waktu jika tugas sumber daya berubah. Dua jenis Pemesanan yang didukung:

- **Definitif** -sumber daya reservasi disetujui dan dikonfirmasi untuk bekerja pada keterlibatan untuk durasi yang ditentukan.
- **Tentatif** - Reservasi sumber daya diatur secara tentatif untuk bekerja pada keterlibatan untuk durasi yang ditentukan.

Prosedur berikut menjelaskan cara membuat tim proyek.

## <a name="create-a-project-team"></a>Membuat tim proyek

1. Pada halaman daftar **semua proyek** , pilih proyek, lalu pilih **Edit**.
2. Pada tab **tim proyek dan penjadwalan** , di bidang **tanggal akhir jadwal** , masukkan tanggal mulai jadwal ditambah satu bulan. Misalnya, jika tanggal mulai jadwal adalah 24 Juni 2017 (24/06/2017), masukkan **24/07/2017**.
3. Pilih **Tambahkan**.
4. Di panel **Tambah peran ke proyek** , di bidang **peran** , pilih **manajer proyek senior**.
5. Pilih **kompetensi yang diperlukan**.
6. Pada halaman **Pilih karakteristik** , karakteristik yang telah Anda atur untuk peran senior manajer proyek dipilih secara default. Pilih **OK**.
7. Pada halaman **Tambah peran ke proyek** , di bidang **jumlah sumber daya** , masukkan **1**.
8. Di bidang **sumber daya** , pencarian menampilkan semua sumber daya yang memiliki kompetensi yang diperlukan. Pilih **Daniel Goldschmidt** , lalu pilih **buat**.
9. Pada halaman **Proyek** , pilih **Tambah**.
10. Di panel **Tambah peran ke proyek** , di bidang **peran** , pilih **Anggota tim**. Di bidang **Jumlah sumber daya** , masukkan **5**.
11. Pilih **Buat**.
12. Pada halaman **proyek** , pilih **penuhi sumber daya**.

## <a name="monitor-project-teams"></a>Memantau tim proyek
1. Pada halaman **semua proyek** , pilih tautan **ID proyek** untuk proyek **peningkatan XYZ fase 2**.
2. Pada FastTab **tim proyek dan penjadwalan** , Verifikasikan bahwa sumber daya proyek yang tercantum sudah benar.

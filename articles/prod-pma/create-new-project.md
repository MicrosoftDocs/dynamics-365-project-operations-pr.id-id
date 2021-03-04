---
title: Buat proyek baru
description: Topik ini menyediakan informasi tentang cara membuat proyek baru.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 727d287c571b2a64bf10b2393a87567093a420d2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078619"
---
# <a name="create-a-new-project"></a>Buat proyek baru

[!include [banner](../includes/banner.md)]

Selesaikan langkah-langkah berikut untuk membuat proyek baru.

1. Di **Manajemen proyek** , pilih **Proyek baru** dan masukkan nilai berikut:

    - **Jenis proyek:** waktu dan material
    - **Nama proyek:** Peningkatan XYZ fase 2
    - **Grup proyek:** TM\_WIP
    - **ID Kontrak Proyek:** 00000002

2. Pilih **Buat proyek baru**.

## <a name="assign-a-resource-to-a-project"></a>Menetapkan sumber daya untuk proyek

1. Pada halaman **pekerja** , dalam **Daftar pekerja** , pilih rekaman untuk pekerja yang sebelumnya Anda konfigurasikan kompetensinya, dan buka rekaman pekerja.
2. Pada panel tindakan, pada tab **Proyek** , di grup **Konfigurasi** , pilih **tetapkan proyek**.
3. Pada halaman **penugasan proyek validasi sumber daya** , pada tab **proyek** , di bidang **Tambah proyek ke proyek yang dipilih** , filter proyek **Peningkatan XYZ fase 2**.
4. Di panel **proyek lainnya** , pilih proyek, lalu pilih tombol panah untuk menambahkannya ke panel **proyek yang dipilih**.

Anda juga dapat menetapkan kategori untuk sumber daya sesuai kebutuhan. Jenis kategori adalah **biaya** atau **pendapatan**. Jenis kategori ditentukan oleh organisasi Anda. Jika tidak ada kategori yang ditetapkan untuk sumber daya, Finance akan mencari kategori default pada harga jam untuk biaya dan pendapatan.

## <a name="set-up-project-resource-and-role-characteristics"></a>Konfigurasi sumber daya proyek dan karakteristik peran

Manajer proyek dapat menggunakan fungsi sumber daya proyek untuk membuat peran yang diperlukan untuk proyek. Peran dapat digunakan jika sumber daya terkonfirmasi masih belum diketahui saat sumber daya dicadangkan. Peran dapat sementara dicadangkan sebagai sumber daya yang direncanakan, sehingga Anda dapat melanjutkan tahapan Perencanaan proyek.

[![Contoh peran](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg) 

**Skenario:** Aswono dipekerjakan untuk menyelesaikan proyek waktu dan material yang memiliki Piagam proyek disetujui. Manajer Proyek Junior masih menyelesaikan cakupan proyek. Manajer sumber daya saat ini mengidentifikasi sumber daya tertentu yang akan dicadangkan untuk mengerjakan proyek baru. Karena sifat penting proyek, sponsor proyek meminta manajer proyek senior sebagai salah satu peran. Manajer sumber daya harus mendapatkan sumber daya baru dan menentukan peran dalam sistem seandainya manajer proyek Junior memerlukan informasi sumber daya selama perencanaan proyek.

Langkah-langkah berikut ini menunjukkan cara manajer sumber daya dapat mengkonfigurasi peran manajer proyek senior dan mengaitkan karakteristik sumber daya dengannya. Selanjutnya, peran dapat digunakan untuk mencari sumber daya yang tersedia yang sesuai dengan kompetensi sumber daya yang diperlukan.

1. Di **Konfigurasi Peran** , pilih **baru** dan masukkan nilai berikut:

    - **ID peran:** manajer proyek senior
    - **Deskripsi:** manajer proyek senior

2. Pilih **Buat**.
3. Pilih peran **manajer proyek senior** , lalu pilih **Konfigurasikan karakteristik**.
4. Di bidang **Jenis karakteristik** , pilih **Keterampilan**.
5. Di bidang **Karakteristik yang tersedia** , masukkan keterampilan yang akan dicari.
6. Di bidang **Jenis karakteristik** , pilih **sertifikat**.
7. Di bidang **Karakteristik yang tersedia** , masukkan jenis sertifikat yang akan dicari.

## <a name="assign-a-project-resource-to-a-project"></a>Menetapkan sumber daya proyek untuk proyek

1. Pada halaman **semua proyek** , pilih proyek **peningkatan XYZ fase 2**.
2. Pada tab **tim proyek dan penjadwalan** , pilih **Tambah**.
3. Di bidang **peran** , pilih **anggota tim**.
4. Pilih **Pesan dari kalender**.
5. Pada halaman **ketersediaan sumber daya** , pilih **lihat pengaturan**.
6. Pada halaman **Atur pengaturan tampilan** , masukkan nilai berikut:

    - **Format untuk tampilan rentang tanggal:** Hari
    - **Tampilkan deskripsi ketersediaan:** ya
    - **Menampilkan kapasitas tersisa:** ya

7. Di daftar sumber daya, pilih sumber daya.
8. Pilih **Definitif** dan **kapasitas penuh**.

## <a name="assign-a-resource-to-a-default-role"></a>Menetapkan sumber daya ke peran keamanan

Untuk membantu manajer proyek atau sumber daya dapat menelusuri dengan detail lebih lanjut tentang sumber daya yang dapat dicadangkan untuk proyek. Anda dapat mengaitkan peran default dengan sumber daya yang ada atau sumber daya yang baru diperoleh. Misalnya, ketika Daniel dipekerjakan, dia memiliki pengalaman dan keterampilan untuk mengisi peran analis bisnis. Manajer sumber daya menetapkan peran ini sebagai peran default Daniel. Oleh karena itu, manajer sumber daya menambahkan Daniel ke kumpulan analis bisnis yang tersedia untuk bekerja pada proyek.

Selama reservasi sumber daya, manajer proyek dapat memfilter sumber daya peran yang tersedia untuk proyek. Mereka dapat menggunakan informasi ini sebagai salah satu kriteria saat mereka melakukan analisis keputusan multi-kriteria selama pemenuhan sumber daya. Mereka juga dapat menambahkan karakteristik sumber daya lain ke filter untuk mencari sumber daya yang memiliki keterampilan khusus, pendidikan, dan pengalaman untuk proyek tertentu.

**Skenario:** proyek yang disetujui telah dimulai, dan peran manajer proyek senior dicadangkan sebagai sumber daya yang direncanakan selama tahap perencanaan proyek. Manajer sumber daya sekarang memperoleh sumber daya untuk memenuhi peran manajer proyek senior.

1. Pada halaman **daftar sumber daya** , pilih **Daniel goldschmidt**.
2. Di **Peran sumber daya** , pilih **baru** dan masukkan nilai berikut:

    - **Efektif:** masukkan tanggal saat ini.
    - **Kedaluwarsa:** Masukkan **tidak pernah**.
    - **Peran:** Masukkan **manajer proyek senior**.

3. Pilih **Simpan** , lalu tutup halaman.
4. Pada tab **kompetensi** , tambahkan Keterampilan **projectmgmt** dan sertifikat **PMP**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
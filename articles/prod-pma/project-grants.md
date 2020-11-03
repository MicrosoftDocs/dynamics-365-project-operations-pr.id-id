---
title: Hibah proyek
description: Topik ini menjelaskan cara membuat atau memodifikasi hibah.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/16/2020
ms.locfileid: "4078665"
---
# <a name="project-grants"></a>Hibah proyek

[!include [banner](../includes/banner.md)]

Hibah adalah hadiah uang untuk tujuan tertentu atau proyek. Biasanya, ada pembatasan tentang bagaimana hibah dapat dibelanjakan. Dalam manajemen proyek dan akuntansi, anda dapat memasukkan dan melacak hibah, dan menentukan Relasi mereka ke proyek dan kontrak proyek. Contohnya, Anda bisa melakukan tugas berikut:

- Mengasosiasikan hibah dengan proyek dan sumber pendanaan melalui tautan ke halaman **Proyek** dan **rincian kontrak proyek**.
- Memasukkan dan melacak perubahan pada hibah saat bergerak dari satu status ke status lainnya.
- Memasukkan dan melacak biaya, jumlah yang diminta, dan jumlah yang diberikan.
- Membuat hibah induk, dan mengaitkan subhibah dengan mereka.

Anda dapat membuat hibah dengan memasukkan semua rincian dalam rekaman baru, atau Anda dapat menyalin rincian dari hibah yang ada dan kemudian memperbaruinya.

## <a name="create-a-new-grant"></a>Buat hibah baru

1. Buka **manajemen proyek dan akuntansi** \> **Hibah** \> **Hibah**.
2. Pilih **baru** \> **hibah**.
3. Pada halaman rincian hibah, pada fasttab **umum** , di bidang **id hibah** , masukkan pengidentifikasi alfanumerik untuk hibah.
4. Di bidang **Nama hibah** , masukkan nama unik untuk hibah.
5. Di bidang **Deskripsi** , Tambahkan rincian tentang hibah baru.

    Sebagian besar bidang lain pada halaman bersifat opsional, dan Anda dapat memasukkan sesedikit atau sebanyak mungkin informasi yang Anda inginkan.

    Daftar berikut ini menjelaskan informasi yang ditentukan pada setiap FastTab dari halaman rincian hibah:

    - **Umum** – Masukkan nama hibah, status, deskripsi, tujuan, dan jumlah.
    - **Informasi kontak** – Masukkan rincian tentang anggota staf, Departemen yang mengelola hibah, dan pelanggan hibah atau sumber organisasi dari hibah. Anda juga dapat menunjukkan Apakah organisasi Anda adalah entitas penerusan yang menerima hibah, lalu meneruskannya ke penerima lain. Pilih **Tambah** untuk menambahkan informasi kontak seperti nomor telepon dan alamat email untuk organisasi yang menyediakan hibah.
    - **Tanggal dan tenggat waktu** – masukkan tanggal yang terkait dengan hibah dan aplikasi hibah. Contohnya mencakup tanggal jatuh tempo, tanggal pengiriman, dan tanggal saat hibah disetujui atau ditolak.
    - **Terkait proyek dan kontrak proyek** – Anda dapat memasukkan informasi tentang fasttab ini hanya jika bidang **status hibah** pada fasttab **umum** diatur ke **aktif** atau **diberikan**. Pilih di antara pilihan berikut untuk menyelesaikan tugas terkait:

        - **Tambah sumber pendanaan** -tambahkan sumber pendanaan baru untuk hibah. Anda dapat memasukkan semua rincian sekarang, atau Anda dapat menggunakan informasi default dan kemudian memperbaruinya nanti.
        - **Tambahkan kontrak proyek** -Tambahkan atau perbarui informasi kontrak proyek.
        - **Tambah proyek** -Tambah atau Perbarui rincian proyek.

    - **Konfigurasi** -Masukkan rincian tentang dana yang cocok, jika informasi ini diperlukan. Banyak organisasi yang memberikan hibah mengharuskan Penerima menghabiskan sejumlah uang atau sumber daya mereka sendiri untuk mencocokkan jumlah yang dianugerahkan dalam hibah. Di bidang **proyek lokal atau id pelacakan** , Anda dapat memasukkan pengidentifikasi yang berbeda dari pengidentifikasi proyek.

        > [!NOTE]
        > Jika bagian dari hibah akan diberikan ke organisasi lain, atur pilihan **subpemberi** ke **ya**. Untuk hibah yang diberikan di Amerika Serikat, Anda dapat menentukan apakah hibah akan diberikan berdasarkan mandat negara bagian atau mandat federal.

    - **Rincian penarikan** -menambah atau memperbarui informasi tentang seberapa sering dana hibah dapat ditarik, ditagih, atau dibelanjakan.

## <a name="create-a-new-grant-from-a-copy"></a>Membuat hibah baru dari salinan

1. Buka **manajemen proyek dan akuntansi** \> **Hibah** \> **Hibah**.
2. Pilih **baru** \> **salinan dari hibah**.
3. Masukkan pengidentifikasi alfanumerik dan nama untuk hibah baru, lalu pilih **OK**.
4. Pada halaman rincian hibah, Tinjau rincian hibah yang disalin, dan buat perubahan yang diperlukan. Sebagian besar bidang pada halaman bersifat opsional.

## <a name="view-or-modify-grant-details"></a>Melihat atau memodifikasi rincian hibah

1. Buka **manajemen proyek dan akuntansi** \> **Hibah** \> **Hibah**.
2. Pilih hibah untuk dimodifikasi.
3. Pada panel tindakan, pada tab **Hibah** , di grup **Kelola** , pilih **Edit**.
4. Tinjau rincian hibah, dan buat perubahan yang diperlukan.

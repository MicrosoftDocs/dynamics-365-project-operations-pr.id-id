---
title: Integrasi Microsoft Project client
description: Merencanakan dan memelihara jadwal proyek dapat menjadi rumit, sehingga manajer proyek harus menggunakan alat bantu yang membantu mereka mengelola tugas ini. Integrasi dengan Microsoft Project Client memberikan dukungan untuk membuka dan mengelola struktur rincian kerja proyek.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289328"
---
# <a name="microsoft-project-client-integration"></a>Integrasi Microsoft Project client

[!include [banner](../includes/banner.md)]

Merencanakan dan memelihara jadwal proyek dapat menjadi rumit, sehingga manajer proyek harus menggunakan alat bantu yang membantu mereka mengelola tugas ini. Integrasi dengan Microsoft Project Client memberikan dukungan untuk membuka dan mengelola struktur rincian kerja proyek. Manajer proyek dapat mempublikasikan perubahan apa pun kembali ke struktur rincian kerja proyek Dynamics 365 Finance.

> [!NOTE]
> Jika Anda menggunakan Pembaruan bulan Juli (versi 10.0.4), Anda harus menginstal KB 4054797 dan 4055884.

## <a name="configure-the-microsoft-project-client-add-in"></a>Mengkonfigurasi Add-in Microsoft Project Client
Untuk mengaktifkan integrasi dengan Microsoft Project Client, Add-in Microsoft Dynamics 365 diperlukan untuk diinstal di aplikasi Microsoft Project Client pengguna. Hal ini dilakukan dengan membuka **ruang kerja manajemen proyek**.

•   Klik **Konfigurasikan Add-in klien proyek** dari bagian **Tautan** > **Konfigurasi** di ruang kerja.

•   Klik **buka**, lalu klik **Jalankan** saat diminta.

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>Membuka dan mengedit struktur rincian kerja konsep yang ada di Microsoft Project Client
Jika proyek di Dynamics 365 Finance sudah memiliki struktur rincian kerja yang dibuat, struktur rincian kerja dapat dibuka di aplikasi Microsoft Project Client jika struktur rincian kerja berada dalam status draf. Untuk membuka dari halaman **proyek**, klik tautan **buka di Microsoft Project** dari tab **Paket**. Halaman ini juga dapat dibuka dari dalam aplikasi Microsoft Project Client dengan mengklik tab **buka** di **Microsoft Dynamics 365.** Pilih **entitas hukum** dan **proyek** dari daftar.

> [!NOTE]
> Jika Anda menggunakan Internet Explorer sebagai browser, Anda harus mengklik **Simpan** untuk membuka secara manual dari lokasi yang akan diunduh file-nya. Atau, klik **Simpan dan buka** untuk membuka file di Microsoft Project Client. Jangan Namai ulang file saat menyimpan.

Sebelum membuat pengeditan apa pun ke file menggunakan Microsoft Project Client, Anda harus memeriksanya. Klik **Check-out** di tab **Microsoft Dynamics 365**. Hal ini akan mencegah pengguna lain mengedit struktur rincian kerja dari dalam Finance pada waktu yang sama. Untuk mempublikasikan struktur rincian kerja setelah menyelesaikan pengeditan apa pun, klik **Check-in** pada tab **Microsoft Dynamics 365**.

Jika tim proyek telah ditambahkan ke proyek di Finance, daftar sumber daya akan diisi dengan anggota tim. Jika tim proyek belum ditambahkan ke proyek, Anda dapat memilih sumber daya dan membuat tim dalam Microsoft Project Client dengan mengklik tombol **sumber daya** pada tab **Microsoft Dynamics 365**. 

Data berikut akan disinkronisasikan kembali ke Finance sebagai bagian dari proses Check-In:

•   Nama tugas

•   Tanggal Mulai

•   Tanggal Berakhir

•   Pendahulu

•   Nama sumber daya

•   Kategori

•   Kategori Sumber Daya

•   Jam Kerja

•   Catatan

•   Prioritas

> [!NOTE]
> Jika Anda menambahkan bidang lain ke file Microsoft Project Client, mereka tidak akan disimpan ke file, dan tidak akan ditampilkan saat file dibuka kembali.

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Buat struktur rincian kerja untuk proyek yang ada menggunakan Microsoft Project Client
Untuk membuat struktur rincian kerja menggunakan Microsoft Project Client, ikuti langkah-langkah berikut ini:


1.  Buka Microsoft Project Client.

2.  Di tab **Microsoft Dynamics 365**, klik **Buka**.

3.  Pilih **entitas hukum** untuk proyek.

4.  Pilih **proyek**.

5.  Klik **Check out** di tab **Microsoft Dynamics 365**.

6.  Bila siap untuk dipublikasikan ke Finance, klik **Check-in** pada tab **Microsoft Dynamics 365**.

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>Ganti struktur rincian kerja yang ada untuk proyek yang ada menggunakan Microsoft Project Client
Untuk membuat struktur rincian kerja baru menggunakan Microsoft Project Client dan mengganti struktur rincian kerja yang ada untuk proyek yang ada, ikuti langkah-langkah berikut:

1.  Buka Microsoft Project Client.

2.  Buat jadwal di Microsoft Project Client.

3.  Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **ganti proyek yang ada**.

4.  Pilih **entitas hukum** untuk proyek.

5.  Pilih **proyek**.

6.  Klik **OK**.

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>Membuat proyek baru dari dalam Microsoft Project client


1.  Buka Microsoft Project Client.

2.  Buat jadwal di Microsoft Project Client.

3.  Pada tab **Microsoft Dynamics 365**, klik **Simpan perubahan** > **Simpan ke Proyek baru**.

4.  Pilih **entitas hukum** untuk proyek.

5.  Masukkan **id proyek**, jika perlu.

6.  Masukkan **nama proyek**.

7.  Pilih **jenis proyek**, **grup proyek**, dan **id kontrak proyek**. Atau, Anda dapat membuat kontrak proyek baru dengan mengeklik **baru**.

8.  Pilih **kalender** yang akan digunakan untuk sumber daya.

11. Klik **OK**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
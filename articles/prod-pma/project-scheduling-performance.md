---
title: Kinerja penjadwalan sumber daya proyek
description: Topik ini menyediakan informasi tentang cara meningkatkan kinerja penjadwalan sumber daya untuk sejumlah besar proyek.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007285"
---
# <a name="project-resource-scheduling-performance"></a>Kinerja penjadwalan sumber daya proyek

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Masalah performa yang terkait dengan penjadwalan sumber daya dapat terjadi saat jumlah proyek mencapai ribuan. Untuk meningkatkan performa penjadwalan sumber daya, tersedia fitur yang memungkinkan pengguna mengurangi waktu yang diperlukan untuk meluncurkan formulir ketersediaan sumber daya. Khususnya, ini akan menghapus proses sinkronisasi peningkatan kapasitas sumber daya dan menggunakan tabel **resprojectresource** untuk mempercepat pencarian sumber daya. Perhatikan bahwa tabel **resrollup** tidak akan lagi digunakan.

> [!IMPORTANT]
> Jika ada ketergantungan pada proses sinkronisasi peningkatan kapasitas sumber daya atau tabel **resprojectresource**, jangan gunakan fitur ini.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Aktifkan peningkatan performa penjadwalan sumber daya
Untuk mengaktifkan peningkatan performa penjadwalan sumber daya, selesaikan langkah berikut.

1. Buka **manajemen fitur** > **semua**, dan dalam daftar fitur, Cari **Aktifkan fitur peningkatan kinerja penjadwalan sumber daya proyek**.
2. Klik **Aktifkan sekarang**.

> [!NOTE]
> Jika Anda tidak dapat menemukan fitur dalam daftar, pilih **Periksa pembaruan** untuk me-refresh daftar.

3. Refresh browser Anda, lalu buka **manajemen proyek dan akuntansi** > **periodik** > **sumber daya proyek** > **sinkronisasikan kapasitas kalender sumber daya di semua perusahaan**.
4. Atur **Hapus rekaman kapasitas yang ada** ke **ya** untuk menghapus data sebelumnya. Jika Anda ingin menghasilkan data inkremental, atur ke **tidak**.
5. Di bidang **kode periode**, pilih periode saat data harus dibuat. Jika Anda memilih kode periode, tanggal mulai dan berakhir tidak perlu ditentukan.
6. Jika Anda membiarkan bidang **kode periode** kosong, pilih tanggal mulai dan berakhir yang spesifik untuk menghasilkan data.
7. Pilih **OK**.

 > [!NOTE]
 > Ini akan mendistribusikan data umum ke tabel **rescalendarcapacity** di semua perusahaan di lingkungan Anda, sehingga pekerjaan batch hanya perlu dijalankan di satu entitas hukum. Data dalam pekerjaan batch ini diperlukan untuk menghitung kapasitas sumber daya melalui kalender terkait.

8. Buka **manajemen proyek akuntansi** > **periodik** > **sumber daya proyek** > **isi sumber daya proyek di semua perusahaan**, lalu pilih **OK**. Ini adalah skrip peningkatan data untuk data umum di tabel **ResProjectResource**, **ResCalendarDateTimeRange**, dan **ResEffectiveDateTimeRange**. Nilai untuk bidang **PSAPRojSchedRole.RootActivity** juga diperbarui. Jika ini tidak dijalankan, Anda akan menerima peringatan saat Anda mencoba menjalankan operasi penjadwalan sumber daya.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Nonaktifkan peningkatan performa penjadwalan sumber daya

1. Buka **manajemen fitur** > **semua**, dan cari **Aktifkan fitur peningkatan kinerja penjadwalan sumber daya proyek**.
2. Pilih fitur, lalu pilih tombol **Nonaktifkan**.
3. Refresh browser Anda.
4. Buka **manajemen proyek dan akuntansi** > **Periodik** > **Sinkronisasi kapasitas** > **Sinkronisasi peningkatan kapasitas sumber daya**.
5. Pada halaman **sinkronisasi peningkatan kapasitas**, atur **penghapusan rekaman kapasitas yang ada** ke **ya** untuk menghapus data sebelumnya. Jika Anda ingin menghasilkan data inkremental, atur ke **tidak**.
6. Di bidang **kode periode**, pilih periode saat data harus dibuat. Jika Anda memilih kode periode, tanggal mulai dan berakhir tidak perlu ditentukan.
7. Jika Anda membiarkan bidang **kode periode** kosong, pilih tanggal mulai dan berakhir yang spesifik untuk menghasilkan data.
8. Pilih **OK**.

> [!NOTE]
> Ini akan mendistribusikan data umum ke tabel **ResRollup** di semua perusahaan di lingkungan Anda, sehingga pekerjaan batch hanya perlu dijalankan di satu entitas hukum. Pekerjaan batch ini diperlukan untuk semua tampilan **ketersediaan sumber daya**. Jika pekerjaan batch ini tidak berjalan, data **ResRollup** akan dibuat sambil berjalan, yang dapat memakan waktu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
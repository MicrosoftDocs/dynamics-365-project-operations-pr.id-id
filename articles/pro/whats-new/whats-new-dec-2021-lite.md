---
title: Yang baru di bulan Desember 2021 - Penyebaran Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di penyebaran Project Operations lite Desember 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 301acc5be76fb0318d6298820b62ae5bb05efac3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8914084"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Yang baru di bulan Desember 2021 - Penyebaran Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

### <a name="subcontract-management"></a>Manajemen subkontrak 

- [Mensubkontrakkan anggota tim proyek](../subcontracting/subcontracting-project-team-members.md): Manajer proyek dapat membuat anggota tim bernama atau generik dengan subkontrak dan baris subkontrak untuk mempengaruhi staf dan perkiraan.
- [Mensubkontrakkan pilihan untuk anggota tim proyek](../subcontracting/subcon-options.md): Bila membuat pilihan staf untuk anggota tim proyek yang bernama atau generik, manajer proyek dapat memeriksa subkontrak yang ada atau membuat subkontrak baru untuk satu atau beberapa anggota tim proyek. 
- [Perkiraan biaya penetapan sumber daya subkontrak](../subcontracting/costing-subcon-ra.md): Perkiraan biaya proyek akan mempertimbangkan penetapan sumber daya subkontrak dan akan dikenakan biaya menggunakan daftar harga pembelian yang terkait dengan subkontrak. 
- [Konfigurasikan Papan Jadwal untuk menampilkan pekerja kontrak dan kapasitas subkontrak](../subcontracting/configure-sb-subcon.md): Papan jadwal dalam Project Operations sekarang dapat dikonfigurasi untuk mencari dan menyarankan jenis pekerja kontrak sumber daya yang dapat dipesan dan kapasitas subkontrak bersama dengan karyawan. Konfigurasi ini dapat diterapkan bila mencari sumber daya dalam konteks staf untuk persyaratan proyek tertentu atau bila mencari di luar konteks persyaratan proyek.
- [Staf proyek dengan pekerja kontrak dan kapasitas subkontrak](../subcontracting/staffing-cw.md): Pekerja kontrak sekarang dapat dipesan pada proyek yang memanfaatkan pengalaman papan jadwal.
- [Waktu perekaman, pengeluaran, dan penggunaan bahan pada proyek untuk komponen subkontrak:](../subcontracting/recording-subcon-actuals.md) Pekerja kontrak dapat merekam waktu dan pengeluaran, dan anggota tim proyek juga dapat merekam penggunaan bahan yang dibeli menggunakan subkontrak pada proyek. Hal ini akan mengakibatkan perekaman biaya yang akurat pada proyek yang menggunakan kapasitas pembelian atau bahan.
- [Transisi status pada subkontrak](../subcontracting/subcon-states.md): Subkontrak dapat dikonfirmasi untuk menyelesaikan negosiasi dengan vendor, ditutup untuk menunjukkan penyelesaian pengiriman, atau dibatalkan untuk menunjukkan penghentikan kontrak dengan vendor sebelum penyelesaian pengiriman.

### <a name="task-planning"></a>Perencanaan Tugas
- Peningkatan pemecahan masalah untuk administrator sistem. Bila pengguna tidak dapat membuka proyek, administrator dapat meninjau kesalahan terkait non-lisensi yang dihasilkan dari Project for the Web dalam [log penjadwalan Proyek](../../project-management/schedule-api-logs.md).
- [Gunakan daftar tugas di Microsoft Project for the Web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Di Microsoft Project for the Web, Anda dapat menambahkan daftar periksa ke tugas untuk melacak item tertentu.

## <a name="quality-updates"></a>Pembaruan kualitas

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Perencanaan dan Pelacakan | 2392596 | Jadwalkan API sekarang memungkinkan pembaruan untuk bidang **Upaya tersisa**, **Upaya diselesaikan**, dan **% Selesai**. |
| Perencanaan dan Pelacakan | 2478497 | **Jumlah aktivitas** API jadwal dan bidang **ID Tugas** dapat kosong pada input karena sistem akan mengisinya menggunakan penomoran otomatis.|
| Waktu dan Pengeluaran | 2468135 | Jumlah retries persetujuan dikurangi dari lima menjadi tiga. |
| Waktu dan Pengeluaran | 2468188 | Memperbaiki masalah teks log yang melebihi panjang maksimum di atribut **notetext** entitas **anotasi**. |

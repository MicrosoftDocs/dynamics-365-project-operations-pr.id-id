---
title: Apa yang baru Desember 2021 - Project Operations lite deployment
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Desember 2021 penyebaran Project Operations lite.
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
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Apa yang baru Desember 2021 - Project Operations lite deployment

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam Dataverse versi lingkungan 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

### <a name="subcontract-management"></a>Manajemen subkontrak 

- [Mensubkontrakkan anggota](../subcontracting/subcontracting-project-team-members.md) tim proyek: Manajer proyek dapat membuat anggota tim bernama atau generik dengan subkontrak dan subkontrak baris untuk memengaruhi kepegawaian dan estimasi.
- [Opsi subkontrak untuk anggota](../subcontracting/subcon-options.md) tim proyek: Saat membuat pilihan staf untuk anggota tim proyek bernama atau generik, manajer proyek dapat meninjau subkontrak yang ada atau membuat subkontrak baru untuk satu atau beberapa anggota tim proyek. 
- [Estimasi biaya penugasan sumber daya yang disubkontrakkan](../subcontracting/costing-subcon-ra.md): Estimasi biaya proyek akan mempertimbangkan penugasan sumber daya yang disubkontrakkan dan akan membebani mereka menggunakan daftar harga pembelian yang terkait dengan subkontrak. 
- [Konfigurasikan Papan Jadwal untuk menunjukkan pekerja kontrak dan kapasitas](../subcontracting/configure-sb-subcon.md) yang disubkontrakkan: Papan jadwal dalam Operasi Proyek sekarang dapat dikonfigurasi untuk mencari dan menyarankan jenis sumber daya yang dapat dipesan dan kapasitas yang dapat dipesan oleh pekerja kontrak bersama dengan karyawan. Konfigurasi ini dapat diterapkan saat mencari sumber daya dalam konteks kepegawaian untuk persyaratan proyek tertentu atau saat mencari di luar konteks persyaratan proyek.
- [Mengelola proyek dengan pekerja kontrak dan kapasitas](../subcontracting/staffing-cw.md) subkontrak: Pekerja kontrak sekarang dapat dipesan pada proyek yang memanfaatkan pengalaman papan jadwal.
- [Mencatat waktu, pengeluaran, dan penggunaan material pada proyek untuk komponen](../subcontracting/recording-subcon-actuals.md) yang disubkontrakkan: Pekerja kontrak dapat mencatat waktu dan pengeluaran, dan anggota tim proyek juga dapat merekam penggunaan bahan yang dibeli menggunakan subkontrak pada proyek. Ini akan menghasilkan pencatatan biaya yang akurat pada proyek yang menggunakan kapasitas atau bahan yang dibeli.
- [Transisi negara pada subkontrak](../subcontracting/subcon-states.md): Subkontrak dapat dikonfirmasi untuk menyelesaikan negosiasi dengan vendor, ditutup untuk menunjukkan penyelesaian pengiriman, atau dibatalkan untuk menunjukkan pemutusan kontrak dengan vendor sebelum penyelesaian pengiriman.

### <a name="task-planning"></a>Perencanaan Tugas
- Pemecahan masalah yang ditingkatkan untuk administrator sistem. Saat pengguna tidak dapat membuka proyek, administrator dapat meninjau kesalahan terkait non-lisensi yang dihasilkan dari Project untuk web di [log](../../project-management/schedule-api-logs.md) penjadwalan Project.
- [Gunakan daftar periksa tugas di Microsoft Project untuk web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Di Microsoft Project untuk web, Anda dapat menambahkan daftar periksa ke tugas untuk melacak item tertentu.

## <a name="quality-updates"></a>Pembaruan kualitas

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Perencanaan dan Pelacakan | 2392596 | Jadwalkan API sekarang memungkinkan pembaruan pada **bidang Upaya yang** tersisa, **Upaya selesai**, dan **% Lengkap**. |
| Perencanaan dan Pelacakan | 2478497 | Jadwalkan API **Nomor** aktivitas dan **bidang ID** Tugas dapat kosong saat input karena sistem akan mengisinya menggunakan penomoran otomatis.|
| Waktu dan Pengeluaran | 2468135 | Jumlah percobaan ulang persetujuan dikurangi dari lima menjadi tiga. |
| Waktu dan Pengeluaran | 2468188 | Memperbaiki masalah dengan teks log yang melebihi panjang maksimum dalam **atribut notetext** dari **entitas anotasi**. |

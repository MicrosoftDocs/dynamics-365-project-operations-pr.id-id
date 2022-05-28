---
title: Yang baru Desember 2021 - Penyebaran lite Operasi Proyek
description: Topik ini memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Implementasi Project Operations lite desember 2021.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1ff0a14bf6cb445913bcba11f83234826014857
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585382"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Yang baru Desember 2021 - Penyebaran lite Operasi Proyek

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Ini topik berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Proyek dalam Dataverse versi lingkungan 4.27.0.195, 4.27.0.242, 4.27.0.244


## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

### <a name="subcontract-management"></a>Manajemen subkontrak 

- [Anggota tim](../subcontracting/subcontracting-project-team-members.md) proyek subkontrak: Seorang manajer proyek dapat membuat anggota tim bernama atau generik dengan subkontrak dan jalur subkontrak untuk memengaruhi kepegawaian dan estimasi.
- [Opsi subkontrak untuk anggota](../subcontracting/subcon-options.md) tim proyek: Saat membuat pilihan kepegawaian untuk anggota tim proyek bernama atau generik, manajer proyek dapat meninjau subkontrak yang ada atau membuat subkontrak baru untuk satu atau lebih anggota tim proyek. 
- [Estimasi biaya penugasan](../subcontracting/costing-subcon-ra.md) sumber daya subkontrak: Estimasi biaya proyek akan mempertimbangkan penugasan sumber daya subkontrak dan akan dikenakan biaya menggunakan daftar harga pembelian yang terkait dengan subkontrak. 
- [Konfigurasikan Papan Jadwal untuk menunjukkan pekerja kontrak dan kapasitas](../subcontracting/configure-sb-subcon.md) subkontrak: Papan jadwal dalam Operasi Proyek sekarang dapat dikonfigurasi untuk mencari dan menyarankan jenis sumber daya yang dapat dipesan oleh pekerja kontrak dan kapasitas subkontrak bersama dengan karyawan. Konfigurasi ini dapat diterapkan ketika mencari sumber daya dalam konteks kepegawaian untuk persyaratan proyek tertentu atau ketika mencari di luar konteks persyaratan proyek.
- [Kepegawaian proyek dengan pekerja kontrak dan kapasitas](../subcontracting/staffing-cw.md) subkontrak: Pekerja kontrak sekarang dapat dipesan pada proyek-proyek yang memanfaatkan pengalaman papan jadwal.
- [Waktu pencatatan, pengeluaran, dan penggunaan material pada proyek untuk komponen](../subcontracting/recording-subcon-actuals.md) subkontrak: Pekerja kontrak dapat mencatat waktu dan pengeluaran, dan anggota tim proyek juga dapat mencatat penggunaan bahan yang dibeli menggunakan subkontrak pada proyek. Ini akan menghasilkan pencatatan biaya yang akurat pada proyek yang menggunakan kapasitas atau bahan yang dibeli.
- [Transisi negara pada subkontrak](../subcontracting/subcon-states.md): Subkontrak dapat dikonfirmasi untuk menyelesaikan negosiasi dengan vendor, ditutup untuk menunjukkan penyelesaian pengiriman, atau dibatalkan untuk menunjukkan pemutusan kontrak dengan vendor sebelum menyelesaikan pengiriman.

### <a name="task-planning"></a>Perencanaan Tugas
- Pemecahan masalah yang ditingkatkan untuk administrator sistem. Saat pengguna tidak dapat membuka proyek, administrator dapat meninjau kesalahan terkait non-lisensi yang dihasilkan dari Project for the web dalam [log](../../project-management/schedule-api-logs.md) penjadwalan Proyek.
- [Gunakan daftar periksa tugas di Microsoft Project untuk web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Di Microsoft Project untuk web, Anda dapat menambahkan daftar periksa ke tugas untuk melacak item tertentu.

## <a name="quality-updates"></a>Pembaruan kualitas

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Perencanaan dan Pelacakan | 2392596 | API Jadwal sekarang memungkinkan pembaruan pada bidang Upaya yang **tersisa**, **Upaya selesai**, dan **% Lengkap**. |
| Perencanaan dan Pelacakan | 2478497 | Jadwalkan API **Nomor** aktivitas dan **bidang ID** Tugas dapat kosong saat input karena sistem akan mengisinya menggunakan penomoran otomatis.|
| Waktu dan Pengeluaran | 2468135 | Jumlah percobaan ulang persetujuan dikurangi dari lima menjadi tiga. |
| Waktu dan Pengeluaran | 2468188 | Memperbaiki masalah dengan teks log melebihi panjang maksimum dalam **atribut teks** catatan dari **entitas anotasi**. |

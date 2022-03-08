---
title: Apa yang baru Desember 2021 - Operasi Proyek lite penyebaran
description: Ini topik memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Desember 2021 dari penyebaran Lite Operasi Proyek.
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0432e2d4970c352e91cca589987bbdace57c6eaf
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942981"
---
# <a name="whats-new-december-2021---project-operations-lite-deployment"></a>Apa yang baru Desember 2021 - Operasi Proyek lite penyebaran

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Ini topik berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Proyek dalam Dataverse versi lingkungan 4.27.0.195, 4.27.0.242


## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

### <a name="subcontract-management"></a>Manajemen subkontrak 

- [Anggota tim proyek subkontrak:](../subcontracting/subcontracting-project-team-members.md) Seorang manajer proyek dapat membuat anggota tim bernama atau generik dengan subkontrak dan garis subkontrak untuk mempengaruhi kepegawaian dan estimasi.
- [Opsi subkontrak untuk anggota tim](../subcontracting/subcon-options.md) proyek: Saat membuat pilihan kepegawaian untuk anggota tim proyek yang disebutkan namanya atau generik, manajer proyek dapat meninjau subkontrak yang ada atau membuat subkontrak baru untuk satu atau lebih anggota tim proyek. 
- [Estimasi biaya tugas sumber daya](../subcontracting/costing-subcon-ra.md) subkontrak: Estimasi biaya proyek akan mempertimbangkan tugas sumber daya subkontrak dan akan membebani mereka menggunakan daftar harga pembelian yang terkait dengan subkontrak. 
- [Konfigurasikan Papan Jadwal untuk menunjukkan pekerja kontrak dan kapasitas subkontrak:](../subcontracting/configure-sb-subcon.md) Papan jadwal dalam Operasi Proyek sekarang dapat dikonfigurasi untuk mencari dan menyarankan jenis pekerja kontrak dari sumber daya yang dapat dipesan dan kapasitas subkontrak bersama dengan karyawan. Konfigurasi ini dapat diterapkan ketika mencari sumber daya dalam konteks kepegawaian untuk kebutuhan proyek tertentu atau ketika mencari di luar konteks persyaratan proyek.
- [Staf proyek dengan pekerja kontrak dan kapasitas subkontrak:](../subcontracting/staffing-cw.md) Pekerja kontrak sekarang dapat dipesan pada proyek-proyek yang memanfaatkan pengalaman papan jadwal.
- [Mencatat waktu, pengeluaran, dan penggunaan material pada proyek untuk komponen subkontrak:](../subcontracting/recording-subcon-actuals.md) Pekerja kontrak dapat mencatat waktu dan pengeluaran, dan anggota tim proyek juga dapat mencatat penggunaan bahan yang dibeli menggunakan subkontrak pada suatu proyek. Ini akan menghasilkan pencatatan biaya yang akurat pada proyek-proyek yang menggunakan kapasitas atau bahan yang dibeli.
- [Transisi negara pada subkontrak:](../subcontracting/subcon-states.md) Subkontrak dapat dikonfirmasi untuk menyelesaikan negosiasi dengan vendor, ditutup untuk menunjukkan penyelesaian pengiriman, atau dibatalkan untuk menunjukkan pemutusan kontrak dengan vendor sebelum selesai pengiriman.

### <a name="task-planning"></a>Perencanaan Tugas
- Pemecahan masalah yang ditingkatkan untuk administrator sistem. Ketika pengguna tidak dapat membuka proyek, administrator dapat meninjau kesalahan terkait non-lisensi yang dihasilkan dari Project untuk web di [log penjadwalan Proyek](../../project-management/schedule-api-logs.md).
- [Gunakan daftar periksa tugas di Microsoft Project untuk web](https://support.microsoft.com/en-us/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c). Di Microsoft Project untuk web, Anda dapat menambahkan daftar periksa ke tugas untuk melacak item tertentu.

## <a name="quality-updates"></a>Pembaruan kualitas

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Perencanaan dan Pelacakan | 2392596 | Jadwal API sekarang memungkinkan pembaruan untuk **Sisa** Usaha, **Usaha** selesai, dan % Bidang **lengkap**. |
| Perencanaan dan Pelacakan | 2478497 | Jadwalkan nomor aktivitas API **dan bidang ID Tugas dapat di kosong pada input karena sistem akan** **mengisinya** menggunakan penomodanan otomatis.|
| Waktu dan Pengeluaran | 2468135 | Jumlah retries persetujuan dikurangi dari lima menjadi tiga. |
| Waktu dan Pengeluaran | 2468188 | Memperbaiki masalah dengan teks log melebihi panjang maksimum dalam **atribut notetext** dari entitas **anotasi.** |

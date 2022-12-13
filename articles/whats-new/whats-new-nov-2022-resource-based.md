---
title: Yang baru di bulan November 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Dynamics 365 Project Operations Microsoft November 2022 untuk skenario berbasis sumber daya/tidak ditebar.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831133"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan November 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.58.0.119
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Penagihan dan Harga | 2781818 | Kunci tidak menemukan kesalahan saat menetapkan harga default untuk log penggunaan material. |
| Penagihan dan Harga | 2922373 | Tidak dapat menautkan baris kutipan ke proyek yang telah ditutup sebagai kutipan yang hilang. |
| Penagihan dan Harga | 2943206 | **Bidang Garis** Kontrak di Entitas Proyek Harus Opsional. |
| Penagihan dan Harga | 2953182 | Perbaiki pesan kesalahan untuk faktur koreksi.|
| Penagihan dan Harga | 2959500 | Tidak dapat menautkan baris kutipan ke tugas proyek yang sudah dikaitkan dengan kutipan yang hilang.|
| Penagihan dan Harga | 2959560 | Pesan "Pelanggan ini sudah ada dalam Kontrak Proyek" yang diterima saat menutup penawaran seperti yang dimenangkan di lokal tertentu. |
| Penagihan dan Harga | 3031727 | Penugasan sumber daya gagal dengan kesalahan Bidang yang diperlukan 'msdyn_Company' hilang. |
| Penagihan dan Harga | 3036905 | Perusahaan Pemilik tidak pernah diinisialisasi di ProjectTeamMember. |
| Manajemen peluang | 2763519 | Kesalahan Referensi Null di EnsureProjectContractAllowsUpdates. |
| Manajemen peluang | 2783798 | Saat mengimpor perkiraan proyek pada baris kutipan, deskripsi tugas tidak ada untuk perkiraan biaya dan material.|
| Manajemen peluang | 2988635 | Tingkatkan deskripsi msg kesalahan saat menghapus Customer on Quote. |
| Manajemen peluang | 3001191 | Tidak dapat membuat kutipan dari Peluang di mana metode penagihan ditentukan sebagai null. |
| Peningkatan | 3012324 | Konversi proyek gagal pada project dengan karakter kontrol seperti Tab dalam namanya. || Perencanaan dan Pelacakan Proyek | 2790384 | Batas waktu Operating Set yang Tertunda terlalu singkat. |
| Perencanaan dan Pelacakan Proyek | 3044275 | Pelokalan yang hilang untuk: missingProjectSchedulerErrorMessage. |
| Perencanaan dan Pelacakan Proyek | 3044277 | Kisi Project Recon tidak dimuat saat penjadwal tidak disetel.|
| Manajemen sumber daya | 2943153 | Perbarui tab Pelacakan untuk memperlihatkan dua tempat desimal untuk Durasi.|
| Membuat subkontrak | 2932774 | Vendor Invoice Line Read Only melempar kesalahan dengan tidak benar. |
| Membuat subkontrak | 2939556 | Status Header Faktur Vendor tidak boleh diatur ke Draf penghapusan online jika tidak aktif. |
| Waktu dan Pengeluaran | 2939998 | Ambil versi TESA baru di ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services, dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).

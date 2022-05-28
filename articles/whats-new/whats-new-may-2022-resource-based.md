---
title: Yang baru di Mei 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Ini topik memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Microsoft Dynamics 365 Project Operations Mei 2022 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710141"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di Mei 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Ini topik berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Proyek dalam Dataverse versi lingkungan 4.42.0.70
- Manajemen proyek dan akuntansi dalam lingkungan Dynamics 365 Finance versi 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel di luar kotak, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti petunjuk di kolom Tabel hilang di [bagian peta di bagian peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Tulis ganda.

## <a name="quality-updates"></a>Pembaruan kualitas
### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen sumber daya | 2634019 | Pesan kesalahan yang ditingkatkan untuk validasi bisnis saat menambahkan anggota tim generik sebagai sumber daya. |
| Perencanaan dan pelacakan proyek | 2648515 | Pembaruan terbatas **ownerid**, **status**, dan **status** dalam entitas penjadwalan. |
| Penagihan dan harga | 2653167 | Pemisah **desimal kisi Perkiraan** harus mengikuti pengaturan format di **Opsi Pribadi**. |
| Penagihan dan harga| 2662251 | Nilai di **bidang unit** dan **grup** Unit yang dikoreksi default saat membuat rekaman dalam estimasi material. |
| Penagihan dan harga| 2571408 | Aktual penjualan yang tidak ditagih dicap dengan ID faktur proforma saat membuat draf faktur. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

Untuk informasi tentang perbaikan bug yang disertakan dalam pembaruan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

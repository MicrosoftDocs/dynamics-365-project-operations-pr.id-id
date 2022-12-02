---
title: Yang baru di Mei 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di perilisan Microsoft Dynamics 365 Project Operations pada Mei 2022 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921398"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di Mei 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.42.0.70
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas
### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Manajemen sumber daya | 2634019 | Pesan kesalahan yang disempurnakan untuk validasi bisnis saat menambahkan anggota tim generik sebagai sumber daya. |
| Perencanaan dan pelacakan proyek | 2648515 | Membatasi Pembaruan **ownerid**, **status**, dan **status** dalam penjadwalan entitas. |
| Penagihan dan harga | 2653167 | Pemisah desimal kisi **estimasi** harus mengikuti pengaturan format di **Opsi Pribadi**. |
| Penagihan dan harga| 2662251 | Nilai dalam bidang **Unit koreksi** dan **grup Unit** di-default ketika membuat rekaman dalam estimasi bahan. |
| Penagihan dan harga| 2571408 | Aktual penjualan belum tertagih dicap dengan ID faktur proforma saat membuat draf faktur. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

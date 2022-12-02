---
title: Yang baru di bulan Agustus 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di perilisan Microsoft Dynamics 365 Project Operations pada Agustus 2022 untuk skenario berbasis sumber daya/non-stok.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403860"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Agustus 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.45.0.53
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
|   Manajemen peluang | 2762089 | Penanganan kesalahan saat menutup kontrak sebagai kalah jika penyimpanan otomatis dinonaktifkan di organisasi.|
|Perencanaan dan Pelacakan Proyek | 2767841 | Telemetri memperbarui skenario Buat atau Perbarui entitas Proyek.|
|Penagihan dan Harga | 2771072 | Penanganan pengecualian referensi null saat memenangkan kuotasi.|
|Penagihan dan Harga | 2844181 |Kegagalan dalam mendapatkan id korelasi dan memblokir pembuatan faktur.|
|Penagihan dan Harga | 2852836 | Aktual antarkompilasi tidak ditemukan untuk Pengeluaran Antarkompilasi yang dibuat dan disetujui pada CE.|


### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

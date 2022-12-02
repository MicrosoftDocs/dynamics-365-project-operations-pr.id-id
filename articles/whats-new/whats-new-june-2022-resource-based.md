---
title: Yang baru di bulan Juni 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di perilisan Microsoft Dynamics 365 Project Operations pada Juni 2022 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031335"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Juni 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations di lingkungan Dataverse versi 4.43.0.77 or 4.43.0.119
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tabel berikut menampilkan peta penulisan ganda yang telah dimodifikasi atau ditambahkan dalam rilis Project Operations Juni 2022.

| Peta entitas | Pembaruan versi | Komentar |
| --- | --- | --- |
| Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Tidak lagi menggunakan bidang lama dan dipetakan ke bidang baru untuk pelacakan status faktur vendor. |

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Membuat subkontrak | 2708885 | Memperbaiki pesan kesalahan yang muncul saat pengguna membuat rekaman header pemesanan sumber daya yang dapat dipesan dengan sumber daya yang tidak dapat dipesan. |
| Perencanaan dan pelacakan proyek | 2629441 | Mengoreksi logika pemicu alur kerja untuk membantu mencegah perulangan tak terbatas saat tugas proyek diperbarui. |
| Waktu dan pengeluaran | 2641209 | Impor entri waktu dari penetapan/pemesanan harus mempertahankan referensi sumber daya yang dapat dipesan. |
| Perencanaan dan pelacakan proyek | 2651148 | Header dokumen proyek harus dilindungi.|
| Perencanaan dan pelacakan proyek | 2653145 | Validasi yang ditambahkan untuk memastikan bahwa rekaman proyek tidak dapat dibuat yang memiliki karakter yang tidak valid atas namanya. |
| Waktu dan pengeluaran | 2654710 | Mengoreksi pemfilteran pada halaman **Persetujuan**. |
| Penagihan dan harga | 2667805 | Menambahkan Validasi untuk membantu mencegah aktual penjualan yang ditagih dibuat jika aktual penjualan belum ditagih pendukung tidak ada. |
| Penagihan dan harga | 2668378 | Menambahkan Validasi untuk membantu mencegah dimensi harga kustom tidak ditambahkan, kecuali jika nama logis dan nama bidang diisi. |
| Membuat subkontrak | 2677485 | Memperbarui versi target peta penulisan ganda baris faktur vendor. |
| Waktu dan pengeluaran | 2700428 | Meningkatkan logika persetujuan untuk memastikan bahwa set persetujuan lain untuk proyek dapat diproses meskipun salah satu dari set persetujuan terjebak dalam pekerjaan sistem. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

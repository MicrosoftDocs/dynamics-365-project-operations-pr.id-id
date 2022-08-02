---
title: Yang baru di bulan Juni 2022 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Juni 2022 Microsoft Dynamics 365 Project Operations untuk skenario berbasis sumber daya/non-stok.
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

- Operasi Proyek dalam Dataverse versi lingkungan 4.43.0.77 atau 4.43.0.119
- Manajemen dan akuntansi proyek dalam lingkungan Dynamics 365 Finance versi 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tabel berikut menunjukkan peta tulis ganda yang telah dimodifikasi atau ditambahkan dalam rilis Operasi Proyek Juni 2022.

| Peta entitas | Pembaruan versi | Komentar |
| --- | --- | --- |
| Entitas ekspor faktur vendor proyek integrasi Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Menghentikan bidang lama dan memetakan ke bidang baru untuk pelacakan status faktur vendor. |

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel out-of-box, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti instruksi di [bagian Kolom tabel hilang di](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) peta bagian Panduan pemecahan masalah penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Subkontrak | 2708885 | Memperbaiki pesan kesalahan yang muncul saat pengguna membuat catatan header pemesanan sumber daya yang dapat dipesan di mana tidak ada sumber daya yang dapat dipesan yang diisi. |
| Perencanaan dan pelacakan proyek | 2629441 | Mengoreksi logika pemicu alur kerja untuk membantu mencegah loop tak terbatas saat tugas proyek diperbarui. |
| Waktu dan pengeluaran | 2641209 | Impor entri waktu dari penugasan/pemesanan harus menyimpan referensi sumber daya yang dapat dipesan. |
| Perencanaan dan pelacakan proyek | 2651148 | Header dokumen proyek harus dijaga.|
| Perencanaan dan pelacakan proyek | 2653145 | Menambahkan validasi untuk memastikan bahwa rekaman proyek tidak dapat dibuat yang memiliki karakter yang tidak valid dalam namanya. |
| Waktu dan pengeluaran | 2654710 | Mengoreksi pemfilteran pada **halaman Persetujuan**. |
| Penagihan dan harga | 2667805 | Menambahkan validasi untuk membantu mencegah aktual penjualan yang ditagih dibuat jika mendukung aktual penjualan yang tidak ditagih tidak ada. |
| Penagihan dan harga | 2668378 | Menambahkan validasi untuk membantu mencegah dimensi harga kustom ditambahkan kecuali nama logis dan nama bidang diisi. |
| Subkontrak | 2677485 | Memperbarui versi target dari baris faktur vendor peta tulis ganda. |
| Waktu dan pengeluaran | 2700428 | Meningkatkan logika persetujuan untuk memastikan bahwa set persetujuan lain untuk proyek dapat diproses bahkan jika salah satu set persetujuan terjebak dalam pekerjaan sistem. |

### <a name="project-management-and-accounting-in-finance"></a>Manajemen proyek dan akuntansi di bidang Keuangan

Untuk informasi tentang perbaikan bug yang disertakan dalam pembaruan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).

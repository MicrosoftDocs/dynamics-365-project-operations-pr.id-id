---
title: Yang baru di April 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis April 2022 Microsoft Dynamics 365 Project Operations untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912382"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di April 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam Dataverse versi lingkungan 4.41.0.45
- Manajemen proyek dan akuntansi dalam lingkungan Dynamics 365 Finance versi 10.0.26

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Kategori pengadaan dapat digunakan dalam pesanan pembelian proyek dan faktur vendor yang tertunda. Untuk informasi selengkapnya, lihat [Menggunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tabel berikut menunjukkan peta tulis ganda yang telah dimodifikasi atau ditambahkan dalam rilis Operasi Proyek maret 2022.

| Peta entitas | Pembaruan versi | Komentar |
| -------------- | ------------------- | ------------|
| Proyek Operasi integrasi proyek vendor baris faktur baris ekspor entitas msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Peta ini mendukung penggunaan kategori pengadaan dengan pesanan pembelian dan faktur vendor yang tertunda. |

Selalu jalankan versi terbaru peta di lingkungan Anda, dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Operasi Dataverse Proyek dan versi solusi Keuangan. Beberapa fitur dan kemampuan mungkin tidak berfungsi dengan benar jika versi terbaru peta tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah mengkustomisasi peta tabel out-of-box, terapkan kembali perubahan tersebut. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda mengalami masalah saat memulai peta, ikuti instruksi di [bagian Kolom tabel hilang di](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) peta bagian Panduan pemecahan masalah penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| ------------ | ---------------- | -------------- |
| Waktu dan pengeluaran | 2573900 | Fitur **Persetujuan** Modern harus diaktifkan secara default. |
| Penagihan dan harga | 2603313 | Memperbaiki kesalahan catatan duplikat yang mencegah kutipan dan baris kontrak yang memiliki produk ditambahkan. |
| Penyebaran dan konfigurasi | 2611368 | Pelanggan harus dapat menambahkan hingga lima entitas kustom ke solusi dengan menggunakan perancang aplikasi modern. |
| Waktu dan pengeluaran | 2628285 | Memperbaiki masalah yang memengaruhi kemampuan untuk mengatur kategori sumber daya yang benar selama impor entri waktu. |
|   Manajemen peluang| 2628815 | Perbarui batas karakter deskripsi detail baris kutipan agar sesuai dengan batas karakter subjek tugas, sehingga impor berhasil untuk tugas di mana subjek lebih panjang dari 100 karakter. |
| Waktu dan pengeluaran| 2629547 | Bidang **persetujuan proyek yang Dikirim Oleh** harus mengarah ke pengguna yang mengirimkan rekaman. |
| Waktu dan pengeluaran| 2629865 | Bidang **Salin kategori** pada tugas saat proyek disalin. |
| Waktu dan pengeluaran| 2636463 | Memperbaiki filter pada persetujuan dalam formulir persetujuan modern. |
| Perencanaan dan pelacakan proyek | 2648300 | Memperbaiki masalah yang mencegah pemilik proyek diubah. |
| Penagihan dan harga | 2563000 | Baris jurnal untuk penjualan yang tidak ditagih di mana mata uang berbeda dari mata uang kontrak tidak boleh diizinkan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

Untuk informasi tentang perbaikan bug yang disertakan dalam pembaruan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

---
title: Yang baru di April 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia di perilisan Microsoft Dynamics 365 Project Operations pada April 2022 untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110888"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di April 2022 - Project Operations untuk skenario berbasis sumber daya/tanpa stok

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Project Operations dalam lingkungan Dataverse versi 4.41.0.45
- Manajemen proyek dan akuntansi di lingkungan aplikasi Dynamics 365 Finance versi 10.0.26

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Kategori pengadaan dapat digunakan dalam pesanan pembelian proyek dan faktur vendor tertunda. Untuk informasi lebih lanjut, lihat [Gunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor tertunda](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tabel berikut menampilkan peta penulisan ganda yang telah dimodifikasi atau ditambahkan perilisan Project Operations pada Maret 2022.

| Peta entitas | Pembaruan versi | Komentar |
| -------------- | ------------------- | ------------|
| Entitas ekspor baris faktur vendor proyek integrasi Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Peta ini mendukung penggunaan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor tertunda. |

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Beberapa fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta dalam kolom **Versi** pada halaman **Penulisan ganda**. Untuk mengaktifkan versi baru peta, pilih versi **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat Anda memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) dari panduan pemecahan masalah Penulisan ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| ------------ | ---------------- | -------------- |
| Waktu dan pengeluaran | 2573900 | Fitur **Persetujuan Modern** harus diaktifkan secara default. |
| Penagihan dan harga | 2603313 | Memperbaiki kesalahan rekaman duplikat yang mencegah ditambahkannya baris kuotasi dan kontrak yang memiliki produk. |
| Penyebaran dan Konfigurasi | 2611368 | Pelanggan harus dapat menambahkan hingga lima entitas kustom ke solusi dengan menggunakan desainer aplikasi modern. |
| Waktu dan pengeluaran | 2628285 | Memperbaiki masalah yang memengaruhi kemampuan untuk mengatur kategori sumber daya yang benar selama impor entri waktu. |
|   Manajemen peluang| 2628815 | Perbarui batas karakter deskripsi detail baris kuotasi agar sesuai dengan batas karakter subjek tugas, sehingga impor berhasil untuk tugas yang subjeknya lebih dari 100 karakter. |
| Waktu dan pengeluaran| 2629547 | Bidang **diajukan Oleh** dari persetujuan proyek harus mengarahkan ke pengguna yang mengajukan rekaman. |
| Waktu dan pengeluaran| 2629865 | Bidang **Salin kategori** pada tugas saat proyek disalin. |
| Waktu dan pengeluaran| 2636463 | Memperbaiki filter saat persetujuan dalam formulir persetujuan modern. |
| Perencanaan dan pelacakan proyek | 2648300 | Memperbaiki masalah yang mencegah pemilik proyek diubah. |
| Penagihan dan harga | 2563000 | Baris jurnal untuk penjualan belum tertagih dengan mata uang yang berbeda dari mata uang kontrak tidak boleh dibolehkan. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

Untuk informasi tentang perbaikan bug yang termasuk dalam peningkatan ini, masuk ke Microsoft Dynamics Lifecycle Services (LCS), dan lihat [artikel KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).

---
title: Yang baru di bulan September 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis September 2021 Operasi Proyek untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c7f764b3e8ee3775167ee57b4f034e383899aea3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923376"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan September 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Artikel ini berlaku untuk komponen dan versi berikut Dynamics 365 Project Operations:

   - Project Operations dalam lingkungan Microsoft Dataverse versi 4.14.0.99.
   - Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini. Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta pada halaman **Penulisan ganda** pada kolom **Versi**. Untuk mengaktifkan versi baru peta, pilih versi  **peta tabel**, pilih versi terbaru, lalu simpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel yang tidak ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) pada panduan pemecahan masalah Penulisan Ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Waktu dan pengeluaran | 1811407 | Peran keamanan Pemberi Persetujuan Proyek untuk persetujuan entri pengeluaran. |
| Waktu dan pengeluaran | 1811438 | Peran keamanan Pemberi Persetujuan Proyek untuk pembatalan persetujuan entri waktu. |
| Waktu dan pengeluaran | 2370126 | Memperbarui ikon **Tugas Proyek** dan **Peran** di entitas **Entri Waktu**. |
| Waktu dan pengeluaran | 2379879 | Mengoreksi fungsi **Salin Pekan** dalam entri waktu saat menggunakan Dynamics 365 untuk ponsel. |
| Penagihan dan Harga | 2371906 | Jumlah total faktur Proforma tidak boleh disesuaikan di Project Operations untuk penyebaran berbasis sumber daya. |
| Penagihan dan Harga | 2385802 | Memperbaiki kesalahan yang terjadi dengan jam aktual negatif saat total proyek di-refresh. |
| Penagihan dan Harga | 2389675 | Memperbaiki perilaku konfirmasi faktur proforma. Entitas pekerjaan yang berjalan lama harus mempertimbangkan aktivitas yang diperlukan untuk menulis hasil konfirmasi akuntansi. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Perjalanan dan Pengeluaran | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Jumlah transaksi vendor dan pajak penjualan yang diposting dari pengeluaran yang dibuat dari transaksi kartu kredit salah. |
| Perjalanan dan Pengeluaran | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Baris penyelesaian yang salah dibuat saat jurnal pembayaran dibuat. |
| Perjalanan dan Pengeluaran | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Jumlah transaksi pajak penjualan yang diposting dari pengeluaran yang dibuat dari transaksi kartu kredit salah. |
| Perjalanan dan Pengeluaran | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Menghapus baris pengeluaran mungkin membutuhkan waktu lama. |
| Akuntansi proyek | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Setelah Anda menerapkan 4619395 KB, mengubah urutan angka ke **Kontinu** tidak didukung dan bila Anda memposting perkiraan, kesalahan berikut terjadi, "Sistem tidak mendukung konfigurasi 'kontinu' urutan nomor Proj_X." |
| Akuntansi proyek | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Posting faktur vendor mungkin gagal dengan pesan kesalahan berikut, "Transaksi pada voucher tidak seimbang sesuai dengan 17/5/2021. (mata uang akuntansi: 0,00 - mata uang pelaporan: 0,01)." |

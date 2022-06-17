---
title: Yang baru di bulan Agustus 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Agustus 2021 Operasi Proyek untuk skenario berbasis sumber daya/non-stok.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912290"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Yang baru di bulan Agustus 2021 - Project Operations untuk skenario berbasis sumber daya/non-stok

*Berlaku untuk: Project Operations untuk skenario berbasis sumber daya/tanpa stok*

Artikel ini berlaku untuk komponen dan versi berikut Dynamics 365 Project Operations:

   - Project Operations dalam lingkungan Microsoft Dataverse versi 4.13.0.152.
   - Manajemen proyek dan akuntansi di lingkungan Dynamics 365 Finance versi 10.0.20.

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- **Rangkaian Persetujuan**: Persetujuan mengatur waktu grup, pengeluaran, atau permintaan persetujuan penggunaan materi bersama-sama ke subset operasi yang lebih kecil. Pengelompokan ini memungkinkan persetujuan untuk diproses menurut proyek, dalam urutan tertentu, dan memungkinkan untuk mencoba ulang dan mengurutkan. Mengelompokkan permintaan akan meningkatkan keandalan dan keterlacakan pemrosesan persetujuan untuk volume persetujuan yang besar. Untuk informasi lebih lanjut lihat [rangkaian persetujuan](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Pembaruan peta Penulisan Ganda Project Operations

Tidak ada pembaruan untuk peta penulisan ganda Project Operations di rilis ini.

Untuk daftar dan versi peta penulisan ganda Project Operations saat ini, lihat [versi peta penulisan ganda Project Operations](../environment/resource-dual-write-maps.md).

Selalu jalankan versi terbaru peta di lingkungan Anda dan aktifkan semua peta tabel terkait saat Anda memperbarui solusi Project Operations Dataverse dan versi solusi Finance. Fitur dan kemampuan tertentu mungkin tidak berfungsi dengan benar jika versi peta terbaru tidak diaktifkan. Anda dapat melihat versi aktif peta pada halaman **Penulisan ganda** pada kolom **Versi**. Aktifkan versi baru peta dengan memilih **versi peta Tabel**, memilih versi terbaru, lalu menyimpan versi yang dipilih. Jika Anda telah menyesuaikan peta tabel siap pakai, aplikasikan ulang perubahan. Untuk informasi lebih lanjut, lihat [manajemen siklus hidup aplikasi](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jika Anda menemui masalah saat memulai peta, ikuti petunjuk dalam bagian [masalah kolom tabel Yang Tidak Ada pada peta](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) di panduan pemecahan masalah Penulisan Ganda.

## <a name="quality-updates"></a>Pembaruan kualitas

### <a name="project-operations-on-dataverse"></a>Project Operations di Dataverse

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan harga | 2295625 | Nama tahapan harus disalin dari jadwal faktur ke detail baris faktur. |
| Penagihan dan harga | 2316323 | Diskon tidak boleh diedit pada faktur proforma dalam Project Operations untuk skenario berbasis sumber daya. |
|   Manajemen peluang | 2338619 | Aturan bisnis **Peluang** dan **Kuotasi** harus diaktifkan hanya pada halaman. |
| Manajemen sumber daya | 2316523 | Menggunakan **Kirim Permintaan** dari persyaratan sumber daya yang memiliki peran yang dilampirkan tidak boleh menampilkan kesalahan. |
| Manajemen sumber daya | 2326885 | Membuat persyaratan sumber daya melalui proyek tidak boleh menampilkan kesalahan. |
| Waktu dan pengeluaran | 2335584 | Alur tugas yang tidak digunakan lagi pada entri waktu. |
| Waktu dan pengeluaran | 2336884 | Tombol entri waktu **Salin Pekan** harus berfungsi untuk lebih dari hanya pengguna saat ini. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Manajemen proyek dan akuntansi di Dynamics 365 Finance

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Perjalanan dan Pengeluaran | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Jumlah transaksi vendor dan pajak penjualan yang salah diposting ketika pengeluaran dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Penyelesaian yang salah adalah baris yang dibuat saat jurnal pembayaran dibuat. |
| Perjalanan dan Pengeluaran | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Jumlah transaksi pajak penjualan yang salah diposting ketika pengeluaran dibuat dari transaksi kartu kredit. |
| Perjalanan dan Pengeluaran | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Menghapus baris pengeluaran mungkin membutuhkan waktu lama. |
| Akuntansi proyek | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistem tidak mendukung konfigurasi deret nomor kontinu saat Anda memposting perkiraan setelah menerapkan KB 4619395. |
| Akuntansi proyek | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Posting faktur vendor mungkin gagal dengan pesan kesalahan, "Transaksi pada voucher tidak seimbang sebagaimana per 17/5/2021. (mata uang akuntansi: 0,00 - mata uang pelaporan: 0,01)" |

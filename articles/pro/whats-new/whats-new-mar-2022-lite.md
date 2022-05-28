---
title: Apa yang baru Maret 2022 - penyebaperan Project Operations lite
description: Topik ini memberikan informasi tentang pembaruan kualitas yang tersedia dalam rilis Penyebaran Project Operations lite maret 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583754"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Apa yang baru Maret 2022 - penyebaperan Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Ini topik berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut:

- Operasi Proyek dalam Dataverse versi lingkungan 4.30.0.99

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

- Subkontrak: Pembuatan faktur vendor dan pengalaman pencocokan

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Waktu dan pengeluaran | 2388011 | Tampilkan komentar penolakan kepada pengirim entri waktu selama persetujuan massal. |
| Perencanaan dan pelacakan proyek | 2495294 | Detail proyek tidak boleh diedit di **halaman Detail** tugas. |
| Penagihan dan harga | 2499605 | Tonggak kontrak yang dibuat dari tonggak kutipan salah ditandai sebagai baca-saja. |
| Perencanaan dan pelacakan proyek | 2506050 | Set operasi tetap tertunda selama satu jam jika tidak ada perubahan untuk disimpan. Set kemudian salah ditandai sebagai **Gagal**, sedangkan itu harus segera diselesaikan. |
| Penagihan dan harga | 2507401 | Unit kontrak default salah dimasukkan pada proyek karena caching yang salah. |
| Penagihan dan harga | 2541660 | **Validasi** Pembuatan Pesanan Penjualan dalam penulisan ganda harus hanya untuk pesanan berbasis proyek. |
| Penagihan dan harga | 2552745 | Pajak tidak dibagi antara pelanggan yang telah menyiapkan aturan penagihan terpisah. |
| Penagihan dan harga | 2558859 | Pesan kesalahan yang ditingkatkan saat dimensi harga disiapkan. |
| Penagihan dan harga | 2558933 | **Impor dari Estimasi** Proyek gagal saat **proyek MSDYN\_** ditambahkan sebagai dimensi harga. |
| Penagihan dan harga | 2559101 | Penghapusan parameter proyek tidak diblokir dan menyebabkan masalah. |
|   Manajemen peluang | 2570390 | Plug-in dual-write memaksa jenis akun pada kutipan, pesanan, dan peluang untuk menjadi **Pelanggan**, bahkan ketika jenis akun itu tidak benar. |
| Penagihan dan harga | 2586097 | Split billed cost actuals tidak dibalik ketika sebuah proyek dihapus dari garis kontrak proyek. |
| Penagihan dan harga | 2589619 | Pajak atas materi penulisan disebarkan ke aktual penjualan dan faktur yang tidak ditagih. |
|   Manajemen peluang | 2594015 | Kutipan tidak dapat ditutup sebagai won untuk pelanggan yang memiliki **persyaratan pembayaran Net60**. |
| Perencanaan dan pelacakan proyek | 2595841 | Di Project for the Web, pengguna menerima pesan kesalahan tentang msdyn **actualstart\_ yang hilang** saat mereka membuat permintaan sumber daya baru. |
| Waktu dan Pengeluaran | 2602511 | Bidang **ditolak oleh** untuk entri waktu menunjukkan **Sistem**, bukan pengguna bernama sebagai penolak. |
| Waktu dan Pengeluaran | 2602528 | Pemberi persetujuan proyek dapat menyetujui waktu pada proyek di mana mereka tidak terdaftar sebagai pemberi persetujuan. |
| Penagihan dan harga | 2608550 | Faktur koreksi dapat dikonfirmasi meskipun tidak ada perubahan pada aslinya. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

Fitur [Yang dihapus atau tidak digunakan lagi di Operasi](../../whats-new/removed-depreciated-features-project.md) Proyek topik menjelaskan fitur yang telah dihapus atau tidak digunakan lagi untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan mungkin akan dihapus dalam pembaruan mendatang.

Pengumuman penghentian akan muncul di [fitur Yang dihapus atau tidak digunakan lagi di Operasi](../../whats-new/removed-depreciated-features-project.md) Proyek topik 12 bulan sebelum fitur apa pun dihapus dari produk.

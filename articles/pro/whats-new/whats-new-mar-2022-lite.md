---
title: Apa yang baru Maret 2022 - penyebaperan Project Operations lite
description: Artikel ini menyediakan informasi tentang pembaruan kualitas yang tersedia dalam rilis Maret 2022 penyebaran Project Operations lite.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934232"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Apa yang baru Maret 2022 - penyebaperan Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Artikel ini berlaku untuk komponen dan versi Microsoft Dynamics 365 Project Operations berikut ini:

- Operasi Proyek dalam Dataverse versi lingkungan 4.30.0.99

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

- Subkontrak: Pembuatan faktur vendor dan pengalaman pencocokan

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Waktu dan pengeluaran | 2388011 | Tampilkan komentar penolakan kepada pengirim entri waktu selama persetujuan massal. |
| Perencanaan dan pelacakan proyek | 2495294 | Detail proyek tidak boleh dapat diedit di **halaman Detail** tugas. |
| Penagihan dan harga | 2499605 | Tonggak kontrak yang dibuat dari tonggak kutipan salah ditandai sebagai baca-saja. |
| Perencanaan dan pelacakan proyek | 2506050 | Set operasi tetap tertunda selama satu jam jika tidak ada perubahan untuk disimpan. Set kemudian ditandai secara salah sebagai **Gagal**, sedangkan itu harus segera diselesaikan. |
| Penagihan dan harga | 2507401 | Unit kontrak default salah dimasukkan pada proyek karena caching yang salah. |
| Penagihan dan harga | 2541660 | **Validasi** Pembuatan Pesanan Penjualan dalam penulisan ganda harus hanya untuk pesanan berbasis proyek. |
| Penagihan dan harga | 2552745 | Pajak tidak dibagi antara pelanggan yang telah menyiapkan aturan penagihan terpisah. |
| Penagihan dan harga | 2558859 | Pesan kesalahan yang ditingkatkan saat dimensi harga disiapkan. |
| Penagihan dan harga | 2558933 | **Impor dari Perkiraan** Proyek gagal ketika **proyek\_ msdyn** ditambahkan sebagai dimensi harga. |
| Penagihan dan harga | 2559101 | Penghapusan parameter proyek tidak diblokir dan menyebabkan masalah. |
|   Manajemen peluang | 2570390 | Plug-in tulis ganda memaksa jenis akun pada kutipan, pesanan, dan peluang untuk menjadi **Pelanggan**, bahkan ketika jenis akun itu tidak benar. |
| Penagihan dan harga | 2586097 | Biaya aktual yang ditagih terpisah tidak dibalik ketika proyek dihapus dari jalur kontrak proyek. |
| Penagihan dan harga | 2589619 | Pajak atas materi write-in disebarkan ke aktual penjualan yang tidak ditagih dan faktur. |
|   Manajemen peluang | 2594015 | Kutipan tidak dapat ditutup sebagai won untuk pelanggan yang memiliki **ketentuan pembayaran Net60**. |
| Perencanaan dan pelacakan proyek | 2595841 | Di Project for the Web, pengguna menerima pesan galat tentang msdyn **actualstart\_ yang hilang** saat mereka membuat permintaan sumber daya baru. |
| Waktu dan Pengeluaran | 2602511 | Bidang **Ditolak oleh** untuk entri waktu memperlihatkan **Sistem** alih-alih pengguna bernama sebagai penolak. |
| Waktu dan Pengeluaran | 2602528 | Pemberi persetujuan proyek dapat menyetujui waktu pada proyek yang tidak tercantum sebagai pemberi persetujuan. |
| Penagihan dan harga | 2608550 | Faktur koreksi dapat dikonfirmasi bahkan jika tidak ada perubahan pada aslinya. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

Artikel Fitur [yang dihapus atau tidak digunakan lagi dalam Operasi](../../whats-new/removed-depreciated-features-project.md) Proyek menjelaskan fitur yang telah dihapus atau tidak digunakan lagi untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan mungkin akan dihapus di pembaruan mendatang.

Pengumuman penghentian akan muncul di [artikel Fitur yang dihapus atau tidak digunakan lagi di Operasi](../../whats-new/removed-depreciated-features-project.md) Proyek 12 bulan sebelum fitur apa pun dihapus dari produk.

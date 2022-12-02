---
title: Apa yang baru Maret 2022 - penyebaperan Project Operations lite
description: Artikel ini memberikan informasi tentang pembaruan kualitas yang tersedia pada rilis Maret 2022 penyebaran Project Operations Lite.
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

- Project Operations dalam lingkungan Dataverse versi 4.30.0.99

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

- Subkontrak: Pembuatan faktur vendor dan pengalaman yang cocok

## <a name="quality-updates"></a>Pembaruan kualitas

| Area fitur | Nomor Referensi | Pembaruan kualitas |
| --- | --- | --- |
| Waktu dan pengeluaran | 2388011 | Tampilkan komentar penolakan untuk pemohon entri waktu selama persetujuan massal. |
| Perencanaan dan pelacakan proyek | 2495294 | Rincian proyek tidak boleh diedit pada halaman **rincian Tugas**. |
| Penagihan dan harga | 2499605 | Tahapan kontrak yang dibuat dari tahapan kuotasi tidak ditandai dengan benar sebagai hanya baca. |
| Perencanaan dan pelacakan proyek | 2506050 | Rangkaian operasi tetap tertunda selama satu jam jika tidak ada perubahan untuk disimpan. Rangkaian kemudian salah ditandai sebagai **Gagal**, padahal harus segera diselesaikan. |
| Penagihan dan harga | 2507401 | Unit kontrak default tidak dimasukkan dengan benar di proyek penembolokan yang salah. |
| Penagihan dan harga | 2541660 | **Validasi Pembuatan Pesanan Penjualan** di penulisan ganda harus hanya untuk pesanan berbasis proyek. |
| Penagihan dan harga | 2552745 | Pajak tidak dipecah antara pelanggan yang telah menyiapkan aturan penagihan terpisah. |
| Penagihan dan harga | 2558859 | memperbaiki pesan kesalahan saat dimensi harga disiapkan. |
| Penagihan dan harga | 2558933 | **Impor dari Estimasi Proyek** gagal saat **msdyn\_project** ditambahkan sebagai dimensi harga. |
| Penagihan dan harga | 2559101 | Penghapusan parameter proyek tidak diblokir dan menyebabkan masalah. |
|   Manajemen peluang | 2570390 | Plug-in penulisan ganda akan mendukung jenis akun pada kuotasi, pesanan, dan peluang sebagai **Pelanggan**, Meskipun jenis akun tersebut tidak benar. |
| Penagihan dan harga | 2586097 | Aktual biaya terbagi tidak dibalik saat proyek dihapus dari baris kontrak proyek. |
| Penagihan dan harga | 2589619 | Pajak bahan pilihan disebarkan ke aktual penjualan belum tertagih dan faktur. |
|   Manajemen peluang | 2594015 | Kuotasi tidak dapat ditutup sebagai menang untuk pelanggan yang memiliki persyaratan pembayaran **Net60**. |
| Perencanaan dan pelacakan proyek | 2595841 | Di Project for the Web, pengguna menerima pesan kesalahan tentang **msdyn\_actualstart** yang hilang ketika mereka membuat permintaan sumber daya baru. |
| Waktu dan Pengeluaran | 2602511 | Bidang **Ditolak oleh** untuk entri waktu menampilkan **Sistem** , bukan pengguna bernama sebagai penolak. |
| Waktu dan Pengeluaran | 2602528 | Pemberi izin proyek dapat menyetujui waktu pada proyek yang tidak terdaftar sebagai pemberi izin. |
| Penagihan dan harga | 2608550 | Faktur koreksi dapat dikonfirmasi meskipun tidak ada perubahan pada yang asli. |

## <a name="removed-and-deprecated-features"></a>Fitur yang dihapus dan tidak digunakan lagi

artikel [Fitur yang dihilangkan atau tidak digunakan lagi di Project Operations](../../whats-new/removed-depreciated-features-project.md) menjelaskan fitur yang telah dihilangkan atau ditolak untuk Dynamics 365 Project Operations.

- Fitur yang dihapuskan tidak akan lagi tersedia di dalam produk.
- Fitur yang tidak digunakan lagi tidak dalam pengembangan aktif dan akan dihapus pada pembaruan mendatang.

Pengumuman pembatalan akan muncul dalam artikel [fitur yang Dihilangkan atau ditolak di Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 bulan sebelum fitur apa pun dihapus dari produk.

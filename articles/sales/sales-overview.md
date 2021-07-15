---
title: Ikhtisar proses penjualan
description: Topik ini menyediakan informasi tentang proses penjualan dasar.
author: rumant
ms.date: 10/29/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: ed9731193e83eebd35e979adffcea529a289b9c5
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368345"
---
# <a name="sales-process-overview"></a>Ikhtisar proses penjualan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Proses penjualan yang digunakan dalam organisasi berbasis proyek berbeda dari proses penjualan yang digunakan dalam organisasi berbasis produk. Ini karena siklus penjualan untuk organisasi berbasis proyek lebih lama dan memerlukan perkiraan teknik yang disesuaikan untuk menganalisis dan membuat kuotasi untuk setiap transaksi. Dynamics 365 Project Operations menggunakan beberapa fungsi berikut yang digunakan dalam proses penjualan:

- Rekaman prospek digunakan untuk melacak proses penjualan.
- Kualifikasi prospek dilacak sebagai peluang.
- Semua artefak terkait untuk peluang dapat diakses. Artefak ini mencakup tim penjualan, pemangku kepentingan, probabilitas, peringkat, tahapan penjualan, dan proses bisnis.
- Beberapa kuotasi dibuat untuk peluang.
- Kuotasi diberi status, **ditutup sebagai pemenang** untuk membuat pesanan penjualan. Dalam Project Operations, pesanan penjualan disesuaikan dan disebut kontrak proyek.

## <a name="estimate-a-sale"></a>Mengestimasi penjualan
Nilai penjualan dapat diperkirakan berdasarkan proyek yang sebelumnya telah dikirim dan kompleksitas proyek. Untuk proyek yang melibatkan ekstensi ke proyek sebelumnya, atau proyek di mana keahlian Penjual tinggi dan template kerja yang telah dikenal digunakan, Anda dapat menggunakan proses estimasi yang lebih sederhana. Proyek yang lebih kompleks biasanya memiliki proses pembelian lebih lama. Oleh karena itu, ada lebih banyak tahapan dalam proses estimasi penjualan. Di awal proses, tim penjualan menggunakan input manajer akun dan ahli (UKM) untuk membuat perkiraan tingkat tinggi untuk setiap komponen pekerjaan yang berbeda yang dibuat kuotasinya. Komponen pekerjaan ini diwakili oleh baris kuotasi. 

Anda dapat membuat perkiraan kuotasi tingkat tinggi. Akhirnya, perkiraan tingkat tinggi ini akan digantikan dengan perkiraan lebih rinci berdasarkan rencana proyek yang Anda buat menggunakan template proyek standar. Template ini membantu Anda membuat jadwal dan menentukan nilai moneter pada kuotasi dan komponennya (baris kuotasi). 

Anda dapat membuat beberapa kuotasi untuk proyek dan mengelompokkannya dalam satu rekaman peluang. Akhirnya, salah satu kuotasi tersebut ditandai **ditutup sebagai menang**, dan kontrak proyek atau pernyataan pekerjaan (Sow) dibuat. Kontrak proyek berisi nilai kontrak untuk setiap komponen (baris kontrak) yang diterima oleh pelanggan untuk pelaksanaan. SOW biasanya dibuat sebagai dokumen Microsoft Word. Semua faktur yang dikirim ke pelanggan selama periode pengiriman proyek merujuk pada kontrak proyek atau SOW.

Anda juga dapat membuat kuotasi alternatif dalam satu rekaman peluang atau mengkonfigurasi sistem sehingga kontrak proyek dibuat saat kuotasi dimenangkan. Dalam kasus ini, Anda dapat melampirkan dokumen Word yang mewakili SOW untuk rekaman kontrak proyek.

## <a name="configure-the-sales-process"></a>Mengkonfigurasi proses penjualan
Anda dapat menggunakan alur proses bisnis untuk mengkonfigurasi proses penjualan Anda. Alur ini menyediakan antarmuka visual terpandu untuk memindahkan transaksi maju melalui tahapan proses penjualan.

Misalnya, perusahaan Anda mungkin memiliki enam tahapan berikut dalam proses penjualan:

1. Kualifikasi
2. Perkiraan
3. Pemeriksaan Internal
4. Kontrak
5. Kirim
6. Tutup
 
Organisasi Anda mungkin menggunakan entitas yang berbeda untuk menunjukkan kesepakatan yang sama seiring perkembangannya. Di awal proses penjualan, kesepakatan diwakili oleh entitas peluang. Seiring berjalannya waktu dan rincian lainnya muncul, Anda dapat menggunakan perkiraan tingkat tinggi untuk membuat satu atau beberapa kuotasi. Jika salah satu dari kuotasi ini ditinjau oleh pemangku kepentingan internal dan pelanggan, entitas kuotasi menunjukkan transaksi. Setelah pelanggan menerima kuotasi, kontrak proyek atau SOW menunjukkan kesepakatan. Untuk mendukung perilaku ini, BPF distrukturkan sehingga setiap tahapan dalam proses dihubungkan dengan tabel database yang berbeda.

Tahapan **kualifikasi** dalam proses penjualan dapat didukung oleh entitas peluang. Tahapan **estimasi** dan **peninjauan internal** dapat didukung oleh entitas kuotasi. Tahapan **kontrak**, **Pelaksanaan**, dan **penutupan** dapat didukung oleh entitas kontrak proyek.

Saat Anda meneruskan transaksi melalui tahapan, Anda akan diminta membuat rekaman entitas yang sesuai untuk membantu dan memandu Anda melakukan proses. Tahapan dapat kondisional. Misalnya, jika Anda memerlukan peninjauan internal pada kuotasi hanya jika kuotasi menggunakan daftar harga kustom, Anda dapat mengkonfigurasikan kondisi tersebut dalam tahapan proses bisnis yang sesuai. Tahap **peninjauan internal** kemudian ditampilkan hanya untuk kuotasi yang menggunakan daftar harga kustom. Untuk semua transaksi dan kuotasi lainnya, tahapan **estimasi** diikuti oleh tahapan **kontrak**.

> [!NOTE]
> Project Operations memiliki halaman tertentu untuk rekaman entitas peluang, kuotasi, pesanan, dan faktur. Anda harus membuat rekaman ini menggunakan halaman informasi proyek untuk entitas ini. Jika tidak, Anda tidak akan dapat membuka rekaman dari halaman **informasi proyek**. Jika Anda ingin membuka rekaman dari halaman **informasi proyek**, Anda harus menghapus rekaman dan membuatnya kembali menggunakan halaman **informasi proyek** dengan logika bisnis untuk masing-masing jenis entitas ini memastikan bahwa bidang **jenis** rekaman diatur dengan benar, dan semua konsep wajib diinisialisasi dengan benar.


## <a name="track-revisions-to-quotes-and-project-plans-in-the-sales-cycle"></a>Melacak revisi untuk kuotasi dan rencana proyek dalam siklus penjualan
Dalam Project Operations, Anda tidak dapat melacak revisi yang dibuat ke kuotasi. Namun, Anda harus menandai kuotasi yang ada **ditutup sebagai kalah**, lalu membuat kuotasi baru. Anda dapat menyalin kuotasi atau mengkloning kuotasi berbasis proyek.

## <a name="track-comments-and-approvals-of-quotes-and-project-contracts"></a>Melacak komentar dan persetujuan kuotasi dan kontrak proyek
Anda dapat mengelola peninjauan dan persetujuan kuotasi dan kontrak proyek menggunakan posting dan dinding rekaman. Organisasi Anda dapat membuat alur kerja dan plug-in kustom untuk menetapkan, mengalihkan, melaporkan, dan mengelola pemberitahuan peninjauan dan persetujuan item kerja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
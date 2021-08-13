---
title: Apa yang baru di bulan April 2021 - penyebaran Project Operations lite
description: Pembaruan topik ini menyediakan informasi tentang pembaruan kualitas yang tersedia di penyebaran Project Operations lite april 2021.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c85e0230840753bc1d28a46b065bce002446f5d8c62da9666d58bc9d2a68af8
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009400"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Apa yang baru di bulan April 2021 - penyebaran Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

  - Lingkungan Project Operations untuk Dataverse versi 4.9.0.221 

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- Bahan tanpa stok untuk proyek. Kemampuan utama mencakup:
  - Memperkirakan dan menentukan harga bahan yang tidak tersedia selama siklus penjualan untuk proyek. Untuk informasi lebih lanjut, lihat [Mengonfigurasikan biaya dan tarif penjualan untuk produk katalog - lite](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Melacak penggunaan bahan yang tidak tersedia selama pelaksanaan proyek. Untuk informasi lebih lanjut, lihat [Merekam penggunaan bahan pada proyek dan tugas proyek](../../material/material-usage-log.md).
  - Menagih biaya bahan non stok yang digunakan. Untuk informasi lebih lanjut, [lihat Mengelola akumulasi penagihan - lite](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - API baru di Dynamics 365 Dataverse memungkinkan operasi buat, perbarui, dan hapus dengan **entitas Penjadwalan**. Untuk informasi lebih lanjut, lihat [Menggunakan API Jadwal untuk melakukan operasi dengan entitas Penjadwalan](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Pembaruan kualitas

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan harga | 2224568 | Menambahkan logika untuk mengaktifkan penyesuaian yang melibatkan faktur plug-in konfirmasi faktur. |
| Penagihan dan harga | 2101098 | Meningkatkan logika bidang default ke faktur proforma: **Alamat Tagihan**, **Tagihan ke Nama**, dan **Persyaratan Pembayaran** sekarang default dari rekaman pelanggan kontrak proyek yang terkait. |
| Penagihan dan harga | 2021413 | Memperbarui bidang **Biaya Aktual** dan **Penjualan** pada entitas **Tugas** untuk mencakup nilai penjualan dari pengeluaran yang belum ditagih dan ditagih pada tugas. |
| Penagihan dan harga | 2182110 | Saat menyalin kontrak proyek, ID baris kontrak diregenerasi dalam kontrak proyek tujuan untuk memastikan keunikannya. |
| Manajemen peluang | 2186741 | Menambahkan validasi untuk memastikan bidang **Asal** dan **Jenis Transaksi** tidak dapat diperbarui pada rincian baris kuotasi yang ada. |
| Manajemen peluang | 2191353 | Tahapan tidak boleh dibuat pada baris kontrak waktu dan bahan. |
| Manajemen peluang | 2216956 | Memperbaiki masalah **Pembaruan Harga**. |
| Perencanaan dan Pelacakan | 2182979 | Fungsi salinan proyek ditingkatkan untuk memastikan baris estimasi pengeluaran disalin dari proyek asli. |
| Perencanaan dan Pelacakan | 2184144 | Fungsi salinan proyek ditingkatkan untuk memastikan nama posisi sumber daya disalin dari proyek asli. |
| Perencanaan dan Pelacakan | 2184799 | Salinan proyek: Kontrol yang dikuatkan untuk memastikan perkiraan tanggal mulai tidak dapat diubah saat penyalinan sedang berlangsung. |
| Perencanaan dan Pelacakan | 2185134 | Salinan proyek: Tanggal mulai perkiraan proyek tujuan diatur ke tanggal hari ini. |
| Perencanaan dan Pelacakan | 2196373 | Salinan proyek: Memastikan rekaman manajer proyek dan anggota tim tidak diduplikasikan dalam tim proyek. |
| Perencanaan dan Pelacakan | 2211833 | Salinan proyek: Penugasan sumber daya disalin dari tugas proyek sumber ke proyek tujuan. |
| Perencanaan dan Pelacakan | 2186541 | Memperbaiki masalah di kisi **Estimasi** saat mengelompokkan berdasarkan sumber daya. |
| Perencanaan dan Pelacakan | 2166906 | Kategori transaksi dari tugas harus disalin ke entitas **Penetapan Sumber Daya**. |
| Manajemen sumber daya | 2125362 | Memperbaiki masalah saat membuat anggota tim generik menggunakan metode alokasi berbasis jam. |
| Waktu dan Pengeluaran | 2113603 | Memperbaiki masalah yang terkait dengan penyesuaian dengan menghapus atribut dari halaman **Entri Waktu**. Sistem sekarang memeriksa apakah atribut sudah ada pada halaman sebelum mengaksesnya menggunakan skrip. |
| Waktu dan Pengeluaran | 2204377 | Lembar waktu yang disalin harus ditampilkan secara otomatis bila Anda memilih **Salin Pekan** selama entri waktu. |
| Waktu dan Pengeluaran | 2209059 | Bidang **status** dapat diedit untuk entri waktu Dynamics 365 Field Service. |

---
title: Apa yang baru di bulan Mei 2021 - penyebaran Project Operations lite
description: Pembaruan topik ini menyediakan informasi tentang pembaruan kualitas yang tersedia di penyebaran Project Operations lite Mei 2021.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6fb1955e2adb8562ac00a90880bf8e147bf5ed6a
ms.sourcegitcommit: 18bb56676999dbde1cf880239847ee9c2b216fe4
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/18/2021
ms.locfileid: "6060437"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Apa yang baru di bulan Mei 2021 - penyebaran Project Operations lite

_Berlaku untuk: Penyebaran sederhana - menangani faktur proforma_

Topik ini berlaku untuk komponen dan versi Dynamics 365 Project Operations berikut ini:

   - Lingkungan Project Operations untuk Dataverse versi 4.10.0.186.

## <a name="features-included-in-this-release"></a>Beberapa fitur tercakup dalam rilis ini

Berikut adalah fitur yang tercakup dalam rilis ini:

- [Mode penjadwalan](../../project-management/scheduling-modes.md): Manajer proyek sekarang dapat menentukan apakah proyek harus dikelola menggunakan durasi tetap, pekerjaan tetap, atau mode penjadwalan unit tetap.

## <a name="quality-updates"></a>Pembaruan kualitas

| **Area fitur** | **Nomor Referensi** | **Pembaruan kualitas** |
| --- | --- | --- |
| Penagihan dan harga | 2224568 | Menambahkan logika untuk mengaktifkan penyesuaian yang melibatkan faktur plug-in konfirmasi faktur. |
| Penagihan dan harga | 2101098 | Meningkatkan logika bidang default menjadi faktur proforma. Bidang tersebut mencakup, **alamat tagih ke**, **Nama tagih ke**, dan **Persyaratan pembayaran**. Bidang sekarang default dari rekaman pelanggan kontrak proyek yang terkait. |
| Penagihan dan harga | 2021413 | Memperbarui bidang **Biaya Aktual** dan **Penjualan** pada entitas **Tugas** untuk mencakup nilai penjualan dari pengeluaran yang belum ditagih dan ditagih pada tugas. |
| Penagihan dan harga | 2182110 | Saat menyalin kontrak proyek, ID baris kontrak diregenerasi dalam kontrak proyek tujuan untuk memastikan keunikannya. |
| Manajemen peluang | 2186741 | Menambahkan validasi untuk memastikan bidang **Asal** dan Jenis Transaksi tidak dapat diperbarui pada rincian baris kuotasi yang ada. |
| Manajemen peluang | 2191353 | Pembuatan tahapan tidak boleh diizinkan pada baris kontrak waktu dan bahan. |
| Manajemen peluang | 2216956 | Memperbaiki masalah **Pembaruan Harga**. |
| Perencanaan dan Pelacakan | 2182979 | Fungsi salinan proyek ditingkatkan untuk memastikan baris estimasi pengeluaran disalin dari proyek asli. |
| Perencanaan dan Pelacakan | 2184144 | Fungsi salinan proyek ditingkatkan untuk memastikan nama posisi sumber daya disalin dari proyek asli. |
| Perencanaan dan Pelacakan | 2184799 | Memperketat kontrol ketika menyalin proyek untuk memastikan perkiraan tanggal mulai tidak dapat diubah saat penyalinan sedang berlangsung. |
| Perencanaan dan Pelacakan | 2185134 | Selama penyalinan proyek, tanggal mulai perkiraan proyek tujuan diatur ke tanggal hari ini. |
| Perencanaan dan Pelacakan | 2196373 | Memastikan rekaman manajer proyek dan anggota tim tidak diduplikasikan dalam tim proyek ketika menyalin proyek. |
| Perencanaan dan Pelacakan | 2211833 | Penugasan sumber daya disalin dari tugas proyek sumber ke proyek tujuan. |
| Perencanaan dan Pelacakan | 2186541 | Memperbaiki masalah di kisi **Estimasi** saat mengelompokkan berdasarkan **sumber daya**. |
| Perencanaan dan Pelacakan | 2166906 | Kategori transaksi dari tugas harus disalin ke entitas **Penetapan Sumber Daya**. |
| Manajemen sumber daya | 2125362 | Memperbaiki masalah saat membuat anggota tim generik menggunakan metode alokasi berbasis jam. |
| Waktu dan Pengeluaran | 2113603 | Memperbaiki masalah yang terkait dengan penyesuaian dengan menghapus atribut dari halaman **Entri Waktu**. Sistem memeriksa apakah atribut sudah ada pada halaman sebelum mengakses atribut menggunakan skrip. |
| Waktu dan Pengeluaran | 2204377 | Lembar waktu yang disalin harus ditampilkan secara otomatis bila Anda memilih **Salin Pekan**. |
| Waktu dan Pengeluaran | 2209059 | Bidang **status** dapat diedit untuk entri waktu Dynamics 365 Field Service. |
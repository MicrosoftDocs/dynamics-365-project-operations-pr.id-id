---
title: Mengelola status dan validasi yang tidak boleh dilewati
description: Topik ini menyediakan informasi tentang pemeriksaan batas yang tidak boleh dilewati yang dilakukan dalam Project Operations.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 09dea414e91a365f33bd23089c427b5f63f55c8e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129997"
---
# <a name="manage-not-to-exceed-status-and-validations"></a>Mengelola status dan validasi yang tidak boleh dilewati 

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

## <a name="not-to-exceed-on-approvals"></a>Tidak boleh dileawti dalam persetujuan

Bila entri waktu atau pengeluaran diajukan, rekaman persetujuan akan dibuat. Jika persetujuan ini dikenakan biaya dan dipetakan ke baris kontrak waktu dan material, sistem akan menyelesaikan pemeriksaan validasi tidak boleh dilewati di tingkat berikut:

  - Periksa terhadap batas yang diatur untuk pelanggan pada baris kontrak proyek
  - Periksa terhadap batas yang diatur pada baris kontrak
  - Periksa terhadap batas yang diatur untuk pelanggan
  - Periksa terhadap batas yang diatur pada kontrak

Pemeriksaan pada setiap tingkat mencakup memastikan bahwa jumlah nilai penjualan pada persetujuan ini tidak akan melanggar batas yang tidak boleh dilewati pada tingkat tersebut setelah penghitungan jumlah untuk akumulasi penagihan direkam, dan jumlah tersebut ditagih pada tanggal untuk tingkat tersebut.

Jika pemeriksaan lulus, persetujuan diberikan status validasi **Berhasil**.

Jika pemeriksaan gagal, persetujuan diberikan status validasi **Gagal**. Rincian validasi tidak boleh dilewati akan menginformasikan pada pengguna tentang tingkat validasi yang gagal.

Bila entri waktu atau pengeluaran yang diajukan dianggap tidak dikenakan biaya, status validasi tidak boleh dilewati diatur **tidak berlaku** dengan detail validasi sama dengan **tidak berlaku**.

## <a name="not-to-exceed-on-unbilled-sales-actuals"></a>Tidak boleh dilewati pada aktual penjualan yang belum ditagih

Bila entri waktu atau pengeluaran disetujui, rekaman aktual biaya dan penjualan yang belum ditagih akan dibuat. Jika aktual penjualan belum ditagih yang dibuat dikenakan biaya dan dipetakan ke baris kontrak waktu dan material, aplikasi akan melakukan pemeriksaan validasi tidak boleh dilewati di tingkat berikut:

  - Periksa terhadap batas yang diatur untuk pelanggan baris kontrak proyek
  - Periksa terhadap batas yang diatur pada baris kontrak
  - Periksa terhadap batas yang diatur untuk pelanggan
  - Periksa terhadap batas yang diatur pada kontrak

Pemeriksaan pada setiap tingkat memastikan bahwa jumlah nilai penjualan pada aktual tidak akan melanggar batas yang tidak boleh dilewati pada tingkat tersebut setelah penghitungan jumlah untuk akumulasi penagihan direkam, dan jumlah tersebut ditagih pada tanggal untuk tingkat tersebut.

Jika pemeriksaan lulus, aktual penjualan yang belum ditagih diberikan status tidak boleh dilewati **Ditindaklanjuti**.

Jika pemeriksaan gagal, aktual penjualan yang belum ditagih diberikan status tidak boleh dilewati **Gagal**. Rincian validasi menginformasikan pada pengguna tentang tingkat validasi yang gagal.

Bila aktual penjualan yang belum ditagih dianggap tidak dikenakan biaya atau gratis, jika tidak ada konfigurasi batas yang tidak boleh terlampaui di salah satu dari empat tingkat, atau jika aktual yang dibuat adalah biaya, panjar, unit sumber daya, atau penjualan antar-organisasi, bidang **status tidak boleh dilewati** dan **Rincian validasi tidak boleh dilewati** harus diatur ke **tidak berlaku**.

## <a name="reset-the-not-to-exceed-status"></a>Atur Ulang Status tidak boleh terlewati

Anda dapat melakukan reset massal dari status tidak boleh terlewati. Hal ini memungkinkan manajer proyek menyesuaikan validasi batas yang tidak boleh terlewati untuk memprioritaskan faktur dari satu badan kerja, waktu, atau pengeluaran tertentu di atas lainnya yang telah ditindaklanjuti dari jumlah tidak boleh terlewati yang tersedia.

Setelah status tidak boleh terlewati diatur ulang pada aktual penjualan yang belum ditagih, jumlah komitmen akan dikurangi. Manajer proyek dapat memilih badan kerja, waktu, atau pengeluaran lain yang sebelumnya telah gagal dalam validasi tidak boleh terlewati dan mengevaluasi ulang. Dengan pengurangan jumlah komitmen, aktual ini sekarang akan lulus validasi. Ini membantu manajer proyek mengerahkan pengaruh yang lebih besar dan kontrol atas transaksi yang bisa ditagih untuk periode tersebut.

Untuk mengatur ulang status tidak boleh terlewati, pilih satu atau beberapa aktual dari tampilan **akumulasi tagihan waktu dan material** atau **aktual**, lalu pilih **Atur ulang status tidak boleh terlewati**.

Status tidak boleh terlewati akan diatur ulang ke **tidak dievaluasi** pada semua aktual yang relevan. Aktual yang diatur ulang status tidak boleh terlewatinya adalah aktual penjualan belum ditagih yang belum difaktur, bukan pada faktur draf, dan ditandai sebagai kena biaya. Setiap aktual lainnya yang dipilih akan diabaikan.

## <a name="reevaluate-not-to-exceed-status"></a>Evaluasi Ulang Status tidak boleh terlewati

Anda dapat melakukan re-evaluasi massal dari status tidak boleh terlewati. Evaluasi ulang status tidak boleh terlewati akan berguna bila:

  - Terdapat renegosiasi batas tidak boleh terlewati dengan pelanggan dan aktual akan perlu dievaluasi ulang.
  - Manajer Proyek ingin menyempurnakan faktur akumulasi penjualan yang belum ditagih dengan memprioritaskan satu badan kerja dibandingkan yang lain.

Untuk mengevaluasi ulang status tidak boleh terlewati, pilih satu atau beberapa aktual dari tampilan **akumulasi tagihan waktu dan material** atau **aktual**, dan pilih **Evaluasi ulang status tidak boleh terlewati**.

Semua aktual tertentu yang relevan dengan batas yang tidak boleh terlewati akan dievaluasi terhadap konfigurasi yang tidak boleh terlewati. Aktual yang relevan untuk evaluasi ulang status tidak boleh terlewati adalah aktual penjualan belum ditagih yang tidak difaktur, bukan pada faktur draf, dan ditandai sebagai kena biaya. Setiap aktual terpilih lainnya dipilih.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
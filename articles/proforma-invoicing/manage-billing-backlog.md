---
title: Mengelola akumulasi tagihan
description: Topik ini menyediakan informasi tentang cara melihat dan bekerja dengan akumulasi penagihan di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ec77f3911a460b96414a61bc44ea254f1b7da660
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087966"
---
# <a name="manage-the-billing-backlog"></a>Mengelola akumulasi tagihan

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Dynamics 365 Project Operations memiliki dua tampilan khusus untuk membantu Anda bekerja dengan dan mengelola akumulasi penagihan. Mereka adalah **Tonggak Harga Tetap** dan **Akumulasi Penagihan Waktu dan Material** Untuk memilih tampilan, di area **Penjualan** Project Operations, di halaman navigasi kiri, pilih **Penagihan**. Tautan akumulasi penagihan disimpan di sana.

## <a name="fixed-price-milestones"></a>Tahapan Harga Tetap

Tampilan ini mencantumkan semua pencapaian harga tetap di semua baris kontrak proyek dalam sistem. Satu atau beberapa tonggak pencapaian dapat ditandai sebagai **Siap untuk Faktur** atau **Tidak Siap untuk Faktur** dari tampilan ini. Saat Anda menandai tonggak pencapaian sebagai **Siap untuk Faktur** , tonggak pencapaian tersedia untuk faktur draf.

Ketika baris kontrak multi-pelanggan memiliki metode penagihan harga tetap, satu tonggak pencapaian dibuat untuk setiap pelanggan di baris kontrak. Pengguna membuat tonggak pencapaian dan tonggak itu dibagi menjadi rekaman tonggak pencapaian spesifik pelanggan secara internal, menurut pemisahan persentase penagihan yang ditentukan untuk setiap pelanggan di baris kontrak. Dalam tampilan **Tonggak Harga Tetap** , Anda akan melihat rekaman tonggak khusus pelanggan individual. Masing-masing rekaman tonggak ini dapat ditandai sebagai **Siap untuk Faktur** secara terpisah dari tampilan ini. Ketika satu atau beberapa pemisahan tonggak terkait ditandai sebagai **Siap untuk Faktur** , header berpindah ke status **Sedang Berlangsung** dari **Belum Dimulai**. Ketika semua pemisahan tonggak pencapaian telah ditagih, status tonggak pencapaian header menjadi **Selesai**.

Tonggak pencapaian pada faktur draf diperlihatkan dalam tampilan ini dengan status tagihan **Faktur Pelanggan Dibuat**. Ketika draf faktur dikonfirmasi, status penagihan pada rekaman ini diperbarui ke **Faktur Diposting**. Memperbarui nilai status ini dengan menggunakan kode kustom tidak disarankan. Project Operations tidak akan berfungsi dengan benar jika nilai status ini diperbarui dengan kode kustom.

## <a name="time-and-material-billing-backlog"></a>Waktu dan Materi Backlog Penagihan

Tampilan ini mencantumkan semua aktual penjualan yang belum ditagih di semua kontrak proyek dalam sistem. Satu atau beberapa aktual penjualan yang belum ditagih dapat ditandai sebagai **Siap untuk Faktur** atau **Tidak Siap untuk Faktur** dari tampilan ini. Menandai aktual penjualan belum ditagih sebagai **Siap untuk Faktur** membuatnya tersedia untuk diletakkan pada faktur draf.

Aktual penjualan yang belum ditagih yang memiliki status **Tidak Boleh Melebihi** **Gagal** tidak dapat ditandai sebagai **Siap untuk Faktur**. Jika aktual ini perlu ditandai seperti itu, reset status pada aktual lain pada baris kontrak yang diterapkan, lalu evaluasi status **Tidak Boleh Melebihi**.

Dalam kasus baris kontrak multi-pelanggan yang memiliki metode penagihan waktu dan material, ketika waktu dan pengeluaran disetujui, aktual penjualan yang belum ditagih dibuat untuk setiap pelanggan di baris kontrak sesuai dengan pemisahan persentase penagihan yang ditentukan untuk setiap pelanggan di baris kontrak. Dalam tampilan **Akumulasi Penagihan Waktu dan Material** , Anda akan melihat aktual penjualan belum ditagih khusus pelanggan ini. Masing-masing rekaman aktual penjualan belum ditagih ini dapat ditandai sebagai **Siap untuk Faktur** secara terpisah dari tampilan ini.

Aktual penjualan belum ditagih pada faktur draf diperlihatkan dalam tampilan ini dengan **status tagihan** **Faktur Pelanggan Dibuat**. Ketika draf faktur dikonfirmasi, status penagihan pada rekaman ini diperbarui ke **Faktur Pelanggan Diposting**. Memperbarui nilai status ini ketika berada dalam status ini dengan menggunakan kode kustom tidak disarankan. Project Operations tidak akan berfungsi dengan benar jika nilai status ini diperbarui dengan kode kustom.

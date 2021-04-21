---
title: Mengelola akumulasi penagihan proyek
description: Informasi topik ini berisi informasi tentang berbagai tampilan yang tersedia untuk digunakan saat mengelola akumulasi penagihan pada proyek.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25dc9cff6aeb6daed9a27ba843a74b892ca4751c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867000"
---
# <a name="manage-project-billing-backlog"></a>Mengelola akumulasi penagihan proyek 

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Dynamics 365 Project Operations memiliki tampilan khusus untuk membantu mengelola akumulasi tagihan. Untuk mengelola akumulasi tagihan, pilih tautan di area **penjualan**, dalam **penagihan**. 

Tampilan berikut tersedia:

- Panjar dan Uang Muka
- Panjar dan Uang Muka yang Tersedia
- Tahapan Harga Tetap
- Backlog Penagihan Produk
- Waktu dan Materi Backlog Penagihan

## <a name="retainers-and-advances"></a>Panjar dan Uang Muka

**Panjar dan uang muka** mencantumkan semua panjar dan uang muka di semua kontrak proyek di sistem. Setelah panjar atau uang muka ditagih, jumlah uang muka akan tersedia untuk digunakan.

## <a name="available-retainers-and-advances"></a>Panjar dan Uang Muka yang Tersedia

**Panjar dan uang muka yang tersedia** mencantumkan semua panjar dan uang muka yang tersedia di semua kontrak proyek di sistem. Setelah panjar atau uang muka ditagih, jumlah uang muka akan tersedia untuk digunakan dan ditambahkan ke daftar. Setelah jumlah panjar atau uang muka digunakan sepenuhnya, akan dihapus dari daftar.

## <a name="fixed-price-milestones"></a>Tahapan Harga Tetap

Tampilan **tonggak pencapaian harga tetap** melihat daftar semua tonggak pencapaian harga tetap di semua baris kontrak proyek di sistem. Satu atau beberapa tonggak pencapaian dapat ditandai sebagai **Siap untuk Faktur** atau **Tidak Siap untuk Faktur** dari tampilan ini. Menandai tonggak pencapaian sebagai **siap faktur** membuatnya tersedia untuk diletakkan pada faktur draft.

Bila baris kontrak multi pelanggan memiliki metode penagihan harga tetap, tonggak pencapaian dibuat untuk setiap pelanggan pada baris kontrak. Sebuah tonggak pencapaian dapat dibuat dan kemudian dibagi menjadi rekaman tonggak pencapaian khusus pelanggan individual. Pemecahan ini bersifat internal dan sesuai dengan pemecahan persentase penagihan yang ditentukan untuk setiap pelanggan pada baris kontrak. Pada tampilan **tonggak pencapaian harga tetap**, Anda akan melihat rekaman tonggak pencapaian spesifik pelanggan individual. Masing-masing rekaman tonggak ini dapat ditandai sebagai **Siap untuk Faktur** secara terpisah dari tampilan ini. Ketika satu atau lebih tonggak pencapaian terkait dibagi ditandai sebagai **siap faktur**, status header diperbarui ke **Sedang berlangsung** dari **belum dimulai**. Bila semua pemecahan tonggak pencapaian ditagih, status header tonggak diperbarui ke **selesai**.

Tonggak pencapaian pada faktur draf diperlihatkan dalam tampilan ini dengan status tagihan **Faktur Pelanggan Dibuat**. Bila faktur draf dikonfirmasi, status penagihan pada rekaman akan diperbarui ke **faktur Pelanggan diposting**. Jangan Perbarui nilai status ini menggunakan kode kustom. Project Operations tidak berfungsi dengan benar saat nilai status ini diperbarui dengan kode kustom.

## <a name="product-billing-backlog"></a>Backlog Penagihan Produk

Tampilan **akumulasi tagihan produk** mencantumkan semua baris kontrak berbasis produk di semua kontrak proyek di sistem. Satu atau beberapa baris kontrak berbasis produk dapat ditandai sebagai **Siap untuk Faktur** atau **Tidak Siap untuk Faktur** dari tampilan ini. Menandai baris kontrak berbasis produk sebagai **siap faktur** membuatnya tersedia untuk diletakkan pada faktur draft.

Baris kontrak berbasis produk yang ada pada faktur draf ditampilkan dalam tampilan ini dengan status penagihan **faktur Pelanggan dibuat**. Ketika draf faktur dikonfirmasi, status penagihan pada rekaman ini diperbarui ke **Faktur Pelanggan Diposting**. Jangan Perbarui nilai status ini menggunakan kode kustom. Project Operations tidak berfungsi dengan benar saat nilai status ini diperbarui dengan kode kustom.

## <a name="time-and-material-billing-backlog"></a>Waktu dan Materi Backlog Penagihan

Tampilan **akumulasi penagihan waktu dan material** mencantumkan semua aktual penjualan yang tidak ditagih di semua kontrak proyek dalam sistem yang belum ditagih. Satu atau beberapa aktual penjualan yang belum ditagih dapat ditandai sebagai **Siap untuk Faktur** atau **Tidak Siap untuk Faktur** dari tampilan ini. Menandai aktual penjualan belum ditagih sebagai **Siap untuk Faktur** membuatnya tersedia untuk diletakkan pada faktur draf.

Aktual penjualan yang tidak ditagih dengan status **tidak boleh melebihi** **Gagal** tidak dapat ditandai sebagai **siap untuk faktur**. Jika aktual harus ditandai sebagai **siap untuk faktur**, atur ulang status pada aktual lain pada baris kontrak yang ditindaklanjuti. lalu evaluasi ulang status **Tidak Boleh Melebihi**.

Jika baris kontrak multi-pelanggan memiliki metode tagihan waktu dan material, bila waktu dan pengeluaran disetujui, satu aktual penjualan tidak ditagih dibuat untuk setiap pelanggan pada baris kontrak berdasarkan persentase penagihan yang ditetapkan untuk setiap pelanggan. Pada tampilan **akumulasi penagihan waktu dan material**, Anda akan melihat aktual penjualan tidak ditagih khusus pelanggan individual ini. Masing-masing rekaman aktual penjualan belum ditagih ini dapat ditandai sebagai **Siap untuk Faktur** secara terpisah dari tampilan ini.

Aktual penjualan tidak tertagih yang ada pada faktur draf ditampilkan dalam tampilan ini dengan status penagihan **faktur Pelanggan dibuat**. Ketika draf faktur dikonfirmasi, status penagihan pada rekaman ini diperbarui ke **Faktur Pelanggan Diposting**. Jangan Perbarui nilai status ini dengan menggunakan kode kustom. Project Operations tidak berfungsi dengan benar saat nilai status ini diperbarui dengan kode kustom.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

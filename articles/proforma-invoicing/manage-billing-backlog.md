---
title: Mengelola akumulasi tagihan
description: Artikel ini menyediakan informasi tentang cara melihat dan bekerja dengan akumulasi penagihan di Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929382"
---
# <a name="manage-billing-backlog"></a>Mengelola akumulasi tagihan

**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok

Dynamics 365 Project Operations memiliki tampilan khusus untuk membantu mengelola akumulasi tagihan. Untuk mengelola akumulasi tagihan, pilih tautan di area **penjualan**, dalam **penagihan**. 

Tampilan berikut tersedia:

- Panjar dan Uang Muka
- Panjar dan Uang Muka yang Tersedia
- Tahapan Harga Tetap
- Waktu dan Materi Backlog Penagihan

## <a name="retainers-and-advances"></a>Panjar dan Uang Muka

Tampilan **Uang muka dan panjar** mencantumkan uang muka dan panjar di seluruh kontrak proyek. Setelah panjar atau uang muka ditagih, jumlah uang muka akan tersedia untuk digunakan.

## <a name="available-retainers-and-advances"></a>Panjar dan Uang Muka yang Tersedia

Tampilan **Uang muka dan panjar yang tersedia** mencantumkan semua uang muka dan panjar yang tersedia di seluruh kontrak proyek. Setelah panjar atau uang muka ditagih, jumlah uang muka akan tersedia untuk digunakan dan ditambahkan ke daftar. Setelah jumlah panjar atau uang muka digunakan seluruhnya, maka jumlah panjar atau uang muka akan dihapus dari daftar.

## <a name="fixed-price-milestones"></a>Tahapan Harga Tetap

Tampilan **Tahapan Harga Tetap** mencantumkan semua tahapan harga tetap di seluruh baris kontrak proyek. Dari tampilan ini, satu atau beberapa tahapan dapat ditandai sebagai **Siap ditagih** atau **Tidak siap untuk faktur**. Menandai tonggak pencapaian sebagai **siap faktur** membuatnya tersedia untuk diletakkan pada faktur draft.

Bila baris kontrak multi pelanggan memiliki metode penagihan harga tetap, tonggak pencapaian dibuat untuk setiap pelanggan pada baris kontrak. Sebuah tonggak pencapaian dapat dibuat dan kemudian dibagi menjadi rekaman tonggak pencapaian khusus pelanggan individual. Pemecahan ini bersifat internal dan sesuai dengan pemecahan persentase penagihan yang ditentukan untuk setiap pelanggan pada baris kontrak. Pada tampilan **tonggak pencapaian harga tetap**, Anda akan melihat rekaman tonggak pencapaian spesifik pelanggan individual. Masing-masing rekaman tonggak ini dapat ditandai sebagai **Siap untuk Faktur** secara terpisah dari tampilan ini. Bila satu atau beberapa dari pecahan tahapan terkait ditandai sebagai **Siap Ditagih**, status header akan diperbarui ke **Sedang Berlangsung** dari **Belum Dimulai**. Bila semua pecahan tahapan ditagihkan, status tahapan header akan diperbarui ke **Selesai**.

Tonggak pencapaian pada faktur draf diperlihatkan dalam tampilan ini dengan status tagihan **Faktur Pelanggan Dibuat**. Bila faktur draf dikonfirmasi, status penagihan pada rekaman akan diperbarui ke **faktur Pelanggan diposting**. 

> [!NOTE] 
> Jangan perbarui nilai status ini menggunakan kode kustom. Project Operations tidak berfungsi dengan benar saat nilai status ini diperbarui dengan kode kustom.

## <a name="time-and-material-billing-backlog"></a>Waktu dan Materi Backlog Penagihan

Tampilan **akumulasi penagihan waktu dan material** mencantumkan semua aktual penjualan yang tidak ditagih di semua kontrak proyek dalam sistem yang belum ditagih. Satu atau beberapa aktual penjualan yang belum ditagih dapat ditandai sebagai **Siap untuk Faktur** atau **Tidak Siap untuk Faktur** dari tampilan ini. Menandai aktual penjualan belum ditagih sebagai **Siap untuk Faktur** membuatnya tersedia untuk diletakkan pada faktur draf.

Aktual penjualan yang tidak ditagih dengan status **tidak boleh melebihi** **Gagal** tidak dapat ditandai sebagai **siap untuk faktur**. Jika aktual harus ditandai sebagai **Siap Ditagih**, atur ulang status pada aktual lain pada baris kontrak yang dilaksanakan, lalu evaluasi ulang status ke **Tidak Melebihi**.

Jika baris kontrak multi-pelanggan memiliki metode tagihan waktu dan material, bila waktu dan pengeluaran disetujui, satu aktual penjualan tidak ditagih dibuat untuk setiap pelanggan pada baris kontrak berdasarkan persentase penagihan yang ditetapkan untuk setiap pelanggan. Pada tampilan **akumulasi penagihan waktu dan material**, Anda akan melihat aktual penjualan tidak ditagih khusus pelanggan individual ini. Masing-masing rekaman aktual penjualan belum ditagih ini dapat ditandai sebagai **Siap untuk Faktur** secara terpisah dari tampilan ini.

aktual Penjualan belum tertagih yang ada pada draf faktur ditampilkan di tampilan ini dengan status penagihan **Faktur Pelanggan Dibuat**. Ketika draf faktur dikonfirmasi, status penagihan pada rekaman ini diperbarui ke **Faktur Pelanggan Diposting**. 

> [!NOTE] 
> Jangan perbarui nilai status ini menggunakan kode kustom. Project Operations tidak berfungsi dengan benar saat nilai status ini diperbarui dengan kode kustom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

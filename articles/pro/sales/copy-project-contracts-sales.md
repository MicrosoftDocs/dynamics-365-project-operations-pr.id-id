---
title: Menyalin kontrak proyek - lite
description: Topik ini menyediakan informasi tentang menyalin kontrak proyek di Project operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee769dbd553e4a174cb71ce7a883f828e587ce36
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003590"
---
# <a name="copy-project-contracts---lite"></a>Menyalin kontrak proyek - lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Anda dapat dengan mudah membuat kontrak proyek baru dengan membuat salinan kontrak yang ada dengan salah satu dari dua cara: 

  - Pada halaman daftar **kontrak proyek**, pilih kontrak proyek, lalu pilih **Salin**.
  - Pada halaman detail **Kontrak Proyek**, pilih **Salin**.

Halaman dialog akan terbuka jika Anda memilih parameter kontrak yang disalin. Bidang berikut ini disertakan pada dialog. Tergantung pada nilai yang dipilih di dialog ini, proses penyalinan dapat berubah.

| **Bidang** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- |
| Topik | Masukkan topik kontrak target. Bila halaman dialog terbuka, sistem akan mengatur bidang ini ke nama kontrak sumber dengan **salinan** ditambahkan padanya. | Tidak ada dampak hilir untuk bidang ini. |
| Pelanggan | Merujuk pada perusahaan atau rekaman akun pelanggan. Bila dialog terbuka, sistem akan mengatur bidang ini ke akun pada kontrak sumber. | Bidang ini adalah pelanggan utama pada kontrak. |
| Unit Kontrak | Unit organisasi yang bertanggung jawab atas pengiriman proyek yang terkait dengan transaksi ini. Bila halaman dialog terbuka, sistem akan diatur ke akun pada unit kontrak kontrak sumber. | Unit kontrak adalah divisi perusahaan yang akan melaksanakan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang. Mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang terjadi selama proyek. |
| Mata uang | Ini adalah mata uang transaksi untuk kesepakatan. Bila halaman dialog terbuka, sistem akan mengatur bidang ke mata uang kontrak sumber. Mata uang dapat diubah. Jika ya, bidang **Salin Harga** selalu diatur ke **Tidak** karena daftar harga pada kontrak sumber tidak lagi relevan. | Mata uang digunakan untuk daftar harga default, untuk membangun estimasi keuangan untuk kontrak, dan untuk menagih pelanggan saat transaksi dimenangkan. |
| Tanggal Pengiriman yang Diminta | Tanggal pengiriman yang diminta oleh pelanggan. | Tanggal ini digunakan sebagai tanggal akhir saat Anda membuat tanggal faktur di sepanjang frekuensi tertentu. |
| Salin Harga | Menunjukkan apakah harga pada kontrak harus disalin dari kontrak sumber. | Jika bidang diatur ke **ya**, daftar harga proyek dan referensi daftar harga produk disalin dari sumber ke kontrak target. Jika **tidak** dipilih, daftar harga akan didefault-kan ulang berdasarkan daftar harga terbaru pada akun atau parameter proyek. |

Bila Anda memilih **OK** pada halaman dialog, sistem akan membuat salinan kontrak berdasarkan parameter yang dipilih. Kontrak baru akan terbuka.

Informasi berikut tidak disalin dari **sumber** ke **kontrak target**:

  - Jadwal faktur
  - Kontrak dan Pelanggan Baris Kontrak
  - Referensi proyek pada baris kontrak berbasis proyek
  - Informasi anggaran Pelanggan

Karena informasi ini spesifik untuk setiap kontrak, bidang dan rekaman ini tidak disalin. Baris kontrak untuk proyek dan produk, detail estimasi baris kontrak, dan nilai yang tidak melebihi batas pada tingkat kontrak akan disalin. Harga dan tingkat biaya default tergantung pada pilihan di bidang **Salin harga** yang dipilih pada halaman dialog **Salin parameter**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
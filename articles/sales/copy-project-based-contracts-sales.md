---
title: Menyalin kontrak berbasis proyek
description: Artikel ini menyediakan informasi tentang menyalin kontrak proyek di Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410371"
---
# <a name="copy-project-based-contracts"></a>Menyalin kontrak berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Anda dapat dengan mudah membuat kontrak proyek baru dengan menyalin kontrak yang ada dengan salah satu dari dua cara:

- Pada halaman **daftar Kontrak** Proyek, pilih kontrak proyek, lalu pilih **Salin**.
- Pada halaman detail **Kontrak Proyek**, pilih **Salin**.

Dalam kedua kasus, kotak dialog muncul, di mana Anda dapat mengatur parameter kontrak yang disalin. Kotak dialog mencakup bidang berikut ini. Bergantung pada nilai yang Anda pilih, proses penyalinan mungkin berubah.

| Bidang | Deskripsi | Dampak hilir |
| --- | --- | --- |
| Topik | Masukkan topik kontrak target. Ketika kotak dialog dibuka, sistem mengatur bidang ke nama kontrak sumber, tetapi kata "salin" ditambahkan ke dalamnya. | Tidak ada dampak hilir untuk bidang ini. |
| yang terhormat | Referensi pada perusahaan atau rekaman akun pelanggan. Ketika kotak dialog dibuka, sistem mengatur bidang ke akun pada kontrak sumber. | Bidang ini adalah pelanggan utama pada kontrak. |
| Perusahaan Pemilik | Perusahaan yang bertanggung jawab atas pengiriman proyek yang terkait dengan kesepakatan ini. Ketika kotak dialog dibuka, sistem mengatur bidang ke perusahaan pemilik kontrak sumber. | Perusahaan pemilik adalah badan hukum yang akan melaksanakan proyek setelah kesepakatan ditutup. Mata uang perusahaan pemilik harus sesuai dengan mata uang unit kontraktor. |
| Unit Kontrak | Unit organisasi yang bertanggung jawab untuk pengiriman proyek yang terkait dengan kesepakatan ini. Ketika kotak dialog dibuka, sistem mengatur bidang ke unit kontrak kontrak sumber. | Unit kontrak adalah divisi perusahaan yang akan melaksanakan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang. Mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang dikeluarkan selama proyek. |
| Mata uang | Ini adalah mata uang transaksi untuk kesepakatan. Ketika kotak dialog dibuka, sistem mengatur bidang ke mata uang kontrak sumber. Mata uang dapat diubah. Jika ya, **bidang Salin Harga** selalu diatur ke **Tidak**, karena daftar harga pada kontrak sumber tidak lagi relevan. | Mata uang ini digunakan untuk daftar harga default, untuk menghasilkan perkiraan keuangan pada kontrak, dan untuk menagih pelanggan ketika kesepakatan dimenangkan. |
| Tanggal Pengiriman yang Diminta | Tanggal pengiriman yang diminta oleh pelanggan. | Tanggal ini digunakan sebagai tanggal akhir saat Anda membuat tanggal faktur pada frekuensi tertentu. |
| Salin Harga | Nilai yang menunjukkan apakah harga pada kontrak harus disalin dari kontrak sumber. | Jika bidang diatur ke **Ya**, referensi daftar harga proyek dan produk disalin dari kontrak sumber ke kontrak target. Jika diatur ke **Tidak**, daftar harga default akan digunakan, berdasarkan daftar harga terbaru di parameter akun atau proyek. |

Saat Anda memilih **OK** di kotak dialog, sistem membuat salinan kontrak, berdasarkan nilai parameter yang Anda tetapkan. Kemudian kontrak baru dibuka.

Informasi **berikut tidak** disalin dari kontrak sumber ke kontrak target, karena khusus untuk setiap kontrak:

- Jadwal faktur
- Kontrak dan Pelanggan Baris Kontrak
- Referensi proyek pada baris kontrak berbasis proyek
- Informasi anggaran Pelanggan

Garis kontrak untuk proyek dan produk, perkiraan dalam detail garis kontrak, dan nilai yang tidak melebihi pada tingkat kontrak disalin. Entri harga default dan tarif biaya bergantung pada pilihan di **bidang Salin harga** di **kotak dialog Salin Parameter**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

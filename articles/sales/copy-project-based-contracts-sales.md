---
title: Menyalin kontrak berbasis proyek
description: artikel ini menyediakan informasi tentang menyalin kontrak proyek di Microsoft Dynamics 365 Project Operations.
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

- Pada halaman daftar **kontrak proyek**, pilih kontrak proyek, lalu pilih **Salin**.
- Pada halaman detail **Kontrak Proyek**, pilih **Salin**.

Di kedua kasus, kotak dialog akan muncul, di mana Anda dapat mengatur parameter kontrak yang disalin. Kotak dialog ini mencakup bidang berikut ini. Tergantung pada nilai yang Anda pilih, proses penyalinan dapat berubah.

| Bidang | Description | Dampak hilir |
| --- | --- | --- |
| Topik | Masukkan topik kontrak target. Bila kotak dialog terbuka, sistem akan mengatur bidang ini ke nama kontrak sumber, tetapi kotak "copy" akan ditambahkan padanya. | Tidak ada dampak hilir untuk bidang ini. |
| yang terhormat | Referensi pada perusahaan atau rekaman akun pelanggan. Bila kotak dialog terbuka, sistem akan mengatur bidang ini ke akun pada kontrak sumber. | Bidang ini adalah pelanggan utama pada kontrak. |
| Perusahaan Pemilik | Perusahaan yang bertanggung jawab atas pengiriman proyek yang terkait dengan transaksi ini. Bila kotak dialog terbuka, sistem akan mengatur bidang ini ke perusahaan pemilik kontrak sumber. | Perusahaan pemilik adalah entitas hukum yang akan melaksanakan proyek setelah transaksi ditutup. Mata uang perusahaan pemilik harus cocok dengan mata uang dari unit kontrak. |
| Unit Kontrak | Unit organisasi yang bertanggung jawab atas pengiriman proyek yang terkait dengan transaksi ini. Bila kotak dialog terbuka, sistem akan mengatur bidang ini ke unit kontrak dari kontrak sumber. | Unit kontrak adalah divisi perusahaan yang akan melaksanakan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang. Mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang dibebankan selama proyek. |
| Mata uang | Ini adalah mata uang transaksi untuk kesepakatan. Bila kotak dialog terbuka, sistem akan mengatur bidang ke mata uang kontrak sumber. Mata uang dapat diubah. Jika ya, bidang **Salin Harga** selalu diatur ke **Tidak**, karena daftar harga pada kontrak sumber tidak lagi relevan. | Mata uang ini digunakan untuk daftar harga default, untuk membuat estimasi keuangan untuk kontrak, dan untuk menagih pelanggan saat transaksi dimenangkan. |
| Tanggal Pengiriman yang Diminta | Tanggal pengiriman yang diminta oleh pelanggan. | Tanggal ini digunakan sebagai tanggal akhir saat Anda membuat tanggal faktur pada frekuensi tertentu. |
| Salin Harga | Nilai yang menunjukkan apakah harga pada kontrak harus disalin dari kontrak sumber. | Jika bidang diatur ke **ya**, daftar harga proyek dan referensi daftar harga produk disalin dari kontrak sumber ke kontrak target. Jika diatur ke **tidak**, daftar harga default akan digunakan, berdasarkan daftar harga terbaru pada akun atau parameter proyek. |

Bila Anda memilih **OK** pada kotak dialog, sistem akan membuat salinan kontrak berdasarkan nilai parameter yang Anda atur. Maka kontrak baru akan terbuka.

Informasi berikut **tidak** disalin dari kontrak sumber ke kontrak target, karena khusus untuk setiap kontrak:

- Jadwal faktur
- Kontrak dan Pelanggan Baris Kontrak
- Referensi proyek pada baris kontrak berbasis proyek
- Informasi anggaran Pelanggan

Baris kontrak untuk proyek dan produk, detail estimasi baris kontrak, dan nilai yang tidak melebihi batas pada tingkat kontrak akan disalin. Entri tingkat biaya dan harga default bergantung pada pilihan di bidang **Salin harga** yang dipilih pada halaman kotak dialog **Salin parameter**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

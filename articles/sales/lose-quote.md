---
title: Menyalin kuotasi berbasis proyek
description: Topik ini memberikan informasi tentang cara menyalin kuotasi berbasis proyek di Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4e70ed1451c1076f72ef5d7200b918c626ab23c
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181816"
---
# <a name="copy-project-based-quotes"></a>Menyalin kuotasi berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Anda dapat dengan mudah membuat kuotasi proyek baru dengan menyalin yang ada. 

- Untuk menyalin kuotasi proyek, pada halaman daftar **kuotasi proyek** atau halaman rincian **kuotasi proyek** , pilih kuotasi proyek yang akan disalin, lalu pilih **Salin**.

Ini akan membuka halaman dialog di mana Anda dapat memasukkan parameter salinan. Tabel berikut mencantumkan bidang yang disertakan di halaman dialog. Tergantung pada nilai yang Anda pilih, proses penyalinan dapat berubah.

| **Bidang** | **Keterangan** | **Dampak hilir** |
| --- | --- | --- |
| Topik | Masukkan topik yang relevan, atau nama, dari kuotasi target. Bila dialog terbuka, sistem akan menetapkannya ke topik sumber kuotasi dengan **-salinan** yang ditambahkan padanya. | |
| Calon Pelanggan | Merujuk pada perusahaan atau rekaman akun pelanggan. Bila dialog terbuka, sistem akan diatur ke akun pada kuotasi sumber. | Bidang ini adalah pelanggan utama pada kuotasi. |
| Unit Kontrak | Unit organisasi yang bertanggung jawab atas pengiriman proyek yang terkait dengan transaksi ini.
Bila dialog terbuka, sistem akan diatur ke akun pada unit kontrak kuotasi sumber. | Unit kontrak adalah divisi perusahaan yang akan melaksanakan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang. Mata uang digunakan untuk melaporkan perkiraan dan biaya aktual yang terjadi selama pelaksanaan proyek. |
| Mata uang | Ini adalah mata uang transaksi untuk kesepakatan. Bila dialog terbuka, sistem akan diatur ke akun pada mata uang kuotasi sumber. Hal ini dapat dimodifikasi dan jika perubahan, bidang **Salin harga** selalu diatur ke **tidak**. Hal ini dikarenakan daftar harga pada kuotasi sumber tidak lagi relevan. | Mata uang digunakan untuk default daftar harga, untuk membangun estimasi keuangan pada kuotasi, dan akhirnya untuk menagih pelanggan saat transaksi dimenangkan. |
| Tanggal Pengiriman yang Diminta | Ini adalah tanggal pengiriman yang diminta oleh pelanggan. | Ini digunakan sebagai tanggal akhir saat membuat tanggal faktur di sepanjang frekuensi tertentu. |
| Salin Harga | Nilai ya/tidak menunjukkan apakah harga pada kuotasi harus disalin dari kuotasi sumber. | Jika **ya** dipilih, daftar harga proyek dan referensi daftar harga produk disalin dari kuotasi sumber ke kuotasi target. Jika **tidak** dipilih, daftar harga akan didefault-kan ulang berdasarkan daftar harga terbaru yang diatur pada akun atau parameter proyek. |

Bila Anda memilih **OK** pada halaman dialog, sistem akan membuat salinan kuotasi proyek berdasarkan parameter yang dipilih dalam dialog. Kuotasi proyek baru akan terbuka. 

> [!NOTE]
> Informasi berikut tidak disalin dari sumber ke kuotasi target:
>
> - Jadwal faktur
> - Pelanggan baris kuotasi dan kuotasi
> - Referensi proyek pada baris kuotasi berbasis proyek- informasi anggaran pelanggan
>
>Karena informasi ini sangat spesifik untuk setiap kuotasi, bidang dan rekaman ini tidak disalin. Baris Kuotasi untuk proyek dan produk, detail estimasi baris kuotasi, dan nilai yang tidak melebihi batas pada tingkat kuotasi akan disalin. Harga dan tingkat biaya default tergantung pada pilihan **Salin harga** yang dipilih pada halaman dialog **Salin parameter**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
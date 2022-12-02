---
title: Menyalin peluang-peluang berbasis proyek
description: Artikel ini memberikan informasi tentang cara menyalin peluang berbasis proyek di Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: cc772391de97f4b2de6e9e29f97a6af4d5514319
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926136"
---
# <a name="copy-project-based-opportunities"></a>Menyalin peluang-peluang berbasis proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_


Peluang proyek dapat dengan mudah disalin untuk membuat peluang proyek baru. 

1. Buka halaman daftar **peluang proyek** dan pilih peluang dari daftar. Atau, buka halaman rincian peluang tertentu. 
2. Dari halaman mana pun, pilih **Salin**. Halaman dialog akan terbuka yang berisi informasi bidang berikut. Tergantung pada nilai yang dipilih di dialog ini, proses penyalinan dapat berubah.

    | **Bidang** | **Keterangan** | **Dampak hilir** |
    | --- | --- | --- |
    | Topik | Masukkan topik yang relevan dari peluang target. Bila dialog terbuka, sistem akan menetapkannya ke topik peluang sumber dengan **salinan** yang ditambahkan padanya. | Tidak ada dampak hilir untuk bidang ini. |
    | Akun | Merujuk pada perusahaan atau rekaman akun pelanggan. Bila dialog terbuka, sistem akan diatur ke akun pada peluang sumber. | Bidang ini adalah pelanggan utama pada peluang. |
    | Unit Kontrak | Unit organisasi yang bertanggung jawab atas pengiriman proyek yang terkait dengan transaksi ini. Bila dialog terbuka, sistem akan diatur ke akun pada unit kontrak peluang sumber. | Unit kontrak adalah divisi perusahaan yang akan melaksanakan proyek setelah transaksi ditutup. Setiap unit kontrak memiliki mata uang, dan mata uang ini digunakan untuk melaporkan perkiraan dan biaya aktual yang timbul selama proyek. |
    | Mata uang | Ini adalah mata uang transaksi untuk kesepakatan. Bila halaman dialog terbuka, sistem akan diatur ke akun pada mata uang peluang sumber. | Mata uang digunakan untuk default daftar harga dan membangun estimasi keuangan pada kuotasi. Akhirnya, mata uang digunakan untuk menagih pelanggan saat transaksi dimenangkan. |
    | Salin Harga | Nilai ya/tidak yang menunjukkan apakah harga pada peluang harus disalin dari peluang sumber. | Jika **ya** dipilih, daftar harga akan disalin dari sumber ke peluang target. Jika **tidak** dipilih, daftar harga akan di-default berdasarkan daftar harga terbaru yang diatur. |

3. Pilih **OK**. Sistem membuat salinan peluang proyek berdasarkan parameter yang dipilih dan peluang proyek baru dibuka.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
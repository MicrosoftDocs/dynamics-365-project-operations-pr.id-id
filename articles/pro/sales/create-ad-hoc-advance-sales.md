---
title: Membuat uang muka ad hoc pada kontrak
description: Topik ini menyediakan informasi tentang cara membuat uang muka pada kontrak sesuai kebutuhan.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ee97710a9f0229cef3ff9dbfda6a2f108726df20
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/14/2022
ms.locfileid: "8594030"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a>Membuat uang muka ad hoc pada kontrak

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

Microsoft Dynamics 365 Project Operations mendukung skenario faktur yang melibatkan prapembayaran dan uang muka. Proses penggunaan **Uang muka** dalam **Project Operations** serupa dengan kontrak **Panjar**. 

Selesaikan langkah-langkah berikut untuk menagih pelanggan untuk uang muka.

1. Buka halaman **kontrak proyek**, lalu pilih tab **Uang muka dan panjar**.
2. Di subkisi yang mencantumkan semua kemajuan dan pembayaran awal yang direkam sebelumnya, pilih **+ Panjar kontrak proyek baru**. 

    Formulir **pembuatan cepat** akan terbuka untuk rekaman pra-pembayaran atau uang muka.
    
3. Tabel di bawah ini berisi daftar bidang untuk perekaman sebelumnya dan pertimbangan yang perlu diingat saat Anda membuat yang baru:

    | Bidang | KETERANGAN | Dampak hilir |
    | --- | --- | --- |
    | **Pelanggan Kontrak Proyek** | Bidang ini menunjukkan pelanggan mana pada kontrak akan ditagih untuk uang muka ini. | Jika Anda memiliki beberapa pelanggan pada kontrak dan ingin menagih masing-masing untuk panjar atau uang muka tertentu, buat uang muka untuk setiap pelanggan secara individual. |
    | **Keterangan** | Deskripsi tentang tujuan atau waktu dari uang muka untuk membantu mengidentifikasi uang muka ini. | Deskripsi ini akan ditampilkan pada baris faktur untuk uang muka ini. |
    | **Jumlah** | Jumlah pembayaran pra-bayar atau uang muka. | Jumlah ini akan ditampilkan pada baris faktur untuk uang muka ini. |
    | **Tanggal Faktur** | Tanggal saat uang muka ini ditagih ke pelanggan. | Ini adalah tanggal untuk proses pembuatan faktur otomatis untuk membuat baris faktur untuk uang muka ini. |
    | **Status Faktur** | Ini adalah pengaturan pilihan yang menunjukkan apakah uang muka ini ditambahkan ke draf faktur untuk pelanggan ini. Nilai yang mungkin adalah:</br>- **Belum siap dibuatkan faktur**</br>- **Siap dibuatkan faktur** | Bila uang muka atau pra-pembayaran ditandai sebagai **siap faktur**, maka ditambahkan sebagai waktu baris pada faktur draft. Hanya uang muka yang sepenuhnya ditagih yang dapat digunakan untuk rekonsiliasi dengan biaya proyek untuk periode faktur berikutnya. |

4. Pilih **Simpan dan tutup** di dialog buat cepat untuk merekam uang muka atau pembayaran di awal.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
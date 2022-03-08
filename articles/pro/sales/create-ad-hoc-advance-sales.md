---
title: Membuat uang muka ad hoc pada kontrak -Lite
description: Topik ini menyediakan informasi tentang cara membuat uang muka pada kontrak sesuai kebutuhan.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a6bf02c2e2ab2f3c696b1eab1b92a20272187bf5
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181366"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract---lite"></a>Membuat uang muka ad hoc pada kontrak -Lite

_**Berlaku untuk:** Penyebaran sederhana - menangani faktur proforma_

Microsoft Dynamics 365 Project Operations mendukung skenario faktur yang melibatkan pra-pembayaran dan uang muka. Proses penggunaan **Uang muka** dalam **Project Operations** serupa dengan kontrak **Panjar**. 

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

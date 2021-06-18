---
title: Mata uang
description: Topik ini memberikan informasi tentang cara menambahkan dan menghapus jenis mata uang dalam Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9c2c6f98e48c5ee251d44131d0c05c705faf1459
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011285"
---
# <a name="currency"></a>Mata uang

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/non-lengkap, penyebaran sederhana -menangani faktur proforma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Mata uang menentukan harga produk dalam Katalog Produk dan biaya transaksi, seperti pesanan penjualan. Jika pelanggan Anda tersebar di berbagai geografis, tambahkan mata uang mereka untuk mengelola transaksi Anda. Tambahkan mata uang yang paling sesuai untuk kebutuhan bisnis saat ini dan masa depan Anda.  

> [!NOTE]
> Jika lingkungan Anda adalah lingkungan Common Data Service, Anda berada di pusat admin Power Platform, dan Anda memilih halaman **mata uang** (**lingkungan** > [Pilih lingkungan]> **pengaturan** > **bisnis** > **mata uang**), halaman akan kosong. Hal ini dikarenakan penetapan mata uang tidak didukung di lingkungan Common Data Service.

## <a name="add-a-currency"></a>Menambahkan mata uang  
Sebelum anda memulai prosedur ini, verifikasikan bahwa peran keamanan anda mencakup izin admin sistem. 

1. Di pusat admin Power Platform, pilih lingkungan. 
2. Pilih **Pengaturan** > **Bisnis**.
3. Pilih **mata uang**.  
4. Pilih **baru**.  
5. Isi informasi yang diperlukan.  


   |          Bidang          |                                                                                                                                                                                                                                                                                                                                                                            Keterangan                                                                                                                                                                                                                                                                                                                                                                            |
   |-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |    **Jenis Mata Uang**    | - **Sistem** -Pilih pilihan ini jika Anda ingin menggunakan mata uang yang tersedia di aplikasi berbasis model di Dynamics 365. Pilih tombol **Pencarian** untuk mencari sebuah mata uang. Ketika Anda memilih sebuah kode mata uang, **nama mata uang** dan **simbol mata uang** akan secara otomatis ditambahkan untuk mata uang yang dipilih.<br />- **Kustom** -Pilih pilihan ini jika Anda ingin menambahkan mata uang yang tidak tersedia di aplikasi berbasis model di Dynamics 365. Dalam kasus ini, Anda harus secara manual memasukkan nilai **kode mata uang**, **presisi mata uang**, **nama mata uang**, **simbol mata uang**, dan **konversi mata uang**. |
   |    **Kode Mata Uang**    |                                                                                                                                                                                                                                                                                                                                            Formulir singkat untuk mata uang. Contoh: **USD** untuk Dolar Amerika Serikat.                                                                                                                                                                                                                                                                                                                                            |
   | **Presisi Mata Uang**  |                                                                                                                                                                                  Ketik jumlah desimal yang Anda ingin gunakan untuk mata uang.  Anda dapat menambahkan nilai antara 0 dan 4. **Catatan:**  Jika Anda telah menetapkan nilai presisi di kotak dialog **pengaturan sistem**, nilai itu akan muncul di sini.                                                                                                                                                                                  |
   |    **Nama Mata Uang**    |                                                                                                                                                                                                                                         Jika Anda memilih kode mata uang dari daftar mata uang yang tersedia di aplikasi berbasis model di Dynamics 365, nama mata uang untuk kode yang dipilih ditampilkan di sini. Jika Anda memilih **Kustom** sebagai jenis mata uang, ketik nama mata uang.                                                                                                                                                                                                                                          |
   |   **Simbol Mata Uang**   |                                                                                                                                                                                                                                                                      Jika Anda memilih kode mata uang dari daftar mata uang yang tersedia, simbol untuk mata uang yang dipilih ditampilkan di sini. Jika Anda memilih **Kustom** sebagai jenis mata uang, masukkan simbol untuk mata uang baru.                                                                                                                                                                                                                                                                       |
   | **Konversi Mata Uang** |                                                                                                                                                                                                                                     Ketik nilai mata uang yang dipilih dalam satu dolar AS. Ini adalah jumlah di mana mata uang yang dipilih dikonversi ke mata uang dasar. **Penting:**  Pastikan Anda memperbarui nilai ini sesering yang diperlukan untuk menghindari setiap perhitungan yang tidak akurat dalam transaksi Anda.                                                                                                                                                                                                                                      |


6. Setelah selesai, di bilah perintah, pilih **Simpan** atau **Simpan dan tutup**.  

   > [!TIP]
   >  Untuk mengedit mata uang, pilih mata uang, dan kemudian masukkan atau pilih nilai baru.  

## <a name="delete-a-currency"></a>Menghapus mata uang  

1. Di pusat admin Power Platform, pilih lingkungan. 
2. Pilih **Pengaturan** > **Bisnis**.
3. Pilih **mata uang**.  
4. Dari daftar mata uang yang ditampilkan, pilih mata uang untuk dihapus.  
5. Pilih **Hapus**.  
6. Konfirmasikan Penghapusan.  

> [!IMPORTANT]
>  Anda tidak dapat menghapus mata uang yang digunakan oleh rekaman lainnya; Anda hanya dapat menonaktifkan mereka. Menonaktifkan mata uang catatan tidak menghapus informasi mata uang yang disimpan dalam catatan yang sudah ada, seperti peluang atau pesanan. Namun, Anda tidak akan dapat memilih mata uang dinonaktifkan untuk transaksi yang baru.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]
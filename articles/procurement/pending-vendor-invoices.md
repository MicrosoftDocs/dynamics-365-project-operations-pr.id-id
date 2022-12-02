---
title: Beli bahan non-stok atau kategori pengadaan dengan faktur vendor tertunda
description: Artikel ini menjelaskan cara mencatat faktur vendor yang tertunda.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b1c05755f6759e90e031a11261f15a2c4b6b716e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921996"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Beli bahan non-stok atau kategori pengadaan dengan faktur vendor tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Sebagai perusahaan yang mendapatkan bahan non-stok atau kategori pengadaan untuk proyek, biayanya dapat dengan segera dicatat terhadap proyek. 

Contohnya, Contoso Robotics US melakukan proyek pembaruan perlengkapan dan memerlukan lisensi perangkat lunak. Lisensi ini diperoleh dari vendor pihak ketiga.  Menggunakan Dynamics 365 Finance, petugas utang dagang mencatat dokumen faktur vendor yang tertunda dan mengaitkan biaya lisensi secara langsung terhadap proyek pembaruan perlengkapan. 

> [!IMPORTANT]
> Sebelum Anda menggunakan fungsi yang dijelaskan di artikel ini, lihat dan terapkan konfigurasi yang diperlukan. Untuk informasi lebih lanjut, lihat [Mengaktifkan bahan non-stok dan faktur vendor yang tertunda](configure-materials-nonstocked.md) serta [Menggunakan pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Posting faktur vendor tertunda terkait proyek 

Faktur vendor yang tertunda dapat direkam pada halaman **faktur vendor tertunda** (**utang dagang** > **Faktur** > **Faktur vendor tertunda**). Selesaikan langkah-langkah berikut untuk memposting faktur vendor tertunda terkait proyek:

1. Buka **utang dagang** > **Faktur**, lalu pilih **Baru**. 
1. Pada bidang **Akun faktur**, pilih vendor kemudian pada bidang **Nomor**, masukkan identifikasi faktur vendor.
1. Tambahkan baris ke faktur vendor kemudian di bidang **Nomor Item**, pilih item non-stok yang dibeli dari vendor. Atau, dalam bidang **Kategori pengadaan**, pilih kategori pengadaan yang dibeli dari vendor.   
1. Tambahkan kuantitas yang dibeli. Sistem akan mengisi harga per unit berdasarkan konfigurasi harga item yang tidak distok. 
1. Verifikasikan jumlah total dan rincian lainnya yang diperlukan di baris.
1. Pada detail baris, pada tab **Proyek**, pilih ID proyek untuk mencatat item ini.
1. Opsional: pilih nomor aktivitas, lalu perbarui kategori proyek dan properti baris.
1. Posting faktur vendor yang tertunda. Ketika faktur diposting, sistem mencatat informasi bidang berikut:
    
    - Jumlah saldo vendor.
    - Jumlah Pajak Penjualan.
    - Biaya terhadap proyek dicatat ke akun integrasi pengadaan.
    - Transaksi biaya aktual proyek dalam Dataverse.  Transaksi ini diproses lebih lanjut menggunakan [jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Mem-posting jurnal ini akan memindahkan jumlah tersebut dari akun integrasi pengadaan ke akun biaya proyek. 
    - Pembelian yang ditagihkan ke pelanggan proyek menggunakan metode penagihan waktu dan bahan. Selain itu, transaksi penjualan belum ditagih dibuat untuk pembelian di Dataverse. Daftar harga produk di Dataverse digunakan untuk harga penjualan dan jumlah transaksi penjualan belum tertagih.

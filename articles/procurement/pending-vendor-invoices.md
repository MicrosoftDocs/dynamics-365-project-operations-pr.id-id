---
title: Membeli materi yang tidak ditebar atau kategori pengadaan menggunakan faktur vendor yang tertunda
description: Laporan topik menjelaskan cara mencatat faktur vendor yang tertunda.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612661"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Membeli materi yang tidak ditebar atau kategori pengadaan menggunakan faktur vendor yang tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Sebagai perusahaan pengadaan bahan non-stocked atau kategori pengadaan untuk proyek, biaya dapat segera dicatat terhadap proyek. 

Contohnya, Contoso Robotics US melakukan proyek pembaruan perlengkapan dan memerlukan lisensi perangkat lunak. Lisensi ini diperoleh dari vendor pihak ketiga.  Dengan menggunakan Dynamics 365 Finance, petugas hutang Akun mencatat dokumen faktur vendor yang tertunda dan mengaitkan biaya lisensi secara langsung terhadap proyek perpanjangan peralatan. 

> [!IMPORTANT]
> Sebelum Anda menggunakan fungsi yang dijelaskan di topik ini, lihat dan terapkan konfigurasi yang diperlukan. Untuk informasi selengkapnya, lihat [Mengaktifkan materi yang tidak ditebar dan faktur vendor](configure-materials-nonstocked.md) yang tertunda serta [Menggunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Posting faktur vendor tertunda terkait proyek 

Faktur vendor yang tertunda dapat direkam pada halaman **faktur vendor tertunda** (**utang dagang** > **Faktur** > **Faktur vendor tertunda**). Selesaikan langkah-langkah berikut untuk memposting faktur vendor tertunda terkait proyek:

1. **Buka Faktur** > **Hutang** Akun, dan pilih **Baru**. 
1. **Di bidang Akun faktur**, pilih vendor, lalu, di **bidang Nomor**, masukkan identifikasi faktur vendor.
1. Tambahkan baris ke faktur vendor, lalu, di **bidang Nomor** item, pilih item yang tidak ditebar yang dibeli dari vendor. Atau, di **bidang kategori** Pengadaan, pilih kategori pengadaan yang dibeli dari vendor.   
1. Tambahkan jumlah yang dibeli. Sistem mengisi harga satuan, berdasarkan konfigurasi harga barang yang tidak terisi. 
1. Verifikasikan jumlah total dan rincian lainnya yang diperlukan di baris.
1. Di detail baris, pada **tab Proyek**, pilih ID proyek tempat item ini akan direkam.
1. Opsional: Pilih nomor aktivitas, dan perbarui kategori proyek dan properti baris.
1. Posting faktur vendor yang tertunda. Saat faktur diposting, sistem mencatat informasi berikut:
    
    - Jumlah saldo vendor.
    - Jumlah Pajak Penjualan.
    - Biaya terhadap proyek dicatat ke akun integrasi pengadaan.
    - Transaksi biaya aktual proyek dalam Dataverse.  Transaksi ini diproses lebih lanjut menggunakan [jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Mem-posting jurnal ini akan memindahkan jumlah tersebut dari akun integrasi pengadaan ke akun biaya proyek. 
    - Pembelian yang ditagihkan ke pelanggan proyek menggunakan metode penagihan waktu dan bahan. Selain itu, transaksi penjualan belum ditagih dibuat untuk pembelian di Dataverse. Daftar harga produk di Dataverse digunakan untuk harga penjualan dan jumlah transaksi penjualan belum tertagih.

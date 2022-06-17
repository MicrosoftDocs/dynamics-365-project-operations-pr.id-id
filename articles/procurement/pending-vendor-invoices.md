---
title: Membeli bahan yang tidak ditebar atau kategori pengadaan menggunakan faktur vendor yang tertunda
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
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>Membeli bahan yang tidak ditebar atau kategori pengadaan menggunakan faktur vendor yang tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Karena perusahaan memperoleh bahan yang tidak ditebar atau kategori pengadaan untuk suatu proyek, biaya dapat segera dicatat terhadap proyek tersebut. 

Contohnya, Contoso Robotics US melakukan proyek pembaruan perlengkapan dan memerlukan lisensi perangkat lunak. Lisensi ini diperoleh dari vendor pihak ketiga.  Dengan Dynamics 365 Finance, petugas hutang Dagang mencatat dokumen faktur vendor yang tertunda dan mengaitkan biaya lisensi secara langsung dengan proyek pembaruan peralatan. 

> [!IMPORTANT]
> Sebelum Anda menggunakan fungsionalitas yang dijelaskan dalam artikel ini, tinjau dan terapkan konfigurasi yang diperlukan. Untuk informasi selengkapnya, lihat [Mengaktifkan materi yang tidak tersedia dan faktur](configure-materials-nonstocked.md) vendor yang tertunda dan [Menggunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>Posting faktur vendor tertunda terkait proyek 

Faktur vendor yang tertunda dapat direkam pada halaman **faktur vendor tertunda** (**utang dagang** > **Faktur** > **Faktur vendor tertunda**). Selesaikan langkah-langkah berikut untuk memposting faktur vendor tertunda terkait proyek:

1. Buka **Faktur hutang** > **Dagang**, dan pilih **Baru**. 
1. **Di bidang Akun faktur**, pilih vendor, lalu, di **bidang Nomor**, masukkan identifikasi faktur vendor.
1. Tambahkan baris ke faktur vendor, lalu, di **bidang Nomor** item, pilih item yang tidak memiliki stok yang dibeli dari vendor. Atau, di **bidang kategori** Pengadaan, pilih kategori pengadaan yang dibeli dari vendor.   
1. Tambahkan jumlah yang dibeli. Sistem mengisi harga satuan, berdasarkan konfigurasi harga barang yang tidak ditebar. 
1. Verifikasikan jumlah total dan rincian lainnya yang diperlukan di baris.
1. Di detail baris, pada tab **Proyek**, pilih ID proyek tempat item ini akan direkam.
1. Opsional: Pilih nomor aktivitas, dan perbarui kategori proyek dan properti baris.
1. Posting faktur vendor yang tertunda. Ketika faktur diposting, sistem mencatat informasi berikut:
    
    - Jumlah saldo vendor.
    - Jumlah Pajak Penjualan.
    - Biaya terhadap proyek dicatat ke akun integrasi pengadaan.
    - Transaksi biaya aktual proyek dalam Dataverse.  Transaksi ini diproses lebih lanjut menggunakan [jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Mem-posting jurnal ini akan memindahkan jumlah tersebut dari akun integrasi pengadaan ke akun biaya proyek. 
    - Pembelian yang ditagihkan ke pelanggan proyek menggunakan metode penagihan waktu dan bahan. Selain itu, transaksi penjualan belum ditagih dibuat untuk pembelian di Dataverse. Daftar harga produk di Dataverse digunakan untuk harga penjualan dan jumlah transaksi penjualan belum tertagih.

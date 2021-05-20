---
title: Beli bahan non-stok dengan faktur vendor tertunda
description: Laporan topik menjelaskan cara mencatat faktur vendor yang tertunda.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880654"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>Beli bahan non-stok dengan faktur vendor tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Sebagai perusahaan yang mendapatkan bahan non-stok untuk proyek, biayanya dapat dengan segera dicatat terhadap proyek. 

Contohnya, Contoso Robotics US sedang melakukan proyek pembaruan perlengkapan dan memerlukan lisensi perangkat lunak. Lisensi ini diperoleh dari vendor pihak ketiga.  Menggunakan Dynamics 365 Finance, petugas utang dagang mencatat dokumen faktur vendor yang tertunda dan mengaitkan biaya lisensi secara langsung terhadap proyek pembaruan perlengkapan. 

> [!IMPORTANT]
> Sebelum Anda menggunakan fungsi yang dijelaskan di topik ini, lihat dan terapkan konfigurasi yang diperlukan. Untuk informasi lebih lanjut, lihat [Mengaktifkan materi non-stok dan faktur vendor yang tertunda](configure-materials-nonstocked.md). 

## <a name="post-a-project-related-pending-vendor-invoice"></a>Posting faktur vendor tertunda terkait proyek 

Faktur vendor yang tertunda dapat direkam pada halaman **faktur vendor tertunda** (**utang dagang** > **Faktur** > **Faktur vendor tertunda**). Selesaikan langkah-langkah berikut untuk memposting faktur vendor tertunda terkait proyek:

1. Buka **utang dagang** > **Faktur**, lalu pilih **Baru**. 
2. Pada bidang **Akun faktur**, pilih vendor dan pada bidang **Nomor**, masukkan identifikasi faktur vendor.
3. Tambahkan baris ke faktur vendor dan di bidang **Nomor Item**, pilih item non-stok yang dibeli dari vendor. 

    > [!NOTE]
    > Baris faktur vendor yang didasarkan pada kategori pengadaan tidak dapat dicatat terhadap proyek. 
    
5. Tambahkan kuantitas yang dibeli. Sistem akan mengisi harga per unit berdasarkan konfigurasi harga item yang tidak distok. 
6. Verifikasikan jumlah total dan rincian lainnya yang diperlukan di baris.
7. Pada detail baris, pada tab **Proyek**, pilih ID proyek untuk mencatat item ini.
8. Atau pilih nomor aktivitas, lalu perbarui kategori proyek dan properti baris.
9. Posting faktur vendor yang tertunda. Saat faktur diposting, sistem mencatat:
    
    - Jumlah saldo vendor.
    - Jumlah Pajak Penjualan.
    - Biaya terhadap proyek dicatat ke akun integrasi pengadaan.
    - Transaksi aktual proyek di Dataverse. Transaksi ini diproses lebih lanjut menggunakan [jurnal Integrasi Project Operations](../project-accounting/project-operations-integration-journal.md). Mem-posting jurnal ini akan memindahkan jumlah tersebut dari akun integrasi pengadaan ke akun biaya proyek.

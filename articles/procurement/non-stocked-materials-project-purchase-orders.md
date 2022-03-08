---
title: Memesan bahan yang tidak memiliki persediaan untuk proyek menggunakan pesanan pembelian proyek
description: Topik ini menjelaskan cara memesan bahan yang tidak memiliki persediaan untuk proyek menggunakan pesanan pembelian proyek.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6e0307ad6474feef96fc8080877eccbbbc7259db
ms.sourcegitcommit: 2d96345fb3afc3b174530285f95271b5ccbdea03
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 09/29/2021
ms.locfileid: "7563026"
---
# <a name="order-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Memesan bahan yang tidak memiliki persediaan untuk proyek menggunakan pesanan pembelian proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Departemen Pengadaan di organisasi Anda dapat menggunakan [pesanan pembelian](/dynamics365/supply-chain/procurement/purchase-order-overview) untuk melacak pesanan barang dan jasa. Pesanan pembelian untuk materi non-persediaan dapat dikaitkan ke proyek. Membuat faktur pesanan pembelian ini akan merekam biaya proyek.

## <a name="prerequisites"></a>Prasyarat
Selesaikan langkah-langkah berikut untuk mengaktifkan fungsi pesanan pembelian proyek.

1. Di Dynamics 365 Finance, buka ruang kerja **manajemen fitur**.
2. Dalam daftar fitur, cari dan pilih fitur, **Aktifkan pesanan pembelian proyek pada Project Operations untuk skenario berbasis sumber daya/non-persediaan**.
3. Klik **Aktifkan**.
4. Konfigurasikan bahan yang tidak ada stok dan faktur vendor tertunda seperti dijelaskan dalam [Konfigurasikan bahan tanpa persediaan dan faktur vendor tertunda](configure-materials-nonstocked.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Membuat pesanan pembelian proyek dari daftar pesanan pembelian proyek

1. Di Finance, buka **Manajemen proyek dan akuntansi** > **Proyek** > **Semua Proyek**, lalu pilih proyek.
2. Pada Panel Tindakan, pada tab **Kelola**, di grup **Baru**, pilih **Tugas item** > **Pesanan pembelian**.
3. Pada halaman **Buat pesanan pembelian**, pilih vendor yang akan melakukan pemesanan pembelian, masukkan informasi lain bila diperlukan, lalu pilih **OK**.
4. Pada halaman **Pesanan pembelian**, di kisi **Baris pesanan Pembelian**, pilih **Tambah baris**.
5. Masukkan nomor item, kuantitas, unit, harga unit, dan informasi lainnya jika diperlukan.

    > [!NOTE]
    > Hanya item dan layanan non-stok yang dapat digunakan dengan pesanan pembelian proyek. Item persediaan dan kategori pengadaan tidak didukung.

6. Lanjutkan untuk menambahkan item sebagaimana diperlukan dan konfirmasikan pesanan pembelian.

    Penerimaan barang dan layanan dapat direkam dengan membuat dan memposting tanda terima produk.

    > [!NOTE]
    > Tanda terima produk tidak direkam ke aktual proyek di Microsoft Dataverse dan tidak mempengaruhi buku besar pembantu proyek.

    Setelah vendor mengirimkan faktur untuk item dan layanan pada pesanan pembelian, departemen pengadaan dapat membuat faktur untuk pesanan pembelian dengan masuk ke **Faktur** > **Buat** > **Faktur** pada Panel Tindakan. Untuk informasi lebih lanjut tentang faktur vendor yang tertunda, lihat [Membeli bahan tanpa stok menggunakan faktur vendor tertunda](pending-vendor-invoices.md).

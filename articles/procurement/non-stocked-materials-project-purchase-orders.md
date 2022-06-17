---
title: Memesan bahan yang tidak memiliki persediaan untuk proyek menggunakan pesanan pembelian proyek
description: Artikel ini menjelaskan bagaimana Anda dapat memesan bahan yang tidak ditebar untuk proyek menggunakan pesanan pembelian proyek.
author: sigitac
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fe24faa143869af2396f3b0f28aae31417cadda7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929816"
---
# <a name="order-procurement-categories-or-non-stocked-materials-for-a-project-using-project-purchase-orders"></a>Memesan kategori pengadaan atau bahan yang tidak ditebar untuk proyek menggunakan pesanan pembelian proyek

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Departemen Pengadaan di organisasi Anda dapat menggunakan [pesanan pembelian](/dynamics365/supply-chain/procurement/purchase-order-overview) untuk melacak pesanan barang dan jasa. Pesanan pembelian untuk kategori pengadaan atau bahan non-stok dapat dikaitkan dengan proyek. Membuat faktur pesanan pembelian ini akan merekam biaya proyek.

## <a name="prerequisites"></a>Prasyarat
Selesaikan langkah-langkah berikut untuk mengaktifkan fungsi pesanan pembelian proyek.

1. Di Dynamics 365 Finance, buka ruang **kerja Manajemen** Fitur.
2. Dalam daftar fitur, cari dan pilih fitur, **Aktifkan pesanan pembelian proyek pada Project Operations untuk skenario berbasis sumber daya/non-persediaan**.
3. Klik **Aktifkan**.
4. Konfigurasikan bahan yang tidak ada stok dan faktur vendor tertunda seperti dijelaskan dalam [Konfigurasikan bahan tanpa persediaan dan faktur vendor tertunda](configure-materials-nonstocked.md).
5. Konfigurasikan kategori pengadaan seperti yang dijelaskan dalam [Gunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda](configure-procurement-categories.md).

## <a name="create-a-project-purchase-order-from-the-project-purchase-order-list"></a>Membuat pesanan pembelian proyek dari daftar pesanan pembelian proyek

1. Di Finance, buka **Manajemen proyek dan akuntansi** > **Proyek** > **Semua Proyek**, lalu pilih proyek.
2. Pada Panel Tindakan, pada tab **Kelola**, di grup **Baru**, pilih **Tugas item** > **Pesanan pembelian**.
3. Pada halaman **Buat pesanan pembelian**, pilih vendor yang akan melakukan pemesanan pembelian, masukkan informasi lain bila diperlukan, lalu pilih **OK**.
4. Pada halaman **Pesanan pembelian**, di kisi **Baris pesanan Pembelian**, pilih **Tambah baris**.
5. Masukkan nomor barang atau kategori pengadaan, kuantitas, satuan, harga satuan, dan informasi lainnya yang sesuai.

    > [!NOTE]
    > Hanya kategori pengadaan, barang yang tidak ditebar, dan layanan yang dapat digunakan dengan pesanan pembelian proyek. Item yang ditebar tidak didukung.

6. Terus tambahkan item atau kategori pengadaan sesuai kebutuhan, dan konfirmasikan pesanan pembelian.

    Penerimaan barang dan layanan dapat direkam dengan membuat dan memposting tanda terima produk.

    > [!NOTE]
    > Tanda terima produk tidak direkam ke aktual proyek di Microsoft Dataverse dan tidak mempengaruhi buku besar pembantu proyek.

    Setelah vendor mengirimkan faktur untuk item dan layanan pada pesanan pembelian, departemen pengadaan dapat membuat faktur untuk pesanan pembelian dengan masuk ke **Faktur** > **Buat** > **Faktur** pada Panel Tindakan. Untuk informasi lebih lanjut tentang faktur vendor yang tertunda, lihat [Membeli bahan tanpa stok menggunakan faktur vendor tertunda](pending-vendor-invoices.md).

---
title: Gunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor tertunda
description: Artikel ini menjelaskan cara mengkonfigurasi kategori pengadaan yang dapat digunakan dengan pesanan pembelian proyek dan faktur vendor tertunda.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f71c6bfcd183613471a4cc10e16a5a54571fac31
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: id-ID
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028614"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Gunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Profesional pembelian dapat membuat dan mengelola katalog item dan layanan yang dapat digunakan dalam pesanan pembelian proyek dan faktur vendor tertunda. [Katalog perolehan](/dynamics365/supply-chain/procurement/procurement-catalogs) memberikan cara mudah untuk mengkategorikan pembelian tanpa harus mengkonfigurasi dan menggunakan katalog produk yang dirilis. Setiap kategori pembelian dapat dipetakan ke kategori proyek untuk transaksi waktu, pengeluaran, atau item. Setelah faktur vendor tertunda yang menggunakan kategori pengadaan diposting, sistem akan membuat entri waktu, pengeluaran, atau aktual proyek bahan, transaksi proyek, dan buku besar pembantu.

## <a name="minimum-version-requirements"></a>Persyaratan versi minimum

Versi berikut diperlukan untuk menggunakan kategori pengadaan dengan pesanan pembelian proyek untuk skenario berbasis non-stok/sumber daya Microsoft Dynamics 365 Project Operations:

- Versi solusi Project Operations Dataverse 4.41.0.45 atau yang lebih baru
- Versi Lingkungan keuangan dan operasi 10.0.26 atau yang lebih baru

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Jalankan peta penulisan ganda untuk dukungan kategori pengadaan

Pastikan pemetaan **Entitas ekspor baris faktur vendor proyek integrasi Project Operations msdyn\_projectvendorinvoicelines** menggunakan versi 1.0.0.4 atau lebih baru.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Aktifkan kunci fitur untuk kategori pengadaan

Ikuti langkah-langkah ini untuk mengaktifkan fungsi menggunakan kategori pembelian proyek menggunakan kategori pembelian proyek.

1. Di Dynamics 365 Finance, buka ruang kerja **Manajemen Fitur**.
1. Dalam daftar fitur, cari fitur **gunakan kategori pengadaan di Project Operations untuk skenario berbasis sumber daya/non-persediaan** dan pilih **Aktifkan**.

> [!IMPORTANT]
> Sebagai prasyarat, Anda juga harus mengaktifkan fitur **Aktifkan faktur vendor tertunda pada Project Operations untuk skenario berbasis sumber daya/non-persediaan**.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Memetakan kategori proyek dalam hierarki kategori pengadaan

Ikuti langkah-langkah berikut untuk memetakan kategori proyek ke kategori pengadaan dalam **hierarki kategori pengadaan**:

1. Buka kategori **pengadaan dan pembekalan \> kategori pengadaan**.
1. Pilih **Edit hierarki kategori**.
1. Pilih node hierarki kategori yang diinginkan, lalu pada tab **Tetapkan kategori proyek**, kaitkan node dengan kategori proyek dari kategori kategori **Waktu**, **Pengeluaran**, atau, **Item Proyek** (yakni kategori **Waktu Default** atau **Pengeluaran Default**).
1. Pilih **Simpan**.
1. Tutup halaman.

> [!NOTE]
> Memetakan kategori pengadaan ke kategori proyek bersifat opsional. Jika Kategori pengadaan tidak dipetakan, sistem akan menggunakan nilai yang diatur dalam bidang **item** di bagian **Default kategori proyek** pada tab **Project Operations pada Dynamics 365 Customer Engagement** di halaman **Parameter manajemen dan akuntansi proyek**.

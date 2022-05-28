---
title: Gunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda
description: Ini topik menjelaskan cara mengonfigurasi kategori pengadaan yang dapat digunakan dengan pesanan pembelian proyek dan faktur vendor yang tertunda.
author: sigitac
ms.date: 04/07/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: ee68d7906cb0c887c19a32363ec7fda547cb74bd
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: id-ID
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613335"
---
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Gunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Profesional pembelian dapat membuat dan memelihara katalog barang dan layanan yang dapat digunakan dalam pesanan pembelian proyek dan faktur vendor yang tertunda. [Katalog pengadaan](/dynamics365/supply-chain/procurement/procurement-catalogs) memberi Anda cara mudah untuk mengkategorikan pembelian tanpa harus mengkonfigurasi dan menggunakan katalog produk yang dirilis. Setiap kategori pengadaan dapat dipetakan ke kategori proyek untuk waktu, biaya, atau transaksi item. Setelah faktur vendor tertunda yang menggunakan kategori pengadaan diposting, sistem akan membuat waktu, biaya, atau aktual proyek material, transaksi proyek, dan entri subledger.

## <a name="minimum-version-requirements"></a>Persyaratan versi minimum

Versi berikut diwajibkan untuk menggunakan kategori pengadaan dengan pesanan pembelian proyek untuk skenario Microsoft Dynamics 365 Project Operations yang tidak terisi/berbasis sumber daya:

- Versi solusi Operasi Dataverse Proyek 4.41.0.45 atau versi lebih baru
- Lingkungan Keuangan dan Operasi versi 10.0.26 atau yang lebih baru

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Menjalankan peta dual-write untuk dukungan kategori pengadaan

Pastikan pemetaan untuk **proyek integrasi Operasi Proyek vendor faktur baris entitas ekspor msdyn\_ projectvendorinvoicelines** menggunakan versi 1.0.0.4 atau yang lebih baru.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Aktifkan kunci fitur untuk kategori pengadaan

Ikuti langkah-langkah ini untuk mengaktifkan fungsionalitas untuk menggunakan kategori pengadaan dengan pesanan pembelian proyek.

1. Di Dynamics 365 Finance, buka **ruang kerja manajemen** fitur.
1. Dalam daftar fitur, temukan **fitur Gunakan kategori pengadaan dalam Operasi Proyek untuk skenario** berbasis sumber daya/non-stok, lalu pilih **Aktifkan**.

> [!IMPORTANT]
> Sebagai prasyarat, Anda juga harus mengaktifkan **fitur Aktifkan faktur vendor yang tertunda pada Operasi Proyek untuk skenario** berbasis sumber daya/non-stok.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Memetakan kategori proyek dalam hierarki kategori Pengadaan

Ikuti langkah-langkah berikut untuk memetakan kategori proyek ke kategori pengadaan dalam **hierarki kategori** Pengadaan:

1. **Buka kategori \> Pengadaan dan pengadaan sumber**.
1. Pilih **Edit hierarki** kategori.
1. Pilih simpul hierarki kategori yang diinginkan, lalu, pada **tab Tetapkan kategori** proyek, kaitkan simpul dengan kategori proyek dari **kategori Waktu**, Pengeluaran**, atau **,Proyek** Item (yaitu, **kategori Default-Time** atau **Default-Expense**).
1. Pilih **Simpan**.
1. Tutup halaman.

> [!NOTE]
> Memetakan kategori pengadaan ke kategori proyek adalah opsional. Jika kategori pengadaan tidak dipetakan, sistem akan menggunakan nilai yang ditetapkan di **bidang Item** di **bagian default** kategori Proyek pada **operasi proyek pada dynamics 365 Tab Keterlibatan** pelanggan dari **halaman Parameter** manajemen proyek dan akuntansi.

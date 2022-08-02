---
title: Menggunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda
description: Artikel ini menjelaskan cara mengonfigurasi kategori pengadaan yang dapat digunakan dengan pesanan pembelian proyek dan faktur vendor yang tertunda.
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
# <a name="use-procurement-categories-with-project-purchase-orders-and-pending-vendor-invoices"></a>Menggunakan kategori pengadaan dengan pesanan pembelian proyek dan faktur vendor yang tertunda

_**Berlaku untuk:** Project Operations untuk skenario berbasis sumber daya/tanpa stok_

Profesional pembelian dapat membuat dan memelihara katalog barang dan layanan yang dapat digunakan dalam pesanan pembelian proyek dan faktur vendor yang tertunda. [Katalog pengadaan](/dynamics365/supply-chain/procurement/procurement-catalogs) memberi Anda cara mudah untuk mengkategorikan pembelian tanpa harus mengonfigurasi dan menggunakan katalog produk yang dirilis. Setiap kategori pengadaan dapat dipetakan ke kategori proyek untuk transaksi waktu, pengeluaran, atau item. Setelah faktur vendor tertunda yang menggunakan kategori pengadaan diposting, sistem akan membuat waktu, pengeluaran, atau aktual proyek material, transaksi proyek, dan entri subledger.

## <a name="minimum-version-requirements"></a>Persyaratan versi minimum

Versi berikut ini diperlukan untuk menggunakan kategori pengadaan dengan pesanan pembelian proyek untuk skenario Microsoft Dynamics 365 Project Operations yang tidak tersedia/berbasis sumber daya:

- Solusi Operasi Dataverse Proyek versi 4.41.0.45 atau yang lebih baru
- Lingkungan keuangan dan operasi versi 10.0.26 atau yang lebih baru

## <a name="run-dual-write-maps-for-procurement-category-support"></a>Jalankan peta tulis ganda untuk dukungan kategori pengadaan

Pastikan bahwa pemetaan untuk **project operations integration project vendor invoice line export entity msdyn\_ projectvendorinvoicelines** menggunakan versi 1.0.0.4 atau yang lebih baru.

## <a name="enable-the-feature-key-for-procurement-categories"></a>Mengaktifkan kunci fitur untuk kategori pengadaan

Ikuti langkah-langkah ini untuk mengaktifkan fungsionalitas untuk menggunakan kategori pengadaan dengan pesanan pembelian proyek.

1. Di Dynamics 365 Finance, buka ruang **kerja Manajemen** fitur.
1. Di daftar fitur, temukan **fitur Gunakan kategori pengadaan di Operasi Proyek untuk skenario** berbasis sumber daya/tidak tersedia, lalu pilih **Aktifkan**.

> [!IMPORTANT]
> Sebagai prasyarat, Anda juga harus mengaktifkan **fitur Aktifkan faktur vendor yang tertunda pada Operasi Proyek untuk skenario** berbasis sumber daya/tidak tersedia.

## <a name="map-project-categories-in-the-procurement-category-hierarchy"></a>Memetakan kategori proyek dalam hierarki kategori Pengadaan

Ikuti langkah-langkah berikut untuk memetakan kategori proyek ke kategori pengadaan dalam **hierarki kategori** Pengadaan:

1. Masuk ke **kategori \> Pengadaan dan pengadaan** Pengadaan.
1. Pilih **Edit hierarki** kategori.
1. Pilih node hierarki kategori yang diinginkan, lalu, pada **tab Tetapkan kategori** proyek, kaitkan node dengan kategori proyek dari **kategori Waktu**, **Beban**, atau, **Proyek** Item (yaitu, **kategori Default-Time** atau **Default-Expense**).
1. Pilih **Simpan**.
1. Tutup halaman.

> [!NOTE]
> Memetakan kategori pengadaan ke kategori proyek bersifat opsional. Jika kategori pengadaan tidak dipetakan, sistem akan menggunakan nilai yang ditetapkan di **bidang Item** di **bagian default** kategori Proyek pada **operasi proyek pada dynamics 365 Customer engagement** tab dari **halaman manajemen proyek dan parameter** akuntansi.
